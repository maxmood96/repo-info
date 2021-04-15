## `php:7-fpm-alpine3.12`

```console
$ docker pull php@sha256:4901f24ac8e5f704c3f773371239a55d993da0f8ea59db2827b7c02367997e97
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

### `php:7-fpm-alpine3.12` - linux; amd64

```console
$ docker pull php@sha256:d5f2755e513b89fe888992781a1f4ad9c4dfd4183478f283bdec440fad449466
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.8 MB (28831008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:021e4ec11a7f67c5a5dce48635e4c11672a91860a64ee42df2cad83dc55024de`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 00:20:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 Apr 2021 00:20:05 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 15 Apr 2021 00:20:06 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 15 Apr 2021 00:20:07 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 Apr 2021 00:20:08 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 15 Apr 2021 00:30:31 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Thu, 15 Apr 2021 00:30:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Apr 2021 00:30:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Apr 2021 00:30:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 Apr 2021 01:17:15 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 15 Apr 2021 01:17:15 GMT
ENV PHP_VERSION=7.4.16
# Thu, 15 Apr 2021 01:17:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Thu, 15 Apr 2021 01:17:15 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Thu, 15 Apr 2021 01:17:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 15 Apr 2021 01:17:21 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 15 Apr 2021 01:22:04 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 15 Apr 2021 01:22:05 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Thu, 15 Apr 2021 01:22:06 GMT
RUN docker-php-ext-enable sodium
# Thu, 15 Apr 2021 01:22:06 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 Apr 2021 01:22:06 GMT
WORKDIR /var/www/html
# Thu, 15 Apr 2021 01:22:07 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 15 Apr 2021 01:22:07 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Apr 2021 01:22:08 GMT
EXPOSE 9000
# Thu, 15 Apr 2021 01:22:08 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a078c9cf1904c807a7567f1e8845b68ff4d8a3a58f3c1e7263248f7503b7ca4`  
		Last Modified: Thu, 15 Apr 2021 02:17:07 GMT  
		Size: 1.4 MB (1369201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7a9502060da7b7cf055c7a9ead992c8961ece7fc27e7906d742a0a7bdfc033`  
		Last Modified: Thu, 15 Apr 2021 02:17:06 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034a8b17f8de9beb0c46cb63259e8248a28ebd6e0bc538f8f2f28c21b07e98ac`  
		Last Modified: Thu, 15 Apr 2021 02:17:06 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ffc6ccc17221573924ee5e4d3dd8ae18f21087fe8b0dfab7086ede9f22952bf`  
		Last Modified: Thu, 15 Apr 2021 02:20:49 GMT  
		Size: 10.4 MB (10353543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be81d1b29dfa563697387e169adf22c6c5ed52ba5b04ff746e48253b4815d8af`  
		Last Modified: Thu, 15 Apr 2021 02:20:45 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9468462b902c1e3570b5cb7b03394132aebb9f8e2904869bc32b40cfd522d07b`  
		Last Modified: Thu, 15 Apr 2021 02:20:54 GMT  
		Size: 14.3 MB (14278096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10dcf7274378fafcd654365d3f120c0b899333e51794af6b9b49fac4db8c14a4`  
		Last Modified: Thu, 15 Apr 2021 02:20:47 GMT  
		Size: 2.3 KB (2264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2993685766affdf3b6120bea627ca21934ee709751b9ee96dcf3c1e2d7d65031`  
		Last Modified: Thu, 15 Apr 2021 02:20:45 GMT  
		Size: 16.9 KB (16872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0dbdb184a8ce7db61724ddeaf98692b5281429afadda2dcba833cc761e59c53`  
		Last Modified: Thu, 15 Apr 2021 02:20:46 GMT  
		Size: 8.4 KB (8444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:7-fpm-alpine3.12` - linux; arm variant v6

```console
$ docker pull php@sha256:e308d5b03d2126e409d23880575f99c2f1a39157b49ed830f29cd5b1bd2b14ef
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27611103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b0513e5cd623be68f2e168487527c898bda7db89de69b6e44f1a0548c12e940`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:49 GMT
ADD file:82fa6a18d24e3f535c9061d2e111d63fe6d8a27710bb34a17b326e605ff478be in / 
# Wed, 14 Apr 2021 18:49:50 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 01:17:51 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 Apr 2021 01:17:57 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 15 Apr 2021 01:18:02 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 15 Apr 2021 01:18:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 Apr 2021 01:18:10 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 15 Apr 2021 01:23:38 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Thu, 15 Apr 2021 01:23:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Apr 2021 01:23:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Apr 2021 01:23:42 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 Apr 2021 01:50:04 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 15 Apr 2021 01:50:05 GMT
ENV PHP_VERSION=7.4.16
# Thu, 15 Apr 2021 01:50:05 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Thu, 15 Apr 2021 01:50:06 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Thu, 15 Apr 2021 01:50:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 15 Apr 2021 01:50:13 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 15 Apr 2021 01:55:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 15 Apr 2021 01:55:24 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Thu, 15 Apr 2021 01:55:29 GMT
RUN docker-php-ext-enable sodium
# Thu, 15 Apr 2021 01:55:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 Apr 2021 01:55:31 GMT
WORKDIR /var/www/html
# Thu, 15 Apr 2021 01:55:35 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 15 Apr 2021 01:55:36 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Apr 2021 01:55:37 GMT
EXPOSE 9000
# Thu, 15 Apr 2021 01:55:39 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:b452d2916bdfd021add56f1eda6bdea35400671ef07b38316ef82fce92a88fee`  
		Last Modified: Wed, 14 Apr 2021 18:50:38 GMT  
		Size: 2.6 MB (2605253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8cad8c4578c5270a90a55846773ce40754729c5f975e7d1654c5027577be4d`  
		Last Modified: Thu, 15 Apr 2021 02:34:49 GMT  
		Size: 1.3 MB (1332677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95839444ef1cef22cc3ad52750fe13ff8a0a9885523f2a8b0c3cd24f4e484f9`  
		Last Modified: Thu, 15 Apr 2021 02:34:48 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:120021bdf73e23b723057a459e2f4f7bb982a0838bb0cb77140d7b8537d5c154`  
		Last Modified: Thu, 15 Apr 2021 02:34:48 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9434a3c864583e992d60a09d839eb66f9028758f8fc1ccc9e7b7fcaf00445ef`  
		Last Modified: Thu, 15 Apr 2021 02:37:28 GMT  
		Size: 10.4 MB (10353553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8585441799a757ecca848431d6877115da7f16c9b0b1197cc2ba98a9dca052`  
		Last Modified: Thu, 15 Apr 2021 02:37:23 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:909d9428b3ea9b32a6fa9eca382da7750e862a99690988cc1e7146c6a7d9971e`  
		Last Modified: Thu, 15 Apr 2021 02:37:29 GMT  
		Size: 13.3 MB (13289998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaffd65445f04a568e2f9d56ba811504a6cda38cce296d1b3badbcd07527a8d7`  
		Last Modified: Thu, 15 Apr 2021 02:37:23 GMT  
		Size: 2.3 KB (2270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8564abca13db6df1df47e190406a0deaa6c78adae17830357eb59cd2e394e1`  
		Last Modified: Thu, 15 Apr 2021 02:37:22 GMT  
		Size: 16.9 KB (16882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fb98be0326097b294911a665bea0d47ba110444f24bc41de95c7a1d4f406a4c`  
		Last Modified: Thu, 15 Apr 2021 02:37:22 GMT  
		Size: 8.4 KB (8444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:7-fpm-alpine3.12` - linux; arm variant v7

```console
$ docker pull php@sha256:136105e0134be5815738b043fb9f7234ee07fc7ef3741c33c4c17cdb6c998697
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 MB (26467236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f44df34fabfc5572bbf00a7037bc91a09f5027bc56236ac1c1913fdd681b53b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:50 GMT
ADD file:d844cc7b5e00fb62be39d903a2fb4a08f700e75112c8eef1f31101e846ed010d in / 
# Wed, 14 Apr 2021 18:57:52 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 02:20:59 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 Apr 2021 02:21:07 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 15 Apr 2021 02:21:23 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 15 Apr 2021 02:21:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 Apr 2021 02:22:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 15 Apr 2021 02:29:09 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Thu, 15 Apr 2021 02:29:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Apr 2021 02:29:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Apr 2021 02:29:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 Apr 2021 02:57:34 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 15 Apr 2021 02:57:35 GMT
ENV PHP_VERSION=7.4.16
# Thu, 15 Apr 2021 02:57:37 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Thu, 15 Apr 2021 02:57:39 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Thu, 15 Apr 2021 02:57:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 15 Apr 2021 02:57:52 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 15 Apr 2021 03:02:16 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 15 Apr 2021 03:02:18 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Thu, 15 Apr 2021 03:02:22 GMT
RUN docker-php-ext-enable sodium
# Thu, 15 Apr 2021 03:02:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 Apr 2021 03:02:24 GMT
WORKDIR /var/www/html
# Thu, 15 Apr 2021 03:02:26 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 15 Apr 2021 03:02:27 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Apr 2021 03:02:28 GMT
EXPOSE 9000
# Thu, 15 Apr 2021 03:02:30 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:420c7481a3a76d5d12df768d2745ddbe40357df0af780c756a5a7d1f2a43d288`  
		Last Modified: Wed, 14 Apr 2021 18:58:46 GMT  
		Size: 2.4 MB (2409178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7db4e41df07c72800bc526ed5085dfb56b791a44201a4aeb443f6c5cde89b7d2`  
		Last Modified: Thu, 15 Apr 2021 03:40:15 GMT  
		Size: 1.2 MB (1233448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e065d0af38976f008e1bbbfcac343cd709823a229184ee5b77f41b3b5b8cc0a`  
		Last Modified: Thu, 15 Apr 2021 03:40:14 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff291ee936c5a1a0de1ecba3948d82473925b62b72ef884cf505c01ece3ee207`  
		Last Modified: Thu, 15 Apr 2021 03:40:15 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a939ff330b3a3fc7a6c9505ebf3c2f12cb3baa80872b0e58deae7de713c86654`  
		Last Modified: Thu, 15 Apr 2021 03:42:44 GMT  
		Size: 10.4 MB (10353544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b858191470f795b8573ddd382b123fee90218084c2e25b59c79090d1df335cd0`  
		Last Modified: Thu, 15 Apr 2021 03:42:40 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22485e1c8369e3cbc2fcfb50779648b5f2df74ef90be204701740f82a73e3e04`  
		Last Modified: Thu, 15 Apr 2021 03:42:44 GMT  
		Size: 12.4 MB (12441465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e97e507e49142ed636033668cb62cdb3ac85b07beb9c00c5619813b7a88933e`  
		Last Modified: Thu, 15 Apr 2021 03:42:40 GMT  
		Size: 2.3 KB (2267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba19df156e727ff5d7e1139125dafabef6b1db203f5c01bd0eb4440a84d0e0a`  
		Last Modified: Thu, 15 Apr 2021 03:42:40 GMT  
		Size: 16.9 KB (16868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be59c42d970c3b6a280b423b3115d953994e43f59dbe6bea65f99e5f9d4cd90c`  
		Last Modified: Thu, 15 Apr 2021 03:42:40 GMT  
		Size: 8.4 KB (8445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:7-fpm-alpine3.12` - linux; arm64 variant v8

```console
$ docker pull php@sha256:99b0c156c4c417fc37f1f805cf1eee214ee6cee53c176535e9d84bc719080712
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28545660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd10f1e97873615b6f2869b3b90601489d20f655b86db9bc2a64aef9422718f6`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:54 GMT
ADD file:3db1e10ac5ebf1cb34939eff736f1384f7d3b17355758cec361489fa7a7e19ca in / 
# Wed, 14 Apr 2021 18:42:55 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 00:40:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 Apr 2021 00:40:19 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 15 Apr 2021 00:40:25 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 15 Apr 2021 00:40:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 Apr 2021 00:40:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 15 Apr 2021 00:46:43 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Thu, 15 Apr 2021 00:46:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Apr 2021 00:46:44 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Apr 2021 00:46:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 Apr 2021 01:17:16 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 15 Apr 2021 01:17:18 GMT
ENV PHP_VERSION=7.4.16
# Thu, 15 Apr 2021 01:17:19 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Thu, 15 Apr 2021 01:17:21 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Thu, 15 Apr 2021 01:17:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 15 Apr 2021 01:17:29 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 15 Apr 2021 01:22:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 15 Apr 2021 01:22:27 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Thu, 15 Apr 2021 01:22:30 GMT
RUN docker-php-ext-enable sodium
# Thu, 15 Apr 2021 01:22:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 Apr 2021 01:22:31 GMT
WORKDIR /var/www/html
# Thu, 15 Apr 2021 01:22:33 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 15 Apr 2021 01:22:34 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Apr 2021 01:22:35 GMT
EXPOSE 9000
# Thu, 15 Apr 2021 01:22:36 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:d2f70382dc9a1658ea3491d7ab4439c22087e426c00e3eb7daf825b83be4ba9c`  
		Last Modified: Wed, 14 Apr 2021 18:43:55 GMT  
		Size: 2.7 MB (2710694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75454ef1d96df8081b852e85f0c79167a62d10ee23634b86540a521a9262b3ad`  
		Last Modified: Thu, 15 Apr 2021 02:00:46 GMT  
		Size: 1.4 MB (1371474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7079a2c7ac37c396fe3f4a33ac65c7df4b7d75c46cc1af7f6b4a6f8c37b780d3`  
		Last Modified: Thu, 15 Apr 2021 02:00:45 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f873453c05b9b2d26344f14143ca10c58c99fb398ebc906016e20ed8b9d20b8`  
		Last Modified: Thu, 15 Apr 2021 02:00:44 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3dcd16bc20b750e8ef454e4ed93a76b19dc5e9e728564b54cb89d26bd3e9ff`  
		Last Modified: Thu, 15 Apr 2021 02:02:54 GMT  
		Size: 10.4 MB (10353539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:615194ef7f7f730254abd52ea0d817a2fdddbfd1423e18acdeef3800bbc3a9b0`  
		Last Modified: Thu, 15 Apr 2021 02:02:52 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c4ecba529104faad6776845085a9a42a51f6adda41064d5e3f5172c2293ced`  
		Last Modified: Thu, 15 Apr 2021 02:02:56 GMT  
		Size: 14.1 MB (14080349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bce13df7bb282b0a8cb62026cca82b181ad4abce9df9f74e0a46e27426c74ad`  
		Last Modified: Thu, 15 Apr 2021 02:02:52 GMT  
		Size: 2.3 KB (2265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38836915443e7fd4837ba6aa8104c76031c81fcda023ba6e772114784ce07bf`  
		Last Modified: Thu, 15 Apr 2021 02:02:52 GMT  
		Size: 16.9 KB (16871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d7c332fdb38890bd564b4368d2256016f8a743883a7c2c73c4b4c78ad31268c`  
		Last Modified: Thu, 15 Apr 2021 02:02:52 GMT  
		Size: 8.4 KB (8445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:7-fpm-alpine3.12` - linux; 386

```console
$ docker pull php@sha256:12c5c067c9a212eb52922a24caecab8eb7e9caec6913151dc818d9560f131f85
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.3 MB (29277764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2767316f1b2597a87b4223b2989409bb47c6e6c84e349f234a90978a3c1f74ef`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 31 Mar 2021 17:43:08 GMT
ADD file:053c3a6154e80758106cbf0fec936c3b41dabf24a9f5eda36416caa90556810c in / 
# Wed, 31 Mar 2021 17:43:09 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 03:02:53 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 01 Apr 2021 03:02:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 01 Apr 2021 03:02:56 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 01 Apr 2021 03:02:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 01 Apr 2021 03:02:57 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 01 Apr 2021 03:08:53 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Thu, 01 Apr 2021 03:08:53 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 01 Apr 2021 03:08:53 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 01 Apr 2021 03:08:53 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 01 Apr 2021 03:41:58 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 01 Apr 2021 03:41:59 GMT
ENV PHP_VERSION=7.4.16
# Thu, 01 Apr 2021 03:41:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Thu, 01 Apr 2021 03:41:59 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Thu, 01 Apr 2021 03:42:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 01 Apr 2021 03:42:14 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 01 Apr 2021 03:47:44 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 01 Apr 2021 03:47:45 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Thu, 01 Apr 2021 03:47:46 GMT
RUN docker-php-ext-enable sodium
# Thu, 01 Apr 2021 03:47:47 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 01 Apr 2021 03:47:47 GMT
WORKDIR /var/www/html
# Thu, 01 Apr 2021 03:47:48 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 01 Apr 2021 03:47:48 GMT
STOPSIGNAL SIGQUIT
# Thu, 01 Apr 2021 03:47:48 GMT
EXPOSE 9000
# Thu, 01 Apr 2021 03:47:49 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:8eca83e4805e4c5e7b071425a4603bc4b02885b817aa7c1bba9605bd2cb9125a`  
		Last Modified: Wed, 31 Mar 2021 17:44:26 GMT  
		Size: 2.8 MB (2794977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca80016dbb16befd5aa82b9149d37c6577450d173d66fb0b638d8377822407d4`  
		Last Modified: Thu, 01 Apr 2021 04:43:07 GMT  
		Size: 1.4 MB (1439817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fafae2eed22e4f4b7c690e28391ddf1a273067a5b12e3c4f32827774dd5bdc15`  
		Last Modified: Thu, 01 Apr 2021 04:43:05 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db45b483048b084820a30ce08c132efa2cbc029b60de461a4e5b5e897e48299f`  
		Last Modified: Thu, 01 Apr 2021 04:43:05 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd522b756a34a4f23f5e58aa3a7fb058e647327976d78979811b8690cb52aa3d`  
		Last Modified: Thu, 01 Apr 2021 04:47:04 GMT  
		Size: 10.4 MB (10353540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e33ac93c2e74a9305906df1452e23ccbdedd01b434bf971eb656ebba4a900e`  
		Last Modified: Thu, 01 Apr 2021 04:47:01 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d09892df0ea0526d8eb917de89f0792a51f9cdbc3a12cc7e963502829ff3ff7`  
		Last Modified: Thu, 01 Apr 2021 04:47:05 GMT  
		Size: 14.7 MB (14659820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5297583fe2f221442c4c57897a419a9c85b6c341b9e0bf04d7be94506a63c3f6`  
		Last Modified: Thu, 01 Apr 2021 04:47:01 GMT  
		Size: 2.3 KB (2265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:229bbbd1ee17cd6dd3814139f1c5f98af229bbdfc7be7b0c046be42efa57f19f`  
		Last Modified: Thu, 01 Apr 2021 04:47:01 GMT  
		Size: 16.9 KB (16877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a671707bff31e85da3249e0c18b47ee85dfaeaee71844f904a0dfb7c1c013c2`  
		Last Modified: Thu, 01 Apr 2021 04:47:01 GMT  
		Size: 8.4 KB (8443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:7-fpm-alpine3.12` - linux; ppc64le

```console
$ docker pull php@sha256:6c85e406ba3eadb4295fdb32ec67e6f581ce0c088d180bfa5b2c75c8ad4a31dd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.9 MB (29859669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc9e787afd8b920087cfb7d777ec141b7e7e43228a07d415ff01330e5d42b57b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 14 Apr 2021 19:31:22 GMT
ADD file:f8b081207f6d35f8ebd06aa471e350644151d183801f678def586d8f37e81366 in / 
# Wed, 14 Apr 2021 19:31:29 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:32:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 14 Apr 2021 20:32:25 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 14 Apr 2021 20:32:39 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 14 Apr 2021 20:32:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 14 Apr 2021 20:32:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 14 Apr 2021 20:38:56 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Wed, 14 Apr 2021 20:39:02 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 14 Apr 2021 20:39:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 14 Apr 2021 20:39:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 14 Apr 2021 21:11:15 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Wed, 14 Apr 2021 21:11:18 GMT
ENV PHP_VERSION=7.4.16
# Wed, 14 Apr 2021 21:11:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Wed, 14 Apr 2021 21:11:30 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Wed, 14 Apr 2021 21:11:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 14 Apr 2021 21:11:52 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 14 Apr 2021 21:15:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 14 Apr 2021 21:16:07 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Wed, 14 Apr 2021 21:16:20 GMT
RUN docker-php-ext-enable sodium
# Wed, 14 Apr 2021 21:16:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 14 Apr 2021 21:16:33 GMT
WORKDIR /var/www/html
# Wed, 14 Apr 2021 21:16:48 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Wed, 14 Apr 2021 21:16:55 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Apr 2021 21:17:05 GMT
EXPOSE 9000
# Wed, 14 Apr 2021 21:17:12 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:45707b9629c4ab8c6046680737229218fe844f38d08e5458b24605e1dbfd2709`  
		Last Modified: Wed, 14 Apr 2021 19:32:50 GMT  
		Size: 2.8 MB (2806750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50d21396f5076961d8b40ffe92797fa964e2f354badb992076ec2e8c341face0`  
		Last Modified: Wed, 14 Apr 2021 22:02:22 GMT  
		Size: 1.4 MB (1409857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d81f1a419911a96a9173df743dcaa56618dc4f880e30a2d57b6571cd744410`  
		Last Modified: Wed, 14 Apr 2021 22:02:21 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30aa25148a768989691435c0455a034cef0f452dba09512d908f008456da8cb`  
		Last Modified: Wed, 14 Apr 2021 22:02:21 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b576e21a08681de977d713e49f025c8612a369912f02ac80423a2b98eb0f303`  
		Last Modified: Wed, 14 Apr 2021 22:05:21 GMT  
		Size: 10.4 MB (10353559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb27ea40f70e3c28c3536ffd194160f44e0f9d98049f6396835466aef18612b7`  
		Last Modified: Wed, 14 Apr 2021 22:05:16 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a83476839bc6ea2168faccc3f976bb7e423472f86fced2f18206a103f34830e8`  
		Last Modified: Wed, 14 Apr 2021 22:05:20 GMT  
		Size: 15.3 MB (15259840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dde30bef5559e0fbd2fd17887a2472c85cfcb7e1d255871aa56d833c611f930`  
		Last Modified: Wed, 14 Apr 2021 22:05:16 GMT  
		Size: 2.3 KB (2267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eeec1e34c670c52da8d3e53c79a46861ffa15dd7aabd279dbefc5c2f1022fcc`  
		Last Modified: Wed, 14 Apr 2021 22:05:16 GMT  
		Size: 16.9 KB (16925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e61c11dd39a9dea1963d6cae6e7e175cc069490e8b73aa9d6ec47928edcd7688`  
		Last Modified: Wed, 14 Apr 2021 22:05:16 GMT  
		Size: 8.4 KB (8447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:7-fpm-alpine3.12` - linux; s390x

```console
$ docker pull php@sha256:2889dcb7e7651667cf859f75b24e8cfd801c0ba2d03ab0fe3ad4f1a1f550611a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.2 MB (28151336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:633a0044e386565eed1db0410ab6c2a2077a45cfcdddb6112468dfa6173f3269`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 14 Apr 2021 18:41:42 GMT
ADD file:c73a5ff435939cdc9d621ee9dc2aa5a54a5f5e0241caae8dc948c03c423d9fef in / 
# Wed, 14 Apr 2021 18:41:42 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:11:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 14 Apr 2021 19:11:10 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 14 Apr 2021 19:11:11 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 14 Apr 2021 19:11:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 14 Apr 2021 19:11:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 14 Apr 2021 19:14:47 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Wed, 14 Apr 2021 19:14:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 14 Apr 2021 19:14:47 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 14 Apr 2021 19:14:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 14 Apr 2021 19:33:39 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Wed, 14 Apr 2021 19:33:40 GMT
ENV PHP_VERSION=7.4.16
# Wed, 14 Apr 2021 19:33:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.16.tar.xz.asc
# Wed, 14 Apr 2021 19:33:40 GMT
ENV PHP_SHA256=1c16cefaf88ded4c92eed6a8a41eb682bb2ef42429deb55f1c4ba159053fb98b
# Wed, 14 Apr 2021 19:33:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 14 Apr 2021 19:33:43 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 14 Apr 2021 19:36:25 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 14 Apr 2021 19:36:26 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Wed, 14 Apr 2021 19:36:27 GMT
RUN docker-php-ext-enable sodium
# Wed, 14 Apr 2021 19:36:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 14 Apr 2021 19:36:27 GMT
WORKDIR /var/www/html
# Wed, 14 Apr 2021 19:36:28 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Wed, 14 Apr 2021 19:36:28 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Apr 2021 19:36:28 GMT
EXPOSE 9000
# Wed, 14 Apr 2021 19:36:29 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:27efec644c4207cbc4d1400f84f3402937aab5ce72489976148896e42a219820`  
		Last Modified: Wed, 14 Apr 2021 18:42:24 GMT  
		Size: 2.6 MB (2568428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71c20a3ecae8cc7ea51ca293c87d17bf04cefeb04d12ffb9652a9766be3f8416`  
		Last Modified: Wed, 14 Apr 2021 20:02:02 GMT  
		Size: 1.4 MB (1382747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccc1d01c306c098f90edda1998ec952dd13e38675b3fed5e7b73efb281d45223`  
		Last Modified: Wed, 14 Apr 2021 20:02:01 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41d0bbd337de43d24bc0a30a3e902ab2dc6a3a37d4c24d543cf4b39987ecb649`  
		Last Modified: Wed, 14 Apr 2021 20:02:01 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b61fe45e7ad8e571abd53eab97454969cfb74dfb77e9e0fc1cce54d5f18b9803`  
		Last Modified: Wed, 14 Apr 2021 20:04:24 GMT  
		Size: 10.4 MB (10353549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e77207303b9a38091026114cf8fb4f92d8350e93a8950cd8e32c56273d146bf`  
		Last Modified: Wed, 14 Apr 2021 20:04:22 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66735203b979dc6dcf6f1974a1ab60d98fe57127e46055c42d0173aa37b3cba4`  
		Last Modified: Wed, 14 Apr 2021 20:04:24 GMT  
		Size: 13.8 MB (13816972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b989b35e921300faafad99c53dafb930a0d9c9defec70a06d1e28ad5cc6336bc`  
		Last Modified: Wed, 14 Apr 2021 20:04:22 GMT  
		Size: 2.3 KB (2264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed77d12cdd4b34088138a3f621b02a1a1781eebc779103c619c8bcb6e2181ab2`  
		Last Modified: Wed, 14 Apr 2021 20:04:22 GMT  
		Size: 16.9 KB (16909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6018741b6809050ab69677cc866c17bf85729f00749b374dd377e6eef655556`  
		Last Modified: Wed, 14 Apr 2021 20:04:22 GMT  
		Size: 8.4 KB (8443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
