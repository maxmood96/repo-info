## `drupal:9-fpm-alpine3.12`

```console
$ docker pull drupal@sha256:e6ee5041c1dc54d27baaf392478bac14ece0b88588295b4eb2647ebec55eb71f
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

### `drupal:9-fpm-alpine3.12` - linux; amd64

```console
$ docker pull drupal@sha256:ce69bf98687612bd4d6f96c235da1aac0a81b58a6856822d63ebc2e0e5926c35
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52503701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9be54bb9f610ede8a09e82771317b19c4531af7158501f38a73db52c81226c55`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Sat, 06 Mar 2021 03:41:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 06 Mar 2021 03:41:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 06 Mar 2021 03:41:29 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 06 Mar 2021 03:41:30 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 06 Mar 2021 03:41:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 06 Mar 2021 03:49:38 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Sat, 06 Mar 2021 03:49:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 06 Mar 2021 03:49:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 06 Mar 2021 03:49:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 06 Mar 2021 03:49:40 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Sat, 06 Mar 2021 03:49:40 GMT
ENV PHP_VERSION=8.0.3
# Sat, 06 Mar 2021 03:49:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.3.tar.xz.asc
# Sat, 06 Mar 2021 03:49:41 GMT
ENV PHP_SHA256=c9816aa9745a9695672951eaff3a35ca5eddcb9cacf87a4f04b9fb1169010251
# Sat, 06 Mar 2021 03:49:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 06 Mar 2021 03:49:48 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 06 Mar 2021 03:56:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 06 Mar 2021 03:56:49 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Sat, 06 Mar 2021 03:56:50 GMT
RUN docker-php-ext-enable sodium
# Sat, 06 Mar 2021 03:56:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 06 Mar 2021 03:56:51 GMT
WORKDIR /var/www/html
# Sat, 06 Mar 2021 03:56:52 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Sat, 06 Mar 2021 03:56:52 GMT
STOPSIGNAL SIGQUIT
# Sat, 06 Mar 2021 03:56:53 GMT
EXPOSE 9000
# Sat, 06 Mar 2021 03:56:53 GMT
CMD ["php-fpm"]
# Sat, 06 Mar 2021 06:55:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps
# Sat, 06 Mar 2021 06:55:07 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Sat, 06 Mar 2021 06:55:07 GMT
COPY file:deb590b59fc201c558f5c400490c99455a4f02093f44f8b429b21b024fa29bb3 in /usr/local/bin/ 
# Sat, 06 Mar 2021 06:55:07 GMT
ENV DRUPAL_VERSION=9.1.5
# Sat, 06 Mar 2021 06:55:07 GMT
WORKDIR /opt/drupal
# Sat, 06 Mar 2021 06:55:18 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Sat, 06 Mar 2021 06:55:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93bf0848637956981647ef811bd93ac5be28d5b6746fcd92c3d47999360827ea`  
		Last Modified: Sat, 06 Mar 2021 06:32:32 GMT  
		Size: 1.3 MB (1340931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42c7ddf3338655197301b034774b31160bbba7c3dc53a967ca60522cbe26f94b`  
		Last Modified: Sat, 06 Mar 2021 06:32:32 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:887892003297c3f91de6457c33937150956578d4a2467ff0d24ba7e74c8e022c`  
		Last Modified: Sat, 06 Mar 2021 06:32:32 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f787ac2e3cfc8ca48030752744b5494104a69280b8a7a5b6734acf393ae404`  
		Last Modified: Sat, 06 Mar 2021 06:33:04 GMT  
		Size: 10.8 MB (10774630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4f431b2100497cf2da2ea205a7667427f1157cf1cb677aa7346401e3f093900`  
		Last Modified: Sat, 06 Mar 2021 06:33:00 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd060ae57421fbd81dd86fb8832713ff3832e945627e17ca3e14f608e33dfbd2`  
		Last Modified: Sat, 06 Mar 2021 06:33:03 GMT  
		Size: 15.0 MB (14967967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b07347fd945fca678990543cb5cff3e1b97f73fa4b8dcd9e8c156fcc57da6c5b`  
		Last Modified: Sat, 06 Mar 2021 06:33:00 GMT  
		Size: 2.3 KB (2267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd3a72c5fc8c1579f79a5a41c916f3db56635d2703c7d616013783946b396e89`  
		Last Modified: Sat, 06 Mar 2021 06:33:00 GMT  
		Size: 16.9 KB (16898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:274d5db003505347f8d83f100e0217172f5f9c7b1daf758e7bdee7d2486ffccf`  
		Last Modified: Sat, 06 Mar 2021 06:33:00 GMT  
		Size: 8.6 KB (8572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:110625872b64fa8e0818b9b4a2d8f9bc717e3dfc31f5cccdeb95933d8458e99d`  
		Last Modified: Sat, 06 Mar 2021 07:09:39 GMT  
		Size: 3.2 MB (3211656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e170244b78d117c5670029b936529019d67eb35c6eb38a1e1469551d24b33729`  
		Last Modified: Sat, 06 Mar 2021 07:09:38 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c6fb8ac8b09bdae20eb7291dd3472ec6757d9ba531a6b6783f2bf153e6ef9eb`  
		Last Modified: Sat, 06 Mar 2021 07:09:39 GMT  
		Size: 551.8 KB (551805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:518419d019d8c66c96e25c951e4c646e6e673659b719ef519e023b2a8b67616e`  
		Last Modified: Sat, 06 Mar 2021 07:09:38 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:841223ac7a85292c00cea106f0dc84f93917f53dc2afc596ca7f56134b0c7d93`  
		Last Modified: Sat, 06 Mar 2021 07:09:44 GMT  
		Size: 18.8 MB (18826981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:9-fpm-alpine3.12` - linux; arm variant v6

```console
$ docker pull drupal@sha256:31980ec61bc0b48c7324ad0a2ca894beab537dce87b86344f4af50522469b468
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50493550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8348bd20c663584ad7bd202c1a8f1402c2c274156a29e673e2b66615a5bb1aa5`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 24 Feb 2021 20:50:34 GMT
ADD file:8bbb59eeaad0cbcf11559bc6e2b4492aadf6822d1935ed50c710f8bed858b7b5 in / 
# Wed, 24 Feb 2021 20:50:35 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 21:48:44 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 24 Feb 2021 21:48:48 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 24 Feb 2021 21:48:51 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 24 Feb 2021 21:48:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 24 Feb 2021 21:48:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 24 Feb 2021 21:53:09 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Wed, 24 Feb 2021 21:53:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Feb 2021 21:53:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Feb 2021 21:53:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 24 Feb 2021 21:53:13 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 05 Mar 2021 00:18:23 GMT
ENV PHP_VERSION=8.0.3
# Fri, 05 Mar 2021 00:18:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.3.tar.xz.asc
# Fri, 05 Mar 2021 00:18:26 GMT
ENV PHP_SHA256=c9816aa9745a9695672951eaff3a35ca5eddcb9cacf87a4f04b9fb1169010251
# Fri, 05 Mar 2021 00:18:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 05 Mar 2021 00:18:33 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:22:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Mar 2021 00:22:14 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:22:17 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Mar 2021 00:22:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Mar 2021 00:22:18 GMT
WORKDIR /var/www/html
# Fri, 05 Mar 2021 00:22:20 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 05 Mar 2021 00:22:21 GMT
STOPSIGNAL SIGQUIT
# Fri, 05 Mar 2021 00:22:22 GMT
EXPOSE 9000
# Fri, 05 Mar 2021 00:22:23 GMT
CMD ["php-fpm"]
# Fri, 05 Mar 2021 01:19:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps
# Fri, 05 Mar 2021 01:19:22 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 05 Mar 2021 01:19:23 GMT
COPY file:deb590b59fc201c558f5c400490c99455a4f02093f44f8b429b21b024fa29bb3 in /usr/local/bin/ 
# Fri, 05 Mar 2021 01:19:23 GMT
ENV DRUPAL_VERSION=9.1.5
# Fri, 05 Mar 2021 01:19:24 GMT
WORKDIR /opt/drupal
# Fri, 05 Mar 2021 01:19:54 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Fri, 05 Mar 2021 01:19:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:55242616b0494f68f44470d864da746cd2a8f8f2d1ffca698114de64032247ef`  
		Last Modified: Wed, 24 Feb 2021 20:51:17 GMT  
		Size: 2.6 MB (2604518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:615a3cb7c8a689c7b4b457673e4a5678045e9719205698379bb794653438a8f8`  
		Last Modified: Wed, 24 Feb 2021 22:25:14 GMT  
		Size: 1.3 MB (1310252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779c61c3f721398235ceaccb55a3fb089907ab61a3bc41f3fe457c740545a965`  
		Last Modified: Wed, 24 Feb 2021 22:25:14 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f577d474ce74b9771d890356acf5aab30aa563d9c7c2edf98725de2e1c194d4`  
		Last Modified: Wed, 24 Feb 2021 22:25:13 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18f9c08ff0d00d30982064c45811e0f019f30c123f706c4c1af9187beca0b68b`  
		Last Modified: Fri, 05 Mar 2021 00:52:45 GMT  
		Size: 10.8 MB (10774628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f0186020cf3cee5065dceb73b2a97dce224d1138411dd29e52fd70101164aa`  
		Last Modified: Fri, 05 Mar 2021 00:52:41 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77303d73098a0666021a3ef557052b626a80c8671ccdc85dc62ea1c0af61adcf`  
		Last Modified: Fri, 05 Mar 2021 00:52:47 GMT  
		Size: 13.6 MB (13646516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28607b319576ae3419f346cb313fa69d3119de7eb3fd48ddbe23f34d390deae`  
		Last Modified: Fri, 05 Mar 2021 00:52:41 GMT  
		Size: 2.3 KB (2265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4b4dfc1eba7fbeb95e13805e01889baec7870f086945caaedbd14701615f14`  
		Last Modified: Fri, 05 Mar 2021 00:52:41 GMT  
		Size: 16.9 KB (16888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b52cca5929b106db3e4a83ddca70be2d688e729f43d09d4dd7dbe5eb7949e6e`  
		Last Modified: Fri, 05 Mar 2021 00:52:41 GMT  
		Size: 8.6 KB (8570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84963b01cf880d931535d6b726bf3926a702a4f91716d4d00fae8cf5f7b8859e`  
		Last Modified: Fri, 05 Mar 2021 01:25:16 GMT  
		Size: 2.7 MB (2748672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ed7d705315c05529d782f6535fd080fc7b5651536aaee57fa6fcd6cfbeea35`  
		Last Modified: Fri, 05 Mar 2021 01:25:16 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4070924af37e291667b8152173818276612f60522fffa11b08eee70e2c456ae2`  
		Last Modified: Fri, 05 Mar 2021 01:25:15 GMT  
		Size: 551.8 KB (551804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf968a855ab8841e434bc88e569dca9df9f0f840f4d5796f66b1786571e1270`  
		Last Modified: Fri, 05 Mar 2021 01:25:15 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e7df2738a99a8419161f5b46363f7b459c20931534651976d0baa0c31cb508`  
		Last Modified: Fri, 05 Mar 2021 01:25:30 GMT  
		Size: 18.8 MB (18826934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:9-fpm-alpine3.12` - linux; arm variant v7

```console
$ docker pull drupal@sha256:afe501b671253b01b9b3590beaf42a02d32fab871088fdaf11dae46068226cb2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49091213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e34680bf2523776b311845ddf4e32b350187035227265749b2906d44c9cdd4c`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 24 Feb 2021 21:03:35 GMT
ADD file:2632f48dd643f8927da2b1af8365b3edb484bd6b7d9fee4009e69f6cf3310e91 in / 
# Wed, 24 Feb 2021 21:03:36 GMT
CMD ["/bin/sh"]
# Thu, 25 Feb 2021 00:38:36 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 25 Feb 2021 00:38:52 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 25 Feb 2021 00:39:06 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 25 Feb 2021 00:39:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 25 Feb 2021 00:39:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 25 Feb 2021 00:45:45 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Thu, 25 Feb 2021 00:45:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Feb 2021 00:45:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Feb 2021 00:45:51 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 25 Feb 2021 00:45:52 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 05 Mar 2021 00:28:59 GMT
ENV PHP_VERSION=8.0.3
# Fri, 05 Mar 2021 00:29:00 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.3.tar.xz.asc
# Fri, 05 Mar 2021 00:29:01 GMT
ENV PHP_SHA256=c9816aa9745a9695672951eaff3a35ca5eddcb9cacf87a4f04b9fb1169010251
# Fri, 05 Mar 2021 00:29:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 05 Mar 2021 00:29:10 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:31:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Mar 2021 00:31:55 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:32:00 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Mar 2021 00:32:02 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Mar 2021 00:32:07 GMT
WORKDIR /var/www/html
# Fri, 05 Mar 2021 00:32:11 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 05 Mar 2021 00:32:12 GMT
STOPSIGNAL SIGQUIT
# Fri, 05 Mar 2021 00:32:16 GMT
EXPOSE 9000
# Fri, 05 Mar 2021 00:32:17 GMT
CMD ["php-fpm"]
# Fri, 05 Mar 2021 02:49:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps
# Fri, 05 Mar 2021 02:49:47 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 05 Mar 2021 02:49:48 GMT
COPY file:deb590b59fc201c558f5c400490c99455a4f02093f44f8b429b21b024fa29bb3 in /usr/local/bin/ 
# Fri, 05 Mar 2021 02:49:49 GMT
ENV DRUPAL_VERSION=9.1.5
# Fri, 05 Mar 2021 02:49:50 GMT
WORKDIR /opt/drupal
# Fri, 05 Mar 2021 02:50:24 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Fri, 05 Mar 2021 02:50:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:8e85c7428c31ea48b47424ca0e4663106c54591c83545d32b66a77093f90ffd0`  
		Last Modified: Wed, 24 Feb 2021 21:04:23 GMT  
		Size: 2.4 MB (2408004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14cc8b4ab32066557eac8444fa33ee5ebaed36826b316cd88df2b9cb3005d89`  
		Last Modified: Thu, 25 Feb 2021 01:29:39 GMT  
		Size: 1.2 MB (1214324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3820ceb6aa3721ffa3c4431d838261590e757f46b57b8598c1ec5ec4262a2a4`  
		Last Modified: Thu, 25 Feb 2021 01:29:38 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af4e3ecf788cb43363fdced38ca2f1e332603abf470c39ac131d849811ca5e95`  
		Last Modified: Thu, 25 Feb 2021 01:29:38 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164e353eaa81bb967bbc283fdbb53bba784acf2d7085d72ed622f2f807064ee7`  
		Last Modified: Fri, 05 Mar 2021 01:18:21 GMT  
		Size: 10.8 MB (10774621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:566061ad3cdbfe75be3fdae0892767d75d28285f9d0a4ac8aae9b15ded5a214c`  
		Last Modified: Fri, 05 Mar 2021 01:18:17 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc2b0d2dfb5374378804d613293b4d38bafc848e81b7dd7ee5d2094f84915e5`  
		Last Modified: Fri, 05 Mar 2021 01:18:22 GMT  
		Size: 12.8 MB (12791043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c5e55491a3852e276dd912f460c17644b9636f28044a94e25227f72bc52418`  
		Last Modified: Fri, 05 Mar 2021 01:18:18 GMT  
		Size: 2.3 KB (2264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60dc93bc03cf9ec7a2d0140c737e84e73d9765f3de3f74fc57fd99c28117c235`  
		Last Modified: Fri, 05 Mar 2021 01:18:17 GMT  
		Size: 16.9 KB (16870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a344bc1aeac7a9f523be67512952297f7350249d79a0cd7e271dd52050adf38e`  
		Last Modified: Fri, 05 Mar 2021 01:18:17 GMT  
		Size: 8.6 KB (8574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8577d5cc99fa58a648b258f1cf07c5d041c0461b94234fe180bcca5e036712c`  
		Last Modified: Fri, 05 Mar 2021 03:09:28 GMT  
		Size: 2.5 MB (2493384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e2a8e1ba5272b74503e2a6d1393574f5f3867e3a1407027d8107c5e66dd3473`  
		Last Modified: Fri, 05 Mar 2021 03:09:27 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b8d2806a4bef4beed760daf0f8dc2d1767a89eb28cead9959f1be62ff59f08c`  
		Last Modified: Fri, 05 Mar 2021 03:09:27 GMT  
		Size: 551.8 KB (551804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c31202c06b2c16eb49c96681fa3c5d978aeb8edc36f87f2f2510d546a4402e01`  
		Last Modified: Fri, 05 Mar 2021 03:09:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d102c8da277b5f796b08576e5d59f176fa40e2cce554926bb1da4e723664049`  
		Last Modified: Fri, 05 Mar 2021 03:09:39 GMT  
		Size: 18.8 MB (18827821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:9-fpm-alpine3.12` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:e843e39c838346a1b4f57ffee59cfcfc71ec868220c0fc3b59ff49a19b3a88fb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51564850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df69db76b28a3d5926c4fd731fd07073d04df334b444ad859eac8adb1714ff57`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 24 Feb 2021 20:39:39 GMT
ADD file:7e82858ef85f6db90c131ed835a390d736cfdbd1a0cf8bccaeed8f7e30172ddb in / 
# Wed, 24 Feb 2021 20:39:40 GMT
CMD ["/bin/sh"]
# Thu, 25 Feb 2021 02:15:11 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 25 Feb 2021 02:15:18 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 25 Feb 2021 02:15:24 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 25 Feb 2021 02:15:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 25 Feb 2021 02:15:35 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 25 Feb 2021 02:19:48 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Thu, 25 Feb 2021 02:19:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Feb 2021 02:19:50 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Feb 2021 02:19:51 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 25 Feb 2021 02:19:52 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 05 Mar 2021 00:13:41 GMT
ENV PHP_VERSION=8.0.3
# Fri, 05 Mar 2021 00:13:42 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.3.tar.xz.asc
# Fri, 05 Mar 2021 00:13:43 GMT
ENV PHP_SHA256=c9816aa9745a9695672951eaff3a35ca5eddcb9cacf87a4f04b9fb1169010251
# Fri, 05 Mar 2021 00:13:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 05 Mar 2021 00:13:50 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:17:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Mar 2021 00:17:36 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:17:41 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Mar 2021 00:17:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Mar 2021 00:17:44 GMT
WORKDIR /var/www/html
# Fri, 05 Mar 2021 00:17:47 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 05 Mar 2021 00:17:48 GMT
STOPSIGNAL SIGQUIT
# Fri, 05 Mar 2021 00:17:49 GMT
EXPOSE 9000
# Fri, 05 Mar 2021 00:17:50 GMT
CMD ["php-fpm"]
# Fri, 05 Mar 2021 01:37:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps
# Fri, 05 Mar 2021 01:37:26 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 05 Mar 2021 01:37:27 GMT
COPY file:deb590b59fc201c558f5c400490c99455a4f02093f44f8b429b21b024fa29bb3 in /usr/local/bin/ 
# Fri, 05 Mar 2021 01:37:28 GMT
ENV DRUPAL_VERSION=9.1.5
# Fri, 05 Mar 2021 01:37:30 GMT
WORKDIR /opt/drupal
# Fri, 05 Mar 2021 01:37:58 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Fri, 05 Mar 2021 01:38:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:dce8679b510e95d136241d02ababff86469dd14220812a7ce9202833c0e32f66`  
		Last Modified: Wed, 24 Feb 2021 20:40:26 GMT  
		Size: 2.7 MB (2709880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd265321b6926cee038cf7fc6338237aac197c6c9ef85b1982906eb78e6ea2c`  
		Last Modified: Thu, 25 Feb 2021 02:52:50 GMT  
		Size: 1.3 MB (1342954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb80a7dbf57a115e70afd93274767256a51782fee74606762ff0c3bbbd5b91d1`  
		Last Modified: Thu, 25 Feb 2021 02:52:50 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba32dc0c8f3fa39e73379ea7a837a9987f419051e77502e949be24d45d001ae2`  
		Last Modified: Thu, 25 Feb 2021 02:52:50 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b0ae0937c0110ce147d1d529d8840485935eb2d1d291ad275c9d16af6122c2`  
		Last Modified: Fri, 05 Mar 2021 01:11:53 GMT  
		Size: 10.8 MB (10774633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561016159f866a3e95ef7781160b1ef730e6e1d508072bc16881f77ab71a75f7`  
		Last Modified: Fri, 05 Mar 2021 01:11:46 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be866a35c37b933b3efc72da2a2948ef84f28bfc70e38448f1cea2a84f065941`  
		Last Modified: Fri, 05 Mar 2021 01:11:49 GMT  
		Size: 14.4 MB (14438778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d34ad8b78d7609cb63e88e6d2fd6a38d508426183f8d97eda4d6ac38ed8c4f0`  
		Last Modified: Fri, 05 Mar 2021 01:11:45 GMT  
		Size: 2.3 KB (2266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c42e1e1a01f2267461697eabc377fc6fda9d8e673693c791a8a85dc528933a`  
		Last Modified: Fri, 05 Mar 2021 01:11:46 GMT  
		Size: 16.9 KB (16893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129f98fafadea1f879e8f189edfb74de7a6b78181e2777b973ec1bde9d2cd857`  
		Last Modified: Fri, 05 Mar 2021 01:11:46 GMT  
		Size: 8.6 KB (8571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea2a956229842725e8b6dc875d89bf1a9c90f96c8ba1a78e1c96515fd8ae004f`  
		Last Modified: Fri, 05 Mar 2021 01:54:37 GMT  
		Size: 2.9 MB (2889287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:721352bd7f2d41951890632808dfa142233adf8880657d9a67b0b3eb7d28a6d5`  
		Last Modified: Fri, 05 Mar 2021 01:54:36 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668a7446d342ab8c21ed3c7e58d1a4f364a570f12e824f023c28ac446e873279`  
		Last Modified: Fri, 05 Mar 2021 01:54:36 GMT  
		Size: 551.8 KB (551801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:721d75890a9d8f5ecf4c12afbf15121c7892a36bc1f83009498e19dcc00a8641`  
		Last Modified: Fri, 05 Mar 2021 01:54:36 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b68722b483fefe88e5364c10c919b198996bb7ff8e613601d2a860829b9070`  
		Last Modified: Fri, 05 Mar 2021 01:54:44 GMT  
		Size: 18.8 MB (18827290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:9-fpm-alpine3.12` - linux; 386

```console
$ docker pull drupal@sha256:a4b57934a497a97a961df261baab43fefb517347d873cd63c185764164994f0d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52512050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e51eb57e08e07ac09b58a8fdde5aa296433b28a8219f5808efc4f521e3a8d30`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 24 Feb 2021 20:38:41 GMT
ADD file:1f1a1b55522505e78fcc069edb6c793371f78991e90dcb464e4ddac7efd6588c in / 
# Wed, 24 Feb 2021 20:38:41 GMT
CMD ["/bin/sh"]
# Sat, 06 Mar 2021 02:28:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 06 Mar 2021 02:28:31 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 06 Mar 2021 02:28:32 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 06 Mar 2021 02:28:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 06 Mar 2021 02:28:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 06 Mar 2021 02:34:58 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Sat, 06 Mar 2021 02:34:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 06 Mar 2021 02:34:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 06 Mar 2021 02:34:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 06 Mar 2021 02:34:59 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Sat, 06 Mar 2021 02:34:59 GMT
ENV PHP_VERSION=8.0.3
# Sat, 06 Mar 2021 02:34:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.3.tar.xz.asc
# Sat, 06 Mar 2021 02:34:59 GMT
ENV PHP_SHA256=c9816aa9745a9695672951eaff3a35ca5eddcb9cacf87a4f04b9fb1169010251
# Sat, 06 Mar 2021 02:35:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 06 Mar 2021 02:35:09 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 06 Mar 2021 02:40:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 06 Mar 2021 02:40:31 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Sat, 06 Mar 2021 02:40:33 GMT
RUN docker-php-ext-enable sodium
# Sat, 06 Mar 2021 02:40:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 06 Mar 2021 02:40:33 GMT
WORKDIR /var/www/html
# Sat, 06 Mar 2021 02:40:34 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Sat, 06 Mar 2021 02:40:34 GMT
STOPSIGNAL SIGQUIT
# Sat, 06 Mar 2021 02:40:34 GMT
EXPOSE 9000
# Sat, 06 Mar 2021 02:40:34 GMT
CMD ["php-fpm"]
# Sat, 06 Mar 2021 06:11:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps
# Sat, 06 Mar 2021 06:11:42 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Sat, 13 Mar 2021 01:40:56 GMT
COPY file:cddfcd7dd4b08ff278956da31aa5501966cc1e2e3488252d8cc9fdf6bb03e79a in /usr/local/bin/ 
# Sat, 13 Mar 2021 01:40:57 GMT
ENV DRUPAL_VERSION=9.1.5
# Sat, 13 Mar 2021 01:40:57 GMT
WORKDIR /opt/drupal
# Sat, 13 Mar 2021 01:41:11 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Sat, 13 Mar 2021 01:41:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:045e8056601208133bee5c98e76028f9b97e055c738892f8d6283205e1006173`  
		Last Modified: Wed, 24 Feb 2021 20:39:27 GMT  
		Size: 2.8 MB (2794750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6df58f7e1c807582274a5142090a7b96424a04744c8523ea259581d2198e7e7`  
		Last Modified: Sat, 06 Mar 2021 05:49:23 GMT  
		Size: 1.4 MB (1439799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de2f52988e279e40c7eb9502c6858f144ef5166db6bb0ee9df70f8727cae2c2`  
		Last Modified: Sat, 06 Mar 2021 05:49:22 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813495ba42f39113454530a1422f6905311d09ce3721a4ee7e5e6a3b4be275b9`  
		Last Modified: Sat, 06 Mar 2021 05:49:22 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79b0b4bf1e48e49ae5d16882dc25cec16839a82daca98e0ae2dedab7ad4ee095`  
		Last Modified: Sat, 06 Mar 2021 05:50:05 GMT  
		Size: 10.8 MB (10774612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:544159469f09af16894b404e9dd20ba58fa8f062b68e277b2401e03937d14451`  
		Last Modified: Sat, 06 Mar 2021 05:50:00 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a870c87c31dc3e6cd9ab6dd301f3805eca4a7ccaa718d667559149c091d9f130`  
		Last Modified: Sat, 06 Mar 2021 05:50:10 GMT  
		Size: 15.0 MB (15014222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de449c812f3ac1ef92d2060d0ab81b61408d393adbab55d3f2569ef10ec1c726`  
		Last Modified: Sat, 06 Mar 2021 05:50:00 GMT  
		Size: 2.3 KB (2267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f541d54520348e77657db1df1512f734a8757c52d67fbccc35fdd401a9ef2316`  
		Last Modified: Sat, 06 Mar 2021 05:50:00 GMT  
		Size: 16.9 KB (16883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:606e830dc6a06f0782193ec6570ace961f9477c561403044035ff92e67334b3c`  
		Last Modified: Sat, 06 Mar 2021 05:50:00 GMT  
		Size: 8.6 KB (8568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:544a7e99b844b9a29a37dd7f0bf2f5c01551dbc02b9e1dbe7ea967236abe30f5`  
		Last Modified: Sat, 06 Mar 2021 06:34:02 GMT  
		Size: 3.1 MB (3078265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54db3a26f0d8873b827d7080c598d6ee8cab36edbe5e665706cc3e85d059ac67`  
		Last Modified: Sat, 06 Mar 2021 06:34:02 GMT  
		Size: 322.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b71d24606907928dbbab691da1954133d4d82b7b195f8de3de5fda0ef197bc`  
		Last Modified: Sat, 13 Mar 2021 02:01:45 GMT  
		Size: 552.9 KB (552899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0805e99397cb2324d8267300cbb930bb73225cfb9846ee9bb06c39f6088cc753`  
		Last Modified: Sat, 13 Mar 2021 02:01:45 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e385c7efced2350f8f0c3b1d067acbb4aafc5e56436da3067049f91a2736bfa`  
		Last Modified: Sat, 13 Mar 2021 02:01:55 GMT  
		Size: 18.8 MB (18827289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:9-fpm-alpine3.12` - linux; ppc64le

```console
$ docker pull drupal@sha256:cd7cf699216ed5b0036dc403f90b35ef366d99cc120a6d9fb0d9331ce868fb91
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53097919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06aac128e5fd0cf9fbc37e03f9441a47c6fa1e67b9d8d3f863d93889b563b457`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 24 Feb 2021 20:45:10 GMT
ADD file:90df4b3d767cd67ff62e490ca0a7d69bae532cf3fa6f8971a0d2c1b27fb4bdd1 in / 
# Wed, 24 Feb 2021 20:45:16 GMT
CMD ["/bin/sh"]
# Thu, 25 Feb 2021 02:18:35 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 25 Feb 2021 02:18:50 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 25 Feb 2021 02:19:09 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 25 Feb 2021 02:19:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 25 Feb 2021 02:19:36 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 25 Feb 2021 02:25:32 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Thu, 25 Feb 2021 02:25:36 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Feb 2021 02:25:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Feb 2021 02:25:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 25 Feb 2021 02:25:53 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 05 Mar 2021 00:24:08 GMT
ENV PHP_VERSION=8.0.3
# Fri, 05 Mar 2021 00:24:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.3.tar.xz.asc
# Fri, 05 Mar 2021 00:24:24 GMT
ENV PHP_SHA256=c9816aa9745a9695672951eaff3a35ca5eddcb9cacf87a4f04b9fb1169010251
# Fri, 05 Mar 2021 00:24:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 05 Mar 2021 00:24:48 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:28:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Mar 2021 00:28:44 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Fri, 05 Mar 2021 00:28:56 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Mar 2021 00:29:06 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Mar 2021 00:29:21 GMT
WORKDIR /var/www/html
# Fri, 05 Mar 2021 00:29:50 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 05 Mar 2021 00:30:00 GMT
STOPSIGNAL SIGQUIT
# Fri, 05 Mar 2021 00:30:14 GMT
EXPOSE 9000
# Fri, 05 Mar 2021 00:30:21 GMT
CMD ["php-fpm"]
# Fri, 05 Mar 2021 02:27:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps
# Fri, 05 Mar 2021 02:27:48 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 05 Mar 2021 02:27:50 GMT
COPY file:deb590b59fc201c558f5c400490c99455a4f02093f44f8b429b21b024fa29bb3 in /usr/local/bin/ 
# Fri, 05 Mar 2021 02:27:55 GMT
ENV DRUPAL_VERSION=9.1.5
# Fri, 05 Mar 2021 02:27:57 GMT
WORKDIR /opt/drupal
# Fri, 05 Mar 2021 02:28:29 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Fri, 05 Mar 2021 02:28:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:8f446c8f22d4a7a7520099080f73ffa6f455358a840b542fb2ad15c0032adeca`  
		Last Modified: Wed, 24 Feb 2021 20:46:19 GMT  
		Size: 2.8 MB (2805893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:442844d8617592bb8b8a6a6806933d8ce610ddeb989712f03f8abc7daf0e8a09`  
		Last Modified: Thu, 25 Feb 2021 03:09:38 GMT  
		Size: 1.4 MB (1383188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:765d755a8614ffa2086b17c3a59d50abbd5a7f85bf41d5c5424d6b7ac1d9aeff`  
		Last Modified: Thu, 25 Feb 2021 03:09:37 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec8dadfb9e7f832d4e8acd90c13b1450c86379a9bc45045f7fca480e61ce4a6`  
		Last Modified: Thu, 25 Feb 2021 03:09:37 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1e7327d2a9b40995bbdb27163e29cbb13faba9bb21408c45ee7d76841dcb7b6`  
		Last Modified: Fri, 05 Mar 2021 01:47:35 GMT  
		Size: 10.8 MB (10774632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b305ca3041478bcaa480a5b12933a3dc820085e93fc7e737236069a77b4be1f`  
		Last Modified: Fri, 05 Mar 2021 01:47:30 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6496eecd821d47db665e9a6c1c212d0a583ad403633c49f7c62dea85544bdd68`  
		Last Modified: Fri, 05 Mar 2021 01:47:35 GMT  
		Size: 15.7 MB (15654002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48aae90e5b234ac0b5eebdf5739795d185981ad50782a07987e6568ebe1712fd`  
		Last Modified: Fri, 05 Mar 2021 01:47:30 GMT  
		Size: 2.3 KB (2266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:570924a31fc3691bbcc427cc90c74ddc889c06fce4bf3bda557092e17de0a054`  
		Last Modified: Fri, 05 Mar 2021 01:47:30 GMT  
		Size: 16.9 KB (16927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9895ae8da8b8fc2569b659d540d86bf5e1182e78b7f08e8e8a15a866a5de6315`  
		Last Modified: Fri, 05 Mar 2021 01:47:31 GMT  
		Size: 8.6 KB (8571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5602644707c92d58b923bb94285d8c838bc178c45d585ac1a837608148a248`  
		Last Modified: Fri, 05 Mar 2021 03:00:29 GMT  
		Size: 3.1 MB (3070837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f476cd206554513c10a69ac679f7a5f3a6edaa26afce1fd4ec07836cf530d2b5`  
		Last Modified: Fri, 05 Mar 2021 03:00:27 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01fcdf96c8d98849a95156ca2781bdba09a4bcae527496268ebc1d3ae57ac278`  
		Last Modified: Fri, 05 Mar 2021 03:00:28 GMT  
		Size: 551.8 KB (551805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b44663ec050029dd3b8679b954728dddfeb887d144934775d48ea4d80790487`  
		Last Modified: Fri, 05 Mar 2021 03:00:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:125fe2761b76281458d12fdc4f47313d7397e35a7cba50ba4189ffd0478257cd`  
		Last Modified: Fri, 05 Mar 2021 03:02:26 GMT  
		Size: 18.8 MB (18827291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:9-fpm-alpine3.12` - linux; s390x

```console
$ docker pull drupal@sha256:0d267314975b3622cd522bcc39ab13dfc027902d1582a14c81b291a62e06cf63
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50989250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2840412a3b2ba4fde582418a83b1cb1960d14013f53f6fdcd0b6b6c1b065739a`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 25 Mar 2021 22:41:39 GMT
ADD file:12766b6fe7c37292d91bd1469b27dc9fb362e3109e9b3f377cff030bc0ca5386 in / 
# Thu, 25 Mar 2021 22:41:39 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 05:41:01 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 26 Mar 2021 05:41:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 26 Mar 2021 05:41:05 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 26 Mar 2021 05:41:05 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 26 Mar 2021 05:41:06 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 26 Mar 2021 05:44:06 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Fri, 26 Mar 2021 05:44:06 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 26 Mar 2021 05:44:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 26 Mar 2021 05:44:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 26 Mar 2021 05:44:06 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 26 Mar 2021 05:44:07 GMT
ENV PHP_VERSION=8.0.3
# Fri, 26 Mar 2021 05:44:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.3.tar.xz.asc
# Fri, 26 Mar 2021 05:44:07 GMT
ENV PHP_SHA256=c9816aa9745a9695672951eaff3a35ca5eddcb9cacf87a4f04b9fb1169010251
# Fri, 26 Mar 2021 05:44:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 26 Mar 2021 05:44:10 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 26 Mar 2021 05:46:47 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 26 Mar 2021 05:46:48 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Fri, 26 Mar 2021 05:46:49 GMT
RUN docker-php-ext-enable sodium
# Fri, 26 Mar 2021 05:46:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 26 Mar 2021 05:46:49 GMT
WORKDIR /var/www/html
# Fri, 26 Mar 2021 05:46:50 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 26 Mar 2021 05:46:50 GMT
STOPSIGNAL SIGQUIT
# Fri, 26 Mar 2021 05:46:51 GMT
EXPOSE 9000
# Fri, 26 Mar 2021 05:46:51 GMT
CMD ["php-fpm"]
# Fri, 26 Mar 2021 10:07:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps
# Fri, 26 Mar 2021 10:07:38 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 26 Mar 2021 10:07:38 GMT
COPY file:cddfcd7dd4b08ff278956da31aa5501966cc1e2e3488252d8cc9fdf6bb03e79a in /usr/local/bin/ 
# Fri, 26 Mar 2021 10:07:38 GMT
ENV DRUPAL_VERSION=9.1.5
# Fri, 26 Mar 2021 10:07:38 GMT
WORKDIR /opt/drupal
# Fri, 26 Mar 2021 10:07:51 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Fri, 26 Mar 2021 10:07:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:be2cdf7cbb6a1aec476a957daaae210624b2b112c20f27f55bbcf2bdc74db281`  
		Last Modified: Thu, 25 Mar 2021 22:42:19 GMT  
		Size: 2.6 MB (2567457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c02c9f7c441c5e95223a25a193205797aa6a48d7653253dbe7324a33be8da248`  
		Last Modified: Fri, 26 Mar 2021 06:31:13 GMT  
		Size: 1.4 MB (1382755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:543ff1ddc0960837b2759b3fc5e3784ead26cc7c2a19b05025cfbbf5205fe7c1`  
		Last Modified: Fri, 26 Mar 2021 06:31:13 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeb33c079e82b97924b3104b5bcd707197c487d74a585eeb3d0068277552a844`  
		Last Modified: Fri, 26 Mar 2021 06:31:13 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f423510e44977676acc760b42a4dfa412d3f733eb1206ef12139ec55fa920614`  
		Last Modified: Fri, 26 Mar 2021 06:31:29 GMT  
		Size: 10.8 MB (10774615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78cf5d07da61b0fce043a5eff6c9debd86b33aebe86a7d99d24f49522ac91b15`  
		Last Modified: Fri, 26 Mar 2021 06:31:27 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e6fef684b9869e2568e8e5fa42e0882aea60e8a777e9248dd6a73febea6727c`  
		Last Modified: Fri, 26 Mar 2021 06:31:29 GMT  
		Size: 13.9 MB (13934587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f64006c532264dd0fb95d0d1dc68d363990550a3bf7d18de3aec7c8c75fa611a`  
		Last Modified: Fri, 26 Mar 2021 06:31:27 GMT  
		Size: 2.3 KB (2262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a958d74b0a58bdc861f1ca0197cec6041e8c79c1a1907e12c3b32402f10f7b31`  
		Last Modified: Fri, 26 Mar 2021 06:31:27 GMT  
		Size: 16.9 KB (16878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecfa1cb273acd37377f4c7b5c7ad2d3f490a3eaab5ab596f1c804c230ac5c04e`  
		Last Modified: Fri, 26 Mar 2021 06:31:27 GMT  
		Size: 8.6 KB (8569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7183b53d448f4ae6e341650caa7b4fc8699c814a51f0e8fe4fd64b26ee8a5837`  
		Last Modified: Fri, 26 Mar 2021 10:15:32 GMT  
		Size: 2.9 MB (2919587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a52773af728b6ac026be9348ff6d733e8a41d4cbf321530b095847f526f5e6`  
		Last Modified: Fri, 26 Mar 2021 10:15:32 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ff840c4e40bb3e3f307e5bfd54c9861eb95229c0beaade45612a7b4b100cfc`  
		Last Modified: Fri, 26 Mar 2021 10:15:32 GMT  
		Size: 552.9 KB (552892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b833f0db5ce74867df07136526901d99e9d6fdd859bcba21ee3fc3fc2fc48203`  
		Last Modified: Fri, 26 Mar 2021 10:15:32 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327810948026dc822e010de600212aa0f524e233e27db474dc46c3838b85fec2`  
		Last Modified: Fri, 26 Mar 2021 10:15:33 GMT  
		Size: 18.8 MB (18827154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
