## `drupal:7-php8.0-fpm-alpine3.16`

```console
$ docker pull drupal@sha256:511126b716fe1e5b94f48c863e4bf27243a26434fa7d08b9dfc682e4ba7902a4
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

### `drupal:7-php8.0-fpm-alpine3.16` - linux; amd64

```console
$ docker pull drupal@sha256:0abaa2468533212bdff69ed451f472b29738803d8d9290627bfc8c04e116ae1c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.8 MB (33839761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f287d857a56e916ebaee3ba03bc8dc4c3549acc0455213a3905a231fcd2d196`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 08:36:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 12 Nov 2022 08:36:56 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 12 Nov 2022 08:36:57 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 12 Nov 2022 08:36:57 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 12 Nov 2022 08:36:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 12 Nov 2022 08:36:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 12 Nov 2022 08:36:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 12 Nov 2022 08:36:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 12 Nov 2022 09:02:54 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F 2C16C765DBE54A088130F1BC4B9B5F600B55F3B4
# Fri, 06 Jan 2023 01:29:30 GMT
ENV PHP_VERSION=8.0.27
# Fri, 06 Jan 2023 01:29:30 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.27.tar.xz.asc
# Fri, 06 Jan 2023 01:29:30 GMT
ENV PHP_SHA256=f942cbfe2f7bacbb8039fb79bbec41c76ea779ac5c8157f21e1e0c1b28a5fc3a
# Fri, 06 Jan 2023 01:29:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 06 Jan 2023 01:29:38 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 06 Jan 2023 01:37:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 06 Jan 2023 01:37:24 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 06 Jan 2023 01:37:25 GMT
RUN docker-php-ext-enable sodium
# Fri, 06 Jan 2023 01:37:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 06 Jan 2023 01:37:25 GMT
WORKDIR /var/www/html
# Fri, 06 Jan 2023 01:37:26 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 06 Jan 2023 01:37:26 GMT
STOPSIGNAL SIGQUIT
# Fri, 06 Jan 2023 01:37:26 GMT
EXPOSE 9000
# Fri, 06 Jan 2023 01:37:26 GMT
CMD ["php-fpm"]
# Fri, 06 Jan 2023 02:39:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps
# Thu, 02 Feb 2023 02:06:17 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 02 Feb 2023 02:10:09 GMT
ENV DRUPAL_VERSION=7.94
# Thu, 02 Feb 2023 02:10:09 GMT
ENV DRUPAL_MD5=dae634ea0da005c5c435cfa9a9c5c322
# Thu, 02 Feb 2023 02:10:11 GMT
RUN set -eux; 	curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b78b4fe0ca1ca5277d0b56997b3a74ac05ac52ff34cf9d5c6c063bd3feca07e`  
		Last Modified: Sat, 12 Nov 2022 09:30:31 GMT  
		Size: 1.7 MB (1721291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d6040f2a28f7fd4288a87be2db7a8886104a1080402d0343e1c527c232d8963`  
		Last Modified: Sat, 12 Nov 2022 09:30:31 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e2e66b89284d71ee13c90182fe35d46d2461573064ae7f020aa4c22c1235e2a`  
		Last Modified: Sat, 12 Nov 2022 09:30:31 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3bc79f449d612654f0ffea53f7ee32a6e34f655b59725facdc7397541010f40`  
		Last Modified: Fri, 06 Jan 2023 01:56:38 GMT  
		Size: 10.8 MB (10822226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63b5c83b03853ec64071ffd1e1424681923ba24dfc87b1b9e9e3ec0065356ea`  
		Last Modified: Fri, 06 Jan 2023 01:56:37 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2357a7a3522d531b71011014e14c5351fb31c10e2a770fbb2d5fea7504a700`  
		Last Modified: Fri, 06 Jan 2023 01:57:04 GMT  
		Size: 12.7 MB (12709264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfd367acec48bcda755a7be077f1a6e5fd7953b56625c86c9d90bd0a99637df1`  
		Last Modified: Fri, 06 Jan 2023 01:57:01 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e67fb67ecbd7e47d759ea43e0b21b9f95462c3c816527694cfe784a50578eaa`  
		Last Modified: Fri, 06 Jan 2023 01:57:01 GMT  
		Size: 18.7 KB (18745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c1bfdf4ec7068cf195bd7a16257d4a4eaccebed31e86f898350868fc87b9794`  
		Last Modified: Fri, 06 Jan 2023 01:57:01 GMT  
		Size: 8.7 KB (8681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96d27541fee90dd134dca40fc70c31d4748d59e4193a0b82002a9560c4f159aa`  
		Last Modified: Fri, 06 Jan 2023 02:58:49 GMT  
		Size: 2.3 MB (2345679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b758afaec444180db395f0f9b16581787cd7867ee98396605e44a378d40310`  
		Last Modified: Thu, 02 Feb 2023 02:27:03 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd9141c5b3b581f24f5252a8ea14409e8e754f14f63e2e64da9313f132342f0`  
		Last Modified: Thu, 02 Feb 2023 02:33:08 GMT  
		Size: 3.4 MB (3402810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:7-php8.0-fpm-alpine3.16` - linux; arm variant v6

```console
$ docker pull drupal@sha256:22507cccb5aee74597ed457fd22d46e0ca129354e7ba30d56e8afac41908474d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (32029789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6737d1571133bfb5710264564bf56cc81e330aad7ba628a9ebfe85b0a8c5e0`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 12 Nov 2022 03:49:18 GMT
ADD file:493290ed8856fa13463defe63da0d30ab3de5dde042c87ef7c0701d66ebb8892 in / 
# Sat, 12 Nov 2022 03:49:18 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 04:54:59 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 12 Nov 2022 04:55:00 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 12 Nov 2022 04:55:01 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 12 Nov 2022 04:55:01 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 12 Nov 2022 04:55:01 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 12 Nov 2022 04:55:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 12 Nov 2022 04:55:02 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 12 Nov 2022 04:55:02 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 12 Nov 2022 05:21:40 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F 2C16C765DBE54A088130F1BC4B9B5F600B55F3B4
# Fri, 06 Jan 2023 01:03:14 GMT
ENV PHP_VERSION=8.0.27
# Fri, 06 Jan 2023 01:03:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.27.tar.xz.asc
# Fri, 06 Jan 2023 01:03:14 GMT
ENV PHP_SHA256=f942cbfe2f7bacbb8039fb79bbec41c76ea779ac5c8157f21e1e0c1b28a5fc3a
# Fri, 06 Jan 2023 01:03:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 06 Jan 2023 01:03:21 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 06 Jan 2023 01:11:35 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 06 Jan 2023 01:11:35 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 06 Jan 2023 01:11:36 GMT
RUN docker-php-ext-enable sodium
# Fri, 06 Jan 2023 01:11:37 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 06 Jan 2023 01:11:37 GMT
WORKDIR /var/www/html
# Fri, 06 Jan 2023 01:11:37 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 06 Jan 2023 01:11:37 GMT
STOPSIGNAL SIGQUIT
# Fri, 06 Jan 2023 01:11:37 GMT
EXPOSE 9000
# Fri, 06 Jan 2023 01:11:37 GMT
CMD ["php-fpm"]
# Fri, 06 Jan 2023 01:54:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps
# Thu, 02 Feb 2023 00:52:02 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 02 Feb 2023 00:53:36 GMT
ENV DRUPAL_VERSION=7.94
# Thu, 02 Feb 2023 00:53:36 GMT
ENV DRUPAL_MD5=dae634ea0da005c5c435cfa9a9c5c322
# Thu, 02 Feb 2023 00:53:37 GMT
RUN set -eux; 	curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes
```

-	Layers:
	-	`sha256:9616ea8c1de4a90b1a50591336485e88ae5c2346e0d778bdbe69b00647bf8e39`  
		Last Modified: Sat, 12 Nov 2022 03:50:12 GMT  
		Size: 2.6 MB (2615105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:089b5ea696a25e03b2eaa2ba4c2d7ca2b161473cb9f1686ca8b9af4b714cc216`  
		Last Modified: Sat, 12 Nov 2022 05:51:25 GMT  
		Size: 1.7 MB (1708068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148c879de0e59a35d228a53d3c70813c09859b8647217f5bdf53e6b8058daa80`  
		Last Modified: Sat, 12 Nov 2022 05:51:24 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b9d16af9cd3acc95ea5a8da94a040a0f63b8af95a60a4ad30aaddbab836604`  
		Last Modified: Sat, 12 Nov 2022 05:51:24 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf846210a8ecda576c10d7e1e179493a574a121c4156d65c1b519b0b5d0270a`  
		Last Modified: Fri, 06 Jan 2023 01:26:11 GMT  
		Size: 10.8 MB (10822217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f65b8237d4c527d2d7737a3707b7a49c52d10d73b7424df0db4320724741bf16`  
		Last Modified: Fri, 06 Jan 2023 01:26:09 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a660940156edbec293c27253256bdadb1572d79cfd66dd0bae56d3dc9b2c3ed9`  
		Last Modified: Fri, 06 Jan 2023 01:26:51 GMT  
		Size: 11.6 MB (11622431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7992236647c33ad7e7786f099d2f7122db1d0ffe7f6d9cc3b0ed64f978cbbb11`  
		Last Modified: Fri, 06 Jan 2023 01:26:48 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef7aa622123e26da1d4b95ce8513d529363124c8ad1a6f67e69c5c1f74b1c768`  
		Last Modified: Fri, 06 Jan 2023 01:26:48 GMT  
		Size: 18.8 KB (18756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31787cb578d25b38dab0b0ea66bfca270d9c1a8ee01767cbd32a61b9c83e31c4`  
		Last Modified: Fri, 06 Jan 2023 01:26:48 GMT  
		Size: 8.7 KB (8681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:977ddae3e72160fcb0760c73e7020428155ef6dccd1bf1af109a959a71a05f93`  
		Last Modified: Fri, 06 Jan 2023 02:04:29 GMT  
		Size: 1.8 MB (1827315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8443a0a1402c5470344a1ee526594ccfc30e5c1c9de14441e742c701592ba1e8`  
		Last Modified: Thu, 02 Feb 2023 01:01:31 GMT  
		Size: 312.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:271d0d575a0148acb2f230cbaa65db2293ff06fbcad4ec20e688b2cb0cd7f02a`  
		Last Modified: Thu, 02 Feb 2023 01:03:26 GMT  
		Size: 3.4 MB (3402502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:7-php8.0-fpm-alpine3.16` - linux; arm variant v7

```console
$ docker pull drupal@sha256:967417b224b8f2ef62531ece097ccddeee90776e7f511fb7197589146766324c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 MB (30840772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:747c242cd0f403c1b3ae317fb41316e674dfe5f62eada3b925535dab7a4763e0`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 12 Nov 2022 03:57:24 GMT
ADD file:0b4a628f529226f5ec9d357ca63138bd2d22411a889c780ac8d395d761e07b2c in / 
# Sat, 12 Nov 2022 03:57:24 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 05:47:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 12 Nov 2022 05:47:35 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 12 Nov 2022 05:47:35 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 12 Nov 2022 05:47:35 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 12 Nov 2022 05:47:36 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 12 Nov 2022 05:47:36 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 12 Nov 2022 05:47:36 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 12 Nov 2022 05:47:36 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 12 Nov 2022 06:14:59 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F 2C16C765DBE54A088130F1BC4B9B5F600B55F3B4
# Fri, 06 Jan 2023 01:18:42 GMT
ENV PHP_VERSION=8.0.27
# Fri, 06 Jan 2023 01:18:42 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.27.tar.xz.asc
# Fri, 06 Jan 2023 01:18:42 GMT
ENV PHP_SHA256=f942cbfe2f7bacbb8039fb79bbec41c76ea779ac5c8157f21e1e0c1b28a5fc3a
# Fri, 06 Jan 2023 01:18:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 06 Jan 2023 01:18:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 06 Jan 2023 01:25:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 06 Jan 2023 01:25:28 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 06 Jan 2023 01:25:30 GMT
RUN docker-php-ext-enable sodium
# Fri, 06 Jan 2023 01:25:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 06 Jan 2023 01:25:31 GMT
WORKDIR /var/www/html
# Fri, 06 Jan 2023 01:25:31 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 06 Jan 2023 01:25:31 GMT
STOPSIGNAL SIGQUIT
# Fri, 06 Jan 2023 01:25:31 GMT
EXPOSE 9000
# Fri, 06 Jan 2023 01:25:31 GMT
CMD ["php-fpm"]
# Fri, 06 Jan 2023 02:41:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps
# Thu, 02 Feb 2023 01:47:10 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 02 Feb 2023 01:53:16 GMT
ENV DRUPAL_VERSION=7.94
# Thu, 02 Feb 2023 01:53:16 GMT
ENV DRUPAL_MD5=dae634ea0da005c5c435cfa9a9c5c322
# Thu, 02 Feb 2023 01:53:18 GMT
RUN set -eux; 	curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes
```

-	Layers:
	-	`sha256:e44ba29d168a7f7c9e914f3724614df9e070aa6ef9b9ba5c9004db3c071f403a`  
		Last Modified: Sat, 12 Nov 2022 03:58:16 GMT  
		Size: 2.4 MB (2418788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525864ff6d6c3a1a9ca039e0999c8d05701858671326bac7253a25aa21de91b9`  
		Last Modified: Sat, 12 Nov 2022 06:53:18 GMT  
		Size: 1.6 MB (1575444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09a62104a768e3175677dcac32aa6ba859b0b7917b110ff8fdda7c64447d13f`  
		Last Modified: Sat, 12 Nov 2022 06:53:17 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd62154db22fa402fe200d63a35937ed4a35c102677a20c24eff0fca7ad7981d`  
		Last Modified: Sat, 12 Nov 2022 06:53:17 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba3bc22e5a16f5646f92bce4791c1d1475034d03e1e0086a85dc8ad91262240`  
		Last Modified: Fri, 06 Jan 2023 01:54:10 GMT  
		Size: 10.8 MB (10822210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0957b6ab57a53c6a0f4d54257bb837532a7871abd362caa257016a828934b259`  
		Last Modified: Fri, 06 Jan 2023 01:54:09 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c10d70dcfc9710b119121df318dd983c6c67024a0cd170acd59c33ffe38cdc8a`  
		Last Modified: Fri, 06 Jan 2023 01:54:47 GMT  
		Size: 10.9 MB (10918322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e80624f38ab914356ceece78105754c2da80bb45c0e06f49a1c77e1d2f92244`  
		Last Modified: Fri, 06 Jan 2023 01:54:45 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64b2f41fc1d1c94ac2190b7f0a62457978285281c955cb217e33aacbc3abb46a`  
		Last Modified: Fri, 06 Jan 2023 01:54:45 GMT  
		Size: 18.7 KB (18746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19bad679a479bec4706ef619baed70ce7d639deba3b324e3e49d0c9990534a42`  
		Last Modified: Fri, 06 Jan 2023 01:54:45 GMT  
		Size: 8.7 KB (8684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0e2b4cb226662f22aef7676c92339fb3a11c7f0385ddfc4f0dc070f5accf5d0`  
		Last Modified: Fri, 06 Jan 2023 03:16:45 GMT  
		Size: 1.7 MB (1671362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a4a1bb9afda91aa82039c80dd48d3363345433c17b6a271f14bea89bd381833`  
		Last Modified: Thu, 02 Feb 2023 02:23:13 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f860519fb9a0c6725f2f7080ce56795b1dff1b2da928a65ef6fbe695dc6a5c`  
		Last Modified: Thu, 02 Feb 2023 02:31:31 GMT  
		Size: 3.4 MB (3402498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:7-php8.0-fpm-alpine3.16` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:23a342e8738efbf4cdb35c8c78a75eaafe373a33d01ff3d1c700746836ccf735
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32195925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:727ae458ca134c1ba19dcc60731e59331174b3f29079c834277e34d177c32345`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:13 GMT
ADD file:738e640812bf6089767190a2976ceffc11f3e809be3e2b1ebb43c85ad3199fba in / 
# Fri, 10 Feb 2023 21:24:13 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 02:14:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 11 Feb 2023 02:14:04 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 11 Feb 2023 02:14:05 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 11 Feb 2023 02:14:05 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 11 Feb 2023 02:14:06 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 11 Feb 2023 02:14:06 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 11 Feb 2023 02:14:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 11 Feb 2023 02:14:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 11 Feb 2023 02:50:28 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F 2C16C765DBE54A088130F1BC4B9B5F600B55F3B4
# Sat, 11 Feb 2023 02:50:28 GMT
ENV PHP_VERSION=8.0.27
# Sat, 11 Feb 2023 02:50:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.27.tar.xz.asc
# Sat, 11 Feb 2023 02:50:28 GMT
ENV PHP_SHA256=f942cbfe2f7bacbb8039fb79bbec41c76ea779ac5c8157f21e1e0c1b28a5fc3a
# Sat, 11 Feb 2023 02:50:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 11 Feb 2023 02:50:35 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 11 Feb 2023 02:55:57 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 11 Feb 2023 02:55:57 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 11 Feb 2023 02:55:58 GMT
RUN docker-php-ext-enable sodium
# Sat, 11 Feb 2023 02:55:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 11 Feb 2023 02:55:58 GMT
WORKDIR /var/www/html
# Sat, 11 Feb 2023 02:55:58 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 11 Feb 2023 02:55:58 GMT
STOPSIGNAL SIGQUIT
# Sat, 11 Feb 2023 02:55:59 GMT
EXPOSE 9000
# Sat, 11 Feb 2023 02:55:59 GMT
CMD ["php-fpm"]
# Sat, 11 Feb 2023 07:36:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps
# Sat, 11 Feb 2023 07:36:41 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Sat, 11 Feb 2023 07:38:13 GMT
ENV DRUPAL_VERSION=7.94
# Sat, 11 Feb 2023 07:38:13 GMT
ENV DRUPAL_MD5=dae634ea0da005c5c435cfa9a9c5c322
# Sat, 11 Feb 2023 07:38:14 GMT
RUN set -eux; 	curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes
```

-	Layers:
	-	`sha256:3760b48202b3e349986edb6fe5dd93cd003726b7c345d51f6fc4ace1b46fc2ba`  
		Last Modified: Fri, 10 Feb 2023 21:24:52 GMT  
		Size: 2.7 MB (2709502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24945052da1277802c9acdaf867899c620d73633d9ffdb9141894016d23502a8`  
		Last Modified: Sat, 11 Feb 2023 03:03:59 GMT  
		Size: 1.7 MB (1715610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aab80b0b76f2ca115ba0bf03f9e94151c3b730634d2d9e928f9cda792e65966`  
		Last Modified: Sat, 11 Feb 2023 03:03:58 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3b2459980e300f1a871481cd0f9ef1a474248c2a36c1a7cad8928a45283a0fa`  
		Last Modified: Sat, 11 Feb 2023 03:03:58 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86f5c5f8a23aaffd1e44c4b8381f882b0aec2126c26854adbd6a51c7b0d5c58a`  
		Last Modified: Sat, 11 Feb 2023 03:06:58 GMT  
		Size: 10.8 MB (10822230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b036b24e83cb459c7a40a6697942291079f44c51ec4fffcae0e3f7b546a6fd7`  
		Last Modified: Sat, 11 Feb 2023 03:06:57 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d311bc0be6031609172bd31e4237ba8e6d5139b32fbb7404c06c6a6dbaaf7d00`  
		Last Modified: Sat, 11 Feb 2023 03:07:24 GMT  
		Size: 11.6 MB (11554440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54eb619148538868b958e247f17705577107a574c84f34d87293338748f31759`  
		Last Modified: Sat, 11 Feb 2023 03:07:22 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:796974253ccfa7afbf5cb0b3748e817ac9c8667a8d4d7a006b22a22d96f804ea`  
		Last Modified: Sat, 11 Feb 2023 03:07:22 GMT  
		Size: 18.7 KB (18670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d52d2a9b0ef5b11c358ddaef5cc65914fbf603c8b344dafea019addbe9fe9d`  
		Last Modified: Sat, 11 Feb 2023 03:07:22 GMT  
		Size: 8.7 KB (8678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de97d2166d0ef82df67c75a4fb904f061c847ae61ecc449f6a967b5ec0c106ec`  
		Last Modified: Sat, 11 Feb 2023 07:46:22 GMT  
		Size: 2.0 MB (1959235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ceae3fa2c47e48c2b78af239f57edee4e19e2b6572ab15f233e03ef3369e002`  
		Last Modified: Sat, 11 Feb 2023 07:46:21 GMT  
		Size: 312.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e65c821a99816c875fa72f5b5fb04650ab131b174e8047a3597ab5c109f15553`  
		Last Modified: Sat, 11 Feb 2023 07:48:06 GMT  
		Size: 3.4 MB (3402779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:7-php8.0-fpm-alpine3.16` - linux; 386

```console
$ docker pull drupal@sha256:e051c24bd9c0d63a4d35e8eeef66b91884efa0aaf53ca79b97601d125d1519ca
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.6 MB (33643047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:618a1782d00c1fe8dbcfff9631603b58e95667753ec90d290396aecce2538fd1`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:29 GMT
ADD file:59ac1f8f33f9b9727892b7e45b33f54ef3c20d9d876c49d6a4c057641821d68f in / 
# Fri, 10 Feb 2023 21:24:29 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 23:15:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 10 Feb 2023 23:15:45 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 10 Feb 2023 23:15:45 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 10 Feb 2023 23:15:46 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 10 Feb 2023 23:15:47 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 10 Feb 2023 23:15:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 10 Feb 2023 23:15:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 10 Feb 2023 23:15:50 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 10 Feb 2023 23:53:07 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F 2C16C765DBE54A088130F1BC4B9B5F600B55F3B4
# Fri, 10 Feb 2023 23:53:08 GMT
ENV PHP_VERSION=8.0.27
# Fri, 10 Feb 2023 23:53:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.27.tar.xz.asc
# Fri, 10 Feb 2023 23:53:10 GMT
ENV PHP_SHA256=f942cbfe2f7bacbb8039fb79bbec41c76ea779ac5c8157f21e1e0c1b28a5fc3a
# Fri, 10 Feb 2023 23:53:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 10 Feb 2023 23:53:19 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 11 Feb 2023 00:01:08 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 11 Feb 2023 00:01:10 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 11 Feb 2023 00:01:10 GMT
RUN docker-php-ext-enable sodium
# Sat, 11 Feb 2023 00:01:11 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 11 Feb 2023 00:01:12 GMT
WORKDIR /var/www/html
# Sat, 11 Feb 2023 00:01:13 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 11 Feb 2023 00:01:14 GMT
STOPSIGNAL SIGQUIT
# Sat, 11 Feb 2023 00:01:15 GMT
EXPOSE 9000
# Sat, 11 Feb 2023 00:01:16 GMT
CMD ["php-fpm"]
# Sat, 11 Feb 2023 04:17:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps
# Sat, 11 Feb 2023 04:17:07 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Sat, 11 Feb 2023 04:19:51 GMT
ENV DRUPAL_VERSION=7.94
# Sat, 11 Feb 2023 04:19:51 GMT
ENV DRUPAL_MD5=dae634ea0da005c5c435cfa9a9c5c322
# Sat, 11 Feb 2023 04:19:53 GMT
RUN set -eux; 	curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes
```

-	Layers:
	-	`sha256:0987f51cd58a7d03bc7d6ff0a3a0a843c1a3fefcd41e3c8adc3999ddde7441e8`  
		Last Modified: Fri, 10 Feb 2023 21:25:30 GMT  
		Size: 2.8 MB (2810653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62122267ef44a612330b6b1a4a8c97503160a6be006e9379c086fb229519dbc2`  
		Last Modified: Sat, 11 Feb 2023 00:14:28 GMT  
		Size: 1.8 MB (1820370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9df37a1ab16734bdad148cabca0143c434769c7b6b386dee1ee9e9ddd57a94e2`  
		Last Modified: Sat, 11 Feb 2023 00:14:27 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7b27bfe2f160f32b567c2dbf1cd11c7f543e7b03e63a1bc64a7074bff11ad54`  
		Last Modified: Sat, 11 Feb 2023 00:14:27 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e86ef51e9335e8b18dd95bd045114064385e899f887d9703c86b473cd0abb566`  
		Last Modified: Sat, 11 Feb 2023 00:18:10 GMT  
		Size: 10.8 MB (10821999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a585dab1db53eb0adbfb6bb31fe1dbfcc106b0ac5717dd9c04f9064344826fef`  
		Last Modified: Sat, 11 Feb 2023 00:18:09 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3972f726ccdea596c0427cadd959065c432bf599af655550a36cda1d0c878cc`  
		Last Modified: Sat, 11 Feb 2023 00:18:44 GMT  
		Size: 12.3 MB (12341387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63fe938011a368bb72b80f365b108fd6d8e00eb943e2ed62e9e08b2889ee0028`  
		Last Modified: Sat, 11 Feb 2023 00:18:42 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dc44130c01d7ec7c38300e91fd230b7fe7679439992550c5f1e8b1dd8574fa0`  
		Last Modified: Sat, 11 Feb 2023 00:18:42 GMT  
		Size: 18.6 KB (18556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f78025e02618f7532aaf67d2173dbb7b6cfc5834f72d34f25f0662b3942b13`  
		Last Modified: Sat, 11 Feb 2023 00:18:42 GMT  
		Size: 8.7 KB (8683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dab09af6fadfb53ea35275cba353d846c8f039198a6599981709dd5b29615c3`  
		Last Modified: Sat, 11 Feb 2023 04:34:04 GMT  
		Size: 2.4 MB (2414213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58bc4b9c7c9edaae1f3af60948f57da67ad3c252c037e51a3374e5a078617c4f`  
		Last Modified: Sat, 11 Feb 2023 04:34:03 GMT  
		Size: 313.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d464f10c057d262c62e25ea6887779c88a19f1b84b9de4df2f995806fdc32e81`  
		Last Modified: Sat, 11 Feb 2023 04:36:26 GMT  
		Size: 3.4 MB (3402476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:7-php8.0-fpm-alpine3.16` - linux; ppc64le

```console
$ docker pull drupal@sha256:3d56d2ba0f4e9b13d1367fe15da60336e9be2ab9e5838c67587a2e0f669bdfc9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 MB (34139048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c8a619369ba2e23f9c66e154c82e2bbdc84dbea0432d8828dcceffbaff2a4e`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 12 Nov 2022 04:16:30 GMT
ADD file:6f7965319fe0caaea57086835c0c2212284c6850f33e3c4d522c758e43acbc98 in / 
# Sat, 12 Nov 2022 04:16:31 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 07:14:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 12 Nov 2022 07:14:31 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 12 Nov 2022 07:14:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 12 Nov 2022 07:14:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 12 Nov 2022 07:14:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 12 Nov 2022 07:14:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 12 Nov 2022 07:14:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 12 Nov 2022 07:14:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 12 Nov 2022 07:47:47 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F 2C16C765DBE54A088130F1BC4B9B5F600B55F3B4
# Fri, 06 Jan 2023 01:03:44 GMT
ENV PHP_VERSION=8.0.27
# Fri, 06 Jan 2023 01:03:44 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.27.tar.xz.asc
# Fri, 06 Jan 2023 01:03:45 GMT
ENV PHP_SHA256=f942cbfe2f7bacbb8039fb79bbec41c76ea779ac5c8157f21e1e0c1b28a5fc3a
# Fri, 06 Jan 2023 01:03:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 06 Jan 2023 01:03:54 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 06 Jan 2023 01:14:00 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 06 Jan 2023 01:14:01 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 06 Jan 2023 01:14:03 GMT
RUN docker-php-ext-enable sodium
# Fri, 06 Jan 2023 01:14:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 06 Jan 2023 01:14:04 GMT
WORKDIR /var/www/html
# Fri, 06 Jan 2023 01:14:05 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 06 Jan 2023 01:14:05 GMT
STOPSIGNAL SIGQUIT
# Fri, 06 Jan 2023 01:14:06 GMT
EXPOSE 9000
# Fri, 06 Jan 2023 01:14:06 GMT
CMD ["php-fpm"]
# Fri, 06 Jan 2023 02:22:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps
# Thu, 02 Feb 2023 00:53:14 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 02 Feb 2023 00:58:31 GMT
ENV DRUPAL_VERSION=7.94
# Thu, 02 Feb 2023 00:58:31 GMT
ENV DRUPAL_MD5=dae634ea0da005c5c435cfa9a9c5c322
# Thu, 02 Feb 2023 00:58:35 GMT
RUN set -eux; 	curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes
```

-	Layers:
	-	`sha256:5c3a6ece62351976dfb4b56dc417aebd2a7dbda14ebac2737edd2ab43883553f`  
		Last Modified: Sat, 12 Nov 2022 04:17:14 GMT  
		Size: 2.8 MB (2801551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6194dd51b13c32835b9a76fe58f7580e66a1df8a2acea27095b556cf63b31a98`  
		Last Modified: Sat, 12 Nov 2022 08:27:35 GMT  
		Size: 1.8 MB (1772559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e966c695081973df431189ce4bf6ed44556dad53c642dfb26fa5c0df97e5a7`  
		Last Modified: Sat, 12 Nov 2022 08:27:35 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cdd33a80e474697f7ae3aeeba872662ed64ab312628cb4eaf63bd9cefb1b5a3`  
		Last Modified: Sat, 12 Nov 2022 08:27:35 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce14d37fb691124fa8c601e539b943db0cd6cfcc21d31cb14df921d44b9dfb06`  
		Last Modified: Fri, 06 Jan 2023 01:38:06 GMT  
		Size: 10.8 MB (10822239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:260d78827890a71877fa2b7ff4389136388327897576762d020432a07a414f8b`  
		Last Modified: Fri, 06 Jan 2023 01:38:05 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61181348159f51b96aaf094df5db361f3f3de3f4ca21208f5459755cf5ce9157`  
		Last Modified: Fri, 06 Jan 2023 01:38:46 GMT  
		Size: 13.2 MB (13188937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:607d95f53b72bfc8f2813a0033dd9c66e225da7674c6a3e0c3cab8f325de152a`  
		Last Modified: Fri, 06 Jan 2023 01:38:42 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee5c91d49a72e7b1ed7d23b385ef29d30225ad3f939d6f18ffd8ce9db9904c9`  
		Last Modified: Fri, 06 Jan 2023 01:38:42 GMT  
		Size: 18.7 KB (18742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34088e56207273c7446830dd90489522a9bad8bdd69e9a1803101790fa01b6c0`  
		Last Modified: Fri, 06 Jan 2023 01:38:42 GMT  
		Size: 8.7 KB (8683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0a036246e6d0f134a2c270108e2da5b87b2e093f14775b64052e9e57676085`  
		Last Modified: Fri, 06 Jan 2023 02:50:49 GMT  
		Size: 2.1 MB (2118741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b3d53b5903403ee95e683c5c37e7cb97d54ac3872e73dce3793e14dc8f98a22`  
		Last Modified: Thu, 02 Feb 2023 01:22:39 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:240c4512935972a00178c2d7b770191c4ef3794acee49529102c95c0f8d3a1d3`  
		Last Modified: Thu, 02 Feb 2023 01:30:42 GMT  
		Size: 3.4 MB (3402806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:7-php8.0-fpm-alpine3.16` - linux; s390x

```console
$ docker pull drupal@sha256:48839bee63f3decea8b4784ecea419e3b8f865d58a674fa6a174e46f22122e34
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32597199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53242b191d78f53353ace2416a85350eb91cdade2c2718438aff6ede7db2641f`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 12 Nov 2022 03:42:05 GMT
ADD file:b78ae95cbacd853e398f187adaf3be51d9e301a66de8f7a4b6c60a9733075cb5 in / 
# Sat, 12 Nov 2022 03:42:06 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 05:31:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 12 Nov 2022 05:31:45 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 12 Nov 2022 05:31:46 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 12 Nov 2022 05:31:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 12 Nov 2022 05:31:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 12 Nov 2022 05:31:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 12 Nov 2022 05:31:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 12 Nov 2022 05:31:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 12 Nov 2022 05:59:40 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F 2C16C765DBE54A088130F1BC4B9B5F600B55F3B4
# Fri, 06 Jan 2023 01:31:36 GMT
ENV PHP_VERSION=8.0.27
# Fri, 06 Jan 2023 01:31:36 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.27.tar.xz.asc
# Fri, 06 Jan 2023 01:31:37 GMT
ENV PHP_SHA256=f942cbfe2f7bacbb8039fb79bbec41c76ea779ac5c8157f21e1e0c1b28a5fc3a
# Fri, 06 Jan 2023 01:31:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 06 Jan 2023 01:31:43 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 06 Jan 2023 01:40:41 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 06 Jan 2023 01:40:45 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 06 Jan 2023 01:40:47 GMT
RUN docker-php-ext-enable sodium
# Fri, 06 Jan 2023 01:40:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 06 Jan 2023 01:40:48 GMT
WORKDIR /var/www/html
# Fri, 06 Jan 2023 01:40:50 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 06 Jan 2023 01:40:51 GMT
STOPSIGNAL SIGQUIT
# Fri, 06 Jan 2023 01:40:52 GMT
EXPOSE 9000
# Fri, 06 Jan 2023 01:40:52 GMT
CMD ["php-fpm"]
# Fri, 06 Jan 2023 02:48:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps
# Thu, 02 Feb 2023 00:50:19 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 02 Feb 2023 00:53:52 GMT
ENV DRUPAL_VERSION=7.94
# Thu, 02 Feb 2023 00:53:52 GMT
ENV DRUPAL_MD5=dae634ea0da005c5c435cfa9a9c5c322
# Thu, 02 Feb 2023 00:53:53 GMT
RUN set -eux; 	curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes
```

-	Layers:
	-	`sha256:cff16a5ffe2df97bc1d10b021c5ceb98bdb36a18a1d70395590444ac204a9b2b`  
		Last Modified: Sat, 12 Nov 2022 03:43:06 GMT  
		Size: 2.6 MB (2591126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d900dcf97f987ab1cb475ea526ac6e9c9784703d1e1be1cd7ae1fb777a7d94`  
		Last Modified: Sat, 12 Nov 2022 06:29:44 GMT  
		Size: 1.8 MB (1776146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a0442afc535a74897e967e16b9e816dd275e3f0af102e3215ad2e35350d268d`  
		Last Modified: Sat, 12 Nov 2022 06:29:44 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3645d9671ef8df3e3310d7ba31ed1e48aa39751f695906393ad5b64366d9f5ee`  
		Last Modified: Sat, 12 Nov 2022 06:29:44 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbc3fbd3847ca23a17377a7d423d7c36eac9dd48c9a77315dbcbe99e106e920d`  
		Last Modified: Fri, 06 Jan 2023 02:00:44 GMT  
		Size: 10.8 MB (10822241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3214705b1b572d0297b8f955d223075b4bafff772bfb43a127e63bdd080265e`  
		Last Modified: Fri, 06 Jan 2023 02:00:44 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1afb204eeee97d4f8351d781b9470e5ef59c9d02386bc5777d5b6bd5e490de36`  
		Last Modified: Fri, 06 Jan 2023 02:01:09 GMT  
		Size: 12.0 MB (11983912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a664d7dba5356d88330d6a48da374dd3e04bcf97f8524cb42d773eeab759e2`  
		Last Modified: Fri, 06 Jan 2023 02:01:07 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69d81a8993cebfe2454d46be9864a41fd6e1977877c2cdbdc777c18e1579a523`  
		Last Modified: Fri, 06 Jan 2023 02:01:07 GMT  
		Size: 18.8 KB (18762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ec69cb3ac57c2caaad742abeedb64ae96bcbf6ba329dc43e19bb54de5d15350`  
		Last Modified: Fri, 06 Jan 2023 02:01:07 GMT  
		Size: 8.7 KB (8683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39233c89b5b27a5cb367a272e8f8ce9280795c4b85044dc6efd425c07b6c171e`  
		Last Modified: Fri, 06 Jan 2023 03:10:45 GMT  
		Size: 2.0 MB (1988734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b40bba348119db2df13d0a7a15a451a1ae67501a5ca4009b94ee62701d053b46`  
		Last Modified: Thu, 02 Feb 2023 01:07:44 GMT  
		Size: 318.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:060aa4b6c78cc23fb7377e79705299a06ecf667dc487729806ab0a69565a8495`  
		Last Modified: Thu, 02 Feb 2023 01:10:59 GMT  
		Size: 3.4 MB (3402802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
