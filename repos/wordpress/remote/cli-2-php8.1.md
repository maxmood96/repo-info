## `wordpress:cli-2-php8.1`

```console
$ docker pull wordpress@sha256:64dccddf9400f89758934b0f3ce2f3129e56f6bb6ed9a61be488502d3e0e90ce
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

### `wordpress:cli-2-php8.1` - linux; amd64

```console
$ docker pull wordpress@sha256:b7fb15ac0679f3113cf831f4edb9d000cacd08e6246f2ee1ff023ed56647ac1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61688819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4254545ccc792295fed0aebf758cfe4d63b40cc98eb9ba62914690ba5347912b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Thu, 31 Jul 2025 19:22:09 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
CMD ["/bin/sh"]
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 31 Jul 2025 19:22:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 31 Jul 2025 19:22:09 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_VERSION=8.1.33
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.33.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.33.tar.xz.asc
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_SHA256=9db83bf4590375562bc1a10b353cccbcf9fcfc56c58b7c8fb814e6865bb928d1
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		patch 		patchutils 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	curl -fL 'https://github.com/php/php-src/commit/577b8ae4226368e66fee7a9b5c58f9e2428372fc.patch?full_index=1' -o 11678.patch; 	echo '6edc20c3bb3e7cc13515abce7f2fffa8ebea6cf7469abfbc78fcdc120350b239 *11678.patch' | sha256sum -c -; 	patch -p1 < 11678.patch; 	rm 11678.patch; 	curl -fL 'https://github.com/php/php-src/commit/67259e451d5d58b4842776c5696a66d74e157609.patch?full_index=1' -o 14834.patch; 	echo 'ed10a1b254091ad676ed204e55628ecbd6c8962004d6185a1821cedecd526c0f *14834.patch' | sha256sum -c -; 	filterdiff -x '*/NEWS' 14834.patch | patch -p1; 	rm 14834.patch; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 31 Jul 2025 19:22:09 GMT
CMD ["php" "-a"]
# Tue, 02 Dec 2025 01:14:17 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Tue, 02 Dec 2025 01:14:17 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Tue, 02 Dec 2025 01:14:17 GMT
WORKDIR /var/www/html
# Tue, 02 Dec 2025 01:15:04 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 01:15:04 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 01:15:07 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Tue, 02 Dec 2025 01:15:07 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Tue, 02 Dec 2025 01:15:07 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Tue, 02 Dec 2025 01:15:07 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Tue, 02 Dec 2025 01:15:07 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 01:15:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:15:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:15:07 GMT
USER www-data
# Tue, 02 Dec 2025 01:15:07 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Sun, 07 Dec 2025 13:55:07 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b9d8fa4ac8c0b818a31c78d7b16a64544669548afb39f6c70970e61559802fe`  
		Last Modified: Sun, 07 Dec 2025 23:56:00 GMT  
		Size: 3.4 MB (3367265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daeb153cd27a12fa4fdf9516242937e5e4b11461f61dc7399872e041b4357b0f`  
		Last Modified: Mon, 08 Dec 2025 00:03:16 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b4bfc408f0a7759b504dff97ace4757333f7eee6ccd2af91d73f6b42f09a265`  
		Last Modified: Mon, 08 Dec 2025 00:03:16 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266d22c9fc5b04a2d1fd27008b342cf78423cc28329e11a7732a0d4b9d003fe2`  
		Last Modified: Mon, 08 Dec 2025 00:03:17 GMT  
		Size: 11.9 MB (11920001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf3bfb407eab00d208a9f72bc6520790b61e0e3db535e52e20bba771ccbc43a`  
		Last Modified: Mon, 08 Dec 2025 00:03:17 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a15ce21c3f7c4faa079f0ebc12f7ecec938ff08c856d96269c2d9d67485f3d0`  
		Last Modified: Mon, 08 Dec 2025 00:03:18 GMT  
		Size: 16.7 MB (16665730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592563f25f790217260ec2f2f194d79c12f2ac691da768f3dbc29187f974fdca`  
		Last Modified: Mon, 08 Dec 2025 00:03:17 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f596b0daf39ff274a600131a5101dad41e2608d4b7d2e5ae6c6ba79f27270778`  
		Last Modified: Mon, 08 Dec 2025 00:03:18 GMT  
		Size: 20.0 KB (19964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b659e622f9bf72a4c71a65d37754c670f001101154f1a8c1414e3c7b8367e8`  
		Last Modified: Mon, 08 Dec 2025 00:03:18 GMT  
		Size: 20.0 KB (19962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e5e114f170c560f78efa2569fb99d431657a092a52a5c7ef0ba3cbcaf11a33`  
		Last Modified: Tue, 02 Dec 2025 01:15:36 GMT  
		Size: 11.1 MB (11075626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf593108993cec949f08ed1d14006634c6773e5a9d806455b46a801f2f411865`  
		Last Modified: Tue, 02 Dec 2025 01:15:37 GMT  
		Size: 13.4 MB (13448158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e881258582e8b264c270a1157a2da15e3884f3708554defc7d8c7f24af0cda04`  
		Last Modified: Tue, 02 Dec 2025 01:15:34 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d24a8fd226964f5c1d3dbd20fed4ddbf9f908e696fa4e0d44046aaf0b90ae9`  
		Last Modified: Tue, 02 Dec 2025 02:39:14 GMT  
		Size: 1.5 MB (1524599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17aa44d796a548094aac8ef30cb0dde4b496cdeabe40be4442ed421241df04a8`  
		Last Modified: Tue, 02 Dec 2025 02:39:13 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2-php8.1` - unknown; unknown

```console
$ docker pull wordpress@sha256:2365986485c3a21950091caf3a894a64fee644cfb18e24776ab8dc1a4348f396
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.3 KB (636265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8f8dd8031dd9d2c91c9e4503119f14196fba69926ed8db699fa2e9c7ac3de50`

```dockerfile
```

-	Layers:
	-	`sha256:cf243f31c5b4b06dee3bf3d79b029c71591de063fbaaaec5c6b7190cf9f66639`  
		Last Modified: Tue, 02 Dec 2025 02:33:52 GMT  
		Size: 594.2 KB (594163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d010c60b6b64cb08ae19b7db79de524ce5ec87a6906b8c6d9325b2148224c1fd`  
		Last Modified: Tue, 02 Dec 2025 02:33:53 GMT  
		Size: 42.1 KB (42102 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2-php8.1` - linux; arm variant v6

```console
$ docker pull wordpress@sha256:5845f1fbcf9bed607d5e48affe6817a73c706297ba6e986dcd1018a562f949e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.0 MB (56995657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf42ce8a66f92f7ec08d566a77a598483d30781d436c6ff241d9c7daccbbd606`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Thu, 31 Jul 2025 19:22:09 GMT
ADD alpine-minirootfs-3.21.5-armhf.tar.gz / # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
CMD ["/bin/sh"]
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 31 Jul 2025 19:22:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 31 Jul 2025 19:22:09 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_VERSION=8.1.33
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.33.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.33.tar.xz.asc
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_SHA256=9db83bf4590375562bc1a10b353cccbcf9fcfc56c58b7c8fb814e6865bb928d1
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		patch 		patchutils 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	curl -fL 'https://github.com/php/php-src/commit/577b8ae4226368e66fee7a9b5c58f9e2428372fc.patch?full_index=1' -o 11678.patch; 	echo '6edc20c3bb3e7cc13515abce7f2fffa8ebea6cf7469abfbc78fcdc120350b239 *11678.patch' | sha256sum -c -; 	patch -p1 < 11678.patch; 	rm 11678.patch; 	curl -fL 'https://github.com/php/php-src/commit/67259e451d5d58b4842776c5696a66d74e157609.patch?full_index=1' -o 14834.patch; 	echo 'ed10a1b254091ad676ed204e55628ecbd6c8962004d6185a1821cedecd526c0f *14834.patch' | sha256sum -c -; 	filterdiff -x '*/NEWS' 14834.patch | patch -p1; 	rm 14834.patch; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 31 Jul 2025 19:22:09 GMT
CMD ["php" "-a"]
# Tue, 02 Dec 2025 01:10:28 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Tue, 02 Dec 2025 01:10:28 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Tue, 02 Dec 2025 01:10:28 GMT
WORKDIR /var/www/html
# Tue, 02 Dec 2025 01:11:24 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 01:11:24 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 01:11:26 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Tue, 02 Dec 2025 01:11:26 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Tue, 02 Dec 2025 01:11:26 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Tue, 02 Dec 2025 01:11:26 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Tue, 02 Dec 2025 01:11:26 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 01:11:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:11:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:11:26 GMT
USER www-data
# Tue, 02 Dec 2025 01:11:26 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:f8b30cbd0fab9e5a803578a09c973d18d7450816d914e63e04e5c2edd79f8bee`  
		Last Modified: Mon, 08 Dec 2025 00:04:31 GMT  
		Size: 3.4 MB (3365468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c52efc7d7ed2bd0ff60fcd59d778526300cbd33f189b6959021904cdcc9f540`  
		Last Modified: Wed, 08 Oct 2025 21:47:31 GMT  
		Size: 3.3 MB (3337157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:facba1823e9fae4ad9f937b57a6a4721e40976b0387fbf8c6343893251f1c442`  
		Last Modified: Mon, 08 Dec 2025 05:06:37 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1612e618cc20dd6e4c8f5b3e6728067e09a81bdcde7830d39015594632eeb4c9`  
		Last Modified: Mon, 08 Dec 2025 05:06:41 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc694e267014e5409a95552ea236d013a85971dac05fef0805a189ffae8df13`  
		Last Modified: Mon, 08 Dec 2025 05:06:40 GMT  
		Size: 11.9 MB (11920007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37ddefaffe56995b734b61c30a822a06f3d496ed8605851e9c3e6daf2b962fc`  
		Last Modified: Mon, 08 Dec 2025 05:06:37 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:854b230d876238c5baa7b35a72c9bc17a94fbc3d335dfd4c08721c8344d63c31`  
		Last Modified: Mon, 08 Dec 2025 05:06:39 GMT  
		Size: 15.1 MB (15058256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1575dfb0a532a60dd9333d9f0eee5e302c2fabea410f7a3d31fd1e359b03165b`  
		Last Modified: Mon, 08 Dec 2025 05:06:37 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07fd952e7e95be27be6c19a933603561722fa1fc1613a4607e0b60db18c1614`  
		Last Modified: Mon, 08 Dec 2025 05:06:38 GMT  
		Size: 19.8 KB (19783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25bed5de27cdaf38aa546069ed4fc1773abc046f86f1210eed042d5dd0d6b25`  
		Last Modified: Mon, 08 Dec 2025 05:06:38 GMT  
		Size: 19.8 KB (19778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb74d303f872e5290359c33a1535bc84a6ea91f6733373f17d6f6394ab0e0751`  
		Last Modified: Tue, 02 Dec 2025 01:11:57 GMT  
		Size: 10.8 MB (10760604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a638845860b70362b11bceea74653cd8ef2d019044d5249c2511d8a828da995c`  
		Last Modified: Tue, 02 Dec 2025 01:11:57 GMT  
		Size: 11.0 MB (10985074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:256b501e7492f7fe7afe411282fb6446d9a44d0ace59f6b05b91b80e4bb1adca`  
		Last Modified: Tue, 02 Dec 2025 01:11:56 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6faae0924713d26690eb3473aebfa8e751e9638049579a616208ac327ed5237`  
		Last Modified: Tue, 02 Dec 2025 01:11:57 GMT  
		Size: 1.5 MB (1524580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b39056c6a1a6af3f463703e56229205db3c3c3b4b1c13162fcd49f7799ebd49b`  
		Last Modified: Tue, 02 Dec 2025 01:11:57 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2-php8.1` - unknown; unknown

```console
$ docker pull wordpress@sha256:2cb1091c73fa99bbb61a0e4748bfd507738ca8f54889cf87d77968404a177172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 KB (42019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c0faafad291fd1cb9169e47a83d178a6e3e7a0e29512119efb3798b541a03e`

```dockerfile
```

-	Layers:
	-	`sha256:10e02992f56a901143ed8c967efcb75579f445035e14ac3f22cdf1ac6a276176`  
		Last Modified: Tue, 02 Dec 2025 02:33:56 GMT  
		Size: 42.0 KB (42019 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2-php8.1` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:99fa6c10468b87b3d49632068ed27f293d54db6722d853f1c32b93baa82e1a53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.3 MB (56290727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:238bc78fd1bfb325ef8e826ede03c3e2e2a63f5221447536cc4a9727c09055fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Thu, 31 Jul 2025 19:22:09 GMT
ADD alpine-minirootfs-3.21.5-armv7.tar.gz / # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
CMD ["/bin/sh"]
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 31 Jul 2025 19:22:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 31 Jul 2025 19:22:09 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_VERSION=8.1.33
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.33.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.33.tar.xz.asc
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_SHA256=9db83bf4590375562bc1a10b353cccbcf9fcfc56c58b7c8fb814e6865bb928d1
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		patch 		patchutils 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	curl -fL 'https://github.com/php/php-src/commit/577b8ae4226368e66fee7a9b5c58f9e2428372fc.patch?full_index=1' -o 11678.patch; 	echo '6edc20c3bb3e7cc13515abce7f2fffa8ebea6cf7469abfbc78fcdc120350b239 *11678.patch' | sha256sum -c -; 	patch -p1 < 11678.patch; 	rm 11678.patch; 	curl -fL 'https://github.com/php/php-src/commit/67259e451d5d58b4842776c5696a66d74e157609.patch?full_index=1' -o 14834.patch; 	echo 'ed10a1b254091ad676ed204e55628ecbd6c8962004d6185a1821cedecd526c0f *14834.patch' | sha256sum -c -; 	filterdiff -x '*/NEWS' 14834.patch | patch -p1; 	rm 14834.patch; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 31 Jul 2025 19:22:09 GMT
CMD ["php" "-a"]
# Tue, 02 Dec 2025 01:15:01 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Tue, 02 Dec 2025 01:15:02 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Tue, 02 Dec 2025 01:15:02 GMT
WORKDIR /var/www/html
# Tue, 02 Dec 2025 01:15:55 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 01:15:55 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 01:15:59 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Tue, 02 Dec 2025 01:15:59 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Tue, 02 Dec 2025 01:15:59 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Tue, 02 Dec 2025 01:15:59 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Tue, 02 Dec 2025 01:15:59 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 01:15:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:15:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:15:59 GMT
USER www-data
# Tue, 02 Dec 2025 01:15:59 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:520d06ecc3ba4ec2920319fa6f2cc6bea9a9c1d5a43808c1d2388522c37d7b30`  
		Last Modified: Sun, 07 Dec 2025 17:58:54 GMT  
		Size: 3.1 MB (3098611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0771e5e68b41c6ddae89913d7aa6608431acd9cde7b6b80655def9d99e8a330d`  
		Last Modified: Mon, 08 Dec 2025 05:06:34 GMT  
		Size: 3.1 MB (3143462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef14973a50223aad327ae9a2e38561b6eb9dff38c3088aa38a494d3ea44d9ff`  
		Last Modified: Mon, 08 Dec 2025 05:06:34 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c38798dfc0f1ba9d8105b6fa523808973e408fa3dd8c96ecf5aedff10c89ab`  
		Last Modified: Mon, 08 Dec 2025 05:06:34 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda3710af0a944c33fefdeb4c863eee8f418b5c98c37ed71927b87b00a68ecb3`  
		Last Modified: Mon, 08 Dec 2025 05:06:35 GMT  
		Size: 11.9 MB (11920000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ae757666f8e4df1183f71918450a431be75714680c82d2f20406d5e3642baa`  
		Last Modified: Mon, 08 Dec 2025 05:06:34 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd2c8ed3b3aca5ae62d65d5fc656578e52039f70245fb3dda1eae4bffdc9140`  
		Last Modified: Mon, 08 Dec 2025 05:06:35 GMT  
		Size: 14.2 MB (14162332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:505241c6bde52485b503b91cecf5042c0663eaf1b387009cfa9093c2d46ab816`  
		Last Modified: Mon, 08 Dec 2025 05:06:34 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e4fa4c894b99b4774e68ca668ca04cf851b7a565069327102f3e045969cf43`  
		Last Modified: Mon, 08 Dec 2025 05:06:35 GMT  
		Size: 19.8 KB (19783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df4df2aa21ebcc4f16e41989097b08e8fb00645cb9a0846a702103f5458c4495`  
		Last Modified: Mon, 08 Dec 2025 05:06:35 GMT  
		Size: 19.8 KB (19774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d66cf8d39ac91691a4d16132172785f29d10be9165fa71ea6b62bf0cab96b8`  
		Last Modified: Tue, 02 Dec 2025 01:16:33 GMT  
		Size: 10.4 MB (10437290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c06b96061ced5cb7a511bb7c50e08258018893b8b01e3c3516267790e5fd436e`  
		Last Modified: Tue, 02 Dec 2025 01:16:33 GMT  
		Size: 12.0 MB (11959948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c4b40d92a2eb523243ab42c65bd7d9f50bb80d7fc8c370eec6ea0acf8d2ebed`  
		Last Modified: Tue, 02 Dec 2025 01:16:32 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc344e4de0131cc79e4a3b040512650ddb700b2c8da168389f7af85ef7e150c`  
		Last Modified: Tue, 02 Dec 2025 01:16:32 GMT  
		Size: 1.5 MB (1524574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5375e0e42cdfade4ea6f5d1f4461ed785e5ffc3343243ff41f670ad8b8c19c06`  
		Last Modified: Tue, 02 Dec 2025 01:16:32 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2-php8.1` - unknown; unknown

```console
$ docker pull wordpress@sha256:ef03a6cbec8a12a5f5636c4287256a07aa30241d5e3de5356fc7b50232dd5ab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **635.2 KB (635189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a548eb50ab5c563d9eb4ce35fd2d20dea2f532e571fb4cc741f82ef83b4d2ef2`

```dockerfile
```

-	Layers:
	-	`sha256:e522f22aa2ef045607a2fa0a2f6e5dd02b3129a4121f41808ec5ec4af36be7bd`  
		Last Modified: Tue, 02 Dec 2025 02:34:00 GMT  
		Size: 593.0 KB (592955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66d83dc0bf9fef231de7573123da8f525ad86ff9eed8af92461a2a1a0a5d84ea`  
		Last Modified: Tue, 02 Dec 2025 02:34:00 GMT  
		Size: 42.2 KB (42234 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2-php8.1` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:c059b81257e216a28b8211bb2903945aaf865da50f35e19ddb3797a055d62a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (62007178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e7f869d2cb16307abaff99962f45f1399e7bb48bbbf7debc44732fdb86dca40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Thu, 31 Jul 2025 19:22:09 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
CMD ["/bin/sh"]
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 31 Jul 2025 19:22:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 31 Jul 2025 19:22:09 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_VERSION=8.1.33
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.33.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.33.tar.xz.asc
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_SHA256=9db83bf4590375562bc1a10b353cccbcf9fcfc56c58b7c8fb814e6865bb928d1
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		patch 		patchutils 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	curl -fL 'https://github.com/php/php-src/commit/577b8ae4226368e66fee7a9b5c58f9e2428372fc.patch?full_index=1' -o 11678.patch; 	echo '6edc20c3bb3e7cc13515abce7f2fffa8ebea6cf7469abfbc78fcdc120350b239 *11678.patch' | sha256sum -c -; 	patch -p1 < 11678.patch; 	rm 11678.patch; 	curl -fL 'https://github.com/php/php-src/commit/67259e451d5d58b4842776c5696a66d74e157609.patch?full_index=1' -o 14834.patch; 	echo 'ed10a1b254091ad676ed204e55628ecbd6c8962004d6185a1821cedecd526c0f *14834.patch' | sha256sum -c -; 	filterdiff -x '*/NEWS' 14834.patch | patch -p1; 	rm 14834.patch; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 31 Jul 2025 19:22:09 GMT
CMD ["php" "-a"]
# Tue, 02 Dec 2025 02:14:44 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Tue, 02 Dec 2025 02:14:45 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Tue, 02 Dec 2025 02:14:45 GMT
WORKDIR /var/www/html
# Tue, 02 Dec 2025 02:15:36 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 02:15:36 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 02:15:38 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Tue, 02 Dec 2025 02:15:38 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Tue, 02 Dec 2025 02:15:38 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Tue, 02 Dec 2025 02:15:38 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Tue, 02 Dec 2025 02:15:38 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 02:15:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 02:15:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 02:15:38 GMT
USER www-data
# Tue, 02 Dec 2025 02:15:38 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Sun, 07 Dec 2025 17:54:48 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3bf6c105049010ed34a53a48fb51cd5dcb63ba57593ae2ecbb4c6440bb3754`  
		Last Modified: Mon, 08 Dec 2025 00:30:53 GMT  
		Size: 3.4 MB (3361524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6938590912584394a280085d149aaa0dd2197d11934473d11c302e3b53656bd6`  
		Last Modified: Mon, 08 Dec 2025 00:30:52 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6885a1c1694d840f91ffa6469d547a547c4f09e5aac037f12be0879dee2ea27d`  
		Last Modified: Mon, 08 Dec 2025 00:30:51 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba188d917c2bc197271520a381a7b3773200dc37e26959a8efacc75e96cfe960`  
		Last Modified: Mon, 08 Dec 2025 00:30:55 GMT  
		Size: 11.9 MB (11920012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da06a92f71b95c42db4170aa46505734009fac6a83ebb4d3c5b06c0fbeb3dbb0`  
		Last Modified: Mon, 08 Dec 2025 00:31:00 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60430927436f47745311927fbe368a3d48acab72b96dd30c084a9a4779b7044c`  
		Last Modified: Mon, 08 Dec 2025 00:30:56 GMT  
		Size: 16.6 MB (16574117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ff31c6fec6f09e164b77eec71581e6dbdcfcb937f19b57a59d8deb8d01568c`  
		Last Modified: Mon, 08 Dec 2025 00:30:55 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9609d51d3cca4ad97e201098947d492b277f9004c6f652804d712ef36d2368`  
		Last Modified: Mon, 08 Dec 2025 00:30:56 GMT  
		Size: 19.8 KB (19787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72fa8af09ee44c776b49e0214d9d1ad8c129d3639040d929fc9e60b1cf38d981`  
		Last Modified: Mon, 08 Dec 2025 00:30:57 GMT  
		Size: 19.8 KB (19784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63abcd8bde6345d3a37182544a4ee6ba88a904b2dc3031e517c5a59c82bd9721`  
		Last Modified: Tue, 02 Dec 2025 02:15:53 GMT  
		Size: 11.1 MB (11083893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef8c8266a17e8e97d6c5948d9faff808a47a1a25c20cfd5cb1667ac6edcc9610`  
		Last Modified: Tue, 02 Dec 2025 02:15:53 GMT  
		Size: 13.5 MB (13506200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d09782ebe3a0b16a49077def5967f25652f156a98a9d7a2301bbea89f86e6be`  
		Last Modified: Tue, 02 Dec 2025 02:15:52 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b17964fc1b61325cbf1a707af8bad649070950ed13c4a62e4ad67760da3537`  
		Last Modified: Tue, 02 Dec 2025 02:15:52 GMT  
		Size: 1.5 MB (1524564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b19f57905d6558bc411edd3d1752db2348cac2d6cc3ace5c03932cd1d127051`  
		Last Modified: Tue, 02 Dec 2025 02:15:52 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2-php8.1` - unknown; unknown

```console
$ docker pull wordpress@sha256:8c276c8a67b791eafc44ac95b4043bcfd780203bcceae7bd46fa881500b8b37b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **635.2 KB (635241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:916ddc1f19825f860ce11351b022f2a85d4a292d684cc28357367190779af391`

```dockerfile
```

-	Layers:
	-	`sha256:0383122c845ac2ff0f6ff78053f28d1030ce029054380aed5442f1fbbf32d0af`  
		Last Modified: Tue, 02 Dec 2025 05:27:57 GMT  
		Size: 593.0 KB (592975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:835e85fe9a6e7802ed35b6f8d1b0e47bdbe2c7a0a15a990f89a220965af338e7`  
		Last Modified: Tue, 02 Dec 2025 05:27:57 GMT  
		Size: 42.3 KB (42266 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2-php8.1` - linux; 386

```console
$ docker pull wordpress@sha256:9cfff6440af728ed13545822947e187b4c1b3bab45743c3c6720921dd3324980
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.0 MB (61047602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ddf198ccee187f78bd2c30f5e25af5994be5585a59955d68c785b3d17e6f99c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Thu, 31 Jul 2025 19:22:09 GMT
ADD alpine-minirootfs-3.21.5-x86.tar.gz / # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
CMD ["/bin/sh"]
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 31 Jul 2025 19:22:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 31 Jul 2025 19:22:09 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_VERSION=8.1.33
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.33.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.33.tar.xz.asc
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_SHA256=9db83bf4590375562bc1a10b353cccbcf9fcfc56c58b7c8fb814e6865bb928d1
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		patch 		patchutils 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	curl -fL 'https://github.com/php/php-src/commit/577b8ae4226368e66fee7a9b5c58f9e2428372fc.patch?full_index=1' -o 11678.patch; 	echo '6edc20c3bb3e7cc13515abce7f2fffa8ebea6cf7469abfbc78fcdc120350b239 *11678.patch' | sha256sum -c -; 	patch -p1 < 11678.patch; 	rm 11678.patch; 	curl -fL 'https://github.com/php/php-src/commit/67259e451d5d58b4842776c5696a66d74e157609.patch?full_index=1' -o 14834.patch; 	echo 'ed10a1b254091ad676ed204e55628ecbd6c8962004d6185a1821cedecd526c0f *14834.patch' | sha256sum -c -; 	filterdiff -x '*/NEWS' 14834.patch | patch -p1; 	rm 14834.patch; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 31 Jul 2025 19:22:09 GMT
CMD ["php" "-a"]
# Tue, 02 Dec 2025 01:09:43 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Tue, 02 Dec 2025 01:09:44 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Tue, 02 Dec 2025 01:09:44 GMT
WORKDIR /var/www/html
# Tue, 02 Dec 2025 01:10:33 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 01:10:33 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 01:10:35 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Tue, 02 Dec 2025 01:10:35 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Tue, 02 Dec 2025 01:10:35 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Tue, 02 Dec 2025 01:10:35 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Tue, 02 Dec 2025 01:10:35 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 01:10:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:10:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:10:35 GMT
USER www-data
# Tue, 02 Dec 2025 01:10:35 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:bbedd1c05bb5090fc3fc2356be88d60b2a60937565b56e91fb4be42c5c73d485`  
		Last Modified: Sun, 07 Dec 2025 18:13:29 GMT  
		Size: 3.5 MB (3464704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa84ce5524a257d361bcfeffdf6024e9aa4318a6e71a53590ee441be96aef81`  
		Last Modified: Wed, 08 Oct 2025 21:32:54 GMT  
		Size: 3.4 MB (3411113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e713158703ba2b7ad001a7d8f546327a830e0ba5e1cc4fefa196b2541a6f5cf4`  
		Last Modified: Wed, 08 Oct 2025 21:32:54 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb66934db01c3939d06a87cdf98b58982568bde253cfe5432cf9d56c9169e28e`  
		Last Modified: Wed, 08 Oct 2025 21:32:54 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f7a44f58961141570548976f861e0820f758fe4e1bdbc8e3f8e33217cdfcd5`  
		Last Modified: Wed, 08 Oct 2025 21:35:54 GMT  
		Size: 11.9 MB (11920003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d383e5e410f25b9ec4a3b630c23163361c0e75c530ad635f259f4e2c8b066a1a`  
		Last Modified: Wed, 08 Oct 2025 21:35:53 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d938cae891fbae748d0bd24859f81216e327ac1c363e00bc351dd9d81e02b5`  
		Last Modified: Wed, 08 Oct 2025 21:35:54 GMT  
		Size: 17.1 MB (17077057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e57c4d2a4f3b107706180c3d6d681d3257bf8b119f130f2d1d30c3e3c87588`  
		Last Modified: Wed, 08 Oct 2025 21:35:53 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c93ad14d74a9c0e19db6cc4f0bbbab80a7120b981e035220c0d663fd30ac98c`  
		Last Modified: Wed, 08 Oct 2025 21:35:54 GMT  
		Size: 20.0 KB (19964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c67f7efecde999b429798f8ad98ebf70b270c0bb134a9af113f14ce841379a1f`  
		Last Modified: Wed, 08 Oct 2025 21:35:55 GMT  
		Size: 20.0 KB (19958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62799fb7ade44872f245928d872c544540a3a6054ed3b5569a047773e0fb695`  
		Last Modified: Tue, 02 Dec 2025 01:10:49 GMT  
		Size: 11.3 MB (11277234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0fe6a443ba729a569f6f77155663e609cace28e258a3a20d23089b497a1949d`  
		Last Modified: Tue, 02 Dec 2025 01:10:50 GMT  
		Size: 12.3 MB (12328072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7a713673c5f2fff538d7f3c6e2c5f4e5c954413e05c2cb2fc76207f91fe3a8`  
		Last Modified: Tue, 02 Dec 2025 01:10:48 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e61f6830eb4ddcb658244241809acc439343004cd4a2624b90e57acb524ea0`  
		Last Modified: Tue, 02 Dec 2025 01:11:00 GMT  
		Size: 1.5 MB (1524550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11df14683e7ed9ac7c35b796a3171d58d36ab3b8f006c1bde8bcacad066a974`  
		Last Modified: Tue, 02 Dec 2025 01:10:48 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2-php8.1` - unknown; unknown

```console
$ docker pull wordpress@sha256:9f76d7d0573548fa51b8896fdf6cfe06af68d0788f29c579deb4510dc9ffe922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.2 KB (636200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26fdb2e3600e47958727241e72a1697741ab8835d6f7958f42b6f1fa4f5441d8`

```dockerfile
```

-	Layers:
	-	`sha256:3a03d9d4b4ecc967a6ef4ac8c66ca7bd205916129119589df8f89023ae59ac08`  
		Last Modified: Tue, 02 Dec 2025 02:34:07 GMT  
		Size: 594.1 KB (594138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6ddb7bc78df81f457f3cb8476df79deab5cc781c5bfa59375567d6e8383e8eb`  
		Last Modified: Tue, 02 Dec 2025 02:34:08 GMT  
		Size: 42.1 KB (42062 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2-php8.1` - linux; ppc64le

```console
$ docker pull wordpress@sha256:a1c9e5a511f67885051572f4cf41a0cca4f6bab3c364b295ac46c3b4dcf80bd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.0 MB (62962111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a05dd2be55eb39002055d735fb6b9624698b4470e27134d564f171f4a970de89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Thu, 31 Jul 2025 19:22:09 GMT
ADD alpine-minirootfs-3.21.5-ppc64le.tar.gz / # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
CMD ["/bin/sh"]
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 31 Jul 2025 19:22:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 31 Jul 2025 19:22:09 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_VERSION=8.1.33
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.33.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.33.tar.xz.asc
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_SHA256=9db83bf4590375562bc1a10b353cccbcf9fcfc56c58b7c8fb814e6865bb928d1
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		patch 		patchutils 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	curl -fL 'https://github.com/php/php-src/commit/577b8ae4226368e66fee7a9b5c58f9e2428372fc.patch?full_index=1' -o 11678.patch; 	echo '6edc20c3bb3e7cc13515abce7f2fffa8ebea6cf7469abfbc78fcdc120350b239 *11678.patch' | sha256sum -c -; 	patch -p1 < 11678.patch; 	rm 11678.patch; 	curl -fL 'https://github.com/php/php-src/commit/67259e451d5d58b4842776c5696a66d74e157609.patch?full_index=1' -o 14834.patch; 	echo 'ed10a1b254091ad676ed204e55628ecbd6c8962004d6185a1821cedecd526c0f *14834.patch' | sha256sum -c -; 	filterdiff -x '*/NEWS' 14834.patch | patch -p1; 	rm 14834.patch; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 31 Jul 2025 19:22:09 GMT
CMD ["php" "-a"]
# Tue, 02 Dec 2025 02:13:54 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Tue, 02 Dec 2025 02:13:55 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Tue, 02 Dec 2025 02:13:55 GMT
WORKDIR /var/www/html
# Tue, 02 Dec 2025 02:15:18 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 02:15:18 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 02:15:24 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Tue, 02 Dec 2025 02:15:24 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Tue, 02 Dec 2025 02:15:24 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Tue, 02 Dec 2025 02:15:24 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Tue, 02 Dec 2025 02:15:24 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 02:15:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 02:15:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 02:15:25 GMT
USER www-data
# Tue, 02 Dec 2025 02:15:25 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:e99908f6ead74bb809123fe0d40505509ed6113949496be71629433c6ea3fa1a`  
		Last Modified: Sun, 07 Dec 2025 17:58:56 GMT  
		Size: 3.6 MB (3574075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05a34606c24896e36ea8bdfe146c7d0b83c28b1470998ac131a82d3cbf692f0`  
		Last Modified: Mon, 08 Dec 2025 02:35:28 GMT  
		Size: 3.5 MB (3513487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c41ef4ee60bf72c2b853908cfc0b6f6c5cc89255619d152b030b79cf281488f`  
		Last Modified: Mon, 08 Dec 2025 02:35:27 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a59e8dfa4a38d292b2272817a061750157530cfd7774765e1be1250c61c3e94`  
		Last Modified: Mon, 08 Dec 2025 02:35:28 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e71691fee2c0834667a010dbc6e219b02d1a19be89da8e36c4114559e3c73029`  
		Last Modified: Thu, 09 Oct 2025 02:38:25 GMT  
		Size: 11.9 MB (11919998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d05363ae150b20ba415c6fb84166f12c51c24ffda49dca00fc9861f5db79813`  
		Last Modified: Thu, 09 Oct 2025 02:38:25 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10973a3537badc87bf17b37cdb1274b04d5365717e3fc5cc585e999e1c681b4`  
		Last Modified: Thu, 09 Oct 2025 02:38:26 GMT  
		Size: 17.4 MB (17416487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba35c8b8cd2c4dadd9ae443e53ee7ea2e9ea8b4ddc01d6419e7251ca847812be`  
		Last Modified: Thu, 09 Oct 2025 02:38:25 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37015d9879a33caeee86932df4542b9ae57dda31a06befe18217ea8f54251bea`  
		Last Modified: Thu, 09 Oct 2025 02:38:26 GMT  
		Size: 19.8 KB (19783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543f07076dfb56590d59bee6a3c7913443f46faf4c7d71002760a7ac90591671`  
		Last Modified: Thu, 09 Oct 2025 02:38:26 GMT  
		Size: 19.8 KB (19781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b06aa2565d48baeace9da8f801e510bac5ee66acffcc892dea15d6a2fa9211`  
		Last Modified: Tue, 02 Dec 2025 02:15:58 GMT  
		Size: 11.7 MB (11685043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b8a39e09e2962aec4b6dd5fde2b2bdd9224a5cd5e8412fda9394c1f870a121`  
		Last Modified: Tue, 02 Dec 2025 02:16:00 GMT  
		Size: 13.3 MB (13283907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b572ddf2c6734e80145207e7a54fbc9c0498a2919e1e1cddb0b615bd9792de`  
		Last Modified: Tue, 02 Dec 2025 02:15:56 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad80fab85b5991343b1d2010a4b650763a78af87c439f15a08637dc078415b1e`  
		Last Modified: Tue, 02 Dec 2025 02:15:56 GMT  
		Size: 1.5 MB (1524590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339f7ed21150d3bbba5ff0f04739e3ea504b45534b799e23358f6edb35538093`  
		Last Modified: Tue, 02 Dec 2025 02:15:56 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2-php8.1` - unknown; unknown

```console
$ docker pull wordpress@sha256:d925eb1da7367941ef77579b1bf2a71bb64bb06c6ea35c36be44efb2e38dd235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.2 KB (633156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bafc048bcb09bd28709a9be69c15896a704edb0b6afe59ca1a9aacb028b4f3a3`

```dockerfile
```

-	Layers:
	-	`sha256:a573827156b2b67c4c2056657473865827cb7e1131a3da7dfcda3196e5073975`  
		Last Modified: Tue, 02 Dec 2025 05:28:02 GMT  
		Size: 591.0 KB (591002 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f16155e6003bc38df2a5213281d6b893e01d2a9546662510757343f87fbb7ab9`  
		Last Modified: Tue, 02 Dec 2025 05:28:03 GMT  
		Size: 42.2 KB (42154 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2-php8.1` - linux; riscv64

```console
$ docker pull wordpress@sha256:2cac6c15959ca853f25971c95590abd070fc8496a4426f165797eac184d04e9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 MB (59090608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:812816823eca84e468976ff3d0cfd70a8b32ba69da7c9aafbd3ac06a58d5b2cb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Thu, 31 Jul 2025 19:22:09 GMT
ADD alpine-minirootfs-3.21.5-riscv64.tar.gz / # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
CMD ["/bin/sh"]
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 31 Jul 2025 19:22:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 31 Jul 2025 19:22:09 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_VERSION=8.1.33
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.33.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.33.tar.xz.asc
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_SHA256=9db83bf4590375562bc1a10b353cccbcf9fcfc56c58b7c8fb814e6865bb928d1
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		patch 		patchutils 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	curl -fL 'https://github.com/php/php-src/commit/577b8ae4226368e66fee7a9b5c58f9e2428372fc.patch?full_index=1' -o 11678.patch; 	echo '6edc20c3bb3e7cc13515abce7f2fffa8ebea6cf7469abfbc78fcdc120350b239 *11678.patch' | sha256sum -c -; 	patch -p1 < 11678.patch; 	rm 11678.patch; 	curl -fL 'https://github.com/php/php-src/commit/67259e451d5d58b4842776c5696a66d74e157609.patch?full_index=1' -o 14834.patch; 	echo 'ed10a1b254091ad676ed204e55628ecbd6c8962004d6185a1821cedecd526c0f *14834.patch' | sha256sum -c -; 	filterdiff -x '*/NEWS' 14834.patch | patch -p1; 	rm 14834.patch; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 31 Jul 2025 19:22:09 GMT
CMD ["php" "-a"]
# Tue, 02 Dec 2025 06:29:17 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Tue, 02 Dec 2025 06:29:18 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Tue, 02 Dec 2025 06:29:18 GMT
WORKDIR /var/www/html
# Tue, 02 Dec 2025 06:39:18 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 06:39:18 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 06:39:32 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Tue, 02 Dec 2025 06:39:32 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Tue, 02 Dec 2025 06:39:32 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Tue, 02 Dec 2025 06:39:32 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Tue, 02 Dec 2025 06:39:32 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 06:39:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 06:39:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 06:39:32 GMT
USER www-data
# Tue, 02 Dec 2025 06:39:32 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:f874295bfcd01a87ee99265d45f0786d35242cd9d53bc2744cb330bf3be277f5`  
		Last Modified: Mon, 08 Dec 2025 00:04:31 GMT  
		Size: 3.4 MB (3351001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b4b6b5df65583dbfb630ea00737b31431acd95351a8911538e0d48988041fe`  
		Last Modified: Thu, 09 Oct 2025 09:24:05 GMT  
		Size: 3.5 MB (3492377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:058411602b31aff80dc2a52786ab3585b8b01a5029568e3b5135401574e8618d`  
		Last Modified: Thu, 09 Oct 2025 09:24:05 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:287d635bbdb57d4de98951a4f3c3c7c37a8517af3c6f9118b910bc76c6421f56`  
		Last Modified: Thu, 09 Oct 2025 09:24:04 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb7912db93521f9252540150dbd0c4988302e21159808a37105c9719c1c2bd9`  
		Last Modified: Fri, 10 Oct 2025 05:30:38 GMT  
		Size: 11.9 MB (11920001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a44b5e0d1562653dc2d36823da12f9e52ef6086e40ba4b66e43779f8d0e046`  
		Last Modified: Fri, 10 Oct 2025 05:30:37 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c351f68a550db4a41135d513f0fb735168b946a3ff13f1d43da8fc20304742`  
		Last Modified: Fri, 10 Oct 2025 05:30:37 GMT  
		Size: 15.8 MB (15799209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e32fcbe0c0c54baf75290199ed86398d324353c8b2381879f82fb80dd404fb`  
		Last Modified: Fri, 10 Oct 2025 05:30:36 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38bb103f1dde1a550b64ec069198772f09df3e2703b6b0909157da4a0e6bc677`  
		Last Modified: Fri, 10 Oct 2025 05:30:37 GMT  
		Size: 19.8 KB (19758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdfb049ffa134d65e94d242f5d48387c5bc8e7bb31830c9b743d6809bfdbf0e1`  
		Last Modified: Fri, 10 Oct 2025 05:30:37 GMT  
		Size: 19.8 KB (19754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f423824eac69b655388d1b3b120e7139ab6ec85bee29fa474de1302d8555d00`  
		Last Modified: Tue, 02 Dec 2025 06:41:19 GMT  
		Size: 11.6 MB (11557552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e07a47425265189ce053a20e7d36b237a4bee185ae4aa335d59cc71a97ef0f`  
		Last Modified: Tue, 02 Dec 2025 06:41:18 GMT  
		Size: 11.4 MB (11401418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a9fa23a53405795e5ec6081cb9407cbdfedb973dcd9809ea259d1f257a30e78`  
		Last Modified: Tue, 02 Dec 2025 06:41:17 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d91c8a0000ea5c51337a5926d388a2f5a367ca8e1c73f8ee630f76448f8ff7`  
		Last Modified: Tue, 02 Dec 2025 06:41:18 GMT  
		Size: 1.5 MB (1524571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16dea765654bafa994efedde6e507609c5a032674e815fc30d3ce32588f4f732`  
		Last Modified: Tue, 02 Dec 2025 06:41:18 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2-php8.1` - unknown; unknown

```console
$ docker pull wordpress@sha256:a8abeab7589bd28105e2cb9096953acf1346caaeef9017610ddfd0734ed7bc80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.2 KB (633152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e758657a7a7aebb652db8b0d9afc5d4da6fe991972286ca4a78e9227cfd5a7f7`

```dockerfile
```

-	Layers:
	-	`sha256:c3403f9cb0290a9bcbdf21cf329b8028a703daab2ae2701b1e765e11cb2bcdf5`  
		Last Modified: Tue, 02 Dec 2025 08:17:10 GMT  
		Size: 591.0 KB (590998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e08d30fb99a589457ffa8cf1fe870df660a908143db11d0bdf54df8f5d954237`  
		Last Modified: Tue, 02 Dec 2025 08:17:10 GMT  
		Size: 42.2 KB (42154 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2-php8.1` - linux; s390x

```console
$ docker pull wordpress@sha256:5376eee1f1f0dff261d9ae204f5fefaf1eed59a935d846d8862bf6687353a96a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.1 MB (63097445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94739901402d1a9f51947b03eb6cdc7b36d16806c8a35b1b727d38e4647f1dc9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Thu, 31 Jul 2025 19:22:09 GMT
ADD alpine-minirootfs-3.21.5-s390x.tar.gz / # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
CMD ["/bin/sh"]
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 31 Jul 2025 19:22:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 31 Jul 2025 19:22:09 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_VERSION=8.1.33
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.33.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.33.tar.xz.asc
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_SHA256=9db83bf4590375562bc1a10b353cccbcf9fcfc56c58b7c8fb814e6865bb928d1
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		patch 		patchutils 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	curl -fL 'https://github.com/php/php-src/commit/577b8ae4226368e66fee7a9b5c58f9e2428372fc.patch?full_index=1' -o 11678.patch; 	echo '6edc20c3bb3e7cc13515abce7f2fffa8ebea6cf7469abfbc78fcdc120350b239 *11678.patch' | sha256sum -c -; 	patch -p1 < 11678.patch; 	rm 11678.patch; 	curl -fL 'https://github.com/php/php-src/commit/67259e451d5d58b4842776c5696a66d74e157609.patch?full_index=1' -o 14834.patch; 	echo 'ed10a1b254091ad676ed204e55628ecbd6c8962004d6185a1821cedecd526c0f *14834.patch' | sha256sum -c -; 	filterdiff -x '*/NEWS' 14834.patch | patch -p1; 	rm 14834.patch; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 31 Jul 2025 19:22:09 GMT
CMD ["php" "-a"]
# Tue, 02 Dec 2025 02:30:48 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Tue, 02 Dec 2025 02:30:48 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Tue, 02 Dec 2025 02:30:49 GMT
WORKDIR /var/www/html
# Tue, 02 Dec 2025 02:32:12 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 02:32:12 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 02:32:17 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Tue, 02 Dec 2025 02:32:17 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Tue, 02 Dec 2025 02:32:17 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Tue, 02 Dec 2025 02:32:17 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Tue, 02 Dec 2025 02:32:17 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 02:32:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 02:32:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 02:32:17 GMT
USER www-data
# Tue, 02 Dec 2025 02:32:17 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:9f2ceebb28b6c8480d6ae26501eda06bf0b6029f7c797c80673b95a60276e050`  
		Last Modified: Sun, 07 Dec 2025 17:58:56 GMT  
		Size: 3.5 MB (3466434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49540c560fe10b1e05647baff6bd09f225aaf3a526cf39dba0a8343e1c6057c5`  
		Last Modified: Thu, 09 Oct 2025 06:27:22 GMT  
		Size: 3.6 MB (3596736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2692170ad3b9023fe7d1f440cb17914dc95961c0c7494e0b1d28ba2eaf006812`  
		Last Modified: Thu, 09 Oct 2025 06:27:22 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6ee6723e50491cb091c047add64e5dbaff649181c8f4090ad9e6de28ec4afbd`  
		Last Modified: Thu, 09 Oct 2025 06:27:22 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:912d8aa95478da361f40542c1c285b6b6571798be423e4f7025a2645f4b8b20f`  
		Last Modified: Thu, 09 Oct 2025 07:13:03 GMT  
		Size: 11.9 MB (11919997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af78867c89a317673e291bc9ce256a87781ee890ec67d2cff994e3dd6e9670f3`  
		Last Modified: Thu, 09 Oct 2025 07:13:03 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31175a5d28accf459b0d51c1d33d29f4e940a69fcbe0f72fd8bbd3b088d58b89`  
		Last Modified: Thu, 09 Oct 2025 07:13:03 GMT  
		Size: 16.7 MB (16704760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6971e6e21e9367011e4bc7429f285a824564cd9af6890ea8f2b012b0c2af639e`  
		Last Modified: Thu, 09 Oct 2025 07:13:03 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2104f51f498f96abc5c4fa63f20c0eb9f6d26c0fcccdbe5354629e197dfe0d67`  
		Last Modified: Thu, 09 Oct 2025 07:13:04 GMT  
		Size: 19.8 KB (19779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b8ef18fc6108fc0294dae872d500e24c4ac9dbecf18d6c75e60b8211eb43be`  
		Last Modified: Thu, 09 Oct 2025 07:13:04 GMT  
		Size: 19.8 KB (19777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86e64f1be6172755603b3f864bb4d5d598c0743ab7dfb01b720329deb056ff0`  
		Last Modified: Tue, 02 Dec 2025 02:32:44 GMT  
		Size: 12.4 MB (12433689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ead6b1c09da40be794a58da88228468b6c17b78af2aae333b8b390e09b8f9cf`  
		Last Modified: Tue, 02 Dec 2025 02:32:44 GMT  
		Size: 13.4 MB (13406744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07150c35367165c9a44470c4eb39bf48e1db16373c7e78896bb8fd49c335b23a`  
		Last Modified: Tue, 02 Dec 2025 02:32:43 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bedd45c1b5c260ff0e020991def32370e9e31f3688f30df560de63c5eabc64ee`  
		Last Modified: Tue, 02 Dec 2025 02:32:46 GMT  
		Size: 1.5 MB (1524584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b38c89694e8b005ac9b4c514946c3082ecc619debfe75df8b08936a653168460`  
		Last Modified: Tue, 02 Dec 2025 02:32:43 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2-php8.1` - unknown; unknown

```console
$ docker pull wordpress@sha256:3c36bc9d695a6cd864ce51a4779d88b4d27af7ba6f373a97a2245510fc7fd9e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.1 KB (633070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:108872564cfac7c6bfd1c4019169adb0f052a20b7f19fb833242784d95b57606`

```dockerfile
```

-	Layers:
	-	`sha256:464ca989bfd6b78604d9c4dc2dc4c4fa7f10a4f97d2d1192e0a9f16fa854be94`  
		Last Modified: Tue, 02 Dec 2025 05:28:08 GMT  
		Size: 591.0 KB (590968 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29ff67eb54c65c9b3e210ce46c24ae5e4333bcf9e111340c78f1be05c2ea4f24`  
		Last Modified: Tue, 02 Dec 2025 05:28:09 GMT  
		Size: 42.1 KB (42102 bytes)  
		MIME: application/vnd.in-toto+json
