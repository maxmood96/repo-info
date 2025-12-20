## `php:8-zts-alpine3.22`

```console
$ docker pull php@sha256:fa69f5d83e2e2650575e76c6c8669d0d8ea0150121f3e40e7aa856c2cb5b934b
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

### `php:8-zts-alpine3.22` - linux; amd64

```console
$ docker pull php@sha256:ccacc3d59f1d6c56bdc2fdb337c15efe3da035af366dccd2cbd97cfc5629c611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49933928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d09f4b85df6ff76158261aa6ace6bab6c92acac579e690f756821de916ca7ef9`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 21:16:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 18 Dec 2025 21:16:48 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 18 Dec 2025 21:16:48 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 18 Dec 2025 21:16:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Dec 2025 21:16:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Dec 2025 21:16:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Dec 2025 21:16:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Dec 2025 21:16:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Dec 2025 21:16:48 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 18 Dec 2025 21:16:48 GMT
ENV PHP_VERSION=8.5.1
# Thu, 18 Dec 2025 21:16:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.1.tar.xz.asc
# Thu, 18 Dec 2025 21:16:48 GMT
ENV PHP_SHA256=3f5bf99ce81201f526d25e288eddb2cfa111d068950d1e9a869530054ff98815
# Thu, 18 Dec 2025 21:16:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 18 Dec 2025 21:16:52 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 21:20:18 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Dec 2025 21:20:18 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 21:20:19 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Dec 2025 21:20:19 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Dec 2025 21:20:19 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f1ef89453576ba1d8b007d5100e5e72bb0a3b2a15609a7b2f100f8e664f0ba`  
		Last Modified: Thu, 18 Dec 2025 21:20:36 GMT  
		Size: 3.5 MB (3464316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8954dc3909dc6ba7e29d8b0215268eb53fe65414a948def1f91f2a05ca937b6`  
		Last Modified: Thu, 18 Dec 2025 21:20:35 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f286ce0d3d41bfd553d24003cad2061e0885453378f23804f336a9ad05ea2bc`  
		Last Modified: Thu, 18 Dec 2025 21:20:35 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2a65e61b2a43ac24e99fd57c7a6b9d375d594e9b836fd0785552f880963646`  
		Last Modified: Thu, 18 Dec 2025 21:20:37 GMT  
		Size: 14.3 MB (14348057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee947b510400a3e1211e599bb12bc37ce50b5a2d9d806b736b0ab4204e66ff0`  
		Last Modified: Thu, 18 Dec 2025 21:20:35 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033da7c5e4d8b53d3bd66ebe44a704b823d3e1d5c47e43e06fc2b365b46d7b17`  
		Last Modified: Thu, 18 Dec 2025 21:20:39 GMT  
		Size: 28.3 MB (28294936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7724b73130eae8ceceec4e6bdb60253b177fdb17507759d188ce13b44596ec8`  
		Last Modified: Thu, 18 Dec 2025 21:20:36 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a1d2fdd7dccc0b8e6399e0216a12c666e71c0a8ab209651dd1ed88767937960`  
		Last Modified: Thu, 18 Dec 2025 21:20:36 GMT  
		Size: 20.1 KB (20079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-alpine3.22` - unknown; unknown

```console
$ docker pull php@sha256:88f98df7985ccbcaef5a576d4cbe2826294bbb75483a9e9dd713a4ac46d96894
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.1 KB (315125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f84375ec9ff8a7dab3710b5036f3e69140ee9e857494a705d02ea2cdc758c77`

```dockerfile
```

-	Layers:
	-	`sha256:044643a58da3bc7a14a08b1c8834e097c7235529e26b7d7f22a7e97c2aa2194c`  
		Last Modified: Fri, 19 Dec 2025 00:01:55 GMT  
		Size: 278.1 KB (278085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8dbc68455d0239e9bc7dec14fe22f46af7777b9783dfdd9b2d76f53a1951ae9`  
		Last Modified: Fri, 19 Dec 2025 00:01:56 GMT  
		Size: 37.0 KB (37040 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts-alpine3.22` - linux; arm variant v6

```console
$ docker pull php@sha256:0dd6f0a590ac28e3e391294eeee37b6afc7ec01fa6d5337d42c66d1cc1fa0c15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45928325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa4a3fdad4ea55072481a71f6b3aa09eb955cc4a78653dd69c670dd7f848df5a`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 21:18:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 18 Dec 2025 21:18:42 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 18 Dec 2025 21:18:42 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 18 Dec 2025 21:18:42 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Dec 2025 21:18:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Dec 2025 21:18:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Dec 2025 21:18:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Dec 2025 21:18:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Dec 2025 21:18:43 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 18 Dec 2025 21:18:43 GMT
ENV PHP_VERSION=8.5.1
# Thu, 18 Dec 2025 21:18:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.1.tar.xz.asc
# Thu, 18 Dec 2025 21:18:43 GMT
ENV PHP_SHA256=3f5bf99ce81201f526d25e288eddb2cfa111d068950d1e9a869530054ff98815
# Thu, 18 Dec 2025 21:18:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 18 Dec 2025 21:18:47 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 21:22:02 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Dec 2025 21:22:02 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 21:22:03 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Dec 2025 21:22:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Dec 2025 21:22:03 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Sun, 07 Dec 2025 22:05:32 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75408393c71de40ba4858d6087ae2d5c2045e98251fd4b676949fba55e115384`  
		Last Modified: Thu, 18 Dec 2025 21:22:17 GMT  
		Size: 3.4 MB (3428660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c0e0c7c2534ae2fcb2f52f9989cafb668220e8c32f2fc8b84024bc808023804`  
		Last Modified: Thu, 18 Dec 2025 21:22:17 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03a0c63bb2c4eaf5253cbe94abc3a3682bc054f72e9f2e406dcc1c05af420e8`  
		Last Modified: Thu, 18 Dec 2025 21:22:17 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:261b2ecd82038fd24479f6b135c438d9f7e795ad33f360bc40e4235940ce80a3`  
		Last Modified: Thu, 18 Dec 2025 21:22:18 GMT  
		Size: 14.3 MB (14348070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50151be2dad4395c321a7d923506988c362b0ea2cf6d28dd1a55d563a32aaeb`  
		Last Modified: Thu, 18 Dec 2025 21:22:17 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b99e1f951433f0b4704db2cccf53234531cc17abfff6dbbc7ef33dc1affb46`  
		Last Modified: Thu, 18 Dec 2025 21:22:19 GMT  
		Size: 24.6 MB (24623556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2b2d04eff00c09d8d7d65cbce264e4b1b6254813ce7e2ed5070ec85f2aeda6`  
		Last Modified: Thu, 18 Dec 2025 21:22:17 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58719312ef775687bc5775339c80c7ab58f5f6f326793193531d2fc9e79ec83`  
		Last Modified: Thu, 18 Dec 2025 21:22:17 GMT  
		Size: 19.9 KB (19866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-alpine3.22` - unknown; unknown

```console
$ docker pull php@sha256:723a5f3259a705d9c34e2caab01e4a0586e42749c796c2bad52187e1a5a04a89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 KB (36970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f95487713425043c4fd520243f9ea446723134c0422f409ebe41de42af449c7`

```dockerfile
```

-	Layers:
	-	`sha256:62ca3631d7ba27c6b0f7ca0b20a32c62dbf5d17dadf38784d08c62de4ac63bd3`  
		Last Modified: Fri, 19 Dec 2025 00:01:59 GMT  
		Size: 37.0 KB (36970 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts-alpine3.22` - linux; arm variant v7

```console
$ docker pull php@sha256:ec5f8c23317c8351c87ddc673b682bfc4d70efdb05862205e61eeee1848a299f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44062122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c80eeb7e9a0347ce2edb21701648efe22ac9f1a4cfbd6c67e6b915be7b095e47`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 21:11:44 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 18 Dec 2025 21:11:44 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 18 Dec 2025 21:11:44 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 18 Dec 2025 21:11:44 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Dec 2025 21:11:44 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Dec 2025 21:11:44 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Dec 2025 21:11:44 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Dec 2025 21:11:44 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Dec 2025 21:11:44 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 18 Dec 2025 21:11:44 GMT
ENV PHP_VERSION=8.5.1
# Thu, 18 Dec 2025 21:11:44 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.1.tar.xz.asc
# Thu, 18 Dec 2025 21:11:44 GMT
ENV PHP_SHA256=3f5bf99ce81201f526d25e288eddb2cfa111d068950d1e9a869530054ff98815
# Thu, 18 Dec 2025 21:11:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 18 Dec 2025 21:11:48 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 21:15:01 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Dec 2025 21:15:01 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 21:15:02 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Dec 2025 21:15:02 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Dec 2025 21:15:02 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Sun, 07 Dec 2025 13:57:17 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edcf49a0dcc922eea6c8d6f082bb8f3b0896348ea924fa4233c6b2eaffc94bb5`  
		Last Modified: Thu, 18 Dec 2025 21:15:18 GMT  
		Size: 3.2 MB (3244501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ab3275ae98b165f49d5d2e1cbdc575db3db2c03168b7f1e2e86083c089c768`  
		Last Modified: Thu, 18 Dec 2025 21:15:18 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d651abe30dcea00a304ec948cd82242aea181108963b69304f689bb6d1ad02c9`  
		Last Modified: Thu, 18 Dec 2025 21:15:18 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cbb32ebdd8e6b425040439274addd29bb68e2efe53fe0f9d56cfe3de9daaabb`  
		Last Modified: Thu, 18 Dec 2025 21:15:22 GMT  
		Size: 14.3 MB (14348061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd430853bcf4c272a7aaacac94c5e64663ce7e03678889896b6d190f41d38848`  
		Last Modified: Thu, 18 Dec 2025 21:15:18 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e1a86c1f2b76a63c724d7332704693a3a00f911d4ae6fa916dbb44dd5e0f9a`  
		Last Modified: Thu, 18 Dec 2025 21:15:21 GMT  
		Size: 23.2 MB (23224075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c7ac338f28e822c09da11f757c362294adca9d24d4f953c05910f53ded2ded`  
		Last Modified: Thu, 18 Dec 2025 21:15:19 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be53be32a54f5be26129d16e768419c40dbb500b1177da9fab053b3e1bf9b24b`  
		Last Modified: Thu, 18 Dec 2025 21:15:19 GMT  
		Size: 19.9 KB (19851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-alpine3.22` - unknown; unknown

```console
$ docker pull php@sha256:bcbcf44e28d85226364e6e137c6797ca77f0219f664ad98524d7c97a42df6187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.3 KB (312314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf96a839531135b8c112fa4a8a3c318c337b12ea2d8a346850d34aa30b4d8a6e`

```dockerfile
```

-	Layers:
	-	`sha256:e0524702abd87e3d2a9443d5080c808ce17872fb8f3763ceeec259bd426bf834`  
		Last Modified: Fri, 19 Dec 2025 00:02:06 GMT  
		Size: 275.1 KB (275131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad660f0763eca28fa45999d0c13fd559555e891003d7162c38c224ee231ef836`  
		Last Modified: Fri, 19 Dec 2025 00:02:07 GMT  
		Size: 37.2 KB (37183 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull php@sha256:4507aefdcf4c1489eb0fb0e69fe584ae082945c7760fa71a61b6b763b37ca5ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49580087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bc29bd7ca43f348388c708f723b7b0304026016c91215117cc4d1098c995868`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 21:11:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 18 Dec 2025 21:11:42 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 18 Dec 2025 21:11:42 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 18 Dec 2025 21:11:42 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Dec 2025 21:11:42 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Dec 2025 21:11:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Dec 2025 21:11:42 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Dec 2025 21:11:42 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Dec 2025 21:11:42 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 18 Dec 2025 21:11:42 GMT
ENV PHP_VERSION=8.5.1
# Thu, 18 Dec 2025 21:11:42 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.1.tar.xz.asc
# Thu, 18 Dec 2025 21:11:42 GMT
ENV PHP_SHA256=3f5bf99ce81201f526d25e288eddb2cfa111d068950d1e9a869530054ff98815
# Thu, 18 Dec 2025 21:11:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 18 Dec 2025 21:11:46 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 21:15:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Dec 2025 21:15:34 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 21:15:35 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Dec 2025 21:15:35 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Dec 2025 21:15:35 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7796cc17157224b562c6b2cfd011b79085702fc89894a3c71487faf44fff3127`  
		Last Modified: Thu, 18 Dec 2025 21:15:51 GMT  
		Size: 3.5 MB (3467211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508cd29b2486cc209a0844c94473cae1a40f568d4d207e838e393f108fd95f20`  
		Last Modified: Thu, 18 Dec 2025 21:15:51 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7beaea010371738e7b89e3088e4276488b747197bf033e05089f11a3a34b211d`  
		Last Modified: Thu, 18 Dec 2025 21:15:51 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4beafa8f22e05d14908eb90b05d9829c2ba3e64297bdb14aa4168b4450ef51`  
		Last Modified: Thu, 18 Dec 2025 21:15:53 GMT  
		Size: 14.3 MB (14348062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61102664786cf13ecd360b391a09622bf42cd8740adda80113e1d49149bce1a1`  
		Last Modified: Thu, 18 Dec 2025 21:15:51 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723ec180b385946d0ec40d706b4a4b8531dbe9f0b9de0b789908892188c8ee30`  
		Last Modified: Thu, 18 Dec 2025 21:15:53 GMT  
		Size: 27.6 MB (27602792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0b653fa8c0607bb9c0f2531347e92dcdf033767387bb9941310a7c9c7805fe`  
		Last Modified: Thu, 18 Dec 2025 21:15:52 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a50f24f95633b20bed9121af6987912e70c56e97998b8545324e5bdf866efa3`  
		Last Modified: Thu, 18 Dec 2025 21:15:52 GMT  
		Size: 19.9 KB (19863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-alpine3.22` - unknown; unknown

```console
$ docker pull php@sha256:841f3ff91c5c81097f92f82d6c4c1d2067a6608f8826dccc25c252c89fff6a1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.4 KB (312369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5fd7392256e66af8a74b5dc48a7a8ffaf73e5ef24e2df1bc323f9c2c459f554`

```dockerfile
```

-	Layers:
	-	`sha256:0a25edeff68e4ff96ce66e0115d1c13ae44db0f0ec2f991d3538979e07556d39`  
		Last Modified: Fri, 19 Dec 2025 00:02:10 GMT  
		Size: 275.2 KB (275151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:997cd860d1cd51f8f25762dced11de5e6a6ce39e8796b59707a206a38c2f9f15`  
		Last Modified: Fri, 19 Dec 2025 00:02:11 GMT  
		Size: 37.2 KB (37218 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts-alpine3.22` - linux; 386

```console
$ docker pull php@sha256:80861d6a59ccadf4f1bfb001982f72c05f419c97655f6c753f1ca4a5dfa94dbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50486943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ca0862c2841cd6de33c4f21ca2d261f0bf9168ab42ff01c318f11bc8d9ad0e`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 21:16:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 18 Dec 2025 21:16:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 18 Dec 2025 21:16:43 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 18 Dec 2025 21:16:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Dec 2025 21:16:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Dec 2025 21:16:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Dec 2025 21:16:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Dec 2025 21:16:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Dec 2025 21:16:43 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 18 Dec 2025 21:16:43 GMT
ENV PHP_VERSION=8.5.1
# Thu, 18 Dec 2025 21:16:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.1.tar.xz.asc
# Thu, 18 Dec 2025 21:16:43 GMT
ENV PHP_SHA256=3f5bf99ce81201f526d25e288eddb2cfa111d068950d1e9a869530054ff98815
# Thu, 18 Dec 2025 21:16:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 18 Dec 2025 21:16:47 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 21:20:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Dec 2025 21:20:34 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 21:20:34 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Dec 2025 21:20:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Dec 2025 21:20:34 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Sun, 07 Dec 2025 14:06:47 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942880168beaa053dbcf6f74f31b32b7e166646d81d707b8c4ba8495c89ce8d3`  
		Last Modified: Thu, 18 Dec 2025 21:20:51 GMT  
		Size: 3.5 MB (3523262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b4990bdfe6601a887cb63df351ae80fd423a7facc7bfd4c8e444f65173d17d`  
		Last Modified: Thu, 18 Dec 2025 21:20:50 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335b41311440a232b8d20f2480e54be9f3c84280e60230940992821df1dfe11d`  
		Last Modified: Thu, 18 Dec 2025 21:20:51 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3980bf26afe62286b8c2c4344320deff4ea21e63af17aebbe9a1965c41de597e`  
		Last Modified: Thu, 18 Dec 2025 21:20:52 GMT  
		Size: 14.3 MB (14348039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5a7b56f385073db388ea58a2e5dccd40e4392e5e24d897a8a9ec8920669e35`  
		Last Modified: Thu, 18 Dec 2025 21:20:51 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74827c70a17a5738e23664ae891a6c7593fb61ee29e4120dd78e44abf90a17a5`  
		Last Modified: Thu, 18 Dec 2025 21:20:54 GMT  
		Size: 29.0 MB (28972573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d40dfa71ad68c2d0d45da86a051e0feb4254f671a20a9d1849fd73b8c6ccec7f`  
		Last Modified: Thu, 18 Dec 2025 21:20:51 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f75c1840442fce3bec6944e4d314a0e23e23d576ebaf1434b8369e8cb4dafbd6`  
		Last Modified: Thu, 18 Dec 2025 21:20:51 GMT  
		Size: 20.1 KB (20050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-alpine3.22` - unknown; unknown

```console
$ docker pull php@sha256:2c051c7cf0bc181b833a1576d7c6854a6d8194f3944208d4bbc1e1967335ea8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.1 KB (315058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70fa57cfae2268bc0277e0107f6c5ebf04164f099df1e55fd3873887374c5167`

```dockerfile
```

-	Layers:
	-	`sha256:2da06e36e7a40688bdf7d68f4c673663c67df814779d37f890e62038ebdae9bb`  
		Last Modified: Fri, 19 Dec 2025 00:02:15 GMT  
		Size: 278.1 KB (278060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90eded162553445aa31e2d1f60ba0d0b7c47421b375d7741edebd59a1f1ca3f3`  
		Last Modified: Fri, 19 Dec 2025 00:02:15 GMT  
		Size: 37.0 KB (36998 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts-alpine3.22` - linux; ppc64le

```console
$ docker pull php@sha256:2ef14c9e75e51f720fd4d4705aa49eb876d62e451ca48da0dac8f44f00331b76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50187715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc67f6452eed5892eb7d32ba2dc354a6f8ca63f6b99a7b9eef5e9f97dc2d0d55`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 09 Oct 2025 00:51:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 09 Oct 2025 00:51:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 09 Oct 2025 00:51:44 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 09 Oct 2025 00:51:44 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 09 Oct 2025 00:51:44 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 09 Oct 2025 00:51:44 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Oct 2025 00:51:44 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Oct 2025 00:51:44 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 09 Oct 2025 00:51:44 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 09 Oct 2025 00:51:44 GMT
ENV PHP_VERSION=8.5.1
# Thu, 09 Oct 2025 00:51:44 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.1.tar.xz.asc
# Thu, 09 Oct 2025 00:51:44 GMT
ENV PHP_SHA256=3f5bf99ce81201f526d25e288eddb2cfa111d068950d1e9a869530054ff98815
# Thu, 18 Dec 2025 21:37:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 18 Dec 2025 21:37:35 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 21:45:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Dec 2025 21:45:39 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 21:45:43 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Dec 2025 21:45:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Dec 2025 21:45:43 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Sun, 07 Dec 2025 14:06:45 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95a0b03903475651b081c7c705a4ab0f68ab5f5bba328735e8dae6e168526c7`  
		Last Modified: Mon, 08 Dec 2025 02:09:34 GMT  
		Size: 3.6 MB (3614664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436cae3ea479232d2bcf67ca55e6705ab3775fa412e53331855937a2a7340b65`  
		Last Modified: Mon, 08 Dec 2025 02:09:34 GMT  
		Size: 937.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1164e359044b0e56f99538c30031735fcef9128820673f06e10663118d04d0e3`  
		Last Modified: Mon, 08 Dec 2025 02:09:34 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0166f3604b35a0cbd02a122fcf9fc130a40c0304ed94908f366c47eaaa1e7b`  
		Last Modified: Thu, 18 Dec 2025 21:41:50 GMT  
		Size: 14.3 MB (14348056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56ca78ecc22e30064d2e1da983b104828aceedba06f51991d350cf8c8fd69f4`  
		Last Modified: Thu, 18 Dec 2025 21:41:49 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ee42054f3329cec1eccfe0a50b763ca36e7fd4a1ddca90ed86ec52618de064`  
		Last Modified: Thu, 18 Dec 2025 21:46:15 GMT  
		Size: 28.5 MB (28468771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b8ff8cbc8e7e2174b0336ffef3168bd31c6aba36dc5f119907f33fc603f61cf`  
		Last Modified: Thu, 18 Dec 2025 21:46:12 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ff1340d49a489550c0b4429778c5e3068db3c3bb0529fd40a0f9b9c19ae30a6`  
		Last Modified: Thu, 18 Dec 2025 21:46:12 GMT  
		Size: 19.9 KB (19882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-alpine3.22` - unknown; unknown

```console
$ docker pull php@sha256:c1d5475c1e967b9176f884deb8d2fd5a8e357491ac6da5fac839aa28f3f93b3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.3 KB (309321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2af896342d9dc73d40e94b49ee4985af2f1259d578cee2f1e41736ba17f5a1a4`

```dockerfile
```

-	Layers:
	-	`sha256:d66f2490b35ea44efde00a9094022b8e8e392014a5ba313b50709d7e9868331f`  
		Last Modified: Fri, 19 Dec 2025 00:02:19 GMT  
		Size: 273.2 KB (273178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0eecc1beb9b3df3a6862085f369621cfcfd331dd0f867c55595dadcd74f2e5c4`  
		Last Modified: Fri, 19 Dec 2025 00:02:19 GMT  
		Size: 36.1 KB (36143 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts-alpine3.22` - linux; riscv64

```console
$ docker pull php@sha256:34f12a63ba040473a44068ef5278e4c3faa62771d035ded59ff47b75e9470632
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47960571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76559238d6cfb194e8c1e97837b6b95127285a5a155c27da14bdfaeb51a834bb`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 09 Oct 2025 05:22:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 09 Oct 2025 05:22:42 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 09 Oct 2025 05:22:42 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 09 Oct 2025 05:22:42 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 09 Oct 2025 05:22:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 09 Oct 2025 05:22:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Oct 2025 05:22:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Oct 2025 05:22:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 09 Oct 2025 05:22:43 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 09 Oct 2025 05:22:43 GMT
ENV PHP_VERSION=8.5.1
# Thu, 09 Oct 2025 05:22:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.1.tar.xz.asc
# Thu, 09 Oct 2025 05:22:43 GMT
ENV PHP_SHA256=3f5bf99ce81201f526d25e288eddb2cfa111d068950d1e9a869530054ff98815
# Sat, 20 Dec 2025 03:39:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Sat, 20 Dec 2025 03:39:02 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 20 Dec 2025 06:12:41 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 20 Dec 2025 06:12:41 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 20 Dec 2025 06:12:47 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 20 Dec 2025 06:12:47 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 20 Dec 2025 06:12:47 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Sun, 07 Dec 2025 22:49:04 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58e9f10e445dbf7ba866462dd44d0f912a09342dc97a4685769a2d057bcc7a9`  
		Last Modified: Tue, 09 Dec 2025 02:08:24 GMT  
		Size: 3.6 MB (3600269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2579c35b4a5055268b9ccb82f8c3307c0a781af77168952679399ed4bde3b60a`  
		Last Modified: Tue, 09 Dec 2025 02:08:23 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b6a920874b5f6759a41702af348a1eefb32a0674eeae4cd9d750418594caed`  
		Last Modified: Tue, 09 Dec 2025 02:08:23 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d9ce714eb8978d7346dfc729904c1af0b19a71bd79ae087c29706bd12097db`  
		Last Modified: Sat, 20 Dec 2025 04:40:18 GMT  
		Size: 14.3 MB (14348025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ef97b571630878d7c239a7037b53856f5daf10c5732ce6cc7a25bf06ab22e1`  
		Last Modified: Sat, 20 Dec 2025 04:40:17 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c085c4a224ed137affdd0fb948b00ac35bba1c1529f109c0a6e7a8276c1c0d0`  
		Last Modified: Sat, 20 Dec 2025 06:14:17 GMT  
		Size: 26.5 MB (26473081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46d1b502a766bbeef354b768954bb6444bda5919d6bffa057a2dee32937e02f`  
		Last Modified: Sat, 20 Dec 2025 06:14:14 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbbddb81c521814a9b58e1188da47762647c68ac0f8cdc7da7d23fbc498b5224`  
		Last Modified: Sat, 20 Dec 2025 06:14:14 GMT  
		Size: 19.9 KB (19861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-alpine3.22` - unknown; unknown

```console
$ docker pull php@sha256:f20d081abd81268e35c291d0aa70a15b9b8df0a64c1866804bd069b07dc40dba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.3 KB (310266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31eb16b5225479cdca4052209e197290bcaf554540987e199b0c2cb97a01eba9`

```dockerfile
```

-	Layers:
	-	`sha256:2a28307d56e6c7e5c0513c6f79a6ce93c59bad343f4728e86bab6e966443ab2c`  
		Last Modified: Sat, 20 Dec 2025 08:54:58 GMT  
		Size: 273.2 KB (273174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bff2dda2bd5a1847370fd919bbf81406b417cc6f2c125375c4f7534af1ee1c87`  
		Last Modified: Sat, 20 Dec 2025 08:54:59 GMT  
		Size: 37.1 KB (37092 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts-alpine3.22` - linux; s390x

```console
$ docker pull php@sha256:341174b73cc7363ea01a699c7dde66866360c66f800754451ab65987e589787a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49120524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19e637d83488aaa2a8759d41e1350a84c0fe2f22e09941114e0d07122de76e7f`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 20 Nov 2025 20:07:46 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Nov 2025 20:07:46 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 18 Dec 2025 21:25:45 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 18 Dec 2025 21:25:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Dec 2025 21:25:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Dec 2025 21:25:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Dec 2025 21:25:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Dec 2025 21:25:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Dec 2025 21:25:45 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 18 Dec 2025 21:25:45 GMT
ENV PHP_VERSION=8.5.1
# Thu, 18 Dec 2025 21:25:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.1.tar.xz.asc
# Thu, 18 Dec 2025 21:25:45 GMT
ENV PHP_SHA256=3f5bf99ce81201f526d25e288eddb2cfa111d068950d1e9a869530054ff98815
# Thu, 18 Dec 2025 21:25:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 18 Dec 2025 21:25:48 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 21:30:47 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 						--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Dec 2025 21:30:47 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 21:30:48 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Dec 2025 21:30:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Dec 2025 21:30:48 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Sun, 07 Dec 2025 14:06:46 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd4b2ff0842c178e1087be78ce7fd9398e218ab3073b14df552c39751910aff3`  
		Last Modified: Thu, 20 Nov 2025 20:25:24 GMT  
		Size: 3.7 MB (3692751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98970dae6ec226fa5b2211ea3ccd1469feab0f7fe3b6e39ee7636d46eda3ec13`  
		Last Modified: Thu, 18 Dec 2025 21:31:04 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ce81fd762306676d63e4ae5519fafe546496c1de85dfad336d2b374a174305`  
		Last Modified: Thu, 18 Dec 2025 21:31:02 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a4f9cead7e2aeaf3a4e035854ab5f61d819adf9901e61a34b28967aa544199`  
		Last Modified: Thu, 18 Dec 2025 21:31:03 GMT  
		Size: 14.3 MB (14348070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fae3a4a9f028fe7f58a1fa08eddab16bb1bd3f802854e7f74bdac583733171b`  
		Last Modified: Thu, 18 Dec 2025 21:31:03 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b8bcd8c28b98df62e976ebb434658e9e4ccc81eeb27f1ca8dff4fb857ec2bb`  
		Last Modified: Thu, 18 Dec 2025 21:31:08 GMT  
		Size: 27.4 MB (27406474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d20b3f914b35051544711b9f2c64d3a9047a9105d9f70d7b307f3566d179638`  
		Last Modified: Thu, 18 Dec 2025 21:31:06 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aff30dbe45456f47d8525443aeb542d65f771142f49d1eafe687c9beb2a69ea`  
		Last Modified: Thu, 18 Dec 2025 21:31:06 GMT  
		Size: 19.9 KB (19884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-alpine3.22` - unknown; unknown

```console
$ docker pull php@sha256:89141bab96397c070f07b7b20e8f0036e5aa3c92278cdb9da7971e7b12528774
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.2 KB (310184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9e69a70781aeaa16beda7e7c80b3c513d9370913c662322dde792d2cf8a96f7`

```dockerfile
```

-	Layers:
	-	`sha256:8ee1e77ce37a103765e26e780c28a9467e49ad371b6d092c7b6933e4592f155b`  
		Last Modified: Fri, 19 Dec 2025 00:02:29 GMT  
		Size: 273.1 KB (273144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95478844c884aa282bcd5b4e7bf27fd8cbb90137ea3943afc1c017c0371ed711`  
		Last Modified: Fri, 19 Dec 2025 00:02:30 GMT  
		Size: 37.0 KB (37040 bytes)  
		MIME: application/vnd.in-toto+json
