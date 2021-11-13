## `yourls:1-fpm-alpine`

```console
$ docker pull yourls@sha256:8f1969d78e56e6ff4fe39237218f820004a57463bce4f470b3c45020aebee1ca
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

### `yourls:1-fpm-alpine` - linux; amd64

```console
$ docker pull yourls@sha256:65b35e20253f98096715c49554bca554029acd8019c8471c45bffe877c186b7c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 MB (34082513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b29fa20379f6512d304cdd969134f6b7ed45746f2ba0a3f4e4eb2b11fc526c8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 07:48:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 13 Nov 2021 07:48:45 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 13 Nov 2021 07:48:47 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 13 Nov 2021 07:48:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 13 Nov 2021 07:48:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 13 Nov 2021 07:48:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 13 Nov 2021 07:48:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 13 Nov 2021 07:48:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 13 Nov 2021 08:32:27 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Sat, 13 Nov 2021 08:32:27 GMT
ENV PHP_VERSION=8.0.12
# Sat, 13 Nov 2021 08:32:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.12.tar.xz.asc
# Sat, 13 Nov 2021 08:32:28 GMT
ENV PHP_SHA256=a501017b3b0fd3023223ea25d98e87369b782f8a82310c4033d7ea6a989fea0a
# Sat, 13 Nov 2021 08:32:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 13 Nov 2021 08:32:43 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 13 Nov 2021 08:52:04 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 13 Nov 2021 08:52:04 GMT
COPY multi:7d7d4b016ee2e2e18720a1a58004eb4d59de798c619f217398cc1066a656bfd0 in /usr/local/bin/ 
# Sat, 13 Nov 2021 08:52:06 GMT
RUN docker-php-ext-enable sodium
# Sat, 13 Nov 2021 08:52:06 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 13 Nov 2021 08:52:06 GMT
WORKDIR /var/www/html
# Sat, 13 Nov 2021 08:52:07 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Sat, 13 Nov 2021 08:52:07 GMT
STOPSIGNAL SIGQUIT
# Sat, 13 Nov 2021 08:52:07 GMT
EXPOSE 9000
# Sat, 13 Nov 2021 08:52:07 GMT
CMD ["php-fpm"]
# Sat, 13 Nov 2021 15:29:32 GMT
LABEL org.opencontainers.image.title=YOURLS
# Sat, 13 Nov 2021 15:29:32 GMT
LABEL org.opencontainers.image.description=Your Own URL Shortener
# Sat, 13 Nov 2021 15:29:32 GMT
LABEL org.opencontainers.image.url=https://yourls.org/
# Sat, 13 Nov 2021 15:29:32 GMT
LABEL org.opencontainers.image.documentation=https://yourls.org/
# Sat, 13 Nov 2021 15:29:32 GMT
LABEL org.opencontainers.image.vendor=YOURLS Org
# Sat, 13 Nov 2021 15:29:32 GMT
LABEL org.opencontainers.image.authors=YOURLS
# Sat, 13 Nov 2021 15:29:33 GMT
LABEL org.opencontainers.image.version=1.8.2
# Sat, 13 Nov 2021 15:30:34 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Sat, 13 Nov 2021 15:30:35 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Sat, 13 Nov 2021 15:30:36 GMT
RUN apk add --no-cache bash
# Sat, 13 Nov 2021 15:30:38 GMT
RUN set -eux;     version="1.8.2";     sha256="6d818622e3ba1d5785c2dbcc088be6890f5675fd4f24a2e3111eda4523bbd7ae";     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${version}.tar.gz";     echo "$sha256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${version}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Sat, 13 Nov 2021 15:30:38 GMT
COPY --chown=www-data:www-datafile:0bcfdfe0566007e7477c55552a1341b82b958e95879a5314f411d2188da2429e in /usr/src/yourls/user/ 
# Sat, 13 Nov 2021 15:30:38 GMT
COPY file:a47a395071c52d8d08402c95253924b09809713039b46033d6f6f75603938896 in /usr/local/bin/ 
# Sat, 13 Nov 2021 15:30:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Nov 2021 15:30:38 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b67f99012ff9aa7245baebc28963e44f53cc1832fcfaec246f78b5e7e861fbe6`  
		Last Modified: Sat, 13 Nov 2021 10:43:29 GMT  
		Size: 1.7 MB (1712224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db81da314e0b3e7be6d4c80bd6a2cdc1d7f66d6fffc8334a527f6b6e20fca340`  
		Last Modified: Sat, 13 Nov 2021 10:43:29 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5646ac679ebe77089fb6446f9911a66ae64db7d5b774d356b04c1c911ca0a081`  
		Last Modified: Sat, 13 Nov 2021 10:43:29 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:339babaad8a9f5a1efc47b491b0e5b5206107bdbe4e4465f117aff68a7437aaa`  
		Last Modified: Sat, 13 Nov 2021 10:45:09 GMT  
		Size: 10.7 MB (10734119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b63bba88ae74da75da44158b0572d2b056caa5624702483b452c136a4877ee60`  
		Last Modified: Sat, 13 Nov 2021 10:45:08 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c3d4fc883404e7da128cf4f1c454bca4a8cee7314eb348d03305fb08ec864c`  
		Last Modified: Sat, 13 Nov 2021 10:46:01 GMT  
		Size: 15.1 MB (15057221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577a1c92e8071c5151801da4711b72ebab22eb46b834cd18590ada0a394d2414`  
		Last Modified: Sat, 13 Nov 2021 10:45:58 GMT  
		Size: 2.3 KB (2303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:965e47da3446f286d3a7f8d9005f6883ad2790a31c5deafc7df71a4f18871ae3`  
		Last Modified: Sat, 13 Nov 2021 10:45:59 GMT  
		Size: 18.2 KB (18193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f65a24df440a1a329adec1580146442492b4fa264270c7fa95efda49dd295576`  
		Last Modified: Sat, 13 Nov 2021 10:45:58 GMT  
		Size: 8.6 KB (8571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01abd7bfafcc03989a83a9d142d954dcf12bd9cedfa14a5e81462bab66e6fbbe`  
		Last Modified: Sat, 13 Nov 2021 15:31:08 GMT  
		Size: 680.6 KB (680556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:714722649d78d006a3865615560424d79fc0a7c3ec98a50df4353f57d2b7bf97`  
		Last Modified: Sat, 13 Nov 2021 15:31:05 GMT  
		Size: 323.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b3c2185fc1b059a660f0380969727e7e58501ba74e95a777f4666daf64cd571`  
		Last Modified: Sat, 13 Nov 2021 15:31:06 GMT  
		Size: 465.9 KB (465909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:256239c52cc5cf978bfa618abe1372c7d24f72039798e206415cf6bf136be18d`  
		Last Modified: Sat, 13 Nov 2021 15:31:06 GMT  
		Size: 2.6 MB (2574515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19252cd73b3b5ff04e45d145933302ce52cf2973352854bf2ac8958d868815a9`  
		Last Modified: Sat, 13 Nov 2021 15:31:05 GMT  
		Size: 2.0 KB (2034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e465e2cb8c45464c0bf0b6a7bbe431a516557a6d6f6a45517402c245be731cbf`  
		Last Modified: Sat, 13 Nov 2021 15:31:05 GMT  
		Size: 1.5 KB (1543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1-fpm-alpine` - linux; arm variant v6

```console
$ docker pull yourls@sha256:c540dd2bc31d29466599d2e6dddfce8f34e87553d5765c53a2461d0ce9cee3b3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32174302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b8083f65c2926974ad485098c1d9520ba7c15562be71efed0a7d2bd7a2f267e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 01:00:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 13 Nov 2021 01:00:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 13 Nov 2021 01:00:57 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 13 Nov 2021 01:00:57 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 13 Nov 2021 01:00:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 13 Nov 2021 01:01:00 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 13 Nov 2021 01:01:00 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 13 Nov 2021 01:01:01 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 13 Nov 2021 01:21:11 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Sat, 13 Nov 2021 01:21:11 GMT
ENV PHP_VERSION=8.0.12
# Sat, 13 Nov 2021 01:21:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.12.tar.xz.asc
# Sat, 13 Nov 2021 01:21:12 GMT
ENV PHP_SHA256=a501017b3b0fd3023223ea25d98e87369b782f8a82310c4033d7ea6a989fea0a
# Sat, 13 Nov 2021 01:21:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 13 Nov 2021 01:21:25 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 13 Nov 2021 01:30:59 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 13 Nov 2021 01:31:00 GMT
COPY multi:7d7d4b016ee2e2e18720a1a58004eb4d59de798c619f217398cc1066a656bfd0 in /usr/local/bin/ 
# Sat, 13 Nov 2021 01:31:02 GMT
RUN docker-php-ext-enable sodium
# Sat, 13 Nov 2021 01:31:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 13 Nov 2021 01:31:03 GMT
WORKDIR /var/www/html
# Sat, 13 Nov 2021 01:31:05 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Sat, 13 Nov 2021 01:31:05 GMT
STOPSIGNAL SIGQUIT
# Sat, 13 Nov 2021 01:31:06 GMT
EXPOSE 9000
# Sat, 13 Nov 2021 01:31:06 GMT
CMD ["php-fpm"]
# Sat, 13 Nov 2021 14:22:13 GMT
LABEL org.opencontainers.image.title=YOURLS
# Sat, 13 Nov 2021 14:22:13 GMT
LABEL org.opencontainers.image.description=Your Own URL Shortener
# Sat, 13 Nov 2021 14:22:14 GMT
LABEL org.opencontainers.image.url=https://yourls.org/
# Sat, 13 Nov 2021 14:22:14 GMT
LABEL org.opencontainers.image.documentation=https://yourls.org/
# Sat, 13 Nov 2021 14:22:14 GMT
LABEL org.opencontainers.image.vendor=YOURLS Org
# Sat, 13 Nov 2021 14:22:15 GMT
LABEL org.opencontainers.image.authors=YOURLS
# Sat, 13 Nov 2021 14:22:15 GMT
LABEL org.opencontainers.image.version=1.8.2
# Sat, 13 Nov 2021 14:23:29 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Sat, 13 Nov 2021 14:23:30 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Sat, 13 Nov 2021 14:23:33 GMT
RUN apk add --no-cache bash
# Sat, 13 Nov 2021 14:23:36 GMT
RUN set -eux;     version="1.8.2";     sha256="6d818622e3ba1d5785c2dbcc088be6890f5675fd4f24a2e3111eda4523bbd7ae";     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${version}.tar.gz";     echo "$sha256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${version}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Sat, 13 Nov 2021 14:23:37 GMT
COPY --chown=www-data:www-datafile:0bcfdfe0566007e7477c55552a1341b82b958e95879a5314f411d2188da2429e in /usr/src/yourls/user/ 
# Sat, 13 Nov 2021 14:23:37 GMT
COPY file:a47a395071c52d8d08402c95253924b09809713039b46033d6f6f75603938896 in /usr/local/bin/ 
# Sat, 13 Nov 2021 14:23:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Nov 2021 14:23:38 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fb65eff99d3570be8bbee58e3796b49e0e6fbc64d6c2b55e01eaf1b07709af`  
		Last Modified: Sat, 13 Nov 2021 02:49:22 GMT  
		Size: 1.7 MB (1702248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ffe18ffa25cea29b8a20ba6c41b7485fd89e792d6d333919ea738dcff33555f`  
		Last Modified: Sat, 13 Nov 2021 02:49:21 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:215c6f1ae3409a42a8b2531ec3f19b4dddc77724624fdc7fe72175b53fa03ad0`  
		Last Modified: Sat, 13 Nov 2021 02:49:21 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f84310626813777ce39ce893e1c22d63296d129fdbd5d0f03118cef47168e43`  
		Last Modified: Sat, 13 Nov 2021 02:51:29 GMT  
		Size: 10.7 MB (10734137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda47246450689080140f99b976b05ed3253af2e5913bbdc1498c4a2d859a2e0`  
		Last Modified: Sat, 13 Nov 2021 02:51:26 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d2fea221aa7d94e140a52071e4b46691f49678bb0cff128409917ad4ae4704e`  
		Last Modified: Sat, 13 Nov 2021 02:52:58 GMT  
		Size: 13.7 MB (13701446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aa2b053f9b93eab5fa25eba5dacfb3b013b4d936762f240d8cfff15c35c6af2`  
		Last Modified: Sat, 13 Nov 2021 02:52:49 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1dcb33769d0ed748d8db9c8d1dee59a927e04c28ef69026e6c509ee8c91d115`  
		Last Modified: Sat, 13 Nov 2021 02:52:49 GMT  
		Size: 18.2 KB (18204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d0615128ed8ba9103de3b969f5c3a6bdceb71f4f0bce18f8ad519675165f409`  
		Last Modified: Sat, 13 Nov 2021 02:52:49 GMT  
		Size: 8.6 KB (8572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6820b8c6d16c98f3b57205559b5cb06ac6cffc1e57b8ea5f813f8b7382e32f3`  
		Last Modified: Sat, 13 Nov 2021 14:24:22 GMT  
		Size: 336.8 KB (336758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db8101b5a4444a48f094f3754f5e71a785a60d8ca17c4a47d90eb2ede7df206b`  
		Last Modified: Sat, 13 Nov 2021 14:24:20 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a761759e738a5427119cf8e3ad2a999d799fcd5a57a1177aba395650c7e0c7`  
		Last Modified: Sat, 13 Nov 2021 14:24:20 GMT  
		Size: 454.8 KB (454793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e4c210a6e1790e7303671300a823e42e8cec514a948ab0c50c121106749d53`  
		Last Modified: Sat, 13 Nov 2021 14:24:22 GMT  
		Size: 2.6 MB (2574514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1090846737f2f71a9e9ef14485930b9f3ebc87e49c363310292a9bd918dcb981`  
		Last Modified: Sat, 13 Nov 2021 14:24:20 GMT  
		Size: 2.0 KB (2039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29fee11c9f3311f8649146403958e3b7821c7e2607ed695dcc4bd0ff4b3aae74`  
		Last Modified: Sat, 13 Nov 2021 14:24:20 GMT  
		Size: 1.5 KB (1547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1-fpm-alpine` - linux; arm variant v7

```console
$ docker pull yourls@sha256:56d8e33a0f0d5c5546f036db3559351ad9ded575ca909f6844b1ffd2207a1c47
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30921244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:115adb3314dd4429174a59f9e950adcabc0aea16308b5244aea1ed7a2325bf9b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 12 Nov 2021 16:57:35 GMT
ADD file:03e0720458c3475758bf4394afa56f2165198eb91e6e9581f7768e433744dd9b in / 
# Fri, 12 Nov 2021 16:57:36 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 02:20:26 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 13 Nov 2021 02:20:29 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 13 Nov 2021 02:20:30 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 13 Nov 2021 02:20:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 13 Nov 2021 02:20:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 13 Nov 2021 02:20:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 13 Nov 2021 02:20:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 13 Nov 2021 02:20:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 13 Nov 2021 02:42:32 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Sat, 13 Nov 2021 02:42:33 GMT
ENV PHP_VERSION=8.0.12
# Sat, 13 Nov 2021 02:42:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.12.tar.xz.asc
# Sat, 13 Nov 2021 02:42:34 GMT
ENV PHP_SHA256=a501017b3b0fd3023223ea25d98e87369b782f8a82310c4033d7ea6a989fea0a
# Sat, 13 Nov 2021 02:42:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 13 Nov 2021 02:42:45 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 13 Nov 2021 02:51:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 13 Nov 2021 02:51:36 GMT
COPY multi:7d7d4b016ee2e2e18720a1a58004eb4d59de798c619f217398cc1066a656bfd0 in /usr/local/bin/ 
# Sat, 13 Nov 2021 02:51:38 GMT
RUN docker-php-ext-enable sodium
# Sat, 13 Nov 2021 02:51:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 13 Nov 2021 02:51:39 GMT
WORKDIR /var/www/html
# Sat, 13 Nov 2021 02:51:41 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Sat, 13 Nov 2021 02:51:41 GMT
STOPSIGNAL SIGQUIT
# Sat, 13 Nov 2021 02:51:42 GMT
EXPOSE 9000
# Sat, 13 Nov 2021 02:51:42 GMT
CMD ["php-fpm"]
# Sat, 13 Nov 2021 18:46:26 GMT
LABEL org.opencontainers.image.title=YOURLS
# Sat, 13 Nov 2021 18:46:26 GMT
LABEL org.opencontainers.image.description=Your Own URL Shortener
# Sat, 13 Nov 2021 18:46:27 GMT
LABEL org.opencontainers.image.url=https://yourls.org/
# Sat, 13 Nov 2021 18:46:27 GMT
LABEL org.opencontainers.image.documentation=https://yourls.org/
# Sat, 13 Nov 2021 18:46:27 GMT
LABEL org.opencontainers.image.vendor=YOURLS Org
# Sat, 13 Nov 2021 18:46:28 GMT
LABEL org.opencontainers.image.authors=YOURLS
# Sat, 13 Nov 2021 18:46:28 GMT
LABEL org.opencontainers.image.version=1.8.2
# Sat, 13 Nov 2021 18:47:38 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Sat, 13 Nov 2021 18:47:40 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Sat, 13 Nov 2021 18:47:43 GMT
RUN apk add --no-cache bash
# Sat, 13 Nov 2021 18:47:46 GMT
RUN set -eux;     version="1.8.2";     sha256="6d818622e3ba1d5785c2dbcc088be6890f5675fd4f24a2e3111eda4523bbd7ae";     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${version}.tar.gz";     echo "$sha256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${version}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Sat, 13 Nov 2021 18:47:47 GMT
COPY --chown=www-data:www-datafile:0bcfdfe0566007e7477c55552a1341b82b958e95879a5314f411d2188da2429e in /usr/src/yourls/user/ 
# Sat, 13 Nov 2021 18:47:47 GMT
COPY file:a47a395071c52d8d08402c95253924b09809713039b46033d6f6f75603938896 in /usr/local/bin/ 
# Sat, 13 Nov 2021 18:47:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Nov 2021 18:47:48 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:764d2e53e1a607f2d8261522185d5b9021ade3ec1a595664ee90308c00176899`  
		Last Modified: Fri, 12 Nov 2021 16:59:33 GMT  
		Size: 2.4 MB (2438618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0d591a38553bed13e4644c2ee36cc92a36f4f866265bcec258baef16176c11b`  
		Last Modified: Sat, 13 Nov 2021 04:21:17 GMT  
		Size: 1.6 MB (1571523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a132a38f5266edd87272c20d2129b4448b3dfb530a70424219ddd45fd1d2eb73`  
		Last Modified: Sat, 13 Nov 2021 04:21:16 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a99b8f25382a7fadffc08ae9ebf09b2a2be48a858daf03148035e46335c089a`  
		Last Modified: Sat, 13 Nov 2021 04:21:16 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ed5414040012d4256aba757aa7d3c9b2980c5718180eb46293d738d5d5627e`  
		Last Modified: Sat, 13 Nov 2021 04:24:57 GMT  
		Size: 10.7 MB (10734117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eba01a4be74c0b9cdad5b856653e5314e11640606e9c4193df15a4b0e77d97b`  
		Last Modified: Sat, 13 Nov 2021 04:24:54 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba97b1642393ece00979cfd2e3a957a723b8551f4f3e09760460bd6a44ebb3a5`  
		Last Modified: Sat, 13 Nov 2021 04:26:25 GMT  
		Size: 12.8 MB (12844579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefc4806f0917387dcff50f0c90119000d16ca9b60c911017045ffba2b1fd261`  
		Last Modified: Sat, 13 Nov 2021 04:26:16 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db6bc853fdddfea6c708fbf6727a02e66f4ca3a3d71f875cd5c2a69cae6aa790`  
		Last Modified: Sat, 13 Nov 2021 04:26:16 GMT  
		Size: 18.2 KB (18195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfaa22d19d7e37ab89f54c52bcd80aa53cea665d6b201ef9cac88a51751fce46`  
		Last Modified: Sat, 13 Nov 2021 04:26:16 GMT  
		Size: 8.6 KB (8566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd8bc9b8e99b1a1818a6668eb8cb405c72a1ce5a5a3ed8793cab4b128d388216`  
		Last Modified: Sat, 13 Nov 2021 18:49:31 GMT  
		Size: 307.6 KB (307630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b0fc73205ea3df753805fffad6ef0f75dc50d920242d93bea04eef09986b654`  
		Last Modified: Sat, 13 Nov 2021 18:49:30 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5079f365b84b192ee0d7e540bf54f67d443e4b71c720cb82fe789670f76678e1`  
		Last Modified: Sat, 13 Nov 2021 18:49:30 GMT  
		Size: 415.3 KB (415271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:142cdc0a1ca0633d45c44df8fc5fbaa119811f74aefd13b1c0aa3e27cc7ce5f4`  
		Last Modified: Sat, 13 Nov 2021 18:49:31 GMT  
		Size: 2.6 MB (2574514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ac4316189c4ee2f31d40099ceebce5b3a66f902a53cfe768ce1732e18be904`  
		Last Modified: Sat, 13 Nov 2021 18:49:29 GMT  
		Size: 2.0 KB (2034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b6efd414aafed832c682b1561e3e8b8d6a20ffcbe3ac3506a904604369e1545`  
		Last Modified: Sat, 13 Nov 2021 18:49:29 GMT  
		Size: 1.5 KB (1546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull yourls@sha256:749009a2a4a3fadd64c050bac6c3f9f64c03889dc5f58b801ecc054d77fa9f5b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.1 MB (33097099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e540271ed7a2a3679e46d6f807ccee33795f58edfbc0895d8605f9a1ecaa2f8c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 19:30:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 12 Nov 2021 19:30:34 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 12 Nov 2021 19:30:35 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 12 Nov 2021 19:30:36 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 12 Nov 2021 19:30:37 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 12 Nov 2021 19:30:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Nov 2021 19:30:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Nov 2021 19:30:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 12 Nov 2021 20:02:23 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 12 Nov 2021 20:02:24 GMT
ENV PHP_VERSION=8.0.12
# Fri, 12 Nov 2021 20:02:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.12.tar.xz.asc
# Fri, 12 Nov 2021 20:02:26 GMT
ENV PHP_SHA256=a501017b3b0fd3023223ea25d98e87369b782f8a82310c4033d7ea6a989fea0a
# Fri, 12 Nov 2021 20:02:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 12 Nov 2021 20:02:36 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 12 Nov 2021 20:12:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 12 Nov 2021 20:12:14 GMT
COPY multi:7d7d4b016ee2e2e18720a1a58004eb4d59de798c619f217398cc1066a656bfd0 in /usr/local/bin/ 
# Fri, 12 Nov 2021 20:12:15 GMT
RUN docker-php-ext-enable sodium
# Fri, 12 Nov 2021 20:12:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 12 Nov 2021 20:12:17 GMT
WORKDIR /var/www/html
# Fri, 12 Nov 2021 20:12:18 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 12 Nov 2021 20:12:19 GMT
STOPSIGNAL SIGQUIT
# Fri, 12 Nov 2021 20:12:20 GMT
EXPOSE 9000
# Fri, 12 Nov 2021 20:12:21 GMT
CMD ["php-fpm"]
# Sat, 13 Nov 2021 15:33:28 GMT
LABEL org.opencontainers.image.title=YOURLS
# Sat, 13 Nov 2021 15:33:29 GMT
LABEL org.opencontainers.image.description=Your Own URL Shortener
# Sat, 13 Nov 2021 15:33:30 GMT
LABEL org.opencontainers.image.url=https://yourls.org/
# Sat, 13 Nov 2021 15:33:31 GMT
LABEL org.opencontainers.image.documentation=https://yourls.org/
# Sat, 13 Nov 2021 15:33:32 GMT
LABEL org.opencontainers.image.vendor=YOURLS Org
# Sat, 13 Nov 2021 15:33:33 GMT
LABEL org.opencontainers.image.authors=YOURLS
# Sat, 13 Nov 2021 15:33:34 GMT
LABEL org.opencontainers.image.version=1.8.2
# Sat, 13 Nov 2021 15:34:16 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Sat, 13 Nov 2021 15:34:17 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Sat, 13 Nov 2021 15:34:19 GMT
RUN apk add --no-cache bash
# Sat, 13 Nov 2021 15:34:21 GMT
RUN set -eux;     version="1.8.2";     sha256="6d818622e3ba1d5785c2dbcc088be6890f5675fd4f24a2e3111eda4523bbd7ae";     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${version}.tar.gz";     echo "$sha256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${version}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Sat, 13 Nov 2021 15:34:23 GMT
COPY --chown=www-data:www-datafile:0bcfdfe0566007e7477c55552a1341b82b958e95879a5314f411d2188da2429e in /usr/src/yourls/user/ 
# Sat, 13 Nov 2021 15:34:24 GMT
COPY file:a47a395071c52d8d08402c95253924b09809713039b46033d6f6f75603938896 in /usr/local/bin/ 
# Sat, 13 Nov 2021 15:34:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Nov 2021 15:34:25 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9716534ffbe55fb7b1cdc9c51401565113fe78d473379c595bf42e6d05fd5e6e`  
		Last Modified: Fri, 12 Nov 2021 21:25:50 GMT  
		Size: 1.7 MB (1711801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49d47cbc9449ef4aab290c562e2d538c1152c89268a02bb026807264d1c3d6da`  
		Last Modified: Fri, 12 Nov 2021 21:25:49 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a654447725655854a94c8af1e17c61ba95c1eb179a627aa323bfd70bfbae408`  
		Last Modified: Fri, 12 Nov 2021 21:25:50 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d0f90b0e2ee0c858826a071b2c2068d7623278701189c9f8f09bfefb68717c0`  
		Last Modified: Fri, 12 Nov 2021 21:27:55 GMT  
		Size: 10.7 MB (10733892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a574420850795d390f17998e57d89b359fa0e0298e8e7d4d0f714174763e37c`  
		Last Modified: Fri, 12 Nov 2021 21:27:54 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8295a362276a2b89d1a26fb280a4b1694c95c50594ac5145ae4b1e1018e2e92`  
		Last Modified: Fri, 12 Nov 2021 21:28:54 GMT  
		Size: 14.5 MB (14501621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c95e6a8b7bad0096f5b5a25c7865c180819a7c527a6ed84b7656cfa7bb2560f`  
		Last Modified: Fri, 12 Nov 2021 21:28:52 GMT  
		Size: 2.3 KB (2299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa3caf1f18ac753fc76f258a3ae3deb11b49e971df0e125c925ba7eae670e0ae`  
		Last Modified: Fri, 12 Nov 2021 21:28:52 GMT  
		Size: 18.1 KB (18109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab0b1b4dd29ba22e0d4b96fe0c3296e446dccd1170aa8293a4978fe11d77ca8`  
		Last Modified: Fri, 12 Nov 2021 21:28:52 GMT  
		Size: 8.6 KB (8570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d0b24e1855d6cc61133dd46521104c344ea154d9d6a3796bad7ddcb1676b4ed`  
		Last Modified: Sat, 13 Nov 2021 15:35:22 GMT  
		Size: 347.6 KB (347611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:818e6206066a18a8cc5e4454393b1f5e83b9f6401034b92a67e6235e3302baec`  
		Last Modified: Sat, 13 Nov 2021 15:35:18 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb8cfa040bb14f6e9dd3d65cc518e8a0841cbeedad728361cc469000a9d2cb67`  
		Last Modified: Sat, 13 Nov 2021 15:35:19 GMT  
		Size: 474.1 KB (474088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57f69bf6dc6aec76621dfa5e3679bf244b46f6d41660eaa01a9bd0523023b38d`  
		Last Modified: Sat, 13 Nov 2021 15:35:19 GMT  
		Size: 2.6 MB (2575553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8921f4f8ec3c57a54c775f724dd3c96a85c61f514951d683b0af7f8e2f446a9`  
		Last Modified: Sat, 13 Nov 2021 15:35:19 GMT  
		Size: 2.0 KB (2034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca86a6cd9fa7a02855f3de624dc3b450f35bf8dac573f44e64045b63a3bcee2`  
		Last Modified: Sat, 13 Nov 2021 15:35:18 GMT  
		Size: 1.5 KB (1547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1-fpm-alpine` - linux; 386

```console
$ docker pull yourls@sha256:cd5c65a0843404ffa8b6fbc90b1f73421e8d709db77fb7d0d57143a2ae56fe81
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34539743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e901a48e28574c665825ed8ba05fdf50c1c301906f8be3a9fc7c9261b90737e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 12 Nov 2021 16:38:42 GMT
ADD file:403428c2903dd9dea10d069185873cb2c2c3149c553797807c69f22aa3d12fe3 in / 
# Fri, 12 Nov 2021 16:38:42 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 00:47:21 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 13 Nov 2021 00:47:24 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 13 Nov 2021 00:47:26 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 13 Nov 2021 00:47:26 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 13 Nov 2021 00:47:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 13 Nov 2021 00:47:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 13 Nov 2021 00:47:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 13 Nov 2021 00:47:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 13 Nov 2021 01:29:07 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Sat, 13 Nov 2021 01:29:08 GMT
ENV PHP_VERSION=8.0.12
# Sat, 13 Nov 2021 01:29:08 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.12.tar.xz.asc
# Sat, 13 Nov 2021 01:29:08 GMT
ENV PHP_SHA256=a501017b3b0fd3023223ea25d98e87369b782f8a82310c4033d7ea6a989fea0a
# Sat, 13 Nov 2021 01:29:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 13 Nov 2021 01:29:26 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 13 Nov 2021 01:48:37 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 13 Nov 2021 01:48:38 GMT
COPY multi:7d7d4b016ee2e2e18720a1a58004eb4d59de798c619f217398cc1066a656bfd0 in /usr/local/bin/ 
# Sat, 13 Nov 2021 01:48:40 GMT
RUN docker-php-ext-enable sodium
# Sat, 13 Nov 2021 01:48:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 13 Nov 2021 01:48:40 GMT
WORKDIR /var/www/html
# Sat, 13 Nov 2021 01:48:42 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Sat, 13 Nov 2021 01:48:42 GMT
STOPSIGNAL SIGQUIT
# Sat, 13 Nov 2021 01:48:42 GMT
EXPOSE 9000
# Sat, 13 Nov 2021 01:48:43 GMT
CMD ["php-fpm"]
# Sat, 13 Nov 2021 11:47:10 GMT
LABEL org.opencontainers.image.title=YOURLS
# Sat, 13 Nov 2021 11:47:10 GMT
LABEL org.opencontainers.image.description=Your Own URL Shortener
# Sat, 13 Nov 2021 11:47:11 GMT
LABEL org.opencontainers.image.url=https://yourls.org/
# Sat, 13 Nov 2021 11:47:11 GMT
LABEL org.opencontainers.image.documentation=https://yourls.org/
# Sat, 13 Nov 2021 11:47:11 GMT
LABEL org.opencontainers.image.vendor=YOURLS Org
# Sat, 13 Nov 2021 11:47:11 GMT
LABEL org.opencontainers.image.authors=YOURLS
# Sat, 13 Nov 2021 11:47:11 GMT
LABEL org.opencontainers.image.version=1.8.2
# Sat, 13 Nov 2021 11:48:24 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Sat, 13 Nov 2021 11:48:25 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Sat, 13 Nov 2021 11:48:27 GMT
RUN apk add --no-cache bash
# Sat, 13 Nov 2021 11:48:29 GMT
RUN set -eux;     version="1.8.2";     sha256="6d818622e3ba1d5785c2dbcc088be6890f5675fd4f24a2e3111eda4523bbd7ae";     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${version}.tar.gz";     echo "$sha256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${version}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Sat, 13 Nov 2021 11:48:29 GMT
COPY --chown=www-data:www-datafile:0bcfdfe0566007e7477c55552a1341b82b958e95879a5314f411d2188da2429e in /usr/src/yourls/user/ 
# Sat, 13 Nov 2021 11:48:29 GMT
COPY file:a47a395071c52d8d08402c95253924b09809713039b46033d6f6f75603938896 in /usr/local/bin/ 
# Sat, 13 Nov 2021 11:48:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Nov 2021 11:48:30 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:5420e0d28c84ecb16748cb90cc6acf8e2a81dab10cb1f674f3eee8533e53c62a`  
		Last Modified: Fri, 12 Nov 2021 16:39:36 GMT  
		Size: 2.8 MB (2830948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c05111b719bf0e9c81182879ace55b68244fff3ccaacc6813f9ce740b1adf4d`  
		Last Modified: Sat, 13 Nov 2021 04:00:31 GMT  
		Size: 1.8 MB (1812696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f12e62d2679739a2acadab070b1c7d0f433a8a46d449147d00fa5c4aa0a8753`  
		Last Modified: Sat, 13 Nov 2021 04:00:30 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f3e1535943b040497915113f37b46a4ba0dc10f27aabcdb6dbf9d0b594ca8be`  
		Last Modified: Sat, 13 Nov 2021 04:00:30 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:281b9e6c22e2166f6ebee0ac019cece183f7594f904d59c3e7c3418fd1acec92`  
		Last Modified: Sat, 13 Nov 2021 04:03:25 GMT  
		Size: 10.7 MB (10734122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7515c0efd4fa8c240534ad08241edf609bd80b58d2c87c79a9a52a95a63aded7`  
		Last Modified: Sat, 13 Nov 2021 04:03:24 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7db138d61437e4cf8ac8ddcb09faa73a374d5649d2aaf30b4a6995ce8c9e17`  
		Last Modified: Sat, 13 Nov 2021 04:04:49 GMT  
		Size: 15.4 MB (15390775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dc5cd726d16341467da852f5eca406faf3f453cc7496a7538c9c97c20ca8fab`  
		Last Modified: Sat, 13 Nov 2021 04:04:42 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa1486360affb9fd8b3767d21fdaa237c2bca16137febf67df21b59a34694b3`  
		Last Modified: Sat, 13 Nov 2021 04:04:42 GMT  
		Size: 18.2 KB (18185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f93abf5c46d8f023eb93e670abe87b72646cdc15d09fc9dca4bb7cf5ee44d558`  
		Last Modified: Sat, 13 Nov 2021 04:04:42 GMT  
		Size: 8.6 KB (8567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ea80eb24c66303d7c32e012c8a93fec78d8c2f872dd24b32ac37c7030d0001`  
		Last Modified: Sat, 13 Nov 2021 11:49:25 GMT  
		Size: 659.5 KB (659495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a6a163d31fa0c538ecaa2d39f4e9561d463cc9bddfe130a544528e70641cf88`  
		Last Modified: Sat, 13 Nov 2021 11:49:23 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f798e3e2e1c835c021f80f6b17573baa9d41e78d0f52599e688b8f301c00d08`  
		Last Modified: Sat, 13 Nov 2021 11:49:23 GMT  
		Size: 502.2 KB (502202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3852861b20c1a9d63b4557c6b7d2565acbda73df0d69e65305983bdc69e09020`  
		Last Modified: Sat, 13 Nov 2021 11:49:23 GMT  
		Size: 2.6 MB (2574518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:468a14b861c703dcd1eb991bfe290fcaa793278ca501c9d58e503ce02bbabfbc`  
		Last Modified: Sat, 13 Nov 2021 11:49:22 GMT  
		Size: 2.0 KB (2035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12bf80592a5515e01493b4dc874652fa1a07607591c892c4e4415a17e8b543d9`  
		Last Modified: Sat, 13 Nov 2021 11:49:23 GMT  
		Size: 1.5 KB (1547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1-fpm-alpine` - linux; ppc64le

```console
$ docker pull yourls@sha256:db3922f224dffd19e3b065a4eb3d8ef2a3bd86b2c4d9c83c634ecf10fdab1d4e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34653919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90e172966db9bdcf9aef0eae94f052d4ae4c9cceeb880a162694d7fbe03d61e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 12 Nov 2021 21:18:00 GMT
ADD file:4d45063079cb28a34f1e382fddb22f156ac99d5449aa05ed37cb653c1f7b80f2 in / 
# Fri, 12 Nov 2021 21:18:01 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 11:56:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 13 Nov 2021 11:56:08 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 13 Nov 2021 11:56:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 13 Nov 2021 11:56:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 13 Nov 2021 11:56:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 13 Nov 2021 11:56:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 13 Nov 2021 11:56:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 13 Nov 2021 11:56:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 13 Nov 2021 12:24:47 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Sat, 13 Nov 2021 12:24:56 GMT
ENV PHP_VERSION=8.0.12
# Sat, 13 Nov 2021 12:25:00 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.12.tar.xz.asc
# Sat, 13 Nov 2021 12:25:05 GMT
ENV PHP_SHA256=a501017b3b0fd3023223ea25d98e87369b782f8a82310c4033d7ea6a989fea0a
# Sat, 13 Nov 2021 12:25:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 13 Nov 2021 12:25:36 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 13 Nov 2021 12:36:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 13 Nov 2021 12:36:37 GMT
COPY multi:7d7d4b016ee2e2e18720a1a58004eb4d59de798c619f217398cc1066a656bfd0 in /usr/local/bin/ 
# Sat, 13 Nov 2021 12:36:49 GMT
RUN docker-php-ext-enable sodium
# Sat, 13 Nov 2021 12:36:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 13 Nov 2021 12:36:58 GMT
WORKDIR /var/www/html
# Sat, 13 Nov 2021 12:37:15 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Sat, 13 Nov 2021 12:37:23 GMT
STOPSIGNAL SIGQUIT
# Sat, 13 Nov 2021 12:37:31 GMT
EXPOSE 9000
# Sat, 13 Nov 2021 12:37:39 GMT
CMD ["php-fpm"]
# Sat, 13 Nov 2021 19:09:24 GMT
LABEL org.opencontainers.image.title=YOURLS
# Sat, 13 Nov 2021 19:09:26 GMT
LABEL org.opencontainers.image.description=Your Own URL Shortener
# Sat, 13 Nov 2021 19:09:28 GMT
LABEL org.opencontainers.image.url=https://yourls.org/
# Sat, 13 Nov 2021 19:09:29 GMT
LABEL org.opencontainers.image.documentation=https://yourls.org/
# Sat, 13 Nov 2021 19:09:33 GMT
LABEL org.opencontainers.image.vendor=YOURLS Org
# Sat, 13 Nov 2021 19:09:36 GMT
LABEL org.opencontainers.image.authors=YOURLS
# Sat, 13 Nov 2021 19:09:40 GMT
LABEL org.opencontainers.image.version=1.8.2
# Sat, 13 Nov 2021 19:10:33 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Sat, 13 Nov 2021 19:10:43 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Sat, 13 Nov 2021 19:10:56 GMT
RUN apk add --no-cache bash
# Sat, 13 Nov 2021 19:11:08 GMT
RUN set -eux;     version="1.8.2";     sha256="6d818622e3ba1d5785c2dbcc088be6890f5675fd4f24a2e3111eda4523bbd7ae";     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${version}.tar.gz";     echo "$sha256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${version}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Sat, 13 Nov 2021 19:11:09 GMT
COPY --chown=www-data:www-datafile:0bcfdfe0566007e7477c55552a1341b82b958e95879a5314f411d2188da2429e in /usr/src/yourls/user/ 
# Sat, 13 Nov 2021 19:11:10 GMT
COPY file:a47a395071c52d8d08402c95253924b09809713039b46033d6f6f75603938896 in /usr/local/bin/ 
# Sat, 13 Nov 2021 19:11:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Nov 2021 19:11:14 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:72940440c1ab65eca4d38846164719ffde4b147543cc658d041407a925b13368`  
		Last Modified: Fri, 12 Nov 2021 21:19:32 GMT  
		Size: 2.8 MB (2817467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf526002982778a0157923a6219fbadd645d22999e9251af0db89be07d002272`  
		Last Modified: Sat, 13 Nov 2021 14:08:23 GMT  
		Size: 1.8 MB (1759206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b47bb623f5bce1748b7a2c4e16b2726478248c03150000de676a1020aaeada`  
		Last Modified: Sat, 13 Nov 2021 14:08:23 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f035bbd1b7db7792a68686cccf93b48bd273f6f89375962d7fae46bab690f7ac`  
		Last Modified: Sat, 13 Nov 2021 14:08:23 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5952cecf5b2487c26418b53a70d34948e09d8cc84a954c2a2faeacf602f089b2`  
		Last Modified: Sat, 13 Nov 2021 14:10:37 GMT  
		Size: 10.7 MB (10734124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3c3a34d5c12f84156c57d82041d9c31244b8cd4c61d9b61b6b67143222948c`  
		Last Modified: Sat, 13 Nov 2021 14:10:35 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2905bed642c5db89b39300aa921d1303299f85f68cb1fce4335b7b444ecd79ad`  
		Last Modified: Sat, 13 Nov 2021 14:11:42 GMT  
		Size: 15.8 MB (15805559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a235fb87cade4fefcf2cf1da9854101e4d0a3469e9ed554effb69f733708be80`  
		Last Modified: Sat, 13 Nov 2021 14:11:38 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c320b6176d8ab261664411e0b584b4d45cfec6f5b0eb7498dc89f10198c0094`  
		Last Modified: Sat, 13 Nov 2021 14:11:38 GMT  
		Size: 18.2 KB (18198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a161b9141daefd70bf9e123532921e158e5817e353cf2a8db5c09be61045250c`  
		Last Modified: Sat, 13 Nov 2021 14:11:38 GMT  
		Size: 8.6 KB (8568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33639a9049b5b86759814ab6e14609c0c323f2ac51af3e1dcbe319788d337838`  
		Last Modified: Sat, 13 Nov 2021 19:12:13 GMT  
		Size: 397.9 KB (397877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13154c5cdba56285d66ed3f2454c34a8aec030f6167f8d648a18de99af20145e`  
		Last Modified: Sat, 13 Nov 2021 19:12:09 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b19a23452fa11537a700bad28eb38503ae96d78c108506662f0cef5802a3e953`  
		Last Modified: Sat, 13 Nov 2021 19:12:09 GMT  
		Size: 530.2 KB (530167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f366e7fe66b9c123a51d92218d89e882bf012b2af02b7da5035f9e27809c07`  
		Last Modified: Sat, 13 Nov 2021 19:12:10 GMT  
		Size: 2.6 MB (2574520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0006568dbe0d3a5024131d493ef8dea539ae7899a0627012f9e87af87491d44`  
		Last Modified: Sat, 13 Nov 2021 19:12:09 GMT  
		Size: 2.0 KB (2035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560f30e4ab0cdc424f192dc94591374ab7e3be23443a0086df693c96594ade60`  
		Last Modified: Sat, 13 Nov 2021 19:12:09 GMT  
		Size: 1.5 KB (1549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1-fpm-alpine` - linux; s390x

```console
$ docker pull yourls@sha256:a83259db9cd0496e3ef81b676a1506814782b7db483bc545151fb91e2acf7d58
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.7 MB (32657287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7edc591fea55dc92f77e4b8b740c46882a8c9234cc3ceb46e81585d722b14bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 12 Nov 2021 16:41:35 GMT
ADD file:7e0cf02b3f015b1a0f867c03b2902b85f2140be1cee7af63c23f367a487e4577 in / 
# Fri, 12 Nov 2021 16:41:36 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 19:58:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 12 Nov 2021 19:58:15 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 12 Nov 2021 19:58:15 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 12 Nov 2021 19:58:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 12 Nov 2021 19:58:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 12 Nov 2021 19:58:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Nov 2021 19:58:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Nov 2021 19:58:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 12 Nov 2021 20:11:25 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 12 Nov 2021 20:11:25 GMT
ENV PHP_VERSION=8.0.12
# Fri, 12 Nov 2021 20:11:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.12.tar.xz.asc
# Fri, 12 Nov 2021 20:11:25 GMT
ENV PHP_SHA256=a501017b3b0fd3023223ea25d98e87369b782f8a82310c4033d7ea6a989fea0a
# Fri, 12 Nov 2021 20:11:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 12 Nov 2021 20:11:42 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 12 Nov 2021 20:17:29 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 12 Nov 2021 20:17:30 GMT
COPY multi:7d7d4b016ee2e2e18720a1a58004eb4d59de798c619f217398cc1066a656bfd0 in /usr/local/bin/ 
# Fri, 12 Nov 2021 20:17:30 GMT
RUN docker-php-ext-enable sodium
# Fri, 12 Nov 2021 20:17:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 12 Nov 2021 20:17:31 GMT
WORKDIR /var/www/html
# Fri, 12 Nov 2021 20:17:31 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 12 Nov 2021 20:17:31 GMT
STOPSIGNAL SIGQUIT
# Fri, 12 Nov 2021 20:17:31 GMT
EXPOSE 9000
# Fri, 12 Nov 2021 20:17:31 GMT
CMD ["php-fpm"]
# Sat, 13 Nov 2021 07:08:39 GMT
LABEL org.opencontainers.image.title=YOURLS
# Sat, 13 Nov 2021 07:08:39 GMT
LABEL org.opencontainers.image.description=Your Own URL Shortener
# Sat, 13 Nov 2021 07:08:39 GMT
LABEL org.opencontainers.image.url=https://yourls.org/
# Sat, 13 Nov 2021 07:08:40 GMT
LABEL org.opencontainers.image.documentation=https://yourls.org/
# Sat, 13 Nov 2021 07:08:40 GMT
LABEL org.opencontainers.image.vendor=YOURLS Org
# Sat, 13 Nov 2021 07:08:40 GMT
LABEL org.opencontainers.image.authors=YOURLS
# Sat, 13 Nov 2021 07:08:40 GMT
LABEL org.opencontainers.image.version=1.8.2
# Sat, 13 Nov 2021 07:09:03 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Sat, 13 Nov 2021 07:09:03 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Sat, 13 Nov 2021 07:09:04 GMT
RUN apk add --no-cache bash
# Sat, 13 Nov 2021 07:09:05 GMT
RUN set -eux;     version="1.8.2";     sha256="6d818622e3ba1d5785c2dbcc088be6890f5675fd4f24a2e3111eda4523bbd7ae";     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${version}.tar.gz";     echo "$sha256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${version}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Sat, 13 Nov 2021 07:09:06 GMT
COPY --chown=www-data:www-datafile:0bcfdfe0566007e7477c55552a1341b82b958e95879a5314f411d2188da2429e in /usr/src/yourls/user/ 
# Sat, 13 Nov 2021 07:09:06 GMT
COPY file:a47a395071c52d8d08402c95253924b09809713039b46033d6f6f75603938896 in /usr/local/bin/ 
# Sat, 13 Nov 2021 07:09:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Nov 2021 07:09:06 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:817a13b0e05928f7491adbf1d2cf261ec35079112247bd03469bbe31156aca7c`  
		Last Modified: Fri, 12 Nov 2021 16:42:44 GMT  
		Size: 2.6 MB (2609278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01c6db577f243875f52f246d8a7fdab675a850569d52d6bba314f58258225c1f`  
		Last Modified: Fri, 12 Nov 2021 21:10:48 GMT  
		Size: 1.8 MB (1774038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a472bfa2a1552842a7406f914151af808b4f2a9e245ddbfe7cbc332697f96b12`  
		Last Modified: Fri, 12 Nov 2021 21:10:47 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3cea1835285017465c0df7a510c36971229f7066ec32d2ac436c4f9ac6ebd3`  
		Last Modified: Fri, 12 Nov 2021 21:10:48 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ece5120b3dfe943c5c28cf52d1eb81ea7ef0b3477ce9e93f1f03cf36eb7c9e1b`  
		Last Modified: Fri, 12 Nov 2021 21:12:36 GMT  
		Size: 10.7 MB (10734131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7e2681f4bfb1b829e3ef56bab0adb51d16a2be5477acdea3c4922a5dafff00`  
		Last Modified: Fri, 12 Nov 2021 21:12:36 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4cbbda3978d0706ae643e35cb89bcae0fdbc2dbe5a3b234ad6867b14ab2b78d`  
		Last Modified: Fri, 12 Nov 2021 21:13:16 GMT  
		Size: 14.1 MB (14092497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbdf1c404c72db9ae4d12cf596a19b79d2fe340778b2293e4bfc4508cb1aa406`  
		Last Modified: Fri, 12 Nov 2021 21:13:14 GMT  
		Size: 2.3 KB (2303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a2205b128d6fa439370ce4018b4a841e88a3cccd1958c65f86ef0117a1f0a3`  
		Last Modified: Fri, 12 Nov 2021 21:13:14 GMT  
		Size: 18.2 KB (18213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e547ad2424a7aa5118b5a9652e825e5719899ce5d3e88f94d684b9d8b1f3472`  
		Last Modified: Fri, 12 Nov 2021 21:13:14 GMT  
		Size: 8.6 KB (8569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16abe101112096a4ba92063d8787206ca209334950dcd09c12e34b9b8febfb3`  
		Last Modified: Sat, 13 Nov 2021 07:09:56 GMT  
		Size: 354.6 KB (354560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95b3254e41d465362b33cf927afd9278fbdc56418d284a00ef7983e960383b9`  
		Last Modified: Sat, 13 Nov 2021 07:09:55 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abffe4ba04392799e3acdd53473acd1f8b4ea4c7b1028a918a3e6ddc1751e753`  
		Last Modified: Sat, 13 Nov 2021 07:09:55 GMT  
		Size: 483.2 KB (483246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3a3959f3366ac66a08f034de0affec0e09f0e09242cef3e0832c8c574ba7920`  
		Last Modified: Sat, 13 Nov 2021 07:09:55 GMT  
		Size: 2.6 MB (2574516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1386792b81cc5c35c506d9820b259331bf69a3970a62c075ee5ff2bc62bd58b`  
		Last Modified: Sat, 13 Nov 2021 07:09:55 GMT  
		Size: 2.0 KB (2039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c31989cb1f966bfdafb2368d80d643ae16daea99d3d3d6baa1c50456a847a7d`  
		Last Modified: Sat, 13 Nov 2021 07:09:55 GMT  
		Size: 1.5 KB (1549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
