## `yourls:fpm-alpine`

```console
$ docker pull yourls@sha256:0f7944ea376d1474592422018779875a4717091998ed3a7b7bf31145742b65ab
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

### `yourls:fpm-alpine` - linux; amd64

```console
$ docker pull yourls@sha256:e4b5a5ec3206052066bcb9ccee9b72bf01cf2c7e84c9794876931e0e4d547629
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34237952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8219e7dccb17816542695ca673411ca6fc8f2ca8ce3fe4733e36f8b4d2f12c55`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 07:06:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 07:06:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 07:06:04 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 07:06:04 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 07:06:05 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 07:06:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 07:06:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 07:06:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 07:50:54 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Tue, 30 Nov 2021 07:50:54 GMT
ENV PHP_VERSION=8.0.13
# Tue, 30 Nov 2021 07:50:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.13.tar.xz.asc
# Tue, 30 Nov 2021 07:50:55 GMT
ENV PHP_SHA256=cd976805ec2e9198417651027dfe16854ba2c2c388151ab9d4d268513d52ed52
# Tue, 30 Nov 2021 07:51:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 30 Nov 2021 07:51:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 30 Nov 2021 08:10:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 30 Nov 2021 08:10:04 GMT
COPY multi:7d7d4b016ee2e2e18720a1a58004eb4d59de798c619f217398cc1066a656bfd0 in /usr/local/bin/ 
# Tue, 30 Nov 2021 08:10:05 GMT
RUN docker-php-ext-enable sodium
# Tue, 30 Nov 2021 08:10:05 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 30 Nov 2021 08:10:06 GMT
WORKDIR /var/www/html
# Tue, 30 Nov 2021 08:10:07 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Tue, 30 Nov 2021 08:10:07 GMT
STOPSIGNAL SIGQUIT
# Tue, 30 Nov 2021 08:10:07 GMT
EXPOSE 9000
# Tue, 30 Nov 2021 08:10:07 GMT
CMD ["php-fpm"]
# Tue, 30 Nov 2021 12:05:58 GMT
LABEL org.opencontainers.image.title=YOURLS
# Tue, 30 Nov 2021 12:05:58 GMT
LABEL org.opencontainers.image.description=Your Own URL Shortener
# Tue, 30 Nov 2021 12:05:58 GMT
LABEL org.opencontainers.image.url=https://yourls.org/
# Tue, 30 Nov 2021 12:05:59 GMT
LABEL org.opencontainers.image.documentation=https://yourls.org/
# Tue, 30 Nov 2021 12:05:59 GMT
LABEL org.opencontainers.image.vendor=YOURLS Org
# Tue, 30 Nov 2021 12:05:59 GMT
LABEL org.opencontainers.image.authors=YOURLS
# Tue, 30 Nov 2021 12:05:59 GMT
LABEL org.opencontainers.image.version=1.8.2
# Tue, 30 Nov 2021 12:06:59 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Tue, 30 Nov 2021 12:07:00 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Tue, 30 Nov 2021 12:07:01 GMT
RUN apk add --no-cache bash
# Tue, 30 Nov 2021 12:07:03 GMT
RUN set -eux;     version="1.8.2";     sha256="6d818622e3ba1d5785c2dbcc088be6890f5675fd4f24a2e3111eda4523bbd7ae";     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${version}.tar.gz";     echo "$sha256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${version}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Tue, 30 Nov 2021 12:07:04 GMT
COPY --chown=www-data:www-datafile:0bcfdfe0566007e7477c55552a1341b82b958e95879a5314f411d2188da2429e in /usr/src/yourls/user/ 
# Tue, 30 Nov 2021 12:07:04 GMT
COPY file:a47a395071c52d8d08402c95253924b09809713039b46033d6f6f75603938896 in /usr/local/bin/ 
# Tue, 30 Nov 2021 12:07:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Nov 2021 12:07:04 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c7da25b2876b1c935b05d7e6efa3e8cd559d031cf30b246d7659ed438726acd`  
		Last Modified: Tue, 30 Nov 2021 09:03:50 GMT  
		Size: 1.7 MB (1709704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc599114627e3bd98e0204b93b161e03065bf9a228bb02ae202469655f12b8d`  
		Last Modified: Tue, 30 Nov 2021 09:03:48 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:927a0b37a45a98d7d74a6d7d1567230eca834fb89417274557de7986d1f39401`  
		Last Modified: Tue, 30 Nov 2021 09:03:48 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8279146e52ed2a974f5b5c9beb9ed70e318d47933f75b90ac98b43fa8d2acb90`  
		Last Modified: Tue, 30 Nov 2021 09:06:07 GMT  
		Size: 10.9 MB (10874437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f188883b50e9cfa0b6c53eade32b6bc7ad6c8fb94f54e367cfb12fb51d2c7463`  
		Last Modified: Tue, 30 Nov 2021 09:06:06 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c64d4e1e1119f9ba45e483f25ed039862777bc357d25d01bfc72b3dc37406b`  
		Last Modified: Tue, 30 Nov 2021 09:06:37 GMT  
		Size: 15.1 MB (15076760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:003d402c413f81aeeaf12e6c9216955bdcead8fa9f5973307adac74dd5380085`  
		Last Modified: Tue, 30 Nov 2021 09:06:35 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6be58cf002ec573fe20946a0095f58f1c8f740c1222cd634c0707398690c32a6`  
		Last Modified: Tue, 30 Nov 2021 09:06:35 GMT  
		Size: 18.2 KB (18207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:944bcdcab902cc1f44eb36d744da209571222ecfb40b2203b5ba4cce191effcc`  
		Last Modified: Tue, 30 Nov 2021 09:06:35 GMT  
		Size: 8.6 KB (8570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb727de379a952e7a0240c2090725aed4af7eab11f5cec17566a3d6c3e53c712`  
		Last Modified: Tue, 30 Nov 2021 12:07:31 GMT  
		Size: 682.7 KB (682679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57b072c37c356a389e7c8b1ab9ad057ae41a03f4f3969828b5f195e8869a6162`  
		Last Modified: Tue, 30 Nov 2021 12:07:28 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e137f6c3e80cd3e814afe8166f05949fb6a63a2f1e7937909ba268e02a7b0b8b`  
		Last Modified: Tue, 30 Nov 2021 12:07:28 GMT  
		Size: 466.4 KB (466436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9b5bda48f02ad962d38b77c49074cb604f74e43d196d1833abd2fa7a0994892`  
		Last Modified: Tue, 30 Nov 2021 12:07:28 GMT  
		Size: 2.6 MB (2574512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df9455970fabb86393baea73571902d73d90ae44878c1bc7df590288f915aca5`  
		Last Modified: Tue, 30 Nov 2021 12:07:28 GMT  
		Size: 2.0 KB (2037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e82563371a38292d201efade51dd97dc63109f38f015192e72855ce2b47fe2ac`  
		Last Modified: Tue, 30 Nov 2021 12:07:28 GMT  
		Size: 1.5 KB (1546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:fpm-alpine` - linux; arm variant v6

```console
$ docker pull yourls@sha256:9112b655d88d41badc2de4d9042f73cad83f3d2b1898ecdb23c67a2aa0a8a7bd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32315329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caef70ec59a25547139bca6d0a8a2a843ccd53bda754e53a0d7c2ada531f132e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 03:20:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 03:20:06 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 03:20:07 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 03:20:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 03:20:10 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 03:20:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 03:20:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 03:20:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 03:40:16 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Tue, 30 Nov 2021 03:40:17 GMT
ENV PHP_VERSION=8.0.13
# Tue, 30 Nov 2021 03:40:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.13.tar.xz.asc
# Tue, 30 Nov 2021 03:40:18 GMT
ENV PHP_SHA256=cd976805ec2e9198417651027dfe16854ba2c2c388151ab9d4d268513d52ed52
# Tue, 30 Nov 2021 03:40:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 30 Nov 2021 03:40:30 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 30 Nov 2021 03:49:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 30 Nov 2021 03:49:53 GMT
COPY multi:7d7d4b016ee2e2e18720a1a58004eb4d59de798c619f217398cc1066a656bfd0 in /usr/local/bin/ 
# Tue, 30 Nov 2021 03:49:56 GMT
RUN docker-php-ext-enable sodium
# Tue, 30 Nov 2021 03:49:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 30 Nov 2021 03:49:57 GMT
WORKDIR /var/www/html
# Tue, 30 Nov 2021 03:49:59 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Tue, 30 Nov 2021 03:49:59 GMT
STOPSIGNAL SIGQUIT
# Tue, 30 Nov 2021 03:50:00 GMT
EXPOSE 9000
# Tue, 30 Nov 2021 03:50:00 GMT
CMD ["php-fpm"]
# Tue, 30 Nov 2021 07:37:55 GMT
LABEL org.opencontainers.image.title=YOURLS
# Tue, 30 Nov 2021 07:37:55 GMT
LABEL org.opencontainers.image.description=Your Own URL Shortener
# Tue, 30 Nov 2021 07:37:56 GMT
LABEL org.opencontainers.image.url=https://yourls.org/
# Tue, 30 Nov 2021 07:37:56 GMT
LABEL org.opencontainers.image.documentation=https://yourls.org/
# Tue, 30 Nov 2021 07:37:57 GMT
LABEL org.opencontainers.image.vendor=YOURLS Org
# Tue, 30 Nov 2021 07:37:57 GMT
LABEL org.opencontainers.image.authors=YOURLS
# Tue, 30 Nov 2021 07:37:57 GMT
LABEL org.opencontainers.image.version=1.8.2
# Tue, 30 Nov 2021 07:39:11 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Tue, 30 Nov 2021 07:39:12 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Tue, 30 Nov 2021 07:39:15 GMT
RUN apk add --no-cache bash
# Tue, 30 Nov 2021 07:39:18 GMT
RUN set -eux;     version="1.8.2";     sha256="6d818622e3ba1d5785c2dbcc088be6890f5675fd4f24a2e3111eda4523bbd7ae";     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${version}.tar.gz";     echo "$sha256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${version}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Tue, 30 Nov 2021 07:39:19 GMT
COPY --chown=www-data:www-datafile:0bcfdfe0566007e7477c55552a1341b82b958e95879a5314f411d2188da2429e in /usr/src/yourls/user/ 
# Tue, 30 Nov 2021 07:39:19 GMT
COPY file:a47a395071c52d8d08402c95253924b09809713039b46033d6f6f75603938896 in /usr/local/bin/ 
# Tue, 30 Nov 2021 07:39:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Nov 2021 07:39:20 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:289be6d758ff0faa38d64732e5736031f2250cbf78d1ca4b32abba4accd6a3fa`  
		Last Modified: Tue, 30 Nov 2021 04:29:36 GMT  
		Size: 1.7 MB (1698826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d0b442a0f679dba79aa838c408cf49916ca26d27e1252e26f3904d7c5b83d6c`  
		Last Modified: Tue, 30 Nov 2021 04:29:33 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fef02b1cade59fbcc24c0ee972dd15d8caa89dda554cdb8aa742de1c6f3d5b7c`  
		Last Modified: Tue, 30 Nov 2021 04:29:33 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c6a247480ef130c8325f9be1fbe1ef2047e23510e25f9d5f225aa541df8f573`  
		Last Modified: Tue, 30 Nov 2021 04:33:02 GMT  
		Size: 10.9 MB (10874432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:262d37c9213794bc797b5852779610048f5977dcbf668151bb98ca8f72ce251c`  
		Last Modified: Tue, 30 Nov 2021 04:32:59 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a37532eefa1deb82e161df2f79889b1358d843171b29c1aeac23b1e050895c4`  
		Last Modified: Tue, 30 Nov 2021 04:33:55 GMT  
		Size: 13.7 MB (13709715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876acb7b0ac81144668793897c2461d25a7792ef3b0966e5b5c8db35d2c39a03`  
		Last Modified: Tue, 30 Nov 2021 04:33:45 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe58f3927080d7d6307681f68274be25b9227d5131615907ec25dcd19e428272`  
		Last Modified: Tue, 30 Nov 2021 04:33:45 GMT  
		Size: 18.2 KB (18203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72c236ec9a62d08919d756e382b75e76b80792d5b6772e56ef7e095a54ba7a0`  
		Last Modified: Tue, 30 Nov 2021 04:33:45 GMT  
		Size: 8.6 KB (8569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccef6195484ac7187c85f39f6ae4f126febcd85c7c89548ab582dae75051a838`  
		Last Modified: Tue, 30 Nov 2021 07:39:53 GMT  
		Size: 336.8 KB (336774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cefeb282c32afce2f8c9fd92096b3f07f7082fe41f4ccc9d7990ba9ad88fbf42`  
		Last Modified: Tue, 30 Nov 2021 07:39:52 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c18635751e73417ede58c128052a685bb2da6d90710c301e49290f77bc56a7c`  
		Last Modified: Tue, 30 Nov 2021 07:39:52 GMT  
		Size: 454.6 KB (454643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9cf1a32e122eecf2a607af212812adf0418d2ef925a51a26099ddc253b14323`  
		Last Modified: Tue, 30 Nov 2021 07:39:54 GMT  
		Size: 2.6 MB (2574510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ff9eeaff0cecb764445186c1f9e9149c2976d7766bbe9650f87c3f777dab14`  
		Last Modified: Tue, 30 Nov 2021 07:39:51 GMT  
		Size: 2.0 KB (2034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de07db08817c19c925f33075ee3e6cc9eaf27e24cbccf3164f1d330a7b4a92ee`  
		Last Modified: Tue, 30 Nov 2021 07:39:51 GMT  
		Size: 1.5 KB (1548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:fpm-alpine` - linux; arm variant v7

```console
$ docker pull yourls@sha256:1b6390ce1b768626048b2462d6ce1ca41998b149a8f2a37b9f81771523a6ed51
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31054363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4781c161f7f31ab0f95a6cc5578fe0063b6d35785d45e8bd42d457e7a125371b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 05:27:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 05:27:16 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 05:27:18 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 05:27:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 05:27:20 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 05:27:20 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 05:27:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 05:27:21 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 05:48:42 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Tue, 30 Nov 2021 05:48:43 GMT
ENV PHP_VERSION=8.0.13
# Tue, 30 Nov 2021 05:48:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.13.tar.xz.asc
# Tue, 30 Nov 2021 05:48:44 GMT
ENV PHP_SHA256=cd976805ec2e9198417651027dfe16854ba2c2c388151ab9d4d268513d52ed52
# Tue, 30 Nov 2021 05:49:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 30 Nov 2021 05:49:02 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 30 Nov 2021 05:57:45 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 30 Nov 2021 05:57:46 GMT
COPY multi:7d7d4b016ee2e2e18720a1a58004eb4d59de798c619f217398cc1066a656bfd0 in /usr/local/bin/ 
# Tue, 30 Nov 2021 05:57:49 GMT
RUN docker-php-ext-enable sodium
# Tue, 30 Nov 2021 05:57:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 30 Nov 2021 05:57:50 GMT
WORKDIR /var/www/html
# Tue, 30 Nov 2021 05:57:51 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Tue, 30 Nov 2021 05:57:52 GMT
STOPSIGNAL SIGQUIT
# Tue, 30 Nov 2021 05:57:52 GMT
EXPOSE 9000
# Tue, 30 Nov 2021 05:57:53 GMT
CMD ["php-fpm"]
# Tue, 30 Nov 2021 16:23:06 GMT
LABEL org.opencontainers.image.title=YOURLS
# Tue, 30 Nov 2021 16:23:07 GMT
LABEL org.opencontainers.image.description=Your Own URL Shortener
# Tue, 30 Nov 2021 16:23:07 GMT
LABEL org.opencontainers.image.url=https://yourls.org/
# Tue, 30 Nov 2021 16:23:08 GMT
LABEL org.opencontainers.image.documentation=https://yourls.org/
# Tue, 30 Nov 2021 16:23:08 GMT
LABEL org.opencontainers.image.vendor=YOURLS Org
# Tue, 30 Nov 2021 16:23:09 GMT
LABEL org.opencontainers.image.authors=YOURLS
# Tue, 30 Nov 2021 16:23:09 GMT
LABEL org.opencontainers.image.version=1.8.2
# Tue, 30 Nov 2021 16:24:19 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Tue, 30 Nov 2021 16:24:21 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Tue, 30 Nov 2021 16:24:23 GMT
RUN apk add --no-cache bash
# Tue, 30 Nov 2021 16:24:26 GMT
RUN set -eux;     version="1.8.2";     sha256="6d818622e3ba1d5785c2dbcc088be6890f5675fd4f24a2e3111eda4523bbd7ae";     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${version}.tar.gz";     echo "$sha256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${version}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Tue, 30 Nov 2021 16:24:27 GMT
COPY --chown=www-data:www-datafile:0bcfdfe0566007e7477c55552a1341b82b958e95879a5314f411d2188da2429e in /usr/src/yourls/user/ 
# Tue, 30 Nov 2021 16:24:28 GMT
COPY file:a47a395071c52d8d08402c95253924b09809713039b46033d6f6f75603938896 in /usr/local/bin/ 
# Tue, 30 Nov 2021 16:24:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Nov 2021 16:24:28 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484fe107211badcebee7c4211e5ed91c7e5212cdd6d7edbb292a63ec60572bdd`  
		Last Modified: Tue, 30 Nov 2021 06:57:00 GMT  
		Size: 1.6 MB (1568802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93353d0a7113f37ba224b9ee296684e49f27c1c9440d3a3c5d310749213da97f`  
		Last Modified: Tue, 30 Nov 2021 06:56:59 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137db50a58959a68358c190d2a143088b82ab25d97cb889876fbc0728e446058`  
		Last Modified: Tue, 30 Nov 2021 06:57:00 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c87492896d37a070cd671acdeddc35fa626c16b56042ccbe125ae386d61b81`  
		Last Modified: Tue, 30 Nov 2021 07:01:07 GMT  
		Size: 10.9 MB (10874434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c951b2578fc00c76c8737687c283fc7850ef1e891c7b7f34e1b9ddbf24699bb`  
		Last Modified: Tue, 30 Nov 2021 07:01:04 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e92b7f731fd73059ae08235b93d3d7d63ab19c500989a37daa4400c950b710f`  
		Last Modified: Tue, 30 Nov 2021 07:01:58 GMT  
		Size: 12.8 MB (12844206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:556a6819e7cb3132b97d67cf20a7c895464b4101e4649cc296b0cf46f77c332b`  
		Last Modified: Tue, 30 Nov 2021 07:01:50 GMT  
		Size: 2.3 KB (2303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59413402f0cb78e1f80439e3030778455a33f86e1b953e836d7f0e91adf4094e`  
		Last Modified: Tue, 30 Nov 2021 07:01:50 GMT  
		Size: 18.2 KB (18208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffe08dab18dec084b093b9958fb18865e8c25423e2049179988a2c09d541eaf1`  
		Last Modified: Tue, 30 Nov 2021 07:01:50 GMT  
		Size: 8.6 KB (8571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f2714ad164a3d5ba4b5dc81bc2f712dfe95048b5618092eaaa550817b3b4f10`  
		Last Modified: Tue, 30 Nov 2021 16:26:09 GMT  
		Size: 307.5 KB (307540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59d44513bc3f915ef5d8444d24d0be5548f76ea088e9ec775948511682d82bf`  
		Last Modified: Tue, 30 Nov 2021 16:26:07 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db04d290d70af175b61444e6322a67f7c6aef97e3804c7931a3a17e18cc8bf73`  
		Last Modified: Tue, 30 Nov 2021 16:26:08 GMT  
		Size: 415.1 KB (415088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cfceb94d1ab78d302106bf4b32562c39b52d29dad68e3db0095d0131faa723f`  
		Last Modified: Tue, 30 Nov 2021 16:26:09 GMT  
		Size: 2.6 MB (2574513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1feb3bfca83d12fe6b6b08cae23427c6c95da38b4657f8d44dbfde1b53f702e`  
		Last Modified: Tue, 30 Nov 2021 16:26:07 GMT  
		Size: 2.0 KB (2039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86ef2a80e4e10c65597130e6333fcba722599fa19e1fcb315ca20aa1f6596337`  
		Last Modified: Tue, 30 Nov 2021 16:26:07 GMT  
		Size: 1.5 KB (1548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull yourls@sha256:30f74815c70e227db9b6fa93b1edacad06910e42eb771b142e1089a9d58a553e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.2 MB (33229084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c34067205ba1b8c65a6ad31a5efae6fec91f078077310edd79ae6bdfd4c5f9d9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 02:50:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 02:50:47 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 02:50:48 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 02:50:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 02:50:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 02:50:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 02:50:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 02:50:53 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 03:15:23 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Tue, 30 Nov 2021 03:15:24 GMT
ENV PHP_VERSION=8.0.13
# Tue, 30 Nov 2021 03:15:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.13.tar.xz.asc
# Tue, 30 Nov 2021 03:15:26 GMT
ENV PHP_SHA256=cd976805ec2e9198417651027dfe16854ba2c2c388151ab9d4d268513d52ed52
# Tue, 30 Nov 2021 03:15:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 30 Nov 2021 03:15:48 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 30 Nov 2021 03:23:08 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 30 Nov 2021 03:23:09 GMT
COPY multi:7d7d4b016ee2e2e18720a1a58004eb4d59de798c619f217398cc1066a656bfd0 in /usr/local/bin/ 
# Tue, 30 Nov 2021 03:23:10 GMT
RUN docker-php-ext-enable sodium
# Tue, 30 Nov 2021 03:23:11 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 30 Nov 2021 03:23:12 GMT
WORKDIR /var/www/html
# Tue, 30 Nov 2021 03:23:13 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Tue, 30 Nov 2021 03:23:14 GMT
STOPSIGNAL SIGQUIT
# Tue, 30 Nov 2021 03:23:15 GMT
EXPOSE 9000
# Tue, 30 Nov 2021 03:23:16 GMT
CMD ["php-fpm"]
# Tue, 30 Nov 2021 07:07:22 GMT
LABEL org.opencontainers.image.title=YOURLS
# Tue, 30 Nov 2021 07:07:23 GMT
LABEL org.opencontainers.image.description=Your Own URL Shortener
# Tue, 30 Nov 2021 07:07:24 GMT
LABEL org.opencontainers.image.url=https://yourls.org/
# Tue, 30 Nov 2021 07:07:25 GMT
LABEL org.opencontainers.image.documentation=https://yourls.org/
# Tue, 30 Nov 2021 07:07:26 GMT
LABEL org.opencontainers.image.vendor=YOURLS Org
# Tue, 30 Nov 2021 07:07:27 GMT
LABEL org.opencontainers.image.authors=YOURLS
# Tue, 30 Nov 2021 07:07:28 GMT
LABEL org.opencontainers.image.version=1.8.2
# Tue, 30 Nov 2021 07:08:00 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Tue, 30 Nov 2021 07:08:01 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Tue, 30 Nov 2021 07:08:03 GMT
RUN apk add --no-cache bash
# Tue, 30 Nov 2021 07:08:05 GMT
RUN set -eux;     version="1.8.2";     sha256="6d818622e3ba1d5785c2dbcc088be6890f5675fd4f24a2e3111eda4523bbd7ae";     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${version}.tar.gz";     echo "$sha256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${version}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Tue, 30 Nov 2021 07:08:06 GMT
COPY --chown=www-data:www-datafile:0bcfdfe0566007e7477c55552a1341b82b958e95879a5314f411d2188da2429e in /usr/src/yourls/user/ 
# Tue, 30 Nov 2021 07:08:07 GMT
COPY file:a47a395071c52d8d08402c95253924b09809713039b46033d6f6f75603938896 in /usr/local/bin/ 
# Tue, 30 Nov 2021 07:08:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Nov 2021 07:08:08 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd720d9f53003155e4cfe3f1974fc0e4d74a622ea8c61cfccb00ee8b842c09b6`  
		Last Modified: Tue, 30 Nov 2021 03:59:34 GMT  
		Size: 1.7 MB (1708308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:680efee530f3c970c3140b358d3dc583ded463f9adbadb737ca64c765cf997ee`  
		Last Modified: Tue, 30 Nov 2021 03:59:33 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643d01251bc949843dbd734a37e7cf28a01af4ea11443738b8b92d17e1e438de`  
		Last Modified: Tue, 30 Nov 2021 03:59:33 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba5d2dd2e9744cc40d2b42c18613e2045ba6b72c922c37c8cda231e7cfcfff09`  
		Last Modified: Tue, 30 Nov 2021 04:02:18 GMT  
		Size: 10.9 MB (10874209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09868cbd5e70feef55023ec2d20dfd178cc2fc4c1b875775b8578dd3758e22f1`  
		Last Modified: Tue, 30 Nov 2021 04:02:16 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53351e4c31dc5141df9db4d7140445d4bd36434a8bd19f404a0a5fe14e64511d`  
		Last Modified: Tue, 30 Nov 2021 04:02:52 GMT  
		Size: 14.5 MB (14499313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:359d93e99a2d2d16a6674242af5c29f150e03fa02dd960efdd018b5240054cc9`  
		Last Modified: Tue, 30 Nov 2021 04:02:50 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c37a5bbbecdfaf97f30eeb1a45f69bf653de48477df4e877fec2a9e17f57419`  
		Last Modified: Tue, 30 Nov 2021 04:02:49 GMT  
		Size: 18.1 KB (18117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc9e8df1efcce2c2808d6442e9f16bb02c6f2c72a3a940c3a90f6a4eeb2a798f`  
		Last Modified: Tue, 30 Nov 2021 04:02:49 GMT  
		Size: 8.6 KB (8571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:220f752124a8e4f06c4a0d6c95fde96e35808a2dacc978107530970352714e22`  
		Last Modified: Tue, 30 Nov 2021 07:08:54 GMT  
		Size: 347.7 KB (347681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62239c088a013a16c8d355d648308b6b292fcba79e2efb0be98ae4cb9433abfd`  
		Last Modified: Tue, 30 Nov 2021 07:08:50 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5976348aff461be3ebed1a595f5e0942beef22689c2d0bbdabefeac9eb8011e9`  
		Last Modified: Tue, 30 Nov 2021 07:08:50 GMT  
		Size: 473.7 KB (473735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c636763ab012d2b925313da94816ebf5b0f64dd7db3bba46d649d9155a87d4a7`  
		Last Modified: Tue, 30 Nov 2021 07:08:51 GMT  
		Size: 2.6 MB (2575552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cbdbfa54363b6561517b50117e1feaa678bbc5286cee5cc6aa11afe6f2b75d6`  
		Last Modified: Tue, 30 Nov 2021 07:08:51 GMT  
		Size: 2.0 KB (2040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:656b943ec4ca294d3d00a0ccc74672e246db7b725365805be5685cb15e41ad78`  
		Last Modified: Tue, 30 Nov 2021 07:08:50 GMT  
		Size: 1.5 KB (1547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:fpm-alpine` - linux; 386

```console
$ docker pull yourls@sha256:2af3fe570f33f2d84a3128a067509578abcb774cf7c7611f0dd76b91a8dc62fb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34692784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eedaa67f8b1e8ae48d1528a7855bcc25d321a7a38acc5b8d2fb12dbb3bed0f4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 24 Nov 2021 20:53:48 GMT
ADD file:b9a17131c440053f2f67e127b447645f25fd7de2d6caca42f569cafab6291855 in / 
# Wed, 24 Nov 2021 20:53:48 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 05:59:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 05:59:06 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 05:59:07 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 05:59:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 05:59:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 05:59:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 05:59:10 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 05:59:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 06:44:18 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Tue, 30 Nov 2021 06:44:19 GMT
ENV PHP_VERSION=8.0.13
# Tue, 30 Nov 2021 06:44:19 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.13.tar.xz.asc
# Tue, 30 Nov 2021 06:44:19 GMT
ENV PHP_SHA256=cd976805ec2e9198417651027dfe16854ba2c2c388151ab9d4d268513d52ed52
# Tue, 30 Nov 2021 06:44:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 30 Nov 2021 06:44:37 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 30 Nov 2021 07:04:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 30 Nov 2021 07:04:55 GMT
COPY multi:7d7d4b016ee2e2e18720a1a58004eb4d59de798c619f217398cc1066a656bfd0 in /usr/local/bin/ 
# Tue, 30 Nov 2021 07:04:57 GMT
RUN docker-php-ext-enable sodium
# Tue, 30 Nov 2021 07:04:57 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 30 Nov 2021 07:04:57 GMT
WORKDIR /var/www/html
# Tue, 30 Nov 2021 07:04:58 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Tue, 30 Nov 2021 07:04:59 GMT
STOPSIGNAL SIGQUIT
# Tue, 30 Nov 2021 07:04:59 GMT
EXPOSE 9000
# Tue, 30 Nov 2021 07:04:59 GMT
CMD ["php-fpm"]
# Tue, 30 Nov 2021 11:01:14 GMT
LABEL org.opencontainers.image.title=YOURLS
# Tue, 30 Nov 2021 11:01:15 GMT
LABEL org.opencontainers.image.description=Your Own URL Shortener
# Tue, 30 Nov 2021 11:01:15 GMT
LABEL org.opencontainers.image.url=https://yourls.org/
# Tue, 30 Nov 2021 11:01:15 GMT
LABEL org.opencontainers.image.documentation=https://yourls.org/
# Tue, 30 Nov 2021 11:01:15 GMT
LABEL org.opencontainers.image.vendor=YOURLS Org
# Tue, 30 Nov 2021 11:01:15 GMT
LABEL org.opencontainers.image.authors=YOURLS
# Tue, 30 Nov 2021 11:01:16 GMT
LABEL org.opencontainers.image.version=1.8.2
# Tue, 30 Nov 2021 11:02:27 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Tue, 30 Nov 2021 11:02:28 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Tue, 30 Nov 2021 11:02:29 GMT
RUN apk add --no-cache bash
# Tue, 30 Nov 2021 11:02:31 GMT
RUN set -eux;     version="1.8.2";     sha256="6d818622e3ba1d5785c2dbcc088be6890f5675fd4f24a2e3111eda4523bbd7ae";     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${version}.tar.gz";     echo "$sha256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${version}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Tue, 30 Nov 2021 11:02:32 GMT
COPY --chown=www-data:www-datafile:0bcfdfe0566007e7477c55552a1341b82b958e95879a5314f411d2188da2429e in /usr/src/yourls/user/ 
# Tue, 30 Nov 2021 11:02:32 GMT
COPY file:a47a395071c52d8d08402c95253924b09809713039b46033d6f6f75603938896 in /usr/local/bin/ 
# Tue, 30 Nov 2021 11:02:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Nov 2021 11:02:32 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:e6889e0d66307a4b916fc844f2dcbc03245c63bc4189dd3e88126d9dcf2f9231`  
		Last Modified: Wed, 24 Nov 2021 20:54:48 GMT  
		Size: 2.8 MB (2827117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14d6acd3b6e4278a7b3ef37d3525813808468237f086215b68594b244dbd1fba`  
		Last Modified: Tue, 30 Nov 2021 08:26:15 GMT  
		Size: 1.8 MB (1810453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc53af545b93519336bed63b8765255ac8280e27c8e3a17c336f92526b3f290`  
		Last Modified: Tue, 30 Nov 2021 08:26:14 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d406b6d62c3d67bec5f638d47d2b1b49c0ee41d80a791a1b90eaec776cf4fd`  
		Last Modified: Tue, 30 Nov 2021 08:26:13 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d123df95de9a3ba60290c45615f21dff954698e79ef5e253db235ba41d8d1c2`  
		Last Modified: Tue, 30 Nov 2021 08:29:53 GMT  
		Size: 10.9 MB (10874428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee5a10462765fcacdbd3d2c18968e7d5506f5f0e6745b0438ebeb60ccbec7e5b`  
		Last Modified: Tue, 30 Nov 2021 08:29:52 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c903faf8dcaad895edb1b385229163879ed82404b121730414686b91043f7e`  
		Last Modified: Tue, 30 Nov 2021 08:30:35 GMT  
		Size: 15.4 MB (15406849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b3e79e53f2bf68a958705590fc46dcfb95425e0313645c6ad7497e6e8cfd83`  
		Last Modified: Tue, 30 Nov 2021 08:30:30 GMT  
		Size: 2.3 KB (2303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bd4edbca43c36e4658f92b1d0fac568fdd44afc759e45cd31764aabe5f5df5e`  
		Last Modified: Tue, 30 Nov 2021 08:30:30 GMT  
		Size: 18.2 KB (18204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32eeccf2c2ad29ed15d933b633ece5ee569a8a814ec52a8e3a8726a41d3d3687`  
		Last Modified: Tue, 30 Nov 2021 08:30:31 GMT  
		Size: 8.6 KB (8570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a9756ec03d48c206514e013fa5182b9a5dc1945823092f00e191f0c04c0635`  
		Last Modified: Tue, 30 Nov 2021 11:03:30 GMT  
		Size: 661.6 KB (661586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbaf03a67e04b0ab6b02eafe7aceace63628c19f9d2f941c7228c2bd6face724`  
		Last Modified: Tue, 30 Nov 2021 11:03:28 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c0ac311d206214095d28f732be862f89f413fdedc70198660df8f145f05cfc3`  
		Last Modified: Tue, 30 Nov 2021 11:03:28 GMT  
		Size: 502.8 KB (502829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:063a3f5884dd6446e68df9a05032c6b671d701724073575f4933c36b2b0386d3`  
		Last Modified: Tue, 30 Nov 2021 11:03:29 GMT  
		Size: 2.6 MB (2574517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2727c10fd2c8cc57478d9ab39c3ddfb33733b3f754cbc33881c939eb2c713da`  
		Last Modified: Tue, 30 Nov 2021 11:03:28 GMT  
		Size: 2.0 KB (2038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c37cd8f856320e10e923f10f8013611fc257a8ccd242aa2213b33cf705c4780f`  
		Last Modified: Tue, 30 Nov 2021 11:03:28 GMT  
		Size: 1.5 KB (1547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:fpm-alpine` - linux; ppc64le

```console
$ docker pull yourls@sha256:ce2a21310e5dee0ebcafec83937734f39c67622542f962b61a37e5d424eac293
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34792687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc90a06213f8e4a70315b70c9c22b736b0d2b96d8a4884d4ae255990a9955fb3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 24 Nov 2021 20:20:16 GMT
ADD file:57115dca2eb707f46b6301e75174e6aa316fb02ac28643b91429b75be51bd8c8 in / 
# Wed, 24 Nov 2021 20:20:20 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 06:02:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 06:03:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 06:03:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 06:03:37 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 06:03:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 06:03:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 06:03:57 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 06:04:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 06:28:05 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Tue, 30 Nov 2021 06:28:07 GMT
ENV PHP_VERSION=8.0.13
# Tue, 30 Nov 2021 06:28:08 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.13.tar.xz.asc
# Tue, 30 Nov 2021 06:28:10 GMT
ENV PHP_SHA256=cd976805ec2e9198417651027dfe16854ba2c2c388151ab9d4d268513d52ed52
# Tue, 30 Nov 2021 06:28:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 30 Nov 2021 06:28:38 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 30 Nov 2021 06:39:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 30 Nov 2021 06:39:07 GMT
COPY multi:7d7d4b016ee2e2e18720a1a58004eb4d59de798c619f217398cc1066a656bfd0 in /usr/local/bin/ 
# Tue, 30 Nov 2021 06:39:15 GMT
RUN docker-php-ext-enable sodium
# Tue, 30 Nov 2021 06:39:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 30 Nov 2021 06:39:22 GMT
WORKDIR /var/www/html
# Tue, 30 Nov 2021 06:39:29 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Tue, 30 Nov 2021 06:39:32 GMT
STOPSIGNAL SIGQUIT
# Tue, 30 Nov 2021 06:39:34 GMT
EXPOSE 9000
# Tue, 30 Nov 2021 06:39:39 GMT
CMD ["php-fpm"]
# Tue, 30 Nov 2021 11:26:22 GMT
LABEL org.opencontainers.image.title=YOURLS
# Tue, 30 Nov 2021 11:26:25 GMT
LABEL org.opencontainers.image.description=Your Own URL Shortener
# Tue, 30 Nov 2021 11:26:28 GMT
LABEL org.opencontainers.image.url=https://yourls.org/
# Tue, 30 Nov 2021 11:26:33 GMT
LABEL org.opencontainers.image.documentation=https://yourls.org/
# Tue, 30 Nov 2021 11:26:36 GMT
LABEL org.opencontainers.image.vendor=YOURLS Org
# Tue, 30 Nov 2021 11:26:38 GMT
LABEL org.opencontainers.image.authors=YOURLS
# Tue, 30 Nov 2021 11:26:40 GMT
LABEL org.opencontainers.image.version=1.8.2
# Tue, 30 Nov 2021 11:27:56 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Tue, 30 Nov 2021 11:28:12 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Tue, 30 Nov 2021 11:28:23 GMT
RUN apk add --no-cache bash
# Tue, 30 Nov 2021 11:28:35 GMT
RUN set -eux;     version="1.8.2";     sha256="6d818622e3ba1d5785c2dbcc088be6890f5675fd4f24a2e3111eda4523bbd7ae";     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${version}.tar.gz";     echo "$sha256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${version}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Tue, 30 Nov 2021 11:28:37 GMT
COPY --chown=www-data:www-datafile:0bcfdfe0566007e7477c55552a1341b82b958e95879a5314f411d2188da2429e in /usr/src/yourls/user/ 
# Tue, 30 Nov 2021 11:28:39 GMT
COPY file:a47a395071c52d8d08402c95253924b09809713039b46033d6f6f75603938896 in /usr/local/bin/ 
# Tue, 30 Nov 2021 11:28:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Nov 2021 11:28:46 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:159b5dcb1717c815c76ff5ea1db730e18e8609c9090238e43282856db9e71f47`  
		Last Modified: Wed, 24 Nov 2021 20:21:14 GMT  
		Size: 2.8 MB (2814780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603762061fb50079a4b6eb13347fd9a84cc1456d628cf781c89924a54bc419c1`  
		Last Modified: Tue, 30 Nov 2021 07:26:39 GMT  
		Size: 1.8 MB (1756276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:645c08440cfaddc2735de2e28697acff0bc71db4cc7242494a44f92c94134e32`  
		Last Modified: Tue, 30 Nov 2021 07:26:39 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5de97a9a329d566f48c2edce253e4ccda6f021041e92326728b7499d13c823b`  
		Last Modified: Tue, 30 Nov 2021 07:26:39 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4479252694b8af910b4be2db9a7d699e99920590df6365ead58741b05f161bef`  
		Last Modified: Tue, 30 Nov 2021 07:29:25 GMT  
		Size: 10.9 MB (10874433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1389516e7bc1f0f56c59866a28554410910aae2e6b7d0539eddd2f7fd64f04ae`  
		Last Modified: Tue, 30 Nov 2021 07:29:24 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29a780112bb524d896186b290192c20d93f5731b6d09b7fb2308697aad36fc66`  
		Last Modified: Tue, 30 Nov 2021 07:30:02 GMT  
		Size: 15.8 MB (15811717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e1b7ffc89aa69ebf9a59156af423be12fddf991bd576a3500ddd414785faf4`  
		Last Modified: Tue, 30 Nov 2021 07:29:58 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653164caf5a0d2d40df063fa50bbc1c9553b46c496893af6408d3cbf81e1f0a3`  
		Last Modified: Tue, 30 Nov 2021 07:29:58 GMT  
		Size: 18.2 KB (18199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa87745ae92ffe2c0deecf3c1461fd5d949f613731ab632a118f1bad0dc2028`  
		Last Modified: Tue, 30 Nov 2021 07:29:58 GMT  
		Size: 8.6 KB (8573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb904133b98d41df8683ea4ecf69703d625a95575905ae058ff3df218e0cb62d`  
		Last Modified: Tue, 30 Nov 2021 11:29:45 GMT  
		Size: 397.5 KB (397468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a4006afaca86c38e0498130d608fc07fe2e9849d95e923f5596f589e4f43d50`  
		Last Modified: Tue, 30 Nov 2021 11:29:42 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a6c180d8a0cdae06b62d45c460551d15ac617e266d3f334178c17897945fa5`  
		Last Modified: Tue, 30 Nov 2021 11:29:42 GMT  
		Size: 528.5 KB (528479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a8fd64471efdda18376a5f90a3b54c6aefb1e48503ee7807e4998408f4250c`  
		Last Modified: Tue, 30 Nov 2021 11:29:43 GMT  
		Size: 2.6 MB (2574520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ccd478377e79418419ec9cea719ee753227d68c3c7e507ea373f1f4ff617e4`  
		Last Modified: Tue, 30 Nov 2021 11:29:42 GMT  
		Size: 2.0 KB (2038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df66f79d496fbb9ba0334a71e7447c808dec3cdc8d43ef054c166fc330a9595e`  
		Last Modified: Tue, 30 Nov 2021 11:29:42 GMT  
		Size: 1.6 KB (1550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:fpm-alpine` - linux; s390x

```console
$ docker pull yourls@sha256:3d89ce0a20c777027c70c4e4009d3d527932ba184fcdbec162844506de39a7f9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 MB (32792591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ae485cb68d66a821c7b0c57e64a1c5de94dd0a3de00e9a6f7b9369da38ae9e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 24 Nov 2021 20:41:23 GMT
ADD file:cd24c711a2ef431b3ff94f9a02bfc42f159bc60de1d0eceecafea4e8af02441d in / 
# Wed, 24 Nov 2021 20:41:23 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 04:50:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 30 Nov 2021 04:50:01 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 30 Nov 2021 04:50:02 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 30 Nov 2021 04:50:02 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Nov 2021 04:50:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 30 Nov 2021 04:50:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 04:50:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Nov 2021 04:50:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Nov 2021 05:03:16 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Tue, 30 Nov 2021 05:03:16 GMT
ENV PHP_VERSION=8.0.13
# Tue, 30 Nov 2021 05:03:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.13.tar.xz.asc
# Tue, 30 Nov 2021 05:03:17 GMT
ENV PHP_SHA256=cd976805ec2e9198417651027dfe16854ba2c2c388151ab9d4d268513d52ed52
# Tue, 30 Nov 2021 05:03:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 30 Nov 2021 05:03:23 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 30 Nov 2021 05:09:10 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 30 Nov 2021 05:09:11 GMT
COPY multi:7d7d4b016ee2e2e18720a1a58004eb4d59de798c619f217398cc1066a656bfd0 in /usr/local/bin/ 
# Tue, 30 Nov 2021 05:09:12 GMT
RUN docker-php-ext-enable sodium
# Tue, 30 Nov 2021 05:09:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 30 Nov 2021 05:09:12 GMT
WORKDIR /var/www/html
# Tue, 30 Nov 2021 05:09:12 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Tue, 30 Nov 2021 05:09:12 GMT
STOPSIGNAL SIGQUIT
# Tue, 30 Nov 2021 05:09:13 GMT
EXPOSE 9000
# Tue, 30 Nov 2021 05:09:13 GMT
CMD ["php-fpm"]
# Tue, 30 Nov 2021 11:55:20 GMT
LABEL org.opencontainers.image.title=YOURLS
# Tue, 30 Nov 2021 11:55:20 GMT
LABEL org.opencontainers.image.description=Your Own URL Shortener
# Tue, 30 Nov 2021 11:55:20 GMT
LABEL org.opencontainers.image.url=https://yourls.org/
# Tue, 30 Nov 2021 11:55:20 GMT
LABEL org.opencontainers.image.documentation=https://yourls.org/
# Tue, 30 Nov 2021 11:55:20 GMT
LABEL org.opencontainers.image.vendor=YOURLS Org
# Tue, 30 Nov 2021 11:55:20 GMT
LABEL org.opencontainers.image.authors=YOURLS
# Tue, 30 Nov 2021 11:55:21 GMT
LABEL org.opencontainers.image.version=1.8.2
# Tue, 30 Nov 2021 11:55:44 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Tue, 30 Nov 2021 11:55:44 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Tue, 30 Nov 2021 11:55:45 GMT
RUN apk add --no-cache bash
# Tue, 30 Nov 2021 11:55:47 GMT
RUN set -eux;     version="1.8.2";     sha256="6d818622e3ba1d5785c2dbcc088be6890f5675fd4f24a2e3111eda4523bbd7ae";     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${version}.tar.gz";     echo "$sha256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${version}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Tue, 30 Nov 2021 11:55:47 GMT
COPY --chown=www-data:www-datafile:0bcfdfe0566007e7477c55552a1341b82b958e95879a5314f411d2188da2429e in /usr/src/yourls/user/ 
# Tue, 30 Nov 2021 11:55:47 GMT
COPY file:a47a395071c52d8d08402c95253924b09809713039b46033d6f6f75603938896 in /usr/local/bin/ 
# Tue, 30 Nov 2021 11:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Nov 2021 11:55:47 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:d6baca485f3d0f7c77221be60fbef5db014a5ef9d8f53db4a310c947c690d189`  
		Last Modified: Wed, 24 Nov 2021 20:42:15 GMT  
		Size: 2.6 MB (2605944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:079fbafa3afc04920b17b503e5d173a44e68fa743eddc7a0eca5e81c7572b8a2`  
		Last Modified: Tue, 30 Nov 2021 08:33:50 GMT  
		Size: 1.8 MB (1771410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00ea1ee8ecbda317521ca15da3d8e45a369d74d9b70a0070ebd705cb9aaf88a2`  
		Last Modified: Tue, 30 Nov 2021 08:33:49 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abad577e66a4ab93646ed4a4aefb0579d577932add0d28121e5aece37cfc08dd`  
		Last Modified: Tue, 30 Nov 2021 08:33:49 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31ea87a2caf3efacfd6163cd632a41aac71423742de7f52d4c0635e61d8c4905`  
		Last Modified: Tue, 30 Nov 2021 08:35:43 GMT  
		Size: 10.9 MB (10874446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37a713981b32d62b43ac0776106c363b80d7ae7dcc8f6bf53fcdcb0b37a58c9c`  
		Last Modified: Tue, 30 Nov 2021 08:35:43 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdad54750e409f4e1d9727c0b28c562da7c8f6e15bfb2761e30354430265208c`  
		Last Modified: Tue, 30 Nov 2021 08:36:03 GMT  
		Size: 14.1 MB (14093937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6268c54bed6cac052c500137573bfff1b75932fdb2aa814b43a13460aec88460`  
		Last Modified: Tue, 30 Nov 2021 08:36:01 GMT  
		Size: 2.3 KB (2301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11bc27e5d85b2c81c6da68cc1d1894ba0af32345ecd8dfa97c9fec15e0cfb536`  
		Last Modified: Tue, 30 Nov 2021 08:36:01 GMT  
		Size: 18.2 KB (18230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c726c8dcbdc78ea1f58bf2c53f60bf190d2d96338b320ca6534ab35ed7c799`  
		Last Modified: Tue, 30 Nov 2021 08:36:01 GMT  
		Size: 8.6 KB (8570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe3d4b536be857bdabbe944982371e2cf743cd7060e4167f3bdd2d4d8a7110b`  
		Last Modified: Tue, 30 Nov 2021 11:56:39 GMT  
		Size: 354.3 KB (354306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5956cc52a3245043928d70de037dabb82e31334beac34e00a5596f92819ba665`  
		Last Modified: Tue, 30 Nov 2021 11:56:38 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c9316be65b728f079558fdfc700636f38a5fdc62f1bcde0a10d7fffe3b2dc63`  
		Last Modified: Tue, 30 Nov 2021 11:56:38 GMT  
		Size: 483.0 KB (482994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a133a0f88fe080817d5c8139cdecf4885094b8ba47b10a08737f75f60241a643`  
		Last Modified: Tue, 30 Nov 2021 11:56:38 GMT  
		Size: 2.6 MB (2574520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86ce6f400f47d9b3794a31bdf9cc45f10958c9b1af0fe925dea4f1334c6c9012`  
		Last Modified: Tue, 30 Nov 2021 11:56:38 GMT  
		Size: 2.0 KB (2037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe417ed2178d195bea23e7074824fdb308799bbcf40a79f754c63a42d503d5e1`  
		Last Modified: Tue, 30 Nov 2021 11:56:38 GMT  
		Size: 1.5 KB (1546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
