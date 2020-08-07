## `wordpress:cli-2-php7.3`

```console
$ docker pull wordpress@sha256:ce275979c4084c1e32fd62eff307cf94952ef7a6e0896dbc3a05e12f498f53b5
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
$ docker pull wordpress@sha256:18c3246d3d7057e9636e63e25ea5beb57acffd334f1a816aaea75f3249680481
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48594129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18a3d19f13b0cbc083e64f99dc30d3af61ff4b650249cdc30be5223f11e799b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Thu, 11 Jun 2020 18:51:57 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 11 Jun 2020 18:51:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 11 Jun 2020 18:51:59 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 11 Jun 2020 18:51:59 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jun 2020 18:52:00 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 11 Jun 2020 18:52:00 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2020 18:52:00 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2020 18:52:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jun 2020 20:49:33 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Thu, 06 Aug 2020 21:28:37 GMT
ENV PHP_VERSION=7.3.21
# Thu, 06 Aug 2020 21:28:37 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.21.tar.xz.asc
# Thu, 06 Aug 2020 21:28:38 GMT
ENV PHP_SHA256=4c8b065746ef776d84b7ae47908c21a79e3d4704b86b60d816716b8697c58ce9 PHP_MD5=
# Thu, 06 Aug 2020 21:28:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 06 Aug 2020 21:28:43 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 06 Aug 2020 21:37:08 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 06 Aug 2020 21:37:09 GMT
COPY multi:cfe027e655535d9b3eb4b44f84eafb2e1d257620ca628247fe5c1c4fb008a78a in /usr/local/bin/ 
# Thu, 06 Aug 2020 21:37:10 GMT
RUN docker-php-ext-enable sodium
# Thu, 06 Aug 2020 21:37:11 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 06 Aug 2020 21:37:11 GMT
CMD ["php" "-a"]
# Fri, 07 Aug 2020 03:02:26 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 	; 		docker-php-ext-configure gd --with-freetype-dir=/usr --with-jpeg-dir=/usr --with-png-dir=/usr; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		mysqli 		zip 	; 	pecl install imagick-3.4.4; 	docker-php-ext-enable imagick; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del .build-deps
# Fri, 07 Aug 2020 03:02:27 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Fri, 07 Aug 2020 03:02:29 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client
# Fri, 07 Aug 2020 03:02:30 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html
# Fri, 07 Aug 2020 03:02:30 GMT
WORKDIR /var/www/html
# Fri, 07 Aug 2020 03:02:30 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Fri, 07 Aug 2020 03:02:30 GMT
ENV WORDPRESS_CLI_VERSION=2.4.0
# Fri, 07 Aug 2020 03:02:31 GMT
ENV WORDPRESS_CLI_SHA512=4049c7e45e14276a70a41c3b0864be7a6a8cfa8ea65ebac8b184a4f503a91baa1a0d29260d03248bc74aef70729824330fb6b396336172a624332e16f64e37ef
# Fri, 07 Aug 2020 03:02:33 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fSL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del .fetch-deps; 		wp --allow-root --version
# Fri, 07 Aug 2020 03:02:33 GMT
VOLUME [/var/www/html]
# Fri, 07 Aug 2020 03:02:33 GMT
COPY file:7798dc600ff57df68d7de781fd8834d5a9371b2ab13ab9649086b34ee0e38fcf in /usr/local/bin/ 
# Fri, 07 Aug 2020 03:02:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Aug 2020 03:02:34 GMT
USER www-data
# Fri, 07 Aug 2020 03:02:34 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b358d6dbbdff5c10cbe23c608b7ff9c6d1dd13331dd7dc7644b727ca5ea8e742`  
		Last Modified: Thu, 11 Jun 2020 22:14:55 GMT  
		Size: 1.3 MB (1340817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0232d962484c6b9a1caa33a12f1beed4cb20996085056b4fb1591a9fd1d8c89f`  
		Last Modified: Thu, 11 Jun 2020 22:14:54 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c1d3ac04d2af7a9f0eee25eccc72e586400051054ffb4aff7cdf2f4ebc993e8`  
		Last Modified: Thu, 11 Jun 2020 22:14:54 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efc30832947e06887994615bd22efd06a9e5d9a397b8d313c31191902b02c142`  
		Last Modified: Fri, 07 Aug 2020 00:28:52 GMT  
		Size: 12.1 MB (12142641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab60efd6c97679325b2a6618679dd8786918b98eaa070b275cf6f72fd4d5f91`  
		Last Modified: Fri, 07 Aug 2020 00:28:49 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4704cdabb1dd1fd663a27ddec00b6f604c653c819ce7f0f60530af38bf800109`  
		Last Modified: Fri, 07 Aug 2020 00:28:54 GMT  
		Size: 14.8 MB (14785741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82c8c75dababe0fc6f49ef651a5494665989eebe6fa212783320c0e24fde8485`  
		Last Modified: Fri, 07 Aug 2020 00:28:49 GMT  
		Size: 2.3 KB (2273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014c05f2ea6d572253bb7b3025620709b019b30bf1ac99bd425c1572b9b787e9`  
		Last Modified: Fri, 07 Aug 2020 00:28:49 GMT  
		Size: 16.8 KB (16790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b5b768ccba36260b7567a5a714dc92cc55572f459544a5691556a3794cb1480`  
		Last Modified: Fri, 07 Aug 2020 03:07:20 GMT  
		Size: 7.0 MB (7020616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e17b7a97eec428abad67c605998028a384dcd2c077e0bc8ca3ce2fd3e3a775d`  
		Last Modified: Fri, 07 Aug 2020 03:07:18 GMT  
		Size: 391.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd48cb6bc6e378a11f1d780456523b12b2d1c0272c7daf70ec226f6ae9d05f64`  
		Last Modified: Fri, 07 Aug 2020 03:07:19 GMT  
		Size: 9.3 MB (9279567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d26e7ddfe56574f3cc60b42f04f15be49ba783e2abaa82b15025281527da61d`  
		Last Modified: Fri, 07 Aug 2020 03:07:17 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89f7361b7306216f40f6b9e572208a9d30383e40f608cad57388c886b68bc00`  
		Last Modified: Fri, 07 Aug 2020 03:07:18 GMT  
		Size: 1.2 MB (1205241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b698a91c7dd8bc8d5a363be7bfde4171447fd1d1d0e28d31404e34ca21babfa`  
		Last Modified: Fri, 07 Aug 2020 03:07:17 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:cli-2-php7.3` - linux; arm variant v6

```console
$ docker pull wordpress@sha256:2b7a6de170f9bfe0285facc4862670bd39453f47f187955ce248744f02283d94
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46544242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5df87e9b7b5478472ce8e4cbcc342c96517b2fd1a3a09488d687b5384dec04cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Fri, 29 May 2020 21:50:55 GMT
ADD file:f46e997a56849423db17e5fc9f0249ab6c73b155245927dba5fcb9dfd65f622f in / 
# Fri, 29 May 2020 21:50:56 GMT
CMD ["/bin/sh"]
# Thu, 11 Jun 2020 18:14:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 11 Jun 2020 18:14:50 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 11 Jun 2020 18:14:52 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 11 Jun 2020 18:14:53 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jun 2020 18:14:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 11 Jun 2020 18:14:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2020 18:14:57 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2020 18:14:57 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jun 2020 18:44:36 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Thu, 06 Aug 2020 19:17:58 GMT
ENV PHP_VERSION=7.3.21
# Thu, 06 Aug 2020 19:18:10 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.21.tar.xz.asc
# Thu, 06 Aug 2020 19:18:24 GMT
ENV PHP_SHA256=4c8b065746ef776d84b7ae47908c21a79e3d4704b86b60d816716b8697c58ce9 PHP_MD5=
# Thu, 06 Aug 2020 19:19:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 06 Aug 2020 19:19:32 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 06 Aug 2020 19:25:18 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 06 Aug 2020 19:25:54 GMT
COPY multi:cfe027e655535d9b3eb4b44f84eafb2e1d257620ca628247fe5c1c4fb008a78a in /usr/local/bin/ 
# Thu, 06 Aug 2020 19:26:32 GMT
RUN docker-php-ext-enable sodium
# Thu, 06 Aug 2020 19:26:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 06 Aug 2020 19:26:55 GMT
CMD ["php" "-a"]
# Fri, 07 Aug 2020 03:18:14 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 	; 		docker-php-ext-configure gd --with-freetype-dir=/usr --with-jpeg-dir=/usr --with-png-dir=/usr; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		mysqli 		zip 	; 	pecl install imagick-3.4.4; 	docker-php-ext-enable imagick; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del .build-deps
# Fri, 07 Aug 2020 03:19:26 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Fri, 07 Aug 2020 03:21:20 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client
# Fri, 07 Aug 2020 03:22:50 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html
# Fri, 07 Aug 2020 03:23:09 GMT
WORKDIR /var/www/html
# Fri, 07 Aug 2020 03:23:24 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Fri, 07 Aug 2020 03:23:40 GMT
ENV WORDPRESS_CLI_VERSION=2.4.0
# Fri, 07 Aug 2020 03:23:55 GMT
ENV WORDPRESS_CLI_SHA512=4049c7e45e14276a70a41c3b0864be7a6a8cfa8ea65ebac8b184a4f503a91baa1a0d29260d03248bc74aef70729824330fb6b396336172a624332e16f64e37ef
# Fri, 07 Aug 2020 03:25:03 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fSL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del .fetch-deps; 		wp --allow-root --version
# Fri, 07 Aug 2020 03:25:18 GMT
VOLUME [/var/www/html]
# Fri, 07 Aug 2020 03:25:40 GMT
COPY file:7798dc600ff57df68d7de781fd8834d5a9371b2ab13ab9649086b34ee0e38fcf in /usr/local/bin/ 
# Fri, 07 Aug 2020 03:25:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Aug 2020 03:26:05 GMT
USER www-data
# Fri, 07 Aug 2020 03:26:26 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:b4b72e716706d29f5d2351709c20bf737b94f876a5472a43ff1b6e203c65d27f`  
		Last Modified: Fri, 29 May 2020 21:51:30 GMT  
		Size: 2.6 MB (2603286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72788d65e292354c2ce4b67441d334d0ba534db5ce71d5b8bf78011a256b566f`  
		Last Modified: Thu, 11 Jun 2020 19:29:37 GMT  
		Size: 1.3 MB (1310273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e32d62de43da999aca07cf15fdbe1cd6b03aebc88c15409c3463daadf13e01`  
		Last Modified: Thu, 11 Jun 2020 19:29:36 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6701e05673b745147608cd1b6eb47a3fbc35bcfd8a65bc536e5b9f919b3d0e77`  
		Last Modified: Thu, 11 Jun 2020 19:29:36 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f278bcf73a3dc4100c19f714464c4bcc8c592aad389f2447ee9fc69b084109`  
		Last Modified: Thu, 06 Aug 2020 21:08:11 GMT  
		Size: 12.1 MB (12142669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a6f092a472735f3fa7d389bb5811479a41ea88efcd3fe14635d1b704d9958b5`  
		Last Modified: Thu, 06 Aug 2020 21:08:11 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c93fcbfdbf43e678a9eee43a8cda8cc3eb34d8dd8c77b7b9c75473d1816e22a`  
		Last Modified: Thu, 06 Aug 2020 21:08:13 GMT  
		Size: 13.7 MB (13742674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34dffa0a8827d7c47d3894775098414e53b646864c36d4c7ce8198117828e54a`  
		Last Modified: Thu, 06 Aug 2020 21:08:10 GMT  
		Size: 2.3 KB (2276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c32325fcde54e299dea06de70debe5fd2182054a1d606c79b3064894ec14510`  
		Last Modified: Thu, 06 Aug 2020 21:08:11 GMT  
		Size: 16.8 KB (16791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb706b29e4728fd148248d5a10ff62aa34efcfb4614010db01a2529d77b5a8d9`  
		Last Modified: Fri, 07 Aug 2020 03:41:11 GMT  
		Size: 6.6 MB (6647850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9795505feda658ad64b610a89c8ece968a829c1b7cb7c9f2dce12bf5f65a47e5`  
		Last Modified: Fri, 07 Aug 2020 03:41:05 GMT  
		Size: 392.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db663de261934e1678e1ff29f53b99848b85c048e3b80604817372c64ca46b60`  
		Last Modified: Fri, 07 Aug 2020 03:41:08 GMT  
		Size: 8.9 MB (8870099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3624609c16772866bd3924beb9ec7c4f471ef62b26d6aa008ba611a8f8ac1e1`  
		Last Modified: Fri, 07 Aug 2020 03:41:05 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d5c1915a50333acd95cd6a535a93fdf3678da57ab661dbc36e97ccfb094f9e7`  
		Last Modified: Fri, 07 Aug 2020 03:41:05 GMT  
		Size: 1.2 MB (1205339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b53c5bfa8462c8cbce1117a8f56da4b7c500c692be7f413e672209b3f6eb0a51`  
		Last Modified: Fri, 07 Aug 2020 03:41:06 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:cli-2-php7.3` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:c6b3077856e1d62a3748073bfacb9191991c354e039f78d1543cef5b67c2db1d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44904670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85b032b5e18c4644a7630ec7242cb62093b2d9bc26ff8f0c9fd83c1b0ca0c396`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Fri, 29 May 2020 21:02:07 GMT
ADD file:e97bf0d217846312b19a9f7264604851aedd125c23b4d291eed4c69b880dce26 in / 
# Fri, 29 May 2020 21:02:08 GMT
CMD ["/bin/sh"]
# Thu, 11 Jun 2020 18:34:59 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 11 Jun 2020 18:35:04 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 11 Jun 2020 18:35:07 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 11 Jun 2020 18:35:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jun 2020 18:35:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 11 Jun 2020 18:35:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2020 18:35:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2020 18:35:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jun 2020 19:35:34 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Thu, 09 Jul 2020 23:39:59 GMT
ENV PHP_VERSION=7.3.20
# Thu, 09 Jul 2020 23:40:00 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.20.tar.xz.asc
# Thu, 09 Jul 2020 23:40:01 GMT
ENV PHP_SHA256=43292046f6684eb13acb637276d4aa1dd9f66b0b7045e6f1493bc90db389b888 PHP_MD5=
# Thu, 09 Jul 2020 23:40:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 09 Jul 2020 23:40:10 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 09 Jul 2020 23:42:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 09 Jul 2020 23:43:00 GMT
COPY multi:cfe027e655535d9b3eb4b44f84eafb2e1d257620ca628247fe5c1c4fb008a78a in /usr/local/bin/ 
# Thu, 09 Jul 2020 23:43:02 GMT
RUN docker-php-ext-enable sodium
# Thu, 09 Jul 2020 23:43:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 09 Jul 2020 23:43:03 GMT
CMD ["php" "-a"]
# Fri, 10 Jul 2020 04:29:09 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 	; 		docker-php-ext-configure gd --with-freetype-dir=/usr --with-jpeg-dir=/usr --with-png-dir=/usr; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		mysqli 		zip 	; 	pecl install imagick-3.4.4; 	docker-php-ext-enable imagick; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del .build-deps
# Fri, 10 Jul 2020 04:29:13 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Fri, 10 Jul 2020 04:29:17 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client
# Fri, 10 Jul 2020 04:29:20 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html
# Fri, 10 Jul 2020 04:29:21 GMT
WORKDIR /var/www/html
# Fri, 10 Jul 2020 04:29:22 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Fri, 10 Jul 2020 04:29:23 GMT
ENV WORDPRESS_CLI_VERSION=2.4.0
# Fri, 10 Jul 2020 04:29:24 GMT
ENV WORDPRESS_CLI_SHA512=4049c7e45e14276a70a41c3b0864be7a6a8cfa8ea65ebac8b184a4f503a91baa1a0d29260d03248bc74aef70729824330fb6b396336172a624332e16f64e37ef
# Fri, 10 Jul 2020 04:29:27 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fSL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del .fetch-deps; 		wp --allow-root --version
# Fri, 10 Jul 2020 04:29:28 GMT
VOLUME [/var/www/html]
# Fri, 10 Jul 2020 04:29:29 GMT
COPY file:7798dc600ff57df68d7de781fd8834d5a9371b2ab13ab9649086b34ee0e38fcf in /usr/local/bin/ 
# Fri, 10 Jul 2020 04:29:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Jul 2020 04:29:30 GMT
USER www-data
# Fri, 10 Jul 2020 04:29:31 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:52278dd8e57993669c5b72a9620e89bebdc098f2af2379caaa8945f7403f77a2`  
		Last Modified: Fri, 29 May 2020 21:02:38 GMT  
		Size: 2.4 MB (2406763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d5b4230297ea0028dae43acf7e134a55e11ebc15c53a61a2c0c72935dd0ed35`  
		Last Modified: Thu, 11 Jun 2020 20:13:04 GMT  
		Size: 1.2 MB (1214376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779feafcddcba2692e3d187a609b90060e7deea16e8b629aada3a236e99c40f7`  
		Last Modified: Thu, 11 Jun 2020 20:13:04 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23b20c0367792ccffce00af872fa2ea0300330509fb8c15fe5c08905d7db739`  
		Last Modified: Thu, 11 Jun 2020 20:13:03 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:357a491a5c093bbd29ee13629161275e7db9641a2c1a5134ce7b6d6df32d3756`  
		Last Modified: Fri, 10 Jul 2020 01:11:01 GMT  
		Size: 12.1 MB (12137658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90eb98f0c9a11bee63294d41aa03e39e834393dc545a3f6ed79b8a640c47ab13`  
		Last Modified: Fri, 10 Jul 2020 01:11:00 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a5c6cb457f2705cf8766cca4724f60214d491f3b3a2c634e85971161ca07b2`  
		Last Modified: Fri, 10 Jul 2020 01:11:05 GMT  
		Size: 12.9 MB (12858790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6c6e2b0253cd6faf7a18ec1f0280a001e8c7791b496b671d58448faf32bda7`  
		Last Modified: Fri, 10 Jul 2020 01:11:00 GMT  
		Size: 2.3 KB (2271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c856d7fbd21836b293ccf134501fa0587d3648c8eb18d687db9ab93bcba5cf81`  
		Last Modified: Fri, 10 Jul 2020 01:11:00 GMT  
		Size: 16.8 KB (16774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90f261e84e3e8ed917d6be1b22902598ba9bb190061c6b2abce19dad2a3f4abb`  
		Last Modified: Fri, 10 Jul 2020 04:35:43 GMT  
		Size: 6.5 MB (6453555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96605fb2a096d0db01832354300f7fbe9b8ca2f64acdf94b858e4ec333bc4844`  
		Last Modified: Fri, 10 Jul 2020 04:35:39 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58715cedfbc06fd0f66f2426c5a28b6bb5df624393676dce7a62b0a67daad800`  
		Last Modified: Fri, 10 Jul 2020 04:35:40 GMT  
		Size: 8.6 MB (8606209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e62791ba313f86f69206607d2a5f109f46247f529cded6efc63db4ff35ceb5f5`  
		Last Modified: Fri, 10 Jul 2020 04:35:39 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c411d7c2b226a9ada414bb63266c1df8316a2468aa36c060d562874af25b17f6`  
		Last Modified: Fri, 10 Jul 2020 04:35:39 GMT  
		Size: 1.2 MB (1205298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5845719ea2d09a82e89c725bff45074a3a5583a86688abdf4ac51c1098c0704`  
		Last Modified: Fri, 10 Jul 2020 04:35:39 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:cli-2-php7.3` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:76158e76767ad48ccb75c16359473a30b887df501fc82fb59e346cccd2e88acb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48127160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e323cc95077f91ef66141c8943408dd429a394b52cda767922dd1b07a9ea6c3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Fri, 29 May 2020 21:43:19 GMT
ADD file:7574aee4e37a85460ab889212d52912723a9b30dda1c060548f0deb4a05fc398 in / 
# Fri, 29 May 2020 21:43:20 GMT
CMD ["/bin/sh"]
# Thu, 11 Jun 2020 18:40:23 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 11 Jun 2020 18:40:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 11 Jun 2020 18:40:31 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 11 Jun 2020 18:40:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jun 2020 18:40:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 11 Jun 2020 18:40:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2020 18:40:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2020 18:40:36 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jun 2020 19:48:46 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Thu, 06 Aug 2020 20:36:26 GMT
ENV PHP_VERSION=7.3.21
# Thu, 06 Aug 2020 20:36:36 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.21.tar.xz.asc
# Thu, 06 Aug 2020 20:36:42 GMT
ENV PHP_SHA256=4c8b065746ef776d84b7ae47908c21a79e3d4704b86b60d816716b8697c58ce9 PHP_MD5=
# Thu, 06 Aug 2020 20:37:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 06 Aug 2020 20:37:12 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 06 Aug 2020 20:40:45 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 06 Aug 2020 20:40:54 GMT
COPY multi:cfe027e655535d9b3eb4b44f84eafb2e1d257620ca628247fe5c1c4fb008a78a in /usr/local/bin/ 
# Thu, 06 Aug 2020 20:41:15 GMT
RUN docker-php-ext-enable sodium
# Thu, 06 Aug 2020 20:41:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 06 Aug 2020 20:41:19 GMT
CMD ["php" "-a"]
# Fri, 07 Aug 2020 05:48:55 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 	; 		docker-php-ext-configure gd --with-freetype-dir=/usr --with-jpeg-dir=/usr --with-png-dir=/usr; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		mysqli 		zip 	; 	pecl install imagick-3.4.4; 	docker-php-ext-enable imagick; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del .build-deps
# Fri, 07 Aug 2020 05:48:57 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Fri, 07 Aug 2020 05:49:00 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client
# Fri, 07 Aug 2020 05:49:02 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html
# Fri, 07 Aug 2020 05:49:03 GMT
WORKDIR /var/www/html
# Fri, 07 Aug 2020 05:49:05 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Fri, 07 Aug 2020 05:49:06 GMT
ENV WORDPRESS_CLI_VERSION=2.4.0
# Fri, 07 Aug 2020 05:49:07 GMT
ENV WORDPRESS_CLI_SHA512=4049c7e45e14276a70a41c3b0864be7a6a8cfa8ea65ebac8b184a4f503a91baa1a0d29260d03248bc74aef70729824330fb6b396336172a624332e16f64e37ef
# Fri, 07 Aug 2020 05:49:11 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fSL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del .fetch-deps; 		wp --allow-root --version
# Fri, 07 Aug 2020 05:49:12 GMT
VOLUME [/var/www/html]
# Fri, 07 Aug 2020 05:49:12 GMT
COPY file:7798dc600ff57df68d7de781fd8834d5a9371b2ab13ab9649086b34ee0e38fcf in /usr/local/bin/ 
# Fri, 07 Aug 2020 05:49:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Aug 2020 05:49:14 GMT
USER www-data
# Fri, 07 Aug 2020 05:49:14 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:b538f80385f9b48122e3da068c932a96ea5018afa3c7be79da00437414bd18cd`  
		Last Modified: Fri, 29 May 2020 21:43:57 GMT  
		Size: 2.7 MB (2707964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dee09877319de284b8141c396485111447d75eb8cf26c68819f92f85a4de5649`  
		Last Modified: Thu, 11 Jun 2020 20:30:06 GMT  
		Size: 1.3 MB (1342990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bad472a11fde1c83808bc84cc9c77da0743b9974bb8c51ab25ed0608cbb4558`  
		Last Modified: Thu, 11 Jun 2020 20:30:06 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72fca52dcdf28b691bbc24b2e2aff931667b865a9188287ef18af016712d3a0f`  
		Last Modified: Thu, 11 Jun 2020 20:30:05 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b97044c72df561f484cd3ef7957136141a6db817ce07db15df6a6e90d1ba62f`  
		Last Modified: Thu, 06 Aug 2020 23:34:24 GMT  
		Size: 12.1 MB (12142680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d9d4396ee83c88fc2f15946d98c1b60d9f9d21b41025e6a0e634394a27cd51c`  
		Last Modified: Thu, 06 Aug 2020 23:34:24 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53e5c83247ed181986d5756b2fde4825d66a55e5e3fe6d2170efb20c87147d5`  
		Last Modified: Thu, 06 Aug 2020 23:34:28 GMT  
		Size: 14.5 MB (14523463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:924b387dd15feb49525b4a412b10cc02db9c5e30151fd96b36c1376da0e7723d`  
		Last Modified: Thu, 06 Aug 2020 23:34:24 GMT  
		Size: 2.3 KB (2274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:183ca32a9045b46927f27170b8a512c9f7d690b31ba563deca988001cb640f75`  
		Last Modified: Thu, 06 Aug 2020 23:34:24 GMT  
		Size: 16.8 KB (16802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:701383753b09cd38055c748d04fb2c479e7e6104b991b844ec619e6aad7d8ab8`  
		Last Modified: Fri, 07 Aug 2020 05:56:01 GMT  
		Size: 6.8 MB (6846923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6603731b545e8af4e394afd0c48406050ab9c28dbd01dde2ed37ddc94b001ddb`  
		Last Modified: Fri, 07 Aug 2020 05:55:57 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9db4ca003d4f6396487a9538a6f2b10390b20efda92a62fa0a89daf44bc672e`  
		Last Modified: Fri, 07 Aug 2020 05:56:00 GMT  
		Size: 9.3 MB (9335829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6a2b30fbd630ef6769e8cb4150fcc740249058643e3fe804abc72d6a1d265ad`  
		Last Modified: Fri, 07 Aug 2020 05:55:57 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3916f482df06f04fd6263c9d7a0515e0f0b7a29c1aa7c64a21a9fe769f180e53`  
		Last Modified: Fri, 07 Aug 2020 05:55:58 GMT  
		Size: 1.2 MB (1205255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b9e6366c6febbff9444e9684cbf6832f4a2f592cf667db9a31e295c5447dcf`  
		Last Modified: Fri, 07 Aug 2020 05:55:57 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:cli-2-php7.3` - linux; 386

```console
$ docker pull wordpress@sha256:d92676a51e9f1e10e75578e42aa8d6de025e7efc4e484d70b388374741b773a2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49328219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87fb095df74dd8b60e5b61ec45e937250864d8e8d6b1b17752e3a2e9dfdd491a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Fri, 29 May 2020 21:38:33 GMT
ADD file:5624441d97aca5eeb82a582941efc3586397098b8391227a9040ebe434cc1d6b in / 
# Fri, 29 May 2020 21:38:33 GMT
CMD ["/bin/sh"]
# Thu, 11 Jun 2020 18:53:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 11 Jun 2020 18:53:04 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 11 Jun 2020 18:53:06 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 11 Jun 2020 18:53:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jun 2020 18:53:08 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 11 Jun 2020 18:53:08 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2020 18:53:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2020 18:53:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jun 2020 21:00:00 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Thu, 06 Aug 2020 21:42:38 GMT
ENV PHP_VERSION=7.3.21
# Thu, 06 Aug 2020 21:42:39 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.21.tar.xz.asc
# Thu, 06 Aug 2020 21:42:39 GMT
ENV PHP_SHA256=4c8b065746ef776d84b7ae47908c21a79e3d4704b86b60d816716b8697c58ce9 PHP_MD5=
# Thu, 06 Aug 2020 21:42:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 06 Aug 2020 21:42:45 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 06 Aug 2020 21:52:26 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 06 Aug 2020 21:52:27 GMT
COPY multi:cfe027e655535d9b3eb4b44f84eafb2e1d257620ca628247fe5c1c4fb008a78a in /usr/local/bin/ 
# Thu, 06 Aug 2020 21:52:30 GMT
RUN docker-php-ext-enable sodium
# Thu, 06 Aug 2020 21:52:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 06 Aug 2020 21:52:30 GMT
CMD ["php" "-a"]
# Fri, 07 Aug 2020 02:40:30 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 	; 		docker-php-ext-configure gd --with-freetype-dir=/usr --with-jpeg-dir=/usr --with-png-dir=/usr; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		mysqli 		zip 	; 	pecl install imagick-3.4.4; 	docker-php-ext-enable imagick; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del .build-deps
# Fri, 07 Aug 2020 02:40:31 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Fri, 07 Aug 2020 02:40:33 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client
# Fri, 07 Aug 2020 02:40:34 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html
# Fri, 07 Aug 2020 02:40:34 GMT
WORKDIR /var/www/html
# Fri, 07 Aug 2020 02:40:34 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Fri, 07 Aug 2020 02:40:34 GMT
ENV WORDPRESS_CLI_VERSION=2.4.0
# Fri, 07 Aug 2020 02:40:34 GMT
ENV WORDPRESS_CLI_SHA512=4049c7e45e14276a70a41c3b0864be7a6a8cfa8ea65ebac8b184a4f503a91baa1a0d29260d03248bc74aef70729824330fb6b396336172a624332e16f64e37ef
# Fri, 07 Aug 2020 02:40:37 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fSL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del .fetch-deps; 		wp --allow-root --version
# Fri, 07 Aug 2020 02:40:37 GMT
VOLUME [/var/www/html]
# Fri, 07 Aug 2020 02:40:37 GMT
COPY file:7798dc600ff57df68d7de781fd8834d5a9371b2ab13ab9649086b34ee0e38fcf in /usr/local/bin/ 
# Fri, 07 Aug 2020 02:40:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Aug 2020 02:40:38 GMT
USER www-data
# Fri, 07 Aug 2020 02:40:38 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:0625b4155e2a59f647ece47c0cd77ed3196b1f84454fa64ce80cad90e2b9b79e`  
		Last Modified: Fri, 29 May 2020 21:38:53 GMT  
		Size: 2.8 MB (2792298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:380f9ca051d120d4ed72890904488f0f1e0fd0128cbd1c73adbff366e90bc2aa`  
		Last Modified: Thu, 11 Jun 2020 22:28:37 GMT  
		Size: 1.4 MB (1439837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613b9419908bb5beb7365d9d340ee3071aebf8c7919f5379a7b99221fd74c78f`  
		Last Modified: Thu, 11 Jun 2020 22:28:36 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd1bd9f7e9212850ee7c4017e1d3e5ec33176a9113258688a743d871983ee8c`  
		Last Modified: Thu, 11 Jun 2020 22:28:37 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31f8ef2960af618fd12e3cccf3506111724dab145565342cb2cb7ef67cc321a3`  
		Last Modified: Fri, 07 Aug 2020 00:51:26 GMT  
		Size: 12.1 MB (12142644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033055dd91f7d395abb9e7dcee8d0c4b32ce3eeea2b509b80af76a765a7ce1a3`  
		Last Modified: Fri, 07 Aug 2020 00:51:07 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cf5b6b09ac6b7e21e401c2bb6bdd1ad057b93f7cf1cfd607226824ec423f31f`  
		Last Modified: Fri, 07 Aug 2020 00:51:11 GMT  
		Size: 15.1 MB (15145078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3773b60600c754ff868fe6d652b4d6906a8352f85db78dec0b95e06be34b69`  
		Last Modified: Fri, 07 Aug 2020 00:51:07 GMT  
		Size: 2.3 KB (2273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c48bce64d530c6250b5bcc3e7c8f33faed4b7a587ff1e1fde0bc71de28670b8`  
		Last Modified: Fri, 07 Aug 2020 00:51:06 GMT  
		Size: 16.8 KB (16798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:722858e4cb3b770d53700f4e3701e50a92d1780f4d8ab3f55dc13b9770b74f9a`  
		Last Modified: Fri, 07 Aug 2020 02:45:42 GMT  
		Size: 7.2 MB (7150881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ffc45135638b006a5099d2856f4d7b82bfa1a76e17d46e08fe48d4287e29754`  
		Last Modified: Fri, 07 Aug 2020 02:45:38 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe096e3348828fe44338b076155d6dc3baca0c6e22de4866d437afde75cf2822`  
		Last Modified: Fri, 07 Aug 2020 02:45:42 GMT  
		Size: 9.4 MB (9430262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e89212b784ffd06f6bbde26fc79e4af3ae77bf5c3b7bcb7eafd897a4f09ac38`  
		Last Modified: Fri, 07 Aug 2020 02:45:38 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3db5892733ffeccbe0cd2678ccec0c9b747ef738ae9ed1ecb90fe0546ae9ca81`  
		Last Modified: Fri, 07 Aug 2020 02:45:39 GMT  
		Size: 1.2 MB (1205249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34936c0339c98f97631a9d3523bfa0483fe7e1da30f0ca509fbd223689f9f96d`  
		Last Modified: Fri, 07 Aug 2020 02:45:38 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:cli-2-php7.3` - linux; ppc64le

```console
$ docker pull wordpress@sha256:509be8138b790159eed792335324f84b61185b9eb0603b0ab0ad97a79ee486ed
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49846892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a1157a57c717bd8946d071972295f6581d3691e7bbc31cccee72fb9bdb24c49`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Fri, 29 May 2020 21:23:03 GMT
ADD file:8194808a812370fd2202d80d1667f851bd9eac4c560d69d347fe1964f54343de in / 
# Fri, 29 May 2020 21:23:06 GMT
CMD ["/bin/sh"]
# Thu, 11 Jun 2020 18:45:11 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 11 Jun 2020 18:45:20 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 11 Jun 2020 18:45:29 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 11 Jun 2020 18:45:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jun 2020 18:45:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 11 Jun 2020 18:45:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2020 18:45:44 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2020 18:45:46 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jun 2020 20:07:28 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Fri, 10 Jul 2020 01:22:37 GMT
ENV PHP_VERSION=7.3.20
# Fri, 10 Jul 2020 01:22:39 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.20.tar.xz.asc
# Fri, 10 Jul 2020 01:22:44 GMT
ENV PHP_SHA256=43292046f6684eb13acb637276d4aa1dd9f66b0b7045e6f1493bc90db389b888 PHP_MD5=
# Fri, 10 Jul 2020 01:22:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 10 Jul 2020 01:22:58 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 10 Jul 2020 01:26:59 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 10 Jul 2020 01:27:02 GMT
COPY multi:cfe027e655535d9b3eb4b44f84eafb2e1d257620ca628247fe5c1c4fb008a78a in /usr/local/bin/ 
# Fri, 10 Jul 2020 01:27:18 GMT
RUN docker-php-ext-enable sodium
# Fri, 10 Jul 2020 01:27:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 10 Jul 2020 01:27:35 GMT
CMD ["php" "-a"]
# Fri, 10 Jul 2020 10:00:09 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 	; 		docker-php-ext-configure gd --with-freetype-dir=/usr --with-jpeg-dir=/usr --with-png-dir=/usr; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		mysqli 		zip 	; 	pecl install imagick-3.4.4; 	docker-php-ext-enable imagick; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del .build-deps
# Fri, 10 Jul 2020 10:00:19 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Fri, 10 Jul 2020 10:00:31 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client
# Fri, 10 Jul 2020 10:00:45 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html
# Fri, 10 Jul 2020 10:00:50 GMT
WORKDIR /var/www/html
# Fri, 10 Jul 2020 10:00:55 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Fri, 10 Jul 2020 10:01:04 GMT
ENV WORDPRESS_CLI_VERSION=2.4.0
# Fri, 10 Jul 2020 10:01:13 GMT
ENV WORDPRESS_CLI_SHA512=4049c7e45e14276a70a41c3b0864be7a6a8cfa8ea65ebac8b184a4f503a91baa1a0d29260d03248bc74aef70729824330fb6b396336172a624332e16f64e37ef
# Fri, 10 Jul 2020 10:01:28 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fSL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del .fetch-deps; 		wp --allow-root --version
# Fri, 10 Jul 2020 10:01:49 GMT
VOLUME [/var/www/html]
# Fri, 10 Jul 2020 10:02:06 GMT
COPY file:7798dc600ff57df68d7de781fd8834d5a9371b2ab13ab9649086b34ee0e38fcf in /usr/local/bin/ 
# Fri, 10 Jul 2020 10:02:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Jul 2020 10:02:58 GMT
USER www-data
# Fri, 10 Jul 2020 10:03:04 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:5077f8601dceb5744d875d7740ebc203f674b108a0188f3a31e292b21a4bee64`  
		Last Modified: Fri, 29 May 2020 21:23:37 GMT  
		Size: 2.8 MB (2805199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46f98eb9049c4fcbaa1cf16ddb44aaf910a89a5471dc303198251fa25bc2a1ef`  
		Last Modified: Thu, 11 Jun 2020 20:57:07 GMT  
		Size: 1.4 MB (1383311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e50cdb8e03fc1b19217cd9f80b86142d090ad3e818795b339ea4d9ef9b74555f`  
		Last Modified: Thu, 11 Jun 2020 20:57:06 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b4466e085b12b265fb47397c7c105fd7d78a5883beef49ab9f386393c4c3dae`  
		Last Modified: Thu, 11 Jun 2020 20:57:06 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74fa1e3092a157929a8fa5849dab9d680dd471497d00956306691d560ae6d3f`  
		Last Modified: Fri, 10 Jul 2020 03:30:06 GMT  
		Size: 12.1 MB (12137686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25bd806bedf8fe9d3a37a067d5c62240deab180ecf5ff2a8984f785695c134b7`  
		Last Modified: Fri, 10 Jul 2020 03:30:05 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7438bdbc81fadc757b77cffa5a512ebcf95a78b4c8ae16226ce7e68eac5e92e2`  
		Last Modified: Fri, 10 Jul 2020 03:30:09 GMT  
		Size: 15.8 MB (15792703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:590f967b8e7dbcbd6b53210a16416c0b8eabe89e4e537850056de08d9b7ccd43`  
		Last Modified: Fri, 10 Jul 2020 03:30:05 GMT  
		Size: 2.3 KB (2274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a0d9e2a0f9d22fe196a4205a0e36ef4fcab88b35d066a1e0bb4a78dedc8a174`  
		Last Modified: Fri, 10 Jul 2020 03:30:05 GMT  
		Size: 16.8 KB (16798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e17b24dfdfd55dfcaa8232c98603c6c4bcc6369bb34239802df633b621b19e9`  
		Last Modified: Fri, 10 Jul 2020 10:16:46 GMT  
		Size: 7.0 MB (7036048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f2bc2ef17263ec40fba3731809d8d781f57a951e8024e9ca72def68f45884eb`  
		Last Modified: Fri, 10 Jul 2020 10:16:37 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f81245f137b6167e75718caaaf407a81364aaf867a6954cb2c5dce44c6fdda`  
		Last Modified: Fri, 10 Jul 2020 10:16:39 GMT  
		Size: 9.5 MB (9464616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4abb1faf4b1f9f0b25f5f747a2bd5c03a20dab147e700a30e4e7211825f3b022`  
		Last Modified: Fri, 10 Jul 2020 10:16:36 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac5571386886188183ad45fd0f8c55449e465f31c2fa7a78635ef10406d341e`  
		Last Modified: Fri, 10 Jul 2020 10:16:37 GMT  
		Size: 1.2 MB (1205276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4027df00234e2b0133bcacf10640b8d02f7304c510a6519d1fa9b97563085ad1`  
		Last Modified: Fri, 10 Jul 2020 10:16:37 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:cli-2-php7.3` - linux; s390x

```console
$ docker pull wordpress@sha256:ed5c19fe3e094bfdfb106819262cd9281dcb7a0506a8b596b029e57539879c7b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47948303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f517eddc83298de17141360711169e47e908e4ab7cef37e6c397132a43c41ece`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Fri, 29 May 2020 21:41:39 GMT
ADD file:9799ce3b2f782a28e10b1846cd9b3db827fa99c9bc601feb268456195856814e in / 
# Fri, 29 May 2020 21:41:39 GMT
CMD ["/bin/sh"]
# Thu, 11 Jun 2020 18:29:35 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 11 Jun 2020 18:29:37 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 11 Jun 2020 18:29:38 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 11 Jun 2020 18:29:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jun 2020 18:29:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 11 Jun 2020 18:29:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2020 18:29:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2020 18:29:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jun 2020 19:04:40 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Thu, 06 Aug 2020 19:03:28 GMT
ENV PHP_VERSION=7.3.21
# Thu, 06 Aug 2020 19:03:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.21.tar.xz.asc
# Thu, 06 Aug 2020 19:03:29 GMT
ENV PHP_SHA256=4c8b065746ef776d84b7ae47908c21a79e3d4704b86b60d816716b8697c58ce9 PHP_MD5=
# Thu, 06 Aug 2020 19:03:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 06 Aug 2020 19:03:32 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 06 Aug 2020 19:05:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 06 Aug 2020 19:05:50 GMT
COPY multi:cfe027e655535d9b3eb4b44f84eafb2e1d257620ca628247fe5c1c4fb008a78a in /usr/local/bin/ 
# Thu, 06 Aug 2020 19:05:51 GMT
RUN docker-php-ext-enable sodium
# Thu, 06 Aug 2020 19:05:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 06 Aug 2020 19:05:51 GMT
CMD ["php" "-a"]
# Thu, 06 Aug 2020 20:57:24 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 	; 		docker-php-ext-configure gd --with-freetype-dir=/usr --with-jpeg-dir=/usr --with-png-dir=/usr; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		mysqli 		zip 	; 	pecl install imagick-3.4.4; 	docker-php-ext-enable imagick; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del .build-deps
# Thu, 06 Aug 2020 20:57:25 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Thu, 06 Aug 2020 20:57:27 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client
# Thu, 06 Aug 2020 20:57:28 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html
# Thu, 06 Aug 2020 20:57:28 GMT
WORKDIR /var/www/html
# Thu, 06 Aug 2020 20:57:28 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Thu, 06 Aug 2020 20:57:29 GMT
ENV WORDPRESS_CLI_VERSION=2.4.0
# Thu, 06 Aug 2020 20:57:29 GMT
ENV WORDPRESS_CLI_SHA512=4049c7e45e14276a70a41c3b0864be7a6a8cfa8ea65ebac8b184a4f503a91baa1a0d29260d03248bc74aef70729824330fb6b396336172a624332e16f64e37ef
# Thu, 06 Aug 2020 20:57:31 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fSL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del .fetch-deps; 		wp --allow-root --version
# Thu, 06 Aug 2020 20:57:31 GMT
VOLUME [/var/www/html]
# Thu, 06 Aug 2020 20:57:31 GMT
COPY file:7798dc600ff57df68d7de781fd8834d5a9371b2ab13ab9649086b34ee0e38fcf in /usr/local/bin/ 
# Thu, 06 Aug 2020 20:57:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Aug 2020 20:57:32 GMT
USER www-data
# Thu, 06 Aug 2020 20:57:32 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:8fb3d41b2e9a59630b51745f257cd2561f96bcd15cf309fcc20120d5fcee8c5b`  
		Last Modified: Fri, 29 May 2020 21:42:03 GMT  
		Size: 2.6 MB (2566189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:057c8475c8b5e21c245ff682a57adf8970d16ccbed87694b3ec200c83e17a8fb`  
		Last Modified: Thu, 11 Jun 2020 19:32:19 GMT  
		Size: 1.4 MB (1382745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad2bbd1ef5644a3638bc6f073de941463cbfceb435ea6d11ce3c7fdb9f8d2539`  
		Last Modified: Thu, 11 Jun 2020 19:32:18 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b73c5118a1a42bce068c040302cb99d7a26ef9ab76544773e9ba70f28d274d3`  
		Last Modified: Thu, 11 Jun 2020 19:32:18 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a211b53d7ee183b2cdbd561059c47558fb52576ebe77b0930c859ff7ce2e799`  
		Last Modified: Thu, 06 Aug 2020 19:50:03 GMT  
		Size: 12.1 MB (12142658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:609434bfb630e4af85be61554e908f3a7e63fdfa620dec48f382f4113d53266b`  
		Last Modified: Thu, 06 Aug 2020 19:49:59 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d0c9d114c9ace559d4a1ffaa9cbb170e364da0bb4fd3e4b2dab4ae91c412be`  
		Last Modified: Thu, 06 Aug 2020 19:50:02 GMT  
		Size: 14.1 MB (14104202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2747827fe683c41ae9e7c1f7753311d8595bae53ee3be3ebf59225f326a24466`  
		Last Modified: Thu, 06 Aug 2020 19:49:59 GMT  
		Size: 2.3 KB (2269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ff93ac958be378195c43dfc6336f05566d6cefdf50f5b8a517c168a401d799`  
		Last Modified: Thu, 06 Aug 2020 19:49:59 GMT  
		Size: 16.8 KB (16781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07eb8da14a380a6f559fb9b8719ef0f8e98a6a1a5e1f60983511526adff9dc06`  
		Last Modified: Thu, 06 Aug 2020 21:01:37 GMT  
		Size: 6.8 MB (6771520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc540896e81245432a086442d87014670b38ae65bcbd95d4d9924022de7d2374`  
		Last Modified: Thu, 06 Aug 2020 21:01:35 GMT  
		Size: 388.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729639056aa0db6caaf648929c9fa6e1539d87cc9bdb3593a1cd90a46261fb29`  
		Last Modified: Thu, 06 Aug 2020 21:01:36 GMT  
		Size: 9.8 MB (9753709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6112d446d05534f5f0adc6e2620c7964c8c5ba62a491124faf2f489e1697e59b`  
		Last Modified: Thu, 06 Aug 2020 21:01:34 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23dfdcc44aeccc563d9306d6d1b8271c09d51ffe19e6d76c2843b14d9102d49a`  
		Last Modified: Thu, 06 Aug 2020 21:01:35 GMT  
		Size: 1.2 MB (1205258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8badda66bb1f30a7f0b8e7d1be85211b322352164207e3e58ec4b37d1a496979`  
		Last Modified: Thu, 06 Aug 2020 21:01:34 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
