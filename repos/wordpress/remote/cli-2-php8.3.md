## `wordpress:cli-2-php8.3`

```console
$ docker pull wordpress@sha256:2668d0c39502269c017efb29e792c91a0900b0684015a099862ea00d2946992e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `wordpress:cli-2-php8.3` - linux; arm variant v6

```console
$ docker pull wordpress@sha256:89e2959ea305aaca061ff01f2c85842f2c9092f9d90fdb0415259aa0c7b44d0d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64942413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:794e7199537e63c2f546499fde7fe5b48c2adfa9dad41afe975c675a0d926dc9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 01:12:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 21 Oct 2023 01:12:15 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 21 Oct 2023 01:12:16 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 21 Oct 2023 01:12:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 21 Oct 2023 01:12:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 21 Oct 2023 01:12:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 21 Oct 2023 01:12:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 21 Oct 2023 01:12:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 21 Oct 2023 01:12:17 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 27 Nov 2023 20:49:30 GMT
ENV PHP_VERSION=8.3.0
# Mon, 27 Nov 2023 20:49:30 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.0.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.0.tar.xz.asc
# Mon, 27 Nov 2023 20:49:30 GMT
ENV PHP_SHA256=1db84fec57125aa93638b51bb2b15103e12ac196e2f960f0d124275b2687ea54
# Mon, 27 Nov 2023 20:49:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Mon, 27 Nov 2023 20:49:38 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Mon, 27 Nov 2023 20:52:59 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Mon, 27 Nov 2023 20:52:59 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Mon, 27 Nov 2023 20:53:00 GMT
RUN docker-php-ext-enable sodium
# Mon, 27 Nov 2023 20:53:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 27 Nov 2023 20:53:00 GMT
CMD ["php" "-a"]
# Thu, 30 Nov 2023 20:54:56 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client
# Thu, 30 Nov 2023 20:54:57 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html
# Thu, 30 Nov 2023 20:54:57 GMT
WORKDIR /var/www/html
# Thu, 30 Nov 2023 20:56:24 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Thu, 30 Nov 2023 20:56:24 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Thu, 30 Nov 2023 20:56:24 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Thu, 30 Nov 2023 20:56:25 GMT
ENV WORDPRESS_CLI_VERSION=2.9.0
# Thu, 30 Nov 2023 20:56:25 GMT
ENV WORDPRESS_CLI_SHA512=39fa365300ab45840e30cc344595bbd175c3558a4499679edd9f9e3a00a846e94179c29c80de3242f1c405f3623605605748d188d9bb98450d9377388f60f113
# Thu, 30 Nov 2023 20:56:27 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version
# Thu, 30 Nov 2023 20:56:27 GMT
VOLUME [/var/www/html]
# Thu, 30 Nov 2023 20:56:28 GMT
COPY file:b6efa5ff0423d61c2df0c8941b896844a8272d8516cdda0fcae8daaf56baac18 in /usr/local/bin/ 
# Thu, 30 Nov 2023 20:56:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Nov 2023 20:56:28 GMT
USER www-data
# Thu, 30 Nov 2023 20:56:28 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e612e11521ddc11f4fbafd4815fd061e99bf827b9952ec407d3c976ea4237db`  
		Last Modified: Sat, 21 Oct 2023 03:21:10 GMT  
		Size: 2.7 MB (2685635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01946457dc0771f96a346d9812bad780b01a21b5e87a4574d8485c060782c4f1`  
		Last Modified: Sat, 21 Oct 2023 03:21:09 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db630a9f175c24d8d95bee24189d4d7e3c04d766b096001c7b8dd8cadb299ddd`  
		Last Modified: Sat, 21 Oct 2023 03:21:09 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e15a2b10f29ced74118b4144b590a1fdb315708c49337d05dc50981ee89f8b32`  
		Last Modified: Mon, 27 Nov 2023 22:28:10 GMT  
		Size: 12.5 MB (12452101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b9ef3ff8fcddb6fed40c428a8075ba47374936a8047b0fa7e4325d7e159546d`  
		Last Modified: Mon, 27 Nov 2023 22:28:09 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb84c0c156c547f0d25252f44aae94be54d6706c2863e6694667836291011b24`  
		Last Modified: Mon, 27 Nov 2023 22:28:14 GMT  
		Size: 18.3 MB (18265434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75746b89baad369b920fa63cb4bd3569862b3d1ed02a395aff581b78b0c9b317`  
		Last Modified: Mon, 27 Nov 2023 22:28:09 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07252f69253df7e3e8eabdc7226e9216e2172bf5f49f166f9712b0195fc5cfad`  
		Last Modified: Mon, 27 Nov 2023 22:28:09 GMT  
		Size: 18.8 KB (18809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e09ca443f3757f074b899c8490dc94ecb3e0b6abcded9b978efa8ba9545176f9`  
		Last Modified: Thu, 30 Nov 2023 20:57:45 GMT  
		Size: 18.4 MB (18369357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:685f49e9698156f905d3341d694c71cb23f83802b874456b9be3989b6cde3a32`  
		Last Modified: Sat, 21 Oct 2023 04:20:27 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f288052ad578b94d55c0746d33a60133bf1ed67348b8288194e14f9e742e9e5c`  
		Last Modified: Thu, 30 Nov 2023 20:57:43 GMT  
		Size: 8.5 MB (8479368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41bd26155093052a11363e9e20e171cf76b86d8af63d75021a141883cc91424`  
		Last Modified: Thu, 30 Nov 2023 20:57:40 GMT  
		Size: 392.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b295e53b5ef9a0186641b23dee24528f54d6a5f1db01da0780007f0fdc324a0e`  
		Last Modified: Thu, 30 Nov 2023 20:57:41 GMT  
		Size: 1.5 MB (1521000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43d9f05563870844162f1772eb7f91ed31a8da6301e67f7e00912e2bec6324f3`  
		Last Modified: Thu, 30 Nov 2023 20:57:41 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:cli-2-php8.3` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:2a4285df36e9105f9a48d2244e806c96070876068cfd4d57f890f6ccd55adbdc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.6 MB (65634781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83f6dd58e6ccbb2c6b2571135f92a7b61a632ee58f0d4d6036ae360569ae68a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Thu, 30 Nov 2023 23:28:59 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 30 Nov 2023 23:29:00 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 30 Nov 2023 23:29:00 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 30 Nov 2023 23:29:01 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 30 Nov 2023 23:29:01 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 30 Nov 2023 23:29:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 30 Nov 2023 23:29:01 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 30 Nov 2023 23:29:01 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 30 Nov 2023 23:29:01 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 30 Nov 2023 23:29:01 GMT
ENV PHP_VERSION=8.3.0
# Thu, 30 Nov 2023 23:29:01 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.0.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.0.tar.xz.asc
# Thu, 30 Nov 2023 23:29:02 GMT
ENV PHP_SHA256=1db84fec57125aa93638b51bb2b15103e12ac196e2f960f0d124275b2687ea54
# Thu, 30 Nov 2023 23:29:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 30 Nov 2023 23:29:08 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 30 Nov 2023 23:32:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 30 Nov 2023 23:32:56 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 30 Nov 2023 23:32:57 GMT
RUN docker-php-ext-enable sodium
# Thu, 30 Nov 2023 23:32:57 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 30 Nov 2023 23:32:57 GMT
CMD ["php" "-a"]
# Fri, 01 Dec 2023 00:57:22 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client
# Fri, 01 Dec 2023 00:57:23 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html
# Fri, 01 Dec 2023 00:57:23 GMT
WORKDIR /var/www/html
# Fri, 01 Dec 2023 00:58:15 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Fri, 01 Dec 2023 00:58:16 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Fri, 01 Dec 2023 00:58:16 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Fri, 01 Dec 2023 00:58:16 GMT
ENV WORDPRESS_CLI_VERSION=2.9.0
# Fri, 01 Dec 2023 00:58:16 GMT
ENV WORDPRESS_CLI_SHA512=39fa365300ab45840e30cc344595bbd175c3558a4499679edd9f9e3a00a846e94179c29c80de3242f1c405f3623605605748d188d9bb98450d9377388f60f113
# Fri, 01 Dec 2023 00:58:18 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version
# Fri, 01 Dec 2023 00:58:18 GMT
VOLUME [/var/www/html]
# Fri, 01 Dec 2023 00:58:18 GMT
COPY file:b6efa5ff0423d61c2df0c8941b896844a8272d8516cdda0fcae8daaf56baac18 in /usr/local/bin/ 
# Fri, 01 Dec 2023 00:58:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 00:58:19 GMT
USER www-data
# Fri, 01 Dec 2023 00:58:19 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec91cb5b5977bc2c77c932761c9cd04eda4b0df9636a46228a4c0af65ad1b4f3`  
		Last Modified: Fri, 01 Dec 2023 00:40:05 GMT  
		Size: 2.7 MB (2717190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1563f945b2330cf35b9fc87a3f6456664dde2d6c4b6739047a9dd457f4a3d681`  
		Last Modified: Fri, 01 Dec 2023 00:40:04 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2549a9ef4a38d3afd713cc21e4de8fdf9a61d4d4f5b2897c0de403ec047f69a`  
		Last Modified: Fri, 01 Dec 2023 00:40:03 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285b1cbb8a2c86c2e2959b55b31fa9ac7abd053db302a937ce14d713aeaf8f44`  
		Last Modified: Fri, 01 Dec 2023 00:40:03 GMT  
		Size: 12.5 MB (12452091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42ac31d6bb70b19a698a7b74ae40261071bc6f22d09403fea931a7923ca8af18`  
		Last Modified: Fri, 01 Dec 2023 00:40:02 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6895913c4c7d243589b136d34c69cf54dc6e3aae7d5e785d8c35c570bb0e012`  
		Last Modified: Fri, 01 Dec 2023 00:40:06 GMT  
		Size: 17.1 MB (17056609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9aea783aa0077ad1860c83cdbc65d3ad9547ba0c7694359f04efe829bec772`  
		Last Modified: Fri, 01 Dec 2023 00:40:02 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f59963826a7f5193afec349b01fd624dd57a56e93881623c88faf7564007df02`  
		Last Modified: Fri, 01 Dec 2023 00:40:02 GMT  
		Size: 18.7 KB (18729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c656c8703723c9cf67ae463a497f642a588e37813b61b3fed56a079d4c7178a`  
		Last Modified: Fri, 01 Dec 2023 01:02:18 GMT  
		Size: 19.7 MB (19694236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc4cea44af12dc96cdfa8f0866778d204a4cf8db62cbd21d0f0b446ab7164be`  
		Last Modified: Fri, 01 Dec 2023 01:01:39 GMT  
		Size: 140.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23f44ffd7974fbe025f3a562a6d13f2b9f6b47bf04b036d31d1db50e8dde286b`  
		Last Modified: Fri, 01 Dec 2023 01:02:16 GMT  
		Size: 8.8 MB (8836624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cfa7a584ad7d76ddac8023d61bac5f70915a4019169cbcaf76f6a5ceee8e927`  
		Last Modified: Fri, 01 Dec 2023 01:02:15 GMT  
		Size: 391.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc6f04ce67e13ea935a93b4a97a9d36bda6efb8e17c6404c1bbd0fa7a77d308`  
		Last Modified: Fri, 01 Dec 2023 01:02:16 GMT  
		Size: 1.5 MB (1520862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec47d4ba390020832508a6385918cd7823fefb4771f77bd54dcbe51620e5a36`  
		Last Modified: Fri, 01 Dec 2023 01:02:15 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:cli-2-php8.3` - linux; s390x

```console
$ docker pull wordpress@sha256:cdb25fb8ecb8ad1a12872b7806d41c199af1017e97d8e0cb72ee80e04141d786
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.7 MB (65692047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09332fc8651b1e09e961308f4e87fe96d024a390d57b4650f13945add7fbf263`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Thu, 30 Nov 2023 22:42:08 GMT
ADD file:50d6643abf7df167a927decd69d193b980557ff73cca48dce86d57e2ff25ad45 in / 
# Thu, 30 Nov 2023 22:42:09 GMT
CMD ["/bin/sh"]
# Thu, 30 Nov 2023 22:45:06 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 30 Nov 2023 22:45:07 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 30 Nov 2023 22:45:08 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 30 Nov 2023 22:45:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 30 Nov 2023 22:45:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 30 Nov 2023 22:45:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 30 Nov 2023 22:45:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 30 Nov 2023 22:45:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 30 Nov 2023 22:45:09 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 30 Nov 2023 22:45:09 GMT
ENV PHP_VERSION=8.3.0
# Thu, 30 Nov 2023 22:45:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.0.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.0.tar.xz.asc
# Thu, 30 Nov 2023 22:45:09 GMT
ENV PHP_SHA256=1db84fec57125aa93638b51bb2b15103e12ac196e2f960f0d124275b2687ea54
# Thu, 30 Nov 2023 22:45:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 30 Nov 2023 22:45:14 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 30 Nov 2023 22:48:07 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 30 Nov 2023 22:48:09 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Thu, 30 Nov 2023 22:48:10 GMT
RUN docker-php-ext-enable sodium
# Thu, 30 Nov 2023 22:48:10 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 30 Nov 2023 22:48:10 GMT
CMD ["php" "-a"]
# Fri, 01 Dec 2023 02:24:49 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client
# Fri, 01 Dec 2023 02:24:52 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html
# Fri, 01 Dec 2023 02:24:52 GMT
WORKDIR /var/www/html
# Fri, 01 Dec 2023 02:25:40 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Fri, 01 Dec 2023 02:25:42 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Fri, 01 Dec 2023 02:25:42 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Fri, 01 Dec 2023 02:25:42 GMT
ENV WORDPRESS_CLI_VERSION=2.9.0
# Fri, 01 Dec 2023 02:25:42 GMT
ENV WORDPRESS_CLI_SHA512=39fa365300ab45840e30cc344595bbd175c3558a4499679edd9f9e3a00a846e94179c29c80de3242f1c405f3623605605748d188d9bb98450d9377388f60f113
# Fri, 01 Dec 2023 02:25:45 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version
# Fri, 01 Dec 2023 02:25:45 GMT
VOLUME [/var/www/html]
# Fri, 01 Dec 2023 02:25:45 GMT
COPY file:b6efa5ff0423d61c2df0c8941b896844a8272d8516cdda0fcae8daaf56baac18 in /usr/local/bin/ 
# Fri, 01 Dec 2023 02:25:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 02:25:46 GMT
USER www-data
# Fri, 01 Dec 2023 02:25:46 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:2ea477e1c0c3db3337ee1d7c659f8c465021a65c036998ed3fa3b667d4b30153`  
		Last Modified: Thu, 30 Nov 2023 22:42:52 GMT  
		Size: 3.2 MB (3217454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa5313d02d4fcc59703ea6bd09df7b0df122fc73121b0954b541c214229202e`  
		Last Modified: Thu, 30 Nov 2023 23:47:29 GMT  
		Size: 2.8 MB (2789878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f082f983656d312447043a024c0fa5528e4055dbd73f4101ac38d1d2d3158ea`  
		Last Modified: Thu, 30 Nov 2023 23:47:28 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35feaf89a3d400114f4864637453e2e21cd9e7cb6a859699bd6272483f3a56ee`  
		Last Modified: Thu, 30 Nov 2023 23:47:28 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b59844514cd33789360a3e46dbaff2cdae06b8cd8d18ee9449808c168be15f9`  
		Last Modified: Thu, 30 Nov 2023 23:47:27 GMT  
		Size: 12.5 MB (12452093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:090f8111976872dd0d1fdf290acf04666250d582cbba875706f055725bc42aff`  
		Last Modified: Thu, 30 Nov 2023 23:47:27 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398c5ca7cbe876f0f1cf80bef52d39ccd6949d12e9836af8af296afb1084c144`  
		Last Modified: Thu, 30 Nov 2023 23:47:30 GMT  
		Size: 16.0 MB (15956254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa90b5b8b99ecde21a6c31cb4effceb2e48d33b4feeb73b3a12ec4545c63d32a`  
		Last Modified: Thu, 30 Nov 2023 23:47:27 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a82796f38dbb8536e9be3b686e7716a2916e08c53622bf88c55aa3ed67802d0`  
		Last Modified: Thu, 30 Nov 2023 23:47:27 GMT  
		Size: 18.8 KB (18764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e8fd324243b4c9e93f5d78ef4a8d6dc4b0bddb9a358bfae9afe5dea61ac829c`  
		Last Modified: Fri, 01 Dec 2023 02:29:11 GMT  
		Size: 20.8 MB (20832329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:556dc8c652c0234b3ccefd0b45f0fe6927d5bf5722aa8867d1c88c56ef081da6`  
		Last Modified: Fri, 01 Dec 2023 02:28:43 GMT  
		Size: 140.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e98e6776c3e073c21b1b147c36c438773e3ec15f1aa6a924c3f5e3497e38198b`  
		Last Modified: Fri, 01 Dec 2023 02:29:08 GMT  
		Size: 8.9 MB (8898981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03e4564f6c118bf21a489bfa0b806f8f812172c4d179421573501c92793a6df1`  
		Last Modified: Fri, 01 Dec 2023 02:29:07 GMT  
		Size: 391.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b72a5decb2807e71b11fc8bc803679b2c6f7d5250bafcd3d1ac365d675dd7567`  
		Last Modified: Fri, 01 Dec 2023 02:29:07 GMT  
		Size: 1.5 MB (1520884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a75884bef630dd8ade141c56e4e950d0d0bc46c1e344e38628af7df26eb43e`  
		Last Modified: Fri, 01 Dec 2023 02:29:07 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
