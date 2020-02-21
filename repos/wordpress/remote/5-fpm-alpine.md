## `wordpress:5-fpm-alpine`

```console
$ docker pull wordpress@sha256:8eb3d636548f4aeab67b64f09225f6038d636267e8852c4d4d273a24bb559b14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `wordpress:5-fpm-alpine` - linux; amd64

```console
$ docker pull wordpress@sha256:41554b3622fdd139f1b3329b186f7e49c0fcac72707d464c5ebfacacc3fbcc44
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68261765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:539515b2a0251435778346457a26a5dc42b1addc197e9eccc6783f54cbcca3ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 18 Jan 2020 01:19:37 GMT
ADD file:e69d441d729412d24675dcd33e04580885df99981cec43de8c9b24015313ff8e in / 
# Sat, 18 Jan 2020 01:19:37 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 03:18:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 18 Jan 2020 03:18:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 18 Jan 2020 03:18:29 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 18 Jan 2020 03:18:29 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 18 Jan 2020 03:18:30 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 18 Jan 2020 03:23:43 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Sat, 18 Jan 2020 03:23:44 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:23:44 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:23:44 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 03:40:28 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Thu, 20 Feb 2020 23:45:16 GMT
ENV PHP_VERSION=7.3.15
# Thu, 20 Feb 2020 23:45:16 GMT
ENV PHP_URL=https://www.php.net/get/php-7.3.15.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.3.15.tar.xz.asc/from/this/mirror
# Thu, 20 Feb 2020 23:45:16 GMT
ENV PHP_SHA256=de7ae7cf3d1dbb2824975b26b32991dac2b732886ec22075b8c53b261b018166 PHP_MD5=
# Thu, 20 Feb 2020 23:45:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Feb 2020 23:45:18 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Feb 2020 23:53:30 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 20 Feb 2020 23:53:31 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Thu, 20 Feb 2020 23:53:33 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Feb 2020 23:53:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Feb 2020 23:53:33 GMT
WORKDIR /var/www/html
# Thu, 20 Feb 2020 23:53:35 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 20 Feb 2020 23:53:35 GMT
STOPSIGNAL SIGQUIT
# Thu, 20 Feb 2020 23:53:35 GMT
EXPOSE 9000
# Thu, 20 Feb 2020 23:53:35 GMT
CMD ["php-fpm"]
# Fri, 21 Feb 2020 06:19:22 GMT
RUN apk add --no-cache 		bash 		sed 		ghostscript
# Fri, 21 Feb 2020 06:20:23 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 	; 		docker-php-ext-configure gd --with-freetype-dir=/usr --with-jpeg-dir=/usr --with-png-dir=/usr; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		mysqli 		opcache 		zip 	; 	pecl install imagick-3.4.4; 	docker-php-ext-enable imagick; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del .build-deps
# Fri, 21 Feb 2020 06:20:24 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 21 Feb 2020 06:20:25 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Fri, 21 Feb 2020 06:20:26 GMT
VOLUME [/var/www/html]
# Fri, 21 Feb 2020 06:20:26 GMT
ENV WORDPRESS_VERSION=5.3.2
# Fri, 21 Feb 2020 06:20:26 GMT
ENV WORDPRESS_SHA1=fded476f112dbab14e3b5acddd2bcfa550e7b01b
# Fri, 21 Feb 2020 06:20:35 GMT
RUN set -ex; 	curl -o wordpress.tar.gz -fSL "https://wordpress.org/wordpress-${WORDPRESS_VERSION}.tar.gz"; 	echo "$WORDPRESS_SHA1 *wordpress.tar.gz" | sha1sum -c -; 	tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 	chown -R www-data:www-data /usr/src/wordpress
# Fri, 21 Feb 2020 06:20:35 GMT
COPY file:d93be233af180b81b8838a1d00e9f930eb82172c751ffaafb4732db4a09a7534 in /usr/local/bin/ 
# Fri, 21 Feb 2020 06:20:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 06:20:36 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c9b1b535fdd91a9855fb7f82348177e5f019329a58c53c47272962dd60f71fc9`  
		Last Modified: Fri, 17 Jan 2020 08:04:01 GMT  
		Size: 2.8 MB (2802957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c0a1817becf025301783a94fa11de700972e7d7c117ca7e45d080db0ec1a11`  
		Last Modified: Sat, 18 Jan 2020 04:09:35 GMT  
		Size: 1.4 MB (1354634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdd5b3ea1fc31791c18f464b5b95dd3d9b8ff97aef4b64e0202f3da7f5550e80`  
		Last Modified: Sat, 18 Jan 2020 04:09:35 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db87396003bdeb76e6e367a5ae26be9642a89986dcda71b3491412c579cb6859`  
		Last Modified: Sat, 18 Jan 2020 04:09:35 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f09a455666b3c26ab0e931207aa730d446e80c0a98a10ba411bd9aef2142d6b9`  
		Last Modified: Fri, 21 Feb 2020 02:32:07 GMT  
		Size: 12.1 MB (12131097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4a989a7fc7b60166ec2cb9b1d45bde2be6ec4e3579395718c12d2dbd05a0981`  
		Last Modified: Fri, 21 Feb 2020 02:32:05 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b308a8c0d759c0e45a1b6fa290961911f84a02dd2ac90777b7f43ce69c31fa`  
		Last Modified: Fri, 21 Feb 2020 02:32:09 GMT  
		Size: 14.9 MB (14896617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:352857664b099deb3d47d0aa1763e71736a7af26cd7d5da5087ceea451a9de5c`  
		Last Modified: Fri, 21 Feb 2020 02:32:05 GMT  
		Size: 2.2 KB (2214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299d966decb7882ffdf473f77aa5ca0138a01a72caf0cbab6b9306a30155328e`  
		Last Modified: Fri, 21 Feb 2020 02:32:05 GMT  
		Size: 72.9 KB (72932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f50ac619e43d6d98e0be7867edcfaf2a263e21524e7b8b7fe0b953a04cbe5df2`  
		Last Modified: Fri, 21 Feb 2020 02:32:05 GMT  
		Size: 8.4 KB (8412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:873fc4f1a4c27c638a32d50890235ed73ec0af88a5310399ba51a9a054178abb`  
		Last Modified: Fri, 21 Feb 2020 06:32:47 GMT  
		Size: 19.1 MB (19090965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fafd6abb7192c0739687a89f8d4fb4a47d0c95f8e3677e4d1196224178ee27b`  
		Last Modified: Fri, 21 Feb 2020 06:32:43 GMT  
		Size: 5.7 MB (5666305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ad4bda739337a7bb5d628d67879e43d776083050bb0ec1ec0db96371da3908`  
		Last Modified: Fri, 21 Feb 2020 06:32:42 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c097824c239a4aafc809b165d9baa5672fc08f9ffaa3f836c31cfc15c3404e7`  
		Last Modified: Fri, 21 Feb 2020 06:32:42 GMT  
		Size: 392.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea161221dfb685c9e94f3510b694f96e040592b037507240f6a8984852ebdac2`  
		Last Modified: Fri, 21 Feb 2020 06:32:46 GMT  
		Size: 12.2 MB (12229081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:777f8bfaf95d16f06f58e1ce5763190f25ec7b0312b853f84fa572529a723136`  
		Last Modified: Fri, 21 Feb 2020 06:32:42 GMT  
		Size: 3.9 KB (3885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:5-fpm-alpine` - linux; arm variant v6

```console
$ docker pull wordpress@sha256:2bc01077730d9e2b745c9646882911252c3821c2b3629c98842d2c477dc1ba40
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66357355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5451ac5f2615c25ae10699395001a9f10f2cf0b775ade2a500a3e331827a799`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 03:40:01 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 18 Jan 2020 03:40:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 18 Jan 2020 03:40:06 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 18 Jan 2020 03:40:07 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 18 Jan 2020 03:40:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 18 Jan 2020 03:44:51 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Sat, 18 Jan 2020 03:44:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:44:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:44:52 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 03:59:33 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Thu, 20 Feb 2020 22:20:08 GMT
ENV PHP_VERSION=7.3.15
# Thu, 20 Feb 2020 22:20:09 GMT
ENV PHP_URL=https://www.php.net/get/php-7.3.15.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.3.15.tar.xz.asc/from/this/mirror
# Thu, 20 Feb 2020 22:20:09 GMT
ENV PHP_SHA256=de7ae7cf3d1dbb2824975b26b32991dac2b732886ec22075b8c53b261b018166 PHP_MD5=
# Thu, 20 Feb 2020 22:20:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Feb 2020 22:20:15 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Feb 2020 22:24:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 20 Feb 2020 22:24:51 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Thu, 20 Feb 2020 22:24:56 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Feb 2020 22:24:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Feb 2020 22:25:00 GMT
WORKDIR /var/www/html
# Thu, 20 Feb 2020 22:25:04 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 20 Feb 2020 22:25:06 GMT
STOPSIGNAL SIGQUIT
# Thu, 20 Feb 2020 22:25:08 GMT
EXPOSE 9000
# Thu, 20 Feb 2020 22:25:10 GMT
CMD ["php-fpm"]
# Fri, 21 Feb 2020 00:20:10 GMT
RUN apk add --no-cache 		bash 		sed 		ghostscript
# Fri, 21 Feb 2020 00:22:02 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 	; 		docker-php-ext-configure gd --with-freetype-dir=/usr --with-jpeg-dir=/usr --with-png-dir=/usr; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		mysqli 		opcache 		zip 	; 	pecl install imagick-3.4.4; 	docker-php-ext-enable imagick; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del .build-deps
# Fri, 21 Feb 2020 00:22:04 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 21 Feb 2020 00:22:07 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Fri, 21 Feb 2020 00:22:09 GMT
VOLUME [/var/www/html]
# Fri, 21 Feb 2020 00:22:10 GMT
ENV WORDPRESS_VERSION=5.3.2
# Fri, 21 Feb 2020 00:22:11 GMT
ENV WORDPRESS_SHA1=fded476f112dbab14e3b5acddd2bcfa550e7b01b
# Fri, 21 Feb 2020 00:22:18 GMT
RUN set -ex; 	curl -o wordpress.tar.gz -fSL "https://wordpress.org/wordpress-${WORDPRESS_VERSION}.tar.gz"; 	echo "$WORDPRESS_SHA1 *wordpress.tar.gz" | sha1sum -c -; 	tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 	chown -R www-data:www-data /usr/src/wordpress
# Fri, 21 Feb 2020 00:22:19 GMT
COPY file:d93be233af180b81b8838a1d00e9f930eb82172c751ffaafb4732db4a09a7534 in /usr/local/bin/ 
# Fri, 21 Feb 2020 00:22:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 00:22:23 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:832e07764099264ef96e50a1e5e41c52d6b0809bd054e29508a6878aa59d156d`  
		Last Modified: Sat, 18 Jan 2020 01:53:52 GMT  
		Size: 2.6 MB (2617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5c701ead53742b2a88bf4f606bd05029ec59ccaf522450bfa76be8cea0cf02`  
		Last Modified: Sat, 18 Jan 2020 04:28:12 GMT  
		Size: 1.3 MB (1321088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574e3d03f7d4228e33415f8592e7ec2a89fe1616e0ab6366ea68045b09d7f280`  
		Last Modified: Sat, 18 Jan 2020 04:28:12 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba27e9ff828195f46a3edb0b1e28b5d10451b66ae080c20794f6d005cffbd72`  
		Last Modified: Sat, 18 Jan 2020 04:28:12 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c23a96e956023ced83a3f796675125db445eade3ea7621f6a3d13f137efe9f28`  
		Last Modified: Thu, 20 Feb 2020 23:12:40 GMT  
		Size: 12.1 MB (12131108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5663ca020a97b2d2d06d8291ee246abbf23791351d8146f5c518191fd0ffe55d`  
		Last Modified: Thu, 20 Feb 2020 23:12:37 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c6ac77c5c8afbdeba5a513926d692a90d63046a286dbba26bd698adc8ff52f`  
		Last Modified: Thu, 20 Feb 2020 23:12:42 GMT  
		Size: 13.9 MB (13858010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:127182063f68832cf5b9feec11be3c125e878bd1ee57b2c69f3a0cde2ba35afa`  
		Last Modified: Thu, 20 Feb 2020 23:12:37 GMT  
		Size: 2.2 KB (2217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fa10da3dde2cd4fcd20afcbcaa07667a2ce10eb4365233c9cda1d4b2f4a5a6`  
		Last Modified: Thu, 20 Feb 2020 23:12:37 GMT  
		Size: 72.5 KB (72462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c2d5e10b12fa0fe56667770e5f7b0b85d632af0adb8600397adbe63ef832d04`  
		Last Modified: Thu, 20 Feb 2020 23:12:37 GMT  
		Size: 8.4 KB (8412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c600c108585102b1420603bcb5596caaf948a20faa955c2b9ca22b2ba9935941`  
		Last Modified: Fri, 21 Feb 2020 00:31:32 GMT  
		Size: 18.6 MB (18597488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d8619ff0b069ec2558a3e7aa5336b3b1c25b462c84184f7949d12b73713edb`  
		Last Modified: Fri, 21 Feb 2020 00:31:25 GMT  
		Size: 5.5 MB (5513257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d921f6e199eadd083092e24c12ca30916fff6fdf7ed1b84bd484bb937bf8a727`  
		Last Modified: Fri, 21 Feb 2020 00:31:24 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e019c133da290ac60176e9a2289a1c6371bb94ab87ee3f45b19b341b0fb24c1`  
		Last Modified: Fri, 21 Feb 2020 00:31:24 GMT  
		Size: 391.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf65da4576cd16c938599b707710e3480f975ae8ac76b9a6d955eec9b31bff4`  
		Last Modified: Fri, 21 Feb 2020 00:31:30 GMT  
		Size: 12.2 MB (12229119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58816793a681a906977b3ec17ca1bec2b27ee00ac682185849dd1230368e474a`  
		Last Modified: Fri, 21 Feb 2020 00:31:24 GMT  
		Size: 3.9 KB (3892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:5-fpm-alpine` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:44832365eada44727d5a98fc6a620142126fb240ecd0a7b5b329663638d3e519
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64161651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4629dba30dc5be43395495d792cbe15a70a2fec4d70d5c0c1616b0cf3a936424`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 18 Jan 2020 02:03:19 GMT
ADD file:4c815f4461ff3b8d481f43d84eb2548cb1adbb3015d370cab86dd7f4d3d94279 in / 
# Sat, 18 Jan 2020 02:03:22 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 05:21:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 18 Jan 2020 05:22:08 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 18 Jan 2020 05:22:16 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 18 Jan 2020 05:22:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 18 Jan 2020 05:22:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 18 Jan 2020 05:27:57 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Sat, 18 Jan 2020 05:27:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 05:27:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 05:28:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 05:42:08 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Thu, 20 Feb 2020 22:03:28 GMT
ENV PHP_VERSION=7.3.15
# Thu, 20 Feb 2020 22:03:29 GMT
ENV PHP_URL=https://www.php.net/get/php-7.3.15.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.3.15.tar.xz.asc/from/this/mirror
# Thu, 20 Feb 2020 22:03:30 GMT
ENV PHP_SHA256=de7ae7cf3d1dbb2824975b26b32991dac2b732886ec22075b8c53b261b018166 PHP_MD5=
# Thu, 20 Feb 2020 22:03:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Feb 2020 22:03:39 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Feb 2020 22:06:44 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 20 Feb 2020 22:06:45 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Thu, 20 Feb 2020 22:06:48 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Feb 2020 22:06:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Feb 2020 22:06:50 GMT
WORKDIR /var/www/html
# Thu, 20 Feb 2020 22:06:53 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 20 Feb 2020 22:06:54 GMT
STOPSIGNAL SIGQUIT
# Thu, 20 Feb 2020 22:06:55 GMT
EXPOSE 9000
# Thu, 20 Feb 2020 22:06:56 GMT
CMD ["php-fpm"]
# Fri, 21 Feb 2020 02:13:01 GMT
RUN apk add --no-cache 		bash 		sed 		ghostscript
# Fri, 21 Feb 2020 02:14:27 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 	; 		docker-php-ext-configure gd --with-freetype-dir=/usr --with-jpeg-dir=/usr --with-png-dir=/usr; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		mysqli 		opcache 		zip 	; 	pecl install imagick-3.4.4; 	docker-php-ext-enable imagick; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del .build-deps
# Fri, 21 Feb 2020 02:14:29 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 21 Feb 2020 02:14:31 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Fri, 21 Feb 2020 02:14:33 GMT
VOLUME [/var/www/html]
# Fri, 21 Feb 2020 02:14:35 GMT
ENV WORDPRESS_VERSION=5.3.2
# Fri, 21 Feb 2020 02:14:36 GMT
ENV WORDPRESS_SHA1=fded476f112dbab14e3b5acddd2bcfa550e7b01b
# Fri, 21 Feb 2020 02:14:43 GMT
RUN set -ex; 	curl -o wordpress.tar.gz -fSL "https://wordpress.org/wordpress-${WORDPRESS_VERSION}.tar.gz"; 	echo "$WORDPRESS_SHA1 *wordpress.tar.gz" | sha1sum -c -; 	tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 	chown -R www-data:www-data /usr/src/wordpress
# Fri, 21 Feb 2020 02:14:44 GMT
COPY file:d93be233af180b81b8838a1d00e9f930eb82172c751ffaafb4732db4a09a7534 in /usr/local/bin/ 
# Fri, 21 Feb 2020 02:14:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 02:14:47 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:3a2c5e3c37b2e3d749405512ef3793aa45a2f5c11615d9e9efa80179262cdf27`  
		Last Modified: Sat, 18 Jan 2020 02:04:05 GMT  
		Size: 2.4 MB (2419554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eecb809efefba021b07183ae486164fd475667a42a78ab308bd01b8d7dd8c1e`  
		Last Modified: Sat, 18 Jan 2020 06:09:11 GMT  
		Size: 1.2 MB (1227271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6ec95513b0eab50a07131cbee828abed358fb86fd276018e1bae6f04611ed9`  
		Last Modified: Sat, 18 Jan 2020 06:09:10 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459d1b57d2f034e68934a4116a4434479186cfce56d1235af4f1c1b9de08acbc`  
		Last Modified: Sat, 18 Jan 2020 06:09:08 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a6ed8dd1052db22f0cf220ee392d0f3f53cd969016bfd90eadc3526fd76d53e`  
		Last Modified: Thu, 20 Feb 2020 23:30:57 GMT  
		Size: 12.1 MB (12131105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c19611b2b3de5ccb934fc6a955b7105828125e7d8d0dc33dfb7fe17f46cb9f`  
		Last Modified: Thu, 20 Feb 2020 23:30:53 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c8e083c7ce85a337ba66d7990d23e2bff53f3fa68940d74ee91ef67abe7d12`  
		Last Modified: Thu, 20 Feb 2020 23:31:00 GMT  
		Size: 13.0 MB (12994261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:017b0306b8f0a94412c6e12bd9d247ebb4f215ce0d1bb178752dd8742d64ee48`  
		Last Modified: Thu, 20 Feb 2020 23:30:53 GMT  
		Size: 2.2 KB (2217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269c09f304bbcfc70e4b448502d0529691a4fd8902b391c4a28b5034dbdc7e1e`  
		Last Modified: Thu, 20 Feb 2020 23:30:53 GMT  
		Size: 72.5 KB (72457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a6b89df3127fafca98abccee0d430386692d34e2bb6470860f45358f24c8da6`  
		Last Modified: Thu, 20 Feb 2020 23:30:53 GMT  
		Size: 8.4 KB (8414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcdd92dcabaea5e64c10348c5c4f7264ab5745605936925c576917d3f27e72a5`  
		Last Modified: Fri, 21 Feb 2020 02:35:27 GMT  
		Size: 17.8 MB (17779155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:926127bcc930bf07a658b6bec6a927dfdac8ba514adf3adf7ab55cb3dddf19c5`  
		Last Modified: Fri, 21 Feb 2020 02:35:18 GMT  
		Size: 5.3 MB (5291481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8787eb2df5a82d2053445f46be72f3ab7d3360a6dc31380601839e389cc0496a`  
		Last Modified: Fri, 21 Feb 2020 02:35:18 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deb632ab45246ad5c47708d0310403133fc49f1528931ccf78694a45e4df63c7`  
		Last Modified: Fri, 21 Feb 2020 02:35:18 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ea3cfb4c5c04b7275ff6ba27b47a1cb8345a5735e8436e767102968de00cfa`  
		Last Modified: Fri, 21 Feb 2020 02:35:23 GMT  
		Size: 12.2 MB (12229108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a83e731a288ec14f36c981b41c90e39370f077b8c894f1150f37f4664610719`  
		Last Modified: Fri, 21 Feb 2020 02:35:18 GMT  
		Size: 3.9 KB (3889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:5-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:709fdf529e235610434c384da505460483fb5438ddf18d0f0c82264dc65bb080
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67824983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca206657718dec27dae4114c51eec568d8ef997537cb6703c96faede8518dc5a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 18 Jan 2020 01:39:43 GMT
ADD file:4109fa86dd80850e84c689ff9e6a3243e30ab1bbcc00c765969b3011bfbb43e1 in / 
# Sat, 18 Jan 2020 01:39:43 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 02:29:01 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 18 Jan 2020 02:29:08 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 18 Jan 2020 02:29:16 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 18 Jan 2020 02:29:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 18 Jan 2020 02:29:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 18 Jan 2020 02:36:02 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Sat, 18 Jan 2020 02:36:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 02:36:08 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 02:36:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 02:54:19 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Thu, 20 Feb 2020 23:08:12 GMT
ENV PHP_VERSION=7.3.15
# Thu, 20 Feb 2020 23:08:13 GMT
ENV PHP_URL=https://www.php.net/get/php-7.3.15.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.3.15.tar.xz.asc/from/this/mirror
# Thu, 20 Feb 2020 23:08:14 GMT
ENV PHP_SHA256=de7ae7cf3d1dbb2824975b26b32991dac2b732886ec22075b8c53b261b018166 PHP_MD5=
# Thu, 20 Feb 2020 23:08:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Feb 2020 23:08:19 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Feb 2020 23:11:19 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 20 Feb 2020 23:11:21 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Thu, 20 Feb 2020 23:11:29 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Feb 2020 23:11:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Feb 2020 23:11:31 GMT
WORKDIR /var/www/html
# Thu, 20 Feb 2020 23:11:33 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 20 Feb 2020 23:11:34 GMT
STOPSIGNAL SIGQUIT
# Thu, 20 Feb 2020 23:11:35 GMT
EXPOSE 9000
# Thu, 20 Feb 2020 23:11:36 GMT
CMD ["php-fpm"]
# Fri, 21 Feb 2020 07:10:54 GMT
RUN apk add --no-cache 		bash 		sed 		ghostscript
# Fri, 21 Feb 2020 07:12:33 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 	; 		docker-php-ext-configure gd --with-freetype-dir=/usr --with-jpeg-dir=/usr --with-png-dir=/usr; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		mysqli 		opcache 		zip 	; 	pecl install imagick-3.4.4; 	docker-php-ext-enable imagick; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del .build-deps
# Fri, 21 Feb 2020 07:12:35 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 21 Feb 2020 07:12:38 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Fri, 21 Feb 2020 07:12:38 GMT
VOLUME [/var/www/html]
# Fri, 21 Feb 2020 07:12:39 GMT
ENV WORDPRESS_VERSION=5.3.2
# Fri, 21 Feb 2020 07:12:40 GMT
ENV WORDPRESS_SHA1=fded476f112dbab14e3b5acddd2bcfa550e7b01b
# Fri, 21 Feb 2020 07:12:44 GMT
RUN set -ex; 	curl -o wordpress.tar.gz -fSL "https://wordpress.org/wordpress-${WORDPRESS_VERSION}.tar.gz"; 	echo "$WORDPRESS_SHA1 *wordpress.tar.gz" | sha1sum -c -; 	tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 	chown -R www-data:www-data /usr/src/wordpress
# Fri, 21 Feb 2020 07:12:45 GMT
COPY file:d93be233af180b81b8838a1d00e9f930eb82172c751ffaafb4732db4a09a7534 in /usr/local/bin/ 
# Fri, 21 Feb 2020 07:12:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 07:12:47 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:8fa90b21c985a6fcfff966bdfbde81cdd088de0aa8af38110057f6ac408f4408`  
		Last Modified: Sat, 18 Jan 2020 01:40:23 GMT  
		Size: 2.7 MB (2723075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34df684e328567a0a35db6301bcecffeb8c2ab6a69340a96db5d3e73a9fde3da`  
		Last Modified: Sat, 18 Jan 2020 03:18:17 GMT  
		Size: 1.4 MB (1359426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dbaaf99effdf014f4ce62ee67d7cf9f23205c645f22d554e6e925ef12ffcd70`  
		Last Modified: Sat, 18 Jan 2020 03:18:17 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99838bf36837f5d2206ac07b2f399dca053921c575c4e9ea8fce917f1672383a`  
		Last Modified: Sat, 18 Jan 2020 03:18:17 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe42459fbf4ba4f04bea958d5cc208e4dd06e92e258c0c1cbc3c1106f6912c4`  
		Last Modified: Fri, 21 Feb 2020 00:34:43 GMT  
		Size: 12.1 MB (12131110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0829431429340e1d95d09e9622b7b13c640f23e298cebe77a7e40983b847fe5c`  
		Last Modified: Fri, 21 Feb 2020 00:34:39 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c24ba5208fc7afd53aefa6304ce3e4d1e82fc85a650afcd0cf6badd75bf9a334`  
		Last Modified: Fri, 21 Feb 2020 00:34:43 GMT  
		Size: 14.6 MB (14626170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:316f3cb9e504616d1e23162623814c9bc53cd7da2b9064cc3f8a5b4af88e5561`  
		Last Modified: Fri, 21 Feb 2020 00:34:39 GMT  
		Size: 2.2 KB (2217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57b080675e2198e1530acb31c244285bde9370b9c9e7741711866b7af68147e9`  
		Last Modified: Fri, 21 Feb 2020 00:34:39 GMT  
		Size: 72.5 KB (72458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b82a92b0687bd2c7bac4eae94001e8a260c479391467b120be0b32972d66b5ab`  
		Last Modified: Fri, 21 Feb 2020 00:34:39 GMT  
		Size: 8.4 KB (8413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3420d927c24e098bbe8b63cf545947df47408df80c7463cc6724971f5d2ee897`  
		Last Modified: Fri, 21 Feb 2020 07:30:19 GMT  
		Size: 19.2 MB (19170588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60c7652d91876b88d97507974c722e616bdc2f6ef6a11ab1b6087fc8e5cf7c5c`  
		Last Modified: Fri, 21 Feb 2020 07:30:13 GMT  
		Size: 5.5 MB (5495777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5be135dc5653f49baa39ca8d4173be92082a5ead12857d6827478a42d0f7b0`  
		Last Modified: Fri, 21 Feb 2020 07:30:14 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dc895c85a3b1dbe5fbfa0a93ecef64476511132bc505bc5bd255fa38f62c02c`  
		Last Modified: Fri, 21 Feb 2020 07:30:11 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c6ede6dae8de92948528024db4b23663c6f6056a93f4bf6d2a9695dde4e450`  
		Last Modified: Fri, 21 Feb 2020 07:30:16 GMT  
		Size: 12.2 MB (12229116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9701124231677ef2d69e9e3d1894b45b7ae8e6d5fcffbcf010119515792af62c`  
		Last Modified: Fri, 21 Feb 2020 07:30:12 GMT  
		Size: 3.9 KB (3890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:5-fpm-alpine` - linux; 386

```console
$ docker pull wordpress@sha256:f98ea7b0553d3b2a557103e93afddc5258c454ffe1eba408e7f1dccbe2113950
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69288483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38548e22d3f1cc07b3b9ad406c9acb4c0040c72363234b2bac37f84f006b3e69`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 18 Jan 2020 01:38:44 GMT
ADD file:381b617b92fe699ad4ef4f30e0d9599f89e43e252883348c420ebe2a0cccbd63 in / 
# Sat, 18 Jan 2020 01:38:45 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 05:41:35 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 18 Jan 2020 05:41:36 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 18 Jan 2020 05:41:37 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 18 Jan 2020 05:41:37 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 18 Jan 2020 05:41:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 18 Jan 2020 05:48:39 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Sat, 18 Jan 2020 05:48:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 05:48:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 05:48:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 06:11:29 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Fri, 21 Feb 2020 00:31:54 GMT
ENV PHP_VERSION=7.3.15
# Fri, 21 Feb 2020 00:31:54 GMT
ENV PHP_URL=https://www.php.net/get/php-7.3.15.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.3.15.tar.xz.asc/from/this/mirror
# Fri, 21 Feb 2020 00:31:54 GMT
ENV PHP_SHA256=de7ae7cf3d1dbb2824975b26b32991dac2b732886ec22075b8c53b261b018166 PHP_MD5=
# Fri, 21 Feb 2020 00:31:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 21 Feb 2020 00:31:59 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 21 Feb 2020 00:41:37 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 21 Feb 2020 00:41:38 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Fri, 21 Feb 2020 00:41:40 GMT
RUN docker-php-ext-enable sodium
# Fri, 21 Feb 2020 00:41:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 21 Feb 2020 00:41:41 GMT
WORKDIR /var/www/html
# Fri, 21 Feb 2020 00:41:42 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 21 Feb 2020 00:41:42 GMT
STOPSIGNAL SIGQUIT
# Fri, 21 Feb 2020 00:41:42 GMT
EXPOSE 9000
# Fri, 21 Feb 2020 00:41:43 GMT
CMD ["php-fpm"]
# Fri, 21 Feb 2020 06:41:42 GMT
RUN apk add --no-cache 		bash 		sed 		ghostscript
# Fri, 21 Feb 2020 06:42:51 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 	; 		docker-php-ext-configure gd --with-freetype-dir=/usr --with-jpeg-dir=/usr --with-png-dir=/usr; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		mysqli 		opcache 		zip 	; 	pecl install imagick-3.4.4; 	docker-php-ext-enable imagick; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del .build-deps
# Fri, 21 Feb 2020 06:42:52 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 21 Feb 2020 06:42:52 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Fri, 21 Feb 2020 06:42:53 GMT
VOLUME [/var/www/html]
# Fri, 21 Feb 2020 06:42:53 GMT
ENV WORDPRESS_VERSION=5.3.2
# Fri, 21 Feb 2020 06:42:53 GMT
ENV WORDPRESS_SHA1=fded476f112dbab14e3b5acddd2bcfa550e7b01b
# Fri, 21 Feb 2020 06:43:02 GMT
RUN set -ex; 	curl -o wordpress.tar.gz -fSL "https://wordpress.org/wordpress-${WORDPRESS_VERSION}.tar.gz"; 	echo "$WORDPRESS_SHA1 *wordpress.tar.gz" | sha1sum -c -; 	tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 	chown -R www-data:www-data /usr/src/wordpress
# Fri, 21 Feb 2020 06:43:02 GMT
COPY file:d93be233af180b81b8838a1d00e9f930eb82172c751ffaafb4732db4a09a7534 in /usr/local/bin/ 
# Fri, 21 Feb 2020 06:43:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 06:43:03 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:f024b1263dc58db07a458b73ae1a2dca02ca55bef1ccd1fa3fd50656551fadf2`  
		Last Modified: Sat, 18 Jan 2020 01:39:18 GMT  
		Size: 2.8 MB (2806560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6686b8c2d7ff02237fc9b12daa86e7e7328b7031b6585a20cd6b5fd618f77486`  
		Last Modified: Sat, 18 Jan 2020 06:45:55 GMT  
		Size: 1.5 MB (1452582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564ce419d6f56887ea2bd9699c37517ecd579e747f1a2698e764ad6f74e66b4c`  
		Last Modified: Sat, 18 Jan 2020 06:45:54 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:694ef48cddae433ef86445fc9786eb75673c1c0c6d903fd7a81b2c56fb7e1b86`  
		Last Modified: Sat, 18 Jan 2020 06:45:54 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d2d7fee60a1c9ff3c32b3b67a3f3f27bdca4bf4a3cada836dff262bdf1da83f`  
		Last Modified: Fri, 21 Feb 2020 03:15:47 GMT  
		Size: 12.1 MB (12131095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83108c2711cfcfad407731f1f7ac043d4b7119eaa87d868490c9bd7930d65420`  
		Last Modified: Fri, 21 Feb 2020 03:15:44 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01beb19e7fa9c02e836357da9e8a8047156677f254de4aa1875a3c98b2742883`  
		Last Modified: Fri, 21 Feb 2020 03:15:51 GMT  
		Size: 15.3 MB (15274794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea412c14b93ce6ad094def7c7438dbd9be40f14b9a0e39de8d88115ea1e96a0`  
		Last Modified: Fri, 21 Feb 2020 03:15:44 GMT  
		Size: 2.2 KB (2216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5296540c4f817d73d0c5203b02a14f39cd4680d970b3ab4a7f365e5ec5233e35`  
		Last Modified: Fri, 21 Feb 2020 03:15:44 GMT  
		Size: 72.1 KB (72119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:511694cd29bf6bc77e3e26b8f50c75999e84c0da1c76d8416035fdd3beb5f004`  
		Last Modified: Fri, 21 Feb 2020 03:15:44 GMT  
		Size: 8.4 KB (8409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95331aa4200805ee5127c27e2836cfaba07f4e318631cc75c0de1bd0d5fb4e6b`  
		Last Modified: Fri, 21 Feb 2020 06:54:28 GMT  
		Size: 19.6 MB (19578782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f5e00dcf2e750b0ec373d4adaf6310716c0f8061f335c9747490f993d2468b`  
		Last Modified: Fri, 21 Feb 2020 06:54:23 GMT  
		Size: 5.7 MB (5726326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f49baf825a861e1092911fdc834bd0af05946c4d9cd26f7774606d18bc36c1e`  
		Last Modified: Fri, 21 Feb 2020 06:54:21 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45229447ae04d757ea2a7c00a1e2e28dabe33300a147eb079a943610fa7c3e19`  
		Last Modified: Fri, 21 Feb 2020 06:54:21 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f11fbf46bde1861735dfafa7e80bfb975646a6311c6b43624530e23680b81e22`  
		Last Modified: Fri, 21 Feb 2020 06:54:30 GMT  
		Size: 12.2 MB (12229049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba48e2940d5c28520d5b34f40b5cbd1558b3ce0f5baef2d3801f94bb5b7fb5f`  
		Last Modified: Fri, 21 Feb 2020 06:54:21 GMT  
		Size: 3.9 KB (3889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:5-fpm-alpine` - linux; ppc64le

```console
$ docker pull wordpress@sha256:848595e8d5cf1fdf2378f44e987f526084df3e42486d9370926212f0a153bba9
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69884028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb29bb67a20c174973418ef2031b0782f7a67e2a69fe6e436840e6ecd9c9ed83`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 18 Jan 2020 02:20:41 GMT
ADD file:32ddb3d5255071cca51573ceee2464dd5a87c8d1cce514ae965b6e824d9ef24b in / 
# Sat, 18 Jan 2020 02:20:45 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 03:24:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 18 Jan 2020 03:24:16 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 18 Jan 2020 03:24:20 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 18 Jan 2020 03:24:23 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 18 Jan 2020 03:24:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 18 Jan 2020 03:29:11 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Sat, 18 Jan 2020 03:29:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:29:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:29:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 03:44:39 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Fri, 24 Jan 2020 00:47:31 GMT
ENV PHP_VERSION=7.3.14
# Fri, 24 Jan 2020 00:47:33 GMT
ENV PHP_URL=https://www.php.net/get/php-7.3.14.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.3.14.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 00:47:35 GMT
ENV PHP_SHA256=cc05dd373ca5d36652800762f65c10e828a17de35aaf246262e3efa99d00cdb0 PHP_MD5=
# Fri, 24 Jan 2020 00:47:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 24 Jan 2020 00:47:46 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 00:52:20 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 00:52:22 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Fri, 24 Jan 2020 00:52:28 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 00:52:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 00:52:40 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 00:52:49 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 24 Jan 2020 00:52:51 GMT
STOPSIGNAL SIGQUIT
# Fri, 24 Jan 2020 00:52:53 GMT
EXPOSE 9000
# Fri, 24 Jan 2020 00:52:55 GMT
CMD ["php-fpm"]
# Fri, 24 Jan 2020 10:18:41 GMT
RUN apk add --no-cache 		bash 		sed 		ghostscript
# Fri, 24 Jan 2020 10:19:57 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 	; 		docker-php-ext-configure gd --with-freetype-dir=/usr --with-jpeg-dir=/usr --with-png-dir=/usr; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		mysqli 		opcache 		zip 	; 	pecl install imagick-3.4.4; 	docker-php-ext-enable imagick; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del .build-deps
# Fri, 24 Jan 2020 10:20:04 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 10:20:13 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Fri, 24 Jan 2020 10:20:17 GMT
VOLUME [/var/www/html]
# Fri, 24 Jan 2020 10:20:21 GMT
ENV WORDPRESS_VERSION=5.3.2
# Fri, 24 Jan 2020 10:20:26 GMT
ENV WORDPRESS_SHA1=fded476f112dbab14e3b5acddd2bcfa550e7b01b
# Fri, 24 Jan 2020 10:20:38 GMT
RUN set -ex; 	curl -o wordpress.tar.gz -fSL "https://wordpress.org/wordpress-${WORDPRESS_VERSION}.tar.gz"; 	echo "$WORDPRESS_SHA1 *wordpress.tar.gz" | sha1sum -c -; 	tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 	chown -R www-data:www-data /usr/src/wordpress
# Fri, 24 Jan 2020 10:20:42 GMT
COPY file:d93be233af180b81b8838a1d00e9f930eb82172c751ffaafb4732db4a09a7534 in /usr/local/bin/ 
# Fri, 24 Jan 2020 10:20:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jan 2020 10:20:52 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:cd95c8a93e39dcaa0634a65d5b86a88bcd5c3092adb1f96504a7030faa165123`  
		Last Modified: Sat, 18 Jan 2020 02:21:25 GMT  
		Size: 2.8 MB (2822125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eccdcd97be351ef8da754f6efea3745b7060b1fe92ab96e4b8f5ff85b6322da9`  
		Last Modified: Sat, 18 Jan 2020 04:12:49 GMT  
		Size: 1.4 MB (1397881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea78a138902aeee431e9b31b236dfea5d4f95a1e155aada946ca57f6650a4da9`  
		Last Modified: Sat, 18 Jan 2020 04:12:49 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda899b5dd7be53564e6266c17b869d98468c50bc887279c51acacfa831de39f`  
		Last Modified: Sat, 18 Jan 2020 04:12:49 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb70b2ce9dbb81b4f41a5ea36fe738576c48128f67e05dfe94feb5970488d88`  
		Last Modified: Fri, 24 Jan 2020 02:41:27 GMT  
		Size: 12.1 MB (12125789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1ded5ff4436bcd6a618c8ecf6704e54a876c3cee438ec0b2f1bf41a51da7504`  
		Last Modified: Fri, 24 Jan 2020 02:41:22 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9140a0636b6ea7f462e8c6504bc375f49a5096916fc57ff033dc20b71bbe7247`  
		Last Modified: Fri, 24 Jan 2020 02:41:31 GMT  
		Size: 15.9 MB (15911329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:713ae1f742527e53b7d49b7ea29ff29bbded891b696ce76ab7bf232f0454a089`  
		Last Modified: Fri, 24 Jan 2020 02:41:22 GMT  
		Size: 2.2 KB (2217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5a28071c0f8c5ce971db829e7663dffff3e4ac61eb1e435381537fcf66c6ecd`  
		Last Modified: Fri, 24 Jan 2020 02:41:22 GMT  
		Size: 72.8 KB (72782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caeec23346e6481edbadde198f67a6a206bfcce5c513bd56079eceeaf1937091`  
		Last Modified: Fri, 24 Jan 2020 02:41:22 GMT  
		Size: 8.4 KB (8413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b7621b1067ab8076371160d56dee00e76451074f041ab179a0679fb102b0876`  
		Last Modified: Fri, 24 Jan 2020 10:49:27 GMT  
		Size: 19.6 MB (19637440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a986ad6f5bef427157738bf779e12b60daf63b848a83cc62f5fdf366838252e8`  
		Last Modified: Fri, 24 Jan 2020 10:49:20 GMT  
		Size: 5.7 MB (5670302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81a895794e900e97f4cad2ef35b57bcdea6b2aaa7a39e8d4baeecde782385f1`  
		Last Modified: Fri, 24 Jan 2020 10:49:19 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e9f798d812904daa6cbcb29131d2da36d6e63ba97841ad036365288ea478a72`  
		Last Modified: Fri, 24 Jan 2020 10:49:19 GMT  
		Size: 394.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf86a5b1fe1eded2dd0a1619b68fe19d6a9f658e4786eaf25b5dcc9adf9152c1`  
		Last Modified: Fri, 24 Jan 2020 10:49:26 GMT  
		Size: 12.2 MB (12229113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2f20b9695a08b26722ceab971a8af94ef2a499f9532123cefc5d983665c5ad`  
		Last Modified: Fri, 24 Jan 2020 10:49:20 GMT  
		Size: 3.9 KB (3894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
