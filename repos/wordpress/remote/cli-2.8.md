## `wordpress:cli-2.8`

```console
$ docker pull wordpress@sha256:5399f5cae6fd140d82126c778ce6db9285cecfc0165303ed99a978a8e4fb430c
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

### `wordpress:cli-2.8` - linux; amd64

```console
$ docker pull wordpress@sha256:b3719f225bb287b48a270e20f7a207e77f8789e83e6b61fdbe284e19d3b5c50a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50513439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18ac0598c63c17f1aa2a3c34e92f3f879fd2c96646c385d5412df2e4574325e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 14 Jun 2023 20:42:09 GMT
ADD file:4af69326e088b3c0f82320e9cd97b60c28bf019b984787c6f1c22489e6221f29 in / 
# Wed, 14 Jun 2023 20:42:09 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 01:40:06 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 Jun 2023 01:40:08 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 15 Jun 2023 01:40:08 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 15 Jun 2023 01:40:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 Jun 2023 01:40:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 15 Jun 2023 01:40:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jun 2023 01:40:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jun 2023 01:40:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 Jun 2023 01:53:05 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F 2C16C765DBE54A088130F1BC4B9B5F600B55F3B4
# Thu, 15 Jun 2023 01:53:05 GMT
ENV PHP_VERSION=8.0.29
# Thu, 15 Jun 2023 01:53:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.29.tar.xz.asc
# Thu, 15 Jun 2023 01:53:06 GMT
ENV PHP_SHA256=14db2fbf26c07d0eb2c9fab25dbde7e27726a3e88452cca671f0896bbb683ca9
# Thu, 15 Jun 2023 01:53:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 15 Jun 2023 01:53:13 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 15 Jun 2023 01:57:02 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 15 Jun 2023 01:57:03 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 15 Jun 2023 01:57:04 GMT
RUN docker-php-ext-enable sodium
# Thu, 15 Jun 2023 01:57:04 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 Jun 2023 01:57:04 GMT
CMD ["php" "-a"]
# Thu, 15 Jun 2023 08:17:46 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client
# Thu, 15 Jun 2023 08:17:47 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html
# Thu, 15 Jun 2023 08:17:47 GMT
WORKDIR /var/www/html
# Thu, 15 Jun 2023 08:18:39 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Thu, 15 Jun 2023 08:18:40 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Thu, 15 Jun 2023 08:18:40 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Thu, 15 Jun 2023 08:18:40 GMT
ENV WORDPRESS_CLI_VERSION=2.8.1
# Thu, 15 Jun 2023 08:18:40 GMT
ENV WORDPRESS_CLI_SHA512=c1d40ee90b330ca1f8ddbed14b938b41ec5d9ff723c7c1cf3f41a2d9a1b271079a51a37ea3d1c9aa9c628fdd43449dba3995a8de150a68abbd505b06b91d9d2b
# Thu, 15 Jun 2023 08:18:43 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version
# Thu, 15 Jun 2023 08:18:43 GMT
VOLUME [/var/www/html]
# Thu, 15 Jun 2023 08:18:43 GMT
COPY file:b6efa5ff0423d61c2df0c8941b896844a8272d8516cdda0fcae8daaf56baac18 in /usr/local/bin/ 
# Thu, 15 Jun 2023 08:18:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jun 2023 08:18:43 GMT
USER www-data
# Thu, 15 Jun 2023 08:18:43 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:c1d6d1b2d5a367259e6e51a7f4d1ccd66a28cc9940d6599d8a8ea9544dd4b4a8`  
		Last Modified: Wed, 14 Jun 2023 20:42:45 GMT  
		Size: 2.8 MB (2807669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f18dab2210bd7d67f6b480dae4e5187f1fa04f169a0684d063d0b4789353cc9`  
		Last Modified: Thu, 15 Jun 2023 02:12:58 GMT  
		Size: 1.8 MB (1757485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c509fa41f3283f176f9d42818cc73fffbe6a7f97bc09947df4daa48bf016a255`  
		Last Modified: Thu, 15 Jun 2023 02:12:57 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2592fe0d29a03ed9e5df89824b6b293d195772b43fa2287f12983f24cb287a5`  
		Last Modified: Thu, 15 Jun 2023 02:12:57 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c90e15a8288a2b70283ce205564f8f589f918a9e98a45a8e9d0432408c29deb7`  
		Last Modified: Thu, 15 Jun 2023 02:13:47 GMT  
		Size: 10.8 MB (10823746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d26a5bc00693fad8866ac408e90c096ec34dd8031d895e5a776abcf7a879127a`  
		Last Modified: Thu, 15 Jun 2023 02:13:45 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3b4f16c44bfbee534a72a64754254f11624ff4ec7fef3e71dffa3bb64f8333d`  
		Last Modified: Thu, 15 Jun 2023 02:13:48 GMT  
		Size: 15.8 MB (15794583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1431445ed2245ca85da4e48aefc72d1d8512d0a50e77a2ac75e08ff43ee18d8`  
		Last Modified: Thu, 15 Jun 2023 02:13:45 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c38cb0a46a5d1d2ee84ffe91aa3d10eb4c633b048aed4a283432bc03f9af8a2`  
		Last Modified: Thu, 15 Jun 2023 02:13:45 GMT  
		Size: 18.7 KB (18665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af2741d545c561277a876e501bc793b937f0b50c713d1ae77afe032b26fab98`  
		Last Modified: Thu, 15 Jun 2023 08:23:24 GMT  
		Size: 9.4 MB (9419340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:534e0cf2cc3821ce9b9c14b72d6e9ac6fb795ce561080d6afdea41b6f5ad7b1f`  
		Last Modified: Thu, 15 Jun 2023 08:23:20 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19aa68ba6006498b3fad2197e694e9e73ed8cd560fd5e3d582f4e09543f0f362`  
		Last Modified: Thu, 15 Jun 2023 08:23:21 GMT  
		Size: 8.4 MB (8409984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30dae029c0c214594fad44469d7c81b055f0d6e974f5f685cc0c7c2168cc1605`  
		Last Modified: Thu, 15 Jun 2023 08:23:20 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7214493d729f008865956f237d8b169e04e540dd05d26784cca5eeb3949b185`  
		Last Modified: Thu, 15 Jun 2023 08:23:20 GMT  
		Size: 1.5 MB (1476557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5ba9583b523057936ac2596c3984fd02da3e416e776833b01d57033d6c4ea18`  
		Last Modified: Thu, 15 Jun 2023 08:23:20 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:cli-2.8` - linux; arm variant v6

```console
$ docker pull wordpress@sha256:9052cc67200279cdd0f4c8e35c6104dfb96457f3305ff141abb49fbdac22cb97
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48094070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:287d6314ab53833c5876f67f6fd45fe76da414f153ef1a9e69396e2ed436a032`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:20 GMT
ADD file:321b24cc0fbd39caa2d7672a740d2cd2030ba99cab16f50c22db9955bd99350b in / 
# Mon, 07 Aug 2023 19:49:20 GMT
CMD ["/bin/sh"]
# Wed, 09 Aug 2023 01:16:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 09 Aug 2023 01:16:26 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 09 Aug 2023 01:16:27 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 09 Aug 2023 01:16:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 09 Aug 2023 01:16:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 09 Aug 2023 01:16:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 09 Aug 2023 01:16:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 09 Aug 2023 01:16:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 09 Aug 2023 01:25:48 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F 2C16C765DBE54A088130F1BC4B9B5F600B55F3B4 39B641343D8C104B2B146DC3F9C39DC0B9698544
# Wed, 09 Aug 2023 01:25:48 GMT
ENV PHP_VERSION=8.0.30
# Wed, 09 Aug 2023 01:25:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.30.tar.xz.asc
# Wed, 09 Aug 2023 01:25:49 GMT
ENV PHP_SHA256=216ab305737a5d392107112d618a755dc5df42058226f1670e9db90e77d777d9
# Wed, 09 Aug 2023 01:25:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 09 Aug 2023 01:25:56 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 09 Aug 2023 01:28:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 09 Aug 2023 01:28:32 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Wed, 09 Aug 2023 01:28:33 GMT
RUN docker-php-ext-enable sodium
# Wed, 09 Aug 2023 01:28:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 09 Aug 2023 01:28:34 GMT
CMD ["php" "-a"]
# Wed, 09 Aug 2023 04:29:46 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client
# Wed, 09 Aug 2023 04:29:46 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html
# Wed, 09 Aug 2023 04:29:47 GMT
WORKDIR /var/www/html
# Wed, 09 Aug 2023 04:30:38 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Wed, 09 Aug 2023 04:30:39 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Wed, 09 Aug 2023 04:30:39 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Wed, 09 Aug 2023 04:30:39 GMT
ENV WORDPRESS_CLI_VERSION=2.8.1
# Wed, 09 Aug 2023 04:30:39 GMT
ENV WORDPRESS_CLI_SHA512=c1d40ee90b330ca1f8ddbed14b938b41ec5d9ff723c7c1cf3f41a2d9a1b271079a51a37ea3d1c9aa9c628fdd43449dba3995a8de150a68abbd505b06b91d9d2b
# Wed, 09 Aug 2023 04:30:41 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version
# Wed, 09 Aug 2023 04:30:42 GMT
VOLUME [/var/www/html]
# Wed, 09 Aug 2023 04:30:42 GMT
COPY file:b6efa5ff0423d61c2df0c8941b896844a8272d8516cdda0fcae8daaf56baac18 in /usr/local/bin/ 
# Wed, 09 Aug 2023 04:30:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Aug 2023 04:30:42 GMT
USER www-data
# Wed, 09 Aug 2023 04:30:42 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:dffa980f71c953938bb194a457aa62e7f1885137331eef8bf7f9403c075f711c`  
		Last Modified: Mon, 07 Aug 2023 19:50:02 GMT  
		Size: 2.6 MB (2615553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235a43ee43e98c2667b11a621972481309d7d36f09eea13b41a16ec09ee41b66`  
		Last Modified: Wed, 09 Aug 2023 01:42:52 GMT  
		Size: 1.7 MB (1748521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec388cc4bd1845620f80ae6071a58c211fa1e13ce54e9fe91f7cf1409d3dceb`  
		Last Modified: Wed, 09 Aug 2023 01:42:51 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5bd3674671bd958707ba8b3c729fdff4b207e2a7254a058c0118f56315dbfb3`  
		Last Modified: Wed, 09 Aug 2023 01:42:51 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ffb72df85db09fdc54963fbbdde78624ef971c26096f6de41b3970be080e1d8`  
		Last Modified: Wed, 09 Aug 2023 01:43:30 GMT  
		Size: 10.8 MB (10841070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4449046c2c01ef48071cc3dc857bd1b9275b481163e21e247d37ce90da59ff29`  
		Last Modified: Wed, 09 Aug 2023 01:43:29 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5a9330a3fa934a0457fc6c344ba8cd1fb5d1bf42fd87a1e009ec0c0a4b476a4`  
		Last Modified: Wed, 09 Aug 2023 01:43:32 GMT  
		Size: 14.4 MB (14411304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c1ddecef7efa28fb17963cc1d717e7ea7fc792bfcd1166db39d13e78c05b68`  
		Last Modified: Wed, 09 Aug 2023 01:43:29 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ba5ae92223db8eddd33029d412bbc32d6a35295b3b53582ff078d15ac25bc01`  
		Last Modified: Wed, 09 Aug 2023 01:43:28 GMT  
		Size: 18.7 KB (18676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4e7d177f2933ac6087e23ccbef9898f5b3a298daecd2fe6a1132cd98dfbe55`  
		Last Modified: Wed, 09 Aug 2023 04:35:19 GMT  
		Size: 9.0 MB (8987809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d324c0a2b6699c8674d347d0092d5b1978624d3a40b281b95cba26e323134030`  
		Last Modified: Wed, 09 Aug 2023 04:35:16 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:115b0104c75752e24b99822c3eebfe6cd11b350d48ccff78111bc078bd6f69e2`  
		Last Modified: Wed, 09 Aug 2023 04:35:17 GMT  
		Size: 8.0 MB (7989148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7cd55d21650a81285d2986508052d0597d33dbc393b2542aff706efc82c5252`  
		Last Modified: Wed, 09 Aug 2023 04:35:15 GMT  
		Size: 388.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f98dcc588b4ea91acea2069580a17048a6b79f1e650981a9f922f33182ee81`  
		Last Modified: Wed, 09 Aug 2023 04:35:15 GMT  
		Size: 1.5 MB (1476575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d5e8872b40445176a0bc82cabbd17118452eb4e062bfbd23054508c2dabfb2f`  
		Last Modified: Wed, 09 Aug 2023 04:35:15 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:cli-2.8` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:4ac3b83b3f9bfce5de8002e82d391ff00a5c75414c704f975a9b5fceaede3ac7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46101494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37e1d702669a2b4c993689314d1f0e5dc70a10f1e11f5235f28b2f56b49ac50b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Mon, 07 Aug 2023 19:57:33 GMT
ADD file:911497ffc967e53c16d8356f320bf61fe06b85fc3250b7c01183f7bcfbfef404 in / 
# Mon, 07 Aug 2023 19:57:33 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 00:47:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 08 Aug 2023 00:47:50 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 08 Aug 2023 00:47:51 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 08 Aug 2023 00:47:51 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 08 Aug 2023 00:47:51 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 08 Aug 2023 00:47:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 08 Aug 2023 00:47:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 08 Aug 2023 00:47:52 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 08 Aug 2023 22:56:41 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F 2C16C765DBE54A088130F1BC4B9B5F600B55F3B4 39B641343D8C104B2B146DC3F9C39DC0B9698544
# Tue, 08 Aug 2023 22:56:41 GMT
ENV PHP_VERSION=8.0.30
# Tue, 08 Aug 2023 22:56:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.30.tar.xz.asc
# Tue, 08 Aug 2023 22:56:41 GMT
ENV PHP_SHA256=216ab305737a5d392107112d618a755dc5df42058226f1670e9db90e77d777d9
# Tue, 08 Aug 2023 22:56:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 08 Aug 2023 22:56:51 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 08 Aug 2023 23:00:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 08 Aug 2023 23:00:59 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Tue, 08 Aug 2023 23:01:00 GMT
RUN docker-php-ext-enable sodium
# Tue, 08 Aug 2023 23:01:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 08 Aug 2023 23:01:00 GMT
CMD ["php" "-a"]
# Wed, 09 Aug 2023 02:24:37 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client
# Wed, 09 Aug 2023 02:24:38 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html
# Wed, 09 Aug 2023 02:24:38 GMT
WORKDIR /var/www/html
# Wed, 09 Aug 2023 02:25:29 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Wed, 09 Aug 2023 02:25:30 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Wed, 09 Aug 2023 02:25:30 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Wed, 09 Aug 2023 02:25:30 GMT
ENV WORDPRESS_CLI_VERSION=2.8.1
# Wed, 09 Aug 2023 02:25:30 GMT
ENV WORDPRESS_CLI_SHA512=c1d40ee90b330ca1f8ddbed14b938b41ec5d9ff723c7c1cf3f41a2d9a1b271079a51a37ea3d1c9aa9c628fdd43449dba3995a8de150a68abbd505b06b91d9d2b
# Wed, 09 Aug 2023 02:25:33 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version
# Wed, 09 Aug 2023 02:25:33 GMT
VOLUME [/var/www/html]
# Wed, 09 Aug 2023 02:25:33 GMT
COPY file:b6efa5ff0423d61c2df0c8941b896844a8272d8516cdda0fcae8daaf56baac18 in /usr/local/bin/ 
# Wed, 09 Aug 2023 02:25:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Aug 2023 02:25:33 GMT
USER www-data
# Wed, 09 Aug 2023 02:25:33 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:d27c9f7e5791cecbf0251c0e7638ad6fbd2b510f038f66cc06c933da98c75979`  
		Last Modified: Mon, 07 Aug 2023 19:58:18 GMT  
		Size: 2.4 MB (2419274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ae1e3485d99b72fb6a5b1ce8b15037ea1b9ab05b1e9cf47cca0b6abe7092d7`  
		Last Modified: Tue, 08 Aug 2023 01:16:27 GMT  
		Size: 1.6 MB (1610619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f61367dfcaeab4fed8f792b96d1198516e3e79fd3f2a38ec845d995138fc494`  
		Last Modified: Tue, 08 Aug 2023 01:16:27 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc0d6651d0d03aa29ed639d5d61324ec6614c118dcc75057a223ab4996be6b5d`  
		Last Modified: Tue, 08 Aug 2023 01:16:26 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86bd4f01ec848e571a9c2169c1e73155261c4597b9457094d350b60735b67157`  
		Last Modified: Tue, 08 Aug 2023 23:14:11 GMT  
		Size: 10.8 MB (10841073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d56a7c617dbbe34820bf0f82a003eee910752821de7030baa673c2a755783e0`  
		Last Modified: Tue, 08 Aug 2023 23:14:10 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a13c19c9a8175e79cd87625052072cdce2906d96b25265529f8e3b4db2e3ce57`  
		Last Modified: Tue, 08 Aug 2023 23:14:13 GMT  
		Size: 13.5 MB (13542771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:259a60693e9b66a570880c6806bfcf10df91d36b14e5746b5b3b7dfc1a108b86`  
		Last Modified: Tue, 08 Aug 2023 23:14:10 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59973f43eaac53f305b5c8e2d3bbffd3033ece3315de4abd43d5835311a057a8`  
		Last Modified: Tue, 08 Aug 2023 23:14:10 GMT  
		Size: 18.7 KB (18665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ff9bf620ae22216b43057b8432a71e70039cffcbb3dead754405404bb4b79a9`  
		Last Modified: Wed, 09 Aug 2023 02:29:49 GMT  
		Size: 8.7 MB (8704595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2b7ea12c31c878a2e1ab18efd6816601b913ed82a1027409307b0caafec9d6`  
		Last Modified: Wed, 09 Aug 2023 02:29:45 GMT  
		Size: 145.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bed1163a78038c99f793a86060a8b67a308cb305cf2dd7e41ea2c22a1c33fc64`  
		Last Modified: Wed, 09 Aug 2023 02:29:46 GMT  
		Size: 7.5 MB (7482541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e935a7cebb6634c0b2a4c7cf6af65883ea514dc3cc4d78940c49d0efb40a5267`  
		Last Modified: Wed, 09 Aug 2023 02:29:45 GMT  
		Size: 388.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7846881664c0e95c32b77e0f6dfa47ea90a0e4558c815fdca7aa8bb430e73cf`  
		Last Modified: Wed, 09 Aug 2023 02:29:45 GMT  
		Size: 1.5 MB (1476546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3b50d20a4e413e8a66b627f2a97c4d8f4f17ad6e648c6a7cf914796703786c`  
		Last Modified: Wed, 09 Aug 2023 02:29:45 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:cli-2.8` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:b49888ab0fe090df87824e4cb8246856cee91f539fe1d72d6544cc1a203e1953
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49678564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06bbc20e253815ea29cc69e0b401146931cc344489ebea7a056cff4532f4db7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 14 Jun 2023 20:49:07 GMT
ADD file:e80eabe59d1f87ef41634428d9f8fdeb633c2128ac97564f96f5495ef6bf2c72 in / 
# Wed, 14 Jun 2023 20:49:07 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 04:16:05 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 Jun 2023 04:16:06 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 15 Jun 2023 04:16:06 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 15 Jun 2023 04:16:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 Jun 2023 04:16:07 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 15 Jun 2023 04:16:07 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jun 2023 04:16:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jun 2023 04:16:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 Jun 2023 04:28:54 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F 2C16C765DBE54A088130F1BC4B9B5F600B55F3B4
# Thu, 15 Jun 2023 04:28:54 GMT
ENV PHP_VERSION=8.0.29
# Thu, 15 Jun 2023 04:28:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.29.tar.xz.asc
# Thu, 15 Jun 2023 04:28:54 GMT
ENV PHP_SHA256=14db2fbf26c07d0eb2c9fab25dbde7e27726a3e88452cca671f0896bbb683ca9
# Thu, 15 Jun 2023 04:29:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 15 Jun 2023 04:29:01 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 15 Jun 2023 04:31:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 15 Jun 2023 04:31:38 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 15 Jun 2023 04:31:39 GMT
RUN docker-php-ext-enable sodium
# Thu, 15 Jun 2023 04:31:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 Jun 2023 04:31:39 GMT
CMD ["php" "-a"]
# Thu, 15 Jun 2023 09:15:43 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client
# Thu, 15 Jun 2023 09:15:43 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html
# Thu, 15 Jun 2023 09:15:44 GMT
WORKDIR /var/www/html
# Thu, 15 Jun 2023 09:16:29 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Thu, 15 Jun 2023 09:16:29 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Thu, 15 Jun 2023 09:16:29 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Thu, 15 Jun 2023 09:16:29 GMT
ENV WORDPRESS_CLI_VERSION=2.8.1
# Thu, 15 Jun 2023 09:16:29 GMT
ENV WORDPRESS_CLI_SHA512=c1d40ee90b330ca1f8ddbed14b938b41ec5d9ff723c7c1cf3f41a2d9a1b271079a51a37ea3d1c9aa9c628fdd43449dba3995a8de150a68abbd505b06b91d9d2b
# Thu, 15 Jun 2023 09:16:32 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version
# Thu, 15 Jun 2023 09:16:32 GMT
VOLUME [/var/www/html]
# Thu, 15 Jun 2023 09:16:32 GMT
COPY file:b6efa5ff0423d61c2df0c8941b896844a8272d8516cdda0fcae8daaf56baac18 in /usr/local/bin/ 
# Thu, 15 Jun 2023 09:16:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jun 2023 09:16:32 GMT
USER www-data
# Thu, 15 Jun 2023 09:16:33 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:a880266d3b77f75696023df2da1ef66c3c565e0f70596242395c9e68de955c7c`  
		Last Modified: Wed, 14 Jun 2023 20:49:43 GMT  
		Size: 2.7 MB (2707906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cce53a806897f7cc9c09832e471350af00886b116b56a26cd6bfb3412b96c16`  
		Last Modified: Thu, 15 Jun 2023 04:44:28 GMT  
		Size: 1.8 MB (1754468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45d91342e09e434ef647bc867d983b896d4ecef678e02f9be4dad1f01acfebc1`  
		Last Modified: Thu, 15 Jun 2023 04:44:27 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a4da02ae427fd4ea692ddc232ff1364440fde0747d6e38f63ae897bf57e338d`  
		Last Modified: Thu, 15 Jun 2023 04:44:27 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ddc8767ffe0d777879e32238197cee1db00fe59be801a7e380494d60e17c8b2`  
		Last Modified: Thu, 15 Jun 2023 04:45:07 GMT  
		Size: 10.8 MB (10823750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccaeddfcd2886fb50d266db6906299ff1c2ac980f5b3624236c11fc6de8cb453`  
		Last Modified: Thu, 15 Jun 2023 04:45:07 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e0066ede6cef9b45f53a42f94ae67d7ccb7a9fee39954a60560dd38c6548577`  
		Last Modified: Thu, 15 Jun 2023 04:45:09 GMT  
		Size: 15.2 MB (15213164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3de41eb79e44fe88d367fef8c5b8f2bf6cc67726ff4304ff963216b00b3bb6b9`  
		Last Modified: Thu, 15 Jun 2023 04:45:06 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76a33c1c317532ec042d800de57347494b08552eb0994e7cc2385466a1bccd46`  
		Last Modified: Thu, 15 Jun 2023 04:45:07 GMT  
		Size: 18.7 KB (18668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b381a225d9c431a56f2bfdfb9e86e35183217dfbec67a86b882c8e0160802920`  
		Last Modified: Thu, 15 Jun 2023 09:20:42 GMT  
		Size: 9.5 MB (9465227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6c6fe8b5e94af26de5e20e9814bb3c1f3b219637c6e6e24806631b036ad6d0c`  
		Last Modified: Thu, 15 Jun 2023 09:20:39 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d543a12cc1f31cf8d28cbff0f6a9f100703750ed1cfc1d91436cfbcd6faaeca1`  
		Last Modified: Thu, 15 Jun 2023 09:20:40 GMT  
		Size: 8.2 MB (8213429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed853aa85ceff527d7610fbc4e61ff381a5d2838d8ae3426f8547f67bce20ab9`  
		Last Modified: Thu, 15 Jun 2023 09:20:39 GMT  
		Size: 388.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f755e97436b57808a1c8432cf91bbe9b7456445671228565400c8d7eb98b6494`  
		Last Modified: Thu, 15 Jun 2023 09:20:40 GMT  
		Size: 1.5 MB (1476542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:187f88fb86c61e1173c17c1a12f508cead52767eaf65c7362245772e7e203b91`  
		Last Modified: Thu, 15 Jun 2023 09:20:39 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:cli-2.8` - linux; 386

```console
$ docker pull wordpress@sha256:60ebd53c051ba22369b83fa3990fbf1bd885b31563f9beb844ae1704a7378e84
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51532831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fc0c4690f3982d6fb11f8da39d06b6f447f800672a3be881f190fc4b743730a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Mon, 07 Aug 2023 19:38:34 GMT
ADD file:c06b4f6991638e506d4d0a4d70c4a78ba30b971767802af4c6b837cdf59d4303 in / 
# Mon, 07 Aug 2023 19:38:34 GMT
CMD ["/bin/sh"]
# Wed, 09 Aug 2023 01:44:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 09 Aug 2023 01:44:19 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 09 Aug 2023 01:44:19 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 09 Aug 2023 01:44:19 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 09 Aug 2023 01:44:20 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 09 Aug 2023 01:44:20 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 09 Aug 2023 01:44:20 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 09 Aug 2023 01:44:20 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 09 Aug 2023 02:46:18 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F 2C16C765DBE54A088130F1BC4B9B5F600B55F3B4 39B641343D8C104B2B146DC3F9C39DC0B9698544
# Wed, 09 Aug 2023 02:46:18 GMT
ENV PHP_VERSION=8.0.30
# Wed, 09 Aug 2023 02:46:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.30.tar.xz.asc
# Wed, 09 Aug 2023 02:46:18 GMT
ENV PHP_SHA256=216ab305737a5d392107112d618a755dc5df42058226f1670e9db90e77d777d9
# Wed, 09 Aug 2023 02:46:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 09 Aug 2023 02:46:26 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 09 Aug 2023 02:53:27 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 09 Aug 2023 02:53:27 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Wed, 09 Aug 2023 02:53:28 GMT
RUN docker-php-ext-enable sodium
# Wed, 09 Aug 2023 02:53:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 09 Aug 2023 02:53:28 GMT
CMD ["php" "-a"]
# Wed, 09 Aug 2023 08:41:40 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client
# Wed, 09 Aug 2023 08:41:40 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html
# Wed, 09 Aug 2023 08:41:40 GMT
WORKDIR /var/www/html
# Wed, 09 Aug 2023 08:42:51 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Wed, 09 Aug 2023 08:42:52 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Wed, 09 Aug 2023 08:42:52 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Wed, 09 Aug 2023 08:42:52 GMT
ENV WORDPRESS_CLI_VERSION=2.8.1
# Wed, 09 Aug 2023 08:42:52 GMT
ENV WORDPRESS_CLI_SHA512=c1d40ee90b330ca1f8ddbed14b938b41ec5d9ff723c7c1cf3f41a2d9a1b271079a51a37ea3d1c9aa9c628fdd43449dba3995a8de150a68abbd505b06b91d9d2b
# Wed, 09 Aug 2023 08:42:55 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version
# Wed, 09 Aug 2023 08:42:55 GMT
VOLUME [/var/www/html]
# Wed, 09 Aug 2023 08:42:55 GMT
COPY file:b6efa5ff0423d61c2df0c8941b896844a8272d8516cdda0fcae8daaf56baac18 in /usr/local/bin/ 
# Wed, 09 Aug 2023 08:42:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Aug 2023 08:42:56 GMT
USER www-data
# Wed, 09 Aug 2023 08:42:56 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:be0d19c155de823c6b37eaaba7cdec9085e8f1e39b1dd5982a19acb6c8c97cc5`  
		Last Modified: Mon, 07 Aug 2023 19:39:20 GMT  
		Size: 2.8 MB (2810553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3a873ad02c34f43ada7a731238ae1cc36dea643dfb138fb20aff34cf61fe19`  
		Last Modified: Wed, 09 Aug 2023 03:19:35 GMT  
		Size: 1.9 MB (1869218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f62b1a840567129050b38d1c806b87180f635e6a42506dd09a37747e1aaab252`  
		Last Modified: Wed, 09 Aug 2023 03:19:35 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78bb0f594d2520f0eef9c133125a028f07e9956b8ccabc2498c2a9490a704e11`  
		Last Modified: Wed, 09 Aug 2023 03:19:35 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20bd720a304e809381d4484ff8f242c558dc0d220cf6f3693ffd5c4d7d244435`  
		Last Modified: Wed, 09 Aug 2023 03:22:50 GMT  
		Size: 10.8 MB (10841071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3504c70821fb843e3dce02b94dc32d85e2346eadafc01ee3e84a185e930958c`  
		Last Modified: Wed, 09 Aug 2023 03:22:49 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90106567bffb79e13af84c09a745a144ca02ac10f4a966024869e92c7e292b92`  
		Last Modified: Wed, 09 Aug 2023 03:22:53 GMT  
		Size: 16.2 MB (16151812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead22ae7ba48cb1b058e4c38d70e53c77111daa54c568fc96523fa717ab9b75b`  
		Last Modified: Wed, 09 Aug 2023 03:22:49 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:265a0b382baed63aee7b576ed61bf9a5394c1cdf48c24a10493eadd497b91fbd`  
		Last Modified: Wed, 09 Aug 2023 03:22:49 GMT  
		Size: 18.7 KB (18669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b88953fd81d6a0f01085878b13076262e6294f7f34e27905948493fc05b8bf2`  
		Last Modified: Wed, 09 Aug 2023 08:50:48 GMT  
		Size: 9.6 MB (9577721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d0007bdffc18833bf464d5434adc302478e27de48394afaa478b25411f27258`  
		Last Modified: Wed, 09 Aug 2023 08:50:44 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:290d08ed585aa2f28de7a2301b2538100fecc32ad0063ec6c6fb1c8101990da6`  
		Last Modified: Wed, 09 Aug 2023 08:50:46 GMT  
		Size: 8.8 MB (8781818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6c0d85ed097a8085f7d808261af37b929a033816e3317841a1c49e4839900d3`  
		Last Modified: Wed, 09 Aug 2023 08:50:44 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f09e834b1f5a63e92aa26d0e60847a435e196e9a54215479f2014546be3aa0`  
		Last Modified: Wed, 09 Aug 2023 08:50:45 GMT  
		Size: 1.5 MB (1476544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1417f498db78725f353ea3dfbbd57ffa1affab305164e18ac47d964c8929e391`  
		Last Modified: Wed, 09 Aug 2023 08:50:44 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:cli-2.8` - linux; ppc64le

```console
$ docker pull wordpress@sha256:3057d5ed9e1a3d61518c156e190163cfaa144d9648c1d765a6192debc950fe70
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51769781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b42567661e814bee97c8f5e37d5312ec4fd8332889427324270ac02ba89a919d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Thu, 15 Jun 2023 00:40:03 GMT
ADD file:687ce61613e63c93be9debda827167f433a51769ad625312ea1250ee87b62f30 in / 
# Thu, 15 Jun 2023 00:40:03 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 03:36:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 Jun 2023 03:36:56 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 15 Jun 2023 03:36:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 15 Jun 2023 03:36:59 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 Jun 2023 03:37:00 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 15 Jun 2023 03:37:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jun 2023 03:37:01 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jun 2023 03:37:01 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 Jun 2023 03:53:33 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F 2C16C765DBE54A088130F1BC4B9B5F600B55F3B4
# Thu, 15 Jun 2023 03:53:33 GMT
ENV PHP_VERSION=8.0.29
# Thu, 15 Jun 2023 03:53:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.29.tar.xz.asc
# Thu, 15 Jun 2023 03:53:34 GMT
ENV PHP_SHA256=14db2fbf26c07d0eb2c9fab25dbde7e27726a3e88452cca671f0896bbb683ca9
# Thu, 15 Jun 2023 03:53:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 15 Jun 2023 03:53:43 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 15 Jun 2023 03:58:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 15 Jun 2023 03:58:45 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 15 Jun 2023 03:58:47 GMT
RUN docker-php-ext-enable sodium
# Thu, 15 Jun 2023 03:58:47 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 Jun 2023 03:58:47 GMT
CMD ["php" "-a"]
# Thu, 15 Jun 2023 12:29:20 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client
# Thu, 15 Jun 2023 12:29:22 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html
# Thu, 15 Jun 2023 12:29:22 GMT
WORKDIR /var/www/html
# Thu, 15 Jun 2023 12:30:57 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Thu, 15 Jun 2023 12:30:59 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Thu, 15 Jun 2023 12:30:59 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Thu, 15 Jun 2023 12:31:00 GMT
ENV WORDPRESS_CLI_VERSION=2.8.1
# Thu, 15 Jun 2023 12:31:00 GMT
ENV WORDPRESS_CLI_SHA512=c1d40ee90b330ca1f8ddbed14b938b41ec5d9ff723c7c1cf3f41a2d9a1b271079a51a37ea3d1c9aa9c628fdd43449dba3995a8de150a68abbd505b06b91d9d2b
# Thu, 15 Jun 2023 12:31:06 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version
# Thu, 15 Jun 2023 12:31:06 GMT
VOLUME [/var/www/html]
# Thu, 15 Jun 2023 12:31:07 GMT
COPY file:b6efa5ff0423d61c2df0c8941b896844a8272d8516cdda0fcae8daaf56baac18 in /usr/local/bin/ 
# Thu, 15 Jun 2023 12:31:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jun 2023 12:31:08 GMT
USER www-data
# Thu, 15 Jun 2023 12:31:09 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:a2010c6a5435acd9b63d7f294696ba1d313d4393be0848195e1e655583ca50af`  
		Last Modified: Thu, 15 Jun 2023 00:40:48 GMT  
		Size: 2.8 MB (2802263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d3fe9251db3dda34b587ee300dae08e97202ec21ca39eebcba831825da166ab`  
		Last Modified: Thu, 15 Jun 2023 04:18:04 GMT  
		Size: 1.8 MB (1813856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f1f20948ec43d6a24614f43e4a6a8ef4f3f5b0bc7257dc904eeb8c12d0a3268`  
		Last Modified: Thu, 15 Jun 2023 04:18:03 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a6ae4841695077e13f2dc31e6a307daf66e51d7ce834b13b4c6b6826771d8f`  
		Last Modified: Thu, 15 Jun 2023 04:18:03 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bc9da9dfced373fb8b9e4d99f55607829579db41cd4288138b52a5e76a0a56e`  
		Last Modified: Thu, 15 Jun 2023 04:18:52 GMT  
		Size: 10.8 MB (10823751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f1d502dceb46c065a2ac92f60fb05ba6a2f648e8083602e5fd9c66618fe1600`  
		Last Modified: Thu, 15 Jun 2023 04:18:50 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7306888d3f532b9fff2c0375e7eb42607da17562f6bb1ed86cd0e337c58ed88`  
		Last Modified: Thu, 15 Jun 2023 04:18:55 GMT  
		Size: 16.6 MB (16591548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1567ab1ede9390d52c658d1e4172e34717b272eb785fda315b8d6805c9534bcc`  
		Last Modified: Thu, 15 Jun 2023 04:18:50 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7dc359d978936ebe26c78cd2881c18a95101ec8c8d4e59822cd2acf10d028bd`  
		Last Modified: Thu, 15 Jun 2023 04:18:50 GMT  
		Size: 18.7 KB (18660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a9bd442f9cd2b6896d82937c3c80cde65d998d3198c1928660762ae9d184846`  
		Last Modified: Thu, 15 Jun 2023 12:38:05 GMT  
		Size: 9.6 MB (9598848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be71578587c7637da2cf99e225b056be79497ae42b8e22a1ca46e6393c857995`  
		Last Modified: Thu, 15 Jun 2023 12:38:00 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d449873f933fb68b24a9668a2a953af55e4805c7c477e385c40e6276f07c5804`  
		Last Modified: Thu, 15 Jun 2023 12:38:03 GMT  
		Size: 8.6 MB (8638880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596bfb018a6214b0ec593ef81198de7c215e50205f9b04ebd88fe5a252635125`  
		Last Modified: Thu, 15 Jun 2023 12:38:00 GMT  
		Size: 394.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5ad624ec8333b8a09615653a9b50081aee815eec343777a606b520f7d74b398`  
		Last Modified: Thu, 15 Jun 2023 12:38:01 GMT  
		Size: 1.5 MB (1476559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b5317ff1452e611b496f02793cda050c8776f901d8f25184d43a565cfbc880d`  
		Last Modified: Thu, 15 Jun 2023 12:38:00 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:cli-2.8` - linux; s390x

```console
$ docker pull wordpress@sha256:a02375bc229d832c0c40bb61b16b92798b20bd98f072c2e7a3f3f5a2f649850d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49893603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef5ed6c85f4b8399c742b0f24965058c892d94b8ad7990abe7582ba2cb6706b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Thu, 15 Jun 2023 05:20:59 GMT
ADD file:16daa03175f0a8d874128d0c563e183e127bce1094ec72183deec297c28e021d in / 
# Thu, 15 Jun 2023 05:21:00 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 20:15:30 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 Jun 2023 20:15:33 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 15 Jun 2023 20:15:35 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 15 Jun 2023 20:15:36 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 Jun 2023 20:15:37 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 15 Jun 2023 20:15:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jun 2023 20:15:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jun 2023 20:15:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 Jun 2023 20:35:36 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F 2C16C765DBE54A088130F1BC4B9B5F600B55F3B4
# Thu, 15 Jun 2023 20:35:36 GMT
ENV PHP_VERSION=8.0.29
# Thu, 15 Jun 2023 20:35:36 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.29.tar.xz.asc
# Thu, 15 Jun 2023 20:35:36 GMT
ENV PHP_SHA256=14db2fbf26c07d0eb2c9fab25dbde7e27726a3e88452cca671f0896bbb683ca9
# Thu, 15 Jun 2023 20:35:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 15 Jun 2023 20:35:41 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 15 Jun 2023 20:39:20 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 15 Jun 2023 20:39:21 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 15 Jun 2023 20:39:23 GMT
RUN docker-php-ext-enable sodium
# Thu, 15 Jun 2023 20:39:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 Jun 2023 20:39:23 GMT
CMD ["php" "-a"]
# Fri, 16 Jun 2023 05:12:30 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client
# Fri, 16 Jun 2023 05:12:32 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html
# Fri, 16 Jun 2023 05:12:32 GMT
WORKDIR /var/www/html
# Fri, 16 Jun 2023 05:13:18 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Fri, 16 Jun 2023 05:13:19 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Fri, 16 Jun 2023 05:13:19 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Fri, 16 Jun 2023 05:13:20 GMT
ENV WORDPRESS_CLI_VERSION=2.8.1
# Fri, 16 Jun 2023 05:13:20 GMT
ENV WORDPRESS_CLI_SHA512=c1d40ee90b330ca1f8ddbed14b938b41ec5d9ff723c7c1cf3f41a2d9a1b271079a51a37ea3d1c9aa9c628fdd43449dba3995a8de150a68abbd505b06b91d9d2b
# Fri, 16 Jun 2023 05:13:23 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version
# Fri, 16 Jun 2023 05:13:23 GMT
VOLUME [/var/www/html]
# Fri, 16 Jun 2023 05:13:23 GMT
COPY file:b6efa5ff0423d61c2df0c8941b896844a8272d8516cdda0fcae8daaf56baac18 in /usr/local/bin/ 
# Fri, 16 Jun 2023 05:13:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jun 2023 05:13:23 GMT
USER www-data
# Fri, 16 Jun 2023 05:13:23 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:835f3b5b8d7d281d273a2dce84bab3df0d219e423e2de23b10fd920f68b5a40e`  
		Last Modified: Thu, 15 Jun 2023 05:31:54 GMT  
		Size: 2.6 MB (2591727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a390d7486f782e50cf669c00d63e9e5c4e2a02176592204f6dd96ae3d546b11d`  
		Last Modified: Thu, 15 Jun 2023 22:33:02 GMT  
		Size: 1.8 MB (1815781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1303eab0745e53c3b9933cbf741877a18ac2826afa0028c8724d122741f8c118`  
		Last Modified: Thu, 15 Jun 2023 22:33:01 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:904804463bb97c59ab8eb892a966bacaf9a6d985b546099c0d06592ba7d64088`  
		Last Modified: Thu, 15 Jun 2023 22:33:02 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba8b61c2970b103830652f03be8e7e4e3478acec71bf6ed259597e22001409c`  
		Last Modified: Thu, 15 Jun 2023 22:40:38 GMT  
		Size: 10.8 MB (10823764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b92cb02f6a76303c87d97d3bea13d6b159b67354800208c17dd7ed94d6056eb1`  
		Last Modified: Thu, 15 Jun 2023 22:40:38 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff84ac79337750befa72f503b3e4b4c932e9c268852e0ca1830eda0572a4982b`  
		Last Modified: Thu, 15 Jun 2023 22:40:40 GMT  
		Size: 14.8 MB (14810540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203e3df7313912cfb077a0406e81931e9fbb04b0215c963fbc0d6a505f0682df`  
		Last Modified: Thu, 15 Jun 2023 22:40:38 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c0a880ada736ca4854ac3bf5516fb971a6b8a7248b82acf28db5cfd517680ac`  
		Last Modified: Thu, 15 Jun 2023 22:40:38 GMT  
		Size: 18.7 KB (18682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73389474ef6e57b07992d8e8f2e1b7c21c8d0cb246e23544579e1b132a0bb803`  
		Last Modified: Fri, 16 Jun 2023 05:43:55 GMT  
		Size: 9.9 MB (9912587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc9b51d81e2f4aac52e110a5322ab15ffb95e4e5bf99d53895eaa57c61bd33f7`  
		Last Modified: Fri, 16 Jun 2023 05:43:52 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efe0ef634a1bccbf975a01dd22ad1ad9813a5096be328275b88265b147063618`  
		Last Modified: Fri, 16 Jun 2023 05:43:54 GMT  
		Size: 8.4 MB (8438532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac092f04daedd2ea57de55fb57e7bb646af63b0168066b2c63ef04a79b398188`  
		Last Modified: Fri, 16 Jun 2023 05:43:53 GMT  
		Size: 388.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31969d4593539a1f2e79aad5edeebe551dd9361d01cd1d04d4bd8c99a0de803`  
		Last Modified: Fri, 16 Jun 2023 05:43:53 GMT  
		Size: 1.5 MB (1476576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:452d64e7a2159042cb7ffde8cefb275797fd34a4da7cc70a0b8ec2030da85e69`  
		Last Modified: Fri, 16 Jun 2023 05:43:52 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
