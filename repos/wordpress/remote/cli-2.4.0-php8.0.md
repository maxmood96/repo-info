## `wordpress:cli-2.4.0-php8.0`

```console
$ docker pull wordpress@sha256:9da0ab623a84ded6bf0ab8b4ef7ba4ee9977b87c1c04c30fce2f7b6443251480
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

### `wordpress:cli-2.4.0-php8.0` - linux; amd64

```console
$ docker pull wordpress@sha256:10721c5296a764eb815e0d27de0cb994bc7a1f2e12937d0691f3c4ee75540730
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.8 MB (41848815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20eb7977ce69851052a38a04c65c193d8d407183a0f836b7f7857056a858236b`
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
# Fri, 29 Jan 2021 01:09:36 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 05 Feb 2021 04:22:44 GMT
ENV PHP_VERSION=8.0.2
# Fri, 05 Feb 2021 04:22:44 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.2.tar.xz?a=1 PHP_ASC_URL=https://www.php.net/distributions/php-8.0.2.tar.xz.asc?a=1
# Fri, 05 Feb 2021 04:22:44 GMT
ENV PHP_SHA256=84dd6e36f48c3a71ff5dceba375c1f6b34b71d4fa9e06b720780127176468ccc
# Fri, 05 Feb 2021 04:22:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 05 Feb 2021 04:22:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Feb 2021 04:34:01 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Feb 2021 04:34:02 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Fri, 05 Feb 2021 04:34:04 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Feb 2021 04:34:05 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Feb 2021 04:34:05 GMT
CMD ["php" "-a"]
# Fri, 05 Feb 2021 05:12:58 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client
# Fri, 05 Feb 2021 05:12:59 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html
# Fri, 05 Feb 2021 05:13:00 GMT
WORKDIR /var/www/html
# Fri, 05 Feb 2021 05:13:45 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		mysqli 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps
# Fri, 05 Feb 2021 05:13:46 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Fri, 05 Feb 2021 05:13:46 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Fri, 05 Feb 2021 05:13:46 GMT
ENV WORDPRESS_CLI_VERSION=2.4.0
# Fri, 05 Feb 2021 05:13:47 GMT
ENV WORDPRESS_CLI_SHA512=4049c7e45e14276a70a41c3b0864be7a6a8cfa8ea65ebac8b184a4f503a91baa1a0d29260d03248bc74aef70729824330fb6b396336172a624332e16f64e37ef
# Fri, 05 Feb 2021 05:13:49 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version
# Fri, 05 Feb 2021 05:13:49 GMT
VOLUME [/var/www/html]
# Fri, 05 Feb 2021 05:13:49 GMT
COPY file:b6efa5ff0423d61c2df0c8941b896844a8272d8516cdda0fcae8daaf56baac18 in /usr/local/bin/ 
# Fri, 05 Feb 2021 05:13:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Feb 2021 05:13:50 GMT
USER www-data
# Fri, 05 Feb 2021 05:13:50 GMT
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
	-	`sha256:fb0ff0908eb3be4251b34a25d351665d82968a1c98b7ba83475e23af3222d267`  
		Last Modified: Fri, 05 Feb 2021 05:05:21 GMT  
		Size: 10.7 MB (10669904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e3194413ee7dec46105ab569c2873edb1523e2121f683b3eae92489c272628f`  
		Last Modified: Fri, 05 Feb 2021 05:05:20 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a3f9163b801e059a4236391e25f963c3f539461cfece99c0016168ca1cd472e`  
		Last Modified: Fri, 05 Feb 2021 05:05:24 GMT  
		Size: 14.9 MB (14946438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68aac131d818516ba0378057d5d3e3fbef370b2c7332d5d13f6175c9114b8004`  
		Last Modified: Fri, 05 Feb 2021 05:05:21 GMT  
		Size: 2.3 KB (2265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc4e7f70d907634f5d04c3b2100e94f90177d4c4caedafb3520a1e49e9a440cc`  
		Last Modified: Fri, 05 Feb 2021 05:05:30 GMT  
		Size: 17.5 KB (17527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f9e3fcf669204b82e81e2b21f35db83d096b89add48f0bb80d2931bf68d56e`  
		Last Modified: Fri, 05 Feb 2021 05:19:10 GMT  
		Size: 9.3 MB (9334540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d772b75bfcfd6d411d26c0c734e9aa5b8c18527ebc0838d6076cedf5aeb3660`  
		Last Modified: Fri, 05 Feb 2021 05:19:07 GMT  
		Size: 145.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a86a1d947753d36466a45ddee14312967bbd24488f7c8895a84f340188f81033`  
		Last Modified: Fri, 05 Feb 2021 05:19:07 GMT  
		Size: 1.2 MB (1172836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a852325610813d639b41e04a83801c5cb6af0075c7e5d281c80ec6759270d118`  
		Last Modified: Fri, 05 Feb 2021 05:19:08 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:669d0dc69328777a5d3f5743b20e71a0d7102145446e6ca0a883a97898fdae7c`  
		Last Modified: Fri, 05 Feb 2021 05:19:08 GMT  
		Size: 1.2 MB (1196250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2a50f1e3a11ed31f49108b30849f56f8f609a2cb9b0aae9a5cb4469aff6a6c`  
		Last Modified: Fri, 05 Feb 2021 05:19:08 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:cli-2.4.0-php8.0` - linux; arm variant v6

```console
$ docker pull wordpress@sha256:3341b27680caf8d63cd6e02000d712d0d726958201ead81197fb5a08f0129c73
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39785131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d8ee5358a35bada0f67b75826d2afbf54a698266302e776cd585ded8b2a38f9`
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
# Wed, 17 Feb 2021 22:17:20 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Wed, 17 Feb 2021 22:17:21 GMT
ENV PHP_VERSION=8.0.2
# Wed, 17 Feb 2021 22:17:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.2.tar.xz?a=1 PHP_ASC_URL=https://www.php.net/distributions/php-8.0.2.tar.xz.asc?a=1
# Wed, 17 Feb 2021 22:17:22 GMT
ENV PHP_SHA256=84dd6e36f48c3a71ff5dceba375c1f6b34b71d4fa9e06b720780127176468ccc
# Wed, 17 Feb 2021 22:17:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 17 Feb 2021 22:17:28 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 17 Feb 2021 22:20:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 17 Feb 2021 22:20:35 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Wed, 17 Feb 2021 22:20:38 GMT
RUN docker-php-ext-enable sodium
# Wed, 17 Feb 2021 22:20:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 17 Feb 2021 22:20:39 GMT
CMD ["php" "-a"]
# Thu, 18 Feb 2021 02:23:06 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client
# Thu, 18 Feb 2021 02:23:10 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html
# Thu, 18 Feb 2021 02:23:11 GMT
WORKDIR /var/www/html
# Thu, 18 Feb 2021 02:24:01 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		mysqli 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps
# Thu, 18 Feb 2021 02:24:03 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Thu, 18 Feb 2021 02:24:04 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Thu, 18 Feb 2021 02:24:04 GMT
ENV WORDPRESS_CLI_VERSION=2.4.0
# Thu, 18 Feb 2021 02:24:05 GMT
ENV WORDPRESS_CLI_SHA512=4049c7e45e14276a70a41c3b0864be7a6a8cfa8ea65ebac8b184a4f503a91baa1a0d29260d03248bc74aef70729824330fb6b396336172a624332e16f64e37ef
# Thu, 18 Feb 2021 02:24:09 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version
# Thu, 18 Feb 2021 02:24:10 GMT
VOLUME [/var/www/html]
# Thu, 18 Feb 2021 02:24:10 GMT
COPY file:b6efa5ff0423d61c2df0c8941b896844a8272d8516cdda0fcae8daaf56baac18 in /usr/local/bin/ 
# Thu, 18 Feb 2021 02:24:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Feb 2021 02:24:12 GMT
USER www-data
# Thu, 18 Feb 2021 02:24:13 GMT
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
	-	`sha256:5a2cd8acca8c00d04d775fbc06a5f948641d84490f69511cc1310355bc805fdd`  
		Last Modified: Wed, 17 Feb 2021 22:57:09 GMT  
		Size: 10.7 MB (10669907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86499947ebe61a0dd04ef562bea57937e9739822d92147fee068f362d5bc537e`  
		Last Modified: Wed, 17 Feb 2021 22:57:08 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33ff03fcd67eb2ac1a244eaabdaf4608d7464ccd158ad8b3aca4ad8918c7c0b8`  
		Last Modified: Wed, 17 Feb 2021 22:57:14 GMT  
		Size: 13.6 MB (13582102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a6e0a080b5c569d5c2f91a301e2aba6354c74d6075b8a36c304c44ce52e0cf`  
		Last Modified: Wed, 17 Feb 2021 22:57:08 GMT  
		Size: 2.3 KB (2267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:126c1e00670ebf190587b40cfb16e7fdb37329d2567e6c9da0720b7a23b30e17`  
		Last Modified: Wed, 17 Feb 2021 22:57:07 GMT  
		Size: 17.5 KB (17524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6943ea508ae72267dd916644a71f9c1d5a6dbf8659d72a262b5a2f983862482`  
		Last Modified: Thu, 18 Feb 2021 02:28:21 GMT  
		Size: 8.9 MB (8943796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907c2ace62b1566f702d0f032c38ab738fd7b733a48d7c8ab204b3f5db52ce29`  
		Last Modified: Thu, 18 Feb 2021 02:28:16 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dd7357e360e0088ab3253e7dc2e992f12872b0e8efc75f63353625e39eca098`  
		Last Modified: Thu, 18 Feb 2021 02:28:15 GMT  
		Size: 1.1 MB (1063554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01c6a90ade0de8c560cfaca6d45260159ac740676c283796ec05463b634dc46b`  
		Last Modified: Thu, 18 Feb 2021 02:28:15 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f166cae6f7e68fcb5c226ed410f30285ed516a6a126f973b3b4cc1236d102b9e`  
		Last Modified: Thu, 18 Feb 2021 02:28:16 GMT  
		Size: 1.2 MB (1196254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed343c7b6f83a1d19a85000864c9bf77a9a0fb636a73a380bdf9390b9f5ca32f`  
		Last Modified: Thu, 18 Feb 2021 02:28:15 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:cli-2.4.0-php8.0` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:34346591cd1dad9dc74971397f9dd935fff3315458040fd630c087dccd5b2111
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38224487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8e9773e61329280e3da7b1fde664c9ee411b2f729fed38900539e2253f7453a`
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
# Wed, 17 Feb 2021 22:57:14 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Wed, 17 Feb 2021 22:57:15 GMT
ENV PHP_VERSION=8.0.2
# Wed, 17 Feb 2021 22:57:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.2.tar.xz?a=1 PHP_ASC_URL=https://www.php.net/distributions/php-8.0.2.tar.xz.asc?a=1
# Wed, 17 Feb 2021 22:57:18 GMT
ENV PHP_SHA256=84dd6e36f48c3a71ff5dceba375c1f6b34b71d4fa9e06b720780127176468ccc
# Wed, 17 Feb 2021 22:57:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 17 Feb 2021 22:57:26 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 17 Feb 2021 23:02:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 17 Feb 2021 23:02:19 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Wed, 17 Feb 2021 23:02:26 GMT
RUN docker-php-ext-enable sodium
# Wed, 17 Feb 2021 23:02:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 17 Feb 2021 23:02:29 GMT
CMD ["php" "-a"]
# Thu, 18 Feb 2021 03:59:51 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client
# Thu, 18 Feb 2021 03:59:53 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html
# Thu, 18 Feb 2021 03:59:53 GMT
WORKDIR /var/www/html
# Thu, 18 Feb 2021 04:00:38 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		mysqli 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps
# Thu, 18 Feb 2021 04:00:41 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Thu, 18 Feb 2021 04:00:42 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Thu, 18 Feb 2021 04:00:43 GMT
ENV WORDPRESS_CLI_VERSION=2.4.0
# Thu, 18 Feb 2021 04:00:44 GMT
ENV WORDPRESS_CLI_SHA512=4049c7e45e14276a70a41c3b0864be7a6a8cfa8ea65ebac8b184a4f503a91baa1a0d29260d03248bc74aef70729824330fb6b396336172a624332e16f64e37ef
# Thu, 18 Feb 2021 04:00:48 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version
# Thu, 18 Feb 2021 04:00:49 GMT
VOLUME [/var/www/html]
# Thu, 18 Feb 2021 04:00:50 GMT
COPY file:b6efa5ff0423d61c2df0c8941b896844a8272d8516cdda0fcae8daaf56baac18 in /usr/local/bin/ 
# Thu, 18 Feb 2021 04:00:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Feb 2021 04:00:52 GMT
USER www-data
# Thu, 18 Feb 2021 04:00:53 GMT
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
	-	`sha256:b324e86e98e340fac51bbad137a0676805757c5706fe63b19c52bb0bf2304814`  
		Last Modified: Wed, 17 Feb 2021 23:33:57 GMT  
		Size: 10.7 MB (10669910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b850d73733997eefb0ce659e8218da573b9b5820593d79f2438f92bcf403ea0`  
		Last Modified: Wed, 17 Feb 2021 23:33:56 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fbcce1987875575118f2884324bfe4f84f722df8e5f026a22c6c84c9c0f1007`  
		Last Modified: Wed, 17 Feb 2021 23:34:00 GMT  
		Size: 12.7 MB (12727025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd7d31037b9fb5685bf02f59ed147a66936b4e6e739fe19c7d2bcb762b5fbc9`  
		Last Modified: Wed, 17 Feb 2021 23:33:56 GMT  
		Size: 2.3 KB (2270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:533cb565f1306982f3aecf66449941029f323359c5afeb21fcfed8ccb26664c5`  
		Last Modified: Wed, 17 Feb 2021 23:33:56 GMT  
		Size: 17.5 KB (17520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a77569cc1aeaf6b0febd288ea52679ad492b5a15ce7551a3327dd55d68358ce6`  
		Last Modified: Thu, 18 Feb 2021 04:06:21 GMT  
		Size: 8.7 MB (8661039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8994c3f310bc87c9d2bba011befdbe7ded7f0d6262d5d1f5b1dedfb123d01a2`  
		Last Modified: Thu, 18 Feb 2021 04:06:16 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d2d744ac8291eba8ba231d0e7c183d127fb0a41ed01867424b55205b8d40f27`  
		Last Modified: Thu, 18 Feb 2021 04:06:17 GMT  
		Size: 968.5 KB (968498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba3b64731f42e6a7bf93a9c93a04ef7f51a6b9c5e85137bf863d7471c9036d59`  
		Last Modified: Thu, 18 Feb 2021 04:06:17 GMT  
		Size: 392.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0df2479b6611e83b835d18212b8cb1e8db3a6670247655ff5f1b5c65c00fd25`  
		Last Modified: Thu, 18 Feb 2021 04:06:17 GMT  
		Size: 1.2 MB (1196243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8eadc8dd07e3f446c329c4f818cfc250f384054efe90e7a2330057c4b2f18c7`  
		Last Modified: Thu, 18 Feb 2021 04:06:16 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:cli-2.4.0-php8.0` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:421b1cadf005f67a879865e39dcc0bbde5499aea6e116ebc86bf489f3639ea5b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.2 MB (41220800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb9aaa2dd3c265d2c47b71afff647ac529178659abb7076358e6627282e14ef3`
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
# Wed, 17 Feb 2021 23:42:45 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Wed, 17 Feb 2021 23:42:45 GMT
ENV PHP_VERSION=8.0.2
# Wed, 17 Feb 2021 23:42:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.2.tar.xz?a=1 PHP_ASC_URL=https://www.php.net/distributions/php-8.0.2.tar.xz.asc?a=1
# Wed, 17 Feb 2021 23:42:47 GMT
ENV PHP_SHA256=84dd6e36f48c3a71ff5dceba375c1f6b34b71d4fa9e06b720780127176468ccc
# Wed, 17 Feb 2021 23:42:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 17 Feb 2021 23:42:55 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 17 Feb 2021 23:47:08 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 17 Feb 2021 23:47:11 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Wed, 17 Feb 2021 23:47:14 GMT
RUN docker-php-ext-enable sodium
# Wed, 17 Feb 2021 23:47:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 17 Feb 2021 23:47:16 GMT
CMD ["php" "-a"]
# Thu, 18 Feb 2021 04:12:04 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client
# Thu, 18 Feb 2021 04:12:06 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html
# Thu, 18 Feb 2021 04:12:07 GMT
WORKDIR /var/www/html
# Thu, 18 Feb 2021 04:12:59 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		mysqli 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps
# Thu, 18 Feb 2021 04:13:01 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Thu, 18 Feb 2021 04:13:02 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Thu, 18 Feb 2021 04:13:02 GMT
ENV WORDPRESS_CLI_VERSION=2.4.0
# Thu, 18 Feb 2021 04:13:03 GMT
ENV WORDPRESS_CLI_SHA512=4049c7e45e14276a70a41c3b0864be7a6a8cfa8ea65ebac8b184a4f503a91baa1a0d29260d03248bc74aef70729824330fb6b396336172a624332e16f64e37ef
# Thu, 18 Feb 2021 04:13:07 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version
# Thu, 18 Feb 2021 04:13:08 GMT
VOLUME [/var/www/html]
# Thu, 18 Feb 2021 04:13:09 GMT
COPY file:b6efa5ff0423d61c2df0c8941b896844a8272d8516cdda0fcae8daaf56baac18 in /usr/local/bin/ 
# Thu, 18 Feb 2021 04:13:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Feb 2021 04:13:10 GMT
USER www-data
# Thu, 18 Feb 2021 04:13:11 GMT
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
	-	`sha256:cfeffe400ab18cc1a3cd5c256f8c8710b9da855a76a2d6cc7386fce7b7aa7b68`  
		Last Modified: Thu, 18 Feb 2021 00:23:33 GMT  
		Size: 10.7 MB (10669929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0f77607b2d5ee1ea5aada5832924fbcbbefa13afa26bc40e5023275ecc8dc43`  
		Last Modified: Thu, 18 Feb 2021 00:23:32 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07887bf661d0faf217ad573921f1117af4749dbbfe238f6ebe892519913dbdc1`  
		Last Modified: Thu, 18 Feb 2021 00:23:37 GMT  
		Size: 14.4 MB (14375123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00f0a3642cc96e4e7cf51b47ae7e8364066b29e0d21876361b0739ba6cf8f3e5`  
		Last Modified: Thu, 18 Feb 2021 00:23:32 GMT  
		Size: 2.3 KB (2265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c491f83e6886dd62d58c8bb91941bc997744f6bfb42f8c0da988f255640775`  
		Last Modified: Thu, 18 Feb 2021 00:23:32 GMT  
		Size: 17.5 KB (17536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e4aec3581417346c86e1775744ad0b4cb9bc4a6fc3e211332dd57a55c4c80a`  
		Last Modified: Thu, 18 Feb 2021 04:18:48 GMT  
		Size: 9.4 MB (9403146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2d3d67b9079f387c5143841cd8e99fc97199da3dc74d6150e50c8cf3ecfea7`  
		Last Modified: Thu, 18 Feb 2021 04:18:44 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3431e89f62bd151e447aed02682fb83caca34c4e6d1b4f3a9364144e558662b`  
		Last Modified: Thu, 18 Feb 2021 04:18:44 GMT  
		Size: 1.1 MB (1147554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0285354a4d47dec7eeaa770aa8f40904e7a5346d6b5f8661b29b08d2ba26ddc`  
		Last Modified: Thu, 18 Feb 2021 04:18:44 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b43b512beb82b7a480dcbd5c01208e30782bdd2d9163880162cbfeba935966c3`  
		Last Modified: Thu, 18 Feb 2021 04:18:44 GMT  
		Size: 1.2 MB (1196255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98fc21a31e4e9e857ad9c1267916daf006c3f61a551aa05f7b7a7df13ce21297`  
		Last Modified: Thu, 18 Feb 2021 04:18:44 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:cli-2.4.0-php8.0` - linux; 386

```console
$ docker pull wordpress@sha256:672079f320a4238b7c1ebe3f08a4e28058c83447af294f6138c655621f349674
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42207642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a8048bd01e662289276ca3019b600ff33270128a5c2aa84f9a784ed751b837a`
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
# Fri, 29 Jan 2021 01:16:36 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 05 Feb 2021 02:55:12 GMT
ENV PHP_VERSION=8.0.2
# Fri, 05 Feb 2021 02:55:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.2.tar.xz?a=1 PHP_ASC_URL=https://www.php.net/distributions/php-8.0.2.tar.xz.asc?a=1
# Fri, 05 Feb 2021 02:55:13 GMT
ENV PHP_SHA256=84dd6e36f48c3a71ff5dceba375c1f6b34b71d4fa9e06b720780127176468ccc
# Fri, 05 Feb 2021 02:55:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 05 Feb 2021 02:55:18 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Feb 2021 03:06:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Feb 2021 03:06:45 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Fri, 05 Feb 2021 03:06:46 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Feb 2021 03:06:47 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Feb 2021 03:06:47 GMT
CMD ["php" "-a"]
# Fri, 05 Feb 2021 03:52:50 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client
# Fri, 05 Feb 2021 03:52:51 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html
# Fri, 05 Feb 2021 03:52:51 GMT
WORKDIR /var/www/html
# Fri, 05 Feb 2021 03:53:35 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		mysqli 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps
# Fri, 05 Feb 2021 03:53:36 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Fri, 05 Feb 2021 03:53:36 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Fri, 05 Feb 2021 03:53:36 GMT
ENV WORDPRESS_CLI_VERSION=2.4.0
# Fri, 05 Feb 2021 03:53:37 GMT
ENV WORDPRESS_CLI_SHA512=4049c7e45e14276a70a41c3b0864be7a6a8cfa8ea65ebac8b184a4f503a91baa1a0d29260d03248bc74aef70729824330fb6b396336172a624332e16f64e37ef
# Fri, 05 Feb 2021 03:53:40 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version
# Fri, 05 Feb 2021 03:53:40 GMT
VOLUME [/var/www/html]
# Fri, 05 Feb 2021 03:53:40 GMT
COPY file:b6efa5ff0423d61c2df0c8941b896844a8272d8516cdda0fcae8daaf56baac18 in /usr/local/bin/ 
# Fri, 05 Feb 2021 03:53:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Feb 2021 03:53:41 GMT
USER www-data
# Fri, 05 Feb 2021 03:53:41 GMT
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
	-	`sha256:eca903ef08ae3bbcf42454b82fc0d17632a9f27d41d88b54af3489a15361d017`  
		Last Modified: Fri, 05 Feb 2021 03:43:27 GMT  
		Size: 10.7 MB (10669888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21a3626d25fc511a2f2706c0191f3cb548cba2b240697873b6a0532a90842b4`  
		Last Modified: Fri, 05 Feb 2021 03:43:24 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0163f74f2fae72844c560e12c351e39f5c2c92c6c4c1d54eb4cec1d6c1bb16f`  
		Last Modified: Fri, 05 Feb 2021 03:43:34 GMT  
		Size: 15.0 MB (14971581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ed3d94022de518cfa6d73eebfa2266be18eb1c4eb9c29fd3e23d1918836cc5`  
		Last Modified: Fri, 05 Feb 2021 03:43:24 GMT  
		Size: 2.3 KB (2263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ec5f2ab4b0a4e8fb0617473ee71770e74107d2c2f319cc8483dce07e585f446`  
		Last Modified: Fri, 05 Feb 2021 03:43:24 GMT  
		Size: 17.5 KB (17509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42ee1271f157c5fe736655cfd4936db8d2772ce5971b5ee11e5ca5fd2dcd3bcf`  
		Last Modified: Fri, 05 Feb 2021 04:01:00 GMT  
		Size: 9.5 MB (9498399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a19f21b35046d23fe4ceb7cb3c9a1db16847c57d46b80d531c5c7cecfaa89031`  
		Last Modified: Fri, 05 Feb 2021 04:00:56 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fdea73b616f1c0fc5e9061888b107e68eb6b428ac52847d2ab2b31f2dcb2682`  
		Last Modified: Fri, 05 Feb 2021 04:00:56 GMT  
		Size: 1.2 MB (1237728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:370665e67584e33eb8014f39e2a8a6c5963941bd1fd12700744d45015b91e80e`  
		Last Modified: Fri, 05 Feb 2021 04:00:56 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b667e84159497b625cd0f02d42202a243f1eee0f21ee2dd181020578855d2770`  
		Last Modified: Fri, 05 Feb 2021 04:00:56 GMT  
		Size: 1.2 MB (1196230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b83463a00c4dfb558a23d60e7c64d70a1c0731eb9ef9ee45a6b59da7d952cc35`  
		Last Modified: Fri, 05 Feb 2021 04:00:56 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:cli-2.4.0-php8.0` - linux; ppc64le

```console
$ docker pull wordpress@sha256:f5dabe49d9cb3c3487c5f792341126d74f91dd189e3e6da59f177e3bc5a586d4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42895877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4ac5946eea07b57e8bd5e433144cf656a55bac2660b378e5b74137f906b4f22`
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
# Fri, 29 Jan 2021 00:47:57 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 05 Feb 2021 10:54:01 GMT
ENV PHP_VERSION=8.0.2
# Fri, 05 Feb 2021 10:54:08 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.2.tar.xz?a=1 PHP_ASC_URL=https://www.php.net/distributions/php-8.0.2.tar.xz.asc?a=1
# Fri, 05 Feb 2021 10:54:16 GMT
ENV PHP_SHA256=84dd6e36f48c3a71ff5dceba375c1f6b34b71d4fa9e06b720780127176468ccc
# Fri, 05 Feb 2021 10:54:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 05 Feb 2021 10:54:43 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Feb 2021 10:59:57 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Feb 2021 11:00:04 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Fri, 05 Feb 2021 11:00:23 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Feb 2021 11:00:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Feb 2021 11:00:40 GMT
CMD ["php" "-a"]
# Fri, 05 Feb 2021 11:46:11 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client
# Fri, 05 Feb 2021 11:46:23 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html
# Fri, 05 Feb 2021 11:46:27 GMT
WORKDIR /var/www/html
# Fri, 05 Feb 2021 11:47:15 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		mysqli 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps
# Fri, 05 Feb 2021 11:47:22 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Fri, 05 Feb 2021 11:47:26 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Fri, 05 Feb 2021 11:47:32 GMT
ENV WORDPRESS_CLI_VERSION=2.4.0
# Fri, 05 Feb 2021 11:47:36 GMT
ENV WORDPRESS_CLI_SHA512=4049c7e45e14276a70a41c3b0864be7a6a8cfa8ea65ebac8b184a4f503a91baa1a0d29260d03248bc74aef70729824330fb6b396336172a624332e16f64e37ef
# Fri, 05 Feb 2021 11:47:49 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version
# Fri, 05 Feb 2021 11:47:52 GMT
VOLUME [/var/www/html]
# Fri, 05 Feb 2021 11:47:54 GMT
COPY file:b6efa5ff0423d61c2df0c8941b896844a8272d8516cdda0fcae8daaf56baac18 in /usr/local/bin/ 
# Fri, 05 Feb 2021 11:47:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Feb 2021 11:48:02 GMT
USER www-data
# Fri, 05 Feb 2021 11:48:08 GMT
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
	-	`sha256:df38515e7585752d0a8361511477a82455a1fd2fc396e66f8d6c5ada2acb8fd4`  
		Last Modified: Fri, 05 Feb 2021 11:27:05 GMT  
		Size: 10.7 MB (10669909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8039f0c0d6d726548ba6f707f360bb3a3960625675e933a801465b3d9d4415`  
		Last Modified: Fri, 05 Feb 2021 11:27:03 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6379a06964588f53f1169928459feb85a6b27064840b39de5e32981098074b97`  
		Last Modified: Fri, 05 Feb 2021 11:27:08 GMT  
		Size: 15.7 MB (15669427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0afd88baf47c25cbc75a281fa31cdf9d469deb11df4389d43d4793c091de9c11`  
		Last Modified: Fri, 05 Feb 2021 11:27:04 GMT  
		Size: 2.3 KB (2268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68d7eaca9819e490feaae741c910f729e98adfc14dc91c84424f9bcac0d23d8e`  
		Last Modified: Fri, 05 Feb 2021 11:27:04 GMT  
		Size: 17.5 KB (17526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60151c729268e207024a8bec646c5a7cdd0f409895ac9c6c1fdeabce6c5ff1e`  
		Last Modified: Fri, 05 Feb 2021 11:54:33 GMT  
		Size: 9.5 MB (9530703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:970444da0e3c2ebf1a9bbf3aff0a299fcd26d485eeee44a6c2ed766b90d558d2`  
		Last Modified: Fri, 05 Feb 2021 11:54:27 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c838e7559a2237a13bacb041bf233389337a45d46de96e284c7d629965046c1`  
		Last Modified: Fri, 05 Feb 2021 11:54:28 GMT  
		Size: 1.3 MB (1252533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94ce0b46d264f50183dc0ca8e82dc9cf84ab1396d4f8600105a5bd2e1bca6712`  
		Last Modified: Fri, 05 Feb 2021 11:54:27 GMT  
		Size: 391.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2da032a67c3f83968bba156a26e47f4788e5677d39eee3bdd224bfb95f38be23`  
		Last Modified: Fri, 05 Feb 2021 11:54:28 GMT  
		Size: 1.2 MB (1196267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d9d026aecdbec5349317c2886603b3fb08d7c480907b98f6d29e3d0dcdd7c75`  
		Last Modified: Fri, 05 Feb 2021 11:54:27 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:cli-2.4.0-php8.0` - linux; s390x

```console
$ docker pull wordpress@sha256:e68a03741e103a9775c508cece01d6a3bc87a318c86e5a85aeaa1ccc4989d334
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.2 MB (41220671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:027ffda70cfe6d94ed2a0b9aa2be863fcd5bfb74d1e204054453f3d9629f925d`
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
# Thu, 18 Feb 2021 00:40:35 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Thu, 18 Feb 2021 00:40:36 GMT
ENV PHP_VERSION=8.0.2
# Thu, 18 Feb 2021 00:40:37 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.2.tar.xz?a=1 PHP_ASC_URL=https://www.php.net/distributions/php-8.0.2.tar.xz.asc?a=1
# Thu, 18 Feb 2021 00:40:37 GMT
ENV PHP_SHA256=84dd6e36f48c3a71ff5dceba375c1f6b34b71d4fa9e06b720780127176468ccc
# Thu, 18 Feb 2021 00:40:42 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 18 Feb 2021 00:40:43 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 18 Feb 2021 00:45:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 18 Feb 2021 00:45:41 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Thu, 18 Feb 2021 00:45:43 GMT
RUN docker-php-ext-enable sodium
# Thu, 18 Feb 2021 00:45:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Feb 2021 00:45:44 GMT
CMD ["php" "-a"]
# Thu, 18 Feb 2021 03:25:51 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client
# Thu, 18 Feb 2021 03:25:54 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html
# Thu, 18 Feb 2021 03:25:55 GMT
WORKDIR /var/www/html
# Thu, 18 Feb 2021 03:26:42 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		mysqli 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps
# Thu, 18 Feb 2021 03:26:44 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Thu, 18 Feb 2021 03:26:45 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Thu, 18 Feb 2021 03:26:45 GMT
ENV WORDPRESS_CLI_VERSION=2.4.0
# Thu, 18 Feb 2021 03:26:46 GMT
ENV WORDPRESS_CLI_SHA512=4049c7e45e14276a70a41c3b0864be7a6a8cfa8ea65ebac8b184a4f503a91baa1a0d29260d03248bc74aef70729824330fb6b396336172a624332e16f64e37ef
# Thu, 18 Feb 2021 03:26:49 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version
# Thu, 18 Feb 2021 03:26:50 GMT
VOLUME [/var/www/html]
# Thu, 18 Feb 2021 03:26:51 GMT
COPY file:b6efa5ff0423d61c2df0c8941b896844a8272d8516cdda0fcae8daaf56baac18 in /usr/local/bin/ 
# Thu, 18 Feb 2021 03:26:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Feb 2021 03:26:52 GMT
USER www-data
# Thu, 18 Feb 2021 03:26:53 GMT
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
	-	`sha256:d57daa3b40970f78adb9b28d367951713e80d1009a73a5b3bb0a0c0ac19a6768`  
		Last Modified: Thu, 18 Feb 2021 01:26:46 GMT  
		Size: 10.7 MB (10669912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f987c292b164ce5b9da787d454670fa610bea163b95db2a8006b7ef903019059`  
		Last Modified: Thu, 18 Feb 2021 01:26:46 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da501df9dc512af3a4787db289cc66eb47fd961affb3fc3d9f6b5db5838daef3`  
		Last Modified: Thu, 18 Feb 2021 01:26:48 GMT  
		Size: 14.0 MB (13968448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afcd5eb7732b0ba16efc0ac27f4d6b8607146c6c00e6c9b9aeb74c7df3fc4bab`  
		Last Modified: Thu, 18 Feb 2021 01:26:46 GMT  
		Size: 2.3 KB (2267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc91df7da0427bc12c70c07de8e2ce48394596fab363dc5f1ad68f5b9acdf270`  
		Last Modified: Thu, 18 Feb 2021 01:26:46 GMT  
		Size: 17.5 KB (17522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88decb84301ade2e94aabfea84439f708be50a1986147a36438bf551f1bc1c15`  
		Last Modified: Thu, 18 Feb 2021 03:31:47 GMT  
		Size: 9.8 MB (9830205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e930f73bc1d1b26fb7b1525253d196f1808be9de6568385074f7ac4ac8fb0877`  
		Last Modified: Thu, 18 Feb 2021 03:31:44 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb2d4718e9418fba369d8645fe3bc66b1e001d0a1eee6538e8092c82aa4ff71d`  
		Last Modified: Thu, 18 Feb 2021 03:31:43 GMT  
		Size: 1.2 MB (1174325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:676a5bd8335ed887cbc0b0cdc338987fc951a269504771a917cc5614f0894a52`  
		Last Modified: Thu, 18 Feb 2021 03:31:43 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40270308b4fa810ff72d3754984526fe2344644247b06b2110c7199c777f2a36`  
		Last Modified: Thu, 18 Feb 2021 03:31:44 GMT  
		Size: 1.2 MB (1196246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8967829eec3630c6c782ceb067103b90436a007f23079b7e2e8e6693770d5f1e`  
		Last Modified: Thu, 18 Feb 2021 03:31:44 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
