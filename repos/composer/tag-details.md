<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `composer`

-	[`composer:2`](#composer2)
-	[`composer:2.2`](#composer22)
-	[`composer:2.2.27`](#composer2227)
-	[`composer:2.9`](#composer29)
-	[`composer:2.9.7`](#composer297)
-	[`composer:latest`](#composerlatest)

## `composer:2`

```console
$ docker pull composer@sha256:709a30cb521103db18992786f7fd747010ad8e24cf581817ddf3e53288d3d281
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
$ docker pull composer@sha256:a3df561dbdddfdb9832ec50f41c0e2f1d27445a67bd71415f05467fedbb2c3c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.2 MB (78237453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39f4699ce5525450650cad74ebb243efd73730fda6d6011a5d805089f9bc61ce`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:17:52 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:17:52 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:17:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:17:52 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:17:52 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:17:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:17:52 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:17:52 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 15 Apr 2026 20:17:52 GMT
ENV PHP_VERSION=8.5.5
# Wed, 15 Apr 2026 20:17:52 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Wed, 15 Apr 2026 20:17:52 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Wed, 15 Apr 2026 20:17:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 20:17:56 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:21:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 20:21:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:21:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 20:21:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 20:21:24 GMT
CMD ["php" "-a"]
# Wed, 15 Apr 2026 21:27:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Wed, 15 Apr 2026 21:27:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Wed, 15 Apr 2026 21:27:31 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 15 Apr 2026 21:27:31 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 15 Apr 2026 21:27:31 GMT
ENV COMPOSER_VERSION=2.9.7
# Wed, 15 Apr 2026 21:27:31 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Wed, 15 Apr 2026 21:27:31 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 21:27:31 GMT
WORKDIR /app
# Wed, 15 Apr 2026 21:27:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:27:31 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7575019b1e32c16a639f3988d9a63ff1c22c036099e3cb267ea5a97ba0fcb31b`  
		Last Modified: Wed, 15 Apr 2026 20:21:32 GMT  
		Size: 3.6 MB (3587447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba54b7e6d1307c692fb0f98a7bb785c3ae59fda44cbd8dc735eb6d32da25bb2`  
		Last Modified: Wed, 15 Apr 2026 20:21:32 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7367014229e0f5079d78d9d65f87aeb106ffa42ef3cacfdde5ccae68a710662d`  
		Last Modified: Wed, 15 Apr 2026 20:21:32 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c74770868277c77b3c7d8e5aa987ffc0183e76f8a003e5ee3e5662475be115`  
		Last Modified: Wed, 15 Apr 2026 20:21:33 GMT  
		Size: 14.4 MB (14379186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f1108694a36c05d3950260f3491806016ec3ab9ba1da15154bda777858d1eb`  
		Last Modified: Wed, 15 Apr 2026 20:21:33 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e321e76cc80892e05feb16337063a65959f21cd03508ea9f6dd1316bd2bfee6`  
		Last Modified: Wed, 15 Apr 2026 20:21:34 GMT  
		Size: 22.5 MB (22528821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2af3ca59c901474266aab6d50192f869e507a229be1b7493e312a32fac0dff9`  
		Last Modified: Wed, 15 Apr 2026 20:21:33 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b12841ff7824946e17f91cf31b444d9a97e15dc30fa55d79e32ae0c00cf27f1`  
		Last Modified: Wed, 15 Apr 2026 20:21:34 GMT  
		Size: 23.4 KB (23395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e55827933a329097ef03bab9834f516b064faf5b72b18d080e967055a42003`  
		Last Modified: Wed, 15 Apr 2026 21:27:42 GMT  
		Size: 32.8 MB (32828568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2933ad071631f9ce3470578aecae812618fd37d7004987532866b0359f6b6de0`  
		Last Modified: Wed, 15 Apr 2026 21:27:41 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d821667065611cf0d7b4bf7f6d8857b118bfd703fe486289b37884a8edbd61`  
		Last Modified: Wed, 15 Apr 2026 21:27:41 GMT  
		Size: 1.0 MB (1020986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae94261b1892c1af044280991b4f2a5dd150a791ec2eeef5af1ea6d3094479e5`  
		Last Modified: Wed, 15 Apr 2026 21:27:41 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb435422e01857a05128024eb0629a6c60655c0d3b45442ea0bc469f1bbd191`  
		Last Modified: Wed, 15 Apr 2026 21:27:42 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:e85e044ddbc3f14041ddacfb9398391fc8292baa3673ee4c95d5b809632bc41f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2209324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4c877852d538421f4a82316e63e564b40bc167997b6947ce7c9b36533714614`

```dockerfile
```

-	Layers:
	-	`sha256:b9fed10922f5326c3cb699a3c5c5bfb4d7c68743354358d37b16875c5fdd6803`  
		Last Modified: Wed, 15 Apr 2026 21:27:41 GMT  
		Size: 2.2 MB (2178657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:615752e487f6d65b8ad402d079106fe3c4610a7aee9abb3e9350d78067b4501f`  
		Last Modified: Wed, 15 Apr 2026 21:27:41 GMT  
		Size: 30.7 KB (30667 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; arm variant v6

```console
$ docker pull composer@sha256:5f618ede41609642ab0415bf163302848fbba617512b9f3bcb4c81d65aea6016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74743627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e102830ff670832c4941a947728bd57ef6a228b56943b1d8d452c9c6f1e395d8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:19:04 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:19:04 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:19:04 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:19:04 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:19:05 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:19:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:19:05 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:19:05 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:19:05 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 15 Apr 2026 20:19:05 GMT
ENV PHP_VERSION=8.5.5
# Wed, 15 Apr 2026 20:19:05 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Wed, 15 Apr 2026 20:19:05 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Wed, 15 Apr 2026 20:19:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 20:19:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:22:18 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 20:22:18 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:22:19 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 20:22:19 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 20:22:19 GMT
CMD ["php" "-a"]
# Wed, 15 Apr 2026 21:22:04 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Wed, 15 Apr 2026 21:22:04 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Wed, 15 Apr 2026 21:22:27 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 15 Apr 2026 21:22:27 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 15 Apr 2026 21:22:27 GMT
ENV COMPOSER_VERSION=2.9.7
# Wed, 15 Apr 2026 21:22:27 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Wed, 15 Apr 2026 21:22:27 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 21:22:27 GMT
WORKDIR /app
# Wed, 15 Apr 2026 21:22:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:22:27 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1d167fc497e35df23f81ef7d507ee40c904d148d7c5e239db360263ce1228f`  
		Last Modified: Wed, 15 Apr 2026 20:22:24 GMT  
		Size: 3.5 MB (3543048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7893272fc58b639fcb274b9cdac380a99a02b7fec1370991d7043a8d745ee731`  
		Last Modified: Wed, 15 Apr 2026 20:22:24 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b5e2d5fa2204fe8d000332835281efd2beeb4e2b1233fda8377dc9fb8d273da`  
		Last Modified: Wed, 15 Apr 2026 20:22:24 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a237864e95f05b7c9e05c3272f303c8616f39f4b50a113166e6e93f5d6eb2867`  
		Last Modified: Wed, 15 Apr 2026 20:22:25 GMT  
		Size: 14.4 MB (14379195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d6cac0622b9c4733975c694271b5cfe4e9e251f5a29439c27931c4334db09d`  
		Last Modified: Wed, 15 Apr 2026 20:22:25 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a5b1613ded78de2dd5fc3a3cbb57bc91cb6f35c9bf29e262676641888899d35`  
		Last Modified: Wed, 15 Apr 2026 20:22:26 GMT  
		Size: 19.5 MB (19534950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7326187f367c7e04eed9c7cfd2fd94e264bdf5da29600b25762d89f896ee8df`  
		Last Modified: Wed, 15 Apr 2026 20:22:26 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf7aab9524160d3a6dc903858b7d9fc9d77b6f4a09bb6c0cdb0b86eca60acbc`  
		Last Modified: Wed, 15 Apr 2026 20:22:26 GMT  
		Size: 23.2 KB (23204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7338db7ab2e6da871e9ca18bf6e41db656dc01552305f5ea294acd98e45f2ff2`  
		Last Modified: Wed, 15 Apr 2026 21:22:35 GMT  
		Size: 32.7 MB (32665496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acff7d213b0f5a23ec528c0624a11975e61306f0ef4705e003a9109c922c9aaf`  
		Last Modified: Wed, 15 Apr 2026 21:22:34 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ab1a1cc99508981bda26983105462a9a3ee15eae1e24e6da36767b441c2244`  
		Last Modified: Wed, 15 Apr 2026 21:22:34 GMT  
		Size: 1.0 MB (1021023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cff2f6c2aff71864717c706d9c7e23510750ed143e2938cb19d5fdafff8be79`  
		Last Modified: Wed, 15 Apr 2026 21:22:34 GMT  
		Size: 416.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2da733922c6146907c3b3634c5c450c96e0638edddca77a676b7cd813427f9`  
		Last Modified: Wed, 15 Apr 2026 21:22:35 GMT  
		Size: 91.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:1eb3fc19c61b35b8a872d9323204996b304beb4dc10e4d11dfd6b5c14cc219a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:784a99b9ab8555f39e0aa608545bfc075b883ab06336eacb31db1b89b4961c24`

```dockerfile
```

-	Layers:
	-	`sha256:1e8a701178ca230dc13cbb78d4e4d281f47957950cbb2e2298d741398449207b`  
		Last Modified: Wed, 15 Apr 2026 21:22:33 GMT  
		Size: 30.6 KB (30557 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; arm variant v7

```console
$ docker pull composer@sha256:582284655bf553416dbce90c395b4dc89da3a7edc9da012ec6e01407c1430ed9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.6 MB (71571453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f9ac974387fafeac611e90eeb97b0514811d16f37141c1796d8eebb9f19295e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:18:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:18:22 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:18:22 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:18:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:18:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:18:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:18:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:18:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:18:22 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 15 Apr 2026 20:18:22 GMT
ENV PHP_VERSION=8.5.5
# Wed, 15 Apr 2026 20:18:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Wed, 15 Apr 2026 20:18:22 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Wed, 15 Apr 2026 20:18:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 20:18:26 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:21:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 20:21:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:21:34 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 20:21:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 20:21:34 GMT
CMD ["php" "-a"]
# Wed, 15 Apr 2026 21:32:22 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Wed, 15 Apr 2026 21:32:22 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Wed, 15 Apr 2026 21:32:44 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 15 Apr 2026 21:32:44 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 15 Apr 2026 21:32:44 GMT
ENV COMPOSER_VERSION=2.9.7
# Wed, 15 Apr 2026 21:32:44 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Wed, 15 Apr 2026 21:32:44 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 21:32:45 GMT
WORKDIR /app
# Wed, 15 Apr 2026 21:32:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:32:45 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40243011337e75e1e1aba1a01eff0f25c670f2784f31a19fe3ceeb28d9cbb386`  
		Last Modified: Wed, 15 Apr 2026 20:21:41 GMT  
		Size: 3.3 MB (3343352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289d25cb3dc6bf4d1acfe704c1d05a812b84cbfe26b06c6e9a423f281efcfd64`  
		Last Modified: Wed, 15 Apr 2026 20:21:41 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457ef191b478c4407082d1c51e695feac2f4425353d54d5d6737f8e3aede1686`  
		Last Modified: Wed, 15 Apr 2026 20:21:41 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef8f20263bc5a42b03699b180b432cb94cb313e98aed5a4238024d8cd3f252ad`  
		Last Modified: Wed, 15 Apr 2026 20:21:41 GMT  
		Size: 14.4 MB (14379203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654a3e48df9d037dc7d582e4d7e753ead3d5f55b619c07d29f0f2701eabf4657`  
		Last Modified: Wed, 15 Apr 2026 20:21:43 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00b79e1670ab000b58c3fa612bf97d881357d5a02a37a01aab4448a263a56aa`  
		Last Modified: Wed, 15 Apr 2026 20:21:43 GMT  
		Size: 18.4 MB (18430268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:670c3d79616cd5914f7e4d0d94505d6570f152e3fab437081ba1b2499bf253df`  
		Last Modified: Wed, 15 Apr 2026 20:21:43 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773025cf5591ee7e2a345d9e429358f0269bd41230fb2da781a05eb990ef0386`  
		Last Modified: Wed, 15 Apr 2026 20:21:43 GMT  
		Size: 23.2 KB (23204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acebb0a04354316add548495911389085f450934caee74f83d543b9e72b2d05e`  
		Last Modified: Wed, 15 Apr 2026 21:32:54 GMT  
		Size: 31.1 MB (31096001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a09a4d2f176f1708944c561d076f811601d10ce9c12f67f368beb5f33e872e0`  
		Last Modified: Wed, 15 Apr 2026 21:32:53 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4554ab557c57e190e9a9c96595d8f20842cdf6c58419124406570b03fb325ec8`  
		Last Modified: Wed, 15 Apr 2026 21:32:54 GMT  
		Size: 1.0 MB (1011452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba1c93167f863ddcc1d5c2653b03c6a8642c2fd9559327b73ed8624251ec144`  
		Last Modified: Wed, 15 Apr 2026 21:32:54 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c681ef1dc9504c4c3f4ad0cf3ffc7c285a57f04dbacae219663ef575ca6acf`  
		Last Modified: Wed, 15 Apr 2026 21:32:55 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:32d0c9b1e4d5d571639eb8de3fd2347a367f829d380db08ff8dbf370f5b11cc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2209101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23ebcb2c2afc717904235ca8d45b56e040e43ae27f90d904adef6de85485e0c1`

```dockerfile
```

-	Layers:
	-	`sha256:1ea500bcc75e9906fcbd4ac18fb9f32b00e2f232209a8695dbdd04027eae30b1`  
		Last Modified: Wed, 15 Apr 2026 21:32:54 GMT  
		Size: 2.2 MB (2178328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d85d9fe7060afbbf94f473725bfe33d128da115ed642a56a0a3c11dc35b8ad8a`  
		Last Modified: Wed, 15 Apr 2026 21:32:53 GMT  
		Size: 30.8 KB (30773 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:02cc0a1729b9f75734a6f1789ad59fa90c54bdb84566b2c7b564f7eaafd5c368
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77892271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b9aa3f48599c920e9268b74581f5d0d24a2eca014342e24e60e1d70f8bfb5ae`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:21 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:16:21 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:16:21 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:16:21 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:16:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:16:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:16:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:16:21 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:16:21 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 15 Apr 2026 20:16:21 GMT
ENV PHP_VERSION=8.5.5
# Wed, 15 Apr 2026 20:16:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Wed, 15 Apr 2026 20:16:21 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Wed, 15 Apr 2026 20:16:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 20:16:25 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:19:57 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 20:19:57 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:19:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 20:19:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 20:19:58 GMT
CMD ["php" "-a"]
# Wed, 15 Apr 2026 21:40:09 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Wed, 15 Apr 2026 21:40:09 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Wed, 15 Apr 2026 21:40:29 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 15 Apr 2026 21:40:29 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 15 Apr 2026 21:40:29 GMT
ENV COMPOSER_VERSION=2.9.7
# Wed, 15 Apr 2026 21:40:29 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Wed, 15 Apr 2026 21:40:29 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 21:40:29 GMT
WORKDIR /app
# Wed, 15 Apr 2026 21:40:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:40:29 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e4c5bcbf8c3068a7d4c178cdd5132463fa53adf8c55efe0d5a02126d958e69`  
		Last Modified: Wed, 15 Apr 2026 20:20:06 GMT  
		Size: 3.6 MB (3596134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c0edc310dc19501413b5668245bc984741c4ac5a3219932a74e83fb33b6f94`  
		Last Modified: Wed, 15 Apr 2026 20:20:02 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d665080207d06b6b7246d46376f6ec0b3a5d072b47f01ab3fe89eb95ea0b9310`  
		Last Modified: Wed, 15 Apr 2026 20:20:02 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e92dbfc45c4b506749680c4bded773db9170a5c594ae07c33aa938ac9b46a1c`  
		Last Modified: Wed, 15 Apr 2026 20:20:07 GMT  
		Size: 14.4 MB (14379192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da631dfa865e2d394e47bb93c95f041d309af42b22cd597826fab10299773bc`  
		Last Modified: Wed, 15 Apr 2026 20:20:03 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0885f624969f9911f18390a16714e49ddcba2831ee9c8002d794ee56d8ca9ca8`  
		Last Modified: Wed, 15 Apr 2026 20:20:07 GMT  
		Size: 21.7 MB (21697840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e202517af7cb78a86ff7f8b255ca452261912c8830cf0b7e352386b5c5472454`  
		Last Modified: Wed, 15 Apr 2026 20:20:05 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4062a55681ba2c31424930678c18614b1e9e0eb63f551ee5faaa3857658f4f0`  
		Last Modified: Wed, 15 Apr 2026 20:20:07 GMT  
		Size: 23.2 KB (23209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247694cf5276fc930925fbd3c766f23524e3c168100355ab0759b2996481c9fe`  
		Last Modified: Wed, 15 Apr 2026 21:40:39 GMT  
		Size: 33.0 MB (32971344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd2df09b94d664b93dffeea3fcc3ec248ab74647c5a4214efe19bfb47fcb05a8`  
		Last Modified: Wed, 15 Apr 2026 21:40:38 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ddb215ec4272be553f5bc3174320405b2f1a91262a8dcef2e0a86a9e49ee716`  
		Last Modified: Wed, 15 Apr 2026 21:40:38 GMT  
		Size: 1.0 MB (1019831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf4152796a067e6883c8510bc549ef6efa7a2938ae8a777ac16b9ce0064b7cb`  
		Last Modified: Wed, 15 Apr 2026 21:40:38 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2e497f91b5d80958253e7e10d4c15d00acc6326888e106b429a9c5308f89fe`  
		Last Modified: Wed, 15 Apr 2026 21:40:39 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:fe7799a0766fcb90d3eee27476e71e060d8359ba6a1af526e40143a0b717c9fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2208959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c81eae5c2a8041b04dcb4644dca7f3e06622961ff2e597b7542f07cfbf49fb89`

```dockerfile
```

-	Layers:
	-	`sha256:b2e0891d2073a415183d3e4d591453fd999ea34870c33d681160d6f91ac3e8e6`  
		Last Modified: Wed, 15 Apr 2026 21:40:38 GMT  
		Size: 2.2 MB (2178158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a29947e152eea3d30a8612f8ec8d06ba8dac35f21c5319fc14e247056d17a8a`  
		Last Modified: Wed, 15 Apr 2026 21:40:38 GMT  
		Size: 30.8 KB (30801 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; 386

```console
$ docker pull composer@sha256:5059aa7f8aeb8fd9ad00e166cfc4504d01b632d5c987150dfde3e7167b11e492
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82480079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05da3dd80cd6d3c296bb9f77ac1d48716d0282b354fc840118af6947f2db6dbd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Fri, 10 Apr 2026 00:13:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 10 Apr 2026 00:13:16 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 10 Apr 2026 00:13:16 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 10 Apr 2026 00:13:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 10 Apr 2026 00:13:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 10 Apr 2026 00:13:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 10 Apr 2026 00:13:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 10 Apr 2026 00:13:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 10 Apr 2026 00:13:16 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 10 Apr 2026 00:13:16 GMT
ENV PHP_VERSION=8.5.5
# Fri, 10 Apr 2026 00:13:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Fri, 10 Apr 2026 00:13:16 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Fri, 10 Apr 2026 00:13:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 10 Apr 2026 00:13:20 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 00:16:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 10 Apr 2026 00:16:53 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 00:16:54 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 10 Apr 2026 00:16:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 10 Apr 2026 00:16:54 GMT
CMD ["php" "-a"]
# Tue, 14 Apr 2026 18:19:28 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Apr 2026 18:19:28 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Apr 2026 18:19:47 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Apr 2026 18:19:47 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Apr 2026 18:19:47 GMT
ENV COMPOSER_VERSION=2.9.7
# Tue, 14 Apr 2026 18:19:47 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Apr 2026 18:19:48 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Apr 2026 18:19:48 GMT
WORKDIR /app
# Tue, 14 Apr 2026 18:19:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Apr 2026 18:19:48 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d2062b0536d4d6a1543e3a6bfd55452c7706979a7def0ad5ff0f3e183f183d`  
		Last Modified: Fri, 10 Apr 2026 00:17:02 GMT  
		Size: 5.9 MB (5909460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb9b53f46bb29bde8242534cc51035c71b65536a0a0acada6428f7a8ba0889c`  
		Last Modified: Fri, 10 Apr 2026 00:17:02 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab50b39601a88f935ec690047331c7481ff9b7ae2bb959cfc4cc98313c492986`  
		Last Modified: Fri, 10 Apr 2026 00:17:02 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92225e063d6f653398ed45adcff1579a3a3cf3ccbe764a4bb5b301283ee3b2ee`  
		Last Modified: Fri, 10 Apr 2026 00:17:02 GMT  
		Size: 14.4 MB (14379292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ccaecce131db93828716f892d3ad6e523dec70db239cc1bed3bb5394e8396c`  
		Last Modified: Fri, 10 Apr 2026 00:17:03 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e4efa73be7dce94cd5df6088620edcd50156eafe81c782274c129a7a3e191d`  
		Last Modified: Fri, 10 Apr 2026 00:17:04 GMT  
		Size: 23.4 MB (23438953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab8684032f9c15ecd79788e50ca55f90486d5bf79b5b3a24018772984e7a1cb5`  
		Last Modified: Fri, 10 Apr 2026 00:17:04 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba72ff6334ace2c9a0d737cdf3c0fa9f61f267a07af45bf21e2ff77820277e5`  
		Last Modified: Fri, 10 Apr 2026 00:17:04 GMT  
		Size: 23.6 KB (23625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb92bca6a7200abd5ed57acbc2406d1b631ce897e9fcb8321df6d6ad30cb6114`  
		Last Modified: Tue, 14 Apr 2026 18:19:58 GMT  
		Size: 33.4 MB (33354023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3acb4361787726cd8ad52c3d9467b84e1d1aa7dfe6414e7e3be8d2816cc76617`  
		Last Modified: Tue, 14 Apr 2026 18:19:57 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9241059ece99827922266cdf5f4d2003877d75ddf68699cd4c70ce7987a21836`  
		Last Modified: Tue, 14 Apr 2026 18:19:57 GMT  
		Size: 1.7 MB (1682879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69641c04f229a2ab6016f07abf23bea732612f28baf219fd9fcf0c899d7617e5`  
		Last Modified: Tue, 14 Apr 2026 18:19:42 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67f4289f14f4bb7e5b1629ac4c78856e0c3b60c94f52f95daa671e1a219d5df8`  
		Last Modified: Tue, 14 Apr 2026 18:19:59 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:c254802094079f1308563379ad369533970752e4908cfa224d9e97811d3d39ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2211056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4ce198e58e85ea5dc923b1568aaa064676ae0112aaf5ac90c6cc3e58fdc12bf`

```dockerfile
```

-	Layers:
	-	`sha256:340334093e4da71051f77042453963dbc6f4fd36456e9b67f499e0b94970d025`  
		Last Modified: Tue, 14 Apr 2026 18:19:57 GMT  
		Size: 2.2 MB (2180425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47bf377a779ae13fd18570cc75e3fe8f0a691c683d330c3c388994b1f8641121`  
		Last Modified: Tue, 14 Apr 2026 18:19:57 GMT  
		Size: 30.6 KB (30631 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; ppc64le

```console
$ docker pull composer@sha256:6b0debe85067d180c3dca5be15549aa709e405e5c6da97f106b302afa0be7b3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 MB (96713081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d658b5ad399d03987449b91b37ae36fb531e2591aba9b560f1469876bcd1472`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Thu, 12 Mar 2026 23:53:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Mar 2026 23:53:02 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Mar 2026 23:53:02 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Mar 2026 23:53:02 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Mar 2026 23:53:02 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Mar 2026 23:53:02 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Mar 2026 23:53:02 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Mar 2026 23:53:02 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Mar 2026 23:53:02 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 12 Mar 2026 23:53:02 GMT
ENV PHP_VERSION=8.5.5
# Thu, 12 Mar 2026 23:53:02 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Thu, 12 Mar 2026 23:53:02 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Thu, 09 Apr 2026 22:33:42 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 09 Apr 2026 22:33:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:38:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 09 Apr 2026 22:38:29 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:38:30 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 09 Apr 2026 22:38:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 09 Apr 2026 22:38:30 GMT
CMD ["php" "-a"]
# Fri, 10 Apr 2026 00:21:05 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 10 Apr 2026 00:21:07 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Apr 2026 18:19:02 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Apr 2026 18:19:02 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Apr 2026 18:19:02 GMT
ENV COMPOSER_VERSION=2.9.7
# Tue, 14 Apr 2026 18:19:02 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Apr 2026 18:19:05 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Apr 2026 18:19:09 GMT
WORKDIR /app
# Tue, 14 Apr 2026 18:19:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Apr 2026 18:19:09 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7db1cc7b26f64d5de44e75f81962c30dead7dbc1dae3ebb93d0dc3d0cea721a`  
		Last Modified: Thu, 12 Mar 2026 23:58:51 GMT  
		Size: 3.8 MB (3768852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4a23ff5963c3f844b77db123769c733318f6ad54386c9f63e356424059470b`  
		Last Modified: Thu, 12 Mar 2026 23:58:51 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a071b7623ea30b2e8950858971a7e7838856db9c469a46b6305dcd619d0531fc`  
		Last Modified: Thu, 12 Mar 2026 23:58:51 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d012a34014d339e95156eab3252cc22fbae82a4670be3766b110c04e96ff1a17`  
		Last Modified: Thu, 09 Apr 2026 22:38:45 GMT  
		Size: 14.4 MB (14379301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8b7c5afa56dcdf0f01aaba59b305697db6b72603309ba573605f5fcd422fc0`  
		Last Modified: Thu, 09 Apr 2026 22:38:45 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1971acbe5d44b0f37d3698908a5766cea69f16ef4c4472ca8a30f5d48eec93ec`  
		Last Modified: Thu, 09 Apr 2026 22:38:46 GMT  
		Size: 23.1 MB (23118163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ee71922b29fe2228fde987804ee785c857383e7941a35e885bb5f06b7c3aba`  
		Last Modified: Thu, 09 Apr 2026 22:38:45 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fbefb03f1cf2736ed7b9f334b7e8f2f16dbedad1876c833ba4682b99ca9f99a`  
		Last Modified: Thu, 09 Apr 2026 22:38:46 GMT  
		Size: 23.4 KB (23442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db29015527299944deffccc76c5bfb597208be66aea62b09cf37a0cef1bb364e`  
		Last Modified: Fri, 10 Apr 2026 00:22:19 GMT  
		Size: 34.2 MB (34177434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972a41e22feca9d4bfcc298283918766cb03ebb7dd146ebbded895c8b431c973`  
		Last Modified: Fri, 10 Apr 2026 00:22:17 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efaac84e88b2da4e607702934bba5a10ee9d45974d858538b478a29b89842e33`  
		Last Modified: Tue, 14 Apr 2026 18:19:37 GMT  
		Size: 17.4 MB (17411381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e029883ecefeeaf8733085cd8e526dfbbca7e594b984c759f9d554d542181f0`  
		Last Modified: Tue, 14 Apr 2026 18:19:37 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebb4782c2d3dfa3ac371b8a44cd1f51c8cca8d476ce08683daefb52097b9bf7`  
		Last Modified: Tue, 14 Apr 2026 18:19:37 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:b96e3b5bce750eb3282de808dd8aafbf3a051c5f80e3f716df031de690321657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2211215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5342929d05c922fd2d787aa2179debfaee17cdccf8781a7e329e1d3d484d07f1`

```dockerfile
```

-	Layers:
	-	`sha256:fc050012567990ae6904da1426da82a6cc21eeb168d8d2fa9b316fe513258f54`  
		Last Modified: Tue, 14 Apr 2026 18:19:37 GMT  
		Size: 2.2 MB (2180498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dc4ab7a528f883fc6476f1d2c72c9454b32b1cd4fefe0ac8fb1da3fec8e6c44`  
		Last Modified: Tue, 14 Apr 2026 18:19:37 GMT  
		Size: 30.7 KB (30717 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; riscv64

```console
$ docker pull composer@sha256:600f68dee998197590fbadd5f49b007afb10faf4f15287a315a79fa198635908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.1 MB (78108283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abd844ec36780aac229ca2fdb372bcc3b96fc3ad9a0c8de0b25c8458b53af256`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 09:13:06 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 28 Jan 2026 09:13:06 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 28 Jan 2026 09:13:06 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 28 Jan 2026 09:13:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 28 Jan 2026 09:13:07 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 28 Jan 2026 09:13:07 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_VERSION=8.5.5
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Fri, 10 Apr 2026 09:29:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 10 Apr 2026 09:29:21 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 10:28:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 10 Apr 2026 10:28:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 10:28:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 10 Apr 2026 10:28:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 10 Apr 2026 10:28:33 GMT
CMD ["php" "-a"]
# Sun, 12 Apr 2026 09:33:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Sun, 12 Apr 2026 09:33:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Apr 2026 18:22:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Apr 2026 18:22:48 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Apr 2026 18:22:48 GMT
ENV COMPOSER_VERSION=2.9.7
# Tue, 14 Apr 2026 18:22:48 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Apr 2026 18:22:48 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Apr 2026 18:22:48 GMT
WORKDIR /app
# Tue, 14 Apr 2026 18:22:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Apr 2026 18:22:48 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d64a68485fdb9ab2ec4159ac3e04e0bb79d9f1d037e580e928ca2b9604180f`  
		Last Modified: Wed, 28 Jan 2026 10:13:59 GMT  
		Size: 3.7 MB (3741000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b030c1b113432578231e8fe7c8a1bc913f2dc5dcba512e805fa9ab07768c9bd4`  
		Last Modified: Wed, 28 Jan 2026 10:13:58 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32a0e9bcb36b34307b4eada1f50c1cd4244d43d19ee57d962818dcb0ff0b110`  
		Last Modified: Wed, 28 Jan 2026 10:13:58 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20501e9e3d17b72af47b7d522d0c369998be222ed66ed9070ed2cbc45e500ca7`  
		Last Modified: Fri, 10 Apr 2026 10:29:42 GMT  
		Size: 14.4 MB (14379290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f7fa0bbe8ea35a7aeededb6a1c62d4e192d88a3cbaa6a9ac613390cef5f797e`  
		Last Modified: Fri, 10 Apr 2026 10:29:38 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c00b6c348638ca2fb138534e98df3a83c5788350e7f682c5dab61388d5988a1`  
		Last Modified: Fri, 10 Apr 2026 10:29:43 GMT  
		Size: 20.8 MB (20772153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf32615937490fdbee93796b59955ce07e051f019b76917819692421da228ef`  
		Last Modified: Fri, 10 Apr 2026 10:29:38 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491cab84c5a842c690a34c22c4cfe20f23d7b27019ca9d80e387fd23ef96828d`  
		Last Modified: Fri, 10 Apr 2026 10:29:39 GMT  
		Size: 23.3 KB (23349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e865e7a35bee8605e802d4714eef1a4cd079ed0b68a414c076e698d97cfbedd6`  
		Last Modified: Sun, 12 Apr 2026 09:38:57 GMT  
		Size: 31.3 MB (31300012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:670c7192db5936f38910b865b3f6746b70a4b2523b1e25db7d274900db0fca4f`  
		Last Modified: Sun, 12 Apr 2026 09:38:52 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849fae3a43556661d0d79306c12a48046432673ac49917b14937307d36a24458`  
		Last Modified: Tue, 14 Apr 2026 18:24:04 GMT  
		Size: 4.3 MB (4302324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01efda7965080036e2b76754ef2276308322ed2394f97d073063348bded60a09`  
		Last Modified: Tue, 14 Apr 2026 18:24:03 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5997a67e70609c3ecf2d0c94e158584b948e5f7e90a85dd896325c6db3a7ed`  
		Last Modified: Tue, 14 Apr 2026 18:22:53 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:55155328eaf6b4a8b732344c31723c0e2e7026edb1151e056f7260b0c23793eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2210153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baabb88b9e58574b8449e58ff8e49bdd472dd2b4eac9aec0cd90224e32a110f8`

```dockerfile
```

-	Layers:
	-	`sha256:14f5989ff5313284e35f85efde25d95ba6cf9e9207afa6539c85ba5cfebf3e22`  
		Last Modified: Tue, 14 Apr 2026 18:24:03 GMT  
		Size: 2.2 MB (2179439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d12e5da0f5f9cce27555430a40d6dc9e18c54764d62f13fed79c09c33cdd6769`  
		Last Modified: Tue, 14 Apr 2026 18:24:03 GMT  
		Size: 30.7 KB (30714 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; s390x

```console
$ docker pull composer@sha256:1f94545e77b0a527f486fd42ce1a3ed8e347a32e951166e75e667c9a8b9c5055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93248850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc4e000a0f721a102b5621d79143082167c85fe36cbab314eff8808e5f343a36`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Mar 2026 23:37:17 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Mar 2026 23:37:17 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Mar 2026 23:37:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Mar 2026 23:37:17 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHP_VERSION=8.5.5
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Thu, 09 Apr 2026 22:21:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 09 Apr 2026 22:21:35 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:27:00 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 09 Apr 2026 22:27:00 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:27:01 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 09 Apr 2026 22:27:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 09 Apr 2026 22:27:01 GMT
CMD ["php" "-a"]
# Thu, 09 Apr 2026 23:18:42 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 09 Apr 2026 23:18:42 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Apr 2026 18:19:36 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Apr 2026 18:19:36 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Apr 2026 18:19:36 GMT
ENV COMPOSER_VERSION=2.9.7
# Tue, 14 Apr 2026 18:19:36 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Apr 2026 18:19:36 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Apr 2026 18:19:36 GMT
WORKDIR /app
# Tue, 14 Apr 2026 18:19:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Apr 2026 18:19:36 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4348d21358ef752a357c33976b85357317bfb623a79cb91ec462b4e5128b82d5`  
		Last Modified: Thu, 12 Mar 2026 23:43:03 GMT  
		Size: 3.8 MB (3795119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a169c2de4deea9b877eb224ec8f2d4f4502dd0bb4e22037516ea41c23c8c1e6`  
		Last Modified: Thu, 12 Mar 2026 23:43:02 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f88a80dfabed7faa02e1bbe28dd4e26c817c26d54bb3411b27cc398ea997ef8`  
		Last Modified: Thu, 12 Mar 2026 23:43:02 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5e7662fcf96af1dfae3edab12e535e5dbb2bd9336314490ac9484222315cc0`  
		Last Modified: Thu, 09 Apr 2026 22:27:14 GMT  
		Size: 14.4 MB (14379286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b2bd611f10e897bc78163d788b300458c71f27af849508076d219371619381`  
		Last Modified: Thu, 09 Apr 2026 22:27:14 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c1175a23bc886b3bc9f9e6845c90d99d1125fc788f6d88d5ad9501ed086f83`  
		Last Modified: Thu, 09 Apr 2026 22:27:15 GMT  
		Size: 21.9 MB (21889964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48a98f93d43e57e9161beb90862e90db489cf9d4b4d09bfbd7d3bc1566f7981`  
		Last Modified: Thu, 09 Apr 2026 22:27:14 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91cdaaeb755a7dbc3a463542f5d9410ef527eb1babc2850059c13f703b6bf5f`  
		Last Modified: Thu, 09 Apr 2026 22:27:15 GMT  
		Size: 23.4 KB (23427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b0c643f457b3285c9b024aac2f31693051af6eb786510b03d7580e65134de8`  
		Last Modified: Thu, 09 Apr 2026 23:19:25 GMT  
		Size: 32.1 MB (32113304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a5512141ecbaa16f283bdbec60a949479d2d7ef6afafc01d5cc3b3351085cd1`  
		Last Modified: Thu, 09 Apr 2026 23:19:20 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd4c500e9eb181938a1ef4ef73f183e9b27420814a10ea55b06e736b40bf16a`  
		Last Modified: Tue, 14 Apr 2026 18:19:51 GMT  
		Size: 17.3 MB (17317554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc53ab4bbf74e12a9c7818288fc97c9f60326574f248c11959ba84015cc1ee0`  
		Last Modified: Tue, 14 Apr 2026 18:19:51 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c73a8be0d813065a838fdca97a14527a4ee7e1530e35f656f93a424f4d7c27`  
		Last Modified: Tue, 14 Apr 2026 18:19:42 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:0bc79feb6a333a11cc49a0e80b8edad445b1bc590d108776ee1d1f9cba4c69b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2209891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e15343c996740440561a353bfba972b4a6752dff34802d7eb98b3923520488bd`

```dockerfile
```

-	Layers:
	-	`sha256:10647c8aceb5f18307cac8578a92f75dc319b2558c6f7cfcacc86be9c1ffd2ee`  
		Last Modified: Tue, 14 Apr 2026 18:19:50 GMT  
		Size: 2.2 MB (2179221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ceacdd28fffe318712ca3aebf2993293f60ba3f21a55c590b010d01ac5e20b8`  
		Last Modified: Tue, 14 Apr 2026 18:19:50 GMT  
		Size: 30.7 KB (30670 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.2`

```console
$ docker pull composer@sha256:41f3f5d851d627fd5b366c70aed952205bcc3d15b7e4fec6a06f63fb41ae284c
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
$ docker pull composer@sha256:1d4c34f32a20484007c6eb4de0b260176fea87afc679390ad59d651bcaf89521
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (78041261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8bbcca4d758e821ee248655c18fcc426631d1c02aa6c1d2ff48fae7dd8c9b30`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:17:52 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:17:52 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:17:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:17:52 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:17:52 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:17:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:17:52 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:17:52 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 15 Apr 2026 20:17:52 GMT
ENV PHP_VERSION=8.5.5
# Wed, 15 Apr 2026 20:17:52 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Wed, 15 Apr 2026 20:17:52 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Wed, 15 Apr 2026 20:17:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 20:17:56 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:21:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 20:21:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:21:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 20:21:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 20:21:24 GMT
CMD ["php" "-a"]
# Wed, 15 Apr 2026 21:27:10 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Wed, 15 Apr 2026 21:27:10 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Wed, 15 Apr 2026 21:27:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 15 Apr 2026 21:27:25 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 15 Apr 2026 21:27:25 GMT
ENV COMPOSER_VERSION=2.2.27
# Wed, 15 Apr 2026 21:27:25 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Wed, 15 Apr 2026 21:27:25 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 21:27:25 GMT
WORKDIR /app
# Wed, 15 Apr 2026 21:27:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:27:25 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7575019b1e32c16a639f3988d9a63ff1c22c036099e3cb267ea5a97ba0fcb31b`  
		Last Modified: Wed, 15 Apr 2026 20:21:32 GMT  
		Size: 3.6 MB (3587447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba54b7e6d1307c692fb0f98a7bb785c3ae59fda44cbd8dc735eb6d32da25bb2`  
		Last Modified: Wed, 15 Apr 2026 20:21:32 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7367014229e0f5079d78d9d65f87aeb106ffa42ef3cacfdde5ccae68a710662d`  
		Last Modified: Wed, 15 Apr 2026 20:21:32 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c74770868277c77b3c7d8e5aa987ffc0183e76f8a003e5ee3e5662475be115`  
		Last Modified: Wed, 15 Apr 2026 20:21:33 GMT  
		Size: 14.4 MB (14379186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f1108694a36c05d3950260f3491806016ec3ab9ba1da15154bda777858d1eb`  
		Last Modified: Wed, 15 Apr 2026 20:21:33 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e321e76cc80892e05feb16337063a65959f21cd03508ea9f6dd1316bd2bfee6`  
		Last Modified: Wed, 15 Apr 2026 20:21:34 GMT  
		Size: 22.5 MB (22528821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2af3ca59c901474266aab6d50192f869e507a229be1b7493e312a32fac0dff9`  
		Last Modified: Wed, 15 Apr 2026 20:21:33 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b12841ff7824946e17f91cf31b444d9a97e15dc30fa55d79e32ae0c00cf27f1`  
		Last Modified: Wed, 15 Apr 2026 20:21:34 GMT  
		Size: 23.4 KB (23395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57079944d1b1c6704b62a38554cbc9eac518eef26bfc4c63ef53dd521e1a266a`  
		Last Modified: Wed, 15 Apr 2026 21:27:36 GMT  
		Size: 32.8 MB (32828035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a085d68ed874eff7f3791196e945d0b56fb9ce296431a7694dd6103638f9329d`  
		Last Modified: Wed, 15 Apr 2026 21:27:35 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd60a45d71c336e91431bf5499d20771638f2cd038be398e13d2aabcc420304d`  
		Last Modified: Wed, 15 Apr 2026 21:27:35 GMT  
		Size: 825.3 KB (825333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:960478e0021327b3f30ffb74841f0d37450c8a5f3a2d4f2f436ccfd70599c409`  
		Last Modified: Wed, 15 Apr 2026 21:27:35 GMT  
		Size: 415.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0c8584100e6db2c11c24c170d1cfce6261a0dbc860141d442ebf8c4b424c48`  
		Last Modified: Wed, 15 Apr 2026 21:27:36 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:06d4d7fa0f03920a6c240e4d072729bdc46987538c5c68aab2ef317aa293e366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2208131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46c769bdd88077126f37041220fded1436c759dff2346e89f6aef997cd325fe0`

```dockerfile
```

-	Layers:
	-	`sha256:e2e99e8ba5356443dbad29b06bc4190a3957e90425a5fb77e98fedd71536a283`  
		Last Modified: Wed, 15 Apr 2026 21:27:35 GMT  
		Size: 2.2 MB (2178067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de1298dfa730854ddb3bf4fac787e6bc8a2aaf92684c3cf519f5366a43fc62f7`  
		Last Modified: Wed, 15 Apr 2026 21:27:35 GMT  
		Size: 30.1 KB (30064 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; arm variant v6

```console
$ docker pull composer@sha256:837725d87752ddf8ddaab26e64b1ab5cf4bbd15695a94e6334c1fab69292228e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74547326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c38c96f2e01f008b141aeae286848621bba080e9e98d2dc2987863029894fb74`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:19:04 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:19:04 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:19:04 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:19:04 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:19:05 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:19:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:19:05 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:19:05 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:19:05 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 15 Apr 2026 20:19:05 GMT
ENV PHP_VERSION=8.5.5
# Wed, 15 Apr 2026 20:19:05 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Wed, 15 Apr 2026 20:19:05 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Wed, 15 Apr 2026 20:19:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 20:19:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:22:18 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 20:22:18 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:22:19 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 20:22:19 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 20:22:19 GMT
CMD ["php" "-a"]
# Wed, 15 Apr 2026 21:22:04 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Wed, 15 Apr 2026 21:22:04 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Wed, 15 Apr 2026 21:22:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 15 Apr 2026 21:22:28 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 15 Apr 2026 21:22:28 GMT
ENV COMPOSER_VERSION=2.2.27
# Wed, 15 Apr 2026 21:22:28 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Wed, 15 Apr 2026 21:22:28 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 21:22:28 GMT
WORKDIR /app
# Wed, 15 Apr 2026 21:22:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:22:28 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1d167fc497e35df23f81ef7d507ee40c904d148d7c5e239db360263ce1228f`  
		Last Modified: Wed, 15 Apr 2026 20:22:24 GMT  
		Size: 3.5 MB (3543048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7893272fc58b639fcb274b9cdac380a99a02b7fec1370991d7043a8d745ee731`  
		Last Modified: Wed, 15 Apr 2026 20:22:24 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b5e2d5fa2204fe8d000332835281efd2beeb4e2b1233fda8377dc9fb8d273da`  
		Last Modified: Wed, 15 Apr 2026 20:22:24 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a237864e95f05b7c9e05c3272f303c8616f39f4b50a113166e6e93f5d6eb2867`  
		Last Modified: Wed, 15 Apr 2026 20:22:25 GMT  
		Size: 14.4 MB (14379195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d6cac0622b9c4733975c694271b5cfe4e9e251f5a29439c27931c4334db09d`  
		Last Modified: Wed, 15 Apr 2026 20:22:25 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a5b1613ded78de2dd5fc3a3cbb57bc91cb6f35c9bf29e262676641888899d35`  
		Last Modified: Wed, 15 Apr 2026 20:22:26 GMT  
		Size: 19.5 MB (19534950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7326187f367c7e04eed9c7cfd2fd94e264bdf5da29600b25762d89f896ee8df`  
		Last Modified: Wed, 15 Apr 2026 20:22:26 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf7aab9524160d3a6dc903858b7d9fc9d77b6f4a09bb6c0cdb0b86eca60acbc`  
		Last Modified: Wed, 15 Apr 2026 20:22:26 GMT  
		Size: 23.2 KB (23204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2c6c58668e522a6546d30e2e0d16f1dc9e65b33a4eeba969e3d61ebb9564fe`  
		Last Modified: Wed, 15 Apr 2026 21:22:36 GMT  
		Size: 32.7 MB (32665512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4947bf681a71f88ccd9a5bb3e83617056fbb25d6034988a7a79a9c8a97b9b05`  
		Last Modified: Wed, 15 Apr 2026 21:22:35 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d63524fbedb3794d475380667167823a9cbb05b4b2506370321caf12069d03f`  
		Last Modified: Wed, 15 Apr 2026 21:22:35 GMT  
		Size: 824.7 KB (824705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eec0de4e89259ab68dad0ab2735d78fa9821e858d1fb905df3c56031c6e0179`  
		Last Modified: Wed, 15 Apr 2026 21:22:35 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5acf5eb8d2fa0eb48c0426b92564b2a5371288eebcd7411ccfd0969b94e969a`  
		Last Modified: Wed, 15 Apr 2026 21:22:36 GMT  
		Size: 91.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:870c19dd765a60097046d1f263461934823473ae9e1c7b16e5ad11e7ef213808
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.9 KB (29939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de96a4283a356a91c500ba91940cb9564592a86f12b7c3e63eb315e1dc75d09c`

```dockerfile
```

-	Layers:
	-	`sha256:53229572f116c44a9361a208605236ab8184f7a741f3f2fe56eee787f318be0f`  
		Last Modified: Wed, 15 Apr 2026 21:22:35 GMT  
		Size: 29.9 KB (29939 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; arm variant v7

```console
$ docker pull composer@sha256:da8d666b84e463409180c65f13ddad9cc253f0a1d44e27411473db9735a952c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 MB (71375730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41452a589beba75b286d0eefef40649738e54779a0e0d48db722b53db61d643d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:18:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:18:22 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:18:22 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:18:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:18:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:18:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:18:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:18:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:18:22 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 15 Apr 2026 20:18:22 GMT
ENV PHP_VERSION=8.5.5
# Wed, 15 Apr 2026 20:18:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Wed, 15 Apr 2026 20:18:22 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Wed, 15 Apr 2026 20:18:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 20:18:26 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:21:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 20:21:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:21:34 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 20:21:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 20:21:34 GMT
CMD ["php" "-a"]
# Wed, 15 Apr 2026 21:32:23 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Wed, 15 Apr 2026 21:32:23 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Wed, 15 Apr 2026 21:32:44 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 15 Apr 2026 21:32:44 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 15 Apr 2026 21:32:44 GMT
ENV COMPOSER_VERSION=2.2.27
# Wed, 15 Apr 2026 21:32:44 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Wed, 15 Apr 2026 21:32:44 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 21:32:44 GMT
WORKDIR /app
# Wed, 15 Apr 2026 21:32:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:32:44 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40243011337e75e1e1aba1a01eff0f25c670f2784f31a19fe3ceeb28d9cbb386`  
		Last Modified: Wed, 15 Apr 2026 20:21:41 GMT  
		Size: 3.3 MB (3343352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289d25cb3dc6bf4d1acfe704c1d05a812b84cbfe26b06c6e9a423f281efcfd64`  
		Last Modified: Wed, 15 Apr 2026 20:21:41 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457ef191b478c4407082d1c51e695feac2f4425353d54d5d6737f8e3aede1686`  
		Last Modified: Wed, 15 Apr 2026 20:21:41 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef8f20263bc5a42b03699b180b432cb94cb313e98aed5a4238024d8cd3f252ad`  
		Last Modified: Wed, 15 Apr 2026 20:21:41 GMT  
		Size: 14.4 MB (14379203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654a3e48df9d037dc7d582e4d7e753ead3d5f55b619c07d29f0f2701eabf4657`  
		Last Modified: Wed, 15 Apr 2026 20:21:43 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00b79e1670ab000b58c3fa612bf97d881357d5a02a37a01aab4448a263a56aa`  
		Last Modified: Wed, 15 Apr 2026 20:21:43 GMT  
		Size: 18.4 MB (18430268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:670c3d79616cd5914f7e4d0d94505d6570f152e3fab437081ba1b2499bf253df`  
		Last Modified: Wed, 15 Apr 2026 20:21:43 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773025cf5591ee7e2a345d9e429358f0269bd41230fb2da781a05eb990ef0386`  
		Last Modified: Wed, 15 Apr 2026 20:21:43 GMT  
		Size: 23.2 KB (23204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8163cc06504257b3d8fa509d21f60978ceefa1cd472dacc146e9060cfefd59ee`  
		Last Modified: Wed, 15 Apr 2026 21:32:54 GMT  
		Size: 31.1 MB (31096177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0da6dabec8b02c8a57a39ddf59fb2cee0a1c872ee63dfd2f2977bae39ff3da`  
		Last Modified: Wed, 15 Apr 2026 21:32:53 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3066dceebf735a3db5b17414e50d2afb21885ae7c8675adf8872105dec35f861`  
		Last Modified: Wed, 15 Apr 2026 21:32:53 GMT  
		Size: 815.6 KB (815555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef3ff58287779bb6f576bb1b79533f8679c2860ea4b5f32fa98203a8d03eaa94`  
		Last Modified: Wed, 15 Apr 2026 21:32:53 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f00f263c0c2026cb35f98332303a28dd1d9cd3173c35bcdb8b80e1eeed2901`  
		Last Modified: Wed, 15 Apr 2026 21:32:54 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:760301001eb8c3052619f101a64223d4afb601923e2ec45c82508b3c6e0a2379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2207876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abbe5388a5ba79dd2a15717dca5ecb25e1d7d8d8589402d9bfe9d1b8c7d2682f`

```dockerfile
```

-	Layers:
	-	`sha256:a87c0263dff8bc23768953af3224577f37510cd7ae2a73dd3dfe81098328e653`  
		Last Modified: Wed, 15 Apr 2026 21:32:53 GMT  
		Size: 2.2 MB (2177722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db09aa483fb8cc3d156aacedb12a66da7d8fdd5f1b358a4ed1d5676d3677327f`  
		Last Modified: Wed, 15 Apr 2026 21:32:53 GMT  
		Size: 30.2 KB (30154 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:de12a763512eefc03bf209f5ee8d95b7ce1e9b6f424654485686e5039ac734e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.7 MB (77696381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b1452a0f806645bd2dbcd3d38a18a64b5cebba142b836475a0b5c610d89082f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:21 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:16:21 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:16:21 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:16:21 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:16:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:16:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:16:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:16:21 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:16:21 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 15 Apr 2026 20:16:21 GMT
ENV PHP_VERSION=8.5.5
# Wed, 15 Apr 2026 20:16:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Wed, 15 Apr 2026 20:16:21 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Wed, 15 Apr 2026 20:16:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 20:16:25 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:19:57 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 20:19:57 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:19:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 20:19:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 20:19:58 GMT
CMD ["php" "-a"]
# Wed, 15 Apr 2026 21:40:25 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Wed, 15 Apr 2026 21:40:25 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Wed, 15 Apr 2026 21:40:45 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 15 Apr 2026 21:40:45 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 15 Apr 2026 21:40:45 GMT
ENV COMPOSER_VERSION=2.2.27
# Wed, 15 Apr 2026 21:40:45 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Wed, 15 Apr 2026 21:40:45 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 21:40:45 GMT
WORKDIR /app
# Wed, 15 Apr 2026 21:40:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:40:45 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e4c5bcbf8c3068a7d4c178cdd5132463fa53adf8c55efe0d5a02126d958e69`  
		Last Modified: Wed, 15 Apr 2026 20:20:06 GMT  
		Size: 3.6 MB (3596134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c0edc310dc19501413b5668245bc984741c4ac5a3219932a74e83fb33b6f94`  
		Last Modified: Wed, 15 Apr 2026 20:20:02 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d665080207d06b6b7246d46376f6ec0b3a5d072b47f01ab3fe89eb95ea0b9310`  
		Last Modified: Wed, 15 Apr 2026 20:20:02 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e92dbfc45c4b506749680c4bded773db9170a5c594ae07c33aa938ac9b46a1c`  
		Last Modified: Wed, 15 Apr 2026 20:20:07 GMT  
		Size: 14.4 MB (14379192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da631dfa865e2d394e47bb93c95f041d309af42b22cd597826fab10299773bc`  
		Last Modified: Wed, 15 Apr 2026 20:20:03 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0885f624969f9911f18390a16714e49ddcba2831ee9c8002d794ee56d8ca9ca8`  
		Last Modified: Wed, 15 Apr 2026 20:20:07 GMT  
		Size: 21.7 MB (21697840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e202517af7cb78a86ff7f8b255ca452261912c8830cf0b7e352386b5c5472454`  
		Last Modified: Wed, 15 Apr 2026 20:20:05 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4062a55681ba2c31424930678c18614b1e9e0eb63f551ee5faaa3857658f4f0`  
		Last Modified: Wed, 15 Apr 2026 20:20:07 GMT  
		Size: 23.2 KB (23209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21fa51673c1b1fb1e3a5b0375d97adccdf20a311f0f8b37c97b2fe70160269f3`  
		Last Modified: Wed, 15 Apr 2026 21:40:56 GMT  
		Size: 33.0 MB (32971367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ef903a9ac3d2369ad60193a24a651e6966d2782be4c36e46b1ee195f45a06e`  
		Last Modified: Wed, 15 Apr 2026 21:40:55 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29a53602668c6febf8628b803a39aa1989644ac101845a846a0ce4ed5e39466`  
		Last Modified: Wed, 15 Apr 2026 21:40:55 GMT  
		Size: 823.9 KB (823918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15c35b1758e67f72c86b8de7a08e1a059ed64a12fc5210e2be6872e3c09726d1`  
		Last Modified: Wed, 15 Apr 2026 21:40:55 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19efc57a96ea43f4c5e0c49c9936f6a3d16268b6c75e27975289d8e36717117d`  
		Last Modified: Wed, 15 Apr 2026 21:40:56 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:67b85ec6315145d387798071ba07f8d99cb5b11b25bf7a8315694cc3d7f312ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2207718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff48fd5266f995141a6dc18c85cfc2406e468fca6b24de0e7b147b634f0ca661`

```dockerfile
```

-	Layers:
	-	`sha256:07abefe7db6f47eae953c963e1b3a27c16ed1d3fa9adac816f9e198e67438e71`  
		Last Modified: Wed, 15 Apr 2026 21:40:55 GMT  
		Size: 2.2 MB (2177544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3619f43de94dad8331a15aab0d281fb653ef0bd905a88215519186c5039c09b7`  
		Last Modified: Wed, 15 Apr 2026 21:40:55 GMT  
		Size: 30.2 KB (30174 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; 386

```console
$ docker pull composer@sha256:35f5329693ba247b75cdf7c773f0ebd55e0e3b9da051c03699b7c9e0abb71cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.3 MB (82285109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:748b8a46da60c2b55abee6ef41e5a4f80192a39cdfcdf03aaad1775dd05a512e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Fri, 10 Apr 2026 00:13:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 10 Apr 2026 00:13:16 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 10 Apr 2026 00:13:16 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 10 Apr 2026 00:13:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 10 Apr 2026 00:13:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 10 Apr 2026 00:13:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 10 Apr 2026 00:13:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 10 Apr 2026 00:13:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 10 Apr 2026 00:13:16 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 10 Apr 2026 00:13:16 GMT
ENV PHP_VERSION=8.5.5
# Fri, 10 Apr 2026 00:13:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Fri, 10 Apr 2026 00:13:16 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Fri, 10 Apr 2026 00:13:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 10 Apr 2026 00:13:20 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 00:16:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 10 Apr 2026 00:16:53 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 00:16:54 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 10 Apr 2026 00:16:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 10 Apr 2026 00:16:54 GMT
CMD ["php" "-a"]
# Tue, 14 Apr 2026 18:19:28 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Apr 2026 18:19:28 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Apr 2026 18:20:22 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Apr 2026 18:20:22 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Apr 2026 18:20:22 GMT
ENV COMPOSER_VERSION=2.2.27
# Tue, 14 Apr 2026 18:20:22 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Apr 2026 18:20:22 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Apr 2026 18:20:22 GMT
WORKDIR /app
# Tue, 14 Apr 2026 18:20:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Apr 2026 18:20:22 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d2062b0536d4d6a1543e3a6bfd55452c7706979a7def0ad5ff0f3e183f183d`  
		Last Modified: Fri, 10 Apr 2026 00:17:02 GMT  
		Size: 5.9 MB (5909460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb9b53f46bb29bde8242534cc51035c71b65536a0a0acada6428f7a8ba0889c`  
		Last Modified: Fri, 10 Apr 2026 00:17:02 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab50b39601a88f935ec690047331c7481ff9b7ae2bb959cfc4cc98313c492986`  
		Last Modified: Fri, 10 Apr 2026 00:17:02 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92225e063d6f653398ed45adcff1579a3a3cf3ccbe764a4bb5b301283ee3b2ee`  
		Last Modified: Fri, 10 Apr 2026 00:17:02 GMT  
		Size: 14.4 MB (14379292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ccaecce131db93828716f892d3ad6e523dec70db239cc1bed3bb5394e8396c`  
		Last Modified: Fri, 10 Apr 2026 00:17:03 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e4efa73be7dce94cd5df6088620edcd50156eafe81c782274c129a7a3e191d`  
		Last Modified: Fri, 10 Apr 2026 00:17:04 GMT  
		Size: 23.4 MB (23438953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab8684032f9c15ecd79788e50ca55f90486d5bf79b5b3a24018772984e7a1cb5`  
		Last Modified: Fri, 10 Apr 2026 00:17:04 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba72ff6334ace2c9a0d737cdf3c0fa9f61f267a07af45bf21e2ff77820277e5`  
		Last Modified: Fri, 10 Apr 2026 00:17:04 GMT  
		Size: 23.6 KB (23625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb92bca6a7200abd5ed57acbc2406d1b631ce897e9fcb8321df6d6ad30cb6114`  
		Last Modified: Tue, 14 Apr 2026 18:19:58 GMT  
		Size: 33.4 MB (33354023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3acb4361787726cd8ad52c3d9467b84e1d1aa7dfe6414e7e3be8d2816cc76617`  
		Last Modified: Tue, 14 Apr 2026 18:19:57 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649871246b4636d3e71336ce00677bad781148c88f1b63a1358cf436f11feac4`  
		Last Modified: Tue, 14 Apr 2026 18:20:28 GMT  
		Size: 1.5 MB (1487908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db2ceeac24b57d267726c3a0854b3db4a10c8f8be761f7f653a0c97fc86e57d`  
		Last Modified: Tue, 14 Apr 2026 18:20:28 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b0fc048d318578d95fbcda07a86c87b70bb13465e4a96a6f8cd472ba6b7fc5`  
		Last Modified: Tue, 14 Apr 2026 18:20:28 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:6884a4f582cf2cce11394bbc1245585b552aa80cf36ceb1c9d4ef7f115bf1e39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2209886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af552b456c5f7c8ba7208226abe75e9da9e899a0cf7f25b20762f8ba266a59e2`

```dockerfile
```

-	Layers:
	-	`sha256:f642b0c6b11ef666fee6cf07735b6410a1f0c832aceb20154fc0006c77c66794`  
		Last Modified: Tue, 14 Apr 2026 18:20:28 GMT  
		Size: 2.2 MB (2179845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffe56978f8a88a319c332992e7ef101b50d32c77831087a868f2c4c7872fb94b`  
		Last Modified: Tue, 14 Apr 2026 18:20:28 GMT  
		Size: 30.0 KB (30041 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; ppc64le

```console
$ docker pull composer@sha256:3bc9df9d34e445d60475370f8bf6ca3238a9de88a772bb54a4cb5978ed15739a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 MB (96516566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1ee0ee938940b40491579bf9c0a7ba8ecda47725576918950bf7b239cd7aa26`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Thu, 12 Mar 2026 23:53:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Mar 2026 23:53:02 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Mar 2026 23:53:02 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Mar 2026 23:53:02 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Mar 2026 23:53:02 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Mar 2026 23:53:02 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Mar 2026 23:53:02 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Mar 2026 23:53:02 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Mar 2026 23:53:02 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 12 Mar 2026 23:53:02 GMT
ENV PHP_VERSION=8.5.5
# Thu, 12 Mar 2026 23:53:02 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Thu, 12 Mar 2026 23:53:02 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Thu, 09 Apr 2026 22:33:42 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 09 Apr 2026 22:33:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:38:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 09 Apr 2026 22:38:29 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:38:30 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 09 Apr 2026 22:38:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 09 Apr 2026 22:38:30 GMT
CMD ["php" "-a"]
# Fri, 10 Apr 2026 00:21:05 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 10 Apr 2026 00:21:07 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Apr 2026 18:19:02 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Apr 2026 18:19:02 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Apr 2026 18:19:02 GMT
ENV COMPOSER_VERSION=2.2.27
# Tue, 14 Apr 2026 18:19:02 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Apr 2026 18:19:05 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Apr 2026 18:19:09 GMT
WORKDIR /app
# Tue, 14 Apr 2026 18:19:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Apr 2026 18:19:09 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7db1cc7b26f64d5de44e75f81962c30dead7dbc1dae3ebb93d0dc3d0cea721a`  
		Last Modified: Thu, 12 Mar 2026 23:58:51 GMT  
		Size: 3.8 MB (3768852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4a23ff5963c3f844b77db123769c733318f6ad54386c9f63e356424059470b`  
		Last Modified: Thu, 12 Mar 2026 23:58:51 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a071b7623ea30b2e8950858971a7e7838856db9c469a46b6305dcd619d0531fc`  
		Last Modified: Thu, 12 Mar 2026 23:58:51 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d012a34014d339e95156eab3252cc22fbae82a4670be3766b110c04e96ff1a17`  
		Last Modified: Thu, 09 Apr 2026 22:38:45 GMT  
		Size: 14.4 MB (14379301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8b7c5afa56dcdf0f01aaba59b305697db6b72603309ba573605f5fcd422fc0`  
		Last Modified: Thu, 09 Apr 2026 22:38:45 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1971acbe5d44b0f37d3698908a5766cea69f16ef4c4472ca8a30f5d48eec93ec`  
		Last Modified: Thu, 09 Apr 2026 22:38:46 GMT  
		Size: 23.1 MB (23118163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ee71922b29fe2228fde987804ee785c857383e7941a35e885bb5f06b7c3aba`  
		Last Modified: Thu, 09 Apr 2026 22:38:45 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fbefb03f1cf2736ed7b9f334b7e8f2f16dbedad1876c833ba4682b99ca9f99a`  
		Last Modified: Thu, 09 Apr 2026 22:38:46 GMT  
		Size: 23.4 KB (23442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db29015527299944deffccc76c5bfb597208be66aea62b09cf37a0cef1bb364e`  
		Last Modified: Fri, 10 Apr 2026 00:22:19 GMT  
		Size: 34.2 MB (34177434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972a41e22feca9d4bfcc298283918766cb03ebb7dd146ebbded895c8b431c973`  
		Last Modified: Fri, 10 Apr 2026 00:22:17 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a00b8129dae026b4288901fdf4844d14631360cd95724ef7a99b65dab607a3a7`  
		Last Modified: Tue, 14 Apr 2026 18:19:38 GMT  
		Size: 17.2 MB (17214867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b642fc002306ffa035fabc99948ab54d676222458872361b5da11d126da7f4a9`  
		Last Modified: Tue, 14 Apr 2026 18:19:38 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33f861bae9f5ec9825aa85d366c341ad622e0c26fad222ee7341b19546dfac2`  
		Last Modified: Tue, 14 Apr 2026 18:19:38 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:a1c93648e57614e4c8f0dcf7199c333eeda49c94176869dc05e8f7de304f3cf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2210002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6040621f06dbe2c2a62e88287ee16b383a874ac09143e68a6d024651c828f7e3`

```dockerfile
```

-	Layers:
	-	`sha256:9d93dcd35f40f1b73d8e6aab1f0ad312cef0d127b4d9561162774bc7ed41925d`  
		Last Modified: Tue, 14 Apr 2026 18:19:37 GMT  
		Size: 2.2 MB (2179896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2a711e174b0c511983fc08afe41d592f4c8cf2cf2facda7a2594455b610ba0b`  
		Last Modified: Tue, 14 Apr 2026 18:19:37 GMT  
		Size: 30.1 KB (30106 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; riscv64

```console
$ docker pull composer@sha256:cf698321e756d82bc12e24f70c655b5d1daf8ed9e605cee5c19a8140aea3fd33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77909972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fe71051367b5659b8bb62a70a49db12f4724db7aee6fde4c3fb22601ce02e9f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 09:13:06 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 28 Jan 2026 09:13:06 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 28 Jan 2026 09:13:06 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 28 Jan 2026 09:13:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 28 Jan 2026 09:13:07 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 28 Jan 2026 09:13:07 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_VERSION=8.5.5
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Fri, 10 Apr 2026 09:29:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 10 Apr 2026 09:29:21 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 10:28:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 10 Apr 2026 10:28:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 10:28:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 10 Apr 2026 10:28:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 10 Apr 2026 10:28:33 GMT
CMD ["php" "-a"]
# Sun, 12 Apr 2026 09:33:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Sun, 12 Apr 2026 09:33:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Apr 2026 18:28:51 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Apr 2026 18:28:51 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Apr 2026 18:28:51 GMT
ENV COMPOSER_VERSION=2.2.27
# Tue, 14 Apr 2026 18:28:51 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Apr 2026 18:28:51 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Apr 2026 18:28:51 GMT
WORKDIR /app
# Tue, 14 Apr 2026 18:28:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Apr 2026 18:28:51 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d64a68485fdb9ab2ec4159ac3e04e0bb79d9f1d037e580e928ca2b9604180f`  
		Last Modified: Wed, 28 Jan 2026 10:13:59 GMT  
		Size: 3.7 MB (3741000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b030c1b113432578231e8fe7c8a1bc913f2dc5dcba512e805fa9ab07768c9bd4`  
		Last Modified: Wed, 28 Jan 2026 10:13:58 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32a0e9bcb36b34307b4eada1f50c1cd4244d43d19ee57d962818dcb0ff0b110`  
		Last Modified: Wed, 28 Jan 2026 10:13:58 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20501e9e3d17b72af47b7d522d0c369998be222ed66ed9070ed2cbc45e500ca7`  
		Last Modified: Fri, 10 Apr 2026 10:29:42 GMT  
		Size: 14.4 MB (14379290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f7fa0bbe8ea35a7aeededb6a1c62d4e192d88a3cbaa6a9ac613390cef5f797e`  
		Last Modified: Fri, 10 Apr 2026 10:29:38 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c00b6c348638ca2fb138534e98df3a83c5788350e7f682c5dab61388d5988a1`  
		Last Modified: Fri, 10 Apr 2026 10:29:43 GMT  
		Size: 20.8 MB (20772153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf32615937490fdbee93796b59955ce07e051f019b76917819692421da228ef`  
		Last Modified: Fri, 10 Apr 2026 10:29:38 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491cab84c5a842c690a34c22c4cfe20f23d7b27019ca9d80e387fd23ef96828d`  
		Last Modified: Fri, 10 Apr 2026 10:29:39 GMT  
		Size: 23.3 KB (23349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e865e7a35bee8605e802d4714eef1a4cd079ed0b68a414c076e698d97cfbedd6`  
		Last Modified: Sun, 12 Apr 2026 09:38:57 GMT  
		Size: 31.3 MB (31300012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:670c7192db5936f38910b865b3f6746b70a4b2523b1e25db7d274900db0fca4f`  
		Last Modified: Sun, 12 Apr 2026 09:38:52 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5bdd2e2f534ae25a788c0f4fe04db08c09d85e043bff17c4238b4c5c6e12e2`  
		Last Modified: Tue, 14 Apr 2026 18:30:04 GMT  
		Size: 4.1 MB (4104012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1ca5c26ad5a331c9c78d1736a316cd75130f2c5fc620da2614c677c1610b79`  
		Last Modified: Tue, 14 Apr 2026 18:30:03 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd33bb4fad3f92609198afdae7d92af15161acef56cb4c6f80fa7a9cdefa0c3`  
		Last Modified: Tue, 14 Apr 2026 18:29:56 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:d499efcf872dd10295b0361b3f735682b694176478d8de89f6e9ed88975b6fef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2208939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a4e7210e9321acd0aa206f7db001b89b492df5fd3f869de1f7910b3ebcaca37`

```dockerfile
```

-	Layers:
	-	`sha256:e1ebc611e5beb930a14f43da834427bd8cba5278ee9b1ae4178ff4cba263cbd8`  
		Last Modified: Tue, 14 Apr 2026 18:30:03 GMT  
		Size: 2.2 MB (2178837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c1b2893b53b2641c74019ec997c6cd50ba35ff87e1cc59416af349b182e62ef`  
		Last Modified: Tue, 14 Apr 2026 18:30:03 GMT  
		Size: 30.1 KB (30102 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; s390x

```console
$ docker pull composer@sha256:093e24e420e8a8867177194221f361d676048cacadf0270ba0b9f58bbf5b2ada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.1 MB (93052143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61dc9356e7aa5e6362a5b41607515476a6800d97e3fbbfc6bdd998a0b89de4db`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Mar 2026 23:37:17 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Mar 2026 23:37:17 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Mar 2026 23:37:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Mar 2026 23:37:17 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHP_VERSION=8.5.5
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Thu, 09 Apr 2026 22:21:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 09 Apr 2026 22:21:35 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:27:00 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 09 Apr 2026 22:27:00 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:27:01 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 09 Apr 2026 22:27:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 09 Apr 2026 22:27:01 GMT
CMD ["php" "-a"]
# Thu, 09 Apr 2026 23:18:55 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 09 Apr 2026 23:18:55 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Apr 2026 18:19:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Apr 2026 18:19:55 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Apr 2026 18:19:55 GMT
ENV COMPOSER_VERSION=2.2.27
# Tue, 14 Apr 2026 18:19:55 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Apr 2026 18:19:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Apr 2026 18:19:55 GMT
WORKDIR /app
# Tue, 14 Apr 2026 18:19:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Apr 2026 18:19:55 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4348d21358ef752a357c33976b85357317bfb623a79cb91ec462b4e5128b82d5`  
		Last Modified: Thu, 12 Mar 2026 23:43:03 GMT  
		Size: 3.8 MB (3795119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a169c2de4deea9b877eb224ec8f2d4f4502dd0bb4e22037516ea41c23c8c1e6`  
		Last Modified: Thu, 12 Mar 2026 23:43:02 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f88a80dfabed7faa02e1bbe28dd4e26c817c26d54bb3411b27cc398ea997ef8`  
		Last Modified: Thu, 12 Mar 2026 23:43:02 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5e7662fcf96af1dfae3edab12e535e5dbb2bd9336314490ac9484222315cc0`  
		Last Modified: Thu, 09 Apr 2026 22:27:14 GMT  
		Size: 14.4 MB (14379286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b2bd611f10e897bc78163d788b300458c71f27af849508076d219371619381`  
		Last Modified: Thu, 09 Apr 2026 22:27:14 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c1175a23bc886b3bc9f9e6845c90d99d1125fc788f6d88d5ad9501ed086f83`  
		Last Modified: Thu, 09 Apr 2026 22:27:15 GMT  
		Size: 21.9 MB (21889964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48a98f93d43e57e9161beb90862e90db489cf9d4b4d09bfbd7d3bc1566f7981`  
		Last Modified: Thu, 09 Apr 2026 22:27:14 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91cdaaeb755a7dbc3a463542f5d9410ef527eb1babc2850059c13f703b6bf5f`  
		Last Modified: Thu, 09 Apr 2026 22:27:15 GMT  
		Size: 23.4 KB (23427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4fdf3eb0ccd09c5d847e8404ebd00d415ec8a926328bb55405913777275f663`  
		Last Modified: Thu, 09 Apr 2026 23:19:34 GMT  
		Size: 32.1 MB (32113289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:233a242e39cffb8912002ca05f6e84274f01e36739c65884086e484ec1f9ce01`  
		Last Modified: Thu, 09 Apr 2026 23:19:33 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d4eb190454ffaef90be5e6e0c819cb3a9e7a990e97007fc908ab14eb6c53b8`  
		Last Modified: Tue, 14 Apr 2026 18:20:11 GMT  
		Size: 17.1 MB (17120862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d69b603af35c10edfc476777fd1bcdd7a3bf814ea42956731c8ce32d7871b70`  
		Last Modified: Tue, 14 Apr 2026 18:20:10 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30182dd14eb74e4c391867549fbf9c4dfb3eb2bd14ffe94db514ef30c07d544c`  
		Last Modified: Tue, 14 Apr 2026 18:20:10 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:064684950c506dc3ada188dc93ce31604db9827dc2a07eb9cec3ddd72297fa76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2208701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e15954f05e76147d256bb7d2637ffee0a926191203bc152df824c2e93d4ec50f`

```dockerfile
```

-	Layers:
	-	`sha256:414ea970aecb739f4c603b73c40816576cbb8d0bfbc46b5d72cc910ca4773312`  
		Last Modified: Tue, 14 Apr 2026 18:20:10 GMT  
		Size: 2.2 MB (2178631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16aeaa77a826b0c9e08631385e3529effaef99aac59efcaa6ed272e688af12ba`  
		Last Modified: Tue, 14 Apr 2026 18:20:10 GMT  
		Size: 30.1 KB (30070 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.2.27`

```console
$ docker pull composer@sha256:41f3f5d851d627fd5b366c70aed952205bcc3d15b7e4fec6a06f63fb41ae284c
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

### `composer:2.2.27` - linux; amd64

```console
$ docker pull composer@sha256:1d4c34f32a20484007c6eb4de0b260176fea87afc679390ad59d651bcaf89521
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (78041261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8bbcca4d758e821ee248655c18fcc426631d1c02aa6c1d2ff48fae7dd8c9b30`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:17:52 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:17:52 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:17:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:17:52 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:17:52 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:17:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:17:52 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:17:52 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 15 Apr 2026 20:17:52 GMT
ENV PHP_VERSION=8.5.5
# Wed, 15 Apr 2026 20:17:52 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Wed, 15 Apr 2026 20:17:52 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Wed, 15 Apr 2026 20:17:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 20:17:56 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:21:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 20:21:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:21:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 20:21:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 20:21:24 GMT
CMD ["php" "-a"]
# Wed, 15 Apr 2026 21:27:10 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Wed, 15 Apr 2026 21:27:10 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Wed, 15 Apr 2026 21:27:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 15 Apr 2026 21:27:25 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 15 Apr 2026 21:27:25 GMT
ENV COMPOSER_VERSION=2.2.27
# Wed, 15 Apr 2026 21:27:25 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Wed, 15 Apr 2026 21:27:25 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 21:27:25 GMT
WORKDIR /app
# Wed, 15 Apr 2026 21:27:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:27:25 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7575019b1e32c16a639f3988d9a63ff1c22c036099e3cb267ea5a97ba0fcb31b`  
		Last Modified: Wed, 15 Apr 2026 20:21:32 GMT  
		Size: 3.6 MB (3587447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba54b7e6d1307c692fb0f98a7bb785c3ae59fda44cbd8dc735eb6d32da25bb2`  
		Last Modified: Wed, 15 Apr 2026 20:21:32 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7367014229e0f5079d78d9d65f87aeb106ffa42ef3cacfdde5ccae68a710662d`  
		Last Modified: Wed, 15 Apr 2026 20:21:32 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c74770868277c77b3c7d8e5aa987ffc0183e76f8a003e5ee3e5662475be115`  
		Last Modified: Wed, 15 Apr 2026 20:21:33 GMT  
		Size: 14.4 MB (14379186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f1108694a36c05d3950260f3491806016ec3ab9ba1da15154bda777858d1eb`  
		Last Modified: Wed, 15 Apr 2026 20:21:33 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e321e76cc80892e05feb16337063a65959f21cd03508ea9f6dd1316bd2bfee6`  
		Last Modified: Wed, 15 Apr 2026 20:21:34 GMT  
		Size: 22.5 MB (22528821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2af3ca59c901474266aab6d50192f869e507a229be1b7493e312a32fac0dff9`  
		Last Modified: Wed, 15 Apr 2026 20:21:33 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b12841ff7824946e17f91cf31b444d9a97e15dc30fa55d79e32ae0c00cf27f1`  
		Last Modified: Wed, 15 Apr 2026 20:21:34 GMT  
		Size: 23.4 KB (23395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57079944d1b1c6704b62a38554cbc9eac518eef26bfc4c63ef53dd521e1a266a`  
		Last Modified: Wed, 15 Apr 2026 21:27:36 GMT  
		Size: 32.8 MB (32828035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a085d68ed874eff7f3791196e945d0b56fb9ce296431a7694dd6103638f9329d`  
		Last Modified: Wed, 15 Apr 2026 21:27:35 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd60a45d71c336e91431bf5499d20771638f2cd038be398e13d2aabcc420304d`  
		Last Modified: Wed, 15 Apr 2026 21:27:35 GMT  
		Size: 825.3 KB (825333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:960478e0021327b3f30ffb74841f0d37450c8a5f3a2d4f2f436ccfd70599c409`  
		Last Modified: Wed, 15 Apr 2026 21:27:35 GMT  
		Size: 415.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0c8584100e6db2c11c24c170d1cfce6261a0dbc860141d442ebf8c4b424c48`  
		Last Modified: Wed, 15 Apr 2026 21:27:36 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.27` - unknown; unknown

```console
$ docker pull composer@sha256:06d4d7fa0f03920a6c240e4d072729bdc46987538c5c68aab2ef317aa293e366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2208131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46c769bdd88077126f37041220fded1436c759dff2346e89f6aef997cd325fe0`

```dockerfile
```

-	Layers:
	-	`sha256:e2e99e8ba5356443dbad29b06bc4190a3957e90425a5fb77e98fedd71536a283`  
		Last Modified: Wed, 15 Apr 2026 21:27:35 GMT  
		Size: 2.2 MB (2178067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de1298dfa730854ddb3bf4fac787e6bc8a2aaf92684c3cf519f5366a43fc62f7`  
		Last Modified: Wed, 15 Apr 2026 21:27:35 GMT  
		Size: 30.1 KB (30064 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.27` - linux; arm variant v6

```console
$ docker pull composer@sha256:837725d87752ddf8ddaab26e64b1ab5cf4bbd15695a94e6334c1fab69292228e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74547326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c38c96f2e01f008b141aeae286848621bba080e9e98d2dc2987863029894fb74`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:19:04 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:19:04 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:19:04 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:19:04 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:19:05 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:19:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:19:05 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:19:05 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:19:05 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 15 Apr 2026 20:19:05 GMT
ENV PHP_VERSION=8.5.5
# Wed, 15 Apr 2026 20:19:05 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Wed, 15 Apr 2026 20:19:05 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Wed, 15 Apr 2026 20:19:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 20:19:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:22:18 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 20:22:18 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:22:19 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 20:22:19 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 20:22:19 GMT
CMD ["php" "-a"]
# Wed, 15 Apr 2026 21:22:04 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Wed, 15 Apr 2026 21:22:04 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Wed, 15 Apr 2026 21:22:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 15 Apr 2026 21:22:28 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 15 Apr 2026 21:22:28 GMT
ENV COMPOSER_VERSION=2.2.27
# Wed, 15 Apr 2026 21:22:28 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Wed, 15 Apr 2026 21:22:28 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 21:22:28 GMT
WORKDIR /app
# Wed, 15 Apr 2026 21:22:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:22:28 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1d167fc497e35df23f81ef7d507ee40c904d148d7c5e239db360263ce1228f`  
		Last Modified: Wed, 15 Apr 2026 20:22:24 GMT  
		Size: 3.5 MB (3543048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7893272fc58b639fcb274b9cdac380a99a02b7fec1370991d7043a8d745ee731`  
		Last Modified: Wed, 15 Apr 2026 20:22:24 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b5e2d5fa2204fe8d000332835281efd2beeb4e2b1233fda8377dc9fb8d273da`  
		Last Modified: Wed, 15 Apr 2026 20:22:24 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a237864e95f05b7c9e05c3272f303c8616f39f4b50a113166e6e93f5d6eb2867`  
		Last Modified: Wed, 15 Apr 2026 20:22:25 GMT  
		Size: 14.4 MB (14379195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d6cac0622b9c4733975c694271b5cfe4e9e251f5a29439c27931c4334db09d`  
		Last Modified: Wed, 15 Apr 2026 20:22:25 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a5b1613ded78de2dd5fc3a3cbb57bc91cb6f35c9bf29e262676641888899d35`  
		Last Modified: Wed, 15 Apr 2026 20:22:26 GMT  
		Size: 19.5 MB (19534950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7326187f367c7e04eed9c7cfd2fd94e264bdf5da29600b25762d89f896ee8df`  
		Last Modified: Wed, 15 Apr 2026 20:22:26 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf7aab9524160d3a6dc903858b7d9fc9d77b6f4a09bb6c0cdb0b86eca60acbc`  
		Last Modified: Wed, 15 Apr 2026 20:22:26 GMT  
		Size: 23.2 KB (23204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2c6c58668e522a6546d30e2e0d16f1dc9e65b33a4eeba969e3d61ebb9564fe`  
		Last Modified: Wed, 15 Apr 2026 21:22:36 GMT  
		Size: 32.7 MB (32665512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4947bf681a71f88ccd9a5bb3e83617056fbb25d6034988a7a79a9c8a97b9b05`  
		Last Modified: Wed, 15 Apr 2026 21:22:35 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d63524fbedb3794d475380667167823a9cbb05b4b2506370321caf12069d03f`  
		Last Modified: Wed, 15 Apr 2026 21:22:35 GMT  
		Size: 824.7 KB (824705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eec0de4e89259ab68dad0ab2735d78fa9821e858d1fb905df3c56031c6e0179`  
		Last Modified: Wed, 15 Apr 2026 21:22:35 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5acf5eb8d2fa0eb48c0426b92564b2a5371288eebcd7411ccfd0969b94e969a`  
		Last Modified: Wed, 15 Apr 2026 21:22:36 GMT  
		Size: 91.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.27` - unknown; unknown

```console
$ docker pull composer@sha256:870c19dd765a60097046d1f263461934823473ae9e1c7b16e5ad11e7ef213808
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.9 KB (29939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de96a4283a356a91c500ba91940cb9564592a86f12b7c3e63eb315e1dc75d09c`

```dockerfile
```

-	Layers:
	-	`sha256:53229572f116c44a9361a208605236ab8184f7a741f3f2fe56eee787f318be0f`  
		Last Modified: Wed, 15 Apr 2026 21:22:35 GMT  
		Size: 29.9 KB (29939 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.27` - linux; arm variant v7

```console
$ docker pull composer@sha256:da8d666b84e463409180c65f13ddad9cc253f0a1d44e27411473db9735a952c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 MB (71375730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41452a589beba75b286d0eefef40649738e54779a0e0d48db722b53db61d643d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:18:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:18:22 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:18:22 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:18:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:18:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:18:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:18:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:18:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:18:22 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 15 Apr 2026 20:18:22 GMT
ENV PHP_VERSION=8.5.5
# Wed, 15 Apr 2026 20:18:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Wed, 15 Apr 2026 20:18:22 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Wed, 15 Apr 2026 20:18:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 20:18:26 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:21:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 20:21:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:21:34 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 20:21:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 20:21:34 GMT
CMD ["php" "-a"]
# Wed, 15 Apr 2026 21:32:23 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Wed, 15 Apr 2026 21:32:23 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Wed, 15 Apr 2026 21:32:44 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 15 Apr 2026 21:32:44 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 15 Apr 2026 21:32:44 GMT
ENV COMPOSER_VERSION=2.2.27
# Wed, 15 Apr 2026 21:32:44 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Wed, 15 Apr 2026 21:32:44 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 21:32:44 GMT
WORKDIR /app
# Wed, 15 Apr 2026 21:32:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:32:44 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40243011337e75e1e1aba1a01eff0f25c670f2784f31a19fe3ceeb28d9cbb386`  
		Last Modified: Wed, 15 Apr 2026 20:21:41 GMT  
		Size: 3.3 MB (3343352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289d25cb3dc6bf4d1acfe704c1d05a812b84cbfe26b06c6e9a423f281efcfd64`  
		Last Modified: Wed, 15 Apr 2026 20:21:41 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457ef191b478c4407082d1c51e695feac2f4425353d54d5d6737f8e3aede1686`  
		Last Modified: Wed, 15 Apr 2026 20:21:41 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef8f20263bc5a42b03699b180b432cb94cb313e98aed5a4238024d8cd3f252ad`  
		Last Modified: Wed, 15 Apr 2026 20:21:41 GMT  
		Size: 14.4 MB (14379203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654a3e48df9d037dc7d582e4d7e753ead3d5f55b619c07d29f0f2701eabf4657`  
		Last Modified: Wed, 15 Apr 2026 20:21:43 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00b79e1670ab000b58c3fa612bf97d881357d5a02a37a01aab4448a263a56aa`  
		Last Modified: Wed, 15 Apr 2026 20:21:43 GMT  
		Size: 18.4 MB (18430268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:670c3d79616cd5914f7e4d0d94505d6570f152e3fab437081ba1b2499bf253df`  
		Last Modified: Wed, 15 Apr 2026 20:21:43 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773025cf5591ee7e2a345d9e429358f0269bd41230fb2da781a05eb990ef0386`  
		Last Modified: Wed, 15 Apr 2026 20:21:43 GMT  
		Size: 23.2 KB (23204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8163cc06504257b3d8fa509d21f60978ceefa1cd472dacc146e9060cfefd59ee`  
		Last Modified: Wed, 15 Apr 2026 21:32:54 GMT  
		Size: 31.1 MB (31096177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0da6dabec8b02c8a57a39ddf59fb2cee0a1c872ee63dfd2f2977bae39ff3da`  
		Last Modified: Wed, 15 Apr 2026 21:32:53 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3066dceebf735a3db5b17414e50d2afb21885ae7c8675adf8872105dec35f861`  
		Last Modified: Wed, 15 Apr 2026 21:32:53 GMT  
		Size: 815.6 KB (815555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef3ff58287779bb6f576bb1b79533f8679c2860ea4b5f32fa98203a8d03eaa94`  
		Last Modified: Wed, 15 Apr 2026 21:32:53 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f00f263c0c2026cb35f98332303a28dd1d9cd3173c35bcdb8b80e1eeed2901`  
		Last Modified: Wed, 15 Apr 2026 21:32:54 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.27` - unknown; unknown

```console
$ docker pull composer@sha256:760301001eb8c3052619f101a64223d4afb601923e2ec45c82508b3c6e0a2379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2207876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abbe5388a5ba79dd2a15717dca5ecb25e1d7d8d8589402d9bfe9d1b8c7d2682f`

```dockerfile
```

-	Layers:
	-	`sha256:a87c0263dff8bc23768953af3224577f37510cd7ae2a73dd3dfe81098328e653`  
		Last Modified: Wed, 15 Apr 2026 21:32:53 GMT  
		Size: 2.2 MB (2177722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db09aa483fb8cc3d156aacedb12a66da7d8fdd5f1b358a4ed1d5676d3677327f`  
		Last Modified: Wed, 15 Apr 2026 21:32:53 GMT  
		Size: 30.2 KB (30154 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.27` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:de12a763512eefc03bf209f5ee8d95b7ce1e9b6f424654485686e5039ac734e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.7 MB (77696381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b1452a0f806645bd2dbcd3d38a18a64b5cebba142b836475a0b5c610d89082f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:21 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:16:21 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:16:21 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:16:21 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:16:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:16:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:16:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:16:21 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:16:21 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 15 Apr 2026 20:16:21 GMT
ENV PHP_VERSION=8.5.5
# Wed, 15 Apr 2026 20:16:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Wed, 15 Apr 2026 20:16:21 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Wed, 15 Apr 2026 20:16:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 20:16:25 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:19:57 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 20:19:57 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:19:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 20:19:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 20:19:58 GMT
CMD ["php" "-a"]
# Wed, 15 Apr 2026 21:40:25 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Wed, 15 Apr 2026 21:40:25 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Wed, 15 Apr 2026 21:40:45 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 15 Apr 2026 21:40:45 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 15 Apr 2026 21:40:45 GMT
ENV COMPOSER_VERSION=2.2.27
# Wed, 15 Apr 2026 21:40:45 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Wed, 15 Apr 2026 21:40:45 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 21:40:45 GMT
WORKDIR /app
# Wed, 15 Apr 2026 21:40:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:40:45 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e4c5bcbf8c3068a7d4c178cdd5132463fa53adf8c55efe0d5a02126d958e69`  
		Last Modified: Wed, 15 Apr 2026 20:20:06 GMT  
		Size: 3.6 MB (3596134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c0edc310dc19501413b5668245bc984741c4ac5a3219932a74e83fb33b6f94`  
		Last Modified: Wed, 15 Apr 2026 20:20:02 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d665080207d06b6b7246d46376f6ec0b3a5d072b47f01ab3fe89eb95ea0b9310`  
		Last Modified: Wed, 15 Apr 2026 20:20:02 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e92dbfc45c4b506749680c4bded773db9170a5c594ae07c33aa938ac9b46a1c`  
		Last Modified: Wed, 15 Apr 2026 20:20:07 GMT  
		Size: 14.4 MB (14379192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da631dfa865e2d394e47bb93c95f041d309af42b22cd597826fab10299773bc`  
		Last Modified: Wed, 15 Apr 2026 20:20:03 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0885f624969f9911f18390a16714e49ddcba2831ee9c8002d794ee56d8ca9ca8`  
		Last Modified: Wed, 15 Apr 2026 20:20:07 GMT  
		Size: 21.7 MB (21697840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e202517af7cb78a86ff7f8b255ca452261912c8830cf0b7e352386b5c5472454`  
		Last Modified: Wed, 15 Apr 2026 20:20:05 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4062a55681ba2c31424930678c18614b1e9e0eb63f551ee5faaa3857658f4f0`  
		Last Modified: Wed, 15 Apr 2026 20:20:07 GMT  
		Size: 23.2 KB (23209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21fa51673c1b1fb1e3a5b0375d97adccdf20a311f0f8b37c97b2fe70160269f3`  
		Last Modified: Wed, 15 Apr 2026 21:40:56 GMT  
		Size: 33.0 MB (32971367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ef903a9ac3d2369ad60193a24a651e6966d2782be4c36e46b1ee195f45a06e`  
		Last Modified: Wed, 15 Apr 2026 21:40:55 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29a53602668c6febf8628b803a39aa1989644ac101845a846a0ce4ed5e39466`  
		Last Modified: Wed, 15 Apr 2026 21:40:55 GMT  
		Size: 823.9 KB (823918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15c35b1758e67f72c86b8de7a08e1a059ed64a12fc5210e2be6872e3c09726d1`  
		Last Modified: Wed, 15 Apr 2026 21:40:55 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19efc57a96ea43f4c5e0c49c9936f6a3d16268b6c75e27975289d8e36717117d`  
		Last Modified: Wed, 15 Apr 2026 21:40:56 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.27` - unknown; unknown

```console
$ docker pull composer@sha256:67b85ec6315145d387798071ba07f8d99cb5b11b25bf7a8315694cc3d7f312ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2207718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff48fd5266f995141a6dc18c85cfc2406e468fca6b24de0e7b147b634f0ca661`

```dockerfile
```

-	Layers:
	-	`sha256:07abefe7db6f47eae953c963e1b3a27c16ed1d3fa9adac816f9e198e67438e71`  
		Last Modified: Wed, 15 Apr 2026 21:40:55 GMT  
		Size: 2.2 MB (2177544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3619f43de94dad8331a15aab0d281fb653ef0bd905a88215519186c5039c09b7`  
		Last Modified: Wed, 15 Apr 2026 21:40:55 GMT  
		Size: 30.2 KB (30174 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.27` - linux; 386

```console
$ docker pull composer@sha256:35f5329693ba247b75cdf7c773f0ebd55e0e3b9da051c03699b7c9e0abb71cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.3 MB (82285109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:748b8a46da60c2b55abee6ef41e5a4f80192a39cdfcdf03aaad1775dd05a512e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Fri, 10 Apr 2026 00:13:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 10 Apr 2026 00:13:16 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 10 Apr 2026 00:13:16 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 10 Apr 2026 00:13:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 10 Apr 2026 00:13:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 10 Apr 2026 00:13:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 10 Apr 2026 00:13:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 10 Apr 2026 00:13:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 10 Apr 2026 00:13:16 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 10 Apr 2026 00:13:16 GMT
ENV PHP_VERSION=8.5.5
# Fri, 10 Apr 2026 00:13:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Fri, 10 Apr 2026 00:13:16 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Fri, 10 Apr 2026 00:13:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 10 Apr 2026 00:13:20 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 00:16:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 10 Apr 2026 00:16:53 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 00:16:54 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 10 Apr 2026 00:16:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 10 Apr 2026 00:16:54 GMT
CMD ["php" "-a"]
# Tue, 14 Apr 2026 18:19:28 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Apr 2026 18:19:28 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Apr 2026 18:20:22 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Apr 2026 18:20:22 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Apr 2026 18:20:22 GMT
ENV COMPOSER_VERSION=2.2.27
# Tue, 14 Apr 2026 18:20:22 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Apr 2026 18:20:22 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Apr 2026 18:20:22 GMT
WORKDIR /app
# Tue, 14 Apr 2026 18:20:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Apr 2026 18:20:22 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d2062b0536d4d6a1543e3a6bfd55452c7706979a7def0ad5ff0f3e183f183d`  
		Last Modified: Fri, 10 Apr 2026 00:17:02 GMT  
		Size: 5.9 MB (5909460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb9b53f46bb29bde8242534cc51035c71b65536a0a0acada6428f7a8ba0889c`  
		Last Modified: Fri, 10 Apr 2026 00:17:02 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab50b39601a88f935ec690047331c7481ff9b7ae2bb959cfc4cc98313c492986`  
		Last Modified: Fri, 10 Apr 2026 00:17:02 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92225e063d6f653398ed45adcff1579a3a3cf3ccbe764a4bb5b301283ee3b2ee`  
		Last Modified: Fri, 10 Apr 2026 00:17:02 GMT  
		Size: 14.4 MB (14379292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ccaecce131db93828716f892d3ad6e523dec70db239cc1bed3bb5394e8396c`  
		Last Modified: Fri, 10 Apr 2026 00:17:03 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e4efa73be7dce94cd5df6088620edcd50156eafe81c782274c129a7a3e191d`  
		Last Modified: Fri, 10 Apr 2026 00:17:04 GMT  
		Size: 23.4 MB (23438953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab8684032f9c15ecd79788e50ca55f90486d5bf79b5b3a24018772984e7a1cb5`  
		Last Modified: Fri, 10 Apr 2026 00:17:04 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba72ff6334ace2c9a0d737cdf3c0fa9f61f267a07af45bf21e2ff77820277e5`  
		Last Modified: Fri, 10 Apr 2026 00:17:04 GMT  
		Size: 23.6 KB (23625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb92bca6a7200abd5ed57acbc2406d1b631ce897e9fcb8321df6d6ad30cb6114`  
		Last Modified: Tue, 14 Apr 2026 18:19:58 GMT  
		Size: 33.4 MB (33354023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3acb4361787726cd8ad52c3d9467b84e1d1aa7dfe6414e7e3be8d2816cc76617`  
		Last Modified: Tue, 14 Apr 2026 18:19:57 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649871246b4636d3e71336ce00677bad781148c88f1b63a1358cf436f11feac4`  
		Last Modified: Tue, 14 Apr 2026 18:20:28 GMT  
		Size: 1.5 MB (1487908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db2ceeac24b57d267726c3a0854b3db4a10c8f8be761f7f653a0c97fc86e57d`  
		Last Modified: Tue, 14 Apr 2026 18:20:28 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b0fc048d318578d95fbcda07a86c87b70bb13465e4a96a6f8cd472ba6b7fc5`  
		Last Modified: Tue, 14 Apr 2026 18:20:28 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.27` - unknown; unknown

```console
$ docker pull composer@sha256:6884a4f582cf2cce11394bbc1245585b552aa80cf36ceb1c9d4ef7f115bf1e39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2209886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af552b456c5f7c8ba7208226abe75e9da9e899a0cf7f25b20762f8ba266a59e2`

```dockerfile
```

-	Layers:
	-	`sha256:f642b0c6b11ef666fee6cf07735b6410a1f0c832aceb20154fc0006c77c66794`  
		Last Modified: Tue, 14 Apr 2026 18:20:28 GMT  
		Size: 2.2 MB (2179845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffe56978f8a88a319c332992e7ef101b50d32c77831087a868f2c4c7872fb94b`  
		Last Modified: Tue, 14 Apr 2026 18:20:28 GMT  
		Size: 30.0 KB (30041 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.27` - linux; ppc64le

```console
$ docker pull composer@sha256:3bc9df9d34e445d60475370f8bf6ca3238a9de88a772bb54a4cb5978ed15739a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 MB (96516566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1ee0ee938940b40491579bf9c0a7ba8ecda47725576918950bf7b239cd7aa26`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Thu, 12 Mar 2026 23:53:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Mar 2026 23:53:02 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Mar 2026 23:53:02 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Mar 2026 23:53:02 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Mar 2026 23:53:02 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Mar 2026 23:53:02 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Mar 2026 23:53:02 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Mar 2026 23:53:02 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Mar 2026 23:53:02 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 12 Mar 2026 23:53:02 GMT
ENV PHP_VERSION=8.5.5
# Thu, 12 Mar 2026 23:53:02 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Thu, 12 Mar 2026 23:53:02 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Thu, 09 Apr 2026 22:33:42 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 09 Apr 2026 22:33:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:38:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 09 Apr 2026 22:38:29 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:38:30 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 09 Apr 2026 22:38:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 09 Apr 2026 22:38:30 GMT
CMD ["php" "-a"]
# Fri, 10 Apr 2026 00:21:05 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 10 Apr 2026 00:21:07 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Apr 2026 18:19:02 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Apr 2026 18:19:02 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Apr 2026 18:19:02 GMT
ENV COMPOSER_VERSION=2.2.27
# Tue, 14 Apr 2026 18:19:02 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Apr 2026 18:19:05 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Apr 2026 18:19:09 GMT
WORKDIR /app
# Tue, 14 Apr 2026 18:19:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Apr 2026 18:19:09 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7db1cc7b26f64d5de44e75f81962c30dead7dbc1dae3ebb93d0dc3d0cea721a`  
		Last Modified: Thu, 12 Mar 2026 23:58:51 GMT  
		Size: 3.8 MB (3768852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4a23ff5963c3f844b77db123769c733318f6ad54386c9f63e356424059470b`  
		Last Modified: Thu, 12 Mar 2026 23:58:51 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a071b7623ea30b2e8950858971a7e7838856db9c469a46b6305dcd619d0531fc`  
		Last Modified: Thu, 12 Mar 2026 23:58:51 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d012a34014d339e95156eab3252cc22fbae82a4670be3766b110c04e96ff1a17`  
		Last Modified: Thu, 09 Apr 2026 22:38:45 GMT  
		Size: 14.4 MB (14379301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8b7c5afa56dcdf0f01aaba59b305697db6b72603309ba573605f5fcd422fc0`  
		Last Modified: Thu, 09 Apr 2026 22:38:45 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1971acbe5d44b0f37d3698908a5766cea69f16ef4c4472ca8a30f5d48eec93ec`  
		Last Modified: Thu, 09 Apr 2026 22:38:46 GMT  
		Size: 23.1 MB (23118163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ee71922b29fe2228fde987804ee785c857383e7941a35e885bb5f06b7c3aba`  
		Last Modified: Thu, 09 Apr 2026 22:38:45 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fbefb03f1cf2736ed7b9f334b7e8f2f16dbedad1876c833ba4682b99ca9f99a`  
		Last Modified: Thu, 09 Apr 2026 22:38:46 GMT  
		Size: 23.4 KB (23442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db29015527299944deffccc76c5bfb597208be66aea62b09cf37a0cef1bb364e`  
		Last Modified: Fri, 10 Apr 2026 00:22:19 GMT  
		Size: 34.2 MB (34177434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972a41e22feca9d4bfcc298283918766cb03ebb7dd146ebbded895c8b431c973`  
		Last Modified: Fri, 10 Apr 2026 00:22:17 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a00b8129dae026b4288901fdf4844d14631360cd95724ef7a99b65dab607a3a7`  
		Last Modified: Tue, 14 Apr 2026 18:19:38 GMT  
		Size: 17.2 MB (17214867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b642fc002306ffa035fabc99948ab54d676222458872361b5da11d126da7f4a9`  
		Last Modified: Tue, 14 Apr 2026 18:19:38 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33f861bae9f5ec9825aa85d366c341ad622e0c26fad222ee7341b19546dfac2`  
		Last Modified: Tue, 14 Apr 2026 18:19:38 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.27` - unknown; unknown

```console
$ docker pull composer@sha256:a1c93648e57614e4c8f0dcf7199c333eeda49c94176869dc05e8f7de304f3cf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2210002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6040621f06dbe2c2a62e88287ee16b383a874ac09143e68a6d024651c828f7e3`

```dockerfile
```

-	Layers:
	-	`sha256:9d93dcd35f40f1b73d8e6aab1f0ad312cef0d127b4d9561162774bc7ed41925d`  
		Last Modified: Tue, 14 Apr 2026 18:19:37 GMT  
		Size: 2.2 MB (2179896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2a711e174b0c511983fc08afe41d592f4c8cf2cf2facda7a2594455b610ba0b`  
		Last Modified: Tue, 14 Apr 2026 18:19:37 GMT  
		Size: 30.1 KB (30106 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.27` - linux; riscv64

```console
$ docker pull composer@sha256:cf698321e756d82bc12e24f70c655b5d1daf8ed9e605cee5c19a8140aea3fd33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77909972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fe71051367b5659b8bb62a70a49db12f4724db7aee6fde4c3fb22601ce02e9f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 09:13:06 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 28 Jan 2026 09:13:06 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 28 Jan 2026 09:13:06 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 28 Jan 2026 09:13:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 28 Jan 2026 09:13:07 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 28 Jan 2026 09:13:07 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_VERSION=8.5.5
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Fri, 10 Apr 2026 09:29:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 10 Apr 2026 09:29:21 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 10:28:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 10 Apr 2026 10:28:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 10:28:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 10 Apr 2026 10:28:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 10 Apr 2026 10:28:33 GMT
CMD ["php" "-a"]
# Sun, 12 Apr 2026 09:33:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Sun, 12 Apr 2026 09:33:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Apr 2026 18:28:51 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Apr 2026 18:28:51 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Apr 2026 18:28:51 GMT
ENV COMPOSER_VERSION=2.2.27
# Tue, 14 Apr 2026 18:28:51 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Apr 2026 18:28:51 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Apr 2026 18:28:51 GMT
WORKDIR /app
# Tue, 14 Apr 2026 18:28:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Apr 2026 18:28:51 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d64a68485fdb9ab2ec4159ac3e04e0bb79d9f1d037e580e928ca2b9604180f`  
		Last Modified: Wed, 28 Jan 2026 10:13:59 GMT  
		Size: 3.7 MB (3741000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b030c1b113432578231e8fe7c8a1bc913f2dc5dcba512e805fa9ab07768c9bd4`  
		Last Modified: Wed, 28 Jan 2026 10:13:58 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32a0e9bcb36b34307b4eada1f50c1cd4244d43d19ee57d962818dcb0ff0b110`  
		Last Modified: Wed, 28 Jan 2026 10:13:58 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20501e9e3d17b72af47b7d522d0c369998be222ed66ed9070ed2cbc45e500ca7`  
		Last Modified: Fri, 10 Apr 2026 10:29:42 GMT  
		Size: 14.4 MB (14379290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f7fa0bbe8ea35a7aeededb6a1c62d4e192d88a3cbaa6a9ac613390cef5f797e`  
		Last Modified: Fri, 10 Apr 2026 10:29:38 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c00b6c348638ca2fb138534e98df3a83c5788350e7f682c5dab61388d5988a1`  
		Last Modified: Fri, 10 Apr 2026 10:29:43 GMT  
		Size: 20.8 MB (20772153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf32615937490fdbee93796b59955ce07e051f019b76917819692421da228ef`  
		Last Modified: Fri, 10 Apr 2026 10:29:38 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491cab84c5a842c690a34c22c4cfe20f23d7b27019ca9d80e387fd23ef96828d`  
		Last Modified: Fri, 10 Apr 2026 10:29:39 GMT  
		Size: 23.3 KB (23349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e865e7a35bee8605e802d4714eef1a4cd079ed0b68a414c076e698d97cfbedd6`  
		Last Modified: Sun, 12 Apr 2026 09:38:57 GMT  
		Size: 31.3 MB (31300012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:670c7192db5936f38910b865b3f6746b70a4b2523b1e25db7d274900db0fca4f`  
		Last Modified: Sun, 12 Apr 2026 09:38:52 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5bdd2e2f534ae25a788c0f4fe04db08c09d85e043bff17c4238b4c5c6e12e2`  
		Last Modified: Tue, 14 Apr 2026 18:30:04 GMT  
		Size: 4.1 MB (4104012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1ca5c26ad5a331c9c78d1736a316cd75130f2c5fc620da2614c677c1610b79`  
		Last Modified: Tue, 14 Apr 2026 18:30:03 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd33bb4fad3f92609198afdae7d92af15161acef56cb4c6f80fa7a9cdefa0c3`  
		Last Modified: Tue, 14 Apr 2026 18:29:56 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.27` - unknown; unknown

```console
$ docker pull composer@sha256:d499efcf872dd10295b0361b3f735682b694176478d8de89f6e9ed88975b6fef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2208939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a4e7210e9321acd0aa206f7db001b89b492df5fd3f869de1f7910b3ebcaca37`

```dockerfile
```

-	Layers:
	-	`sha256:e1ebc611e5beb930a14f43da834427bd8cba5278ee9b1ae4178ff4cba263cbd8`  
		Last Modified: Tue, 14 Apr 2026 18:30:03 GMT  
		Size: 2.2 MB (2178837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c1b2893b53b2641c74019ec997c6cd50ba35ff87e1cc59416af349b182e62ef`  
		Last Modified: Tue, 14 Apr 2026 18:30:03 GMT  
		Size: 30.1 KB (30102 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.27` - linux; s390x

```console
$ docker pull composer@sha256:093e24e420e8a8867177194221f361d676048cacadf0270ba0b9f58bbf5b2ada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.1 MB (93052143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61dc9356e7aa5e6362a5b41607515476a6800d97e3fbbfc6bdd998a0b89de4db`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Mar 2026 23:37:17 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Mar 2026 23:37:17 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Mar 2026 23:37:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Mar 2026 23:37:17 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHP_VERSION=8.5.5
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Thu, 09 Apr 2026 22:21:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 09 Apr 2026 22:21:35 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:27:00 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 09 Apr 2026 22:27:00 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:27:01 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 09 Apr 2026 22:27:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 09 Apr 2026 22:27:01 GMT
CMD ["php" "-a"]
# Thu, 09 Apr 2026 23:18:55 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 09 Apr 2026 23:18:55 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Apr 2026 18:19:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Apr 2026 18:19:55 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Apr 2026 18:19:55 GMT
ENV COMPOSER_VERSION=2.2.27
# Tue, 14 Apr 2026 18:19:55 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Apr 2026 18:19:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Apr 2026 18:19:55 GMT
WORKDIR /app
# Tue, 14 Apr 2026 18:19:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Apr 2026 18:19:55 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4348d21358ef752a357c33976b85357317bfb623a79cb91ec462b4e5128b82d5`  
		Last Modified: Thu, 12 Mar 2026 23:43:03 GMT  
		Size: 3.8 MB (3795119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a169c2de4deea9b877eb224ec8f2d4f4502dd0bb4e22037516ea41c23c8c1e6`  
		Last Modified: Thu, 12 Mar 2026 23:43:02 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f88a80dfabed7faa02e1bbe28dd4e26c817c26d54bb3411b27cc398ea997ef8`  
		Last Modified: Thu, 12 Mar 2026 23:43:02 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5e7662fcf96af1dfae3edab12e535e5dbb2bd9336314490ac9484222315cc0`  
		Last Modified: Thu, 09 Apr 2026 22:27:14 GMT  
		Size: 14.4 MB (14379286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b2bd611f10e897bc78163d788b300458c71f27af849508076d219371619381`  
		Last Modified: Thu, 09 Apr 2026 22:27:14 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c1175a23bc886b3bc9f9e6845c90d99d1125fc788f6d88d5ad9501ed086f83`  
		Last Modified: Thu, 09 Apr 2026 22:27:15 GMT  
		Size: 21.9 MB (21889964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48a98f93d43e57e9161beb90862e90db489cf9d4b4d09bfbd7d3bc1566f7981`  
		Last Modified: Thu, 09 Apr 2026 22:27:14 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91cdaaeb755a7dbc3a463542f5d9410ef527eb1babc2850059c13f703b6bf5f`  
		Last Modified: Thu, 09 Apr 2026 22:27:15 GMT  
		Size: 23.4 KB (23427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4fdf3eb0ccd09c5d847e8404ebd00d415ec8a926328bb55405913777275f663`  
		Last Modified: Thu, 09 Apr 2026 23:19:34 GMT  
		Size: 32.1 MB (32113289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:233a242e39cffb8912002ca05f6e84274f01e36739c65884086e484ec1f9ce01`  
		Last Modified: Thu, 09 Apr 2026 23:19:33 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d4eb190454ffaef90be5e6e0c819cb3a9e7a990e97007fc908ab14eb6c53b8`  
		Last Modified: Tue, 14 Apr 2026 18:20:11 GMT  
		Size: 17.1 MB (17120862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d69b603af35c10edfc476777fd1bcdd7a3bf814ea42956731c8ce32d7871b70`  
		Last Modified: Tue, 14 Apr 2026 18:20:10 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30182dd14eb74e4c391867549fbf9c4dfb3eb2bd14ffe94db514ef30c07d544c`  
		Last Modified: Tue, 14 Apr 2026 18:20:10 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.27` - unknown; unknown

```console
$ docker pull composer@sha256:064684950c506dc3ada188dc93ce31604db9827dc2a07eb9cec3ddd72297fa76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2208701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e15954f05e76147d256bb7d2637ffee0a926191203bc152df824c2e93d4ec50f`

```dockerfile
```

-	Layers:
	-	`sha256:414ea970aecb739f4c603b73c40816576cbb8d0bfbc46b5d72cc910ca4773312`  
		Last Modified: Tue, 14 Apr 2026 18:20:10 GMT  
		Size: 2.2 MB (2178631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16aeaa77a826b0c9e08631385e3529effaef99aac59efcaa6ed272e688af12ba`  
		Last Modified: Tue, 14 Apr 2026 18:20:10 GMT  
		Size: 30.1 KB (30070 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.9`

```console
$ docker pull composer@sha256:709a30cb521103db18992786f7fd747010ad8e24cf581817ddf3e53288d3d281
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

### `composer:2.9` - linux; amd64

```console
$ docker pull composer@sha256:a3df561dbdddfdb9832ec50f41c0e2f1d27445a67bd71415f05467fedbb2c3c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.2 MB (78237453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39f4699ce5525450650cad74ebb243efd73730fda6d6011a5d805089f9bc61ce`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:17:52 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:17:52 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:17:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:17:52 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:17:52 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:17:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:17:52 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:17:52 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 15 Apr 2026 20:17:52 GMT
ENV PHP_VERSION=8.5.5
# Wed, 15 Apr 2026 20:17:52 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Wed, 15 Apr 2026 20:17:52 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Wed, 15 Apr 2026 20:17:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 20:17:56 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:21:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 20:21:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:21:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 20:21:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 20:21:24 GMT
CMD ["php" "-a"]
# Wed, 15 Apr 2026 21:27:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Wed, 15 Apr 2026 21:27:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Wed, 15 Apr 2026 21:27:31 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 15 Apr 2026 21:27:31 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 15 Apr 2026 21:27:31 GMT
ENV COMPOSER_VERSION=2.9.7
# Wed, 15 Apr 2026 21:27:31 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Wed, 15 Apr 2026 21:27:31 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 21:27:31 GMT
WORKDIR /app
# Wed, 15 Apr 2026 21:27:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:27:31 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7575019b1e32c16a639f3988d9a63ff1c22c036099e3cb267ea5a97ba0fcb31b`  
		Last Modified: Wed, 15 Apr 2026 20:21:32 GMT  
		Size: 3.6 MB (3587447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba54b7e6d1307c692fb0f98a7bb785c3ae59fda44cbd8dc735eb6d32da25bb2`  
		Last Modified: Wed, 15 Apr 2026 20:21:32 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7367014229e0f5079d78d9d65f87aeb106ffa42ef3cacfdde5ccae68a710662d`  
		Last Modified: Wed, 15 Apr 2026 20:21:32 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c74770868277c77b3c7d8e5aa987ffc0183e76f8a003e5ee3e5662475be115`  
		Last Modified: Wed, 15 Apr 2026 20:21:33 GMT  
		Size: 14.4 MB (14379186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f1108694a36c05d3950260f3491806016ec3ab9ba1da15154bda777858d1eb`  
		Last Modified: Wed, 15 Apr 2026 20:21:33 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e321e76cc80892e05feb16337063a65959f21cd03508ea9f6dd1316bd2bfee6`  
		Last Modified: Wed, 15 Apr 2026 20:21:34 GMT  
		Size: 22.5 MB (22528821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2af3ca59c901474266aab6d50192f869e507a229be1b7493e312a32fac0dff9`  
		Last Modified: Wed, 15 Apr 2026 20:21:33 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b12841ff7824946e17f91cf31b444d9a97e15dc30fa55d79e32ae0c00cf27f1`  
		Last Modified: Wed, 15 Apr 2026 20:21:34 GMT  
		Size: 23.4 KB (23395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e55827933a329097ef03bab9834f516b064faf5b72b18d080e967055a42003`  
		Last Modified: Wed, 15 Apr 2026 21:27:42 GMT  
		Size: 32.8 MB (32828568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2933ad071631f9ce3470578aecae812618fd37d7004987532866b0359f6b6de0`  
		Last Modified: Wed, 15 Apr 2026 21:27:41 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d821667065611cf0d7b4bf7f6d8857b118bfd703fe486289b37884a8edbd61`  
		Last Modified: Wed, 15 Apr 2026 21:27:41 GMT  
		Size: 1.0 MB (1020986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae94261b1892c1af044280991b4f2a5dd150a791ec2eeef5af1ea6d3094479e5`  
		Last Modified: Wed, 15 Apr 2026 21:27:41 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb435422e01857a05128024eb0629a6c60655c0d3b45442ea0bc469f1bbd191`  
		Last Modified: Wed, 15 Apr 2026 21:27:42 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.9` - unknown; unknown

```console
$ docker pull composer@sha256:e85e044ddbc3f14041ddacfb9398391fc8292baa3673ee4c95d5b809632bc41f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2209324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4c877852d538421f4a82316e63e564b40bc167997b6947ce7c9b36533714614`

```dockerfile
```

-	Layers:
	-	`sha256:b9fed10922f5326c3cb699a3c5c5bfb4d7c68743354358d37b16875c5fdd6803`  
		Last Modified: Wed, 15 Apr 2026 21:27:41 GMT  
		Size: 2.2 MB (2178657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:615752e487f6d65b8ad402d079106fe3c4610a7aee9abb3e9350d78067b4501f`  
		Last Modified: Wed, 15 Apr 2026 21:27:41 GMT  
		Size: 30.7 KB (30667 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.9` - linux; arm variant v6

```console
$ docker pull composer@sha256:5f618ede41609642ab0415bf163302848fbba617512b9f3bcb4c81d65aea6016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74743627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e102830ff670832c4941a947728bd57ef6a228b56943b1d8d452c9c6f1e395d8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:19:04 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:19:04 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:19:04 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:19:04 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:19:05 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:19:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:19:05 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:19:05 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:19:05 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 15 Apr 2026 20:19:05 GMT
ENV PHP_VERSION=8.5.5
# Wed, 15 Apr 2026 20:19:05 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Wed, 15 Apr 2026 20:19:05 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Wed, 15 Apr 2026 20:19:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 20:19:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:22:18 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 20:22:18 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:22:19 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 20:22:19 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 20:22:19 GMT
CMD ["php" "-a"]
# Wed, 15 Apr 2026 21:22:04 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Wed, 15 Apr 2026 21:22:04 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Wed, 15 Apr 2026 21:22:27 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 15 Apr 2026 21:22:27 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 15 Apr 2026 21:22:27 GMT
ENV COMPOSER_VERSION=2.9.7
# Wed, 15 Apr 2026 21:22:27 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Wed, 15 Apr 2026 21:22:27 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 21:22:27 GMT
WORKDIR /app
# Wed, 15 Apr 2026 21:22:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:22:27 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1d167fc497e35df23f81ef7d507ee40c904d148d7c5e239db360263ce1228f`  
		Last Modified: Wed, 15 Apr 2026 20:22:24 GMT  
		Size: 3.5 MB (3543048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7893272fc58b639fcb274b9cdac380a99a02b7fec1370991d7043a8d745ee731`  
		Last Modified: Wed, 15 Apr 2026 20:22:24 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b5e2d5fa2204fe8d000332835281efd2beeb4e2b1233fda8377dc9fb8d273da`  
		Last Modified: Wed, 15 Apr 2026 20:22:24 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a237864e95f05b7c9e05c3272f303c8616f39f4b50a113166e6e93f5d6eb2867`  
		Last Modified: Wed, 15 Apr 2026 20:22:25 GMT  
		Size: 14.4 MB (14379195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d6cac0622b9c4733975c694271b5cfe4e9e251f5a29439c27931c4334db09d`  
		Last Modified: Wed, 15 Apr 2026 20:22:25 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a5b1613ded78de2dd5fc3a3cbb57bc91cb6f35c9bf29e262676641888899d35`  
		Last Modified: Wed, 15 Apr 2026 20:22:26 GMT  
		Size: 19.5 MB (19534950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7326187f367c7e04eed9c7cfd2fd94e264bdf5da29600b25762d89f896ee8df`  
		Last Modified: Wed, 15 Apr 2026 20:22:26 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf7aab9524160d3a6dc903858b7d9fc9d77b6f4a09bb6c0cdb0b86eca60acbc`  
		Last Modified: Wed, 15 Apr 2026 20:22:26 GMT  
		Size: 23.2 KB (23204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7338db7ab2e6da871e9ca18bf6e41db656dc01552305f5ea294acd98e45f2ff2`  
		Last Modified: Wed, 15 Apr 2026 21:22:35 GMT  
		Size: 32.7 MB (32665496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acff7d213b0f5a23ec528c0624a11975e61306f0ef4705e003a9109c922c9aaf`  
		Last Modified: Wed, 15 Apr 2026 21:22:34 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ab1a1cc99508981bda26983105462a9a3ee15eae1e24e6da36767b441c2244`  
		Last Modified: Wed, 15 Apr 2026 21:22:34 GMT  
		Size: 1.0 MB (1021023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cff2f6c2aff71864717c706d9c7e23510750ed143e2938cb19d5fdafff8be79`  
		Last Modified: Wed, 15 Apr 2026 21:22:34 GMT  
		Size: 416.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2da733922c6146907c3b3634c5c450c96e0638edddca77a676b7cd813427f9`  
		Last Modified: Wed, 15 Apr 2026 21:22:35 GMT  
		Size: 91.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.9` - unknown; unknown

```console
$ docker pull composer@sha256:1eb3fc19c61b35b8a872d9323204996b304beb4dc10e4d11dfd6b5c14cc219a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:784a99b9ab8555f39e0aa608545bfc075b883ab06336eacb31db1b89b4961c24`

```dockerfile
```

-	Layers:
	-	`sha256:1e8a701178ca230dc13cbb78d4e4d281f47957950cbb2e2298d741398449207b`  
		Last Modified: Wed, 15 Apr 2026 21:22:33 GMT  
		Size: 30.6 KB (30557 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.9` - linux; arm variant v7

```console
$ docker pull composer@sha256:582284655bf553416dbce90c395b4dc89da3a7edc9da012ec6e01407c1430ed9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.6 MB (71571453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f9ac974387fafeac611e90eeb97b0514811d16f37141c1796d8eebb9f19295e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:18:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:18:22 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:18:22 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:18:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:18:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:18:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:18:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:18:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:18:22 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 15 Apr 2026 20:18:22 GMT
ENV PHP_VERSION=8.5.5
# Wed, 15 Apr 2026 20:18:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Wed, 15 Apr 2026 20:18:22 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Wed, 15 Apr 2026 20:18:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 20:18:26 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:21:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 20:21:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:21:34 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 20:21:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 20:21:34 GMT
CMD ["php" "-a"]
# Wed, 15 Apr 2026 21:32:22 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Wed, 15 Apr 2026 21:32:22 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Wed, 15 Apr 2026 21:32:44 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 15 Apr 2026 21:32:44 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 15 Apr 2026 21:32:44 GMT
ENV COMPOSER_VERSION=2.9.7
# Wed, 15 Apr 2026 21:32:44 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Wed, 15 Apr 2026 21:32:44 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 21:32:45 GMT
WORKDIR /app
# Wed, 15 Apr 2026 21:32:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:32:45 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40243011337e75e1e1aba1a01eff0f25c670f2784f31a19fe3ceeb28d9cbb386`  
		Last Modified: Wed, 15 Apr 2026 20:21:41 GMT  
		Size: 3.3 MB (3343352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289d25cb3dc6bf4d1acfe704c1d05a812b84cbfe26b06c6e9a423f281efcfd64`  
		Last Modified: Wed, 15 Apr 2026 20:21:41 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457ef191b478c4407082d1c51e695feac2f4425353d54d5d6737f8e3aede1686`  
		Last Modified: Wed, 15 Apr 2026 20:21:41 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef8f20263bc5a42b03699b180b432cb94cb313e98aed5a4238024d8cd3f252ad`  
		Last Modified: Wed, 15 Apr 2026 20:21:41 GMT  
		Size: 14.4 MB (14379203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654a3e48df9d037dc7d582e4d7e753ead3d5f55b619c07d29f0f2701eabf4657`  
		Last Modified: Wed, 15 Apr 2026 20:21:43 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00b79e1670ab000b58c3fa612bf97d881357d5a02a37a01aab4448a263a56aa`  
		Last Modified: Wed, 15 Apr 2026 20:21:43 GMT  
		Size: 18.4 MB (18430268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:670c3d79616cd5914f7e4d0d94505d6570f152e3fab437081ba1b2499bf253df`  
		Last Modified: Wed, 15 Apr 2026 20:21:43 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773025cf5591ee7e2a345d9e429358f0269bd41230fb2da781a05eb990ef0386`  
		Last Modified: Wed, 15 Apr 2026 20:21:43 GMT  
		Size: 23.2 KB (23204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acebb0a04354316add548495911389085f450934caee74f83d543b9e72b2d05e`  
		Last Modified: Wed, 15 Apr 2026 21:32:54 GMT  
		Size: 31.1 MB (31096001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a09a4d2f176f1708944c561d076f811601d10ce9c12f67f368beb5f33e872e0`  
		Last Modified: Wed, 15 Apr 2026 21:32:53 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4554ab557c57e190e9a9c96595d8f20842cdf6c58419124406570b03fb325ec8`  
		Last Modified: Wed, 15 Apr 2026 21:32:54 GMT  
		Size: 1.0 MB (1011452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba1c93167f863ddcc1d5c2653b03c6a8642c2fd9559327b73ed8624251ec144`  
		Last Modified: Wed, 15 Apr 2026 21:32:54 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c681ef1dc9504c4c3f4ad0cf3ffc7c285a57f04dbacae219663ef575ca6acf`  
		Last Modified: Wed, 15 Apr 2026 21:32:55 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.9` - unknown; unknown

```console
$ docker pull composer@sha256:32d0c9b1e4d5d571639eb8de3fd2347a367f829d380db08ff8dbf370f5b11cc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2209101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23ebcb2c2afc717904235ca8d45b56e040e43ae27f90d904adef6de85485e0c1`

```dockerfile
```

-	Layers:
	-	`sha256:1ea500bcc75e9906fcbd4ac18fb9f32b00e2f232209a8695dbdd04027eae30b1`  
		Last Modified: Wed, 15 Apr 2026 21:32:54 GMT  
		Size: 2.2 MB (2178328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d85d9fe7060afbbf94f473725bfe33d128da115ed642a56a0a3c11dc35b8ad8a`  
		Last Modified: Wed, 15 Apr 2026 21:32:53 GMT  
		Size: 30.8 KB (30773 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.9` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:02cc0a1729b9f75734a6f1789ad59fa90c54bdb84566b2c7b564f7eaafd5c368
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77892271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b9aa3f48599c920e9268b74581f5d0d24a2eca014342e24e60e1d70f8bfb5ae`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:21 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:16:21 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:16:21 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:16:21 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:16:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:16:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:16:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:16:21 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:16:21 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 15 Apr 2026 20:16:21 GMT
ENV PHP_VERSION=8.5.5
# Wed, 15 Apr 2026 20:16:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Wed, 15 Apr 2026 20:16:21 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Wed, 15 Apr 2026 20:16:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 20:16:25 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:19:57 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 20:19:57 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:19:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 20:19:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 20:19:58 GMT
CMD ["php" "-a"]
# Wed, 15 Apr 2026 21:40:09 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Wed, 15 Apr 2026 21:40:09 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Wed, 15 Apr 2026 21:40:29 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 15 Apr 2026 21:40:29 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 15 Apr 2026 21:40:29 GMT
ENV COMPOSER_VERSION=2.9.7
# Wed, 15 Apr 2026 21:40:29 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Wed, 15 Apr 2026 21:40:29 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 21:40:29 GMT
WORKDIR /app
# Wed, 15 Apr 2026 21:40:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:40:29 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e4c5bcbf8c3068a7d4c178cdd5132463fa53adf8c55efe0d5a02126d958e69`  
		Last Modified: Wed, 15 Apr 2026 20:20:06 GMT  
		Size: 3.6 MB (3596134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c0edc310dc19501413b5668245bc984741c4ac5a3219932a74e83fb33b6f94`  
		Last Modified: Wed, 15 Apr 2026 20:20:02 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d665080207d06b6b7246d46376f6ec0b3a5d072b47f01ab3fe89eb95ea0b9310`  
		Last Modified: Wed, 15 Apr 2026 20:20:02 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e92dbfc45c4b506749680c4bded773db9170a5c594ae07c33aa938ac9b46a1c`  
		Last Modified: Wed, 15 Apr 2026 20:20:07 GMT  
		Size: 14.4 MB (14379192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da631dfa865e2d394e47bb93c95f041d309af42b22cd597826fab10299773bc`  
		Last Modified: Wed, 15 Apr 2026 20:20:03 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0885f624969f9911f18390a16714e49ddcba2831ee9c8002d794ee56d8ca9ca8`  
		Last Modified: Wed, 15 Apr 2026 20:20:07 GMT  
		Size: 21.7 MB (21697840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e202517af7cb78a86ff7f8b255ca452261912c8830cf0b7e352386b5c5472454`  
		Last Modified: Wed, 15 Apr 2026 20:20:05 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4062a55681ba2c31424930678c18614b1e9e0eb63f551ee5faaa3857658f4f0`  
		Last Modified: Wed, 15 Apr 2026 20:20:07 GMT  
		Size: 23.2 KB (23209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247694cf5276fc930925fbd3c766f23524e3c168100355ab0759b2996481c9fe`  
		Last Modified: Wed, 15 Apr 2026 21:40:39 GMT  
		Size: 33.0 MB (32971344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd2df09b94d664b93dffeea3fcc3ec248ab74647c5a4214efe19bfb47fcb05a8`  
		Last Modified: Wed, 15 Apr 2026 21:40:38 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ddb215ec4272be553f5bc3174320405b2f1a91262a8dcef2e0a86a9e49ee716`  
		Last Modified: Wed, 15 Apr 2026 21:40:38 GMT  
		Size: 1.0 MB (1019831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf4152796a067e6883c8510bc549ef6efa7a2938ae8a777ac16b9ce0064b7cb`  
		Last Modified: Wed, 15 Apr 2026 21:40:38 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2e497f91b5d80958253e7e10d4c15d00acc6326888e106b429a9c5308f89fe`  
		Last Modified: Wed, 15 Apr 2026 21:40:39 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.9` - unknown; unknown

```console
$ docker pull composer@sha256:fe7799a0766fcb90d3eee27476e71e060d8359ba6a1af526e40143a0b717c9fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2208959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c81eae5c2a8041b04dcb4644dca7f3e06622961ff2e597b7542f07cfbf49fb89`

```dockerfile
```

-	Layers:
	-	`sha256:b2e0891d2073a415183d3e4d591453fd999ea34870c33d681160d6f91ac3e8e6`  
		Last Modified: Wed, 15 Apr 2026 21:40:38 GMT  
		Size: 2.2 MB (2178158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a29947e152eea3d30a8612f8ec8d06ba8dac35f21c5319fc14e247056d17a8a`  
		Last Modified: Wed, 15 Apr 2026 21:40:38 GMT  
		Size: 30.8 KB (30801 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.9` - linux; 386

```console
$ docker pull composer@sha256:5059aa7f8aeb8fd9ad00e166cfc4504d01b632d5c987150dfde3e7167b11e492
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82480079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05da3dd80cd6d3c296bb9f77ac1d48716d0282b354fc840118af6947f2db6dbd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Fri, 10 Apr 2026 00:13:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 10 Apr 2026 00:13:16 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 10 Apr 2026 00:13:16 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 10 Apr 2026 00:13:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 10 Apr 2026 00:13:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 10 Apr 2026 00:13:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 10 Apr 2026 00:13:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 10 Apr 2026 00:13:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 10 Apr 2026 00:13:16 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 10 Apr 2026 00:13:16 GMT
ENV PHP_VERSION=8.5.5
# Fri, 10 Apr 2026 00:13:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Fri, 10 Apr 2026 00:13:16 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Fri, 10 Apr 2026 00:13:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 10 Apr 2026 00:13:20 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 00:16:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 10 Apr 2026 00:16:53 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 00:16:54 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 10 Apr 2026 00:16:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 10 Apr 2026 00:16:54 GMT
CMD ["php" "-a"]
# Tue, 14 Apr 2026 18:19:28 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Apr 2026 18:19:28 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Apr 2026 18:19:47 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Apr 2026 18:19:47 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Apr 2026 18:19:47 GMT
ENV COMPOSER_VERSION=2.9.7
# Tue, 14 Apr 2026 18:19:47 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Apr 2026 18:19:48 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Apr 2026 18:19:48 GMT
WORKDIR /app
# Tue, 14 Apr 2026 18:19:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Apr 2026 18:19:48 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d2062b0536d4d6a1543e3a6bfd55452c7706979a7def0ad5ff0f3e183f183d`  
		Last Modified: Fri, 10 Apr 2026 00:17:02 GMT  
		Size: 5.9 MB (5909460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb9b53f46bb29bde8242534cc51035c71b65536a0a0acada6428f7a8ba0889c`  
		Last Modified: Fri, 10 Apr 2026 00:17:02 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab50b39601a88f935ec690047331c7481ff9b7ae2bb959cfc4cc98313c492986`  
		Last Modified: Fri, 10 Apr 2026 00:17:02 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92225e063d6f653398ed45adcff1579a3a3cf3ccbe764a4bb5b301283ee3b2ee`  
		Last Modified: Fri, 10 Apr 2026 00:17:02 GMT  
		Size: 14.4 MB (14379292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ccaecce131db93828716f892d3ad6e523dec70db239cc1bed3bb5394e8396c`  
		Last Modified: Fri, 10 Apr 2026 00:17:03 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e4efa73be7dce94cd5df6088620edcd50156eafe81c782274c129a7a3e191d`  
		Last Modified: Fri, 10 Apr 2026 00:17:04 GMT  
		Size: 23.4 MB (23438953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab8684032f9c15ecd79788e50ca55f90486d5bf79b5b3a24018772984e7a1cb5`  
		Last Modified: Fri, 10 Apr 2026 00:17:04 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba72ff6334ace2c9a0d737cdf3c0fa9f61f267a07af45bf21e2ff77820277e5`  
		Last Modified: Fri, 10 Apr 2026 00:17:04 GMT  
		Size: 23.6 KB (23625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb92bca6a7200abd5ed57acbc2406d1b631ce897e9fcb8321df6d6ad30cb6114`  
		Last Modified: Tue, 14 Apr 2026 18:19:58 GMT  
		Size: 33.4 MB (33354023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3acb4361787726cd8ad52c3d9467b84e1d1aa7dfe6414e7e3be8d2816cc76617`  
		Last Modified: Tue, 14 Apr 2026 18:19:57 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9241059ece99827922266cdf5f4d2003877d75ddf68699cd4c70ce7987a21836`  
		Last Modified: Tue, 14 Apr 2026 18:19:57 GMT  
		Size: 1.7 MB (1682879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69641c04f229a2ab6016f07abf23bea732612f28baf219fd9fcf0c899d7617e5`  
		Last Modified: Tue, 14 Apr 2026 18:19:42 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67f4289f14f4bb7e5b1629ac4c78856e0c3b60c94f52f95daa671e1a219d5df8`  
		Last Modified: Tue, 14 Apr 2026 18:19:59 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.9` - unknown; unknown

```console
$ docker pull composer@sha256:c254802094079f1308563379ad369533970752e4908cfa224d9e97811d3d39ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2211056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4ce198e58e85ea5dc923b1568aaa064676ae0112aaf5ac90c6cc3e58fdc12bf`

```dockerfile
```

-	Layers:
	-	`sha256:340334093e4da71051f77042453963dbc6f4fd36456e9b67f499e0b94970d025`  
		Last Modified: Tue, 14 Apr 2026 18:19:57 GMT  
		Size: 2.2 MB (2180425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47bf377a779ae13fd18570cc75e3fe8f0a691c683d330c3c388994b1f8641121`  
		Last Modified: Tue, 14 Apr 2026 18:19:57 GMT  
		Size: 30.6 KB (30631 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.9` - linux; ppc64le

```console
$ docker pull composer@sha256:6b0debe85067d180c3dca5be15549aa709e405e5c6da97f106b302afa0be7b3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 MB (96713081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d658b5ad399d03987449b91b37ae36fb531e2591aba9b560f1469876bcd1472`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Thu, 12 Mar 2026 23:53:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Mar 2026 23:53:02 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Mar 2026 23:53:02 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Mar 2026 23:53:02 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Mar 2026 23:53:02 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Mar 2026 23:53:02 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Mar 2026 23:53:02 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Mar 2026 23:53:02 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Mar 2026 23:53:02 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 12 Mar 2026 23:53:02 GMT
ENV PHP_VERSION=8.5.5
# Thu, 12 Mar 2026 23:53:02 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Thu, 12 Mar 2026 23:53:02 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Thu, 09 Apr 2026 22:33:42 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 09 Apr 2026 22:33:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:38:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 09 Apr 2026 22:38:29 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:38:30 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 09 Apr 2026 22:38:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 09 Apr 2026 22:38:30 GMT
CMD ["php" "-a"]
# Fri, 10 Apr 2026 00:21:05 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 10 Apr 2026 00:21:07 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Apr 2026 18:19:02 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Apr 2026 18:19:02 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Apr 2026 18:19:02 GMT
ENV COMPOSER_VERSION=2.9.7
# Tue, 14 Apr 2026 18:19:02 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Apr 2026 18:19:05 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Apr 2026 18:19:09 GMT
WORKDIR /app
# Tue, 14 Apr 2026 18:19:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Apr 2026 18:19:09 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7db1cc7b26f64d5de44e75f81962c30dead7dbc1dae3ebb93d0dc3d0cea721a`  
		Last Modified: Thu, 12 Mar 2026 23:58:51 GMT  
		Size: 3.8 MB (3768852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4a23ff5963c3f844b77db123769c733318f6ad54386c9f63e356424059470b`  
		Last Modified: Thu, 12 Mar 2026 23:58:51 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a071b7623ea30b2e8950858971a7e7838856db9c469a46b6305dcd619d0531fc`  
		Last Modified: Thu, 12 Mar 2026 23:58:51 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d012a34014d339e95156eab3252cc22fbae82a4670be3766b110c04e96ff1a17`  
		Last Modified: Thu, 09 Apr 2026 22:38:45 GMT  
		Size: 14.4 MB (14379301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8b7c5afa56dcdf0f01aaba59b305697db6b72603309ba573605f5fcd422fc0`  
		Last Modified: Thu, 09 Apr 2026 22:38:45 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1971acbe5d44b0f37d3698908a5766cea69f16ef4c4472ca8a30f5d48eec93ec`  
		Last Modified: Thu, 09 Apr 2026 22:38:46 GMT  
		Size: 23.1 MB (23118163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ee71922b29fe2228fde987804ee785c857383e7941a35e885bb5f06b7c3aba`  
		Last Modified: Thu, 09 Apr 2026 22:38:45 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fbefb03f1cf2736ed7b9f334b7e8f2f16dbedad1876c833ba4682b99ca9f99a`  
		Last Modified: Thu, 09 Apr 2026 22:38:46 GMT  
		Size: 23.4 KB (23442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db29015527299944deffccc76c5bfb597208be66aea62b09cf37a0cef1bb364e`  
		Last Modified: Fri, 10 Apr 2026 00:22:19 GMT  
		Size: 34.2 MB (34177434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972a41e22feca9d4bfcc298283918766cb03ebb7dd146ebbded895c8b431c973`  
		Last Modified: Fri, 10 Apr 2026 00:22:17 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efaac84e88b2da4e607702934bba5a10ee9d45974d858538b478a29b89842e33`  
		Last Modified: Tue, 14 Apr 2026 18:19:37 GMT  
		Size: 17.4 MB (17411381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e029883ecefeeaf8733085cd8e526dfbbca7e594b984c759f9d554d542181f0`  
		Last Modified: Tue, 14 Apr 2026 18:19:37 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebb4782c2d3dfa3ac371b8a44cd1f51c8cca8d476ce08683daefb52097b9bf7`  
		Last Modified: Tue, 14 Apr 2026 18:19:37 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.9` - unknown; unknown

```console
$ docker pull composer@sha256:b96e3b5bce750eb3282de808dd8aafbf3a051c5f80e3f716df031de690321657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2211215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5342929d05c922fd2d787aa2179debfaee17cdccf8781a7e329e1d3d484d07f1`

```dockerfile
```

-	Layers:
	-	`sha256:fc050012567990ae6904da1426da82a6cc21eeb168d8d2fa9b316fe513258f54`  
		Last Modified: Tue, 14 Apr 2026 18:19:37 GMT  
		Size: 2.2 MB (2180498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dc4ab7a528f883fc6476f1d2c72c9454b32b1cd4fefe0ac8fb1da3fec8e6c44`  
		Last Modified: Tue, 14 Apr 2026 18:19:37 GMT  
		Size: 30.7 KB (30717 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.9` - linux; riscv64

```console
$ docker pull composer@sha256:600f68dee998197590fbadd5f49b007afb10faf4f15287a315a79fa198635908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.1 MB (78108283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abd844ec36780aac229ca2fdb372bcc3b96fc3ad9a0c8de0b25c8458b53af256`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 09:13:06 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 28 Jan 2026 09:13:06 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 28 Jan 2026 09:13:06 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 28 Jan 2026 09:13:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 28 Jan 2026 09:13:07 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 28 Jan 2026 09:13:07 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_VERSION=8.5.5
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Fri, 10 Apr 2026 09:29:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 10 Apr 2026 09:29:21 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 10:28:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 10 Apr 2026 10:28:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 10:28:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 10 Apr 2026 10:28:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 10 Apr 2026 10:28:33 GMT
CMD ["php" "-a"]
# Sun, 12 Apr 2026 09:33:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Sun, 12 Apr 2026 09:33:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Apr 2026 18:22:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Apr 2026 18:22:48 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Apr 2026 18:22:48 GMT
ENV COMPOSER_VERSION=2.9.7
# Tue, 14 Apr 2026 18:22:48 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Apr 2026 18:22:48 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Apr 2026 18:22:48 GMT
WORKDIR /app
# Tue, 14 Apr 2026 18:22:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Apr 2026 18:22:48 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d64a68485fdb9ab2ec4159ac3e04e0bb79d9f1d037e580e928ca2b9604180f`  
		Last Modified: Wed, 28 Jan 2026 10:13:59 GMT  
		Size: 3.7 MB (3741000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b030c1b113432578231e8fe7c8a1bc913f2dc5dcba512e805fa9ab07768c9bd4`  
		Last Modified: Wed, 28 Jan 2026 10:13:58 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32a0e9bcb36b34307b4eada1f50c1cd4244d43d19ee57d962818dcb0ff0b110`  
		Last Modified: Wed, 28 Jan 2026 10:13:58 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20501e9e3d17b72af47b7d522d0c369998be222ed66ed9070ed2cbc45e500ca7`  
		Last Modified: Fri, 10 Apr 2026 10:29:42 GMT  
		Size: 14.4 MB (14379290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f7fa0bbe8ea35a7aeededb6a1c62d4e192d88a3cbaa6a9ac613390cef5f797e`  
		Last Modified: Fri, 10 Apr 2026 10:29:38 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c00b6c348638ca2fb138534e98df3a83c5788350e7f682c5dab61388d5988a1`  
		Last Modified: Fri, 10 Apr 2026 10:29:43 GMT  
		Size: 20.8 MB (20772153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf32615937490fdbee93796b59955ce07e051f019b76917819692421da228ef`  
		Last Modified: Fri, 10 Apr 2026 10:29:38 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491cab84c5a842c690a34c22c4cfe20f23d7b27019ca9d80e387fd23ef96828d`  
		Last Modified: Fri, 10 Apr 2026 10:29:39 GMT  
		Size: 23.3 KB (23349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e865e7a35bee8605e802d4714eef1a4cd079ed0b68a414c076e698d97cfbedd6`  
		Last Modified: Sun, 12 Apr 2026 09:38:57 GMT  
		Size: 31.3 MB (31300012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:670c7192db5936f38910b865b3f6746b70a4b2523b1e25db7d274900db0fca4f`  
		Last Modified: Sun, 12 Apr 2026 09:38:52 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849fae3a43556661d0d79306c12a48046432673ac49917b14937307d36a24458`  
		Last Modified: Tue, 14 Apr 2026 18:24:04 GMT  
		Size: 4.3 MB (4302324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01efda7965080036e2b76754ef2276308322ed2394f97d073063348bded60a09`  
		Last Modified: Tue, 14 Apr 2026 18:24:03 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5997a67e70609c3ecf2d0c94e158584b948e5f7e90a85dd896325c6db3a7ed`  
		Last Modified: Tue, 14 Apr 2026 18:22:53 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.9` - unknown; unknown

```console
$ docker pull composer@sha256:55155328eaf6b4a8b732344c31723c0e2e7026edb1151e056f7260b0c23793eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2210153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baabb88b9e58574b8449e58ff8e49bdd472dd2b4eac9aec0cd90224e32a110f8`

```dockerfile
```

-	Layers:
	-	`sha256:14f5989ff5313284e35f85efde25d95ba6cf9e9207afa6539c85ba5cfebf3e22`  
		Last Modified: Tue, 14 Apr 2026 18:24:03 GMT  
		Size: 2.2 MB (2179439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d12e5da0f5f9cce27555430a40d6dc9e18c54764d62f13fed79c09c33cdd6769`  
		Last Modified: Tue, 14 Apr 2026 18:24:03 GMT  
		Size: 30.7 KB (30714 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.9` - linux; s390x

```console
$ docker pull composer@sha256:1f94545e77b0a527f486fd42ce1a3ed8e347a32e951166e75e667c9a8b9c5055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93248850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc4e000a0f721a102b5621d79143082167c85fe36cbab314eff8808e5f343a36`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Mar 2026 23:37:17 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Mar 2026 23:37:17 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Mar 2026 23:37:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Mar 2026 23:37:17 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHP_VERSION=8.5.5
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Thu, 09 Apr 2026 22:21:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 09 Apr 2026 22:21:35 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:27:00 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 09 Apr 2026 22:27:00 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:27:01 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 09 Apr 2026 22:27:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 09 Apr 2026 22:27:01 GMT
CMD ["php" "-a"]
# Thu, 09 Apr 2026 23:18:42 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 09 Apr 2026 23:18:42 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Apr 2026 18:19:36 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Apr 2026 18:19:36 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Apr 2026 18:19:36 GMT
ENV COMPOSER_VERSION=2.9.7
# Tue, 14 Apr 2026 18:19:36 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Apr 2026 18:19:36 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Apr 2026 18:19:36 GMT
WORKDIR /app
# Tue, 14 Apr 2026 18:19:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Apr 2026 18:19:36 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4348d21358ef752a357c33976b85357317bfb623a79cb91ec462b4e5128b82d5`  
		Last Modified: Thu, 12 Mar 2026 23:43:03 GMT  
		Size: 3.8 MB (3795119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a169c2de4deea9b877eb224ec8f2d4f4502dd0bb4e22037516ea41c23c8c1e6`  
		Last Modified: Thu, 12 Mar 2026 23:43:02 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f88a80dfabed7faa02e1bbe28dd4e26c817c26d54bb3411b27cc398ea997ef8`  
		Last Modified: Thu, 12 Mar 2026 23:43:02 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5e7662fcf96af1dfae3edab12e535e5dbb2bd9336314490ac9484222315cc0`  
		Last Modified: Thu, 09 Apr 2026 22:27:14 GMT  
		Size: 14.4 MB (14379286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b2bd611f10e897bc78163d788b300458c71f27af849508076d219371619381`  
		Last Modified: Thu, 09 Apr 2026 22:27:14 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c1175a23bc886b3bc9f9e6845c90d99d1125fc788f6d88d5ad9501ed086f83`  
		Last Modified: Thu, 09 Apr 2026 22:27:15 GMT  
		Size: 21.9 MB (21889964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48a98f93d43e57e9161beb90862e90db489cf9d4b4d09bfbd7d3bc1566f7981`  
		Last Modified: Thu, 09 Apr 2026 22:27:14 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91cdaaeb755a7dbc3a463542f5d9410ef527eb1babc2850059c13f703b6bf5f`  
		Last Modified: Thu, 09 Apr 2026 22:27:15 GMT  
		Size: 23.4 KB (23427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b0c643f457b3285c9b024aac2f31693051af6eb786510b03d7580e65134de8`  
		Last Modified: Thu, 09 Apr 2026 23:19:25 GMT  
		Size: 32.1 MB (32113304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a5512141ecbaa16f283bdbec60a949479d2d7ef6afafc01d5cc3b3351085cd1`  
		Last Modified: Thu, 09 Apr 2026 23:19:20 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd4c500e9eb181938a1ef4ef73f183e9b27420814a10ea55b06e736b40bf16a`  
		Last Modified: Tue, 14 Apr 2026 18:19:51 GMT  
		Size: 17.3 MB (17317554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc53ab4bbf74e12a9c7818288fc97c9f60326574f248c11959ba84015cc1ee0`  
		Last Modified: Tue, 14 Apr 2026 18:19:51 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c73a8be0d813065a838fdca97a14527a4ee7e1530e35f656f93a424f4d7c27`  
		Last Modified: Tue, 14 Apr 2026 18:19:42 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.9` - unknown; unknown

```console
$ docker pull composer@sha256:0bc79feb6a333a11cc49a0e80b8edad445b1bc590d108776ee1d1f9cba4c69b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2209891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e15343c996740440561a353bfba972b4a6752dff34802d7eb98b3923520488bd`

```dockerfile
```

-	Layers:
	-	`sha256:10647c8aceb5f18307cac8578a92f75dc319b2558c6f7cfcacc86be9c1ffd2ee`  
		Last Modified: Tue, 14 Apr 2026 18:19:50 GMT  
		Size: 2.2 MB (2179221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ceacdd28fffe318712ca3aebf2993293f60ba3f21a55c590b010d01ac5e20b8`  
		Last Modified: Tue, 14 Apr 2026 18:19:50 GMT  
		Size: 30.7 KB (30670 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.9.7`

```console
$ docker pull composer@sha256:709a30cb521103db18992786f7fd747010ad8e24cf581817ddf3e53288d3d281
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

### `composer:2.9.7` - linux; amd64

```console
$ docker pull composer@sha256:a3df561dbdddfdb9832ec50f41c0e2f1d27445a67bd71415f05467fedbb2c3c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.2 MB (78237453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39f4699ce5525450650cad74ebb243efd73730fda6d6011a5d805089f9bc61ce`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:17:52 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:17:52 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:17:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:17:52 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:17:52 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:17:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:17:52 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:17:52 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 15 Apr 2026 20:17:52 GMT
ENV PHP_VERSION=8.5.5
# Wed, 15 Apr 2026 20:17:52 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Wed, 15 Apr 2026 20:17:52 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Wed, 15 Apr 2026 20:17:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 20:17:56 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:21:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 20:21:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:21:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 20:21:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 20:21:24 GMT
CMD ["php" "-a"]
# Wed, 15 Apr 2026 21:27:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Wed, 15 Apr 2026 21:27:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Wed, 15 Apr 2026 21:27:31 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 15 Apr 2026 21:27:31 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 15 Apr 2026 21:27:31 GMT
ENV COMPOSER_VERSION=2.9.7
# Wed, 15 Apr 2026 21:27:31 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Wed, 15 Apr 2026 21:27:31 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 21:27:31 GMT
WORKDIR /app
# Wed, 15 Apr 2026 21:27:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:27:31 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7575019b1e32c16a639f3988d9a63ff1c22c036099e3cb267ea5a97ba0fcb31b`  
		Last Modified: Wed, 15 Apr 2026 20:21:32 GMT  
		Size: 3.6 MB (3587447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba54b7e6d1307c692fb0f98a7bb785c3ae59fda44cbd8dc735eb6d32da25bb2`  
		Last Modified: Wed, 15 Apr 2026 20:21:32 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7367014229e0f5079d78d9d65f87aeb106ffa42ef3cacfdde5ccae68a710662d`  
		Last Modified: Wed, 15 Apr 2026 20:21:32 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c74770868277c77b3c7d8e5aa987ffc0183e76f8a003e5ee3e5662475be115`  
		Last Modified: Wed, 15 Apr 2026 20:21:33 GMT  
		Size: 14.4 MB (14379186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f1108694a36c05d3950260f3491806016ec3ab9ba1da15154bda777858d1eb`  
		Last Modified: Wed, 15 Apr 2026 20:21:33 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e321e76cc80892e05feb16337063a65959f21cd03508ea9f6dd1316bd2bfee6`  
		Last Modified: Wed, 15 Apr 2026 20:21:34 GMT  
		Size: 22.5 MB (22528821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2af3ca59c901474266aab6d50192f869e507a229be1b7493e312a32fac0dff9`  
		Last Modified: Wed, 15 Apr 2026 20:21:33 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b12841ff7824946e17f91cf31b444d9a97e15dc30fa55d79e32ae0c00cf27f1`  
		Last Modified: Wed, 15 Apr 2026 20:21:34 GMT  
		Size: 23.4 KB (23395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e55827933a329097ef03bab9834f516b064faf5b72b18d080e967055a42003`  
		Last Modified: Wed, 15 Apr 2026 21:27:42 GMT  
		Size: 32.8 MB (32828568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2933ad071631f9ce3470578aecae812618fd37d7004987532866b0359f6b6de0`  
		Last Modified: Wed, 15 Apr 2026 21:27:41 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d821667065611cf0d7b4bf7f6d8857b118bfd703fe486289b37884a8edbd61`  
		Last Modified: Wed, 15 Apr 2026 21:27:41 GMT  
		Size: 1.0 MB (1020986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae94261b1892c1af044280991b4f2a5dd150a791ec2eeef5af1ea6d3094479e5`  
		Last Modified: Wed, 15 Apr 2026 21:27:41 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb435422e01857a05128024eb0629a6c60655c0d3b45442ea0bc469f1bbd191`  
		Last Modified: Wed, 15 Apr 2026 21:27:42 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.9.7` - unknown; unknown

```console
$ docker pull composer@sha256:e85e044ddbc3f14041ddacfb9398391fc8292baa3673ee4c95d5b809632bc41f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2209324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4c877852d538421f4a82316e63e564b40bc167997b6947ce7c9b36533714614`

```dockerfile
```

-	Layers:
	-	`sha256:b9fed10922f5326c3cb699a3c5c5bfb4d7c68743354358d37b16875c5fdd6803`  
		Last Modified: Wed, 15 Apr 2026 21:27:41 GMT  
		Size: 2.2 MB (2178657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:615752e487f6d65b8ad402d079106fe3c4610a7aee9abb3e9350d78067b4501f`  
		Last Modified: Wed, 15 Apr 2026 21:27:41 GMT  
		Size: 30.7 KB (30667 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.9.7` - linux; arm variant v6

```console
$ docker pull composer@sha256:5f618ede41609642ab0415bf163302848fbba617512b9f3bcb4c81d65aea6016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74743627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e102830ff670832c4941a947728bd57ef6a228b56943b1d8d452c9c6f1e395d8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:19:04 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:19:04 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:19:04 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:19:04 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:19:05 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:19:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:19:05 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:19:05 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:19:05 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 15 Apr 2026 20:19:05 GMT
ENV PHP_VERSION=8.5.5
# Wed, 15 Apr 2026 20:19:05 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Wed, 15 Apr 2026 20:19:05 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Wed, 15 Apr 2026 20:19:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 20:19:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:22:18 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 20:22:18 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:22:19 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 20:22:19 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 20:22:19 GMT
CMD ["php" "-a"]
# Wed, 15 Apr 2026 21:22:04 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Wed, 15 Apr 2026 21:22:04 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Wed, 15 Apr 2026 21:22:27 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 15 Apr 2026 21:22:27 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 15 Apr 2026 21:22:27 GMT
ENV COMPOSER_VERSION=2.9.7
# Wed, 15 Apr 2026 21:22:27 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Wed, 15 Apr 2026 21:22:27 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 21:22:27 GMT
WORKDIR /app
# Wed, 15 Apr 2026 21:22:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:22:27 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1d167fc497e35df23f81ef7d507ee40c904d148d7c5e239db360263ce1228f`  
		Last Modified: Wed, 15 Apr 2026 20:22:24 GMT  
		Size: 3.5 MB (3543048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7893272fc58b639fcb274b9cdac380a99a02b7fec1370991d7043a8d745ee731`  
		Last Modified: Wed, 15 Apr 2026 20:22:24 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b5e2d5fa2204fe8d000332835281efd2beeb4e2b1233fda8377dc9fb8d273da`  
		Last Modified: Wed, 15 Apr 2026 20:22:24 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a237864e95f05b7c9e05c3272f303c8616f39f4b50a113166e6e93f5d6eb2867`  
		Last Modified: Wed, 15 Apr 2026 20:22:25 GMT  
		Size: 14.4 MB (14379195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d6cac0622b9c4733975c694271b5cfe4e9e251f5a29439c27931c4334db09d`  
		Last Modified: Wed, 15 Apr 2026 20:22:25 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a5b1613ded78de2dd5fc3a3cbb57bc91cb6f35c9bf29e262676641888899d35`  
		Last Modified: Wed, 15 Apr 2026 20:22:26 GMT  
		Size: 19.5 MB (19534950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7326187f367c7e04eed9c7cfd2fd94e264bdf5da29600b25762d89f896ee8df`  
		Last Modified: Wed, 15 Apr 2026 20:22:26 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf7aab9524160d3a6dc903858b7d9fc9d77b6f4a09bb6c0cdb0b86eca60acbc`  
		Last Modified: Wed, 15 Apr 2026 20:22:26 GMT  
		Size: 23.2 KB (23204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7338db7ab2e6da871e9ca18bf6e41db656dc01552305f5ea294acd98e45f2ff2`  
		Last Modified: Wed, 15 Apr 2026 21:22:35 GMT  
		Size: 32.7 MB (32665496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acff7d213b0f5a23ec528c0624a11975e61306f0ef4705e003a9109c922c9aaf`  
		Last Modified: Wed, 15 Apr 2026 21:22:34 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ab1a1cc99508981bda26983105462a9a3ee15eae1e24e6da36767b441c2244`  
		Last Modified: Wed, 15 Apr 2026 21:22:34 GMT  
		Size: 1.0 MB (1021023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cff2f6c2aff71864717c706d9c7e23510750ed143e2938cb19d5fdafff8be79`  
		Last Modified: Wed, 15 Apr 2026 21:22:34 GMT  
		Size: 416.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2da733922c6146907c3b3634c5c450c96e0638edddca77a676b7cd813427f9`  
		Last Modified: Wed, 15 Apr 2026 21:22:35 GMT  
		Size: 91.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.9.7` - unknown; unknown

```console
$ docker pull composer@sha256:1eb3fc19c61b35b8a872d9323204996b304beb4dc10e4d11dfd6b5c14cc219a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:784a99b9ab8555f39e0aa608545bfc075b883ab06336eacb31db1b89b4961c24`

```dockerfile
```

-	Layers:
	-	`sha256:1e8a701178ca230dc13cbb78d4e4d281f47957950cbb2e2298d741398449207b`  
		Last Modified: Wed, 15 Apr 2026 21:22:33 GMT  
		Size: 30.6 KB (30557 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.9.7` - linux; arm variant v7

```console
$ docker pull composer@sha256:582284655bf553416dbce90c395b4dc89da3a7edc9da012ec6e01407c1430ed9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.6 MB (71571453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f9ac974387fafeac611e90eeb97b0514811d16f37141c1796d8eebb9f19295e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:18:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:18:22 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:18:22 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:18:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:18:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:18:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:18:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:18:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:18:22 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 15 Apr 2026 20:18:22 GMT
ENV PHP_VERSION=8.5.5
# Wed, 15 Apr 2026 20:18:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Wed, 15 Apr 2026 20:18:22 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Wed, 15 Apr 2026 20:18:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 20:18:26 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:21:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 20:21:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:21:34 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 20:21:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 20:21:34 GMT
CMD ["php" "-a"]
# Wed, 15 Apr 2026 21:32:22 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Wed, 15 Apr 2026 21:32:22 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Wed, 15 Apr 2026 21:32:44 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 15 Apr 2026 21:32:44 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 15 Apr 2026 21:32:44 GMT
ENV COMPOSER_VERSION=2.9.7
# Wed, 15 Apr 2026 21:32:44 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Wed, 15 Apr 2026 21:32:44 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 21:32:45 GMT
WORKDIR /app
# Wed, 15 Apr 2026 21:32:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:32:45 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40243011337e75e1e1aba1a01eff0f25c670f2784f31a19fe3ceeb28d9cbb386`  
		Last Modified: Wed, 15 Apr 2026 20:21:41 GMT  
		Size: 3.3 MB (3343352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289d25cb3dc6bf4d1acfe704c1d05a812b84cbfe26b06c6e9a423f281efcfd64`  
		Last Modified: Wed, 15 Apr 2026 20:21:41 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457ef191b478c4407082d1c51e695feac2f4425353d54d5d6737f8e3aede1686`  
		Last Modified: Wed, 15 Apr 2026 20:21:41 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef8f20263bc5a42b03699b180b432cb94cb313e98aed5a4238024d8cd3f252ad`  
		Last Modified: Wed, 15 Apr 2026 20:21:41 GMT  
		Size: 14.4 MB (14379203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654a3e48df9d037dc7d582e4d7e753ead3d5f55b619c07d29f0f2701eabf4657`  
		Last Modified: Wed, 15 Apr 2026 20:21:43 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00b79e1670ab000b58c3fa612bf97d881357d5a02a37a01aab4448a263a56aa`  
		Last Modified: Wed, 15 Apr 2026 20:21:43 GMT  
		Size: 18.4 MB (18430268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:670c3d79616cd5914f7e4d0d94505d6570f152e3fab437081ba1b2499bf253df`  
		Last Modified: Wed, 15 Apr 2026 20:21:43 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773025cf5591ee7e2a345d9e429358f0269bd41230fb2da781a05eb990ef0386`  
		Last Modified: Wed, 15 Apr 2026 20:21:43 GMT  
		Size: 23.2 KB (23204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acebb0a04354316add548495911389085f450934caee74f83d543b9e72b2d05e`  
		Last Modified: Wed, 15 Apr 2026 21:32:54 GMT  
		Size: 31.1 MB (31096001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a09a4d2f176f1708944c561d076f811601d10ce9c12f67f368beb5f33e872e0`  
		Last Modified: Wed, 15 Apr 2026 21:32:53 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4554ab557c57e190e9a9c96595d8f20842cdf6c58419124406570b03fb325ec8`  
		Last Modified: Wed, 15 Apr 2026 21:32:54 GMT  
		Size: 1.0 MB (1011452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba1c93167f863ddcc1d5c2653b03c6a8642c2fd9559327b73ed8624251ec144`  
		Last Modified: Wed, 15 Apr 2026 21:32:54 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c681ef1dc9504c4c3f4ad0cf3ffc7c285a57f04dbacae219663ef575ca6acf`  
		Last Modified: Wed, 15 Apr 2026 21:32:55 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.9.7` - unknown; unknown

```console
$ docker pull composer@sha256:32d0c9b1e4d5d571639eb8de3fd2347a367f829d380db08ff8dbf370f5b11cc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2209101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23ebcb2c2afc717904235ca8d45b56e040e43ae27f90d904adef6de85485e0c1`

```dockerfile
```

-	Layers:
	-	`sha256:1ea500bcc75e9906fcbd4ac18fb9f32b00e2f232209a8695dbdd04027eae30b1`  
		Last Modified: Wed, 15 Apr 2026 21:32:54 GMT  
		Size: 2.2 MB (2178328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d85d9fe7060afbbf94f473725bfe33d128da115ed642a56a0a3c11dc35b8ad8a`  
		Last Modified: Wed, 15 Apr 2026 21:32:53 GMT  
		Size: 30.8 KB (30773 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.9.7` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:02cc0a1729b9f75734a6f1789ad59fa90c54bdb84566b2c7b564f7eaafd5c368
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77892271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b9aa3f48599c920e9268b74581f5d0d24a2eca014342e24e60e1d70f8bfb5ae`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:21 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:16:21 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:16:21 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:16:21 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:16:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:16:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:16:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:16:21 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:16:21 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 15 Apr 2026 20:16:21 GMT
ENV PHP_VERSION=8.5.5
# Wed, 15 Apr 2026 20:16:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Wed, 15 Apr 2026 20:16:21 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Wed, 15 Apr 2026 20:16:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 20:16:25 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:19:57 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 20:19:57 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:19:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 20:19:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 20:19:58 GMT
CMD ["php" "-a"]
# Wed, 15 Apr 2026 21:40:09 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Wed, 15 Apr 2026 21:40:09 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Wed, 15 Apr 2026 21:40:29 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 15 Apr 2026 21:40:29 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 15 Apr 2026 21:40:29 GMT
ENV COMPOSER_VERSION=2.9.7
# Wed, 15 Apr 2026 21:40:29 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Wed, 15 Apr 2026 21:40:29 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 21:40:29 GMT
WORKDIR /app
# Wed, 15 Apr 2026 21:40:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:40:29 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e4c5bcbf8c3068a7d4c178cdd5132463fa53adf8c55efe0d5a02126d958e69`  
		Last Modified: Wed, 15 Apr 2026 20:20:06 GMT  
		Size: 3.6 MB (3596134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c0edc310dc19501413b5668245bc984741c4ac5a3219932a74e83fb33b6f94`  
		Last Modified: Wed, 15 Apr 2026 20:20:02 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d665080207d06b6b7246d46376f6ec0b3a5d072b47f01ab3fe89eb95ea0b9310`  
		Last Modified: Wed, 15 Apr 2026 20:20:02 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e92dbfc45c4b506749680c4bded773db9170a5c594ae07c33aa938ac9b46a1c`  
		Last Modified: Wed, 15 Apr 2026 20:20:07 GMT  
		Size: 14.4 MB (14379192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da631dfa865e2d394e47bb93c95f041d309af42b22cd597826fab10299773bc`  
		Last Modified: Wed, 15 Apr 2026 20:20:03 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0885f624969f9911f18390a16714e49ddcba2831ee9c8002d794ee56d8ca9ca8`  
		Last Modified: Wed, 15 Apr 2026 20:20:07 GMT  
		Size: 21.7 MB (21697840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e202517af7cb78a86ff7f8b255ca452261912c8830cf0b7e352386b5c5472454`  
		Last Modified: Wed, 15 Apr 2026 20:20:05 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4062a55681ba2c31424930678c18614b1e9e0eb63f551ee5faaa3857658f4f0`  
		Last Modified: Wed, 15 Apr 2026 20:20:07 GMT  
		Size: 23.2 KB (23209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247694cf5276fc930925fbd3c766f23524e3c168100355ab0759b2996481c9fe`  
		Last Modified: Wed, 15 Apr 2026 21:40:39 GMT  
		Size: 33.0 MB (32971344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd2df09b94d664b93dffeea3fcc3ec248ab74647c5a4214efe19bfb47fcb05a8`  
		Last Modified: Wed, 15 Apr 2026 21:40:38 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ddb215ec4272be553f5bc3174320405b2f1a91262a8dcef2e0a86a9e49ee716`  
		Last Modified: Wed, 15 Apr 2026 21:40:38 GMT  
		Size: 1.0 MB (1019831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf4152796a067e6883c8510bc549ef6efa7a2938ae8a777ac16b9ce0064b7cb`  
		Last Modified: Wed, 15 Apr 2026 21:40:38 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2e497f91b5d80958253e7e10d4c15d00acc6326888e106b429a9c5308f89fe`  
		Last Modified: Wed, 15 Apr 2026 21:40:39 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.9.7` - unknown; unknown

```console
$ docker pull composer@sha256:fe7799a0766fcb90d3eee27476e71e060d8359ba6a1af526e40143a0b717c9fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2208959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c81eae5c2a8041b04dcb4644dca7f3e06622961ff2e597b7542f07cfbf49fb89`

```dockerfile
```

-	Layers:
	-	`sha256:b2e0891d2073a415183d3e4d591453fd999ea34870c33d681160d6f91ac3e8e6`  
		Last Modified: Wed, 15 Apr 2026 21:40:38 GMT  
		Size: 2.2 MB (2178158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a29947e152eea3d30a8612f8ec8d06ba8dac35f21c5319fc14e247056d17a8a`  
		Last Modified: Wed, 15 Apr 2026 21:40:38 GMT  
		Size: 30.8 KB (30801 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.9.7` - linux; 386

```console
$ docker pull composer@sha256:5059aa7f8aeb8fd9ad00e166cfc4504d01b632d5c987150dfde3e7167b11e492
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82480079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05da3dd80cd6d3c296bb9f77ac1d48716d0282b354fc840118af6947f2db6dbd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Fri, 10 Apr 2026 00:13:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 10 Apr 2026 00:13:16 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 10 Apr 2026 00:13:16 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 10 Apr 2026 00:13:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 10 Apr 2026 00:13:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 10 Apr 2026 00:13:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 10 Apr 2026 00:13:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 10 Apr 2026 00:13:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 10 Apr 2026 00:13:16 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 10 Apr 2026 00:13:16 GMT
ENV PHP_VERSION=8.5.5
# Fri, 10 Apr 2026 00:13:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Fri, 10 Apr 2026 00:13:16 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Fri, 10 Apr 2026 00:13:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 10 Apr 2026 00:13:20 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 00:16:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 10 Apr 2026 00:16:53 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 00:16:54 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 10 Apr 2026 00:16:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 10 Apr 2026 00:16:54 GMT
CMD ["php" "-a"]
# Tue, 14 Apr 2026 18:19:28 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Apr 2026 18:19:28 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Apr 2026 18:19:47 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Apr 2026 18:19:47 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Apr 2026 18:19:47 GMT
ENV COMPOSER_VERSION=2.9.7
# Tue, 14 Apr 2026 18:19:47 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Apr 2026 18:19:48 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Apr 2026 18:19:48 GMT
WORKDIR /app
# Tue, 14 Apr 2026 18:19:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Apr 2026 18:19:48 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d2062b0536d4d6a1543e3a6bfd55452c7706979a7def0ad5ff0f3e183f183d`  
		Last Modified: Fri, 10 Apr 2026 00:17:02 GMT  
		Size: 5.9 MB (5909460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb9b53f46bb29bde8242534cc51035c71b65536a0a0acada6428f7a8ba0889c`  
		Last Modified: Fri, 10 Apr 2026 00:17:02 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab50b39601a88f935ec690047331c7481ff9b7ae2bb959cfc4cc98313c492986`  
		Last Modified: Fri, 10 Apr 2026 00:17:02 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92225e063d6f653398ed45adcff1579a3a3cf3ccbe764a4bb5b301283ee3b2ee`  
		Last Modified: Fri, 10 Apr 2026 00:17:02 GMT  
		Size: 14.4 MB (14379292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ccaecce131db93828716f892d3ad6e523dec70db239cc1bed3bb5394e8396c`  
		Last Modified: Fri, 10 Apr 2026 00:17:03 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e4efa73be7dce94cd5df6088620edcd50156eafe81c782274c129a7a3e191d`  
		Last Modified: Fri, 10 Apr 2026 00:17:04 GMT  
		Size: 23.4 MB (23438953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab8684032f9c15ecd79788e50ca55f90486d5bf79b5b3a24018772984e7a1cb5`  
		Last Modified: Fri, 10 Apr 2026 00:17:04 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba72ff6334ace2c9a0d737cdf3c0fa9f61f267a07af45bf21e2ff77820277e5`  
		Last Modified: Fri, 10 Apr 2026 00:17:04 GMT  
		Size: 23.6 KB (23625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb92bca6a7200abd5ed57acbc2406d1b631ce897e9fcb8321df6d6ad30cb6114`  
		Last Modified: Tue, 14 Apr 2026 18:19:58 GMT  
		Size: 33.4 MB (33354023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3acb4361787726cd8ad52c3d9467b84e1d1aa7dfe6414e7e3be8d2816cc76617`  
		Last Modified: Tue, 14 Apr 2026 18:19:57 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9241059ece99827922266cdf5f4d2003877d75ddf68699cd4c70ce7987a21836`  
		Last Modified: Tue, 14 Apr 2026 18:19:57 GMT  
		Size: 1.7 MB (1682879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69641c04f229a2ab6016f07abf23bea732612f28baf219fd9fcf0c899d7617e5`  
		Last Modified: Tue, 14 Apr 2026 18:19:42 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67f4289f14f4bb7e5b1629ac4c78856e0c3b60c94f52f95daa671e1a219d5df8`  
		Last Modified: Tue, 14 Apr 2026 18:19:59 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.9.7` - unknown; unknown

```console
$ docker pull composer@sha256:c254802094079f1308563379ad369533970752e4908cfa224d9e97811d3d39ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2211056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4ce198e58e85ea5dc923b1568aaa064676ae0112aaf5ac90c6cc3e58fdc12bf`

```dockerfile
```

-	Layers:
	-	`sha256:340334093e4da71051f77042453963dbc6f4fd36456e9b67f499e0b94970d025`  
		Last Modified: Tue, 14 Apr 2026 18:19:57 GMT  
		Size: 2.2 MB (2180425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47bf377a779ae13fd18570cc75e3fe8f0a691c683d330c3c388994b1f8641121`  
		Last Modified: Tue, 14 Apr 2026 18:19:57 GMT  
		Size: 30.6 KB (30631 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.9.7` - linux; ppc64le

```console
$ docker pull composer@sha256:6b0debe85067d180c3dca5be15549aa709e405e5c6da97f106b302afa0be7b3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 MB (96713081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d658b5ad399d03987449b91b37ae36fb531e2591aba9b560f1469876bcd1472`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Thu, 12 Mar 2026 23:53:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Mar 2026 23:53:02 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Mar 2026 23:53:02 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Mar 2026 23:53:02 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Mar 2026 23:53:02 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Mar 2026 23:53:02 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Mar 2026 23:53:02 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Mar 2026 23:53:02 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Mar 2026 23:53:02 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 12 Mar 2026 23:53:02 GMT
ENV PHP_VERSION=8.5.5
# Thu, 12 Mar 2026 23:53:02 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Thu, 12 Mar 2026 23:53:02 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Thu, 09 Apr 2026 22:33:42 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 09 Apr 2026 22:33:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:38:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 09 Apr 2026 22:38:29 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:38:30 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 09 Apr 2026 22:38:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 09 Apr 2026 22:38:30 GMT
CMD ["php" "-a"]
# Fri, 10 Apr 2026 00:21:05 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 10 Apr 2026 00:21:07 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Apr 2026 18:19:02 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Apr 2026 18:19:02 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Apr 2026 18:19:02 GMT
ENV COMPOSER_VERSION=2.9.7
# Tue, 14 Apr 2026 18:19:02 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Apr 2026 18:19:05 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Apr 2026 18:19:09 GMT
WORKDIR /app
# Tue, 14 Apr 2026 18:19:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Apr 2026 18:19:09 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7db1cc7b26f64d5de44e75f81962c30dead7dbc1dae3ebb93d0dc3d0cea721a`  
		Last Modified: Thu, 12 Mar 2026 23:58:51 GMT  
		Size: 3.8 MB (3768852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4a23ff5963c3f844b77db123769c733318f6ad54386c9f63e356424059470b`  
		Last Modified: Thu, 12 Mar 2026 23:58:51 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a071b7623ea30b2e8950858971a7e7838856db9c469a46b6305dcd619d0531fc`  
		Last Modified: Thu, 12 Mar 2026 23:58:51 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d012a34014d339e95156eab3252cc22fbae82a4670be3766b110c04e96ff1a17`  
		Last Modified: Thu, 09 Apr 2026 22:38:45 GMT  
		Size: 14.4 MB (14379301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8b7c5afa56dcdf0f01aaba59b305697db6b72603309ba573605f5fcd422fc0`  
		Last Modified: Thu, 09 Apr 2026 22:38:45 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1971acbe5d44b0f37d3698908a5766cea69f16ef4c4472ca8a30f5d48eec93ec`  
		Last Modified: Thu, 09 Apr 2026 22:38:46 GMT  
		Size: 23.1 MB (23118163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ee71922b29fe2228fde987804ee785c857383e7941a35e885bb5f06b7c3aba`  
		Last Modified: Thu, 09 Apr 2026 22:38:45 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fbefb03f1cf2736ed7b9f334b7e8f2f16dbedad1876c833ba4682b99ca9f99a`  
		Last Modified: Thu, 09 Apr 2026 22:38:46 GMT  
		Size: 23.4 KB (23442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db29015527299944deffccc76c5bfb597208be66aea62b09cf37a0cef1bb364e`  
		Last Modified: Fri, 10 Apr 2026 00:22:19 GMT  
		Size: 34.2 MB (34177434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972a41e22feca9d4bfcc298283918766cb03ebb7dd146ebbded895c8b431c973`  
		Last Modified: Fri, 10 Apr 2026 00:22:17 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efaac84e88b2da4e607702934bba5a10ee9d45974d858538b478a29b89842e33`  
		Last Modified: Tue, 14 Apr 2026 18:19:37 GMT  
		Size: 17.4 MB (17411381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e029883ecefeeaf8733085cd8e526dfbbca7e594b984c759f9d554d542181f0`  
		Last Modified: Tue, 14 Apr 2026 18:19:37 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebb4782c2d3dfa3ac371b8a44cd1f51c8cca8d476ce08683daefb52097b9bf7`  
		Last Modified: Tue, 14 Apr 2026 18:19:37 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.9.7` - unknown; unknown

```console
$ docker pull composer@sha256:b96e3b5bce750eb3282de808dd8aafbf3a051c5f80e3f716df031de690321657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2211215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5342929d05c922fd2d787aa2179debfaee17cdccf8781a7e329e1d3d484d07f1`

```dockerfile
```

-	Layers:
	-	`sha256:fc050012567990ae6904da1426da82a6cc21eeb168d8d2fa9b316fe513258f54`  
		Last Modified: Tue, 14 Apr 2026 18:19:37 GMT  
		Size: 2.2 MB (2180498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dc4ab7a528f883fc6476f1d2c72c9454b32b1cd4fefe0ac8fb1da3fec8e6c44`  
		Last Modified: Tue, 14 Apr 2026 18:19:37 GMT  
		Size: 30.7 KB (30717 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.9.7` - linux; riscv64

```console
$ docker pull composer@sha256:600f68dee998197590fbadd5f49b007afb10faf4f15287a315a79fa198635908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.1 MB (78108283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abd844ec36780aac229ca2fdb372bcc3b96fc3ad9a0c8de0b25c8458b53af256`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 09:13:06 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 28 Jan 2026 09:13:06 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 28 Jan 2026 09:13:06 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 28 Jan 2026 09:13:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 28 Jan 2026 09:13:07 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 28 Jan 2026 09:13:07 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_VERSION=8.5.5
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Fri, 10 Apr 2026 09:29:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 10 Apr 2026 09:29:21 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 10:28:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 10 Apr 2026 10:28:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 10:28:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 10 Apr 2026 10:28:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 10 Apr 2026 10:28:33 GMT
CMD ["php" "-a"]
# Sun, 12 Apr 2026 09:33:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Sun, 12 Apr 2026 09:33:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Apr 2026 18:22:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Apr 2026 18:22:48 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Apr 2026 18:22:48 GMT
ENV COMPOSER_VERSION=2.9.7
# Tue, 14 Apr 2026 18:22:48 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Apr 2026 18:22:48 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Apr 2026 18:22:48 GMT
WORKDIR /app
# Tue, 14 Apr 2026 18:22:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Apr 2026 18:22:48 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d64a68485fdb9ab2ec4159ac3e04e0bb79d9f1d037e580e928ca2b9604180f`  
		Last Modified: Wed, 28 Jan 2026 10:13:59 GMT  
		Size: 3.7 MB (3741000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b030c1b113432578231e8fe7c8a1bc913f2dc5dcba512e805fa9ab07768c9bd4`  
		Last Modified: Wed, 28 Jan 2026 10:13:58 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32a0e9bcb36b34307b4eada1f50c1cd4244d43d19ee57d962818dcb0ff0b110`  
		Last Modified: Wed, 28 Jan 2026 10:13:58 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20501e9e3d17b72af47b7d522d0c369998be222ed66ed9070ed2cbc45e500ca7`  
		Last Modified: Fri, 10 Apr 2026 10:29:42 GMT  
		Size: 14.4 MB (14379290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f7fa0bbe8ea35a7aeededb6a1c62d4e192d88a3cbaa6a9ac613390cef5f797e`  
		Last Modified: Fri, 10 Apr 2026 10:29:38 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c00b6c348638ca2fb138534e98df3a83c5788350e7f682c5dab61388d5988a1`  
		Last Modified: Fri, 10 Apr 2026 10:29:43 GMT  
		Size: 20.8 MB (20772153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf32615937490fdbee93796b59955ce07e051f019b76917819692421da228ef`  
		Last Modified: Fri, 10 Apr 2026 10:29:38 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491cab84c5a842c690a34c22c4cfe20f23d7b27019ca9d80e387fd23ef96828d`  
		Last Modified: Fri, 10 Apr 2026 10:29:39 GMT  
		Size: 23.3 KB (23349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e865e7a35bee8605e802d4714eef1a4cd079ed0b68a414c076e698d97cfbedd6`  
		Last Modified: Sun, 12 Apr 2026 09:38:57 GMT  
		Size: 31.3 MB (31300012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:670c7192db5936f38910b865b3f6746b70a4b2523b1e25db7d274900db0fca4f`  
		Last Modified: Sun, 12 Apr 2026 09:38:52 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849fae3a43556661d0d79306c12a48046432673ac49917b14937307d36a24458`  
		Last Modified: Tue, 14 Apr 2026 18:24:04 GMT  
		Size: 4.3 MB (4302324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01efda7965080036e2b76754ef2276308322ed2394f97d073063348bded60a09`  
		Last Modified: Tue, 14 Apr 2026 18:24:03 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5997a67e70609c3ecf2d0c94e158584b948e5f7e90a85dd896325c6db3a7ed`  
		Last Modified: Tue, 14 Apr 2026 18:22:53 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.9.7` - unknown; unknown

```console
$ docker pull composer@sha256:55155328eaf6b4a8b732344c31723c0e2e7026edb1151e056f7260b0c23793eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2210153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baabb88b9e58574b8449e58ff8e49bdd472dd2b4eac9aec0cd90224e32a110f8`

```dockerfile
```

-	Layers:
	-	`sha256:14f5989ff5313284e35f85efde25d95ba6cf9e9207afa6539c85ba5cfebf3e22`  
		Last Modified: Tue, 14 Apr 2026 18:24:03 GMT  
		Size: 2.2 MB (2179439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d12e5da0f5f9cce27555430a40d6dc9e18c54764d62f13fed79c09c33cdd6769`  
		Last Modified: Tue, 14 Apr 2026 18:24:03 GMT  
		Size: 30.7 KB (30714 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.9.7` - linux; s390x

```console
$ docker pull composer@sha256:1f94545e77b0a527f486fd42ce1a3ed8e347a32e951166e75e667c9a8b9c5055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93248850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc4e000a0f721a102b5621d79143082167c85fe36cbab314eff8808e5f343a36`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Mar 2026 23:37:17 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Mar 2026 23:37:17 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Mar 2026 23:37:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Mar 2026 23:37:17 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHP_VERSION=8.5.5
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Thu, 09 Apr 2026 22:21:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 09 Apr 2026 22:21:35 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:27:00 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 09 Apr 2026 22:27:00 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:27:01 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 09 Apr 2026 22:27:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 09 Apr 2026 22:27:01 GMT
CMD ["php" "-a"]
# Thu, 09 Apr 2026 23:18:42 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 09 Apr 2026 23:18:42 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Apr 2026 18:19:36 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Apr 2026 18:19:36 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Apr 2026 18:19:36 GMT
ENV COMPOSER_VERSION=2.9.7
# Tue, 14 Apr 2026 18:19:36 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Apr 2026 18:19:36 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Apr 2026 18:19:36 GMT
WORKDIR /app
# Tue, 14 Apr 2026 18:19:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Apr 2026 18:19:36 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4348d21358ef752a357c33976b85357317bfb623a79cb91ec462b4e5128b82d5`  
		Last Modified: Thu, 12 Mar 2026 23:43:03 GMT  
		Size: 3.8 MB (3795119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a169c2de4deea9b877eb224ec8f2d4f4502dd0bb4e22037516ea41c23c8c1e6`  
		Last Modified: Thu, 12 Mar 2026 23:43:02 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f88a80dfabed7faa02e1bbe28dd4e26c817c26d54bb3411b27cc398ea997ef8`  
		Last Modified: Thu, 12 Mar 2026 23:43:02 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5e7662fcf96af1dfae3edab12e535e5dbb2bd9336314490ac9484222315cc0`  
		Last Modified: Thu, 09 Apr 2026 22:27:14 GMT  
		Size: 14.4 MB (14379286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b2bd611f10e897bc78163d788b300458c71f27af849508076d219371619381`  
		Last Modified: Thu, 09 Apr 2026 22:27:14 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c1175a23bc886b3bc9f9e6845c90d99d1125fc788f6d88d5ad9501ed086f83`  
		Last Modified: Thu, 09 Apr 2026 22:27:15 GMT  
		Size: 21.9 MB (21889964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48a98f93d43e57e9161beb90862e90db489cf9d4b4d09bfbd7d3bc1566f7981`  
		Last Modified: Thu, 09 Apr 2026 22:27:14 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91cdaaeb755a7dbc3a463542f5d9410ef527eb1babc2850059c13f703b6bf5f`  
		Last Modified: Thu, 09 Apr 2026 22:27:15 GMT  
		Size: 23.4 KB (23427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b0c643f457b3285c9b024aac2f31693051af6eb786510b03d7580e65134de8`  
		Last Modified: Thu, 09 Apr 2026 23:19:25 GMT  
		Size: 32.1 MB (32113304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a5512141ecbaa16f283bdbec60a949479d2d7ef6afafc01d5cc3b3351085cd1`  
		Last Modified: Thu, 09 Apr 2026 23:19:20 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd4c500e9eb181938a1ef4ef73f183e9b27420814a10ea55b06e736b40bf16a`  
		Last Modified: Tue, 14 Apr 2026 18:19:51 GMT  
		Size: 17.3 MB (17317554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc53ab4bbf74e12a9c7818288fc97c9f60326574f248c11959ba84015cc1ee0`  
		Last Modified: Tue, 14 Apr 2026 18:19:51 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c73a8be0d813065a838fdca97a14527a4ee7e1530e35f656f93a424f4d7c27`  
		Last Modified: Tue, 14 Apr 2026 18:19:42 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.9.7` - unknown; unknown

```console
$ docker pull composer@sha256:0bc79feb6a333a11cc49a0e80b8edad445b1bc590d108776ee1d1f9cba4c69b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2209891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e15343c996740440561a353bfba972b4a6752dff34802d7eb98b3923520488bd`

```dockerfile
```

-	Layers:
	-	`sha256:10647c8aceb5f18307cac8578a92f75dc319b2558c6f7cfcacc86be9c1ffd2ee`  
		Last Modified: Tue, 14 Apr 2026 18:19:50 GMT  
		Size: 2.2 MB (2179221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ceacdd28fffe318712ca3aebf2993293f60ba3f21a55c590b010d01ac5e20b8`  
		Last Modified: Tue, 14 Apr 2026 18:19:50 GMT  
		Size: 30.7 KB (30670 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:latest`

```console
$ docker pull composer@sha256:709a30cb521103db18992786f7fd747010ad8e24cf581817ddf3e53288d3d281
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
$ docker pull composer@sha256:a3df561dbdddfdb9832ec50f41c0e2f1d27445a67bd71415f05467fedbb2c3c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.2 MB (78237453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39f4699ce5525450650cad74ebb243efd73730fda6d6011a5d805089f9bc61ce`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:17:52 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:17:52 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:17:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:17:52 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:17:52 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:17:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:17:52 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:17:52 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 15 Apr 2026 20:17:52 GMT
ENV PHP_VERSION=8.5.5
# Wed, 15 Apr 2026 20:17:52 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Wed, 15 Apr 2026 20:17:52 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Wed, 15 Apr 2026 20:17:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 20:17:56 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:21:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 20:21:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:21:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 20:21:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 20:21:24 GMT
CMD ["php" "-a"]
# Wed, 15 Apr 2026 21:27:13 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Wed, 15 Apr 2026 21:27:13 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Wed, 15 Apr 2026 21:27:31 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 15 Apr 2026 21:27:31 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 15 Apr 2026 21:27:31 GMT
ENV COMPOSER_VERSION=2.9.7
# Wed, 15 Apr 2026 21:27:31 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Wed, 15 Apr 2026 21:27:31 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 21:27:31 GMT
WORKDIR /app
# Wed, 15 Apr 2026 21:27:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:27:31 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7575019b1e32c16a639f3988d9a63ff1c22c036099e3cb267ea5a97ba0fcb31b`  
		Last Modified: Wed, 15 Apr 2026 20:21:32 GMT  
		Size: 3.6 MB (3587447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba54b7e6d1307c692fb0f98a7bb785c3ae59fda44cbd8dc735eb6d32da25bb2`  
		Last Modified: Wed, 15 Apr 2026 20:21:32 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7367014229e0f5079d78d9d65f87aeb106ffa42ef3cacfdde5ccae68a710662d`  
		Last Modified: Wed, 15 Apr 2026 20:21:32 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c74770868277c77b3c7d8e5aa987ffc0183e76f8a003e5ee3e5662475be115`  
		Last Modified: Wed, 15 Apr 2026 20:21:33 GMT  
		Size: 14.4 MB (14379186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f1108694a36c05d3950260f3491806016ec3ab9ba1da15154bda777858d1eb`  
		Last Modified: Wed, 15 Apr 2026 20:21:33 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e321e76cc80892e05feb16337063a65959f21cd03508ea9f6dd1316bd2bfee6`  
		Last Modified: Wed, 15 Apr 2026 20:21:34 GMT  
		Size: 22.5 MB (22528821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2af3ca59c901474266aab6d50192f869e507a229be1b7493e312a32fac0dff9`  
		Last Modified: Wed, 15 Apr 2026 20:21:33 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b12841ff7824946e17f91cf31b444d9a97e15dc30fa55d79e32ae0c00cf27f1`  
		Last Modified: Wed, 15 Apr 2026 20:21:34 GMT  
		Size: 23.4 KB (23395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e55827933a329097ef03bab9834f516b064faf5b72b18d080e967055a42003`  
		Last Modified: Wed, 15 Apr 2026 21:27:42 GMT  
		Size: 32.8 MB (32828568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2933ad071631f9ce3470578aecae812618fd37d7004987532866b0359f6b6de0`  
		Last Modified: Wed, 15 Apr 2026 21:27:41 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d821667065611cf0d7b4bf7f6d8857b118bfd703fe486289b37884a8edbd61`  
		Last Modified: Wed, 15 Apr 2026 21:27:41 GMT  
		Size: 1.0 MB (1020986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae94261b1892c1af044280991b4f2a5dd150a791ec2eeef5af1ea6d3094479e5`  
		Last Modified: Wed, 15 Apr 2026 21:27:41 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb435422e01857a05128024eb0629a6c60655c0d3b45442ea0bc469f1bbd191`  
		Last Modified: Wed, 15 Apr 2026 21:27:42 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:e85e044ddbc3f14041ddacfb9398391fc8292baa3673ee4c95d5b809632bc41f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2209324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4c877852d538421f4a82316e63e564b40bc167997b6947ce7c9b36533714614`

```dockerfile
```

-	Layers:
	-	`sha256:b9fed10922f5326c3cb699a3c5c5bfb4d7c68743354358d37b16875c5fdd6803`  
		Last Modified: Wed, 15 Apr 2026 21:27:41 GMT  
		Size: 2.2 MB (2178657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:615752e487f6d65b8ad402d079106fe3c4610a7aee9abb3e9350d78067b4501f`  
		Last Modified: Wed, 15 Apr 2026 21:27:41 GMT  
		Size: 30.7 KB (30667 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; arm variant v6

```console
$ docker pull composer@sha256:5f618ede41609642ab0415bf163302848fbba617512b9f3bcb4c81d65aea6016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74743627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e102830ff670832c4941a947728bd57ef6a228b56943b1d8d452c9c6f1e395d8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:19:04 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:19:04 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:19:04 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:19:04 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:19:05 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:19:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:19:05 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:19:05 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:19:05 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 15 Apr 2026 20:19:05 GMT
ENV PHP_VERSION=8.5.5
# Wed, 15 Apr 2026 20:19:05 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Wed, 15 Apr 2026 20:19:05 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Wed, 15 Apr 2026 20:19:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 20:19:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:22:18 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 20:22:18 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:22:19 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 20:22:19 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 20:22:19 GMT
CMD ["php" "-a"]
# Wed, 15 Apr 2026 21:22:04 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Wed, 15 Apr 2026 21:22:04 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Wed, 15 Apr 2026 21:22:27 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 15 Apr 2026 21:22:27 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 15 Apr 2026 21:22:27 GMT
ENV COMPOSER_VERSION=2.9.7
# Wed, 15 Apr 2026 21:22:27 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Wed, 15 Apr 2026 21:22:27 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 21:22:27 GMT
WORKDIR /app
# Wed, 15 Apr 2026 21:22:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:22:27 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1d167fc497e35df23f81ef7d507ee40c904d148d7c5e239db360263ce1228f`  
		Last Modified: Wed, 15 Apr 2026 20:22:24 GMT  
		Size: 3.5 MB (3543048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7893272fc58b639fcb274b9cdac380a99a02b7fec1370991d7043a8d745ee731`  
		Last Modified: Wed, 15 Apr 2026 20:22:24 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b5e2d5fa2204fe8d000332835281efd2beeb4e2b1233fda8377dc9fb8d273da`  
		Last Modified: Wed, 15 Apr 2026 20:22:24 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a237864e95f05b7c9e05c3272f303c8616f39f4b50a113166e6e93f5d6eb2867`  
		Last Modified: Wed, 15 Apr 2026 20:22:25 GMT  
		Size: 14.4 MB (14379195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d6cac0622b9c4733975c694271b5cfe4e9e251f5a29439c27931c4334db09d`  
		Last Modified: Wed, 15 Apr 2026 20:22:25 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a5b1613ded78de2dd5fc3a3cbb57bc91cb6f35c9bf29e262676641888899d35`  
		Last Modified: Wed, 15 Apr 2026 20:22:26 GMT  
		Size: 19.5 MB (19534950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7326187f367c7e04eed9c7cfd2fd94e264bdf5da29600b25762d89f896ee8df`  
		Last Modified: Wed, 15 Apr 2026 20:22:26 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf7aab9524160d3a6dc903858b7d9fc9d77b6f4a09bb6c0cdb0b86eca60acbc`  
		Last Modified: Wed, 15 Apr 2026 20:22:26 GMT  
		Size: 23.2 KB (23204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7338db7ab2e6da871e9ca18bf6e41db656dc01552305f5ea294acd98e45f2ff2`  
		Last Modified: Wed, 15 Apr 2026 21:22:35 GMT  
		Size: 32.7 MB (32665496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acff7d213b0f5a23ec528c0624a11975e61306f0ef4705e003a9109c922c9aaf`  
		Last Modified: Wed, 15 Apr 2026 21:22:34 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ab1a1cc99508981bda26983105462a9a3ee15eae1e24e6da36767b441c2244`  
		Last Modified: Wed, 15 Apr 2026 21:22:34 GMT  
		Size: 1.0 MB (1021023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cff2f6c2aff71864717c706d9c7e23510750ed143e2938cb19d5fdafff8be79`  
		Last Modified: Wed, 15 Apr 2026 21:22:34 GMT  
		Size: 416.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2da733922c6146907c3b3634c5c450c96e0638edddca77a676b7cd813427f9`  
		Last Modified: Wed, 15 Apr 2026 21:22:35 GMT  
		Size: 91.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:1eb3fc19c61b35b8a872d9323204996b304beb4dc10e4d11dfd6b5c14cc219a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:784a99b9ab8555f39e0aa608545bfc075b883ab06336eacb31db1b89b4961c24`

```dockerfile
```

-	Layers:
	-	`sha256:1e8a701178ca230dc13cbb78d4e4d281f47957950cbb2e2298d741398449207b`  
		Last Modified: Wed, 15 Apr 2026 21:22:33 GMT  
		Size: 30.6 KB (30557 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; arm variant v7

```console
$ docker pull composer@sha256:582284655bf553416dbce90c395b4dc89da3a7edc9da012ec6e01407c1430ed9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.6 MB (71571453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f9ac974387fafeac611e90eeb97b0514811d16f37141c1796d8eebb9f19295e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:18:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:18:22 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:18:22 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:18:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:18:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:18:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:18:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:18:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:18:22 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 15 Apr 2026 20:18:22 GMT
ENV PHP_VERSION=8.5.5
# Wed, 15 Apr 2026 20:18:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Wed, 15 Apr 2026 20:18:22 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Wed, 15 Apr 2026 20:18:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 20:18:26 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:21:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 20:21:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:21:34 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 20:21:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 20:21:34 GMT
CMD ["php" "-a"]
# Wed, 15 Apr 2026 21:32:22 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Wed, 15 Apr 2026 21:32:22 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Wed, 15 Apr 2026 21:32:44 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 15 Apr 2026 21:32:44 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 15 Apr 2026 21:32:44 GMT
ENV COMPOSER_VERSION=2.9.7
# Wed, 15 Apr 2026 21:32:44 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Wed, 15 Apr 2026 21:32:44 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 21:32:45 GMT
WORKDIR /app
# Wed, 15 Apr 2026 21:32:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:32:45 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40243011337e75e1e1aba1a01eff0f25c670f2784f31a19fe3ceeb28d9cbb386`  
		Last Modified: Wed, 15 Apr 2026 20:21:41 GMT  
		Size: 3.3 MB (3343352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289d25cb3dc6bf4d1acfe704c1d05a812b84cbfe26b06c6e9a423f281efcfd64`  
		Last Modified: Wed, 15 Apr 2026 20:21:41 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457ef191b478c4407082d1c51e695feac2f4425353d54d5d6737f8e3aede1686`  
		Last Modified: Wed, 15 Apr 2026 20:21:41 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef8f20263bc5a42b03699b180b432cb94cb313e98aed5a4238024d8cd3f252ad`  
		Last Modified: Wed, 15 Apr 2026 20:21:41 GMT  
		Size: 14.4 MB (14379203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654a3e48df9d037dc7d582e4d7e753ead3d5f55b619c07d29f0f2701eabf4657`  
		Last Modified: Wed, 15 Apr 2026 20:21:43 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00b79e1670ab000b58c3fa612bf97d881357d5a02a37a01aab4448a263a56aa`  
		Last Modified: Wed, 15 Apr 2026 20:21:43 GMT  
		Size: 18.4 MB (18430268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:670c3d79616cd5914f7e4d0d94505d6570f152e3fab437081ba1b2499bf253df`  
		Last Modified: Wed, 15 Apr 2026 20:21:43 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773025cf5591ee7e2a345d9e429358f0269bd41230fb2da781a05eb990ef0386`  
		Last Modified: Wed, 15 Apr 2026 20:21:43 GMT  
		Size: 23.2 KB (23204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acebb0a04354316add548495911389085f450934caee74f83d543b9e72b2d05e`  
		Last Modified: Wed, 15 Apr 2026 21:32:54 GMT  
		Size: 31.1 MB (31096001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a09a4d2f176f1708944c561d076f811601d10ce9c12f67f368beb5f33e872e0`  
		Last Modified: Wed, 15 Apr 2026 21:32:53 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4554ab557c57e190e9a9c96595d8f20842cdf6c58419124406570b03fb325ec8`  
		Last Modified: Wed, 15 Apr 2026 21:32:54 GMT  
		Size: 1.0 MB (1011452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba1c93167f863ddcc1d5c2653b03c6a8642c2fd9559327b73ed8624251ec144`  
		Last Modified: Wed, 15 Apr 2026 21:32:54 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c681ef1dc9504c4c3f4ad0cf3ffc7c285a57f04dbacae219663ef575ca6acf`  
		Last Modified: Wed, 15 Apr 2026 21:32:55 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:32d0c9b1e4d5d571639eb8de3fd2347a367f829d380db08ff8dbf370f5b11cc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2209101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23ebcb2c2afc717904235ca8d45b56e040e43ae27f90d904adef6de85485e0c1`

```dockerfile
```

-	Layers:
	-	`sha256:1ea500bcc75e9906fcbd4ac18fb9f32b00e2f232209a8695dbdd04027eae30b1`  
		Last Modified: Wed, 15 Apr 2026 21:32:54 GMT  
		Size: 2.2 MB (2178328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d85d9fe7060afbbf94f473725bfe33d128da115ed642a56a0a3c11dc35b8ad8a`  
		Last Modified: Wed, 15 Apr 2026 21:32:53 GMT  
		Size: 30.8 KB (30773 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:02cc0a1729b9f75734a6f1789ad59fa90c54bdb84566b2c7b564f7eaafd5c368
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77892271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b9aa3f48599c920e9268b74581f5d0d24a2eca014342e24e60e1d70f8bfb5ae`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:21 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:16:21 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:16:21 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:16:21 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:16:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:16:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:16:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:16:21 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:16:21 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 15 Apr 2026 20:16:21 GMT
ENV PHP_VERSION=8.5.5
# Wed, 15 Apr 2026 20:16:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Wed, 15 Apr 2026 20:16:21 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Wed, 15 Apr 2026 20:16:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 20:16:25 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:19:57 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 20:19:57 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:19:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 20:19:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 20:19:58 GMT
CMD ["php" "-a"]
# Wed, 15 Apr 2026 21:40:09 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Wed, 15 Apr 2026 21:40:09 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Wed, 15 Apr 2026 21:40:29 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 15 Apr 2026 21:40:29 GMT
ENV COMPOSER_HOME=/tmp
# Wed, 15 Apr 2026 21:40:29 GMT
ENV COMPOSER_VERSION=2.9.7
# Wed, 15 Apr 2026 21:40:29 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Wed, 15 Apr 2026 21:40:29 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 21:40:29 GMT
WORKDIR /app
# Wed, 15 Apr 2026 21:40:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:40:29 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e4c5bcbf8c3068a7d4c178cdd5132463fa53adf8c55efe0d5a02126d958e69`  
		Last Modified: Wed, 15 Apr 2026 20:20:06 GMT  
		Size: 3.6 MB (3596134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c0edc310dc19501413b5668245bc984741c4ac5a3219932a74e83fb33b6f94`  
		Last Modified: Wed, 15 Apr 2026 20:20:02 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d665080207d06b6b7246d46376f6ec0b3a5d072b47f01ab3fe89eb95ea0b9310`  
		Last Modified: Wed, 15 Apr 2026 20:20:02 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e92dbfc45c4b506749680c4bded773db9170a5c594ae07c33aa938ac9b46a1c`  
		Last Modified: Wed, 15 Apr 2026 20:20:07 GMT  
		Size: 14.4 MB (14379192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da631dfa865e2d394e47bb93c95f041d309af42b22cd597826fab10299773bc`  
		Last Modified: Wed, 15 Apr 2026 20:20:03 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0885f624969f9911f18390a16714e49ddcba2831ee9c8002d794ee56d8ca9ca8`  
		Last Modified: Wed, 15 Apr 2026 20:20:07 GMT  
		Size: 21.7 MB (21697840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e202517af7cb78a86ff7f8b255ca452261912c8830cf0b7e352386b5c5472454`  
		Last Modified: Wed, 15 Apr 2026 20:20:05 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4062a55681ba2c31424930678c18614b1e9e0eb63f551ee5faaa3857658f4f0`  
		Last Modified: Wed, 15 Apr 2026 20:20:07 GMT  
		Size: 23.2 KB (23209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247694cf5276fc930925fbd3c766f23524e3c168100355ab0759b2996481c9fe`  
		Last Modified: Wed, 15 Apr 2026 21:40:39 GMT  
		Size: 33.0 MB (32971344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd2df09b94d664b93dffeea3fcc3ec248ab74647c5a4214efe19bfb47fcb05a8`  
		Last Modified: Wed, 15 Apr 2026 21:40:38 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ddb215ec4272be553f5bc3174320405b2f1a91262a8dcef2e0a86a9e49ee716`  
		Last Modified: Wed, 15 Apr 2026 21:40:38 GMT  
		Size: 1.0 MB (1019831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf4152796a067e6883c8510bc549ef6efa7a2938ae8a777ac16b9ce0064b7cb`  
		Last Modified: Wed, 15 Apr 2026 21:40:38 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2e497f91b5d80958253e7e10d4c15d00acc6326888e106b429a9c5308f89fe`  
		Last Modified: Wed, 15 Apr 2026 21:40:39 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:fe7799a0766fcb90d3eee27476e71e060d8359ba6a1af526e40143a0b717c9fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2208959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c81eae5c2a8041b04dcb4644dca7f3e06622961ff2e597b7542f07cfbf49fb89`

```dockerfile
```

-	Layers:
	-	`sha256:b2e0891d2073a415183d3e4d591453fd999ea34870c33d681160d6f91ac3e8e6`  
		Last Modified: Wed, 15 Apr 2026 21:40:38 GMT  
		Size: 2.2 MB (2178158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a29947e152eea3d30a8612f8ec8d06ba8dac35f21c5319fc14e247056d17a8a`  
		Last Modified: Wed, 15 Apr 2026 21:40:38 GMT  
		Size: 30.8 KB (30801 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; 386

```console
$ docker pull composer@sha256:5059aa7f8aeb8fd9ad00e166cfc4504d01b632d5c987150dfde3e7167b11e492
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82480079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05da3dd80cd6d3c296bb9f77ac1d48716d0282b354fc840118af6947f2db6dbd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Fri, 10 Apr 2026 00:13:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 10 Apr 2026 00:13:16 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 10 Apr 2026 00:13:16 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 10 Apr 2026 00:13:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 10 Apr 2026 00:13:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 10 Apr 2026 00:13:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 10 Apr 2026 00:13:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 10 Apr 2026 00:13:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 10 Apr 2026 00:13:16 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 10 Apr 2026 00:13:16 GMT
ENV PHP_VERSION=8.5.5
# Fri, 10 Apr 2026 00:13:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Fri, 10 Apr 2026 00:13:16 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Fri, 10 Apr 2026 00:13:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 10 Apr 2026 00:13:20 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 00:16:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 10 Apr 2026 00:16:53 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 00:16:54 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 10 Apr 2026 00:16:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 10 Apr 2026 00:16:54 GMT
CMD ["php" "-a"]
# Tue, 14 Apr 2026 18:19:28 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Apr 2026 18:19:28 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Apr 2026 18:19:47 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Apr 2026 18:19:47 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Apr 2026 18:19:47 GMT
ENV COMPOSER_VERSION=2.9.7
# Tue, 14 Apr 2026 18:19:47 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Apr 2026 18:19:48 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Apr 2026 18:19:48 GMT
WORKDIR /app
# Tue, 14 Apr 2026 18:19:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Apr 2026 18:19:48 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d2062b0536d4d6a1543e3a6bfd55452c7706979a7def0ad5ff0f3e183f183d`  
		Last Modified: Fri, 10 Apr 2026 00:17:02 GMT  
		Size: 5.9 MB (5909460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb9b53f46bb29bde8242534cc51035c71b65536a0a0acada6428f7a8ba0889c`  
		Last Modified: Fri, 10 Apr 2026 00:17:02 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab50b39601a88f935ec690047331c7481ff9b7ae2bb959cfc4cc98313c492986`  
		Last Modified: Fri, 10 Apr 2026 00:17:02 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92225e063d6f653398ed45adcff1579a3a3cf3ccbe764a4bb5b301283ee3b2ee`  
		Last Modified: Fri, 10 Apr 2026 00:17:02 GMT  
		Size: 14.4 MB (14379292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ccaecce131db93828716f892d3ad6e523dec70db239cc1bed3bb5394e8396c`  
		Last Modified: Fri, 10 Apr 2026 00:17:03 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e4efa73be7dce94cd5df6088620edcd50156eafe81c782274c129a7a3e191d`  
		Last Modified: Fri, 10 Apr 2026 00:17:04 GMT  
		Size: 23.4 MB (23438953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab8684032f9c15ecd79788e50ca55f90486d5bf79b5b3a24018772984e7a1cb5`  
		Last Modified: Fri, 10 Apr 2026 00:17:04 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba72ff6334ace2c9a0d737cdf3c0fa9f61f267a07af45bf21e2ff77820277e5`  
		Last Modified: Fri, 10 Apr 2026 00:17:04 GMT  
		Size: 23.6 KB (23625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb92bca6a7200abd5ed57acbc2406d1b631ce897e9fcb8321df6d6ad30cb6114`  
		Last Modified: Tue, 14 Apr 2026 18:19:58 GMT  
		Size: 33.4 MB (33354023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3acb4361787726cd8ad52c3d9467b84e1d1aa7dfe6414e7e3be8d2816cc76617`  
		Last Modified: Tue, 14 Apr 2026 18:19:57 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9241059ece99827922266cdf5f4d2003877d75ddf68699cd4c70ce7987a21836`  
		Last Modified: Tue, 14 Apr 2026 18:19:57 GMT  
		Size: 1.7 MB (1682879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69641c04f229a2ab6016f07abf23bea732612f28baf219fd9fcf0c899d7617e5`  
		Last Modified: Tue, 14 Apr 2026 18:19:42 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67f4289f14f4bb7e5b1629ac4c78856e0c3b60c94f52f95daa671e1a219d5df8`  
		Last Modified: Tue, 14 Apr 2026 18:19:59 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:c254802094079f1308563379ad369533970752e4908cfa224d9e97811d3d39ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2211056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4ce198e58e85ea5dc923b1568aaa064676ae0112aaf5ac90c6cc3e58fdc12bf`

```dockerfile
```

-	Layers:
	-	`sha256:340334093e4da71051f77042453963dbc6f4fd36456e9b67f499e0b94970d025`  
		Last Modified: Tue, 14 Apr 2026 18:19:57 GMT  
		Size: 2.2 MB (2180425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47bf377a779ae13fd18570cc75e3fe8f0a691c683d330c3c388994b1f8641121`  
		Last Modified: Tue, 14 Apr 2026 18:19:57 GMT  
		Size: 30.6 KB (30631 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; ppc64le

```console
$ docker pull composer@sha256:6b0debe85067d180c3dca5be15549aa709e405e5c6da97f106b302afa0be7b3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 MB (96713081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d658b5ad399d03987449b91b37ae36fb531e2591aba9b560f1469876bcd1472`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Thu, 12 Mar 2026 23:53:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Mar 2026 23:53:02 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Mar 2026 23:53:02 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Mar 2026 23:53:02 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Mar 2026 23:53:02 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Mar 2026 23:53:02 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Mar 2026 23:53:02 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Mar 2026 23:53:02 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Mar 2026 23:53:02 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 12 Mar 2026 23:53:02 GMT
ENV PHP_VERSION=8.5.5
# Thu, 12 Mar 2026 23:53:02 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Thu, 12 Mar 2026 23:53:02 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Thu, 09 Apr 2026 22:33:42 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 09 Apr 2026 22:33:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:38:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 09 Apr 2026 22:38:29 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:38:30 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 09 Apr 2026 22:38:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 09 Apr 2026 22:38:30 GMT
CMD ["php" "-a"]
# Fri, 10 Apr 2026 00:21:05 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 10 Apr 2026 00:21:07 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Apr 2026 18:19:02 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Apr 2026 18:19:02 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Apr 2026 18:19:02 GMT
ENV COMPOSER_VERSION=2.9.7
# Tue, 14 Apr 2026 18:19:02 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Apr 2026 18:19:05 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Apr 2026 18:19:09 GMT
WORKDIR /app
# Tue, 14 Apr 2026 18:19:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Apr 2026 18:19:09 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7db1cc7b26f64d5de44e75f81962c30dead7dbc1dae3ebb93d0dc3d0cea721a`  
		Last Modified: Thu, 12 Mar 2026 23:58:51 GMT  
		Size: 3.8 MB (3768852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4a23ff5963c3f844b77db123769c733318f6ad54386c9f63e356424059470b`  
		Last Modified: Thu, 12 Mar 2026 23:58:51 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a071b7623ea30b2e8950858971a7e7838856db9c469a46b6305dcd619d0531fc`  
		Last Modified: Thu, 12 Mar 2026 23:58:51 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d012a34014d339e95156eab3252cc22fbae82a4670be3766b110c04e96ff1a17`  
		Last Modified: Thu, 09 Apr 2026 22:38:45 GMT  
		Size: 14.4 MB (14379301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8b7c5afa56dcdf0f01aaba59b305697db6b72603309ba573605f5fcd422fc0`  
		Last Modified: Thu, 09 Apr 2026 22:38:45 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1971acbe5d44b0f37d3698908a5766cea69f16ef4c4472ca8a30f5d48eec93ec`  
		Last Modified: Thu, 09 Apr 2026 22:38:46 GMT  
		Size: 23.1 MB (23118163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ee71922b29fe2228fde987804ee785c857383e7941a35e885bb5f06b7c3aba`  
		Last Modified: Thu, 09 Apr 2026 22:38:45 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fbefb03f1cf2736ed7b9f334b7e8f2f16dbedad1876c833ba4682b99ca9f99a`  
		Last Modified: Thu, 09 Apr 2026 22:38:46 GMT  
		Size: 23.4 KB (23442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db29015527299944deffccc76c5bfb597208be66aea62b09cf37a0cef1bb364e`  
		Last Modified: Fri, 10 Apr 2026 00:22:19 GMT  
		Size: 34.2 MB (34177434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972a41e22feca9d4bfcc298283918766cb03ebb7dd146ebbded895c8b431c973`  
		Last Modified: Fri, 10 Apr 2026 00:22:17 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efaac84e88b2da4e607702934bba5a10ee9d45974d858538b478a29b89842e33`  
		Last Modified: Tue, 14 Apr 2026 18:19:37 GMT  
		Size: 17.4 MB (17411381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e029883ecefeeaf8733085cd8e526dfbbca7e594b984c759f9d554d542181f0`  
		Last Modified: Tue, 14 Apr 2026 18:19:37 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebb4782c2d3dfa3ac371b8a44cd1f51c8cca8d476ce08683daefb52097b9bf7`  
		Last Modified: Tue, 14 Apr 2026 18:19:37 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:b96e3b5bce750eb3282de808dd8aafbf3a051c5f80e3f716df031de690321657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2211215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5342929d05c922fd2d787aa2179debfaee17cdccf8781a7e329e1d3d484d07f1`

```dockerfile
```

-	Layers:
	-	`sha256:fc050012567990ae6904da1426da82a6cc21eeb168d8d2fa9b316fe513258f54`  
		Last Modified: Tue, 14 Apr 2026 18:19:37 GMT  
		Size: 2.2 MB (2180498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dc4ab7a528f883fc6476f1d2c72c9454b32b1cd4fefe0ac8fb1da3fec8e6c44`  
		Last Modified: Tue, 14 Apr 2026 18:19:37 GMT  
		Size: 30.7 KB (30717 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; riscv64

```console
$ docker pull composer@sha256:600f68dee998197590fbadd5f49b007afb10faf4f15287a315a79fa198635908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.1 MB (78108283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abd844ec36780aac229ca2fdb372bcc3b96fc3ad9a0c8de0b25c8458b53af256`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 09:13:06 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 28 Jan 2026 09:13:06 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 28 Jan 2026 09:13:06 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 28 Jan 2026 09:13:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 28 Jan 2026 09:13:07 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 28 Jan 2026 09:13:07 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_VERSION=8.5.5
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Fri, 10 Apr 2026 09:29:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 10 Apr 2026 09:29:21 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 10:28:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 10 Apr 2026 10:28:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 10:28:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 10 Apr 2026 10:28:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 10 Apr 2026 10:28:33 GMT
CMD ["php" "-a"]
# Sun, 12 Apr 2026 09:33:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Sun, 12 Apr 2026 09:33:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Apr 2026 18:22:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Apr 2026 18:22:48 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Apr 2026 18:22:48 GMT
ENV COMPOSER_VERSION=2.9.7
# Tue, 14 Apr 2026 18:22:48 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Apr 2026 18:22:48 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Apr 2026 18:22:48 GMT
WORKDIR /app
# Tue, 14 Apr 2026 18:22:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Apr 2026 18:22:48 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d64a68485fdb9ab2ec4159ac3e04e0bb79d9f1d037e580e928ca2b9604180f`  
		Last Modified: Wed, 28 Jan 2026 10:13:59 GMT  
		Size: 3.7 MB (3741000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b030c1b113432578231e8fe7c8a1bc913f2dc5dcba512e805fa9ab07768c9bd4`  
		Last Modified: Wed, 28 Jan 2026 10:13:58 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32a0e9bcb36b34307b4eada1f50c1cd4244d43d19ee57d962818dcb0ff0b110`  
		Last Modified: Wed, 28 Jan 2026 10:13:58 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20501e9e3d17b72af47b7d522d0c369998be222ed66ed9070ed2cbc45e500ca7`  
		Last Modified: Fri, 10 Apr 2026 10:29:42 GMT  
		Size: 14.4 MB (14379290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f7fa0bbe8ea35a7aeededb6a1c62d4e192d88a3cbaa6a9ac613390cef5f797e`  
		Last Modified: Fri, 10 Apr 2026 10:29:38 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c00b6c348638ca2fb138534e98df3a83c5788350e7f682c5dab61388d5988a1`  
		Last Modified: Fri, 10 Apr 2026 10:29:43 GMT  
		Size: 20.8 MB (20772153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf32615937490fdbee93796b59955ce07e051f019b76917819692421da228ef`  
		Last Modified: Fri, 10 Apr 2026 10:29:38 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491cab84c5a842c690a34c22c4cfe20f23d7b27019ca9d80e387fd23ef96828d`  
		Last Modified: Fri, 10 Apr 2026 10:29:39 GMT  
		Size: 23.3 KB (23349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e865e7a35bee8605e802d4714eef1a4cd079ed0b68a414c076e698d97cfbedd6`  
		Last Modified: Sun, 12 Apr 2026 09:38:57 GMT  
		Size: 31.3 MB (31300012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:670c7192db5936f38910b865b3f6746b70a4b2523b1e25db7d274900db0fca4f`  
		Last Modified: Sun, 12 Apr 2026 09:38:52 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849fae3a43556661d0d79306c12a48046432673ac49917b14937307d36a24458`  
		Last Modified: Tue, 14 Apr 2026 18:24:04 GMT  
		Size: 4.3 MB (4302324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01efda7965080036e2b76754ef2276308322ed2394f97d073063348bded60a09`  
		Last Modified: Tue, 14 Apr 2026 18:24:03 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5997a67e70609c3ecf2d0c94e158584b948e5f7e90a85dd896325c6db3a7ed`  
		Last Modified: Tue, 14 Apr 2026 18:22:53 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:55155328eaf6b4a8b732344c31723c0e2e7026edb1151e056f7260b0c23793eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2210153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baabb88b9e58574b8449e58ff8e49bdd472dd2b4eac9aec0cd90224e32a110f8`

```dockerfile
```

-	Layers:
	-	`sha256:14f5989ff5313284e35f85efde25d95ba6cf9e9207afa6539c85ba5cfebf3e22`  
		Last Modified: Tue, 14 Apr 2026 18:24:03 GMT  
		Size: 2.2 MB (2179439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d12e5da0f5f9cce27555430a40d6dc9e18c54764d62f13fed79c09c33cdd6769`  
		Last Modified: Tue, 14 Apr 2026 18:24:03 GMT  
		Size: 30.7 KB (30714 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; s390x

```console
$ docker pull composer@sha256:1f94545e77b0a527f486fd42ce1a3ed8e347a32e951166e75e667c9a8b9c5055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93248850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc4e000a0f721a102b5621d79143082167c85fe36cbab314eff8808e5f343a36`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Mar 2026 23:37:17 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Mar 2026 23:37:17 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Mar 2026 23:37:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Mar 2026 23:37:17 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHP_VERSION=8.5.5
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Thu, 09 Apr 2026 22:21:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 09 Apr 2026 22:21:35 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:27:00 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 09 Apr 2026 22:27:00 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:27:01 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 09 Apr 2026 22:27:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 09 Apr 2026 22:27:01 GMT
CMD ["php" "-a"]
# Thu, 09 Apr 2026 23:18:42 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Thu, 09 Apr 2026 23:18:42 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Apr 2026 18:19:36 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Apr 2026 18:19:36 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Apr 2026 18:19:36 GMT
ENV COMPOSER_VERSION=2.9.7
# Tue, 14 Apr 2026 18:19:36 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Apr 2026 18:19:36 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Apr 2026 18:19:36 GMT
WORKDIR /app
# Tue, 14 Apr 2026 18:19:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Apr 2026 18:19:36 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4348d21358ef752a357c33976b85357317bfb623a79cb91ec462b4e5128b82d5`  
		Last Modified: Thu, 12 Mar 2026 23:43:03 GMT  
		Size: 3.8 MB (3795119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a169c2de4deea9b877eb224ec8f2d4f4502dd0bb4e22037516ea41c23c8c1e6`  
		Last Modified: Thu, 12 Mar 2026 23:43:02 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f88a80dfabed7faa02e1bbe28dd4e26c817c26d54bb3411b27cc398ea997ef8`  
		Last Modified: Thu, 12 Mar 2026 23:43:02 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5e7662fcf96af1dfae3edab12e535e5dbb2bd9336314490ac9484222315cc0`  
		Last Modified: Thu, 09 Apr 2026 22:27:14 GMT  
		Size: 14.4 MB (14379286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b2bd611f10e897bc78163d788b300458c71f27af849508076d219371619381`  
		Last Modified: Thu, 09 Apr 2026 22:27:14 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c1175a23bc886b3bc9f9e6845c90d99d1125fc788f6d88d5ad9501ed086f83`  
		Last Modified: Thu, 09 Apr 2026 22:27:15 GMT  
		Size: 21.9 MB (21889964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48a98f93d43e57e9161beb90862e90db489cf9d4b4d09bfbd7d3bc1566f7981`  
		Last Modified: Thu, 09 Apr 2026 22:27:14 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91cdaaeb755a7dbc3a463542f5d9410ef527eb1babc2850059c13f703b6bf5f`  
		Last Modified: Thu, 09 Apr 2026 22:27:15 GMT  
		Size: 23.4 KB (23427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b0c643f457b3285c9b024aac2f31693051af6eb786510b03d7580e65134de8`  
		Last Modified: Thu, 09 Apr 2026 23:19:25 GMT  
		Size: 32.1 MB (32113304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a5512141ecbaa16f283bdbec60a949479d2d7ef6afafc01d5cc3b3351085cd1`  
		Last Modified: Thu, 09 Apr 2026 23:19:20 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd4c500e9eb181938a1ef4ef73f183e9b27420814a10ea55b06e736b40bf16a`  
		Last Modified: Tue, 14 Apr 2026 18:19:51 GMT  
		Size: 17.3 MB (17317554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc53ab4bbf74e12a9c7818288fc97c9f60326574f248c11959ba84015cc1ee0`  
		Last Modified: Tue, 14 Apr 2026 18:19:51 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c73a8be0d813065a838fdca97a14527a4ee7e1530e35f656f93a424f4d7c27`  
		Last Modified: Tue, 14 Apr 2026 18:19:42 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:0bc79feb6a333a11cc49a0e80b8edad445b1bc590d108776ee1d1f9cba4c69b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2209891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e15343c996740440561a353bfba972b4a6752dff34802d7eb98b3923520488bd`

```dockerfile
```

-	Layers:
	-	`sha256:10647c8aceb5f18307cac8578a92f75dc319b2558c6f7cfcacc86be9c1ffd2ee`  
		Last Modified: Tue, 14 Apr 2026 18:19:50 GMT  
		Size: 2.2 MB (2179221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ceacdd28fffe318712ca3aebf2993293f60ba3f21a55c590b010d01ac5e20b8`  
		Last Modified: Tue, 14 Apr 2026 18:19:50 GMT  
		Size: 30.7 KB (30670 bytes)  
		MIME: application/vnd.in-toto+json
