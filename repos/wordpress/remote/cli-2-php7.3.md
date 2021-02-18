## `wordpress:cli-2-php7.3`

```console
$ docker pull wordpress@sha256:1d8b445c361263000315d0155efd73452708c2d5b809bc05261ade4dfd9c6a0c
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

### `wordpress:cli-2-php7.3` - linux; amd64

```console
$ docker pull wordpress@sha256:3148ae8fce7d01c2c28c7cf8178357122646db04431cec3eb17c1ce71e2757ea
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 MB (46570272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9f641d5972a1b3f9c66a8ef388a1b6b13352cf6aaa9c1f7f14d4c6f35f57ad8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Thu, 28 Jan 2021 23:19:38 GMT
ADD file:0e2d487cd80773e947c8aae6daad3d565b7bb019a954af2b8bff188681c00d81 in / 
# Thu, 28 Jan 2021 23:19:38 GMT
CMD ["/bin/sh"]
# Fri, 29 Jan 2021 01:09:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 29 Jan 2021 01:09:33 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 29 Jan 2021 01:09:34 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 29 Jan 2021 01:09:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 29 Jan 2021 01:09:35 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 29 Jan 2021 01:09:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 29 Jan 2021 01:09:36 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 29 Jan 2021 01:09:36 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 29 Jan 2021 02:09:44 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Thu, 04 Feb 2021 19:38:31 GMT
ENV PHP_VERSION=7.3.27
# Thu, 04 Feb 2021 19:38:31 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.27.tar.xz.asc
# Thu, 04 Feb 2021 19:38:31 GMT
ENV PHP_SHA256=65f616e2d5b6faacedf62830fa047951b0136d5da34ae59e6744cbaf5dca148d
# Thu, 04 Feb 2021 19:38:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 04 Feb 2021 19:38:36 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 04 Feb 2021 19:49:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 04 Feb 2021 19:49:23 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Thu, 04 Feb 2021 19:49:25 GMT
RUN docker-php-ext-enable sodium
# Thu, 04 Feb 2021 19:49:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Feb 2021 19:49:25 GMT
CMD ["php" "-a"]
# Thu, 04 Feb 2021 23:23:44 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client
# Thu, 04 Feb 2021 23:23:45 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html
# Thu, 04 Feb 2021 23:23:45 GMT
WORKDIR /var/www/html
# Thu, 04 Feb 2021 23:24:47 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype-dir=/usr 		--with-jpeg-dir=/usr 		--with-png-dir=/usr 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		mysqli 		zip 	; 	pecl install imagick-3.4.4; 	docker-php-ext-enable imagick; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps
# Thu, 04 Feb 2021 23:24:48 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Thu, 04 Feb 2021 23:24:48 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Thu, 04 Feb 2021 23:24:48 GMT
ENV WORDPRESS_CLI_VERSION=2.4.0
# Thu, 04 Feb 2021 23:24:48 GMT
ENV WORDPRESS_CLI_SHA512=4049c7e45e14276a70a41c3b0864be7a6a8cfa8ea65ebac8b184a4f503a91baa1a0d29260d03248bc74aef70729824330fb6b396336172a624332e16f64e37ef
# Thu, 04 Feb 2021 23:24:51 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version
# Thu, 04 Feb 2021 23:24:51 GMT
VOLUME [/var/www/html]
# Thu, 04 Feb 2021 23:24:51 GMT
COPY file:b6efa5ff0423d61c2df0c8941b896844a8272d8516cdda0fcae8daaf56baac18 in /usr/local/bin/ 
# Thu, 04 Feb 2021 23:24:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Feb 2021 23:24:52 GMT
USER www-data
# Thu, 04 Feb 2021 23:24:52 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:4c0d98bf9879488e0407f897d9dd4bf758555a78e39675e72b5124ccf12c2580`  
		Last Modified: Thu, 28 Jan 2021 23:20:08 GMT  
		Size: 2.8 MB (2811321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed03eff2d6362e11708d8c6c19ad4c39f85830d917a40c5254ff7f589caa9982`  
		Last Modified: Fri, 29 Jan 2021 02:50:08 GMT  
		Size: 1.7 MB (1694844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa67667da1de1f032c9daa354a18c7525286103540b8f4a884606ccdef49006f`  
		Last Modified: Fri, 29 Jan 2021 02:50:07 GMT  
		Size: 1.2 KB (1229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6961b2fabe936ad3c26fc41f241379caba86b0d660acaf263f971d8d33e4219b`  
		Last Modified: Fri, 29 Jan 2021 02:50:07 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a10a8e0f249e2fa066456cc780662aa12dcea40f87c45df26fff3b3321b735`  
		Last Modified: Thu, 04 Feb 2021 20:51:30 GMT  
		Size: 12.2 MB (12157770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ad69800ee6a25932f5e588906347951bfa16f77aeb3e03085ffc8e515df208a`  
		Last Modified: Thu, 04 Feb 2021 20:51:28 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36515c7f0ca201aecd40b95000b7fb93b016e65780b4e1602b591545b020252`  
		Last Modified: Thu, 04 Feb 2021 20:51:33 GMT  
		Size: 14.5 MB (14456739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097ec8ef5525a6cdaaa98eb3201d76e137e3b382130ebadd18a8e0cf5fd64985`  
		Last Modified: Thu, 04 Feb 2021 20:51:28 GMT  
		Size: 2.3 KB (2267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0d395fad884d6f130601fc7094dae7cd7ed3736ea5dd418d820577b289d6582`  
		Last Modified: Thu, 04 Feb 2021 20:51:28 GMT  
		Size: 17.3 KB (17343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b63676460bb95ae8c67434e7068ca88759fd3434a61a66163b17b04058fe7cc`  
		Last Modified: Thu, 04 Feb 2021 23:30:58 GMT  
		Size: 9.3 MB (9334979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c4695b4941f554a86e22637fd8882d495676c7d02f2deb5d321cf3fd2942a2`  
		Last Modified: Thu, 04 Feb 2021 23:30:54 GMT  
		Size: 145.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4809f0eca48b7893a39bce6372c8f6d11564e26aaa576d47e2b117e3718d6e46`  
		Last Modified: Thu, 04 Feb 2021 23:30:55 GMT  
		Size: 4.9 MB (4886305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e761725a1f7897e1072e0b0ea46d49c718d455987cbb7ef73181f7ba9a7a90fa`  
		Last Modified: Thu, 04 Feb 2021 23:30:53 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0346785d593481c6fca6b7fa23a135831552a1793be36bea60b6a9ba6352ffcd`  
		Last Modified: Thu, 04 Feb 2021 23:30:54 GMT  
		Size: 1.2 MB (1205811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c840b3e08ed5b836394a171f97af7ec7633ebefb44c160d907fb0a2f38c58645`  
		Last Modified: Thu, 04 Feb 2021 23:30:53 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:cli-2-php7.3` - linux; arm variant v6

```console
$ docker pull wordpress@sha256:8d9512d6631bfd315519b7a40ac954e41311a1b3d185d30e5f518eb6cf8c3b2d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44731664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78de74ca9080703bc165cc0956c9d52a5c6cc10face82d6df108994d33b251b0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 17 Feb 2021 20:49:32 GMT
ADD file:c04fbd3b039001c592cfa14f8388f8934ed4223ccf274dbb926e75039e172af4 in / 
# Wed, 17 Feb 2021 20:49:33 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 22:17:10 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 17 Feb 2021 22:17:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 17 Feb 2021 22:17:15 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 17 Feb 2021 22:17:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 17 Feb 2021 22:17:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 17 Feb 2021 22:17:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Feb 2021 22:17:19 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Feb 2021 22:17:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 17 Feb 2021 22:39:00 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Wed, 17 Feb 2021 22:39:00 GMT
ENV PHP_VERSION=7.3.27
# Wed, 17 Feb 2021 22:39:01 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.27.tar.xz.asc
# Wed, 17 Feb 2021 22:39:02 GMT
ENV PHP_SHA256=65f616e2d5b6faacedf62830fa047951b0136d5da34ae59e6744cbaf5dca148d
# Wed, 17 Feb 2021 22:39:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 17 Feb 2021 22:39:10 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 17 Feb 2021 22:44:30 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 17 Feb 2021 22:44:33 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Wed, 17 Feb 2021 22:44:38 GMT
RUN docker-php-ext-enable sodium
# Wed, 17 Feb 2021 22:44:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 17 Feb 2021 22:44:40 GMT
CMD ["php" "-a"]
# Thu, 18 Feb 2021 02:21:15 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client
# Thu, 18 Feb 2021 02:21:17 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html
# Thu, 18 Feb 2021 02:21:18 GMT
WORKDIR /var/www/html
# Thu, 18 Feb 2021 02:22:33 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype-dir=/usr 		--with-jpeg-dir=/usr 		--with-png-dir=/usr 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		mysqli 		zip 	; 	pecl install imagick-3.4.4; 	docker-php-ext-enable imagick; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps
# Thu, 18 Feb 2021 02:22:35 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Thu, 18 Feb 2021 02:22:36 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Thu, 18 Feb 2021 02:22:37 GMT
ENV WORDPRESS_CLI_VERSION=2.4.0
# Thu, 18 Feb 2021 02:22:38 GMT
ENV WORDPRESS_CLI_SHA512=4049c7e45e14276a70a41c3b0864be7a6a8cfa8ea65ebac8b184a4f503a91baa1a0d29260d03248bc74aef70729824330fb6b396336172a624332e16f64e37ef
# Thu, 18 Feb 2021 02:22:42 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version
# Thu, 18 Feb 2021 02:22:43 GMT
VOLUME [/var/www/html]
# Thu, 18 Feb 2021 02:22:43 GMT
COPY file:b6efa5ff0423d61c2df0c8941b896844a8272d8516cdda0fcae8daaf56baac18 in /usr/local/bin/ 
# Thu, 18 Feb 2021 02:22:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Feb 2021 02:22:45 GMT
USER www-data
# Thu, 18 Feb 2021 02:22:46 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:1353527ebe111f9bb1e271264a3c182e909e4b36463f80d7dbde1be0713eb892`  
		Last Modified: Wed, 17 Feb 2021 20:50:06 GMT  
		Size: 2.6 MB (2622039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9a33e390360f607fe5a7fe0a0203b7347693b0d8cab270352594a3700e1a1d0`  
		Last Modified: Wed, 17 Feb 2021 22:57:10 GMT  
		Size: 1.7 MB (1684729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40d1bbb88bd210deaf33702df9d6fa7f35e72f23dfbb55196147ab537320e9f3`  
		Last Modified: Wed, 17 Feb 2021 22:57:09 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b99fbc527c373db47c36282e5bbd82010870902db2af45982bbb8d700375a32`  
		Last Modified: Wed, 17 Feb 2021 22:57:09 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50e0576155ee269d1d7868376fcec4193b77c2e29ca16b0ac14738af3f61868b`  
		Last Modified: Wed, 17 Feb 2021 22:59:38 GMT  
		Size: 12.2 MB (12157775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec32089485012fbb25e2a8efbb09d8f6ddd1aa28477a70de85c4feeddaaf384c`  
		Last Modified: Wed, 17 Feb 2021 22:59:34 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f69feeff7980908ebc2fbbd4a801e5583b70953a23636c42fb7ec781d4da9c73`  
		Last Modified: Wed, 17 Feb 2021 22:59:43 GMT  
		Size: 13.4 MB (13388881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d08fea0a1fd79de2dc33d36ea4a92d8fbc0483eff5a7dc84f8174f02d2e5a80`  
		Last Modified: Wed, 17 Feb 2021 22:59:35 GMT  
		Size: 2.3 KB (2267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:927d3f2d30bdbebb5ca29dc5e2f0538f1146358cc3ed6e8b6411c8404e35957d`  
		Last Modified: Wed, 17 Feb 2021 22:59:34 GMT  
		Size: 17.3 KB (17338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fff9f2ffbe58314b1878c8114f96b240f1341c96d6dc2463a10d3d2c5fead9e`  
		Last Modified: Thu, 18 Feb 2021 02:28:05 GMT  
		Size: 8.9 MB (8943793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6383a386070c885138b3b61c8f19620f1ee1bbadd814b3a43316fd22a58907a7`  
		Last Modified: Thu, 18 Feb 2021 02:28:00 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bb245118308f6e6570b0a37c36ce4245ff984bcbd61a92317cd7b3a2df62bc9`  
		Last Modified: Thu, 18 Feb 2021 02:28:01 GMT  
		Size: 4.7 MB (4706051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08956446583022cdf267af5b8912ff97f3d6183a4de3d30b1fef0cbcd1185941`  
		Last Modified: Thu, 18 Feb 2021 02:28:00 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb6c2f125493e3febc5e2ba16f999a3dc214eff778fa9b85b6a8bef66ab5a44`  
		Last Modified: Thu, 18 Feb 2021 02:28:00 GMT  
		Size: 1.2 MB (1205831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2222f312e134809b93f8e99ce957529a31df0c7378829050b511f803a011281`  
		Last Modified: Thu, 18 Feb 2021 02:28:00 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:cli-2-php7.3` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:9271473e2918bb3da9be68fe4b67146be079bbbb558b45e3378ff1d3dbb11bde
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.0 MB (42957697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:414ddd5f90c842d3b7e10958f2c4ad0dcc62f325322488c2d34c471b05170dff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 17 Feb 2021 20:57:36 GMT
ADD file:efdd39e5243eaf378f12ad5a85d2222b44930850a90263e5f17e8a6b5e9bc9b8 in / 
# Wed, 17 Feb 2021 20:57:37 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 22:56:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 17 Feb 2021 22:57:00 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 17 Feb 2021 22:57:04 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 17 Feb 2021 22:57:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 17 Feb 2021 22:57:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 17 Feb 2021 22:57:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Feb 2021 22:57:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Feb 2021 22:57:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 17 Feb 2021 23:19:06 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Wed, 17 Feb 2021 23:19:07 GMT
ENV PHP_VERSION=7.3.27
# Wed, 17 Feb 2021 23:19:08 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.27.tar.xz.asc
# Wed, 17 Feb 2021 23:19:09 GMT
ENV PHP_SHA256=65f616e2d5b6faacedf62830fa047951b0136d5da34ae59e6744cbaf5dca148d
# Wed, 17 Feb 2021 23:19:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 17 Feb 2021 23:19:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 17 Feb 2021 23:22:25 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 17 Feb 2021 23:22:26 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Wed, 17 Feb 2021 23:22:29 GMT
RUN docker-php-ext-enable sodium
# Wed, 17 Feb 2021 23:22:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 17 Feb 2021 23:22:30 GMT
CMD ["php" "-a"]
# Thu, 18 Feb 2021 03:58:03 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client
# Thu, 18 Feb 2021 03:58:06 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html
# Thu, 18 Feb 2021 03:58:07 GMT
WORKDIR /var/www/html
# Thu, 18 Feb 2021 03:59:18 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype-dir=/usr 		--with-jpeg-dir=/usr 		--with-png-dir=/usr 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		mysqli 		zip 	; 	pecl install imagick-3.4.4; 	docker-php-ext-enable imagick; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps
# Thu, 18 Feb 2021 03:59:20 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Thu, 18 Feb 2021 03:59:21 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Thu, 18 Feb 2021 03:59:22 GMT
ENV WORDPRESS_CLI_VERSION=2.4.0
# Thu, 18 Feb 2021 03:59:22 GMT
ENV WORDPRESS_CLI_SHA512=4049c7e45e14276a70a41c3b0864be7a6a8cfa8ea65ebac8b184a4f503a91baa1a0d29260d03248bc74aef70729824330fb6b396336172a624332e16f64e37ef
# Thu, 18 Feb 2021 03:59:26 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version
# Thu, 18 Feb 2021 03:59:26 GMT
VOLUME [/var/www/html]
# Thu, 18 Feb 2021 03:59:27 GMT
COPY file:b6efa5ff0423d61c2df0c8941b896844a8272d8516cdda0fcae8daaf56baac18 in /usr/local/bin/ 
# Thu, 18 Feb 2021 03:59:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Feb 2021 03:59:28 GMT
USER www-data
# Thu, 18 Feb 2021 03:59:29 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:f55b840e27d3dbe27e44497103a4397f043749f933eb0433d29e2f104b3435ef`  
		Last Modified: Wed, 17 Feb 2021 20:58:14 GMT  
		Size: 2.4 MB (2423892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf491575714634902d01e3e48f3b92702cb2e4c42056aa5421058d2a2cbfd9f6`  
		Last Modified: Wed, 17 Feb 2021 23:33:58 GMT  
		Size: 1.6 MB (1555125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8ae33f1196d3a62a9383b30d3fd81dd4be1bcf1a99a3d928f585b0d85c5408`  
		Last Modified: Wed, 17 Feb 2021 23:33:58 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d16bd16ac2dc3896b7ddf5e8e50bafcc3990d8313dc26634a51beafc97cc6374`  
		Last Modified: Wed, 17 Feb 2021 23:33:58 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9629b131b45727ab352eb7c708d21f26b1a1ca90853dd3acfa5e19d87f1e552`  
		Last Modified: Wed, 17 Feb 2021 23:36:44 GMT  
		Size: 12.2 MB (12157785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4af4353f35f7272a729ab8943fd66ead6518760a65d00e3f1d794ff0a860d3`  
		Last Modified: Wed, 17 Feb 2021 23:36:43 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d982c7de57a74bc981acb4d01c58e25adab6f55ef1c8fc5bb1d2fdf2da90f402`  
		Last Modified: Wed, 17 Feb 2021 23:36:47 GMT  
		Size: 12.5 MB (12534635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd077574a707d44158a7d0bcea4f392b2cbca639663b63164bef4f3331d2d3a`  
		Last Modified: Wed, 17 Feb 2021 23:36:43 GMT  
		Size: 2.3 KB (2262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c33c6b3360974ef56bfc45a6bce22429181c7867913f226956d2bfd8d5d391e`  
		Last Modified: Wed, 17 Feb 2021 23:36:43 GMT  
		Size: 17.3 KB (17326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a59e4b8e4beedc5b813694afe37497229329cc9c089a6a573843f8ff063c182`  
		Last Modified: Thu, 18 Feb 2021 04:06:05 GMT  
		Size: 8.7 MB (8660686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28212d9c7a235e3d8cc75f610480fb579274cbfdc6c48cb504c671dae565f129`  
		Last Modified: Thu, 18 Feb 2021 04:06:00 GMT  
		Size: 145.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48c76c4511ca48a96a22526a09695395993cbe009e86bb89e3e5de4f43e95f7e`  
		Last Modified: Thu, 18 Feb 2021 04:06:02 GMT  
		Size: 4.4 MB (4397209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4147634542958c793e82b3d203cfb92b6b5a63a1caa736b4222f52602f74cd4`  
		Last Modified: Thu, 18 Feb 2021 04:06:00 GMT  
		Size: 392.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6111d22dbc487602b57a03dbfeb2641bd3d5904a4f23115bb060cebffd24b5a1`  
		Last Modified: Thu, 18 Feb 2021 04:06:01 GMT  
		Size: 1.2 MB (1205806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad6164563677cdca7a7f0e4c5ce0a6597fc48e0747542af009fa7429fffdc4b`  
		Last Modified: Thu, 18 Feb 2021 04:06:01 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:cli-2-php7.3` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:029415b37733c1885b0b8f0019dcfc1413bc80d122d5992d02e93f46fcf26370
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46053049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d78f867e87d970c59e4d50b8a6cf243f50a100f0fff952550182540217981e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 17 Feb 2021 20:39:29 GMT
ADD file:3bf1497bd250cf7c73c12231dc4ebe3a3a67f2cd99e35bce47ef6674683aeb1d in / 
# Wed, 17 Feb 2021 20:39:30 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 23:42:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 17 Feb 2021 23:42:33 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 17 Feb 2021 23:42:38 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 17 Feb 2021 23:42:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 17 Feb 2021 23:42:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 17 Feb 2021 23:42:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Feb 2021 23:42:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Feb 2021 23:42:44 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Feb 2021 00:08:23 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Thu, 18 Feb 2021 00:08:24 GMT
ENV PHP_VERSION=7.3.27
# Thu, 18 Feb 2021 00:08:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.27.tar.xz.asc
# Thu, 18 Feb 2021 00:08:25 GMT
ENV PHP_SHA256=65f616e2d5b6faacedf62830fa047951b0136d5da34ae59e6744cbaf5dca148d
# Thu, 18 Feb 2021 00:08:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 18 Feb 2021 00:08:32 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 18 Feb 2021 00:12:00 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 18 Feb 2021 00:12:02 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Thu, 18 Feb 2021 00:12:06 GMT
RUN docker-php-ext-enable sodium
# Thu, 18 Feb 2021 00:12:08 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Feb 2021 00:12:09 GMT
CMD ["php" "-a"]
# Thu, 18 Feb 2021 04:10:15 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client
# Thu, 18 Feb 2021 04:10:17 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html
# Thu, 18 Feb 2021 04:10:18 GMT
WORKDIR /var/www/html
# Thu, 18 Feb 2021 04:11:39 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype-dir=/usr 		--with-jpeg-dir=/usr 		--with-png-dir=/usr 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		mysqli 		zip 	; 	pecl install imagick-3.4.4; 	docker-php-ext-enable imagick; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps
# Thu, 18 Feb 2021 04:11:41 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Thu, 18 Feb 2021 04:11:42 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Thu, 18 Feb 2021 04:11:43 GMT
ENV WORDPRESS_CLI_VERSION=2.4.0
# Thu, 18 Feb 2021 04:11:44 GMT
ENV WORDPRESS_CLI_SHA512=4049c7e45e14276a70a41c3b0864be7a6a8cfa8ea65ebac8b184a4f503a91baa1a0d29260d03248bc74aef70729824330fb6b396336172a624332e16f64e37ef
# Thu, 18 Feb 2021 04:11:47 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version
# Thu, 18 Feb 2021 04:11:48 GMT
VOLUME [/var/www/html]
# Thu, 18 Feb 2021 04:11:49 GMT
COPY file:b6efa5ff0423d61c2df0c8941b896844a8272d8516cdda0fcae8daaf56baac18 in /usr/local/bin/ 
# Thu, 18 Feb 2021 04:11:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Feb 2021 04:11:50 GMT
USER www-data
# Thu, 18 Feb 2021 04:11:51 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:069a56d6d07f6b186fbb82e4486616b9be9a37ce32a63013af6cddcb65898182`  
		Last Modified: Wed, 17 Feb 2021 20:40:04 GMT  
		Size: 2.7 MB (2711572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4b642bcaaef409203aaedc803835562ee86d3ea457bf4ccdd22e5d7b2367f1`  
		Last Modified: Thu, 18 Feb 2021 00:23:35 GMT  
		Size: 1.7 MB (1694455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06ea39643e14bb66b107bb23b02b8c7a193ed89d38f4ae52b1decbe763fb0db9`  
		Last Modified: Thu, 18 Feb 2021 00:23:34 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3455119714d8ce066305d3b121e103a3cf690db26bb556906ba67e7a7c1f559`  
		Last Modified: Thu, 18 Feb 2021 00:23:34 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc483012b435ebcd3f12132cb68870836f0affc40377b25c3ce45a421123ab3`  
		Last Modified: Thu, 18 Feb 2021 00:26:10 GMT  
		Size: 12.2 MB (12157801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1606f180dbbeabd8f2c7b1fff19fa02ca82d3a02ba1a647be8781ee887dc01ad`  
		Last Modified: Thu, 18 Feb 2021 00:26:10 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de50ff1390e4569d07830f69f25c24a6fe1e69f47bf346da28ce3f5c6d7212d6`  
		Last Modified: Thu, 18 Feb 2021 00:26:13 GMT  
		Size: 14.1 MB (14145410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86f64eea0f221980c6e5b25206085f4e7ba5c2587a50643f659cc016e86a87b`  
		Last Modified: Thu, 18 Feb 2021 00:26:09 GMT  
		Size: 2.3 KB (2266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19ba6d51e078116178c28807ba4b7ed4468f657a9dbeeafff659be9b740e36ff`  
		Last Modified: Thu, 18 Feb 2021 00:26:09 GMT  
		Size: 17.3 KB (17348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:671869270a42e34c73771a8d11501ab47b01b32ebbc143c41ee65e97c2dc4754`  
		Last Modified: Thu, 18 Feb 2021 04:18:34 GMT  
		Size: 9.4 MB (9403497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:886d5553e71e7a9fa5436f62bef20b3762c27ff8232b47ecb96942f52bbe5448`  
		Last Modified: Thu, 18 Feb 2021 04:18:30 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34c17538807b5dac137e8daee5a4f5abe223447bc22ddb4943fc60d0017487e9`  
		Last Modified: Thu, 18 Feb 2021 04:18:31 GMT  
		Size: 4.7 MB (4711921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a41eb547930647322e2530f14eeb579b5dea5e4f2ea44aad13155bcaf27ae27a`  
		Last Modified: Thu, 18 Feb 2021 04:18:29 GMT  
		Size: 388.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69244a0806b873681ee33acf196d0ca69a7ef7db1bd0fcca4cfee656e45219bb`  
		Last Modified: Thu, 18 Feb 2021 04:18:31 GMT  
		Size: 1.2 MB (1205816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:427e3e8468c37f0853edadb78c6f3cd9ecb650f973c3f5d7ccac0cf1df945b34`  
		Last Modified: Thu, 18 Feb 2021 04:18:29 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:cli-2-php7.3` - linux; 386

```console
$ docker pull wordpress@sha256:15af00154985f5c62fbebadc5571056d283ea334ba8a4cfeae0a751fbc5c2a98
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47324810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:202d1c3c44e56c200bec579373573a002cee3d821ebd4dd40ab978c30bce5ce7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Thu, 28 Jan 2021 23:38:31 GMT
ADD file:c0e9ea135d66ad6504c77915a7a48b3bead60892d155d3258b746cb4945981c0 in / 
# Thu, 28 Jan 2021 23:38:31 GMT
CMD ["/bin/sh"]
# Fri, 29 Jan 2021 01:16:30 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 29 Jan 2021 01:16:33 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 29 Jan 2021 01:16:34 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 29 Jan 2021 01:16:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 29 Jan 2021 01:16:35 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 29 Jan 2021 01:16:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 29 Jan 2021 01:16:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 29 Jan 2021 01:16:36 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 29 Jan 2021 02:20:53 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Thu, 04 Feb 2021 20:21:31 GMT
ENV PHP_VERSION=7.3.27
# Thu, 04 Feb 2021 20:21:31 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.27.tar.xz.asc
# Thu, 04 Feb 2021 20:21:31 GMT
ENV PHP_SHA256=65f616e2d5b6faacedf62830fa047951b0136d5da34ae59e6744cbaf5dca148d
# Thu, 04 Feb 2021 20:21:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 04 Feb 2021 20:21:36 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 04 Feb 2021 20:33:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 04 Feb 2021 20:33:37 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Thu, 04 Feb 2021 20:33:40 GMT
RUN docker-php-ext-enable sodium
# Thu, 04 Feb 2021 20:33:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Feb 2021 20:33:41 GMT
CMD ["php" "-a"]
# Fri, 05 Feb 2021 00:03:03 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client
# Fri, 05 Feb 2021 00:03:04 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html
# Fri, 05 Feb 2021 00:03:04 GMT
WORKDIR /var/www/html
# Fri, 05 Feb 2021 00:04:02 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype-dir=/usr 		--with-jpeg-dir=/usr 		--with-png-dir=/usr 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		mysqli 		zip 	; 	pecl install imagick-3.4.4; 	docker-php-ext-enable imagick; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps
# Fri, 05 Feb 2021 00:04:03 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Fri, 05 Feb 2021 00:04:03 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Fri, 05 Feb 2021 00:04:03 GMT
ENV WORDPRESS_CLI_VERSION=2.4.0
# Fri, 05 Feb 2021 00:04:03 GMT
ENV WORDPRESS_CLI_SHA512=4049c7e45e14276a70a41c3b0864be7a6a8cfa8ea65ebac8b184a4f503a91baa1a0d29260d03248bc74aef70729824330fb6b396336172a624332e16f64e37ef
# Fri, 05 Feb 2021 00:04:05 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version
# Fri, 05 Feb 2021 00:04:06 GMT
VOLUME [/var/www/html]
# Fri, 05 Feb 2021 00:04:06 GMT
COPY file:b6efa5ff0423d61c2df0c8941b896844a8272d8516cdda0fcae8daaf56baac18 in /usr/local/bin/ 
# Fri, 05 Feb 2021 00:04:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Feb 2021 00:04:06 GMT
USER www-data
# Fri, 05 Feb 2021 00:04:06 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:3fea00a81341ce917db671eb3ad24ef5750cb6928b7f760e3ce4dab619eeb1fa`  
		Last Modified: Thu, 28 Jan 2021 23:39:02 GMT  
		Size: 2.8 MB (2817627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7693c189358487be8693c8f24f54e75dc5e54a6d33edc79a7ddf6851c9f2e670`  
		Last Modified: Fri, 29 Jan 2021 03:00:10 GMT  
		Size: 1.8 MB (1793522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2956bde582e6c6782cd1f42ba90c812f6449eec18badce15706f72fb5fed3db4`  
		Last Modified: Fri, 29 Jan 2021 03:00:07 GMT  
		Size: 1.2 KB (1230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63eb950875108b8e92353d43040a08536210b13d2ea2a265b8a93f88149d556f`  
		Last Modified: Fri, 29 Jan 2021 03:00:08 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab8981bb9ad1626ea2e837d68ea96fbf9697e3d537b535c7521cf8df8f41e334`  
		Last Modified: Thu, 04 Feb 2021 21:22:23 GMT  
		Size: 12.2 MB (12157745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75acc72d3a69b5944730a32b1841cdde28b9e1de8cd41fa8632035531c2a4e2b`  
		Last Modified: Thu, 04 Feb 2021 21:22:21 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1ee251ba944726e272b470ff2259b7f271fa26f06723b9d1990de555e664a93`  
		Last Modified: Thu, 04 Feb 2021 21:22:27 GMT  
		Size: 14.8 MB (14780051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c80c8505ec1bd0fa396450d7ff1c7722e4e9c76121065c46cfe70285ba12b678`  
		Last Modified: Thu, 04 Feb 2021 21:22:21 GMT  
		Size: 2.3 KB (2267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9c76fb9741028561bd6ee2370eb1e749e32bd55cfd2d1438b7cd4cdffcaa37a`  
		Last Modified: Thu, 04 Feb 2021 21:22:21 GMT  
		Size: 17.3 KB (17330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3b5149fd56ee67c81e0a29ee3ef27f2d7138f641cc47a3b8311591adeb49a0b`  
		Last Modified: Fri, 05 Feb 2021 00:09:34 GMT  
		Size: 9.5 MB (9498359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fecaf593be10acf9451b5e7330bdcf460043a7d0ac7e6a65245b4abdeecc054`  
		Last Modified: Fri, 05 Feb 2021 00:09:31 GMT  
		Size: 145.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37f8a2daa2f15d0d9e3dae2a52f00d2cc799e9edb8fb422cf4a5aca74cc0a331`  
		Last Modified: Fri, 05 Feb 2021 00:09:32 GMT  
		Size: 5.0 MB (5049229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:766e239ae9dd10130be88c3eeb2f5b46986c9aa80ef3808bfc18198368fd9207`  
		Last Modified: Fri, 05 Feb 2021 00:09:31 GMT  
		Size: 391.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad640ec0884c74c7a408fec14e8a9e5b5ca1c4a5377bdc665ec5d5b2d751adc6`  
		Last Modified: Fri, 05 Feb 2021 00:09:31 GMT  
		Size: 1.2 MB (1205788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d028a65e6368b3bb04ae18f30e6b1455bac30d90f732c6f1bef7a19009ba990f`  
		Last Modified: Fri, 05 Feb 2021 00:09:30 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:cli-2-php7.3` - linux; ppc64le

```console
$ docker pull wordpress@sha256:ebc54a44d71b9a6e455e098d72ed8ce4cf26c95068142212136accbc98a9462a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47967462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c5e10c4aca8edb88c20924860352eb1aac1ef860a29dabdec652aadd869867`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Thu, 28 Jan 2021 23:55:50 GMT
ADD file:b14fd5f3f7fcd16e2b4ec6932d3e9c07c7400c577cee5fdcb88b0795a70a7bfb in / 
# Thu, 28 Jan 2021 23:55:52 GMT
CMD ["/bin/sh"]
# Fri, 29 Jan 2021 00:47:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 29 Jan 2021 00:47:11 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 29 Jan 2021 00:47:28 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 29 Jan 2021 00:47:35 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 29 Jan 2021 00:47:47 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 29 Jan 2021 00:47:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 29 Jan 2021 00:47:53 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 29 Jan 2021 00:47:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 29 Jan 2021 01:22:35 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Thu, 04 Feb 2021 19:20:34 GMT
ENV PHP_VERSION=7.3.27
# Thu, 04 Feb 2021 19:20:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.27.tar.xz.asc
# Thu, 04 Feb 2021 19:20:48 GMT
ENV PHP_SHA256=65f616e2d5b6faacedf62830fa047951b0136d5da34ae59e6744cbaf5dca148d
# Thu, 04 Feb 2021 19:21:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 04 Feb 2021 19:21:21 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 04 Feb 2021 19:26:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 04 Feb 2021 19:26:21 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Thu, 04 Feb 2021 19:26:33 GMT
RUN docker-php-ext-enable sodium
# Thu, 04 Feb 2021 19:26:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Feb 2021 19:26:53 GMT
CMD ["php" "-a"]
# Fri, 05 Feb 2021 07:57:27 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client
# Fri, 05 Feb 2021 07:57:40 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html
# Fri, 05 Feb 2021 07:57:57 GMT
WORKDIR /var/www/html
# Fri, 05 Feb 2021 07:59:41 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype-dir=/usr 		--with-jpeg-dir=/usr 		--with-png-dir=/usr 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		mysqli 		zip 	; 	pecl install imagick-3.4.4; 	docker-php-ext-enable imagick; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps
# Fri, 05 Feb 2021 08:00:00 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Fri, 05 Feb 2021 08:00:10 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Fri, 05 Feb 2021 08:00:20 GMT
ENV WORDPRESS_CLI_VERSION=2.4.0
# Fri, 05 Feb 2021 08:00:25 GMT
ENV WORDPRESS_CLI_SHA512=4049c7e45e14276a70a41c3b0864be7a6a8cfa8ea65ebac8b184a4f503a91baa1a0d29260d03248bc74aef70729824330fb6b396336172a624332e16f64e37ef
# Fri, 05 Feb 2021 08:00:47 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version
# Fri, 05 Feb 2021 08:00:53 GMT
VOLUME [/var/www/html]
# Fri, 05 Feb 2021 08:00:57 GMT
COPY file:b6efa5ff0423d61c2df0c8941b896844a8272d8516cdda0fcae8daaf56baac18 in /usr/local/bin/ 
# Fri, 05 Feb 2021 08:01:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Feb 2021 08:01:12 GMT
USER www-data
# Fri, 05 Feb 2021 08:01:23 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:f3b94a1d8d591af02f1b419642bee91066ecbb9c65099d6903deed310fd1c2ff`  
		Last Modified: Thu, 28 Jan 2021 23:56:32 GMT  
		Size: 2.8 MB (2812517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9051dfce6625cce4ab1471f70365886b7c23ec19442e08bf3bc297f0a38d57f6`  
		Last Modified: Fri, 29 Jan 2021 01:43:50 GMT  
		Size: 1.7 MB (1741752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82481345688ea8ca47c72ddbbae52d55e215ba3458011ffc13503f16e7caba02`  
		Last Modified: Fri, 29 Jan 2021 01:43:48 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06851413a731c975b7b2d96c8a3ebb2848c57555cf34ab98ca93d7873280b947`  
		Last Modified: Fri, 29 Jan 2021 01:43:47 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd0c3d3afc9d6e7840a7967218d5796c9d043599ee1258f3bb14ff1c876607c5`  
		Last Modified: Thu, 04 Feb 2021 20:09:52 GMT  
		Size: 12.2 MB (12157776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a138eefbdc9a664b31c84887720b526ff05391242f1fe3c53ae21cb5b92425d`  
		Last Modified: Thu, 04 Feb 2021 20:09:51 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d520f14ea63395613030cd5c49cd73a686d1a54527041388cce14b2c0ec75e71`  
		Last Modified: Thu, 04 Feb 2021 20:09:55 GMT  
		Size: 15.5 MB (15518500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1f78e4e7db9903fe46a83ce7321b7792dd991221d3384b0c1ceb16cca082414`  
		Last Modified: Thu, 04 Feb 2021 20:09:51 GMT  
		Size: 2.3 KB (2267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acaaecd8be07f1d4df914d4e81c758fb08c1c2e6d8e8bd9a07c3b72a468f7953`  
		Last Modified: Thu, 04 Feb 2021 20:09:51 GMT  
		Size: 17.3 KB (17340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6568e9c4c131b5d1777cd27ef24608475c8034bb05a2a354d293e84f6af741`  
		Last Modified: Fri, 05 Feb 2021 08:19:13 GMT  
		Size: 9.5 MB (9530512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43c858939daf267219b5614d2b966902c04a16af34067c439891ebf52a1d3ddd`  
		Last Modified: Fri, 05 Feb 2021 08:19:08 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21bea96a1515179648cb49e876fe98d76f571dfdc2b78d4634ea2ed12b2357bb`  
		Last Modified: Fri, 05 Feb 2021 08:19:09 GMT  
		Size: 5.0 MB (4977999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c1682d820e1e8a562f1bb4ad27e7f95bf68a648c47029359f802f769ed8bfeb`  
		Last Modified: Fri, 05 Feb 2021 08:19:08 GMT  
		Size: 391.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeb9b55e5e91dacd33e33f4a607a3cdbfedc0acae6b1e4e4e2199a5c003f40e9`  
		Last Modified: Fri, 05 Feb 2021 08:19:09 GMT  
		Size: 1.2 MB (1205825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964fee6863cf4d0c941eb2b32324e73532b9eddeb6c97a91b59d95dfc719bb4d`  
		Last Modified: Fri, 05 Feb 2021 08:19:08 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:cli-2-php7.3` - linux; s390x

```console
$ docker pull wordpress@sha256:f0a7281e201f8a143262f8dce78489779ca6739cc87cf9dc60bca25cb7bba4dd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46269771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7edb7e91e3c1006d4fc8df998523ce523cf8b5f1db5276d1d6f5cb7eb93b919a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 17 Feb 2021 20:41:27 GMT
ADD file:630c66f8d774d75b51e32aff812b438d377ebd3389c4aa6c324fdf8c03b6fa13 in / 
# Wed, 17 Feb 2021 20:41:27 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 00:40:26 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 18 Feb 2021 00:40:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 18 Feb 2021 00:40:31 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 18 Feb 2021 00:40:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Feb 2021 00:40:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 18 Feb 2021 00:40:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Feb 2021 00:40:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Feb 2021 00:40:35 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Feb 2021 01:08:19 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Thu, 18 Feb 2021 01:08:20 GMT
ENV PHP_VERSION=7.3.27
# Thu, 18 Feb 2021 01:08:20 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.27.tar.xz.asc
# Thu, 18 Feb 2021 01:08:21 GMT
ENV PHP_SHA256=65f616e2d5b6faacedf62830fa047951b0136d5da34ae59e6744cbaf5dca148d
# Thu, 18 Feb 2021 01:08:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 18 Feb 2021 01:08:28 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 18 Feb 2021 01:13:07 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 18 Feb 2021 01:13:11 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Thu, 18 Feb 2021 01:13:13 GMT
RUN docker-php-ext-enable sodium
# Thu, 18 Feb 2021 01:13:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Feb 2021 01:13:14 GMT
CMD ["php" "-a"]
# Thu, 18 Feb 2021 03:24:18 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client
# Thu, 18 Feb 2021 03:24:21 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html
# Thu, 18 Feb 2021 03:24:21 GMT
WORKDIR /var/www/html
# Thu, 18 Feb 2021 03:25:31 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype-dir=/usr 		--with-jpeg-dir=/usr 		--with-png-dir=/usr 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		mysqli 		zip 	; 	pecl install imagick-3.4.4; 	docker-php-ext-enable imagick; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps
# Thu, 18 Feb 2021 03:25:33 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Thu, 18 Feb 2021 03:25:34 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Thu, 18 Feb 2021 03:25:34 GMT
ENV WORDPRESS_CLI_VERSION=2.4.0
# Thu, 18 Feb 2021 03:25:35 GMT
ENV WORDPRESS_CLI_SHA512=4049c7e45e14276a70a41c3b0864be7a6a8cfa8ea65ebac8b184a4f503a91baa1a0d29260d03248bc74aef70729824330fb6b396336172a624332e16f64e37ef
# Thu, 18 Feb 2021 03:25:38 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version
# Thu, 18 Feb 2021 03:25:39 GMT
VOLUME [/var/www/html]
# Thu, 18 Feb 2021 03:25:40 GMT
COPY file:b6efa5ff0423d61c2df0c8941b896844a8272d8516cdda0fcae8daaf56baac18 in /usr/local/bin/ 
# Thu, 18 Feb 2021 03:25:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Feb 2021 03:25:40 GMT
USER www-data
# Thu, 18 Feb 2021 03:25:41 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:ff5e8cb87555e9fa38a441f5cf0414e91353e2cd21cdb48d48b7de5bb39ce674`  
		Last Modified: Wed, 17 Feb 2021 20:41:58 GMT  
		Size: 2.6 MB (2602381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b2eaf748a32e76be0f1aa6246cb11c8aa5022aa834df364bb87f581198e6376`  
		Last Modified: Thu, 18 Feb 2021 01:26:48 GMT  
		Size: 1.8 MB (1756400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5716be54c61b8e2a38b4d6a0cbece88801726747842f6bd1a50aaf4e8442013f`  
		Last Modified: Thu, 18 Feb 2021 01:26:48 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6aa66a8dad4ec1443c27324fc452b05c4299dbffefcebee55700880033b3ff7`  
		Last Modified: Thu, 18 Feb 2021 01:26:47 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4386739cd9730c5a4ea8b284ac4ee92e51e29c2074338d34429d4782284aea4`  
		Last Modified: Thu, 18 Feb 2021 01:29:22 GMT  
		Size: 12.2 MB (12157778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c03a0b0abe522899ec19f204239f071a918e7e8dc36073c349c318a6c873f48f`  
		Last Modified: Thu, 18 Feb 2021 01:29:21 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df91b094d6423a332e4f67360effc42c8e5263846323d5204d3f3be187f42e7`  
		Last Modified: Thu, 18 Feb 2021 01:29:24 GMT  
		Size: 13.8 MB (13836043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:724da77b08336c628f3c17b6d36c272925cad7c5f6172da67ab9b9636b122672`  
		Last Modified: Thu, 18 Feb 2021 01:29:21 GMT  
		Size: 2.3 KB (2265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1264dd566b77b174644c34fe1a8491deca53bd1f27e41b00455d5bcccc5335a9`  
		Last Modified: Thu, 18 Feb 2021 01:29:21 GMT  
		Size: 17.3 KB (17338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcba3b8dbfe8fb5ee715fdbcf613a69b7cdf31e31220c55d4e8d316310ceef27`  
		Last Modified: Thu, 18 Feb 2021 03:31:34 GMT  
		Size: 9.8 MB (9829897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b4902601940f8138ff00790d23a206ff22011e3229aeca4303bb573a1cdd8d`  
		Last Modified: Thu, 18 Feb 2021 03:31:31 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b0d224f358a07ec7b5baa0f0f992ef5138bca0bed0e0b37e4eb342837eb517f`  
		Last Modified: Thu, 18 Feb 2021 03:31:32 GMT  
		Size: 4.9 MB (4858913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7793f3fbef678ea6f73ad611fae702076a81943825def08b3de1fad39b65ec9f`  
		Last Modified: Thu, 18 Feb 2021 03:31:31 GMT  
		Size: 391.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a3ca0520ef980ce6a0756321dbaa7e274dd13bf2660cc179fa6ab9409378b8d`  
		Last Modified: Thu, 18 Feb 2021 03:31:31 GMT  
		Size: 1.2 MB (1205792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a735d57dde21e1182883e4e287f27e82e162d1002d8cc9ebd9c37856e11c504f`  
		Last Modified: Thu, 18 Feb 2021 03:31:31 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
