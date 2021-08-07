## `wordpress:cli-php8.0`

```console
$ docker pull wordpress@sha256:96803b3714096d5466faa0e3ba6627cf0b694a33bb0be89d7df0400aa0bcd171
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

### `wordpress:cli-php8.0` - linux; amd64

```console
$ docker pull wordpress@sha256:ac7a594f87c24607a06c7a18bfd59a92adfcfcb9646cda83729e7e90b0aa1055
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45916819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f7ab79dabb925cf93cb7945ea7600f2a3d3b78584c256c7576989b1831ebed6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Tue, 15 Jun 2021 22:19:37 GMT
ADD file:f278386b0cef68136129f5f58c52445590a417b624d62bca158d4dc926c340df in / 
# Tue, 15 Jun 2021 22:19:37 GMT
CMD ["/bin/sh"]
# Wed, 16 Jun 2021 23:32:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 16 Jun 2021 23:32:47 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 16 Jun 2021 23:32:48 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 16 Jun 2021 23:32:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 16 Jun 2021 23:32:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 16 Jun 2021 23:32:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 16 Jun 2021 23:32:50 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 16 Jun 2021 23:32:50 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 16 Jun 2021 23:35:57 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 30 Jul 2021 00:51:38 GMT
ENV PHP_VERSION=8.0.9
# Fri, 30 Jul 2021 00:51:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.9.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.9.tar.xz.asc
# Fri, 30 Jul 2021 00:51:38 GMT
ENV PHP_SHA256=71a01b2b56544e20e28696ad5b366e431a0984eaa39aa5e35426a4843e172010
# Fri, 30 Jul 2021 00:51:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 30 Jul 2021 00:51:45 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 30 Jul 2021 00:58:39 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 30 Jul 2021 00:58:39 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Fri, 30 Jul 2021 00:58:41 GMT
RUN docker-php-ext-enable sodium
# Fri, 30 Jul 2021 00:58:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 30 Jul 2021 00:58:41 GMT
CMD ["php" "-a"]
# Fri, 30 Jul 2021 04:53:10 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client
# Fri, 30 Jul 2021 04:53:12 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html
# Fri, 30 Jul 2021 04:53:12 GMT
WORKDIR /var/www/html
# Fri, 30 Jul 2021 04:53:58 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		mysqli 		zip 	; 	pecl install imagick-3.5.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps
# Fri, 30 Jul 2021 04:53:59 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Fri, 30 Jul 2021 04:53:59 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Fri, 30 Jul 2021 04:53:59 GMT
ENV WORDPRESS_CLI_VERSION=2.5.0
# Fri, 30 Jul 2021 04:54:00 GMT
ENV WORDPRESS_CLI_SHA512=08dd9035fda1d529807380d5b757839e2809e289eb1a698fe33e7e21a1431d3f77c551c2b2db5adc55083d5075ea4137407994111890f765e790a97e6d9ca7af
# Fri, 30 Jul 2021 04:54:02 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version
# Fri, 30 Jul 2021 04:54:02 GMT
VOLUME [/var/www/html]
# Fri, 30 Jul 2021 04:54:03 GMT
COPY file:b6efa5ff0423d61c2df0c8941b896844a8272d8516cdda0fcae8daaf56baac18 in /usr/local/bin/ 
# Fri, 30 Jul 2021 04:54:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 Jul 2021 04:54:03 GMT
USER www-data
# Fri, 30 Jul 2021 04:54:03 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:5843afab387455b37944e709ee8c78d7520df80f8d01cf7f861aae63beeddb6b`  
		Last Modified: Tue, 15 Jun 2021 22:20:04 GMT  
		Size: 2.8 MB (2811478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfcf566573f3f708d78b43786614663e55d9a9d02621f3dab2127292efbbacab`  
		Last Modified: Fri, 25 Jun 2021 21:36:24 GMT  
		Size: 1.7 MB (1707289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ff9828d9544109bb07a2fa8308b1ed77b75738fa50300d61284755c126426a`  
		Last Modified: Fri, 25 Jun 2021 21:36:24 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165b10189b0ff16bb4ac114562bc55a25c753c9fc11999774fc42e9979feef99`  
		Last Modified: Fri, 25 Jun 2021 21:36:23 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b173a4f4479608ae0259d421ebcaa47a791f7e7f9a0c2a56c80808c9a147070a`  
		Last Modified: Fri, 30 Jul 2021 02:21:46 GMT  
		Size: 10.7 MB (10698212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65667bc930e86953f8b27d435c0d6717417dc671d57fc119ff9d05e7da68094f`  
		Last Modified: Fri, 30 Jul 2021 02:21:45 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1110963b7e5c1853d0e443aa63f56c95638638b0aad7381e6b75543a3a8434c`  
		Last Modified: Fri, 30 Jul 2021 02:21:48 GMT  
		Size: 15.2 MB (15205231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b486066f940355876565c63fcca619584fcd9939310d0b12b9954b687c5a998`  
		Last Modified: Fri, 30 Jul 2021 02:21:45 GMT  
		Size: 2.3 KB (2264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1908b790d85cd0e907e97e0e62f5b4d186e85dcb3f912a395dcb9da39c8bccb0`  
		Last Modified: Fri, 30 Jul 2021 02:21:45 GMT  
		Size: 17.8 KB (17818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1258326442b148973c05e59d8b1bd59459cbabe3a32f969bec4e10e4220e573`  
		Last Modified: Fri, 30 Jul 2021 04:59:54 GMT  
		Size: 9.4 MB (9350027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5186b173f6e5492775546a3c6dd896c2e8cd505ee30ff1e1014c893965e2bdc8`  
		Last Modified: Fri, 30 Jul 2021 04:59:50 GMT  
		Size: 145.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d37586ec1bebd0be8dfbc0011a0ab808fdc3dc9345804e4e7841e35b75eae7a`  
		Last Modified: Fri, 30 Jul 2021 04:59:51 GMT  
		Size: 4.8 MB (4806172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:115b53158d38c9fa5f3bd470c1c221269e4119d3007473ad88cccaf5ac67c4c8`  
		Last Modified: Fri, 30 Jul 2021 04:59:50 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0d885d07dafb25db6564abdd8d3d82c834015d9a942e3d5e64202e7303723f`  
		Last Modified: Fri, 30 Jul 2021 04:59:50 GMT  
		Size: 1.3 MB (1315361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc02c131cc46fec3de86102f251306924aa28fc8b3062e71d42f3d5b00658f4`  
		Last Modified: Fri, 30 Jul 2021 04:59:50 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:cli-php8.0` - linux; arm variant v6

```console
$ docker pull wordpress@sha256:dfb9b3bfb0d85fa57719f2724fe1cf92c85b4fc9265edec9f09db72ad34e942e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43564968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3f7ec364b6ed7bc7d7f60d80f258e461899f98c443a77d7304bcac53a41ecb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Fri, 06 Aug 2021 17:49:32 GMT
ADD file:7f2c7deda009eabdcbbdccb11e854043d32c498e64e7e1ca02165d7bb4261d39 in / 
# Fri, 06 Aug 2021 17:49:32 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 20:25:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 06 Aug 2021 20:25:29 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 06 Aug 2021 20:25:30 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 06 Aug 2021 20:25:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 06 Aug 2021 20:25:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 06 Aug 2021 20:25:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Aug 2021 20:25:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Aug 2021 20:25:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 06 Aug 2021 20:35:54 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 06 Aug 2021 20:35:55 GMT
ENV PHP_VERSION=8.0.9
# Fri, 06 Aug 2021 20:35:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.9.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.9.tar.xz.asc
# Fri, 06 Aug 2021 20:35:56 GMT
ENV PHP_SHA256=71a01b2b56544e20e28696ad5b366e431a0984eaa39aa5e35426a4843e172010
# Fri, 06 Aug 2021 20:36:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 06 Aug 2021 20:36:05 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 06 Aug 2021 20:40:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 06 Aug 2021 20:40:32 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Fri, 06 Aug 2021 20:40:35 GMT
RUN docker-php-ext-enable sodium
# Fri, 06 Aug 2021 20:40:36 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 06 Aug 2021 20:40:36 GMT
CMD ["php" "-a"]
# Sat, 07 Aug 2021 02:45:16 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client
# Sat, 07 Aug 2021 02:45:17 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html
# Sat, 07 Aug 2021 02:45:18 GMT
WORKDIR /var/www/html
# Sat, 07 Aug 2021 02:47:07 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		mysqli 		zip 	; 	pecl install imagick-3.5.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps
# Sat, 07 Aug 2021 02:47:09 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Sat, 07 Aug 2021 02:47:10 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Sat, 07 Aug 2021 02:47:10 GMT
ENV WORDPRESS_CLI_VERSION=2.5.0
# Sat, 07 Aug 2021 02:47:11 GMT
ENV WORDPRESS_CLI_SHA512=08dd9035fda1d529807380d5b757839e2809e289eb1a698fe33e7e21a1431d3f77c551c2b2db5adc55083d5075ea4137407994111890f765e790a97e6d9ca7af
# Sat, 07 Aug 2021 02:47:15 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version
# Sat, 07 Aug 2021 02:47:16 GMT
VOLUME [/var/www/html]
# Sat, 07 Aug 2021 02:47:16 GMT
COPY file:b6efa5ff0423d61c2df0c8941b896844a8272d8516cdda0fcae8daaf56baac18 in /usr/local/bin/ 
# Sat, 07 Aug 2021 02:47:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 07 Aug 2021 02:47:17 GMT
USER www-data
# Sat, 07 Aug 2021 02:47:18 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:f465bb3e9fcd0c42f936ecc566c6e40353c00f3089b2b2c2ea1663c30f89d3ab`  
		Last Modified: Fri, 06 Aug 2021 17:51:00 GMT  
		Size: 2.6 MB (2626350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c308e0cc29c44fbd995ee591fe7289bde1e488176fb402318132d40caa05c299`  
		Last Modified: Fri, 06 Aug 2021 21:25:23 GMT  
		Size: 1.7 MB (1696670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:983c92fbbed0d3241e2a4aa8f6ec320484791f6923f18c795878fea03971b8bd`  
		Last Modified: Fri, 06 Aug 2021 21:25:22 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1f89139d48debd7c21fa5272e8bb4a983181e2f8d1f37a9f65ee5c99086cd7c`  
		Last Modified: Fri, 06 Aug 2021 21:25:22 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c34db1d62e96009a0fe4726eac49a986250cee2ee98f46fff14e1b95f4d7b391`  
		Last Modified: Fri, 06 Aug 2021 21:26:50 GMT  
		Size: 10.7 MB (10698215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d4c4b169f6777079cd1e30d47c14f8b4cbf94c127de86a8ee4c851da614baa`  
		Last Modified: Fri, 06 Aug 2021 21:26:48 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc16aa4475c8b7ebcdc107941aa0cdc9478d6b958cbf667cc3da0ca39bbba204`  
		Last Modified: Fri, 06 Aug 2021 21:26:58 GMT  
		Size: 13.6 MB (13605357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f161520581756b99b6efe0aebb47ceeff57c0f3bd9e964b5a7cfb641817508b`  
		Last Modified: Fri, 06 Aug 2021 21:26:48 GMT  
		Size: 2.3 KB (2267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516d65a37a98bd783dd3c4ec1e007dd8d1c055c6caf595a9eaf2a2f4b0d5a71b`  
		Last Modified: Fri, 06 Aug 2021 21:26:49 GMT  
		Size: 17.8 KB (17798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1260ac6d7d529eb121317cfd287eb5e1ba1e02d5b3e3fc6ea2c7f38cc07e2b7`  
		Last Modified: Sat, 07 Aug 2021 02:53:51 GMT  
		Size: 9.0 MB (8956975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c24ecf9446cfd20852bba25849c8c15954adcb906cbf7a07f85488a63bc38fbd`  
		Last Modified: Sat, 07 Aug 2021 02:53:43 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ac2e6237ebe6d0fa2930c4c282b9905c1e4900a8a69c73d45997bd3507eb02`  
		Last Modified: Sat, 07 Aug 2021 02:53:46 GMT  
		Size: 4.6 MB (4643051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b53c612576eafc025b81ff3cdfcaa90fbb4d4e7ab759f06516deb34633446030`  
		Last Modified: Sat, 07 Aug 2021 02:53:43 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67568d5b01cee562175ceb7df97f8b686feb5002bd0488054cdc21867969bb38`  
		Last Modified: Sat, 07 Aug 2021 02:53:45 GMT  
		Size: 1.3 MB (1315318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aad8b970dc58a43306b8b8804570b4059b724f7a4ee28139bcc9f3d84ab69038`  
		Last Modified: Sat, 07 Aug 2021 02:53:43 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:cli-php8.0` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:47c03ffc791b98544199ab711e2f4f913ade33809f6d69ceed00128b05c8cbb9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.8 MB (41758740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c454dda2e2e484980231c0e1bf98f9aaa4d984345e8e0dd5fd9e8d0ccdc723b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Fri, 30 Jul 2021 18:36:19 GMT
ADD file:416a8b507abdc6bdcb22997a4be0a4170796c3f9f77e315b2dbff2b0a212bc68 in / 
# Fri, 30 Jul 2021 18:36:20 GMT
CMD ["/bin/sh"]
# Sat, 31 Jul 2021 06:33:39 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 31 Jul 2021 06:33:42 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 31 Jul 2021 06:33:44 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 31 Jul 2021 06:33:44 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 31 Jul 2021 06:33:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 31 Jul 2021 06:33:46 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 31 Jul 2021 06:33:46 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 31 Jul 2021 06:33:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 31 Jul 2021 06:54:16 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Sat, 31 Jul 2021 06:54:16 GMT
ENV PHP_VERSION=8.0.9
# Sat, 31 Jul 2021 06:54:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.9.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.9.tar.xz.asc
# Sat, 31 Jul 2021 06:54:17 GMT
ENV PHP_SHA256=71a01b2b56544e20e28696ad5b366e431a0984eaa39aa5e35426a4843e172010
# Sat, 31 Jul 2021 06:54:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 31 Jul 2021 06:54:26 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 31 Jul 2021 06:58:46 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 31 Jul 2021 06:58:48 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Sat, 31 Jul 2021 06:58:50 GMT
RUN docker-php-ext-enable sodium
# Sat, 31 Jul 2021 06:58:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 31 Jul 2021 06:58:51 GMT
CMD ["php" "-a"]
# Sat, 31 Jul 2021 16:21:27 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client
# Sat, 31 Jul 2021 16:21:28 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html
# Sat, 31 Jul 2021 16:21:29 GMT
WORKDIR /var/www/html
# Sat, 31 Jul 2021 16:23:13 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		mysqli 		zip 	; 	pecl install imagick-3.5.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps
# Sat, 31 Jul 2021 16:23:15 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Sat, 31 Jul 2021 16:23:16 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Sat, 31 Jul 2021 16:23:16 GMT
ENV WORDPRESS_CLI_VERSION=2.5.0
# Sat, 31 Jul 2021 16:23:16 GMT
ENV WORDPRESS_CLI_SHA512=08dd9035fda1d529807380d5b757839e2809e289eb1a698fe33e7e21a1431d3f77c551c2b2db5adc55083d5075ea4137407994111890f765e790a97e6d9ca7af
# Sat, 31 Jul 2021 16:23:21 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version
# Sat, 31 Jul 2021 16:23:21 GMT
VOLUME [/var/www/html]
# Sat, 31 Jul 2021 16:23:22 GMT
COPY file:b6efa5ff0423d61c2df0c8941b896844a8272d8516cdda0fcae8daaf56baac18 in /usr/local/bin/ 
# Sat, 31 Jul 2021 16:23:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jul 2021 16:23:23 GMT
USER www-data
# Sat, 31 Jul 2021 16:23:23 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:136482bf81d1fa351b424ebb8c7e34d15f2c5ed3fc0b66b544b8312bda3d52d9`  
		Last Modified: Tue, 15 Jun 2021 23:16:40 GMT  
		Size: 2.4 MB (2427917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c695d54d72235b2a641e5c0e2982ce2288faafa7c7a15cf38314d32eadde549a`  
		Last Modified: Sat, 31 Jul 2021 08:31:05 GMT  
		Size: 1.6 MB (1564631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62bcce9183bdd1bc68e82fa8188ef251388c691dafd2352ad787ddb168450e33`  
		Last Modified: Sat, 31 Jul 2021 08:31:04 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a89d6c9a81dd0be6901229c1d2f4adae785f73bf6302ddbd7eb88227ec22de0b`  
		Last Modified: Sat, 31 Jul 2021 08:31:03 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b76249c6065efd4cb7e6bd20b5a01815dca0d9e1fc7e9de57cd8c2277c4e35e`  
		Last Modified: Sat, 31 Jul 2021 08:34:07 GMT  
		Size: 10.7 MB (10698205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4df09276fd7fbb2c2bec23c2abb089272b45d8bcc4fa9c5c75076465e70cf4ba`  
		Last Modified: Sat, 31 Jul 2021 08:34:05 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e0c3752cb2d70a0a0c0ce4d947f12300905c1187bbfeb5f73ee5cd0d6bf579`  
		Last Modified: Sat, 31 Jul 2021 08:34:13 GMT  
		Size: 12.7 MB (12738240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ecd88ab2254febda5ef9c0b8cdb6e53297c691a13bb00eb15c41eb7f72342da`  
		Last Modified: Sat, 31 Jul 2021 08:34:05 GMT  
		Size: 2.3 KB (2266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a5ec8debacc64d9cfb994f2a914c2b04aad14edddf5271a313610fd24959d25`  
		Last Modified: Sat, 31 Jul 2021 08:34:04 GMT  
		Size: 17.8 KB (17787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ce77cbb9896e82e7bed5a46baefd3beaa016cb4fa52f46f2c2656418d15eb33`  
		Last Modified: Sat, 31 Jul 2021 16:34:16 GMT  
		Size: 8.7 MB (8670780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:841271a383b69973abe449e8a10d2fd9f038faa0aaa3595a53347fae48b4d70a`  
		Last Modified: Sat, 31 Jul 2021 16:34:08 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5413dc57e47e23ffc56a8752dad99dd8be4b6b2b1e8f4334c03935b33236fc77`  
		Last Modified: Sat, 31 Jul 2021 16:34:11 GMT  
		Size: 4.3 MB (4320648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:807824704e3c39fecabac40874cdce00ccb771c9698d03543e69d4203b0a6360`  
		Last Modified: Sat, 31 Jul 2021 16:34:08 GMT  
		Size: 392.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5db3b4d6ca24e427c774ff6ba07614d054cfd11706721274cb36aa777cfdc68d`  
		Last Modified: Sat, 31 Jul 2021 16:34:09 GMT  
		Size: 1.3 MB (1315296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9715b5bb874472cf975ab5bea77bcaade2a3e8306622a54c16c5da5ba5e86ef1`  
		Last Modified: Sat, 31 Jul 2021 16:34:08 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:cli-php8.0` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:c50fd7a10ff671eb008b209911b1b6a1c41d4d9d96a81e54497d2ba5defbef0b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45146430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a63739eb9d87a3c15435ebc54e246b470bb9b6c09b856b86e79cdf44f68f1da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Tue, 15 Jun 2021 21:44:56 GMT
ADD file:6797caacbfe41bfe44000b39ed017016c6fcc492b3d6557cdaba88536df6c876 in / 
# Tue, 15 Jun 2021 21:44:56 GMT
CMD ["/bin/sh"]
# Wed, 16 Jun 2021 22:42:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 16 Jun 2021 22:42:41 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 16 Jun 2021 22:42:42 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 16 Jun 2021 22:42:42 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 16 Jun 2021 22:42:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 16 Jun 2021 22:42:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 16 Jun 2021 22:42:44 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 16 Jun 2021 22:42:44 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 16 Jun 2021 22:46:39 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Thu, 29 Jul 2021 22:58:10 GMT
ENV PHP_VERSION=8.0.9
# Thu, 29 Jul 2021 22:58:10 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.9.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.9.tar.xz.asc
# Thu, 29 Jul 2021 22:58:10 GMT
ENV PHP_SHA256=71a01b2b56544e20e28696ad5b366e431a0984eaa39aa5e35426a4843e172010
# Thu, 29 Jul 2021 22:58:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 29 Jul 2021 22:58:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 29 Jul 2021 23:03:08 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 29 Jul 2021 23:03:08 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Thu, 29 Jul 2021 23:03:09 GMT
RUN docker-php-ext-enable sodium
# Thu, 29 Jul 2021 23:03:10 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 29 Jul 2021 23:03:10 GMT
CMD ["php" "-a"]
# Fri, 30 Jul 2021 02:57:58 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client
# Fri, 30 Jul 2021 02:57:59 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html
# Fri, 30 Jul 2021 02:57:59 GMT
WORKDIR /var/www/html
# Fri, 30 Jul 2021 02:58:45 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		mysqli 		zip 	; 	pecl install imagick-3.5.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps
# Fri, 30 Jul 2021 02:58:45 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Fri, 30 Jul 2021 02:58:45 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Fri, 30 Jul 2021 02:58:46 GMT
ENV WORDPRESS_CLI_VERSION=2.5.0
# Fri, 30 Jul 2021 02:58:46 GMT
ENV WORDPRESS_CLI_SHA512=08dd9035fda1d529807380d5b757839e2809e289eb1a698fe33e7e21a1431d3f77c551c2b2db5adc55083d5075ea4137407994111890f765e790a97e6d9ca7af
# Fri, 30 Jul 2021 02:58:48 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version
# Fri, 30 Jul 2021 02:58:48 GMT
VOLUME [/var/www/html]
# Fri, 30 Jul 2021 02:58:48 GMT
COPY file:b6efa5ff0423d61c2df0c8941b896844a8272d8516cdda0fcae8daaf56baac18 in /usr/local/bin/ 
# Fri, 30 Jul 2021 02:58:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 Jul 2021 02:58:49 GMT
USER www-data
# Fri, 30 Jul 2021 02:58:49 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:58ab47519297212468320b23b8100fc1b2b96e8d342040806ae509a778a0a07a`  
		Last Modified: Tue, 15 Jun 2021 21:46:03 GMT  
		Size: 2.7 MB (2709626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1dbb31d082d4e4f90933b28b4719802e03a2261dafc489b60e4c94dd8f4e56a`  
		Last Modified: Fri, 25 Jun 2021 20:47:47 GMT  
		Size: 1.7 MB (1709425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:681ea156e05a3343d484d4b75ca6196085b59763b04185e7a76b8c4a5b355568`  
		Last Modified: Fri, 25 Jun 2021 20:47:47 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e1c9b66e33460d7ebc60517e350c7107ee8977e3f6b05d2be0a44b4758d1c6`  
		Last Modified: Fri, 25 Jun 2021 20:47:46 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa40339f9b15574b6aea17326e0af49343ea4217ef38c53834c3d05ad80c28f`  
		Last Modified: Fri, 30 Jul 2021 00:15:28 GMT  
		Size: 10.7 MB (10698213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4daac18033cee87cc3aaa0aca17b82c68a013e40ef45359f6c1a7ffc8fdc0155`  
		Last Modified: Fri, 30 Jul 2021 00:15:27 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb86a782a89eaecb505ef6b34a32d7a0b3403d07f85637ca7f772530ec0f51b6`  
		Last Modified: Fri, 30 Jul 2021 00:15:30 GMT  
		Size: 14.6 MB (14644245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24fc58adec9a83541faf564d04b2504e4ea050a314ee36620e667da81931b425`  
		Last Modified: Fri, 30 Jul 2021 00:15:27 GMT  
		Size: 2.3 KB (2265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d32f91ebb2257b4ff2393dcb58477aa3f7c5188c6f28cbcaa0d72d24925d9a`  
		Last Modified: Fri, 30 Jul 2021 00:15:27 GMT  
		Size: 17.8 KB (17817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a51dfbc8035cb4902dd3be52109c267311255d35c4b043959e77f9640d15ed`  
		Last Modified: Fri, 30 Jul 2021 03:07:11 GMT  
		Size: 9.4 MB (9400208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43222a0b48b66dfdc2c16ceae2955464bcc5b79d6777677eb640e4dae6fca227`  
		Last Modified: Fri, 30 Jul 2021 03:07:07 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf5ad5a81dcf2a40266154f01794774294b40bac6fdc46e3c94b463e8f4c7f6`  
		Last Modified: Fri, 30 Jul 2021 03:07:07 GMT  
		Size: 4.6 MB (4646319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e494f6faee827ee363db178614d29175e3304c997bd0fd5650fb61e95a396e`  
		Last Modified: Fri, 30 Jul 2021 03:07:07 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b05b6abc101bc3eacf15abc1430b5a0b08402d041e8d399adc2d2ee5c47705`  
		Last Modified: Fri, 30 Jul 2021 03:07:07 GMT  
		Size: 1.3 MB (1315346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b789da21ff744b2267ded38c392899a374d18fd28c6621eaebd6d257877f014`  
		Last Modified: Fri, 30 Jul 2021 03:07:06 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:cli-php8.0` - linux; 386

```console
$ docker pull wordpress@sha256:02b2c361dc587d51a8e3c61d44324a3322a57c4ff60fc56afb19401ceffe6b93
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46733977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:330b3511482c612d138211be4f53a03e97f3605c820ce643fbd9e6efa8f82f40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Tue, 15 Jun 2021 21:38:30 GMT
ADD file:3b0fe1454491bb05e218b090fd461f2fd39546aa4a53eb3f953ee8eae149ac57 in / 
# Tue, 15 Jun 2021 21:38:30 GMT
CMD ["/bin/sh"]
# Wed, 16 Jun 2021 22:42:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 16 Jun 2021 22:42:50 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 16 Jun 2021 22:42:51 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 16 Jun 2021 22:42:51 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 16 Jun 2021 22:42:52 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 16 Jun 2021 22:42:52 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 16 Jun 2021 22:42:53 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 16 Jun 2021 22:42:53 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 16 Jun 2021 22:46:53 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Thu, 29 Jul 2021 21:24:47 GMT
ENV PHP_VERSION=8.0.9
# Thu, 29 Jul 2021 21:24:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.9.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.9.tar.xz.asc
# Thu, 29 Jul 2021 21:24:48 GMT
ENV PHP_SHA256=71a01b2b56544e20e28696ad5b366e431a0984eaa39aa5e35426a4843e172010
# Thu, 29 Jul 2021 21:24:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 29 Jul 2021 21:24:55 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 29 Jul 2021 21:34:18 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 29 Jul 2021 21:34:18 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Thu, 29 Jul 2021 21:34:20 GMT
RUN docker-php-ext-enable sodium
# Thu, 29 Jul 2021 21:34:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 29 Jul 2021 21:34:20 GMT
CMD ["php" "-a"]
# Fri, 30 Jul 2021 03:52:12 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client
# Fri, 30 Jul 2021 03:52:13 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html
# Fri, 30 Jul 2021 03:52:13 GMT
WORKDIR /var/www/html
# Fri, 30 Jul 2021 03:53:17 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		mysqli 		zip 	; 	pecl install imagick-3.5.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps
# Fri, 30 Jul 2021 03:53:18 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Fri, 30 Jul 2021 03:53:18 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Fri, 30 Jul 2021 03:53:18 GMT
ENV WORDPRESS_CLI_VERSION=2.5.0
# Fri, 30 Jul 2021 03:53:18 GMT
ENV WORDPRESS_CLI_SHA512=08dd9035fda1d529807380d5b757839e2809e289eb1a698fe33e7e21a1431d3f77c551c2b2db5adc55083d5075ea4137407994111890f765e790a97e6d9ca7af
# Fri, 30 Jul 2021 03:53:21 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version
# Fri, 30 Jul 2021 03:53:22 GMT
VOLUME [/var/www/html]
# Fri, 30 Jul 2021 03:53:22 GMT
COPY file:b6efa5ff0423d61c2df0c8941b896844a8272d8516cdda0fcae8daaf56baac18 in /usr/local/bin/ 
# Fri, 30 Jul 2021 03:53:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 Jul 2021 03:53:22 GMT
USER www-data
# Fri, 30 Jul 2021 03:53:23 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:be21df321efb39c5daf3151073ebff7688e15ea6cd5158878bc9559a5db76ac6`  
		Last Modified: Tue, 15 Jun 2021 21:39:16 GMT  
		Size: 2.8 MB (2820718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c93eab99e0ef5f9d723ae4897063553cae85d76d084993a6ef1f4753c87cc5be`  
		Last Modified: Fri, 25 Jun 2021 21:42:26 GMT  
		Size: 1.8 MB (1804771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed49b65d5b9099a8d60337fc7a53d1ab0b053dc9d9ed95f1d212417c2f502f9`  
		Last Modified: Fri, 25 Jun 2021 21:42:26 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cf026c104ba1de5b61fbc98582049fd882405b54f7b58a5db53aa5b999ff14c`  
		Last Modified: Fri, 25 Jun 2021 21:42:26 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c412b324b588195ffab2eba8f07b051defdd26d1972c855f288f174ff417601`  
		Last Modified: Fri, 30 Jul 2021 00:14:25 GMT  
		Size: 10.7 MB (10698203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30b2db1ba879039c87818c0eb16027ad371607a700c2d5747961ef591969ef02`  
		Last Modified: Fri, 30 Jul 2021 00:14:23 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12b30b21961791da104bbe501bb3fa23723c1a0ee30c982a8b9bb01d0034aba6`  
		Last Modified: Fri, 30 Jul 2021 00:14:28 GMT  
		Size: 15.6 MB (15581477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aea72e74f0dd32f4917b43e58aeb0c566783e8a3d9ecc9620cff1f3eb897e2a`  
		Last Modified: Fri, 30 Jul 2021 00:14:24 GMT  
		Size: 2.3 KB (2261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de202126995b946dae76f1d8581a79ae2faba507147305e4ee2bb1e1f63a6a44`  
		Last Modified: Fri, 30 Jul 2021 00:14:24 GMT  
		Size: 17.8 KB (17820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a1f59b07d3a3fc673a3a6bc07078a3bdd5874009c46b35dc83bdfce0a7abc11`  
		Last Modified: Fri, 30 Jul 2021 04:02:31 GMT  
		Size: 9.5 MB (9513190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9aba86dc8e83d2d7ca36be0aa1f2846e5571a4d7461c561c4088345f23c254d`  
		Last Modified: Fri, 30 Jul 2021 04:02:26 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aacf5ab3a0120d0dccc82d20043a0aea9450d4394f7eb9da929b1e9c9673912`  
		Last Modified: Fri, 30 Jul 2021 04:02:27 GMT  
		Size: 5.0 MB (4977205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a833c9b1440f4426e9952b1546d2e32923ec258f6804e5bff3f942a7c1f65a3`  
		Last Modified: Fri, 30 Jul 2021 04:02:26 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:605945180b768752e80872ecd45c05aeac0e79076d241f7501a9d7e4b276db4d`  
		Last Modified: Fri, 30 Jul 2021 04:02:27 GMT  
		Size: 1.3 MB (1315362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f1b73d5ea9ac321d2dec200c4e9386a28296378804a10f6c03f2ef18c8a40f`  
		Last Modified: Fri, 30 Jul 2021 04:02:26 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:cli-php8.0` - linux; ppc64le

```console
$ docker pull wordpress@sha256:bc1a27c7e4692f8d9c7f4b8d92c35fc696351651526efab846c99a184e84760f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46742568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7284d02a700a0f234147135ec9acc3bf667dc618be82a48e5238e7c6f1a326f6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Fri, 30 Jul 2021 17:24:32 GMT
ADD file:0075aad7a94f0496483442bb2d9fdaa13e9c23087b90638d014b4bc263aa3861 in / 
# Fri, 30 Jul 2021 17:24:37 GMT
CMD ["/bin/sh"]
# Sat, 31 Jul 2021 02:06:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 31 Jul 2021 02:07:04 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 31 Jul 2021 02:07:21 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 31 Jul 2021 02:07:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 31 Jul 2021 02:07:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 31 Jul 2021 02:07:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 31 Jul 2021 02:07:44 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 31 Jul 2021 02:07:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 31 Jul 2021 02:33:52 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Sat, 31 Jul 2021 02:33:54 GMT
ENV PHP_VERSION=8.0.9
# Sat, 31 Jul 2021 02:33:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.9.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.9.tar.xz.asc
# Sat, 31 Jul 2021 02:33:59 GMT
ENV PHP_SHA256=71a01b2b56544e20e28696ad5b366e431a0984eaa39aa5e35426a4843e172010
# Sat, 31 Jul 2021 02:34:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 31 Jul 2021 02:34:16 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 31 Jul 2021 02:39:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 31 Jul 2021 02:39:07 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Sat, 31 Jul 2021 02:39:15 GMT
RUN docker-php-ext-enable sodium
# Sat, 31 Jul 2021 02:39:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 31 Jul 2021 02:39:40 GMT
CMD ["php" "-a"]
# Sat, 31 Jul 2021 13:09:14 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client
# Sat, 31 Jul 2021 13:09:24 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html
# Sat, 31 Jul 2021 13:09:28 GMT
WORKDIR /var/www/html
# Sat, 31 Jul 2021 13:10:40 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		mysqli 		zip 	; 	pecl install imagick-3.5.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps
# Sat, 31 Jul 2021 13:10:53 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Sat, 31 Jul 2021 13:10:57 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Sat, 31 Jul 2021 13:11:00 GMT
ENV WORDPRESS_CLI_VERSION=2.5.0
# Sat, 31 Jul 2021 13:11:02 GMT
ENV WORDPRESS_CLI_SHA512=08dd9035fda1d529807380d5b757839e2809e289eb1a698fe33e7e21a1431d3f77c551c2b2db5adc55083d5075ea4137407994111890f765e790a97e6d9ca7af
# Sat, 31 Jul 2021 13:11:22 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version
# Sat, 31 Jul 2021 13:11:24 GMT
VOLUME [/var/www/html]
# Sat, 31 Jul 2021 13:11:26 GMT
COPY file:b6efa5ff0423d61c2df0c8941b896844a8272d8516cdda0fcae8daaf56baac18 in /usr/local/bin/ 
# Sat, 31 Jul 2021 13:11:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jul 2021 13:11:35 GMT
USER www-data
# Sat, 31 Jul 2021 13:11:41 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:baf144cfb66ebe9df1969f3b90f1c448beff98edc84de1ccb5d6346195a070d4`  
		Last Modified: Tue, 15 Jun 2021 22:27:38 GMT  
		Size: 2.8 MB (2810478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ccd35cdcd0d2f44750979fa156369560b3d83d0fd6c9b5b6835504233171cbf`  
		Last Modified: Sat, 31 Jul 2021 04:32:59 GMT  
		Size: 1.8 MB (1753665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a0343a7c328a00ea39b214651b5817a2158019d1c2b6acb6ae687007ce40017`  
		Last Modified: Sat, 31 Jul 2021 04:32:58 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13fb577a40a607849a76b566636558cf133d947986988e0a2aac93d0715aece0`  
		Last Modified: Sat, 31 Jul 2021 04:32:58 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f44a0de4437fa4a89522bd9489eb8e15b9359a078a0180dba2a43d49b5182b2d`  
		Last Modified: Sat, 31 Jul 2021 04:34:56 GMT  
		Size: 10.7 MB (10698213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15e31f13a7f0f252428fb6be35be82506d7166fda7fe5996b2b37e8fd93ac951`  
		Last Modified: Sat, 31 Jul 2021 04:34:55 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39da34166be484e78e378ed13123b2b94c3f6a633799f21cdc8bef15126bc3db`  
		Last Modified: Sat, 31 Jul 2021 04:34:58 GMT  
		Size: 15.7 MB (15691426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213d04d309a83bc106b6d318a6bdbef7db5f0dc160d7e6984a8b1c4241e5a96f`  
		Last Modified: Sat, 31 Jul 2021 04:34:54 GMT  
		Size: 2.3 KB (2266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4da81612b547d23e52d570266988858b7c7ede2eff009e779ce37d4c6c0e35d1`  
		Last Modified: Sat, 31 Jul 2021 04:34:55 GMT  
		Size: 17.8 KB (17792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f38458d3189f1fb7dd0034d0d17297b54420e0bdc37fdd8b953c77d13fffe36`  
		Last Modified: Sat, 31 Jul 2021 13:17:48 GMT  
		Size: 9.5 MB (9533140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fd5cd9efbeefd86fcd4bd346b5684c2eeeca4c3d4a4656da1008d80ccd13fda`  
		Last Modified: Sat, 31 Jul 2021 13:17:44 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e5d11ededfe787db999d281dbd257bd2843b211faf2444a5ea36a40ff1b8ac3`  
		Last Modified: Sat, 31 Jul 2021 13:17:45 GMT  
		Size: 4.9 MB (4917289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c17330dcd118516d3e23ab1551ba5a7168c2893d5f8fa907e1983ac168ffc472`  
		Last Modified: Sat, 31 Jul 2021 13:17:44 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc6356d9d0bf4488972a6618572547a31a146636e531be925ad4b4b8c530b8b7`  
		Last Modified: Sat, 31 Jul 2021 13:17:44 GMT  
		Size: 1.3 MB (1315322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83b02fd63437d84e0fc25b1fd4aae35d470f5695c7483b1fd8ea5f4916a91c6f`  
		Last Modified: Sat, 31 Jul 2021 13:17:44 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:cli-php8.0` - linux; s390x

```console
$ docker pull wordpress@sha256:42a7a2016d04c10ebceef3c1cd485138d95126ffaad4880b765086fec7a2876d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45730698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea6142107044c9471389252138662d3b04ba3e3457fc59e4720e5cd5547e127`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["wp","shell"]`

```dockerfile
# Wed, 14 Apr 2021 18:41:35 GMT
ADD file:c715fef757fe2b022ae1bbff71dbc58bddf5a858deb0aac5a6fbcf10d5f3111c in / 
# Wed, 14 Apr 2021 18:41:36 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:00:51 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 14 Apr 2021 19:00:54 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 14 Apr 2021 19:00:56 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 14 Apr 2021 19:00:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 14 Apr 2021 19:00:57 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 14 Apr 2021 19:00:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 14 Apr 2021 19:00:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 14 Apr 2021 19:00:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 14 Apr 2021 19:00:59 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 04 Jun 2021 19:04:59 GMT
ENV PHP_VERSION=8.0.7
# Fri, 04 Jun 2021 19:04:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.7.tar.xz.asc
# Fri, 04 Jun 2021 19:04:59 GMT
ENV PHP_SHA256=d5fc2e4fc780a32404d88c360e3e0009bc725d936459668e9c2ac992f2d83654
# Fri, 04 Jun 2021 19:05:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 04 Jun 2021 19:05:07 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 04 Jun 2021 19:10:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 04 Jun 2021 19:10:36 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Fri, 04 Jun 2021 19:10:39 GMT
RUN docker-php-ext-enable sodium
# Fri, 04 Jun 2021 19:10:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 04 Jun 2021 19:10:40 GMT
CMD ["php" "-a"]
# Sun, 27 Jun 2021 12:52:49 GMT
RUN apk add --no-cache 		bash 		less 		mysql-client
# Sun, 27 Jun 2021 12:52:51 GMT
RUN set -ex; 	mkdir -p /var/www/html; 	chown -R www-data:www-data /var/www/html
# Sun, 27 Jun 2021 12:52:51 GMT
WORKDIR /var/www/html
# Wed, 30 Jun 2021 22:04:20 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		mysqli 		zip 	; 	pecl install imagick-3.5.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps
# Wed, 30 Jun 2021 22:04:23 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Wed, 30 Jun 2021 22:04:23 GMT
ENV WORDPRESS_CLI_GPG_KEY=63AF7AA15067C05616FDDD88A3A2E8F226F0BC06
# Wed, 30 Jun 2021 22:04:24 GMT
ENV WORDPRESS_CLI_VERSION=2.5.0
# Wed, 30 Jun 2021 22:04:25 GMT
ENV WORDPRESS_CLI_SHA512=08dd9035fda1d529807380d5b757839e2809e289eb1a698fe33e7e21a1431d3f77c551c2b2db5adc55083d5075ea4137407994111890f765e790a97e6d9ca7af
# Wed, 30 Jun 2021 22:05:00 GMT
RUN set -ex; 		apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -o /usr/local/bin/wp.gpg -fL "https://github.com/wp-cli/wp-cli/releases/download/v${WORDPRESS_CLI_VERSION}/wp-cli-${WORDPRESS_CLI_VERSION}.phar.gpg"; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$WORDPRESS_CLI_GPG_KEY"; 	gpg --batch --decrypt --output /usr/local/bin/wp /usr/local/bin/wp.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/wp.gpg; unset GNUPGHOME; 		echo "$WORDPRESS_CLI_SHA512 */usr/local/bin/wp" | sha512sum -c -; 	chmod +x /usr/local/bin/wp; 		apk del --no-network .fetch-deps; 		wp --allow-root --version
# Wed, 30 Jun 2021 22:05:01 GMT
VOLUME [/var/www/html]
# Wed, 30 Jun 2021 22:05:02 GMT
COPY file:b6efa5ff0423d61c2df0c8941b896844a8272d8516cdda0fcae8daaf56baac18 in /usr/local/bin/ 
# Wed, 30 Jun 2021 22:05:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Jun 2021 22:05:03 GMT
USER www-data
# Wed, 30 Jun 2021 22:05:04 GMT
CMD ["wp" "shell"]
```

-	Layers:
	-	`sha256:afadee6ad6a38d3172beeeca818219604c782efbe93201ef4d39512f289b05ae`  
		Last Modified: Wed, 14 Apr 2021 18:42:16 GMT  
		Size: 2.6 MB (2602650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d300c94e92b07eb0727117362a4c02c33a3af45a2c84e27e191b18fd64537ff2`  
		Last Modified: Wed, 14 Apr 2021 20:01:05 GMT  
		Size: 1.8 MB (1760701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21c222b785aeace308f4ae843bd963ab89b5e43b40c39e44819a79a97ab65ffd`  
		Last Modified: Wed, 14 Apr 2021 20:01:04 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abdca579f326f21cb64727b7a043ef139e61e18d78e009c7aaa0d00c8787d500`  
		Last Modified: Wed, 14 Apr 2021 20:01:04 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe6e68029a9d4aa3de94bcd1c7351e4d7e3ba199bbaf9266b32c85a95413ba1`  
		Last Modified: Fri, 04 Jun 2021 19:31:01 GMT  
		Size: 10.8 MB (10788566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eea44cf0ed3b67e9363eeba2ea08f57d69eac8f4bf27e04f949a3df344064e4`  
		Last Modified: Fri, 04 Jun 2021 19:31:00 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6caee3485f44f47a6f791419c9a45426bffc883a41a816b98317146bf013fbf`  
		Last Modified: Fri, 04 Jun 2021 19:31:03 GMT  
		Size: 14.2 MB (14233345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c03406abb4d60276c7555e3a655d2173e889fc8bc056e64dbaa70cfbca28dcc`  
		Last Modified: Fri, 04 Jun 2021 19:31:00 GMT  
		Size: 2.3 KB (2266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ec95014943a4afed7accb8e6f39dde96d0ebdf27de094f6657275119c232f7e`  
		Last Modified: Fri, 04 Jun 2021 19:31:00 GMT  
		Size: 17.6 KB (17601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed2cd3b8bd5f69e45aff686c89d9a727a20f84d9ada0188fba40431e215229b4`  
		Last Modified: Sun, 27 Jun 2021 13:05:59 GMT  
		Size: 9.8 MB (9841004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f72f9e99b94608b3c4ba2f857468aea264bd679a4b841542857265ec15112f`  
		Last Modified: Fri, 04 Jun 2021 20:23:26 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:238e6bf95c49a6ae12f6b857c663bb9657b45082f76a8722a12b76a5930a6a3c`  
		Last Modified: Wed, 30 Jun 2021 23:22:34 GMT  
		Size: 5.2 MB (5166720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7079311d00857d5d1c3261b8430e1cb0fb39aaca1c4a32a91703ab43d82b5a90`  
		Last Modified: Wed, 30 Jun 2021 23:22:34 GMT  
		Size: 394.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51fbe357f42e33b985f06eb678c6f0c55a025158ef91a2d154af46d1e9c8fa50`  
		Last Modified: Wed, 30 Jun 2021 23:22:34 GMT  
		Size: 1.3 MB (1314867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce92727ef6997a008548a306f08054fd8df95c0ec33f9796a02c0580c900de47`  
		Last Modified: Wed, 30 Jun 2021 23:22:34 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
