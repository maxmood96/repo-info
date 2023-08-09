## `wordpress:cli-2.8.1-php8.2`

```console
$ docker pull wordpress@sha256:4b10f0c4e5f0936beb672b2485f9339076d9522e932250abdab3d8f86267770b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `wordpress:cli-2.8.1-php8.2` - linux; amd64

```console
$ docker pull wordpress@sha256:d4a3f210963a7d005d31a39b6d8bb4b8a153cb681cb90e5f0e8ac139bdb0e664
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.5 MB (64544527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e413cabb3f0822c0922b4ccd4c4c9648af0abf4ec595041b87b4a0fdb7355f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 00:31:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 Jun 2023 00:31:26 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 15 Jun 2023 00:31:26 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 15 Jun 2023 00:31:26 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 Jun 2023 00:31:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 15 Jun 2023 00:31:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jun 2023 00:31:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jun 2023 00:31:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 Jun 2023 00:54:34 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Mon, 10 Jul 2023 22:18:20 GMT
ENV PHP_VERSION=8.2.8
# Mon, 10 Jul 2023 22:18:20 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.8.tar.xz.asc
# Mon, 10 Jul 2023 22:18:20 GMT
ENV PHP_SHA256=cfe1055fbcd486de7d3312da6146949aae577365808790af6018205567609801
# Mon, 10 Jul 2023 22:18:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Mon, 10 Jul 2023 22:18:27 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Mon, 10 Jul 2023 22:21:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Mon, 10 Jul 2023 22:21:54 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Mon, 10 Jul 2023 22:21:55 GMT
RUN docker-php-ext-enable sodium
# Mon, 10 Jul 2023 22:21:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 10 Jul 2023 22:21:55 GMT
CMD ["php" "-a"]
# Tue, 11 Jul 2023 03:55:53 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client
# Tue, 11 Jul 2023 03:55:54 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html
# Tue, 11 Jul 2023 03:55:54 GMT
WORKDIR /var/www/html
# Tue, 11 Jul 2023 03:56:50 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Tue, 11 Jul 2023 03:56:50 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Tue, 11 Jul 2023 03:56:50 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Tue, 11 Jul 2023 03:56:50 GMT
ENV WORDPRESS_CLI_VERSION=2.8.1
# Tue, 11 Jul 2023 03:56:51 GMT
ENV WORDPRESS_CLI_SHA512=c1d40ee90b330ca1f8ddbed14b938b41ec5d9ff723c7c1cf3f41a2d9a1b271079a51a37ea3d1c9aa9c628fdd43449dba3995a8de150a68abbd505b06b91d9d2b
# Tue, 11 Jul 2023 03:56:53 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version
# Tue, 11 Jul 2023 03:56:53 GMT
VOLUME [/var/www/html]
# Tue, 11 Jul 2023 03:56:53 GMT
COPY file:b6efa5ff0423d61c2df0c8941b896844a8272d8516cdda0fcae8daaf56baac18 in /usr/local/bin/ 
# Tue, 11 Jul 2023 03:56:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 03:56:53 GMT
USER www-data
# Tue, 11 Jul 2023 03:56:53 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f034080c2b5d3afb2ec354e2b425f48df6326f28bcf3d2cee4ed50b9721ba482`  
		Last Modified: Thu, 15 Jun 2023 02:07:05 GMT  
		Size: 2.7 MB (2659635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b8701d6f7d5844dd4fa64c17ce3e1999f152f0dbfa3ea704bf38e8617e6b4d5`  
		Last Modified: Thu, 15 Jun 2023 02:07:05 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:259e9197ff8b826653ac60962d424d223ae725c1368f3fbd6efe6853200e945c`  
		Last Modified: Thu, 15 Jun 2023 02:07:04 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2392abb1ba7637b75a33ff6d92da9b21e06ad93e287aa70395423e70ab9cb71`  
		Last Modified: Mon, 10 Jul 2023 23:52:53 GMT  
		Size: 12.1 MB (12055821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d702db174c5d175eb9525ed88eece39997c57f2f6bc82af1ba9ae7f458ad04b0`  
		Last Modified: Mon, 10 Jul 2023 23:52:53 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5788a92b08ccf6093b9b035cd4bedac253f01539f0965c5244395a4e75d66ae7`  
		Last Modified: Mon, 10 Jul 2023 23:52:55 GMT  
		Size: 16.8 MB (16755941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f837013f4dd7d7bcb0994c5a50e6da607b0eaf5f5c35aadc6e8bfba2fcb5c34`  
		Last Modified: Mon, 10 Jul 2023 23:52:53 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ea37a3bff824c19f95eecb679aab7c49a8560f29b26b1f141773882c3665ba`  
		Last Modified: Mon, 10 Jul 2023 23:52:53 GMT  
		Size: 18.9 KB (18938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6df37289eac7c87ff3b4e85ee6875863e65614978c5bcfe33471f838ede0249`  
		Last Modified: Tue, 11 Jul 2023 04:02:05 GMT  
		Size: 19.3 MB (19271168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdcc23112a8c84df5a602fa30dffc737be918997d5f5a13cefe808a153b5e030`  
		Last Modified: Thu, 15 Jun 2023 08:23:46 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b306a0548963538699f45cb772255bfb2f75c63dce90b49666186ab2336f85e`  
		Last Modified: Tue, 11 Jul 2023 04:02:02 GMT  
		Size: 8.9 MB (8866636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf3e11f05e52083ec90bf82bf7ab5a3d0527a5574ed9f3514d7f3f2128d1449`  
		Last Modified: Tue, 11 Jul 2023 04:02:02 GMT  
		Size: 388.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2fd6af8396ad19e6d800b9687d71fb25e46d20f3bca48e7bc4408701231e5a`  
		Last Modified: Tue, 11 Jul 2023 04:02:01 GMT  
		Size: 1.5 MB (1513096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2098b984c6a0d962c933a95405475858efd28788cde3e76ad34dfbd3652d7e20`  
		Last Modified: Tue, 11 Jul 2023 04:02:01 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:cli-2.8.1-php8.2` - linux; arm variant v6

```console
$ docker pull wordpress@sha256:27dcfe3e1d5ed83a3e8645bbf5fd2e5b2c0047707f54e3d7b98d103a64fa1104
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61589113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a27f3ef9b37b57cdc51cf850b6c0a4b45c895c5aa2f2feaee647369b5cedd374`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:14 GMT
ADD file:9882e99e5f94ab2db05c029648ac5be7cf0f063a8701394fcbb543a7ef5d4b90 in / 
# Mon, 07 Aug 2023 19:49:15 GMT
CMD ["/bin/sh"]
# Wed, 09 Aug 2023 00:06:11 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 09 Aug 2023 00:06:12 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 09 Aug 2023 00:06:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 09 Aug 2023 00:06:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 09 Aug 2023 00:06:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 09 Aug 2023 00:06:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 09 Aug 2023 00:06:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 09 Aug 2023 00:06:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 09 Aug 2023 00:24:44 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 09 Aug 2023 00:42:48 GMT
ENV PHP_VERSION=8.2.8
# Wed, 09 Aug 2023 00:42:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.8.tar.xz.asc
# Wed, 09 Aug 2023 00:42:48 GMT
ENV PHP_SHA256=cfe1055fbcd486de7d3312da6146949aae577365808790af6018205567609801
# Wed, 09 Aug 2023 00:42:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 09 Aug 2023 00:42:56 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 09 Aug 2023 00:45:29 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 09 Aug 2023 00:45:29 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Wed, 09 Aug 2023 00:45:30 GMT
RUN docker-php-ext-enable sodium
# Wed, 09 Aug 2023 00:45:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 09 Aug 2023 00:45:30 GMT
CMD ["php" "-a"]
# Wed, 09 Aug 2023 04:32:05 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client
# Wed, 09 Aug 2023 04:32:06 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html
# Wed, 09 Aug 2023 04:32:06 GMT
WORKDIR /var/www/html
# Wed, 09 Aug 2023 04:33:01 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Wed, 09 Aug 2023 04:33:02 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Wed, 09 Aug 2023 04:33:02 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Wed, 09 Aug 2023 04:33:02 GMT
ENV WORDPRESS_CLI_VERSION=2.8.1
# Wed, 09 Aug 2023 04:33:02 GMT
ENV WORDPRESS_CLI_SHA512=c1d40ee90b330ca1f8ddbed14b938b41ec5d9ff723c7c1cf3f41a2d9a1b271079a51a37ea3d1c9aa9c628fdd43449dba3995a8de150a68abbd505b06b91d9d2b
# Wed, 09 Aug 2023 04:33:04 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version
# Wed, 09 Aug 2023 04:33:05 GMT
VOLUME [/var/www/html]
# Wed, 09 Aug 2023 04:33:05 GMT
COPY file:b6efa5ff0423d61c2df0c8941b896844a8272d8516cdda0fcae8daaf56baac18 in /usr/local/bin/ 
# Wed, 09 Aug 2023 04:33:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Aug 2023 04:33:05 GMT
USER www-data
# Wed, 09 Aug 2023 04:33:05 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:af09961d4a43b504efc76e38b50918977c28be73eeb8b926247783a00e8b9f2f`  
		Last Modified: Mon, 07 Aug 2023 19:49:38 GMT  
		Size: 3.1 MB (3144809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c86f23b6f54d6e2a8ad7bd169a67e8c3b546cb7f2a7f2a6a59b252b11a54fd64`  
		Last Modified: Wed, 09 Aug 2023 01:35:32 GMT  
		Size: 2.7 MB (2666341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5831210199409c627f51822ba56a05e076469f5375f7841904326dd9ae6c8c3e`  
		Last Modified: Wed, 09 Aug 2023 01:35:31 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b818ba6e6fe1abab346c1e22bac5a61390d2b9d0909558a79ce40dac5f44e82e`  
		Last Modified: Wed, 09 Aug 2023 01:35:31 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1cfd8dbf828bbe0ed959fcb7ea32087fb564911e8d09d14d86b334584cae463`  
		Last Modified: Wed, 09 Aug 2023 01:38:43 GMT  
		Size: 12.1 MB (12055820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc68d84957095e9edd32c73299dff4a5a6fc7e8af477d38a77c6b283a96c98aa`  
		Last Modified: Wed, 09 Aug 2023 01:38:42 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a969ecd846d86f1f806aeebf6b43b12a1c5985030996251cc5648ddc1a818e00`  
		Last Modified: Wed, 09 Aug 2023 01:38:45 GMT  
		Size: 15.3 MB (15339314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d573fe2286ed254d742c75597fe5da544e97ec7cd865ad9e867f38dddd5cb0`  
		Last Modified: Wed, 09 Aug 2023 01:38:42 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ebaabf1d9d43023c331cbba1a6c70b2f9ecb8510f0ae14e2dca0456ccb83232`  
		Last Modified: Wed, 09 Aug 2023 01:38:42 GMT  
		Size: 18.7 KB (18742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aa7d51b0318248d4cae215078fbe55628ff5e4b2f281e80a0a1245b65fd0612`  
		Last Modified: Wed, 09 Aug 2023 04:36:07 GMT  
		Size: 18.4 MB (18368884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fa99a58cb24208f07d18866a42f967f15377274ec6ced4b27dbf0c9926c939b`  
		Last Modified: Wed, 09 Aug 2023 04:35:42 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddf154a566d5067bf84550b2b2408d1625a91239843557303ce7f562b9b4c1d1`  
		Last Modified: Wed, 09 Aug 2023 04:36:04 GMT  
		Size: 8.5 MB (8476700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a3488755bfabcd5373a2de38cbac12930c9c625be68145e9931c9c2ca1318fb`  
		Last Modified: Wed, 09 Aug 2023 04:36:03 GMT  
		Size: 392.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35b7ae392457ff936e725cf7144b6b08ce4cdc342d6decdc720f8de73129a705`  
		Last Modified: Wed, 09 Aug 2023 04:36:03 GMT  
		Size: 1.5 MB (1513092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:189b6bf510da7df4b995a2b433ef1b5bf308f7c9f76493b5f84d1cb7a7efde1a`  
		Last Modified: Wed, 09 Aug 2023 04:36:03 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:cli-2.8.1-php8.2` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:466dcfe03d395c635e388303cdbc3ae3019e370f17e13d3c3ae945cb88ddca73
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59456753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1fdc2130600f016fca526acc228b4642cbc5f5f1f8eb36e9cf1cac46145991c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Mon, 07 Aug 2023 19:57:25 GMT
ADD file:e3f56488d3d3bb67729714db13ddadf6652e7efb5281cfc7010d3e71f9d6607f in / 
# Mon, 07 Aug 2023 19:57:25 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 23:45:01 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 07 Aug 2023 23:45:02 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Mon, 07 Aug 2023 23:45:03 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Mon, 07 Aug 2023 23:45:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 07 Aug 2023 23:45:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Mon, 07 Aug 2023 23:45:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Aug 2023 23:45:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Aug 2023 23:45:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 08 Aug 2023 00:01:01 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Tue, 08 Aug 2023 00:16:46 GMT
ENV PHP_VERSION=8.2.8
# Tue, 08 Aug 2023 00:16:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.8.tar.xz.asc
# Tue, 08 Aug 2023 00:16:46 GMT
ENV PHP_SHA256=cfe1055fbcd486de7d3312da6146949aae577365808790af6018205567609801
# Tue, 08 Aug 2023 00:16:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 08 Aug 2023 00:16:53 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 08 Aug 2023 00:19:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 08 Aug 2023 00:19:13 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Tue, 08 Aug 2023 00:19:14 GMT
RUN docker-php-ext-enable sodium
# Tue, 08 Aug 2023 00:19:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 08 Aug 2023 00:19:14 GMT
CMD ["php" "-a"]
# Tue, 08 Aug 2023 05:54:08 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client
# Tue, 08 Aug 2023 05:54:08 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html
# Tue, 08 Aug 2023 05:54:08 GMT
WORKDIR /var/www/html
# Tue, 08 Aug 2023 05:55:02 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Tue, 08 Aug 2023 05:55:02 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Tue, 08 Aug 2023 05:55:02 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Tue, 08 Aug 2023 05:55:03 GMT
ENV WORDPRESS_CLI_VERSION=2.8.1
# Tue, 08 Aug 2023 05:55:03 GMT
ENV WORDPRESS_CLI_SHA512=c1d40ee90b330ca1f8ddbed14b938b41ec5d9ff723c7c1cf3f41a2d9a1b271079a51a37ea3d1c9aa9c628fdd43449dba3995a8de150a68abbd505b06b91d9d2b
# Tue, 08 Aug 2023 05:55:05 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version
# Tue, 08 Aug 2023 05:55:05 GMT
VOLUME [/var/www/html]
# Tue, 08 Aug 2023 05:55:05 GMT
COPY file:b6efa5ff0423d61c2df0c8941b896844a8272d8516cdda0fcae8daaf56baac18 in /usr/local/bin/ 
# Tue, 08 Aug 2023 05:55:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Aug 2023 05:55:06 GMT
USER www-data
# Tue, 08 Aug 2023 05:55:06 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:f8dec92eec42224ef9e6ca9c6207ea6b9195dcf93d06bd5ceff0f814b62bf064`  
		Last Modified: Mon, 07 Aug 2023 19:57:55 GMT  
		Size: 2.9 MB (2899480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c53730165c5dd25f49dfa5e188b41f8d9be86e5e86adf6c765ceb1120853f36`  
		Last Modified: Tue, 08 Aug 2023 01:08:04 GMT  
		Size: 2.5 MB (2506232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10cb15fb50aac58af758965db75571d10382d95341fb109bee5260d370560772`  
		Last Modified: Tue, 08 Aug 2023 01:08:02 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe5f5b7d39cd3a05f25820f07393ecbd138724348b5cf7a7be272495f109290`  
		Last Modified: Tue, 08 Aug 2023 01:08:03 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66ee51d65203f67afa9d2a8782fcb8a8b22452578a619b7e273af6e9fc70c39f`  
		Last Modified: Tue, 08 Aug 2023 01:12:03 GMT  
		Size: 12.1 MB (12055827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:948a61c923c1739cea9e60cff8f3b52e1c1478581776ccb8e8bac0ef1b286eee`  
		Last Modified: Tue, 08 Aug 2023 01:12:02 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24418c9fad8f5137c7fcf5ab9e418fbef959c00c862f05a808ec1313815a42d2`  
		Last Modified: Tue, 08 Aug 2023 01:12:04 GMT  
		Size: 14.3 MB (14326479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1ae48480b508c3850ba8345a250ae4a604bc71a4377c6dd0ad547fca198cf31`  
		Last Modified: Tue, 08 Aug 2023 01:12:01 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3980e928586ab2dcd64a3ba04a938a40d1feaa2f39c483c991618f5bbd816bd5`  
		Last Modified: Tue, 08 Aug 2023 01:12:01 GMT  
		Size: 18.8 KB (18760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1f612bc9bbd7726358cf6b049fe1eaba86188a84696783774ac42109a3cd846`  
		Last Modified: Tue, 08 Aug 2023 06:00:08 GMT  
		Size: 17.9 MB (17942493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ced5a0043690c36123c8a0e11bfb2fe1bec66ffbaa76e0defd31e280fc7131a`  
		Last Modified: Tue, 08 Aug 2023 05:59:41 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f899d6c7a43fdd1ea8edc1d1a0b51e87e25f351d1822f3d72e8e9d8d5a48fc7a`  
		Last Modified: Tue, 08 Aug 2023 06:00:05 GMT  
		Size: 8.2 MB (8188981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f326dc337ef2068e4e21e1d05aa56ca019bcac101aca72ea4baebf7b7b359e7a`  
		Last Modified: Tue, 08 Aug 2023 06:00:03 GMT  
		Size: 391.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c56dff833aa0777434d78828fc79764dba00ee354e2ee25a009c31b71cd211`  
		Last Modified: Tue, 08 Aug 2023 06:00:04 GMT  
		Size: 1.5 MB (1513092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44cdccd4f229197d8884581407a37b0c1c3a03ab05399d30fcde978c56a1407a`  
		Last Modified: Tue, 08 Aug 2023 06:00:04 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:cli-2.8.1-php8.2` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:edacab9dbd276714c10bd3531318cd979fe75910c8c4bf70b9552fd8128b692f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64878988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8954d083521ec2d382a342e28cc7dc98f2bacc29f9dbf40e0b7a594d1a3ffa62`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 03:05:37 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 Jun 2023 03:05:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 15 Jun 2023 03:05:39 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 15 Jun 2023 03:05:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 Jun 2023 03:05:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 15 Jun 2023 03:05:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jun 2023 03:05:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jun 2023 03:05:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 Jun 2023 03:30:20 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Mon, 10 Jul 2023 23:02:37 GMT
ENV PHP_VERSION=8.2.8
# Mon, 10 Jul 2023 23:02:37 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.8.tar.xz.asc
# Mon, 10 Jul 2023 23:02:37 GMT
ENV PHP_SHA256=cfe1055fbcd486de7d3312da6146949aae577365808790af6018205567609801
# Mon, 10 Jul 2023 23:02:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Mon, 10 Jul 2023 23:02:44 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Mon, 10 Jul 2023 23:06:07 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Mon, 10 Jul 2023 23:06:08 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Mon, 10 Jul 2023 23:06:08 GMT
RUN docker-php-ext-enable sodium
# Mon, 10 Jul 2023 23:06:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 10 Jul 2023 23:06:09 GMT
CMD ["php" "-a"]
# Tue, 11 Jul 2023 04:20:49 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client
# Tue, 11 Jul 2023 04:20:49 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html
# Tue, 11 Jul 2023 04:20:49 GMT
WORKDIR /var/www/html
# Tue, 11 Jul 2023 04:21:39 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Tue, 11 Jul 2023 04:21:39 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Tue, 11 Jul 2023 04:21:39 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Tue, 11 Jul 2023 04:21:39 GMT
ENV WORDPRESS_CLI_VERSION=2.8.1
# Tue, 11 Jul 2023 04:21:39 GMT
ENV WORDPRESS_CLI_SHA512=c1d40ee90b330ca1f8ddbed14b938b41ec5d9ff723c7c1cf3f41a2d9a1b271079a51a37ea3d1c9aa9c628fdd43449dba3995a8de150a68abbd505b06b91d9d2b
# Tue, 11 Jul 2023 04:21:42 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version
# Tue, 11 Jul 2023 04:21:42 GMT
VOLUME [/var/www/html]
# Tue, 11 Jul 2023 04:21:42 GMT
COPY file:b6efa5ff0423d61c2df0c8941b896844a8272d8516cdda0fcae8daaf56baac18 in /usr/local/bin/ 
# Tue, 11 Jul 2023 04:21:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 04:21:42 GMT
USER www-data
# Tue, 11 Jul 2023 04:21:42 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68cbf4f33af4ff20fa90638cea5f48dda44f171afe80c0ca68a40b5c67ee1102`  
		Last Modified: Thu, 15 Jun 2023 04:39:12 GMT  
		Size: 2.7 MB (2696456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0262450c79d37bc5398bf1154c4bb2681100ef9caf7e008c5d0bd06c3d840a7`  
		Last Modified: Thu, 15 Jun 2023 04:39:11 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ca0f0b2514d4e2b8323c60eece66557c89959c380362deb6862fe5ffe3ad14`  
		Last Modified: Thu, 15 Jun 2023 04:39:11 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc9f367bc792d1e117225a211e2e4ae1221cc48c2a09615e05b0f75b630daff`  
		Last Modified: Tue, 11 Jul 2023 00:34:42 GMT  
		Size: 12.1 MB (12055813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e16d2a5e0aa3b2bb7f74ad466170e87dd144390e777cae42042bb91586e7e6`  
		Last Modified: Tue, 11 Jul 2023 00:34:41 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:710c3d1457f2f3537250bc44c71f80e61df86753a13f3cf5838c041b3d6b0170`  
		Last Modified: Tue, 11 Jul 2023 00:34:44 GMT  
		Size: 16.7 MB (16738378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:959d1a9ee254accc71807e64320df1e637f0f61ccaf7cdbf7b85ba82c1c6fd6d`  
		Last Modified: Tue, 11 Jul 2023 00:34:41 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638d744e6a4e82fac17b46a5d1136a6a0655d7749917728af084570ae40240f6`  
		Last Modified: Tue, 11 Jul 2023 00:34:41 GMT  
		Size: 18.7 KB (18707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f13027a96211fe19e877ceafb18869b89eb71a9d1f2af796539e7af49741ee`  
		Last Modified: Tue, 11 Jul 2023 04:26:28 GMT  
		Size: 19.7 MB (19686140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018acf6a00be1098ad14fddde1ce7c63cc4c9e7af96f77b9ad185aef95bf56d6`  
		Last Modified: Thu, 15 Jun 2023 09:21:03 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1e95d7ed73e6e1a8727331561bd88bacdaf599038dd1eb226b1890544379842`  
		Last Modified: Tue, 11 Jul 2023 04:26:26 GMT  
		Size: 8.8 MB (8835790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4d613f84833834024f4904159248f25f7e6e6d051cf6251210fe5c88261180a`  
		Last Modified: Tue, 11 Jul 2023 04:26:25 GMT  
		Size: 388.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f4264d095d2b56d5eeb7cad335f7cd4726f49e528ffe2beb2289ea3535e4928`  
		Last Modified: Tue, 11 Jul 2023 04:26:25 GMT  
		Size: 1.5 MB (1513045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b3f734a58286246cef3e59857b0ec3f532028e5ff448813ca5a20d6a5711256`  
		Last Modified: Tue, 11 Jul 2023 04:26:24 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:cli-2.8.1-php8.2` - linux; 386

```console
$ docker pull wordpress@sha256:b259e445acd793de6ee5ceb8f5373409c06e66eb0e90dd1883c27165e192c95c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64175481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63844e2e47c7cfe44cac1481abfd086f87b6eed1a8bed399fe5e73eb5e8342af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Mon, 07 Aug 2023 19:38:26 GMT
ADD file:4b33c52e11b19fde30197c62ead0b77bde28d34edaa08346a5302cd892d3cebe in / 
# Mon, 07 Aug 2023 19:38:27 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 23:13:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 08 Aug 2023 23:13:24 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 08 Aug 2023 23:13:24 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 08 Aug 2023 23:13:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 08 Aug 2023 23:13:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 08 Aug 2023 23:13:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 08 Aug 2023 23:13:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 08 Aug 2023 23:13:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 08 Aug 2023 23:51:54 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 09 Aug 2023 00:29:56 GMT
ENV PHP_VERSION=8.2.8
# Wed, 09 Aug 2023 00:29:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.8.tar.xz.asc
# Wed, 09 Aug 2023 00:29:56 GMT
ENV PHP_SHA256=cfe1055fbcd486de7d3312da6146949aae577365808790af6018205567609801
# Wed, 09 Aug 2023 00:30:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 09 Aug 2023 00:30:04 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 09 Aug 2023 00:36:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 09 Aug 2023 00:36:13 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Wed, 09 Aug 2023 00:36:14 GMT
RUN docker-php-ext-enable sodium
# Wed, 09 Aug 2023 00:36:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 09 Aug 2023 00:36:14 GMT
CMD ["php" "-a"]
# Wed, 09 Aug 2023 08:44:26 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client
# Wed, 09 Aug 2023 08:44:27 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html
# Wed, 09 Aug 2023 08:44:27 GMT
WORKDIR /var/www/html
# Wed, 09 Aug 2023 08:45:36 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Wed, 09 Aug 2023 08:45:36 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Wed, 09 Aug 2023 08:45:37 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Wed, 09 Aug 2023 08:45:37 GMT
ENV WORDPRESS_CLI_VERSION=2.8.1
# Wed, 09 Aug 2023 08:45:37 GMT
ENV WORDPRESS_CLI_SHA512=c1d40ee90b330ca1f8ddbed14b938b41ec5d9ff723c7c1cf3f41a2d9a1b271079a51a37ea3d1c9aa9c628fdd43449dba3995a8de150a68abbd505b06b91d9d2b
# Wed, 09 Aug 2023 08:45:39 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version
# Wed, 09 Aug 2023 08:45:40 GMT
VOLUME [/var/www/html]
# Wed, 09 Aug 2023 08:45:40 GMT
COPY file:b6efa5ff0423d61c2df0c8941b896844a8272d8516cdda0fcae8daaf56baac18 in /usr/local/bin/ 
# Wed, 09 Aug 2023 08:45:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Aug 2023 08:45:40 GMT
USER www-data
# Wed, 09 Aug 2023 08:45:40 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:95dc695758361a4038a2d9026959d72e1f531114edb0341be7ce47d912ef069e`  
		Last Modified: Mon, 07 Aug 2023 19:38:56 GMT  
		Size: 3.2 MB (3235144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7b2187279b62839adee215aff0a17bafb09ccd31d0570c33d4e98042a183874`  
		Last Modified: Wed, 09 Aug 2023 03:11:03 GMT  
		Size: 2.7 MB (2702127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5141c6405baaddb270a3c61e413a7537d8dbc121079b59d34890bcc5924823d3`  
		Last Modified: Wed, 09 Aug 2023 03:11:02 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b100920b232fdc449e8cff1b9c496bf2866fe12c32e7153b97d586e7d2d609`  
		Last Modified: Wed, 09 Aug 2023 03:11:02 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8550b67f90ac511f8a355c4b4df40f82b531cf31dbd46b99819ebcdd24918734`  
		Last Modified: Wed, 09 Aug 2023 03:15:07 GMT  
		Size: 12.1 MB (12055824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675d3f72d1dda6333a7a4e70fa582f988dc2f9ef49cae942cc111b998a6f7d26`  
		Last Modified: Wed, 09 Aug 2023 03:15:06 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a731de6218eddfe0fbbcae26b212b8df32d6bf0c8957a5c06c13c1ae17b27db`  
		Last Modified: Wed, 09 Aug 2023 03:15:10 GMT  
		Size: 17.0 MB (17035894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7a1093478db90fa82e378d2da49c54284729dd8c33fe6c34b82f051a6441c5`  
		Last Modified: Wed, 09 Aug 2023 03:15:06 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0def522e67d1247cbdea55bed0025024d655a37ff76387dcb32be86a127d5712`  
		Last Modified: Wed, 09 Aug 2023 03:15:06 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b42ecb581590d792477e05d22b53300c02cdebf630a55c6f78a48b06431ba13`  
		Last Modified: Wed, 09 Aug 2023 08:51:41 GMT  
		Size: 18.7 MB (18673766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17591721747b180bf4666112e16840762775c3013121933318b9c843d8a55430`  
		Last Modified: Wed, 09 Aug 2023 08:51:15 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08f70c2d23536ecfe51f02850d63e41f3ce450f92c672c21e427b9f60f50550c`  
		Last Modified: Wed, 09 Aug 2023 08:51:38 GMT  
		Size: 8.9 MB (8935308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b594f59e9dda9125b75fbf1efe5986e3144d95ee93c2b3bd94732540f19bffa0`  
		Last Modified: Wed, 09 Aug 2023 08:51:36 GMT  
		Size: 391.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d76084f0488af99c8437119f945ffd3dcc854a23cb9486e07586fc3be095499`  
		Last Modified: Wed, 09 Aug 2023 08:51:37 GMT  
		Size: 1.5 MB (1513082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87797e25839cd96ba07842e3f02fbc66016fa7d977162c3c454efea15ca35534`  
		Last Modified: Wed, 09 Aug 2023 08:51:36 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:cli-2.8.1-php8.2` - linux; ppc64le

```console
$ docker pull wordpress@sha256:c2a13d1593003c0cff0908a4f908e47fe22cbd151564606f2883dbc5f06122d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.1 MB (66077051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc079c91266dcfa29989929750a45c2b96ef7a831c65be2d38d41f04d8bf9b2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Thu, 15 Jun 2023 00:39:49 GMT
ADD file:694c636c0dd19fd01accbc189e4c1dc4d063952692c6e7eb26dce02a7adba833 in / 
# Thu, 15 Jun 2023 00:39:49 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 02:20:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 Jun 2023 02:20:19 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 15 Jun 2023 02:20:20 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 15 Jun 2023 02:20:20 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 Jun 2023 02:20:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 15 Jun 2023 02:20:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jun 2023 02:20:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jun 2023 02:20:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 Jun 2023 02:46:03 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Mon, 10 Jul 2023 23:35:05 GMT
ENV PHP_VERSION=8.2.8
# Mon, 10 Jul 2023 23:35:05 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.8.tar.xz.asc
# Mon, 10 Jul 2023 23:35:06 GMT
ENV PHP_SHA256=cfe1055fbcd486de7d3312da6146949aae577365808790af6018205567609801
# Mon, 10 Jul 2023 23:35:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Mon, 10 Jul 2023 23:35:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Mon, 10 Jul 2023 23:39:18 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Mon, 10 Jul 2023 23:39:20 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Mon, 10 Jul 2023 23:39:23 GMT
RUN docker-php-ext-enable sodium
# Mon, 10 Jul 2023 23:39:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 10 Jul 2023 23:39:25 GMT
CMD ["php" "-a"]
# Tue, 11 Jul 2023 07:22:21 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client
# Tue, 11 Jul 2023 07:22:24 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html
# Tue, 11 Jul 2023 07:22:25 GMT
WORKDIR /var/www/html
# Tue, 11 Jul 2023 07:24:08 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Tue, 11 Jul 2023 07:24:10 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Tue, 11 Jul 2023 07:24:10 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Tue, 11 Jul 2023 07:24:11 GMT
ENV WORDPRESS_CLI_VERSION=2.8.1
# Tue, 11 Jul 2023 07:24:11 GMT
ENV WORDPRESS_CLI_SHA512=c1d40ee90b330ca1f8ddbed14b938b41ec5d9ff723c7c1cf3f41a2d9a1b271079a51a37ea3d1c9aa9c628fdd43449dba3995a8de150a68abbd505b06b91d9d2b
# Tue, 11 Jul 2023 07:24:16 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version
# Tue, 11 Jul 2023 07:24:17 GMT
VOLUME [/var/www/html]
# Tue, 11 Jul 2023 07:24:18 GMT
COPY file:b6efa5ff0423d61c2df0c8941b896844a8272d8516cdda0fcae8daaf56baac18 in /usr/local/bin/ 
# Tue, 11 Jul 2023 07:24:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 07:24:19 GMT
USER www-data
# Tue, 11 Jul 2023 07:24:19 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:ffa4a466dbb8eebd7e7f25590a9df12390de9016abf82279c29c9a64aa76491a`  
		Last Modified: Thu, 15 Jun 2023 00:40:26 GMT  
		Size: 3.3 MB (3344781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a82af153dde64aaecebbaa654ef25fe458cadc53b82b53ef2709b36ee12472`  
		Last Modified: Thu, 15 Jun 2023 04:11:27 GMT  
		Size: 2.7 MB (2743785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:513a439724cb0dce6489fcef92ec4c613854488cc971907f16b38f06ff6e8a14`  
		Last Modified: Thu, 15 Jun 2023 04:11:26 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60c5f3fdb07b83b724766e77b9ffeaaa86c0112dc077280c28d8ab36d1b52955`  
		Last Modified: Thu, 15 Jun 2023 04:11:26 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee2f8de8efb5e3f0eacdfc5c9ee5c77495033c64695cf8b1bc4f82538d7d9f3d`  
		Last Modified: Tue, 11 Jul 2023 01:39:22 GMT  
		Size: 12.1 MB (12055817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd4ea97683ddbf39a918a6653c39e5671799725b6c63944d07ac43dd81e82303`  
		Last Modified: Tue, 11 Jul 2023 01:39:21 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e03f060fe9351b0a9e559ecec51cb100eb4d22a531a1dbd1e29498c030d08ce8`  
		Last Modified: Tue, 11 Jul 2023 01:39:26 GMT  
		Size: 17.5 MB (17534647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a0ea337e6d31705b2c58e3727dcddcc8950c6bc79c6aae50f5bd4d985fcafa`  
		Last Modified: Tue, 11 Jul 2023 01:39:21 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03bd1e71d9d3f7015b0861bf0abf0d2a6c2d71f4c5e919baf51f752e6996351e`  
		Last Modified: Tue, 11 Jul 2023 01:39:21 GMT  
		Size: 18.7 KB (18729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e38489b38a5fd761d7944e3050f2b0208c91c7ce7e7c4eafc67bf7b74e4eb44f`  
		Last Modified: Tue, 11 Jul 2023 07:33:04 GMT  
		Size: 19.7 MB (19691138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30cb7352fa9c1ccc703543decd147874b6993bf98a6003b2d0be1201f38034f6`  
		Last Modified: Thu, 15 Jun 2023 12:38:30 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db9fc69ed9597352cbed2ee21f7710a0149f22968f722ae9aca913e6353c97e9`  
		Last Modified: Tue, 11 Jul 2023 07:32:59 GMT  
		Size: 9.2 MB (9169680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89d00e676dc41460ecc6177f7c8ba7667bfb81bdbd15d7dcfae277a62ee4133c`  
		Last Modified: Tue, 11 Jul 2023 07:32:56 GMT  
		Size: 392.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da0cbb5afbd1e5d36a773429c080055749911e433eab88750edd304a9ad5e7be`  
		Last Modified: Tue, 11 Jul 2023 07:32:57 GMT  
		Size: 1.5 MB (1513057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a587d33a3f09d07616e652b7265f3e040d2133ae58ab49f3715710108be2a45f`  
		Last Modified: Tue, 11 Jul 2023 07:32:57 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:cli-2.8.1-php8.2` - linux; s390x

```console
$ docker pull wordpress@sha256:4afd58825da0336b587c3ee16a6e91c0c66289e1c8dff64f9ccc3870cabf23e9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64944564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eae7f36c43e4d7080bb69be7a72abd767791ee8a85f0e747fc417f3541dc938a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Thu, 15 Jun 2023 05:18:38 GMT
ADD file:a59beca78118ebf4f86cc1685237dc3a29a519401a70668da520beaa3d29eb7a in / 
# Thu, 15 Jun 2023 05:18:38 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 18:32:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 Jun 2023 18:32:18 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 15 Jun 2023 18:32:20 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 15 Jun 2023 18:32:20 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 Jun 2023 18:32:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 15 Jun 2023 18:32:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jun 2023 18:32:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jun 2023 18:32:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 Jun 2023 19:09:45 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Tue, 11 Jul 2023 04:24:54 GMT
ENV PHP_VERSION=8.2.8
# Tue, 11 Jul 2023 04:24:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.8.tar.xz.asc
# Tue, 11 Jul 2023 04:24:55 GMT
ENV PHP_SHA256=cfe1055fbcd486de7d3312da6146949aae577365808790af6018205567609801
# Tue, 11 Jul 2023 04:24:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 11 Jul 2023 04:25:00 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 11 Jul 2023 04:28:04 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 11 Jul 2023 04:28:06 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Tue, 11 Jul 2023 04:28:07 GMT
RUN docker-php-ext-enable sodium
# Tue, 11 Jul 2023 04:28:07 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 11 Jul 2023 04:28:07 GMT
CMD ["php" "-a"]
# Tue, 11 Jul 2023 07:44:53 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client
# Tue, 11 Jul 2023 07:44:55 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html
# Tue, 11 Jul 2023 07:44:56 GMT
WORKDIR /var/www/html
# Tue, 11 Jul 2023 07:45:40 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Tue, 11 Jul 2023 07:45:42 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Tue, 11 Jul 2023 07:45:42 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Tue, 11 Jul 2023 07:45:42 GMT
ENV WORDPRESS_CLI_VERSION=2.8.1
# Tue, 11 Jul 2023 07:45:42 GMT
ENV WORDPRESS_CLI_SHA512=c1d40ee90b330ca1f8ddbed14b938b41ec5d9ff723c7c1cf3f41a2d9a1b271079a51a37ea3d1c9aa9c628fdd43449dba3995a8de150a68abbd505b06b91d9d2b
# Tue, 11 Jul 2023 07:45:44 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version
# Tue, 11 Jul 2023 07:45:44 GMT
VOLUME [/var/www/html]
# Tue, 11 Jul 2023 07:45:44 GMT
COPY file:b6efa5ff0423d61c2df0c8941b896844a8272d8516cdda0fcae8daaf56baac18 in /usr/local/bin/ 
# Tue, 11 Jul 2023 07:45:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jul 2023 07:45:45 GMT
USER www-data
# Tue, 11 Jul 2023 07:45:45 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:998cc98447b44e5f0fe799dce691412796ba586ab22eb7c99aebf9d45f34833b`  
		Last Modified: Thu, 15 Jun 2023 05:29:38 GMT  
		Size: 3.2 MB (3213497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9863b5dcc3e5885fe5ff8335b86d4287dfd59b451fe22e94b79f83b396c3776d`  
		Last Modified: Thu, 15 Jun 2023 21:54:07 GMT  
		Size: 2.8 MB (2766871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f159305449b6c309659dadfedb968259be79e6f5b9f552d97134f0a94490ae8`  
		Last Modified: Thu, 15 Jun 2023 21:54:07 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0e5f78cdbb2bcfe6b24c6cc002d51d1551a0fbabd06fa3baaee2be566d6d55f`  
		Last Modified: Thu, 15 Jun 2023 21:54:07 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db651d70c1113ea67c57f04de6578937a1822d540ea190adb9b62b74c523f671`  
		Last Modified: Tue, 11 Jul 2023 05:40:13 GMT  
		Size: 12.1 MB (12055817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79d0fcf43facc9ad25e15871e8a258d7f3294f702dc8444ab7a1f9d25cf8fa7f`  
		Last Modified: Tue, 11 Jul 2023 05:40:12 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b986921c8d645ceb85ebe0f5bd36e512943735b3b681a4d98c0adcd12f8dd1`  
		Last Modified: Tue, 11 Jul 2023 05:40:15 GMT  
		Size: 15.6 MB (15645341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946af675f7198859b37ad636c6713027c9cbed3fe30f41f559611ccaef26744e`  
		Last Modified: Tue, 11 Jul 2023 05:40:12 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3228efbf5921e1eb8b794fc340712264fe951424151fd1f7a9d7665ee6cf24d8`  
		Last Modified: Tue, 11 Jul 2023 05:40:12 GMT  
		Size: 18.8 KB (18759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5a30bf70cdaa27733257225da16d99be2d9b47919bbfb25972644e4d6bcd8c0`  
		Last Modified: Tue, 11 Jul 2023 07:51:18 GMT  
		Size: 20.8 MB (20828364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08eeae35ce526006a2cdf72a22adc445949c38a4a60027f3e9b9fff381441f27`  
		Last Modified: Fri, 16 Jun 2023 05:45:08 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a641b89a531a03f158c8db52d924265dc0c4ec6268e46109c14c3cd2e127ab`  
		Last Modified: Tue, 11 Jul 2023 07:51:15 GMT  
		Size: 8.9 MB (8897413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b77170ca3a4a82b1300b45a69f306d32afce09b04b0cf980156b53d51d884dc2`  
		Last Modified: Tue, 11 Jul 2023 07:51:14 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ca9a8e220409bcb7fcc5b53ba5beb1709263de15b38b910dab940a9628099c3`  
		Last Modified: Tue, 11 Jul 2023 07:51:14 GMT  
		Size: 1.5 MB (1513088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:956c7f85ab8481ef2c7dfecd44ae3765ac6a5977ceba6b90fa275c6cdd09c590`  
		Last Modified: Tue, 11 Jul 2023 07:51:14 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
