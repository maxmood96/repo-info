## `wordpress:cli-2-php8.1`

```console
$ docker pull wordpress@sha256:6f35516a2a8182f232ecf8c73829ec238dff86f8391623a8db3765eac074d228
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
$ docker pull wordpress@sha256:f6534b40833bcc3adc261e609e99f3b2a026a43d585a54092b150c852842438b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61696819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8baa318d69a25b7d72aa8c4324d70573666a057ecf670d416d342c872fcd9e0f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Fri, 19 Dec 2025 23:41:04 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Dec 2025 23:41:04 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Dec 2025 23:41:04 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Dec 2025 23:41:04 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Dec 2025 23:41:04 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Dec 2025 23:41:04 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Dec 2025 23:41:04 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Dec 2025 23:41:04 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Dec 2025 23:41:04 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 19 Dec 2025 23:41:04 GMT
ENV PHP_VERSION=8.1.34
# Fri, 19 Dec 2025 23:41:04 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.34.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.34.tar.xz.asc
# Fri, 19 Dec 2025 23:41:04 GMT
ENV PHP_SHA256=ffa9e0982e82eeaea848f57687b425ed173aa278fe563001310ae2638db5c251
# Fri, 19 Dec 2025 23:41:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Dec 2025 23:41:08 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 23:43:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		patch 		patchutils 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	curl -fL 'https://github.com/php/php-src/commit/577b8ae4226368e66fee7a9b5c58f9e2428372fc.patch?full_index=1' -o 11678.patch; 	echo '6edc20c3bb3e7cc13515abce7f2fffa8ebea6cf7469abfbc78fcdc120350b239 *11678.patch' | sha256sum -c -; 	patch -p1 < 11678.patch; 	rm 11678.patch; 	curl -fL 'https://github.com/php/php-src/commit/a5df26691d1b1f71b964b869510473a5d5413999.patch?full_index=1' -o 19131.patch; 	echo 'c98c01c74d3a6da197116f8511b16fed361ca6bbb6a8af8df629a933f541c213 *19131.patch' | sha256sum -c -; 	patch --reverse -p1 < 19131.patch; 	rm 19131.patch; 	curl -fL 'https://github.com/php/php-src/commit/67259e451d5d58b4842776c5696a66d74e157609.patch?full_index=1' -o 14834.patch; 	echo 'ed10a1b254091ad676ed204e55628ecbd6c8962004d6185a1821cedecd526c0f *14834.patch' | sha256sum -c -; 	filterdiff -x '*/NEWS' 14834.patch | patch -p1; 	rm 14834.patch; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Dec 2025 23:43:54 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 23:43:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Dec 2025 23:43:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Dec 2025 23:43:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Dec 2025 23:43:55 GMT
CMD ["php" "-a"]
# Sat, 20 Dec 2025 00:08:17 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Sat, 20 Dec 2025 00:08:17 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Sat, 20 Dec 2025 00:08:17 GMT
WORKDIR /var/www/html
# Sat, 20 Dec 2025 00:09:02 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Sat, 20 Dec 2025 00:09:02 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Sat, 20 Dec 2025 00:09:04 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Sat, 20 Dec 2025 00:09:04 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Sat, 20 Dec 2025 00:09:04 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Sat, 20 Dec 2025 00:09:04 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Sat, 20 Dec 2025 00:09:04 GMT
VOLUME [/var/www/html]
# Sat, 20 Dec 2025 00:09:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 20 Dec 2025 00:09:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 20 Dec 2025 00:09:04 GMT
USER www-data
# Sat, 20 Dec 2025 00:09:04 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Sun, 07 Dec 2025 13:55:07 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c769295445bc37324a408c56419f4f76f69fbcb4c42a65a3ea95347e09cd0af2`  
		Last Modified: Fri, 19 Dec 2025 23:44:10 GMT  
		Size: 3.4 MB (3367615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e77662968dd7ed1c034f785cd89f4aaf52012c80096a1c2298d8661c9e4175`  
		Last Modified: Fri, 19 Dec 2025 23:44:10 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd78fd5671e660c33f54d404110f20e1b2ff24f07a48881a239323abee76084`  
		Last Modified: Fri, 19 Dec 2025 23:44:10 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa267d384b6eb8afc00a0b50591abd82fbbc45a64661b731b7188faea58b2ee9`  
		Last Modified: Fri, 19 Dec 2025 23:44:11 GMT  
		Size: 11.9 MB (11925148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b4249299cb43ae5b0126477548bce343fae00f39403c3b965042c440719dd0`  
		Last Modified: Fri, 19 Dec 2025 23:44:10 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a731bc8f497d628213a18641d7547d2d45fffd611b78ab1c58026c488dcdf6f3`  
		Last Modified: Fri, 19 Dec 2025 23:44:11 GMT  
		Size: 16.7 MB (16668109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea6dd63a208eabaee9c7c3913b915dc380938f4063482de59af7072909943b85`  
		Last Modified: Fri, 19 Dec 2025 23:44:10 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503acfe38957bbbebd542097db0befe8ea41160d17ee6c91e575fdb934bf2821`  
		Last Modified: Fri, 19 Dec 2025 23:44:11 GMT  
		Size: 20.0 KB (19959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:472cd3cac13d7b7ca40e9fcdb0fcf9b45ece7814af10217c8030ba6817bdf11a`  
		Last Modified: Fri, 19 Dec 2025 23:44:10 GMT  
		Size: 19.9 KB (19948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad6d1959e27fd120dd7591547b275c15eab6c7a5bb65f0c494620a64d2bcb8dd`  
		Last Modified: Sat, 20 Dec 2025 00:09:21 GMT  
		Size: 11.1 MB (11075573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361fdc9b5569681ef682ba112c84c1a1b23b4143a4d5dbfd13ac53c4f7682f98`  
		Last Modified: Sat, 20 Dec 2025 00:09:21 GMT  
		Size: 13.4 MB (13448346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef9b43295faeeaa00a6d43d63a3a33934cce80366de732cb7729c119a85dd194`  
		Last Modified: Sat, 20 Dec 2025 00:09:20 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6874ca0b72c7ed9f19e4db27e9d0d7819117c23baa207a3a0a29297be3d0b0`  
		Last Modified: Sat, 20 Dec 2025 00:09:20 GMT  
		Size: 1.5 MB (1524611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6ded70a4becf69aa5119d7794186a97e8a195e0a83967d7e79a32a97232edb`  
		Last Modified: Sat, 20 Dec 2025 00:09:20 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2-php8.1` - unknown; unknown

```console
$ docker pull wordpress@sha256:e4795bc7b314620b3fbd20c7d5e9af21105084c2040a97aef7662c6578372943
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.3 KB (636265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44216588387c45e6ed4acce4d5e81895c0550ea4a5fdf75117f491a0534efa16`

```dockerfile
```

-	Layers:
	-	`sha256:6e7a516215e93652be069fa7c4146dcf3564c6ee0686da52de45f6c4e3c4f454`  
		Last Modified: Sat, 20 Dec 2025 02:16:35 GMT  
		Size: 594.2 KB (594163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dda68cba04c4a9757f28608f3cfc05ffaaef50d4d99541dfad79683d8a95883d`  
		Last Modified: Sat, 20 Dec 2025 02:16:36 GMT  
		Size: 42.1 KB (42102 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2-php8.1` - linux; arm variant v6

```console
$ docker pull wordpress@sha256:780cec441112046db3bec15640603e7a55422264939845dbea63d6758489b203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.0 MB (57003241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:089f8c8d4bc912f4988603c9b1a10af925dffccd28304ad695175ae183871dd1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Fri, 19 Dec 2025 23:43:59 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Dec 2025 23:43:59 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Dec 2025 23:43:59 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Dec 2025 23:43:59 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Dec 2025 23:44:00 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Dec 2025 23:44:00 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Dec 2025 23:44:00 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Dec 2025 23:44:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Dec 2025 23:44:00 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 19 Dec 2025 23:44:00 GMT
ENV PHP_VERSION=8.1.34
# Fri, 19 Dec 2025 23:44:00 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.34.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.34.tar.xz.asc
# Fri, 19 Dec 2025 23:44:00 GMT
ENV PHP_SHA256=ffa9e0982e82eeaea848f57687b425ed173aa278fe563001310ae2638db5c251
# Fri, 19 Dec 2025 23:44:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Dec 2025 23:44:04 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 23:46:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		patch 		patchutils 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	curl -fL 'https://github.com/php/php-src/commit/577b8ae4226368e66fee7a9b5c58f9e2428372fc.patch?full_index=1' -o 11678.patch; 	echo '6edc20c3bb3e7cc13515abce7f2fffa8ebea6cf7469abfbc78fcdc120350b239 *11678.patch' | sha256sum -c -; 	patch -p1 < 11678.patch; 	rm 11678.patch; 	curl -fL 'https://github.com/php/php-src/commit/a5df26691d1b1f71b964b869510473a5d5413999.patch?full_index=1' -o 19131.patch; 	echo 'c98c01c74d3a6da197116f8511b16fed361ca6bbb6a8af8df629a933f541c213 *19131.patch' | sha256sum -c -; 	patch --reverse -p1 < 19131.patch; 	rm 19131.patch; 	curl -fL 'https://github.com/php/php-src/commit/67259e451d5d58b4842776c5696a66d74e157609.patch?full_index=1' -o 14834.patch; 	echo 'ed10a1b254091ad676ed204e55628ecbd6c8962004d6185a1821cedecd526c0f *14834.patch' | sha256sum -c -; 	filterdiff -x '*/NEWS' 14834.patch | patch -p1; 	rm 14834.patch; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Dec 2025 23:46:52 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 23:46:52 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Dec 2025 23:46:53 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Dec 2025 23:46:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Dec 2025 23:46:53 GMT
CMD ["php" "-a"]
# Sat, 20 Dec 2025 00:06:03 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Sat, 20 Dec 2025 00:06:03 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Sat, 20 Dec 2025 00:06:03 GMT
WORKDIR /var/www/html
# Sat, 20 Dec 2025 00:07:04 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Sat, 20 Dec 2025 00:07:04 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Sat, 20 Dec 2025 00:07:06 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Sat, 20 Dec 2025 00:07:06 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Sat, 20 Dec 2025 00:07:06 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Sat, 20 Dec 2025 00:07:06 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Sat, 20 Dec 2025 00:07:06 GMT
VOLUME [/var/www/html]
# Sat, 20 Dec 2025 00:07:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 20 Dec 2025 00:07:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 20 Dec 2025 00:07:06 GMT
USER www-data
# Sat, 20 Dec 2025 00:07:06 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:f8b30cbd0fab9e5a803578a09c973d18d7450816d914e63e04e5c2edd79f8bee`  
		Last Modified: Mon, 08 Dec 2025 00:04:31 GMT  
		Size: 3.4 MB (3365468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90603a2a410a85e12f63a2cde510005c4a1364922a80647ca30edb748234c956`  
		Last Modified: Fri, 19 Dec 2025 23:47:07 GMT  
		Size: 3.3 MB (3337518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ff78408204e3ebc30e175aa7f8367a36f52d890e2d9e7729acf5fc21cf58df`  
		Last Modified: Fri, 19 Dec 2025 23:47:06 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56e02572a06f7680998eb325969df27ad21aed09cb6e30aa228144d368e48f3`  
		Last Modified: Fri, 19 Dec 2025 23:47:06 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51fb4692009ec0ae0bbdd73c71ca9681f00ac5ac8f99f154e8855dd0d9f2137a`  
		Last Modified: Fri, 19 Dec 2025 23:47:09 GMT  
		Size: 11.9 MB (11925158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa368bf39a1ee24cbd025faef582d75adfc1d68367a9c39fa65bdee666f69f54`  
		Last Modified: Fri, 19 Dec 2025 23:47:06 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e2a91efedeecdf7bf72576568ca5e5b135ca1ff26807df0a338d7211e0e7728`  
		Last Modified: Fri, 19 Dec 2025 23:47:09 GMT  
		Size: 15.1 MB (15059588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60a3c6d11fcb59a869b54a374bdc771f1189bfffcf58963e58db3ec0691056c`  
		Last Modified: Fri, 19 Dec 2025 23:47:06 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d16af064177ba3db354b92f2d614d5522ef7adaf20034c904a287659f5dfafd`  
		Last Modified: Fri, 19 Dec 2025 23:47:18 GMT  
		Size: 19.8 KB (19772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e17fa876c3394626f77c05ea46d995c2bc5ca5e696e384edc91a89fb7428b92`  
		Last Modified: Fri, 19 Dec 2025 23:47:06 GMT  
		Size: 19.8 KB (19769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:863b0c005d5195a3db33cfe63ee36e15af79d27093d2fe0f596957cffda8fc81`  
		Last Modified: Sat, 20 Dec 2025 00:07:24 GMT  
		Size: 10.8 MB (10760577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f587b2f97ff96e2dc83062ee1e64e7f1cd376c28bd31962622b3f07a549ddc`  
		Last Modified: Sat, 20 Dec 2025 00:07:22 GMT  
		Size: 11.0 MB (10985880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad0687639e63121f2577e9c0f6291d3cd507f9354962aaa4d7ca1ccec124bae`  
		Last Modified: Sat, 20 Dec 2025 00:07:21 GMT  
		Size: 383.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a82a07aed60783f00256705eaf3ed36898b41edecac399fafa29ff3a1e33fd6`  
		Last Modified: Sat, 20 Dec 2025 00:07:22 GMT  
		Size: 1.5 MB (1524570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5c44a7524ef8af00e7bd47a074fa53b8d5f95b7b297453cd83748aba8c1eab`  
		Last Modified: Sat, 20 Dec 2025 00:07:22 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2-php8.1` - unknown; unknown

```console
$ docker pull wordpress@sha256:91a727e643fd1704eefd82df6b89eb0067addf174dcbb4ebd7ec29bec69d6147
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 KB (42019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb17bf6a4f059de1c0a41be50900c8cb54a2bf638d171f6764a1e981e9e70180`

```dockerfile
```

-	Layers:
	-	`sha256:f65bbc0f1d273fed78c76f58bde71f01426178e41651d19a5de81233117553fe`  
		Last Modified: Sat, 20 Dec 2025 02:16:39 GMT  
		Size: 42.0 KB (42019 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2-php8.1` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:c3be78a1d72dd02c6408fda810127f3807db940752516da00b57acd01aff3da1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.3 MB (56298495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6a1bc1fbf07126a717020d80b1e22282fa3beb430a6b422bcd275d018755e34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Fri, 19 Dec 2025 23:40:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Dec 2025 23:40:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Dec 2025 23:40:27 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Dec 2025 23:40:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Dec 2025 23:40:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Dec 2025 23:40:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Dec 2025 23:40:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Dec 2025 23:40:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Dec 2025 23:40:27 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 19 Dec 2025 23:40:27 GMT
ENV PHP_VERSION=8.1.34
# Fri, 19 Dec 2025 23:40:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.34.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.34.tar.xz.asc
# Fri, 19 Dec 2025 23:40:27 GMT
ENV PHP_SHA256=ffa9e0982e82eeaea848f57687b425ed173aa278fe563001310ae2638db5c251
# Fri, 19 Dec 2025 23:40:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Dec 2025 23:40:34 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 23:43:29 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		patch 		patchutils 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	curl -fL 'https://github.com/php/php-src/commit/577b8ae4226368e66fee7a9b5c58f9e2428372fc.patch?full_index=1' -o 11678.patch; 	echo '6edc20c3bb3e7cc13515abce7f2fffa8ebea6cf7469abfbc78fcdc120350b239 *11678.patch' | sha256sum -c -; 	patch -p1 < 11678.patch; 	rm 11678.patch; 	curl -fL 'https://github.com/php/php-src/commit/a5df26691d1b1f71b964b869510473a5d5413999.patch?full_index=1' -o 19131.patch; 	echo 'c98c01c74d3a6da197116f8511b16fed361ca6bbb6a8af8df629a933f541c213 *19131.patch' | sha256sum -c -; 	patch --reverse -p1 < 19131.patch; 	rm 19131.patch; 	curl -fL 'https://github.com/php/php-src/commit/67259e451d5d58b4842776c5696a66d74e157609.patch?full_index=1' -o 14834.patch; 	echo 'ed10a1b254091ad676ed204e55628ecbd6c8962004d6185a1821cedecd526c0f *14834.patch' | sha256sum -c -; 	filterdiff -x '*/NEWS' 14834.patch | patch -p1; 	rm 14834.patch; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Dec 2025 23:43:29 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 23:43:29 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Dec 2025 23:43:30 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Dec 2025 23:43:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Dec 2025 23:43:30 GMT
CMD ["php" "-a"]
# Sat, 20 Dec 2025 00:08:30 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Sat, 20 Dec 2025 00:08:30 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Sat, 20 Dec 2025 00:08:30 GMT
WORKDIR /var/www/html
# Sat, 20 Dec 2025 00:09:25 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Sat, 20 Dec 2025 00:09:25 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Sat, 20 Dec 2025 00:09:27 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Sat, 20 Dec 2025 00:09:27 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Sat, 20 Dec 2025 00:09:27 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Sat, 20 Dec 2025 00:09:27 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Sat, 20 Dec 2025 00:09:27 GMT
VOLUME [/var/www/html]
# Sat, 20 Dec 2025 00:09:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 20 Dec 2025 00:09:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 20 Dec 2025 00:09:27 GMT
USER www-data
# Sat, 20 Dec 2025 00:09:27 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:520d06ecc3ba4ec2920319fa6f2cc6bea9a9c1d5a43808c1d2388522c37d7b30`  
		Last Modified: Sun, 07 Dec 2025 17:58:54 GMT  
		Size: 3.1 MB (3098611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28c294cf4ae4f413891d04f3bf474cf5f06f774d578b551b0ce2ad987241bd7`  
		Last Modified: Fri, 19 Dec 2025 23:43:42 GMT  
		Size: 3.1 MB (3143728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a17ffa5be3fa885fe4c7f3e4166b6c7d1df83560cc2b7ace155cdf75945c26`  
		Last Modified: Fri, 19 Dec 2025 23:43:42 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0745bc74ee649a65793a2533f9cdb3fc97c653410a489825637130dc49e8765f`  
		Last Modified: Fri, 19 Dec 2025 23:43:42 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a818154ac6daf3442c41a86940fdee8a5ab6ebdaf3cbff018779edf0794afc`  
		Last Modified: Fri, 19 Dec 2025 23:43:43 GMT  
		Size: 11.9 MB (11925152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e337915a48619218e9f6f170fc7fc9e9c95d7a284cd17a284f09b39c8a71a90b`  
		Last Modified: Fri, 19 Dec 2025 23:43:45 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaeb34ecf64defa9127f89559b7e51f4e59fc423233c59650d4e0b4cecfa8102`  
		Last Modified: Fri, 19 Dec 2025 23:43:44 GMT  
		Size: 14.2 MB (14164488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dcf0202e21366cc8de77437a8f955425d0386d53211ccb315649d05584beb1c`  
		Last Modified: Fri, 19 Dec 2025 23:43:43 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82aef60e7f15d9d847332d76e96634ae0ce78ceaf581c8b352c3ad1a9066e67e`  
		Last Modified: Fri, 19 Dec 2025 23:43:43 GMT  
		Size: 19.8 KB (19777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6879e6c74c7237278afeecf7620748be796e1281eab9e844b84ea2320807cd44`  
		Last Modified: Fri, 19 Dec 2025 23:43:43 GMT  
		Size: 19.8 KB (19779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ee0a1d4bc499d638721f5e6e9a23e61faed5bcbe8182a646cf4e11938ba930a`  
		Last Modified: Sat, 20 Dec 2025 00:09:44 GMT  
		Size: 10.4 MB (10437270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd32d14a7a939b04097c29437fbe1d2c19eee003e89164081384b44985f370d`  
		Last Modified: Sat, 20 Dec 2025 00:09:45 GMT  
		Size: 12.0 MB (11960187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c485740a9cbc9457425c0577457ada43eb70fe7c485ef9f9ed0a4d65e4639176`  
		Last Modified: Sat, 20 Dec 2025 00:09:44 GMT  
		Size: 384.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:419aaa7194a487b358b84233b2b69f73882166d1ec9e7c5054288eaaf18ffe21`  
		Last Modified: Sat, 20 Dec 2025 00:09:43 GMT  
		Size: 1.5 MB (1524560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20609bdcfed7937821aa04ab30dbf168e48d745251b5542df65050d4dfc9c24a`  
		Last Modified: Sat, 20 Dec 2025 00:09:43 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2-php8.1` - unknown; unknown

```console
$ docker pull wordpress@sha256:cad9c27aad562b7a8ac64f488ac29a8949f422bd3e21512e55879a212811e515
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **635.2 KB (635188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6676bd20d55991142e38f27df9a19d9f06bb8c415d92d357eec640b56a60270`

```dockerfile
```

-	Layers:
	-	`sha256:8503dac89632bda76a84e9607309b6a302ddeecf33769f55c91583c35b785a2d`  
		Last Modified: Sat, 20 Dec 2025 02:16:42 GMT  
		Size: 593.0 KB (592955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16100f07b26c869f11b251a0f5e73a3b2f3ed2ff100cb77868812988b2f79ede`  
		Last Modified: Sat, 20 Dec 2025 02:16:43 GMT  
		Size: 42.2 KB (42233 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2-php8.1` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:e992fe9a41906ebc3580391935a229aa9b92877ab3d5830efb9a74a805a7ff60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (62016518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf17d98bc5215ddc5fcbdcdbf29cf6f91c7153c2717e611fe9ac1a7280f05436`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Fri, 19 Dec 2025 23:40:26 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Dec 2025 23:40:26 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Dec 2025 23:40:26 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Dec 2025 23:40:26 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Dec 2025 23:40:26 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Dec 2025 23:40:26 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Dec 2025 23:40:26 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Dec 2025 23:40:26 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Dec 2025 23:40:26 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 19 Dec 2025 23:40:26 GMT
ENV PHP_VERSION=8.1.34
# Fri, 19 Dec 2025 23:40:26 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.34.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.34.tar.xz.asc
# Fri, 19 Dec 2025 23:40:26 GMT
ENV PHP_SHA256=ffa9e0982e82eeaea848f57687b425ed173aa278fe563001310ae2638db5c251
# Fri, 19 Dec 2025 23:40:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Dec 2025 23:40:30 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 23:44:46 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		patch 		patchutils 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	curl -fL 'https://github.com/php/php-src/commit/577b8ae4226368e66fee7a9b5c58f9e2428372fc.patch?full_index=1' -o 11678.patch; 	echo '6edc20c3bb3e7cc13515abce7f2fffa8ebea6cf7469abfbc78fcdc120350b239 *11678.patch' | sha256sum -c -; 	patch -p1 < 11678.patch; 	rm 11678.patch; 	curl -fL 'https://github.com/php/php-src/commit/a5df26691d1b1f71b964b869510473a5d5413999.patch?full_index=1' -o 19131.patch; 	echo 'c98c01c74d3a6da197116f8511b16fed361ca6bbb6a8af8df629a933f541c213 *19131.patch' | sha256sum -c -; 	patch --reverse -p1 < 19131.patch; 	rm 19131.patch; 	curl -fL 'https://github.com/php/php-src/commit/67259e451d5d58b4842776c5696a66d74e157609.patch?full_index=1' -o 14834.patch; 	echo 'ed10a1b254091ad676ed204e55628ecbd6c8962004d6185a1821cedecd526c0f *14834.patch' | sha256sum -c -; 	filterdiff -x '*/NEWS' 14834.patch | patch -p1; 	rm 14834.patch; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Dec 2025 23:44:46 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 23:44:47 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Dec 2025 23:44:48 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Dec 2025 23:44:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Dec 2025 23:44:48 GMT
CMD ["php" "-a"]
# Sat, 20 Dec 2025 00:08:11 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Sat, 20 Dec 2025 00:08:11 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Sat, 20 Dec 2025 00:08:11 GMT
WORKDIR /var/www/html
# Sat, 20 Dec 2025 00:09:01 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Sat, 20 Dec 2025 00:09:01 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Sat, 20 Dec 2025 00:09:03 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Sat, 20 Dec 2025 00:09:03 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Sat, 20 Dec 2025 00:09:03 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Sat, 20 Dec 2025 00:09:03 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Sat, 20 Dec 2025 00:09:03 GMT
VOLUME [/var/www/html]
# Sat, 20 Dec 2025 00:09:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 20 Dec 2025 00:09:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 20 Dec 2025 00:09:03 GMT
USER www-data
# Sat, 20 Dec 2025 00:09:03 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Sun, 07 Dec 2025 17:54:48 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cdf075910714cea38950e87fd11d24c977550486158e9f2f0653dce6e3f4809`  
		Last Modified: Fri, 19 Dec 2025 23:45:03 GMT  
		Size: 3.4 MB (3361720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a80d0394155edda91631906d378a987d2c67b8ee354f0599714eda5579e793bb`  
		Last Modified: Fri, 19 Dec 2025 23:45:03 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3607e81e2bb8bc0b1beb7e6d66ac1cf507a4cb4d2ea2a0cd67110c21cc8828db`  
		Last Modified: Fri, 19 Dec 2025 23:45:03 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e4292ad5be7088b88478170348a0863c1b0c0d0d6ce27796472d20ba4894f8`  
		Last Modified: Fri, 19 Dec 2025 23:45:04 GMT  
		Size: 11.9 MB (11925164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea1e3c520b02b6f82813168d7916ae99c9c2f2f1ccf84d456b5b4fdf7c7617a`  
		Last Modified: Fri, 19 Dec 2025 23:45:03 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d47bfca75f7d690ccf6649c4091e5f096f5c5570c8015e39fe7d65a19e1725`  
		Last Modified: Fri, 19 Dec 2025 23:45:05 GMT  
		Size: 16.6 MB (16577517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86491f097dd7c7791651a97adcb82fe6feb514749136b451c16268dcad5f8f10`  
		Last Modified: Fri, 19 Dec 2025 23:45:03 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d915901d5f72f0a011afca25cdc8fb383f1078718f49b12a6020c36cdcf76362`  
		Last Modified: Fri, 19 Dec 2025 23:45:03 GMT  
		Size: 19.8 KB (19780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994cd154528b5c8fcecbeeeb98b93aef3e65e0d7755b22210f1dbc0ca0127bee`  
		Last Modified: Fri, 19 Dec 2025 23:45:03 GMT  
		Size: 19.8 KB (19777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfaad256f20782141212c140dcad9ce149ce2fecb7b7f3d1d038725b5275789d`  
		Last Modified: Sat, 20 Dec 2025 00:09:20 GMT  
		Size: 11.1 MB (11083852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87b31d961ef2ed7c72bd4ba8bae6f6e90c1e23efc997fea35734495400d8dc37`  
		Last Modified: Sat, 20 Dec 2025 00:09:21 GMT  
		Size: 13.5 MB (13506857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:244b2558a14e7121e0ad0d0f7a05b7c5026c36790fe401fc6f9cd8ddb0591b44`  
		Last Modified: Sat, 20 Dec 2025 00:09:20 GMT  
		Size: 385.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:206216b0f0c515908792053cd27c6749738ed1a9cd7dc272fdd7961f8973d61d`  
		Last Modified: Sat, 20 Dec 2025 00:09:20 GMT  
		Size: 1.5 MB (1524559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b212b0c85ad64414b82cef01aa65685b5f7d9d74383a767bb62a3b8415b005`  
		Last Modified: Sat, 20 Dec 2025 00:09:20 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2-php8.1` - unknown; unknown

```console
$ docker pull wordpress@sha256:8c44ff21c3e02c254748b001060344f83b6e8aeffe97641cea109c3bd99c825a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **635.2 KB (635241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef26e488fe64798329b1d7f1db521772bda7bc7de4a4316306b326b82eb03a2`

```dockerfile
```

-	Layers:
	-	`sha256:c716ef1e052d0c7bce9423abe459989d9d606db674f03ae97cda4cbf8d4d0a80`  
		Last Modified: Sat, 20 Dec 2025 02:16:46 GMT  
		Size: 593.0 KB (592975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6232822f9f114374788920a3f2be9b0cc032f8797722f838eb429c1b2f15ec84`  
		Last Modified: Sat, 20 Dec 2025 02:16:47 GMT  
		Size: 42.3 KB (42266 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2-php8.1` - linux; 386

```console
$ docker pull wordpress@sha256:55f8247dd862318dc36ad469bbc0d738de081a27c0364f056b543a4ad86fd4d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61055506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a229fb83e3df1fae47a29f7adf2455711c75cc92e3a4c7b453428fe4b892c21f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Fri, 19 Dec 2025 23:44:44 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Dec 2025 23:44:44 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Dec 2025 23:44:44 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Dec 2025 23:44:44 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Dec 2025 23:44:44 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Dec 2025 23:44:44 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Dec 2025 23:44:44 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Dec 2025 23:44:44 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Dec 2025 23:44:44 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 19 Dec 2025 23:44:44 GMT
ENV PHP_VERSION=8.1.34
# Fri, 19 Dec 2025 23:44:44 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.34.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.34.tar.xz.asc
# Fri, 19 Dec 2025 23:44:44 GMT
ENV PHP_SHA256=ffa9e0982e82eeaea848f57687b425ed173aa278fe563001310ae2638db5c251
# Fri, 19 Dec 2025 23:44:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Dec 2025 23:44:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 23:48:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		patch 		patchutils 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	curl -fL 'https://github.com/php/php-src/commit/577b8ae4226368e66fee7a9b5c58f9e2428372fc.patch?full_index=1' -o 11678.patch; 	echo '6edc20c3bb3e7cc13515abce7f2fffa8ebea6cf7469abfbc78fcdc120350b239 *11678.patch' | sha256sum -c -; 	patch -p1 < 11678.patch; 	rm 11678.patch; 	curl -fL 'https://github.com/php/php-src/commit/a5df26691d1b1f71b964b869510473a5d5413999.patch?full_index=1' -o 19131.patch; 	echo 'c98c01c74d3a6da197116f8511b16fed361ca6bbb6a8af8df629a933f541c213 *19131.patch' | sha256sum -c -; 	patch --reverse -p1 < 19131.patch; 	rm 19131.patch; 	curl -fL 'https://github.com/php/php-src/commit/67259e451d5d58b4842776c5696a66d74e157609.patch?full_index=1' -o 14834.patch; 	echo 'ed10a1b254091ad676ed204e55628ecbd6c8962004d6185a1821cedecd526c0f *14834.patch' | sha256sum -c -; 	filterdiff -x '*/NEWS' 14834.patch | patch -p1; 	rm 14834.patch; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Dec 2025 23:48:23 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 23:48:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Dec 2025 23:48:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Dec 2025 23:48:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Dec 2025 23:48:24 GMT
CMD ["php" "-a"]
# Sat, 20 Dec 2025 00:09:03 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Sat, 20 Dec 2025 00:09:03 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Sat, 20 Dec 2025 00:09:03 GMT
WORKDIR /var/www/html
# Sat, 20 Dec 2025 00:09:53 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Sat, 20 Dec 2025 00:09:53 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Sat, 20 Dec 2025 00:09:54 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Sat, 20 Dec 2025 00:09:54 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Sat, 20 Dec 2025 00:09:54 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Sat, 20 Dec 2025 00:09:54 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Sat, 20 Dec 2025 00:09:54 GMT
VOLUME [/var/www/html]
# Sat, 20 Dec 2025 00:09:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 20 Dec 2025 00:09:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 20 Dec 2025 00:09:54 GMT
USER www-data
# Sat, 20 Dec 2025 00:09:54 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:bbedd1c05bb5090fc3fc2356be88d60b2a60937565b56e91fb4be42c5c73d485`  
		Last Modified: Sun, 07 Dec 2025 18:13:29 GMT  
		Size: 3.5 MB (3464704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54a4e4174bdb5b3908bb3628a23a549348e90673f38ba7267ec60bde401efee`  
		Last Modified: Fri, 19 Dec 2025 23:48:38 GMT  
		Size: 3.4 MB (3411348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51869970539db5eac1cb61c5413fb4d8a8dd495b12c141d3299ab834a27effc7`  
		Last Modified: Fri, 19 Dec 2025 23:48:38 GMT  
		Size: 937.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41bcd6beb893bbdcdd68e53785fa7b1185696c52879067ca9d568820dcb5b813`  
		Last Modified: Fri, 19 Dec 2025 23:48:38 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9e59fd208f9d8956ed99f29d921c3ae5f699a73682daf7f4cf1a4d0ea97159c`  
		Last Modified: Fri, 19 Dec 2025 23:48:39 GMT  
		Size: 11.9 MB (11925152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8482476a38f00ae67165d832b775964783cb7140fa947a9896bf18e432c48382`  
		Last Modified: Fri, 19 Dec 2025 23:48:38 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:038f512d16c8303887d10f4150fea873195ab08672e7ce0b0c29bc8efbbafe24`  
		Last Modified: Fri, 19 Dec 2025 23:48:43 GMT  
		Size: 17.1 MB (17079470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c884c239fd8a4b8a08eaf23da6e0bde477bddbe1af23d3c492a40bd909233832`  
		Last Modified: Fri, 19 Dec 2025 23:48:39 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc93bad599d699bee2cc4fd5669076094e2ddf46e0485824a89ff946694ed24`  
		Last Modified: Fri, 19 Dec 2025 23:48:39 GMT  
		Size: 20.0 KB (19965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b8e0b6bb1d9ba7dcda85d4f81d41809fae3a479a93e2e0ac6c5ba0e4578f31`  
		Last Modified: Fri, 19 Dec 2025 23:48:39 GMT  
		Size: 20.0 KB (19960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e7cfd5712d8fb9561bd4969019bbd33f5bdcf85d330d346c4f57a8e2e93cff`  
		Last Modified: Sat, 20 Dec 2025 00:10:13 GMT  
		Size: 11.3 MB (11277238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6073126a7cc0cfbd5a9d1646a04a5dc269329d3c754a31702074b34f9b8d169f`  
		Last Modified: Sat, 20 Dec 2025 00:10:11 GMT  
		Size: 12.3 MB (12328177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc9693a5e2a6c4b151eee8cfd11b9544ef26f73afae2465dcc697d7b808bc95c`  
		Last Modified: Sat, 20 Dec 2025 00:10:10 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbaff09bfa38eba2017978e43fcf4841197f47bd5523b01f95dca94fd64add6`  
		Last Modified: Sat, 20 Dec 2025 00:10:10 GMT  
		Size: 1.5 MB (1524546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1548f7c4ac457b177522d27d52e30102b0e6a393243716e4cdc1850bcf1b8edc`  
		Last Modified: Sat, 20 Dec 2025 00:10:10 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2-php8.1` - unknown; unknown

```console
$ docker pull wordpress@sha256:10689952790e7d14e9d06abd43edbc7d3a0994fd3ae48ea9c9ef66136880d626
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.2 KB (636199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4c9f471242d4c6bec72ebc4bad0a17781d4c14923970ea45540f6c4b81eb993`

```dockerfile
```

-	Layers:
	-	`sha256:5f65fab6f4a36b25c892f97b5235e3445c6fbd2c96b1be31060427f8dbf73568`  
		Last Modified: Sat, 20 Dec 2025 02:16:50 GMT  
		Size: 594.1 KB (594138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ada08b835a95df3880e83de1f5662a2acdd8d632c08f9656e896993647ff57bb`  
		Last Modified: Sat, 20 Dec 2025 02:16:51 GMT  
		Size: 42.1 KB (42061 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:cli-2-php8.1` - linux; ppc64le

```console
$ docker pull wordpress@sha256:d12829ccafb666065c3eab8e4bba8bc20aad422b90a95a6a7f698a643838661e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.0 MB (62967223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38966cef0ba486cecf6d0ed1b8d23f9ab7b5fbcf893fe3df37a6c4ee94440dfc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Sat, 20 Dec 2025 00:04:06 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 20 Dec 2025 00:04:06 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Sat, 20 Dec 2025 00:04:06 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Sat, 20 Dec 2025 00:04:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 20 Dec 2025 00:04:07 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 20 Dec 2025 00:04:07 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 20 Dec 2025 00:04:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 20 Dec 2025 00:04:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 20 Dec 2025 00:04:07 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 20 Dec 2025 00:04:07 GMT
ENV PHP_VERSION=8.1.34
# Sat, 20 Dec 2025 00:04:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.34.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.34.tar.xz.asc
# Sat, 20 Dec 2025 00:04:07 GMT
ENV PHP_SHA256=ffa9e0982e82eeaea848f57687b425ed173aa278fe563001310ae2638db5c251
# Sat, 20 Dec 2025 00:04:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Sat, 20 Dec 2025 00:04:17 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 20 Dec 2025 00:08:00 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		patch 		patchutils 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	curl -fL 'https://github.com/php/php-src/commit/577b8ae4226368e66fee7a9b5c58f9e2428372fc.patch?full_index=1' -o 11678.patch; 	echo '6edc20c3bb3e7cc13515abce7f2fffa8ebea6cf7469abfbc78fcdc120350b239 *11678.patch' | sha256sum -c -; 	patch -p1 < 11678.patch; 	rm 11678.patch; 	curl -fL 'https://github.com/php/php-src/commit/a5df26691d1b1f71b964b869510473a5d5413999.patch?full_index=1' -o 19131.patch; 	echo 'c98c01c74d3a6da197116f8511b16fed361ca6bbb6a8af8df629a933f541c213 *19131.patch' | sha256sum -c -; 	patch --reverse -p1 < 19131.patch; 	rm 19131.patch; 	curl -fL 'https://github.com/php/php-src/commit/67259e451d5d58b4842776c5696a66d74e157609.patch?full_index=1' -o 14834.patch; 	echo 'ed10a1b254091ad676ed204e55628ecbd6c8962004d6185a1821cedecd526c0f *14834.patch' | sha256sum -c -; 	filterdiff -x '*/NEWS' 14834.patch | patch -p1; 	rm 14834.patch; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 20 Dec 2025 00:08:01 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 20 Dec 2025 00:08:02 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 20 Dec 2025 00:08:04 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 20 Dec 2025 00:08:04 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 20 Dec 2025 00:08:04 GMT
CMD ["php" "-a"]
# Sat, 20 Dec 2025 01:09:51 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Sat, 20 Dec 2025 01:09:52 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Sat, 20 Dec 2025 01:09:52 GMT
WORKDIR /var/www/html
# Sat, 20 Dec 2025 01:11:12 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Sat, 20 Dec 2025 01:11:12 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Sat, 20 Dec 2025 01:11:14 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Sat, 20 Dec 2025 01:11:14 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Sat, 20 Dec 2025 01:11:14 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Sat, 20 Dec 2025 01:11:14 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Sat, 20 Dec 2025 01:11:14 GMT
VOLUME [/var/www/html]
# Sat, 20 Dec 2025 01:11:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 20 Dec 2025 01:11:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 20 Dec 2025 01:11:15 GMT
USER www-data
# Sat, 20 Dec 2025 01:11:15 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:e99908f6ead74bb809123fe0d40505509ed6113949496be71629433c6ea3fa1a`  
		Last Modified: Sun, 07 Dec 2025 17:58:56 GMT  
		Size: 3.6 MB (3574075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8234c75cdf8473830bd6b3512561730e81ee79b867090fd2073159b1bddc031b`  
		Last Modified: Sat, 20 Dec 2025 00:08:31 GMT  
		Size: 3.5 MB (3514047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1956d0ce9ac6ee1796e3d5aedf7f8bddae2ad668111123c81bee12693cb3f98`  
		Last Modified: Sat, 20 Dec 2025 00:08:30 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe395c5bdd710299e5c2fc0c342d124306ed28c306010d563e5e04b3adb57f6`  
		Last Modified: Sat, 20 Dec 2025 00:08:31 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3e1037f14e3dd9036390ccf109a5f230ec1dafadd79f5d212965ea206135af`  
		Last Modified: Sat, 20 Dec 2025 00:08:32 GMT  
		Size: 11.9 MB (11925152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84aaa0283012556b1c167c4a608fb3d77cfaeaf3c608cb48768206b57c98c4bf`  
		Last Modified: Sat, 20 Dec 2025 00:08:30 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd023d650fdd8c5a78fcbcd0996e593c7c5ea785b7fa2cf6ff1d72d925679e2b`  
		Last Modified: Sat, 20 Dec 2025 00:08:32 GMT  
		Size: 17.4 MB (17415892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a12cdbfa1d62d31a31bc2b724b8666023641e8c9619778a0229a9d021e960a8`  
		Last Modified: Sat, 20 Dec 2025 00:08:31 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7780a244c75e36e46fe670bd4fefa9b3f17d6ff58003abb540dbf2b2bf72ff3`  
		Last Modified: Sat, 20 Dec 2025 00:08:30 GMT  
		Size: 19.8 KB (19777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:214cb1821fcc50829d6f786826449e2ae6a6c773fe7c35ef3978248d992c280d`  
		Last Modified: Sat, 20 Dec 2025 00:08:31 GMT  
		Size: 19.8 KB (19770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd97344399e5324d92d33293e575ac2720152043b9f45147baff0162a12f60a1`  
		Last Modified: Sat, 20 Dec 2025 01:11:42 GMT  
		Size: 11.7 MB (11685116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1be76b63ca7ebd62e90b12c84398af69c75d18dbcbde115b3738bfc137b154`  
		Last Modified: Sat, 20 Dec 2025 01:11:57 GMT  
		Size: 13.3 MB (13283843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c7204228a9459da7b3e711a8c386541cf3b8ee1d211e8fbd9daaeac7e74286`  
		Last Modified: Sat, 20 Dec 2025 01:11:56 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17fee916ee2f8287ef1c8faaa2321443b5343ccdca832fc15d967015732afdee`  
		Last Modified: Sat, 20 Dec 2025 01:11:56 GMT  
		Size: 1.5 MB (1524592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ec064493c6b8f9bb2fb0cefd16b3caed01367a20b2edb59bbbb0a84fc7f17d`  
		Last Modified: Sat, 20 Dec 2025 01:11:56 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2-php8.1` - unknown; unknown

```console
$ docker pull wordpress@sha256:00089b47ec4f59cb1a9c2d4d87ae8355ccacf957270c5263d35351d15756ed11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.2 KB (633156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d5b1eeafb1066c4e4a1f19bb0872708045533dce67836c425a5966843a7c16d`

```dockerfile
```

-	Layers:
	-	`sha256:4efb8e7e7ec740121af417a725eab5342bbbbe91286d344e71ee69d5f2a93f5e`  
		Last Modified: Sat, 20 Dec 2025 02:16:54 GMT  
		Size: 591.0 KB (591002 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4863cbd0efcfa85ab114c94a9946e30e4aa63829accb0d485d627256f7213f6f`  
		Last Modified: Sat, 20 Dec 2025 02:16:55 GMT  
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
		Last Modified: Tue, 09 Dec 2025 13:48:10 GMT  
		Size: 3.5 MB (3492377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:058411602b31aff80dc2a52786ab3585b8b01a5029568e3b5135401574e8618d`  
		Last Modified: Tue, 09 Dec 2025 13:48:10 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:287d635bbdb57d4de98951a4f3c3c7c37a8517af3c6f9118b910bc76c6421f56`  
		Last Modified: Tue, 09 Dec 2025 13:48:09 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb7912db93521f9252540150dbd0c4988302e21159808a37105c9719c1c2bd9`  
		Last Modified: Tue, 09 Dec 2025 13:48:11 GMT  
		Size: 11.9 MB (11920001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a44b5e0d1562653dc2d36823da12f9e52ef6086e40ba4b66e43779f8d0e046`  
		Last Modified: Tue, 09 Dec 2025 13:48:11 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c351f68a550db4a41135d513f0fb735168b946a3ff13f1d43da8fc20304742`  
		Last Modified: Wed, 10 Dec 2025 22:45:50 GMT  
		Size: 15.8 MB (15799209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e32fcbe0c0c54baf75290199ed86398d324353c8b2381879f82fb80dd404fb`  
		Last Modified: Wed, 10 Dec 2025 22:45:48 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38bb103f1dde1a550b64ec069198772f09df3e2703b6b0909157da4a0e6bc677`  
		Last Modified: Wed, 10 Dec 2025 22:45:46 GMT  
		Size: 19.8 KB (19758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdfb049ffa134d65e94d242f5d48387c5bc8e7bb31830c9b743d6809bfdbf0e1`  
		Last Modified: Wed, 10 Dec 2025 22:45:24 GMT  
		Size: 19.8 KB (19754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f423824eac69b655388d1b3b120e7139ab6ec85bee29fa474de1302d8555d00`  
		Last Modified: Tue, 02 Dec 2025 06:41:19 GMT  
		Size: 11.6 MB (11557552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
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
$ docker pull wordpress@sha256:0ef1dae7bcff353c3711afe0c391d01a64ed20184c3b5987358ecd7ac1c1e5ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.1 MB (63105190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb9e2cfe8bcfb770eaeffbf52f922dbfab5c095738d8d0bfc6b26ba5a149f02e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Fri, 19 Dec 2025 23:48:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Dec 2025 23:48:16 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Dec 2025 23:48:16 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Dec 2025 23:48:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Dec 2025 23:48:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Dec 2025 23:48:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Dec 2025 23:48:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Dec 2025 23:48:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Dec 2025 23:48:16 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 19 Dec 2025 23:48:16 GMT
ENV PHP_VERSION=8.1.34
# Fri, 19 Dec 2025 23:48:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.34.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.34.tar.xz.asc
# Fri, 19 Dec 2025 23:48:16 GMT
ENV PHP_SHA256=ffa9e0982e82eeaea848f57687b425ed173aa278fe563001310ae2638db5c251
# Fri, 19 Dec 2025 23:48:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Dec 2025 23:48:23 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 23:52:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		patch 		patchutils 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	curl -fL 'https://github.com/php/php-src/commit/577b8ae4226368e66fee7a9b5c58f9e2428372fc.patch?full_index=1' -o 11678.patch; 	echo '6edc20c3bb3e7cc13515abce7f2fffa8ebea6cf7469abfbc78fcdc120350b239 *11678.patch' | sha256sum -c -; 	patch -p1 < 11678.patch; 	rm 11678.patch; 	curl -fL 'https://github.com/php/php-src/commit/a5df26691d1b1f71b964b869510473a5d5413999.patch?full_index=1' -o 19131.patch; 	echo 'c98c01c74d3a6da197116f8511b16fed361ca6bbb6a8af8df629a933f541c213 *19131.patch' | sha256sum -c -; 	patch --reverse -p1 < 19131.patch; 	rm 19131.patch; 	curl -fL 'https://github.com/php/php-src/commit/67259e451d5d58b4842776c5696a66d74e157609.patch?full_index=1' -o 14834.patch; 	echo 'ed10a1b254091ad676ed204e55628ecbd6c8962004d6185a1821cedecd526c0f *14834.patch' | sha256sum -c -; 	filterdiff -x '*/NEWS' 14834.patch | patch -p1; 	rm 14834.patch; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Dec 2025 23:52:53 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 23:52:54 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Dec 2025 23:52:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Dec 2025 23:52:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Dec 2025 23:52:55 GMT
CMD ["php" "-a"]
# Sat, 20 Dec 2025 00:05:13 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client # buildkit
# Sat, 20 Dec 2025 00:05:13 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html # buildkit
# Sat, 20 Dec 2025 00:05:13 GMT
WORKDIR /var/www/html
# Sat, 20 Dec 2025 00:06:10 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Sat, 20 Dec 2025 00:06:10 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Sat, 20 Dec 2025 00:06:12 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Sat, 20 Dec 2025 00:06:12 GMT
ENV WORDPRESS_CLI_VERSION=2.12.0
# Sat, 20 Dec 2025 00:06:12 GMT
ENV WORDPRESS_CLI_SHA512=be928f6b8ca1e8dfb9d2f4b75a13aa4aee0896f8a9a0a1c45cd5d2c98605e6172e6d014dda2e27f88c98befc16c040cbb2bd1bfa121510ea5cdf5f6a30fe8832
# Sat, 20 Dec 2025 00:06:12 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version # buildkit
# Sat, 20 Dec 2025 00:06:12 GMT
VOLUME [/var/www/html]
# Sat, 20 Dec 2025 00:06:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 20 Dec 2025 00:06:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 20 Dec 2025 00:06:12 GMT
USER www-data
# Sat, 20 Dec 2025 00:06:12 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:9f2ceebb28b6c8480d6ae26501eda06bf0b6029f7c797c80673b95a60276e050`  
		Last Modified: Sun, 07 Dec 2025 17:58:56 GMT  
		Size: 3.5 MB (3466434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c995452a6f3b5884334d0bcef1538883087a008b2c57c3c5066efa9f7e9aed2`  
		Last Modified: Fri, 19 Dec 2025 23:53:13 GMT  
		Size: 3.6 MB (3597069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b6b815032520b7639ad5f9b01780201cfeb726de5b05d9444613a4460256aff`  
		Last Modified: Fri, 19 Dec 2025 23:53:13 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9ca55d47f504e81b31d97fea6b43923f5e06076344e5048d4f415b02454313d`  
		Last Modified: Fri, 19 Dec 2025 23:53:13 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:424c960a966b75d54654646d5203f5b09bf5849e50bf909ed80c112de2472195`  
		Last Modified: Fri, 19 Dec 2025 23:53:14 GMT  
		Size: 11.9 MB (11925152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3de39b51f0fea58170ede6781831ed5cdd8bbaa5e40f84d639714b038ac6aee`  
		Last Modified: Fri, 19 Dec 2025 23:53:13 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f3639761aa275232097fcc1c4dbdc4b0fb51abb4322f4f327adfc9ab4e7e0b`  
		Last Modified: Fri, 19 Dec 2025 23:53:14 GMT  
		Size: 16.7 MB (16706953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54e92ad6d65fc8f2e5c24b4b8cc377a0d20896d43943a257114438b9559fb5f`  
		Last Modified: Fri, 19 Dec 2025 23:53:13 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea7fc6954b8dbc952b74d4bc9d1a8b758c075a6d50f1a90e765d25b25b1bd5c`  
		Last Modified: Fri, 19 Dec 2025 23:53:13 GMT  
		Size: 19.8 KB (19782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa2987012e517f55dd2ccafae371bf267eda2b405da3970339384eab0a70963`  
		Last Modified: Fri, 19 Dec 2025 23:53:17 GMT  
		Size: 19.8 KB (19771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:956c7eeb5361f14ae48aa3a07cefe3ba4d5d6f9d02b9d318c7d804036d8f2e3f`  
		Last Modified: Sat, 20 Dec 2025 00:06:35 GMT  
		Size: 12.4 MB (12433632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3876ebfd317e5480664e9436e77646a74cb14624005b84b51308d7d518c9aa61`  
		Last Modified: Sat, 20 Dec 2025 00:06:34 GMT  
		Size: 13.4 MB (13406879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3629fecf4234a7817196af94e946d61f185fc2bc09276a3be80c30a10264ce44`  
		Last Modified: Sat, 20 Dec 2025 00:06:33 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c380684c2f350d4ab3a33f68cf685efd4acb20ba8a821c064e1bcd5baf6e22a`  
		Last Modified: Sat, 20 Dec 2025 00:06:36 GMT  
		Size: 1.5 MB (1524577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d55b1939a66ea47860d4f4ab0922385462c97687cf3ee5d1c516366048e4618`  
		Last Modified: Sat, 20 Dec 2025 00:06:33 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:cli-2-php8.1` - unknown; unknown

```console
$ docker pull wordpress@sha256:9494c8d50e948f53d7162e856d8c073ad4c0822ffba7f98814a2eef99f7036f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.1 KB (633068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eb099b2c5b247927af03c33548d297f2e0db389a6d024f4133feb453aa9b6a6`

```dockerfile
```

-	Layers:
	-	`sha256:34868d01de00ce9cad4750740761bed2be03582dae4cd111ad488e7c755ecc66`  
		Last Modified: Sat, 20 Dec 2025 02:17:02 GMT  
		Size: 591.0 KB (590968 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89455ffe5c428b982be9a23997f3b0efda70b15db1ef006e5b630b614d984549`  
		Last Modified: Sat, 20 Dec 2025 02:17:02 GMT  
		Size: 42.1 KB (42100 bytes)  
		MIME: application/vnd.in-toto+json
