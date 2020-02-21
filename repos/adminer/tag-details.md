<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `adminer`

-	[`adminer:4`](#adminer4)
-	[`adminer:4.7`](#adminer47)
-	[`adminer:4.7.6`](#adminer476)
-	[`adminer:4.7.6-fastcgi`](#adminer476-fastcgi)
-	[`adminer:4.7.6-standalone`](#adminer476-standalone)
-	[`adminer:4.7-fastcgi`](#adminer47-fastcgi)
-	[`adminer:4.7-standalone`](#adminer47-standalone)
-	[`adminer:4-fastcgi`](#adminer4-fastcgi)
-	[`adminer:4-standalone`](#adminer4-standalone)
-	[`adminer:fastcgi`](#adminerfastcgi)
-	[`adminer:latest`](#adminerlatest)
-	[`adminer:standalone`](#adminerstandalone)

## `adminer:4`

```console
$ docker pull adminer@sha256:c689401f4ee85e37ba2cd62d401af2d569833dd8efa2c338177889fa9c525882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `adminer:4` - linux; amd64

```console
$ docker pull adminer@sha256:6ceb642133ac56e267c50ae4bfb24ac0008b0eb02b772abae9059caa45211bee
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31058191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:259cc60bdb72538cffc06536d8bb73c3d9afd7156afc71b0c97fb1659917805e`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Sat, 18 Jan 2020 03:18:30 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:18:30 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:18:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 03:18:30 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 24 Jan 2020 07:05:12 GMT
ENV PHP_VERSION=7.4.2
# Fri, 24 Jan 2020 07:05:13 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.2.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.2.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 07:05:13 GMT
ENV PHP_SHA256=98284deac017da0d426117ecae7599a1f1bf62ae3911e8bc16c4403a8f4bdf13 PHP_MD5=
# Fri, 24 Jan 2020 07:05:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 24 Jan 2020 07:05:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 07:13:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 07:13:16 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Fri, 24 Jan 2020 07:13:17 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 07:13:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 07:13:17 GMT
CMD ["php" "-a"]
# Fri, 24 Jan 2020 10:52:17 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 24 Jan 2020 10:52:17 GMT
STOPSIGNAL SIGINT
# Fri, 24 Jan 2020 10:52:18 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 24 Jan 2020 10:52:18 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 10:52:19 GMT
RUN apk add --no-cache libpq
# Fri, 24 Jan 2020 10:52:38 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Fri, 24 Jan 2020 10:52:39 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 31 Jan 2020 17:19:26 GMT
ENV ADMINER_VERSION=4.7.6
# Fri, 31 Jan 2020 17:19:26 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Fri, 31 Jan 2020 17:19:26 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Fri, 31 Jan 2020 17:19:27 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 31 Jan 2020 17:19:28 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 31 Jan 2020 17:19:28 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 31 Jan 2020 17:19:28 GMT
USER adminer
# Fri, 31 Jan 2020 17:19:28 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 31 Jan 2020 17:19:28 GMT
EXPOSE 8080
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
	-	`sha256:5fa47f19b1e835f47f4c1273ccb215a42ee2aefafe300409d92b05b899a757d8`  
		Last Modified: Fri, 24 Jan 2020 10:39:33 GMT  
		Size: 10.3 MB (10271096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4556adb19ddcb43be3cd12b973f718e5edc74d6986ae4406a0c3011cbeb3dc93`  
		Last Modified: Fri, 24 Jan 2020 10:39:33 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:205de55b7ed0d389ac2c9777321f11ba9377a148002c2ef1d7b68d02a96472f3`  
		Last Modified: Fri, 24 Jan 2020 10:39:42 GMT  
		Size: 14.6 MB (14574023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c35aa7da966a732561c37c8b5d56949eedcb7865066b86da95c8bc58c18c48d2`  
		Last Modified: Fri, 24 Jan 2020 10:39:32 GMT  
		Size: 2.2 KB (2216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82a54ca6f814c156199e3266c4297efe2f54fb83bfb1645f53582eae3d1e222e`  
		Last Modified: Fri, 24 Jan 2020 10:39:33 GMT  
		Size: 73.1 KB (73145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e28f69f8cf7d397d8bd78cab68b9713275989e440016ec98580b94d0b0dc23f8`  
		Last Modified: Fri, 24 Jan 2020 10:53:42 GMT  
		Size: 306.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b527d0b89c2ea24dd10be7c18c1dcdf592fd4e1a5ff2c9da47fba2940fbb25a7`  
		Last Modified: Fri, 24 Jan 2020 10:53:42 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35b881820e3f1402cd2b2836dc6064db1b8ef029479448d5a058baa86b0f2e29`  
		Last Modified: Fri, 24 Jan 2020 10:53:41 GMT  
		Size: 1.3 MB (1277246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97e920225fdf7c9fc6bd8762ee3efbc9225341331c21812757347e46b22a2db3`  
		Last Modified: Fri, 24 Jan 2020 10:53:41 GMT  
		Size: 126.6 KB (126617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c8cde070aec4f16d202102cbdad6a161e48b4ffae4426da85717e9ee116fbec`  
		Last Modified: Fri, 24 Jan 2020 10:53:40 GMT  
		Size: 1.5 KB (1474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:028d5feebf26f852c8d09343a1b1ea1be953837a2f402743e1c021ea7b15ccee`  
		Last Modified: Fri, 31 Jan 2020 17:19:44 GMT  
		Size: 570.7 KB (570688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e0b9ec991cbee8b6377946c76367fcaa9782c4be8d265be834c5158b2638d40`  
		Last Modified: Fri, 31 Jan 2020 17:19:44 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4` - linux; arm variant v6

```console
$ docker pull adminer@sha256:086342d4149c1554e7c334711e0c6ccfa783ce0991cdd33d1687ca56e83020c7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.8 MB (29825140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08598589c478e6d488e3d5892d914c3ccac2ca333bf32b79046b127a04438a92`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Sat, 18 Jan 2020 03:40:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:40:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:40:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 03:40:19 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 20 Feb 2020 21:49:41 GMT
ENV PHP_VERSION=7.4.3
# Thu, 20 Feb 2020 21:49:43 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.3.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.3.tar.xz.asc/from/this/mirror
# Thu, 20 Feb 2020 21:49:44 GMT
ENV PHP_SHA256=cf1f856d877c268124ded1ede40c9fb6142b125fdaafdc54f855120b8bc6982a PHP_MD5=
# Thu, 20 Feb 2020 21:49:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Feb 2020 21:49:57 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Feb 2020 21:53:47 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 20 Feb 2020 21:53:50 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 20 Feb 2020 21:53:53 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Feb 2020 21:53:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Feb 2020 21:53:54 GMT
CMD ["php" "-a"]
# Thu, 20 Feb 2020 23:45:59 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Thu, 20 Feb 2020 23:45:59 GMT
STOPSIGNAL SIGINT
# Thu, 20 Feb 2020 23:46:02 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 20 Feb 2020 23:46:03 GMT
WORKDIR /var/www/html
# Thu, 20 Feb 2020 23:46:05 GMT
RUN apk add --no-cache libpq
# Thu, 20 Feb 2020 23:46:36 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Thu, 20 Feb 2020 23:46:39 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Thu, 20 Feb 2020 23:46:41 GMT
ENV ADMINER_VERSION=4.7.6
# Thu, 20 Feb 2020 23:46:41 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Thu, 20 Feb 2020 23:46:42 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Thu, 20 Feb 2020 23:46:45 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Thu, 20 Feb 2020 23:46:46 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 20 Feb 2020 23:46:46 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Thu, 20 Feb 2020 23:46:47 GMT
USER adminer
# Thu, 20 Feb 2020 23:46:48 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 20 Feb 2020 23:46:48 GMT
EXPOSE 8080
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
	-	`sha256:f246fe8b62d43a3f633a04898577258a2ce5dd84edf5fd464403b9a108b301e2`  
		Last Modified: Thu, 20 Feb 2020 23:10:06 GMT  
		Size: 10.3 MB (10280264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b4e0af10768397859f6f19eca4b17ee9f21d61a1cb06989aba861267cf1b6a`  
		Last Modified: Thu, 20 Feb 2020 23:10:05 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a228bdc8e070add11170637553b04b0eeab55a8af3159561b2878b3bcc00bbb`  
		Last Modified: Thu, 20 Feb 2020 23:10:11 GMT  
		Size: 13.6 MB (13600067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:936640ed543c6bb114e0374d4aa5d00b0ad989151337d4edfe6047bad672c605`  
		Last Modified: Thu, 20 Feb 2020 23:10:05 GMT  
		Size: 2.2 KB (2214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071eed09e44daa0c7c7d337a517208fa4a3c08e02029c0970082688456496bec`  
		Last Modified: Thu, 20 Feb 2020 23:10:05 GMT  
		Size: 72.7 KB (72679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:500b89ded2f6c4841beacd80fbbc9393d964cc71bd39c391faf7dc97822dbdb9`  
		Last Modified: Thu, 20 Feb 2020 23:47:57 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512f9b08d8b23f60cb6dff75b2270418b1aef35536dd655abbebc984b88a251b`  
		Last Modified: Thu, 20 Feb 2020 23:47:58 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c471a8e9c45607043e4014b7f0974b76407454a97e750d9055d0aa5e834e6739`  
		Last Modified: Thu, 20 Feb 2020 23:47:56 GMT  
		Size: 1.2 MB (1234698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7b673bbf243a89365a23ad683cd4498bf6d1d0ed02684c8a18d0a21cb8d178`  
		Last Modified: Thu, 20 Feb 2020 23:47:55 GMT  
		Size: 120.1 KB (120109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c24ab3064784c4410d659ea6e1f0df253d4425d982dc6458c3a3ba583e9b8ec5`  
		Last Modified: Thu, 20 Feb 2020 23:47:56 GMT  
		Size: 1.5 KB (1470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f98dd355d60f4139fe6bc5acd57c5dddf79d2130ae3198cc94d132632d3727`  
		Last Modified: Thu, 20 Feb 2020 23:47:56 GMT  
		Size: 570.8 KB (570766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9027f8cb6506a233c5d6eee529c13558fd054e963701cb92c8151588f40361cb`  
		Last Modified: Thu, 20 Feb 2020 23:47:55 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4` - linux; arm variant v7

```console
$ docker pull adminer@sha256:46b5ed40565812c4e0553a75ca1a4b5bffb897b489e88cb69626a97bb5de6a91
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.6 MB (28569758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f180ec2391291be9bea6f1f484659a40aa29806d769cebcb326e9b3da944208`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Sat, 18 Jan 2020 05:22:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 05:22:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 05:22:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 05:22:49 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 20 Feb 2020 21:11:31 GMT
ENV PHP_VERSION=7.4.3
# Thu, 20 Feb 2020 21:11:32 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.3.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.3.tar.xz.asc/from/this/mirror
# Thu, 20 Feb 2020 21:11:32 GMT
ENV PHP_SHA256=cf1f856d877c268124ded1ede40c9fb6142b125fdaafdc54f855120b8bc6982a PHP_MD5=
# Thu, 20 Feb 2020 21:11:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Feb 2020 21:11:37 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Feb 2020 21:13:57 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 20 Feb 2020 21:13:59 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 20 Feb 2020 21:14:01 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Feb 2020 21:14:02 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Feb 2020 21:14:02 GMT
CMD ["php" "-a"]
# Thu, 20 Feb 2020 23:50:58 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Thu, 20 Feb 2020 23:50:58 GMT
STOPSIGNAL SIGINT
# Thu, 20 Feb 2020 23:51:00 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 20 Feb 2020 23:51:02 GMT
WORKDIR /var/www/html
# Thu, 20 Feb 2020 23:51:04 GMT
RUN apk add --no-cache libpq
# Thu, 20 Feb 2020 23:51:35 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Thu, 20 Feb 2020 23:51:36 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Thu, 20 Feb 2020 23:51:37 GMT
ENV ADMINER_VERSION=4.7.6
# Thu, 20 Feb 2020 23:51:38 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Thu, 20 Feb 2020 23:51:39 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Thu, 20 Feb 2020 23:51:42 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Thu, 20 Feb 2020 23:51:43 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 20 Feb 2020 23:51:44 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Thu, 20 Feb 2020 23:51:45 GMT
USER adminer
# Thu, 20 Feb 2020 23:51:46 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 20 Feb 2020 23:51:47 GMT
EXPOSE 8080
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
	-	`sha256:6c492689366599e65cb0add947004a2dba1350bb15c7e6d5cf0926aba55ce6ec`  
		Last Modified: Thu, 20 Feb 2020 23:26:18 GMT  
		Size: 10.3 MB (10280256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e5617623e9ad0a01e633e336a37f6ff4d4a71c6cb1277692357d52303452d2f`  
		Last Modified: Thu, 20 Feb 2020 23:26:17 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4302d0c4f38943fda60770816f7eba1edb1d2f6a0c6f489e97ba67d9bdad574`  
		Last Modified: Thu, 20 Feb 2020 23:26:22 GMT  
		Size: 12.8 MB (12751449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc244875b6924b539df26879b4496e91b8eee4f5000e1ea5b774d83b9546b93`  
		Last Modified: Thu, 20 Feb 2020 23:26:18 GMT  
		Size: 2.2 KB (2214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04543010f9cd746143ced265c7b4b63d09ddc611588a131cbafe2099993fb5eb`  
		Last Modified: Thu, 20 Feb 2020 23:26:17 GMT  
		Size: 72.7 KB (72683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccb0170041c03fedc1121c07c7a06ee726f8a727c7c1eb5af04d1ee8f5654d5`  
		Last Modified: Thu, 20 Feb 2020 23:53:18 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1581d0fa71215a6ef8bb771f93fa001d361b8a02c3976b035408c6846e18be`  
		Last Modified: Thu, 20 Feb 2020 23:53:18 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f10e2f522b5d5b3116470d1761f55ab3feeb58372a087e3f6e80ea4f8f9dce7`  
		Last Modified: Thu, 20 Feb 2020 23:53:16 GMT  
		Size: 1.1 MB (1124902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c7b2368289baa2b3bc92adf31146c857cd78eecc8908bc78513c4f768c50323`  
		Last Modified: Thu, 20 Feb 2020 23:53:16 GMT  
		Size: 115.0 KB (114953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:765ac7cdcb3c5567be3929620bd1b2714a2af370ad604183f149ad40b19fd29c`  
		Last Modified: Thu, 20 Feb 2020 23:53:16 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45fe2c562cb0866875f0499d9583698863ee29b34a5a94406a42202b70885f6f`  
		Last Modified: Thu, 20 Feb 2020 23:53:16 GMT  
		Size: 570.8 KB (570772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e31dee670440ee2efcb54b84d9b9acccc709250fcb875c7ab9f31b21aded9fc`  
		Last Modified: Thu, 20 Feb 2020 23:53:16 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:d6ac77d178d83433a94f4c1ac85d37eb6bde9a3b5e2ddd70510ab8366580d72d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 MB (30795142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59720519dbc2aaa04f42da6be01d883724212b4503025e14148efe901e90b553`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Sat, 18 Jan 2020 02:29:26 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 02:29:26 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 02:29:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 02:29:29 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 24 Jan 2020 00:09:58 GMT
ENV PHP_VERSION=7.4.2
# Fri, 24 Jan 2020 00:10:02 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.2.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.2.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 00:10:03 GMT
ENV PHP_SHA256=98284deac017da0d426117ecae7599a1f1bf62ae3911e8bc16c4403a8f4bdf13 PHP_MD5=
# Fri, 24 Jan 2020 00:10:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 24 Jan 2020 00:10:10 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 00:14:01 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 00:14:05 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Fri, 24 Jan 2020 00:14:09 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 00:14:10 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 00:14:11 GMT
CMD ["php" "-a"]
# Fri, 24 Jan 2020 02:50:27 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 24 Jan 2020 02:50:28 GMT
STOPSIGNAL SIGINT
# Fri, 24 Jan 2020 02:50:32 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 24 Jan 2020 02:50:32 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 02:50:36 GMT
RUN apk add --no-cache libpq
# Fri, 24 Jan 2020 02:51:09 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Fri, 24 Jan 2020 02:51:10 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 31 Jan 2020 17:39:37 GMT
ENV ADMINER_VERSION=4.7.6
# Fri, 31 Jan 2020 17:39:37 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Fri, 31 Jan 2020 17:39:38 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Fri, 31 Jan 2020 17:39:40 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 31 Jan 2020 17:39:41 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 31 Jan 2020 17:39:42 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 31 Jan 2020 17:39:42 GMT
USER adminer
# Fri, 31 Jan 2020 17:39:43 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 31 Jan 2020 17:39:44 GMT
EXPOSE 8080
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
	-	`sha256:aa724be546925194dbbb305717c1ec1404bd825d4e768f5fa30758fc836a1dda`  
		Last Modified: Fri, 24 Jan 2020 02:37:49 GMT  
		Size: 10.3 MB (10271109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b0bc8c61926931859ef4bf710fb73b709a407ca1086dfe704e7654934b4bdd`  
		Last Modified: Fri, 24 Jan 2020 02:37:45 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07be412705d63c11275e2018adae846b8861d4f678a21f2c43e2c22ae0bcee6d`  
		Last Modified: Fri, 24 Jan 2020 02:37:49 GMT  
		Size: 14.4 MB (14366228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73cafd3dde7ad30752409223dc0b26b0a5f4fa98d9a875225e2566bd99806655`  
		Last Modified: Fri, 24 Jan 2020 02:37:45 GMT  
		Size: 2.2 KB (2216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59195632759b7e9a57fb9ac253284ecbea9055d01c12f9caa49d23ca8f40bc1c`  
		Last Modified: Fri, 24 Jan 2020 02:37:45 GMT  
		Size: 72.7 KB (72676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6576a2f957338815a3fd8d1023a31cbb8ef8592406942ab75483b02adbe1c384`  
		Last Modified: Fri, 24 Jan 2020 02:52:47 GMT  
		Size: 310.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f6446e74a0df8b21f4f9ad86cf10fa3f6b6a9231d643d4174a5ddd3cf84f184`  
		Last Modified: Fri, 24 Jan 2020 02:52:47 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b69655ccf3f62cf1149958c93543bc91f9addef901545f4c74831b5c65b29039`  
		Last Modified: Fri, 24 Jan 2020 02:52:44 GMT  
		Size: 1.3 MB (1299236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:986406fbe9d0af0aeacc6c7cc032415d7552b4fd8f3fe60ea2313caa9193649c`  
		Last Modified: Fri, 24 Jan 2020 02:52:44 GMT  
		Size: 124.7 KB (124696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:382b47ced56d800090d03dff8f4d1183a7209bfd39013db12812d2efc2a39f54`  
		Last Modified: Fri, 24 Jan 2020 02:52:44 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23f30f175d57f1ffdc2f5c4308d886c2f842ce1a163c77b1747b628a89684ac`  
		Last Modified: Fri, 31 Jan 2020 17:40:10 GMT  
		Size: 570.8 KB (570779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d5044dac86a165d99ffacf0aaeb789461f31935ef0847d4e80ae612f101599`  
		Last Modified: Fri, 31 Jan 2020 17:40:10 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4` - linux; 386

```console
$ docker pull adminer@sha256:d094fa6fd940847cd20c8dd698284d004cf1d6a5fa23d777f0b19667afa76346
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31684075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed77c13afb1993912752a1a0383da2185144a458fde112b713496146d193cb19`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Sat, 18 Jan 2020 05:41:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 05:41:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 05:41:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 05:41:39 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 23 Jan 2020 23:13:49 GMT
ENV PHP_VERSION=7.4.2
# Thu, 23 Jan 2020 23:13:49 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.2.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.2.tar.xz.asc/from/this/mirror
# Thu, 23 Jan 2020 23:13:49 GMT
ENV PHP_SHA256=98284deac017da0d426117ecae7599a1f1bf62ae3911e8bc16c4403a8f4bdf13 PHP_MD5=
# Thu, 23 Jan 2020 23:13:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 23 Jan 2020 23:13:52 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Jan 2020 23:21:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 23 Jan 2020 23:21:57 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 23 Jan 2020 23:21:59 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Jan 2020 23:21:59 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Jan 2020 23:22:00 GMT
CMD ["php" "-a"]
# Fri, 24 Jan 2020 07:25:41 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 24 Jan 2020 07:25:41 GMT
STOPSIGNAL SIGINT
# Fri, 24 Jan 2020 07:25:42 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 24 Jan 2020 07:25:42 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 07:25:43 GMT
RUN apk add --no-cache libpq
# Fri, 24 Jan 2020 07:26:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Fri, 24 Jan 2020 07:26:02 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 31 Jan 2020 17:38:17 GMT
ENV ADMINER_VERSION=4.7.6
# Fri, 31 Jan 2020 17:38:18 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Fri, 31 Jan 2020 17:38:18 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Fri, 31 Jan 2020 17:38:19 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 31 Jan 2020 17:38:19 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 31 Jan 2020 17:38:20 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 31 Jan 2020 17:38:20 GMT
USER adminer
# Fri, 31 Jan 2020 17:38:20 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 31 Jan 2020 17:38:20 GMT
EXPOSE 8080
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
	-	`sha256:9f3628b223c4b093cf7c2d7723ccd39dfcb6977a659c9c183e7673f22f44865b`  
		Last Modified: Fri, 24 Jan 2020 02:36:11 GMT  
		Size: 10.3 MB (10271099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e167c61f346105deafdbe6bff7f521715a3d31cd4c9ca27d6dca67654d916c`  
		Last Modified: Fri, 24 Jan 2020 02:36:08 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53425617927914b1561c930b3ce2f90644de41394e731ca71a5d66feeba55d5b`  
		Last Modified: Fri, 24 Jan 2020 02:36:19 GMT  
		Size: 15.0 MB (14974599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809347a8b4ae69caee1b666ac61ec86e0f2dd5d64744592a59f65fd9bb49c7c9`  
		Last Modified: Fri, 24 Jan 2020 02:36:10 GMT  
		Size: 2.2 KB (2216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31917077d16c99b9c58e44f9267cbda55763d759a59379d7e4ca1f9fd6acf60a`  
		Last Modified: Fri, 24 Jan 2020 02:36:09 GMT  
		Size: 72.3 KB (72331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc6ba5ae7aae77ac94c185eef225136d01333d8840f8896b412e359fa89e3ae6`  
		Last Modified: Fri, 24 Jan 2020 07:27:19 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aab9a7fed181e4a8d1621cf6e92e6b4525a242e1c102cac7a259b3336202c16`  
		Last Modified: Fri, 24 Jan 2020 07:27:19 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1120969ea66ac41447ffffddcda8e8d389a0a1c0c7feb7d9d650117b973459d`  
		Last Modified: Fri, 24 Jan 2020 07:27:18 GMT  
		Size: 1.4 MB (1397662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cf37d29a0120ccd9ef7f4f99c6d10673cd93097ebe961c86faf275c144f5929`  
		Last Modified: Fri, 24 Jan 2020 07:27:18 GMT  
		Size: 130.8 KB (130760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf17f4f8d6baa9c93722150405686cf214bc377adbb7ff2b891efe5ca38809c9`  
		Last Modified: Fri, 24 Jan 2020 07:27:18 GMT  
		Size: 1.5 KB (1472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cac8221b3739531c0e54a60c4d8d795c187ce863f2fb79955540c1b62347fbc7`  
		Last Modified: Fri, 31 Jan 2020 17:38:36 GMT  
		Size: 570.7 KB (570691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8127a70cc3e20105c94ab16913cab965e775aaa7cb37cc6398e47d4a1830241e`  
		Last Modified: Fri, 31 Jan 2020 17:38:36 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4` - linux; ppc64le

```console
$ docker pull adminer@sha256:8906a11939b6681a5c547d8a1b3d8e58493fb85a66ef14177592239c9cd3ab6f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32169343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:251a9f8c0d32635a09c63fc8d5e5fbad2fee09cca0a4ea7cca903b5d9ac6f815`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Sat, 18 Jan 2020 03:24:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:24:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:24:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 03:24:34 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 23 Jan 2020 23:32:44 GMT
ENV PHP_VERSION=7.4.2
# Thu, 23 Jan 2020 23:32:47 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.2.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.2.tar.xz.asc/from/this/mirror
# Thu, 23 Jan 2020 23:32:50 GMT
ENV PHP_SHA256=98284deac017da0d426117ecae7599a1f1bf62ae3911e8bc16c4403a8f4bdf13 PHP_MD5=
# Thu, 23 Jan 2020 23:33:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 23 Jan 2020 23:33:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Jan 2020 23:36:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 23 Jan 2020 23:36:54 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 23 Jan 2020 23:37:00 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Jan 2020 23:37:02 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Jan 2020 23:37:04 GMT
CMD ["php" "-a"]
# Fri, 24 Jan 2020 05:51:10 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 24 Jan 2020 05:51:12 GMT
STOPSIGNAL SIGINT
# Fri, 24 Jan 2020 05:51:17 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 24 Jan 2020 05:51:19 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 05:51:23 GMT
RUN apk add --no-cache libpq
# Fri, 24 Jan 2020 05:51:48 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Fri, 24 Jan 2020 05:51:50 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 31 Jan 2020 17:16:45 GMT
ENV ADMINER_VERSION=4.7.6
# Fri, 31 Jan 2020 17:16:48 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Fri, 31 Jan 2020 17:16:51 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Fri, 31 Jan 2020 17:17:00 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 31 Jan 2020 17:17:01 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 31 Jan 2020 17:17:03 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 31 Jan 2020 17:17:05 GMT
USER adminer
# Fri, 31 Jan 2020 17:17:08 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 31 Jan 2020 17:17:10 GMT
EXPOSE 8080
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
	-	`sha256:c24c1e693453ad6efa656fcfa28e76c0786f80b4467d83c277d1116117942973`  
		Last Modified: Fri, 24 Jan 2020 02:32:44 GMT  
		Size: 10.3 MB (10271124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb71fc05f0fe0d365d8b9891f304e0cf2c1f6f0d2200ecdc0ea9a1c569117a1d`  
		Last Modified: Fri, 24 Jan 2020 02:32:41 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf26116548345ee1f676a6c1fabb768cd60750eb7a3a0ac7f09724350dde3b1`  
		Last Modified: Fri, 24 Jan 2020 02:32:54 GMT  
		Size: 15.5 MB (15539990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc4f870d6f2e6bbade33c0f28534b50765c4b56a093dc7565bd3ec3b37a7c603`  
		Last Modified: Fri, 24 Jan 2020 02:32:41 GMT  
		Size: 2.2 KB (2211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6a738ee51d709e4c4db983f9206a240500a2fc0dbaf3c76f6da2f99e5f6eb3b`  
		Last Modified: Fri, 24 Jan 2020 02:32:41 GMT  
		Size: 73.0 KB (72992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47bf1b73f7bf1089b7cf019ae582b63d77fa46e6c5b2b4efc16b0bf9d9b1ad9a`  
		Last Modified: Fri, 24 Jan 2020 05:53:47 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f984dcaccfb46a5cafd49380217e97342575055ceaaab4ff65a67f43af2da028`  
		Last Modified: Fri, 24 Jan 2020 05:53:47 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9e4520026a60556f0b631a13532b9a39d91d8eae94d4d3514359ef189ce4c94`  
		Last Modified: Fri, 24 Jan 2020 05:53:45 GMT  
		Size: 1.4 MB (1350626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba57cd117c3f571c3379a3fbb16d112291f4de925499dfeaad0bc7966c9483fb`  
		Last Modified: Fri, 24 Jan 2020 05:53:44 GMT  
		Size: 135.9 KB (135919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faef1730db86976915b65b75f76c1a057c321a983034e019f37ec833f5a1ffc9`  
		Last Modified: Fri, 24 Jan 2020 05:53:44 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:620c9c1b5881ba0a3be097e7cb57c695406737868e7b1adc02c5561c5f7b1649`  
		Last Modified: Fri, 31 Jan 2020 17:18:05 GMT  
		Size: 570.8 KB (570776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03e77753eec72902172405ef4c8c0c667bf7377cd0dc6cc1441afd0890991d43`  
		Last Modified: Fri, 31 Jan 2020 17:18:04 GMT  
		Size: 501.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:4.7`

```console
$ docker pull adminer@sha256:c689401f4ee85e37ba2cd62d401af2d569833dd8efa2c338177889fa9c525882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `adminer:4.7` - linux; amd64

```console
$ docker pull adminer@sha256:6ceb642133ac56e267c50ae4bfb24ac0008b0eb02b772abae9059caa45211bee
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31058191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:259cc60bdb72538cffc06536d8bb73c3d9afd7156afc71b0c97fb1659917805e`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Sat, 18 Jan 2020 03:18:30 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:18:30 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:18:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 03:18:30 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 24 Jan 2020 07:05:12 GMT
ENV PHP_VERSION=7.4.2
# Fri, 24 Jan 2020 07:05:13 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.2.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.2.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 07:05:13 GMT
ENV PHP_SHA256=98284deac017da0d426117ecae7599a1f1bf62ae3911e8bc16c4403a8f4bdf13 PHP_MD5=
# Fri, 24 Jan 2020 07:05:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 24 Jan 2020 07:05:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 07:13:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 07:13:16 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Fri, 24 Jan 2020 07:13:17 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 07:13:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 07:13:17 GMT
CMD ["php" "-a"]
# Fri, 24 Jan 2020 10:52:17 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 24 Jan 2020 10:52:17 GMT
STOPSIGNAL SIGINT
# Fri, 24 Jan 2020 10:52:18 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 24 Jan 2020 10:52:18 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 10:52:19 GMT
RUN apk add --no-cache libpq
# Fri, 24 Jan 2020 10:52:38 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Fri, 24 Jan 2020 10:52:39 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 31 Jan 2020 17:19:26 GMT
ENV ADMINER_VERSION=4.7.6
# Fri, 31 Jan 2020 17:19:26 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Fri, 31 Jan 2020 17:19:26 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Fri, 31 Jan 2020 17:19:27 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 31 Jan 2020 17:19:28 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 31 Jan 2020 17:19:28 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 31 Jan 2020 17:19:28 GMT
USER adminer
# Fri, 31 Jan 2020 17:19:28 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 31 Jan 2020 17:19:28 GMT
EXPOSE 8080
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
	-	`sha256:5fa47f19b1e835f47f4c1273ccb215a42ee2aefafe300409d92b05b899a757d8`  
		Last Modified: Fri, 24 Jan 2020 10:39:33 GMT  
		Size: 10.3 MB (10271096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4556adb19ddcb43be3cd12b973f718e5edc74d6986ae4406a0c3011cbeb3dc93`  
		Last Modified: Fri, 24 Jan 2020 10:39:33 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:205de55b7ed0d389ac2c9777321f11ba9377a148002c2ef1d7b68d02a96472f3`  
		Last Modified: Fri, 24 Jan 2020 10:39:42 GMT  
		Size: 14.6 MB (14574023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c35aa7da966a732561c37c8b5d56949eedcb7865066b86da95c8bc58c18c48d2`  
		Last Modified: Fri, 24 Jan 2020 10:39:32 GMT  
		Size: 2.2 KB (2216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82a54ca6f814c156199e3266c4297efe2f54fb83bfb1645f53582eae3d1e222e`  
		Last Modified: Fri, 24 Jan 2020 10:39:33 GMT  
		Size: 73.1 KB (73145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e28f69f8cf7d397d8bd78cab68b9713275989e440016ec98580b94d0b0dc23f8`  
		Last Modified: Fri, 24 Jan 2020 10:53:42 GMT  
		Size: 306.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b527d0b89c2ea24dd10be7c18c1dcdf592fd4e1a5ff2c9da47fba2940fbb25a7`  
		Last Modified: Fri, 24 Jan 2020 10:53:42 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35b881820e3f1402cd2b2836dc6064db1b8ef029479448d5a058baa86b0f2e29`  
		Last Modified: Fri, 24 Jan 2020 10:53:41 GMT  
		Size: 1.3 MB (1277246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97e920225fdf7c9fc6bd8762ee3efbc9225341331c21812757347e46b22a2db3`  
		Last Modified: Fri, 24 Jan 2020 10:53:41 GMT  
		Size: 126.6 KB (126617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c8cde070aec4f16d202102cbdad6a161e48b4ffae4426da85717e9ee116fbec`  
		Last Modified: Fri, 24 Jan 2020 10:53:40 GMT  
		Size: 1.5 KB (1474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:028d5feebf26f852c8d09343a1b1ea1be953837a2f402743e1c021ea7b15ccee`  
		Last Modified: Fri, 31 Jan 2020 17:19:44 GMT  
		Size: 570.7 KB (570688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e0b9ec991cbee8b6377946c76367fcaa9782c4be8d265be834c5158b2638d40`  
		Last Modified: Fri, 31 Jan 2020 17:19:44 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7` - linux; arm variant v6

```console
$ docker pull adminer@sha256:086342d4149c1554e7c334711e0c6ccfa783ce0991cdd33d1687ca56e83020c7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.8 MB (29825140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08598589c478e6d488e3d5892d914c3ccac2ca333bf32b79046b127a04438a92`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Sat, 18 Jan 2020 03:40:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:40:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:40:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 03:40:19 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 20 Feb 2020 21:49:41 GMT
ENV PHP_VERSION=7.4.3
# Thu, 20 Feb 2020 21:49:43 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.3.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.3.tar.xz.asc/from/this/mirror
# Thu, 20 Feb 2020 21:49:44 GMT
ENV PHP_SHA256=cf1f856d877c268124ded1ede40c9fb6142b125fdaafdc54f855120b8bc6982a PHP_MD5=
# Thu, 20 Feb 2020 21:49:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Feb 2020 21:49:57 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Feb 2020 21:53:47 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 20 Feb 2020 21:53:50 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 20 Feb 2020 21:53:53 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Feb 2020 21:53:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Feb 2020 21:53:54 GMT
CMD ["php" "-a"]
# Thu, 20 Feb 2020 23:45:59 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Thu, 20 Feb 2020 23:45:59 GMT
STOPSIGNAL SIGINT
# Thu, 20 Feb 2020 23:46:02 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 20 Feb 2020 23:46:03 GMT
WORKDIR /var/www/html
# Thu, 20 Feb 2020 23:46:05 GMT
RUN apk add --no-cache libpq
# Thu, 20 Feb 2020 23:46:36 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Thu, 20 Feb 2020 23:46:39 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Thu, 20 Feb 2020 23:46:41 GMT
ENV ADMINER_VERSION=4.7.6
# Thu, 20 Feb 2020 23:46:41 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Thu, 20 Feb 2020 23:46:42 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Thu, 20 Feb 2020 23:46:45 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Thu, 20 Feb 2020 23:46:46 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 20 Feb 2020 23:46:46 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Thu, 20 Feb 2020 23:46:47 GMT
USER adminer
# Thu, 20 Feb 2020 23:46:48 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 20 Feb 2020 23:46:48 GMT
EXPOSE 8080
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
	-	`sha256:f246fe8b62d43a3f633a04898577258a2ce5dd84edf5fd464403b9a108b301e2`  
		Last Modified: Thu, 20 Feb 2020 23:10:06 GMT  
		Size: 10.3 MB (10280264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b4e0af10768397859f6f19eca4b17ee9f21d61a1cb06989aba861267cf1b6a`  
		Last Modified: Thu, 20 Feb 2020 23:10:05 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a228bdc8e070add11170637553b04b0eeab55a8af3159561b2878b3bcc00bbb`  
		Last Modified: Thu, 20 Feb 2020 23:10:11 GMT  
		Size: 13.6 MB (13600067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:936640ed543c6bb114e0374d4aa5d00b0ad989151337d4edfe6047bad672c605`  
		Last Modified: Thu, 20 Feb 2020 23:10:05 GMT  
		Size: 2.2 KB (2214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071eed09e44daa0c7c7d337a517208fa4a3c08e02029c0970082688456496bec`  
		Last Modified: Thu, 20 Feb 2020 23:10:05 GMT  
		Size: 72.7 KB (72679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:500b89ded2f6c4841beacd80fbbc9393d964cc71bd39c391faf7dc97822dbdb9`  
		Last Modified: Thu, 20 Feb 2020 23:47:57 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512f9b08d8b23f60cb6dff75b2270418b1aef35536dd655abbebc984b88a251b`  
		Last Modified: Thu, 20 Feb 2020 23:47:58 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c471a8e9c45607043e4014b7f0974b76407454a97e750d9055d0aa5e834e6739`  
		Last Modified: Thu, 20 Feb 2020 23:47:56 GMT  
		Size: 1.2 MB (1234698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7b673bbf243a89365a23ad683cd4498bf6d1d0ed02684c8a18d0a21cb8d178`  
		Last Modified: Thu, 20 Feb 2020 23:47:55 GMT  
		Size: 120.1 KB (120109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c24ab3064784c4410d659ea6e1f0df253d4425d982dc6458c3a3ba583e9b8ec5`  
		Last Modified: Thu, 20 Feb 2020 23:47:56 GMT  
		Size: 1.5 KB (1470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f98dd355d60f4139fe6bc5acd57c5dddf79d2130ae3198cc94d132632d3727`  
		Last Modified: Thu, 20 Feb 2020 23:47:56 GMT  
		Size: 570.8 KB (570766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9027f8cb6506a233c5d6eee529c13558fd054e963701cb92c8151588f40361cb`  
		Last Modified: Thu, 20 Feb 2020 23:47:55 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7` - linux; arm variant v7

```console
$ docker pull adminer@sha256:46b5ed40565812c4e0553a75ca1a4b5bffb897b489e88cb69626a97bb5de6a91
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.6 MB (28569758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f180ec2391291be9bea6f1f484659a40aa29806d769cebcb326e9b3da944208`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Sat, 18 Jan 2020 05:22:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 05:22:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 05:22:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 05:22:49 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 20 Feb 2020 21:11:31 GMT
ENV PHP_VERSION=7.4.3
# Thu, 20 Feb 2020 21:11:32 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.3.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.3.tar.xz.asc/from/this/mirror
# Thu, 20 Feb 2020 21:11:32 GMT
ENV PHP_SHA256=cf1f856d877c268124ded1ede40c9fb6142b125fdaafdc54f855120b8bc6982a PHP_MD5=
# Thu, 20 Feb 2020 21:11:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Feb 2020 21:11:37 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Feb 2020 21:13:57 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 20 Feb 2020 21:13:59 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 20 Feb 2020 21:14:01 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Feb 2020 21:14:02 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Feb 2020 21:14:02 GMT
CMD ["php" "-a"]
# Thu, 20 Feb 2020 23:50:58 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Thu, 20 Feb 2020 23:50:58 GMT
STOPSIGNAL SIGINT
# Thu, 20 Feb 2020 23:51:00 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 20 Feb 2020 23:51:02 GMT
WORKDIR /var/www/html
# Thu, 20 Feb 2020 23:51:04 GMT
RUN apk add --no-cache libpq
# Thu, 20 Feb 2020 23:51:35 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Thu, 20 Feb 2020 23:51:36 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Thu, 20 Feb 2020 23:51:37 GMT
ENV ADMINER_VERSION=4.7.6
# Thu, 20 Feb 2020 23:51:38 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Thu, 20 Feb 2020 23:51:39 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Thu, 20 Feb 2020 23:51:42 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Thu, 20 Feb 2020 23:51:43 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 20 Feb 2020 23:51:44 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Thu, 20 Feb 2020 23:51:45 GMT
USER adminer
# Thu, 20 Feb 2020 23:51:46 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 20 Feb 2020 23:51:47 GMT
EXPOSE 8080
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
	-	`sha256:6c492689366599e65cb0add947004a2dba1350bb15c7e6d5cf0926aba55ce6ec`  
		Last Modified: Thu, 20 Feb 2020 23:26:18 GMT  
		Size: 10.3 MB (10280256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e5617623e9ad0a01e633e336a37f6ff4d4a71c6cb1277692357d52303452d2f`  
		Last Modified: Thu, 20 Feb 2020 23:26:17 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4302d0c4f38943fda60770816f7eba1edb1d2f6a0c6f489e97ba67d9bdad574`  
		Last Modified: Thu, 20 Feb 2020 23:26:22 GMT  
		Size: 12.8 MB (12751449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc244875b6924b539df26879b4496e91b8eee4f5000e1ea5b774d83b9546b93`  
		Last Modified: Thu, 20 Feb 2020 23:26:18 GMT  
		Size: 2.2 KB (2214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04543010f9cd746143ced265c7b4b63d09ddc611588a131cbafe2099993fb5eb`  
		Last Modified: Thu, 20 Feb 2020 23:26:17 GMT  
		Size: 72.7 KB (72683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccb0170041c03fedc1121c07c7a06ee726f8a727c7c1eb5af04d1ee8f5654d5`  
		Last Modified: Thu, 20 Feb 2020 23:53:18 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1581d0fa71215a6ef8bb771f93fa001d361b8a02c3976b035408c6846e18be`  
		Last Modified: Thu, 20 Feb 2020 23:53:18 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f10e2f522b5d5b3116470d1761f55ab3feeb58372a087e3f6e80ea4f8f9dce7`  
		Last Modified: Thu, 20 Feb 2020 23:53:16 GMT  
		Size: 1.1 MB (1124902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c7b2368289baa2b3bc92adf31146c857cd78eecc8908bc78513c4f768c50323`  
		Last Modified: Thu, 20 Feb 2020 23:53:16 GMT  
		Size: 115.0 KB (114953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:765ac7cdcb3c5567be3929620bd1b2714a2af370ad604183f149ad40b19fd29c`  
		Last Modified: Thu, 20 Feb 2020 23:53:16 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45fe2c562cb0866875f0499d9583698863ee29b34a5a94406a42202b70885f6f`  
		Last Modified: Thu, 20 Feb 2020 23:53:16 GMT  
		Size: 570.8 KB (570772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e31dee670440ee2efcb54b84d9b9acccc709250fcb875c7ab9f31b21aded9fc`  
		Last Modified: Thu, 20 Feb 2020 23:53:16 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:d6ac77d178d83433a94f4c1ac85d37eb6bde9a3b5e2ddd70510ab8366580d72d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 MB (30795142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59720519dbc2aaa04f42da6be01d883724212b4503025e14148efe901e90b553`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Sat, 18 Jan 2020 02:29:26 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 02:29:26 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 02:29:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 02:29:29 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 24 Jan 2020 00:09:58 GMT
ENV PHP_VERSION=7.4.2
# Fri, 24 Jan 2020 00:10:02 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.2.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.2.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 00:10:03 GMT
ENV PHP_SHA256=98284deac017da0d426117ecae7599a1f1bf62ae3911e8bc16c4403a8f4bdf13 PHP_MD5=
# Fri, 24 Jan 2020 00:10:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 24 Jan 2020 00:10:10 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 00:14:01 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 00:14:05 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Fri, 24 Jan 2020 00:14:09 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 00:14:10 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 00:14:11 GMT
CMD ["php" "-a"]
# Fri, 24 Jan 2020 02:50:27 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 24 Jan 2020 02:50:28 GMT
STOPSIGNAL SIGINT
# Fri, 24 Jan 2020 02:50:32 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 24 Jan 2020 02:50:32 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 02:50:36 GMT
RUN apk add --no-cache libpq
# Fri, 24 Jan 2020 02:51:09 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Fri, 24 Jan 2020 02:51:10 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 31 Jan 2020 17:39:37 GMT
ENV ADMINER_VERSION=4.7.6
# Fri, 31 Jan 2020 17:39:37 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Fri, 31 Jan 2020 17:39:38 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Fri, 31 Jan 2020 17:39:40 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 31 Jan 2020 17:39:41 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 31 Jan 2020 17:39:42 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 31 Jan 2020 17:39:42 GMT
USER adminer
# Fri, 31 Jan 2020 17:39:43 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 31 Jan 2020 17:39:44 GMT
EXPOSE 8080
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
	-	`sha256:aa724be546925194dbbb305717c1ec1404bd825d4e768f5fa30758fc836a1dda`  
		Last Modified: Fri, 24 Jan 2020 02:37:49 GMT  
		Size: 10.3 MB (10271109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b0bc8c61926931859ef4bf710fb73b709a407ca1086dfe704e7654934b4bdd`  
		Last Modified: Fri, 24 Jan 2020 02:37:45 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07be412705d63c11275e2018adae846b8861d4f678a21f2c43e2c22ae0bcee6d`  
		Last Modified: Fri, 24 Jan 2020 02:37:49 GMT  
		Size: 14.4 MB (14366228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73cafd3dde7ad30752409223dc0b26b0a5f4fa98d9a875225e2566bd99806655`  
		Last Modified: Fri, 24 Jan 2020 02:37:45 GMT  
		Size: 2.2 KB (2216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59195632759b7e9a57fb9ac253284ecbea9055d01c12f9caa49d23ca8f40bc1c`  
		Last Modified: Fri, 24 Jan 2020 02:37:45 GMT  
		Size: 72.7 KB (72676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6576a2f957338815a3fd8d1023a31cbb8ef8592406942ab75483b02adbe1c384`  
		Last Modified: Fri, 24 Jan 2020 02:52:47 GMT  
		Size: 310.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f6446e74a0df8b21f4f9ad86cf10fa3f6b6a9231d643d4174a5ddd3cf84f184`  
		Last Modified: Fri, 24 Jan 2020 02:52:47 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b69655ccf3f62cf1149958c93543bc91f9addef901545f4c74831b5c65b29039`  
		Last Modified: Fri, 24 Jan 2020 02:52:44 GMT  
		Size: 1.3 MB (1299236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:986406fbe9d0af0aeacc6c7cc032415d7552b4fd8f3fe60ea2313caa9193649c`  
		Last Modified: Fri, 24 Jan 2020 02:52:44 GMT  
		Size: 124.7 KB (124696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:382b47ced56d800090d03dff8f4d1183a7209bfd39013db12812d2efc2a39f54`  
		Last Modified: Fri, 24 Jan 2020 02:52:44 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23f30f175d57f1ffdc2f5c4308d886c2f842ce1a163c77b1747b628a89684ac`  
		Last Modified: Fri, 31 Jan 2020 17:40:10 GMT  
		Size: 570.8 KB (570779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d5044dac86a165d99ffacf0aaeb789461f31935ef0847d4e80ae612f101599`  
		Last Modified: Fri, 31 Jan 2020 17:40:10 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7` - linux; 386

```console
$ docker pull adminer@sha256:d094fa6fd940847cd20c8dd698284d004cf1d6a5fa23d777f0b19667afa76346
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31684075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed77c13afb1993912752a1a0383da2185144a458fde112b713496146d193cb19`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Sat, 18 Jan 2020 05:41:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 05:41:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 05:41:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 05:41:39 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 23 Jan 2020 23:13:49 GMT
ENV PHP_VERSION=7.4.2
# Thu, 23 Jan 2020 23:13:49 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.2.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.2.tar.xz.asc/from/this/mirror
# Thu, 23 Jan 2020 23:13:49 GMT
ENV PHP_SHA256=98284deac017da0d426117ecae7599a1f1bf62ae3911e8bc16c4403a8f4bdf13 PHP_MD5=
# Thu, 23 Jan 2020 23:13:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 23 Jan 2020 23:13:52 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Jan 2020 23:21:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 23 Jan 2020 23:21:57 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 23 Jan 2020 23:21:59 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Jan 2020 23:21:59 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Jan 2020 23:22:00 GMT
CMD ["php" "-a"]
# Fri, 24 Jan 2020 07:25:41 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 24 Jan 2020 07:25:41 GMT
STOPSIGNAL SIGINT
# Fri, 24 Jan 2020 07:25:42 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 24 Jan 2020 07:25:42 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 07:25:43 GMT
RUN apk add --no-cache libpq
# Fri, 24 Jan 2020 07:26:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Fri, 24 Jan 2020 07:26:02 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 31 Jan 2020 17:38:17 GMT
ENV ADMINER_VERSION=4.7.6
# Fri, 31 Jan 2020 17:38:18 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Fri, 31 Jan 2020 17:38:18 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Fri, 31 Jan 2020 17:38:19 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 31 Jan 2020 17:38:19 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 31 Jan 2020 17:38:20 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 31 Jan 2020 17:38:20 GMT
USER adminer
# Fri, 31 Jan 2020 17:38:20 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 31 Jan 2020 17:38:20 GMT
EXPOSE 8080
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
	-	`sha256:9f3628b223c4b093cf7c2d7723ccd39dfcb6977a659c9c183e7673f22f44865b`  
		Last Modified: Fri, 24 Jan 2020 02:36:11 GMT  
		Size: 10.3 MB (10271099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e167c61f346105deafdbe6bff7f521715a3d31cd4c9ca27d6dca67654d916c`  
		Last Modified: Fri, 24 Jan 2020 02:36:08 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53425617927914b1561c930b3ce2f90644de41394e731ca71a5d66feeba55d5b`  
		Last Modified: Fri, 24 Jan 2020 02:36:19 GMT  
		Size: 15.0 MB (14974599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809347a8b4ae69caee1b666ac61ec86e0f2dd5d64744592a59f65fd9bb49c7c9`  
		Last Modified: Fri, 24 Jan 2020 02:36:10 GMT  
		Size: 2.2 KB (2216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31917077d16c99b9c58e44f9267cbda55763d759a59379d7e4ca1f9fd6acf60a`  
		Last Modified: Fri, 24 Jan 2020 02:36:09 GMT  
		Size: 72.3 KB (72331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc6ba5ae7aae77ac94c185eef225136d01333d8840f8896b412e359fa89e3ae6`  
		Last Modified: Fri, 24 Jan 2020 07:27:19 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aab9a7fed181e4a8d1621cf6e92e6b4525a242e1c102cac7a259b3336202c16`  
		Last Modified: Fri, 24 Jan 2020 07:27:19 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1120969ea66ac41447ffffddcda8e8d389a0a1c0c7feb7d9d650117b973459d`  
		Last Modified: Fri, 24 Jan 2020 07:27:18 GMT  
		Size: 1.4 MB (1397662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cf37d29a0120ccd9ef7f4f99c6d10673cd93097ebe961c86faf275c144f5929`  
		Last Modified: Fri, 24 Jan 2020 07:27:18 GMT  
		Size: 130.8 KB (130760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf17f4f8d6baa9c93722150405686cf214bc377adbb7ff2b891efe5ca38809c9`  
		Last Modified: Fri, 24 Jan 2020 07:27:18 GMT  
		Size: 1.5 KB (1472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cac8221b3739531c0e54a60c4d8d795c187ce863f2fb79955540c1b62347fbc7`  
		Last Modified: Fri, 31 Jan 2020 17:38:36 GMT  
		Size: 570.7 KB (570691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8127a70cc3e20105c94ab16913cab965e775aaa7cb37cc6398e47d4a1830241e`  
		Last Modified: Fri, 31 Jan 2020 17:38:36 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7` - linux; ppc64le

```console
$ docker pull adminer@sha256:8906a11939b6681a5c547d8a1b3d8e58493fb85a66ef14177592239c9cd3ab6f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32169343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:251a9f8c0d32635a09c63fc8d5e5fbad2fee09cca0a4ea7cca903b5d9ac6f815`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Sat, 18 Jan 2020 03:24:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:24:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:24:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 03:24:34 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 23 Jan 2020 23:32:44 GMT
ENV PHP_VERSION=7.4.2
# Thu, 23 Jan 2020 23:32:47 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.2.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.2.tar.xz.asc/from/this/mirror
# Thu, 23 Jan 2020 23:32:50 GMT
ENV PHP_SHA256=98284deac017da0d426117ecae7599a1f1bf62ae3911e8bc16c4403a8f4bdf13 PHP_MD5=
# Thu, 23 Jan 2020 23:33:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 23 Jan 2020 23:33:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Jan 2020 23:36:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 23 Jan 2020 23:36:54 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 23 Jan 2020 23:37:00 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Jan 2020 23:37:02 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Jan 2020 23:37:04 GMT
CMD ["php" "-a"]
# Fri, 24 Jan 2020 05:51:10 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 24 Jan 2020 05:51:12 GMT
STOPSIGNAL SIGINT
# Fri, 24 Jan 2020 05:51:17 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 24 Jan 2020 05:51:19 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 05:51:23 GMT
RUN apk add --no-cache libpq
# Fri, 24 Jan 2020 05:51:48 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Fri, 24 Jan 2020 05:51:50 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 31 Jan 2020 17:16:45 GMT
ENV ADMINER_VERSION=4.7.6
# Fri, 31 Jan 2020 17:16:48 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Fri, 31 Jan 2020 17:16:51 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Fri, 31 Jan 2020 17:17:00 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 31 Jan 2020 17:17:01 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 31 Jan 2020 17:17:03 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 31 Jan 2020 17:17:05 GMT
USER adminer
# Fri, 31 Jan 2020 17:17:08 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 31 Jan 2020 17:17:10 GMT
EXPOSE 8080
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
	-	`sha256:c24c1e693453ad6efa656fcfa28e76c0786f80b4467d83c277d1116117942973`  
		Last Modified: Fri, 24 Jan 2020 02:32:44 GMT  
		Size: 10.3 MB (10271124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb71fc05f0fe0d365d8b9891f304e0cf2c1f6f0d2200ecdc0ea9a1c569117a1d`  
		Last Modified: Fri, 24 Jan 2020 02:32:41 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf26116548345ee1f676a6c1fabb768cd60750eb7a3a0ac7f09724350dde3b1`  
		Last Modified: Fri, 24 Jan 2020 02:32:54 GMT  
		Size: 15.5 MB (15539990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc4f870d6f2e6bbade33c0f28534b50765c4b56a093dc7565bd3ec3b37a7c603`  
		Last Modified: Fri, 24 Jan 2020 02:32:41 GMT  
		Size: 2.2 KB (2211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6a738ee51d709e4c4db983f9206a240500a2fc0dbaf3c76f6da2f99e5f6eb3b`  
		Last Modified: Fri, 24 Jan 2020 02:32:41 GMT  
		Size: 73.0 KB (72992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47bf1b73f7bf1089b7cf019ae582b63d77fa46e6c5b2b4efc16b0bf9d9b1ad9a`  
		Last Modified: Fri, 24 Jan 2020 05:53:47 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f984dcaccfb46a5cafd49380217e97342575055ceaaab4ff65a67f43af2da028`  
		Last Modified: Fri, 24 Jan 2020 05:53:47 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9e4520026a60556f0b631a13532b9a39d91d8eae94d4d3514359ef189ce4c94`  
		Last Modified: Fri, 24 Jan 2020 05:53:45 GMT  
		Size: 1.4 MB (1350626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba57cd117c3f571c3379a3fbb16d112291f4de925499dfeaad0bc7966c9483fb`  
		Last Modified: Fri, 24 Jan 2020 05:53:44 GMT  
		Size: 135.9 KB (135919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faef1730db86976915b65b75f76c1a057c321a983034e019f37ec833f5a1ffc9`  
		Last Modified: Fri, 24 Jan 2020 05:53:44 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:620c9c1b5881ba0a3be097e7cb57c695406737868e7b1adc02c5561c5f7b1649`  
		Last Modified: Fri, 31 Jan 2020 17:18:05 GMT  
		Size: 570.8 KB (570776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03e77753eec72902172405ef4c8c0c667bf7377cd0dc6cc1441afd0890991d43`  
		Last Modified: Fri, 31 Jan 2020 17:18:04 GMT  
		Size: 501.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:4.7.6`

```console
$ docker pull adminer@sha256:c689401f4ee85e37ba2cd62d401af2d569833dd8efa2c338177889fa9c525882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `adminer:4.7.6` - linux; amd64

```console
$ docker pull adminer@sha256:6ceb642133ac56e267c50ae4bfb24ac0008b0eb02b772abae9059caa45211bee
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31058191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:259cc60bdb72538cffc06536d8bb73c3d9afd7156afc71b0c97fb1659917805e`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Sat, 18 Jan 2020 03:18:30 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:18:30 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:18:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 03:18:30 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 24 Jan 2020 07:05:12 GMT
ENV PHP_VERSION=7.4.2
# Fri, 24 Jan 2020 07:05:13 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.2.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.2.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 07:05:13 GMT
ENV PHP_SHA256=98284deac017da0d426117ecae7599a1f1bf62ae3911e8bc16c4403a8f4bdf13 PHP_MD5=
# Fri, 24 Jan 2020 07:05:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 24 Jan 2020 07:05:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 07:13:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 07:13:16 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Fri, 24 Jan 2020 07:13:17 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 07:13:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 07:13:17 GMT
CMD ["php" "-a"]
# Fri, 24 Jan 2020 10:52:17 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 24 Jan 2020 10:52:17 GMT
STOPSIGNAL SIGINT
# Fri, 24 Jan 2020 10:52:18 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 24 Jan 2020 10:52:18 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 10:52:19 GMT
RUN apk add --no-cache libpq
# Fri, 24 Jan 2020 10:52:38 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Fri, 24 Jan 2020 10:52:39 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 31 Jan 2020 17:19:26 GMT
ENV ADMINER_VERSION=4.7.6
# Fri, 31 Jan 2020 17:19:26 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Fri, 31 Jan 2020 17:19:26 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Fri, 31 Jan 2020 17:19:27 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 31 Jan 2020 17:19:28 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 31 Jan 2020 17:19:28 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 31 Jan 2020 17:19:28 GMT
USER adminer
# Fri, 31 Jan 2020 17:19:28 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 31 Jan 2020 17:19:28 GMT
EXPOSE 8080
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
	-	`sha256:5fa47f19b1e835f47f4c1273ccb215a42ee2aefafe300409d92b05b899a757d8`  
		Last Modified: Fri, 24 Jan 2020 10:39:33 GMT  
		Size: 10.3 MB (10271096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4556adb19ddcb43be3cd12b973f718e5edc74d6986ae4406a0c3011cbeb3dc93`  
		Last Modified: Fri, 24 Jan 2020 10:39:33 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:205de55b7ed0d389ac2c9777321f11ba9377a148002c2ef1d7b68d02a96472f3`  
		Last Modified: Fri, 24 Jan 2020 10:39:42 GMT  
		Size: 14.6 MB (14574023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c35aa7da966a732561c37c8b5d56949eedcb7865066b86da95c8bc58c18c48d2`  
		Last Modified: Fri, 24 Jan 2020 10:39:32 GMT  
		Size: 2.2 KB (2216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82a54ca6f814c156199e3266c4297efe2f54fb83bfb1645f53582eae3d1e222e`  
		Last Modified: Fri, 24 Jan 2020 10:39:33 GMT  
		Size: 73.1 KB (73145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e28f69f8cf7d397d8bd78cab68b9713275989e440016ec98580b94d0b0dc23f8`  
		Last Modified: Fri, 24 Jan 2020 10:53:42 GMT  
		Size: 306.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b527d0b89c2ea24dd10be7c18c1dcdf592fd4e1a5ff2c9da47fba2940fbb25a7`  
		Last Modified: Fri, 24 Jan 2020 10:53:42 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35b881820e3f1402cd2b2836dc6064db1b8ef029479448d5a058baa86b0f2e29`  
		Last Modified: Fri, 24 Jan 2020 10:53:41 GMT  
		Size: 1.3 MB (1277246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97e920225fdf7c9fc6bd8762ee3efbc9225341331c21812757347e46b22a2db3`  
		Last Modified: Fri, 24 Jan 2020 10:53:41 GMT  
		Size: 126.6 KB (126617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c8cde070aec4f16d202102cbdad6a161e48b4ffae4426da85717e9ee116fbec`  
		Last Modified: Fri, 24 Jan 2020 10:53:40 GMT  
		Size: 1.5 KB (1474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:028d5feebf26f852c8d09343a1b1ea1be953837a2f402743e1c021ea7b15ccee`  
		Last Modified: Fri, 31 Jan 2020 17:19:44 GMT  
		Size: 570.7 KB (570688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e0b9ec991cbee8b6377946c76367fcaa9782c4be8d265be834c5158b2638d40`  
		Last Modified: Fri, 31 Jan 2020 17:19:44 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7.6` - linux; arm variant v6

```console
$ docker pull adminer@sha256:086342d4149c1554e7c334711e0c6ccfa783ce0991cdd33d1687ca56e83020c7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.8 MB (29825140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08598589c478e6d488e3d5892d914c3ccac2ca333bf32b79046b127a04438a92`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Sat, 18 Jan 2020 03:40:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:40:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:40:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 03:40:19 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 20 Feb 2020 21:49:41 GMT
ENV PHP_VERSION=7.4.3
# Thu, 20 Feb 2020 21:49:43 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.3.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.3.tar.xz.asc/from/this/mirror
# Thu, 20 Feb 2020 21:49:44 GMT
ENV PHP_SHA256=cf1f856d877c268124ded1ede40c9fb6142b125fdaafdc54f855120b8bc6982a PHP_MD5=
# Thu, 20 Feb 2020 21:49:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Feb 2020 21:49:57 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Feb 2020 21:53:47 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 20 Feb 2020 21:53:50 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 20 Feb 2020 21:53:53 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Feb 2020 21:53:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Feb 2020 21:53:54 GMT
CMD ["php" "-a"]
# Thu, 20 Feb 2020 23:45:59 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Thu, 20 Feb 2020 23:45:59 GMT
STOPSIGNAL SIGINT
# Thu, 20 Feb 2020 23:46:02 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 20 Feb 2020 23:46:03 GMT
WORKDIR /var/www/html
# Thu, 20 Feb 2020 23:46:05 GMT
RUN apk add --no-cache libpq
# Thu, 20 Feb 2020 23:46:36 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Thu, 20 Feb 2020 23:46:39 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Thu, 20 Feb 2020 23:46:41 GMT
ENV ADMINER_VERSION=4.7.6
# Thu, 20 Feb 2020 23:46:41 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Thu, 20 Feb 2020 23:46:42 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Thu, 20 Feb 2020 23:46:45 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Thu, 20 Feb 2020 23:46:46 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 20 Feb 2020 23:46:46 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Thu, 20 Feb 2020 23:46:47 GMT
USER adminer
# Thu, 20 Feb 2020 23:46:48 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 20 Feb 2020 23:46:48 GMT
EXPOSE 8080
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
	-	`sha256:f246fe8b62d43a3f633a04898577258a2ce5dd84edf5fd464403b9a108b301e2`  
		Last Modified: Thu, 20 Feb 2020 23:10:06 GMT  
		Size: 10.3 MB (10280264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b4e0af10768397859f6f19eca4b17ee9f21d61a1cb06989aba861267cf1b6a`  
		Last Modified: Thu, 20 Feb 2020 23:10:05 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a228bdc8e070add11170637553b04b0eeab55a8af3159561b2878b3bcc00bbb`  
		Last Modified: Thu, 20 Feb 2020 23:10:11 GMT  
		Size: 13.6 MB (13600067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:936640ed543c6bb114e0374d4aa5d00b0ad989151337d4edfe6047bad672c605`  
		Last Modified: Thu, 20 Feb 2020 23:10:05 GMT  
		Size: 2.2 KB (2214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071eed09e44daa0c7c7d337a517208fa4a3c08e02029c0970082688456496bec`  
		Last Modified: Thu, 20 Feb 2020 23:10:05 GMT  
		Size: 72.7 KB (72679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:500b89ded2f6c4841beacd80fbbc9393d964cc71bd39c391faf7dc97822dbdb9`  
		Last Modified: Thu, 20 Feb 2020 23:47:57 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512f9b08d8b23f60cb6dff75b2270418b1aef35536dd655abbebc984b88a251b`  
		Last Modified: Thu, 20 Feb 2020 23:47:58 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c471a8e9c45607043e4014b7f0974b76407454a97e750d9055d0aa5e834e6739`  
		Last Modified: Thu, 20 Feb 2020 23:47:56 GMT  
		Size: 1.2 MB (1234698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7b673bbf243a89365a23ad683cd4498bf6d1d0ed02684c8a18d0a21cb8d178`  
		Last Modified: Thu, 20 Feb 2020 23:47:55 GMT  
		Size: 120.1 KB (120109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c24ab3064784c4410d659ea6e1f0df253d4425d982dc6458c3a3ba583e9b8ec5`  
		Last Modified: Thu, 20 Feb 2020 23:47:56 GMT  
		Size: 1.5 KB (1470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f98dd355d60f4139fe6bc5acd57c5dddf79d2130ae3198cc94d132632d3727`  
		Last Modified: Thu, 20 Feb 2020 23:47:56 GMT  
		Size: 570.8 KB (570766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9027f8cb6506a233c5d6eee529c13558fd054e963701cb92c8151588f40361cb`  
		Last Modified: Thu, 20 Feb 2020 23:47:55 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7.6` - linux; arm variant v7

```console
$ docker pull adminer@sha256:46b5ed40565812c4e0553a75ca1a4b5bffb897b489e88cb69626a97bb5de6a91
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.6 MB (28569758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f180ec2391291be9bea6f1f484659a40aa29806d769cebcb326e9b3da944208`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Sat, 18 Jan 2020 05:22:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 05:22:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 05:22:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 05:22:49 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 20 Feb 2020 21:11:31 GMT
ENV PHP_VERSION=7.4.3
# Thu, 20 Feb 2020 21:11:32 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.3.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.3.tar.xz.asc/from/this/mirror
# Thu, 20 Feb 2020 21:11:32 GMT
ENV PHP_SHA256=cf1f856d877c268124ded1ede40c9fb6142b125fdaafdc54f855120b8bc6982a PHP_MD5=
# Thu, 20 Feb 2020 21:11:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Feb 2020 21:11:37 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Feb 2020 21:13:57 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 20 Feb 2020 21:13:59 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 20 Feb 2020 21:14:01 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Feb 2020 21:14:02 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Feb 2020 21:14:02 GMT
CMD ["php" "-a"]
# Thu, 20 Feb 2020 23:50:58 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Thu, 20 Feb 2020 23:50:58 GMT
STOPSIGNAL SIGINT
# Thu, 20 Feb 2020 23:51:00 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 20 Feb 2020 23:51:02 GMT
WORKDIR /var/www/html
# Thu, 20 Feb 2020 23:51:04 GMT
RUN apk add --no-cache libpq
# Thu, 20 Feb 2020 23:51:35 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Thu, 20 Feb 2020 23:51:36 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Thu, 20 Feb 2020 23:51:37 GMT
ENV ADMINER_VERSION=4.7.6
# Thu, 20 Feb 2020 23:51:38 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Thu, 20 Feb 2020 23:51:39 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Thu, 20 Feb 2020 23:51:42 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Thu, 20 Feb 2020 23:51:43 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 20 Feb 2020 23:51:44 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Thu, 20 Feb 2020 23:51:45 GMT
USER adminer
# Thu, 20 Feb 2020 23:51:46 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 20 Feb 2020 23:51:47 GMT
EXPOSE 8080
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
	-	`sha256:6c492689366599e65cb0add947004a2dba1350bb15c7e6d5cf0926aba55ce6ec`  
		Last Modified: Thu, 20 Feb 2020 23:26:18 GMT  
		Size: 10.3 MB (10280256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e5617623e9ad0a01e633e336a37f6ff4d4a71c6cb1277692357d52303452d2f`  
		Last Modified: Thu, 20 Feb 2020 23:26:17 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4302d0c4f38943fda60770816f7eba1edb1d2f6a0c6f489e97ba67d9bdad574`  
		Last Modified: Thu, 20 Feb 2020 23:26:22 GMT  
		Size: 12.8 MB (12751449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc244875b6924b539df26879b4496e91b8eee4f5000e1ea5b774d83b9546b93`  
		Last Modified: Thu, 20 Feb 2020 23:26:18 GMT  
		Size: 2.2 KB (2214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04543010f9cd746143ced265c7b4b63d09ddc611588a131cbafe2099993fb5eb`  
		Last Modified: Thu, 20 Feb 2020 23:26:17 GMT  
		Size: 72.7 KB (72683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccb0170041c03fedc1121c07c7a06ee726f8a727c7c1eb5af04d1ee8f5654d5`  
		Last Modified: Thu, 20 Feb 2020 23:53:18 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1581d0fa71215a6ef8bb771f93fa001d361b8a02c3976b035408c6846e18be`  
		Last Modified: Thu, 20 Feb 2020 23:53:18 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f10e2f522b5d5b3116470d1761f55ab3feeb58372a087e3f6e80ea4f8f9dce7`  
		Last Modified: Thu, 20 Feb 2020 23:53:16 GMT  
		Size: 1.1 MB (1124902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c7b2368289baa2b3bc92adf31146c857cd78eecc8908bc78513c4f768c50323`  
		Last Modified: Thu, 20 Feb 2020 23:53:16 GMT  
		Size: 115.0 KB (114953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:765ac7cdcb3c5567be3929620bd1b2714a2af370ad604183f149ad40b19fd29c`  
		Last Modified: Thu, 20 Feb 2020 23:53:16 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45fe2c562cb0866875f0499d9583698863ee29b34a5a94406a42202b70885f6f`  
		Last Modified: Thu, 20 Feb 2020 23:53:16 GMT  
		Size: 570.8 KB (570772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e31dee670440ee2efcb54b84d9b9acccc709250fcb875c7ab9f31b21aded9fc`  
		Last Modified: Thu, 20 Feb 2020 23:53:16 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7.6` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:d6ac77d178d83433a94f4c1ac85d37eb6bde9a3b5e2ddd70510ab8366580d72d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 MB (30795142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59720519dbc2aaa04f42da6be01d883724212b4503025e14148efe901e90b553`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Sat, 18 Jan 2020 02:29:26 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 02:29:26 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 02:29:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 02:29:29 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 24 Jan 2020 00:09:58 GMT
ENV PHP_VERSION=7.4.2
# Fri, 24 Jan 2020 00:10:02 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.2.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.2.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 00:10:03 GMT
ENV PHP_SHA256=98284deac017da0d426117ecae7599a1f1bf62ae3911e8bc16c4403a8f4bdf13 PHP_MD5=
# Fri, 24 Jan 2020 00:10:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 24 Jan 2020 00:10:10 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 00:14:01 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 00:14:05 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Fri, 24 Jan 2020 00:14:09 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 00:14:10 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 00:14:11 GMT
CMD ["php" "-a"]
# Fri, 24 Jan 2020 02:50:27 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 24 Jan 2020 02:50:28 GMT
STOPSIGNAL SIGINT
# Fri, 24 Jan 2020 02:50:32 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 24 Jan 2020 02:50:32 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 02:50:36 GMT
RUN apk add --no-cache libpq
# Fri, 24 Jan 2020 02:51:09 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Fri, 24 Jan 2020 02:51:10 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 31 Jan 2020 17:39:37 GMT
ENV ADMINER_VERSION=4.7.6
# Fri, 31 Jan 2020 17:39:37 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Fri, 31 Jan 2020 17:39:38 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Fri, 31 Jan 2020 17:39:40 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 31 Jan 2020 17:39:41 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 31 Jan 2020 17:39:42 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 31 Jan 2020 17:39:42 GMT
USER adminer
# Fri, 31 Jan 2020 17:39:43 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 31 Jan 2020 17:39:44 GMT
EXPOSE 8080
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
	-	`sha256:aa724be546925194dbbb305717c1ec1404bd825d4e768f5fa30758fc836a1dda`  
		Last Modified: Fri, 24 Jan 2020 02:37:49 GMT  
		Size: 10.3 MB (10271109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b0bc8c61926931859ef4bf710fb73b709a407ca1086dfe704e7654934b4bdd`  
		Last Modified: Fri, 24 Jan 2020 02:37:45 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07be412705d63c11275e2018adae846b8861d4f678a21f2c43e2c22ae0bcee6d`  
		Last Modified: Fri, 24 Jan 2020 02:37:49 GMT  
		Size: 14.4 MB (14366228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73cafd3dde7ad30752409223dc0b26b0a5f4fa98d9a875225e2566bd99806655`  
		Last Modified: Fri, 24 Jan 2020 02:37:45 GMT  
		Size: 2.2 KB (2216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59195632759b7e9a57fb9ac253284ecbea9055d01c12f9caa49d23ca8f40bc1c`  
		Last Modified: Fri, 24 Jan 2020 02:37:45 GMT  
		Size: 72.7 KB (72676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6576a2f957338815a3fd8d1023a31cbb8ef8592406942ab75483b02adbe1c384`  
		Last Modified: Fri, 24 Jan 2020 02:52:47 GMT  
		Size: 310.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f6446e74a0df8b21f4f9ad86cf10fa3f6b6a9231d643d4174a5ddd3cf84f184`  
		Last Modified: Fri, 24 Jan 2020 02:52:47 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b69655ccf3f62cf1149958c93543bc91f9addef901545f4c74831b5c65b29039`  
		Last Modified: Fri, 24 Jan 2020 02:52:44 GMT  
		Size: 1.3 MB (1299236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:986406fbe9d0af0aeacc6c7cc032415d7552b4fd8f3fe60ea2313caa9193649c`  
		Last Modified: Fri, 24 Jan 2020 02:52:44 GMT  
		Size: 124.7 KB (124696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:382b47ced56d800090d03dff8f4d1183a7209bfd39013db12812d2efc2a39f54`  
		Last Modified: Fri, 24 Jan 2020 02:52:44 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23f30f175d57f1ffdc2f5c4308d886c2f842ce1a163c77b1747b628a89684ac`  
		Last Modified: Fri, 31 Jan 2020 17:40:10 GMT  
		Size: 570.8 KB (570779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d5044dac86a165d99ffacf0aaeb789461f31935ef0847d4e80ae612f101599`  
		Last Modified: Fri, 31 Jan 2020 17:40:10 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7.6` - linux; 386

```console
$ docker pull adminer@sha256:d094fa6fd940847cd20c8dd698284d004cf1d6a5fa23d777f0b19667afa76346
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31684075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed77c13afb1993912752a1a0383da2185144a458fde112b713496146d193cb19`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Sat, 18 Jan 2020 05:41:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 05:41:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 05:41:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 05:41:39 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 23 Jan 2020 23:13:49 GMT
ENV PHP_VERSION=7.4.2
# Thu, 23 Jan 2020 23:13:49 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.2.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.2.tar.xz.asc/from/this/mirror
# Thu, 23 Jan 2020 23:13:49 GMT
ENV PHP_SHA256=98284deac017da0d426117ecae7599a1f1bf62ae3911e8bc16c4403a8f4bdf13 PHP_MD5=
# Thu, 23 Jan 2020 23:13:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 23 Jan 2020 23:13:52 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Jan 2020 23:21:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 23 Jan 2020 23:21:57 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 23 Jan 2020 23:21:59 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Jan 2020 23:21:59 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Jan 2020 23:22:00 GMT
CMD ["php" "-a"]
# Fri, 24 Jan 2020 07:25:41 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 24 Jan 2020 07:25:41 GMT
STOPSIGNAL SIGINT
# Fri, 24 Jan 2020 07:25:42 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 24 Jan 2020 07:25:42 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 07:25:43 GMT
RUN apk add --no-cache libpq
# Fri, 24 Jan 2020 07:26:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Fri, 24 Jan 2020 07:26:02 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 31 Jan 2020 17:38:17 GMT
ENV ADMINER_VERSION=4.7.6
# Fri, 31 Jan 2020 17:38:18 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Fri, 31 Jan 2020 17:38:18 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Fri, 31 Jan 2020 17:38:19 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 31 Jan 2020 17:38:19 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 31 Jan 2020 17:38:20 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 31 Jan 2020 17:38:20 GMT
USER adminer
# Fri, 31 Jan 2020 17:38:20 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 31 Jan 2020 17:38:20 GMT
EXPOSE 8080
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
	-	`sha256:9f3628b223c4b093cf7c2d7723ccd39dfcb6977a659c9c183e7673f22f44865b`  
		Last Modified: Fri, 24 Jan 2020 02:36:11 GMT  
		Size: 10.3 MB (10271099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e167c61f346105deafdbe6bff7f521715a3d31cd4c9ca27d6dca67654d916c`  
		Last Modified: Fri, 24 Jan 2020 02:36:08 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53425617927914b1561c930b3ce2f90644de41394e731ca71a5d66feeba55d5b`  
		Last Modified: Fri, 24 Jan 2020 02:36:19 GMT  
		Size: 15.0 MB (14974599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809347a8b4ae69caee1b666ac61ec86e0f2dd5d64744592a59f65fd9bb49c7c9`  
		Last Modified: Fri, 24 Jan 2020 02:36:10 GMT  
		Size: 2.2 KB (2216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31917077d16c99b9c58e44f9267cbda55763d759a59379d7e4ca1f9fd6acf60a`  
		Last Modified: Fri, 24 Jan 2020 02:36:09 GMT  
		Size: 72.3 KB (72331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc6ba5ae7aae77ac94c185eef225136d01333d8840f8896b412e359fa89e3ae6`  
		Last Modified: Fri, 24 Jan 2020 07:27:19 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aab9a7fed181e4a8d1621cf6e92e6b4525a242e1c102cac7a259b3336202c16`  
		Last Modified: Fri, 24 Jan 2020 07:27:19 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1120969ea66ac41447ffffddcda8e8d389a0a1c0c7feb7d9d650117b973459d`  
		Last Modified: Fri, 24 Jan 2020 07:27:18 GMT  
		Size: 1.4 MB (1397662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cf37d29a0120ccd9ef7f4f99c6d10673cd93097ebe961c86faf275c144f5929`  
		Last Modified: Fri, 24 Jan 2020 07:27:18 GMT  
		Size: 130.8 KB (130760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf17f4f8d6baa9c93722150405686cf214bc377adbb7ff2b891efe5ca38809c9`  
		Last Modified: Fri, 24 Jan 2020 07:27:18 GMT  
		Size: 1.5 KB (1472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cac8221b3739531c0e54a60c4d8d795c187ce863f2fb79955540c1b62347fbc7`  
		Last Modified: Fri, 31 Jan 2020 17:38:36 GMT  
		Size: 570.7 KB (570691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8127a70cc3e20105c94ab16913cab965e775aaa7cb37cc6398e47d4a1830241e`  
		Last Modified: Fri, 31 Jan 2020 17:38:36 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7.6` - linux; ppc64le

```console
$ docker pull adminer@sha256:8906a11939b6681a5c547d8a1b3d8e58493fb85a66ef14177592239c9cd3ab6f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32169343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:251a9f8c0d32635a09c63fc8d5e5fbad2fee09cca0a4ea7cca903b5d9ac6f815`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Sat, 18 Jan 2020 03:24:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:24:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:24:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 03:24:34 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 23 Jan 2020 23:32:44 GMT
ENV PHP_VERSION=7.4.2
# Thu, 23 Jan 2020 23:32:47 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.2.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.2.tar.xz.asc/from/this/mirror
# Thu, 23 Jan 2020 23:32:50 GMT
ENV PHP_SHA256=98284deac017da0d426117ecae7599a1f1bf62ae3911e8bc16c4403a8f4bdf13 PHP_MD5=
# Thu, 23 Jan 2020 23:33:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 23 Jan 2020 23:33:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Jan 2020 23:36:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 23 Jan 2020 23:36:54 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 23 Jan 2020 23:37:00 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Jan 2020 23:37:02 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Jan 2020 23:37:04 GMT
CMD ["php" "-a"]
# Fri, 24 Jan 2020 05:51:10 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 24 Jan 2020 05:51:12 GMT
STOPSIGNAL SIGINT
# Fri, 24 Jan 2020 05:51:17 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 24 Jan 2020 05:51:19 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 05:51:23 GMT
RUN apk add --no-cache libpq
# Fri, 24 Jan 2020 05:51:48 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Fri, 24 Jan 2020 05:51:50 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 31 Jan 2020 17:16:45 GMT
ENV ADMINER_VERSION=4.7.6
# Fri, 31 Jan 2020 17:16:48 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Fri, 31 Jan 2020 17:16:51 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Fri, 31 Jan 2020 17:17:00 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 31 Jan 2020 17:17:01 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 31 Jan 2020 17:17:03 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 31 Jan 2020 17:17:05 GMT
USER adminer
# Fri, 31 Jan 2020 17:17:08 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 31 Jan 2020 17:17:10 GMT
EXPOSE 8080
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
	-	`sha256:c24c1e693453ad6efa656fcfa28e76c0786f80b4467d83c277d1116117942973`  
		Last Modified: Fri, 24 Jan 2020 02:32:44 GMT  
		Size: 10.3 MB (10271124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb71fc05f0fe0d365d8b9891f304e0cf2c1f6f0d2200ecdc0ea9a1c569117a1d`  
		Last Modified: Fri, 24 Jan 2020 02:32:41 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf26116548345ee1f676a6c1fabb768cd60750eb7a3a0ac7f09724350dde3b1`  
		Last Modified: Fri, 24 Jan 2020 02:32:54 GMT  
		Size: 15.5 MB (15539990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc4f870d6f2e6bbade33c0f28534b50765c4b56a093dc7565bd3ec3b37a7c603`  
		Last Modified: Fri, 24 Jan 2020 02:32:41 GMT  
		Size: 2.2 KB (2211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6a738ee51d709e4c4db983f9206a240500a2fc0dbaf3c76f6da2f99e5f6eb3b`  
		Last Modified: Fri, 24 Jan 2020 02:32:41 GMT  
		Size: 73.0 KB (72992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47bf1b73f7bf1089b7cf019ae582b63d77fa46e6c5b2b4efc16b0bf9d9b1ad9a`  
		Last Modified: Fri, 24 Jan 2020 05:53:47 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f984dcaccfb46a5cafd49380217e97342575055ceaaab4ff65a67f43af2da028`  
		Last Modified: Fri, 24 Jan 2020 05:53:47 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9e4520026a60556f0b631a13532b9a39d91d8eae94d4d3514359ef189ce4c94`  
		Last Modified: Fri, 24 Jan 2020 05:53:45 GMT  
		Size: 1.4 MB (1350626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba57cd117c3f571c3379a3fbb16d112291f4de925499dfeaad0bc7966c9483fb`  
		Last Modified: Fri, 24 Jan 2020 05:53:44 GMT  
		Size: 135.9 KB (135919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faef1730db86976915b65b75f76c1a057c321a983034e019f37ec833f5a1ffc9`  
		Last Modified: Fri, 24 Jan 2020 05:53:44 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:620c9c1b5881ba0a3be097e7cb57c695406737868e7b1adc02c5561c5f7b1649`  
		Last Modified: Fri, 31 Jan 2020 17:18:05 GMT  
		Size: 570.8 KB (570776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03e77753eec72902172405ef4c8c0c667bf7377cd0dc6cc1441afd0890991d43`  
		Last Modified: Fri, 31 Jan 2020 17:18:04 GMT  
		Size: 501.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:4.7.6-fastcgi`

```console
$ docker pull adminer@sha256:85ef53ce6942c89cdacf05991c16132da81d158741e42e2eef13b3c4111ba801
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `adminer:4.7.6-fastcgi` - linux; amd64

```console
$ docker pull adminer@sha256:3261472ab50e9daaf45a30818ad65311dc175417adf46363ecf18c7fb79f4048
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31132621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f894c56f8bea377d752a7839e5b2af6ffeab97af51d7b9b54e8c3113a954b088`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
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
# Sat, 18 Jan 2020 03:23:44 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 24 Jan 2020 07:13:33 GMT
ENV PHP_VERSION=7.4.2
# Fri, 24 Jan 2020 07:13:33 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.2.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.2.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 07:13:34 GMT
ENV PHP_SHA256=98284deac017da0d426117ecae7599a1f1bf62ae3911e8bc16c4403a8f4bdf13 PHP_MD5=
# Fri, 24 Jan 2020 07:13:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 24 Jan 2020 07:13:36 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 07:19:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 07:19:23 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Fri, 24 Jan 2020 07:19:24 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 07:19:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 07:19:24 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 07:19:25 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 24 Jan 2020 07:19:25 GMT
STOPSIGNAL SIGQUIT
# Fri, 24 Jan 2020 07:19:25 GMT
EXPOSE 9000
# Fri, 24 Jan 2020 07:19:25 GMT
CMD ["php-fpm"]
# Fri, 24 Jan 2020 10:52:50 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 24 Jan 2020 10:52:51 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 24 Jan 2020 10:52:52 GMT
RUN apk add --no-cache libpq
# Fri, 24 Jan 2020 10:53:11 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Fri, 24 Jan 2020 10:53:11 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 31 Jan 2020 17:19:33 GMT
ENV ADMINER_VERSION=4.7.6
# Fri, 31 Jan 2020 17:19:33 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Fri, 31 Jan 2020 17:19:33 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Fri, 31 Jan 2020 17:19:34 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 31 Jan 2020 17:19:34 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 31 Jan 2020 17:19:35 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 31 Jan 2020 17:19:35 GMT
USER adminer
# Fri, 31 Jan 2020 17:19:35 GMT
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
	-	`sha256:6e71cca12e10fbf7814b66f3f30f2c626a76931eb1658b35580520657aa1c472`  
		Last Modified: Fri, 24 Jan 2020 10:39:58 GMT  
		Size: 10.3 MB (10271098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed2310d2f7910e8f29ab569006386735c80fdb8d7a9f4b50c2233347335ef47e`  
		Last Modified: Fri, 24 Jan 2020 10:39:55 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:601ef2217a14892579aa55bfff77d380170c0c5b6bb97ba4275769e288cc008e`  
		Last Modified: Fri, 24 Jan 2020 10:40:00 GMT  
		Size: 14.6 MB (14640028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41dc18d982f54d4c5634f99e7933d9ad3069ef493b460cf998e1954caa2f24b7`  
		Last Modified: Fri, 24 Jan 2020 10:39:55 GMT  
		Size: 2.2 KB (2219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72be421f63f8c4ae023b97af91e72adcad7347edfff80e8fe6d0fea64be89f41`  
		Last Modified: Fri, 24 Jan 2020 10:39:56 GMT  
		Size: 73.1 KB (73144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f10dd871243fb2f678d5abcd0925bfc78bf759edf24b577c2aaaecce51ac30fb`  
		Last Modified: Fri, 24 Jan 2020 10:39:55 GMT  
		Size: 8.4 KB (8409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df30bf875af7c93a1a5f0231eb502f80916cc360f7bb5301af9fd174346bae03`  
		Last Modified: Fri, 24 Jan 2020 10:53:53 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb01654c81755c04f51d84470d9460f05137a60b5cb6af11a277b81ffdb12844`  
		Last Modified: Fri, 24 Jan 2020 10:53:53 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc08268651428df387dfafc653a2ce4c616f5eb02a72752692c59c871b99d37`  
		Last Modified: Fri, 24 Jan 2020 10:53:52 GMT  
		Size: 1.3 MB (1277248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ee28a212305aa260efa44f897f666e2d55a5c7b69b1eacb4913985baf64c9a`  
		Last Modified: Fri, 24 Jan 2020 10:53:52 GMT  
		Size: 126.6 KB (126627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60596dcdb9d8dba4d1f1beb1964daee86e4d999728581b4ed91e9edc6dd78a87`  
		Last Modified: Fri, 24 Jan 2020 10:53:52 GMT  
		Size: 1.5 KB (1474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30705479566e7b730c43bc045a5c98474f7fa05a827632e22deb9c00247a1792`  
		Last Modified: Fri, 31 Jan 2020 17:19:53 GMT  
		Size: 570.7 KB (570684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d656991abfa4ac7b964071b05e6a5c7e82cfb72e2de48fb119f733649768109`  
		Last Modified: Fri, 31 Jan 2020 17:19:53 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7.6-fastcgi` - linux; arm variant v6

```console
$ docker pull adminer@sha256:f3ef94b81d53fa10bdf91813ec1727746da25896c82eb5418da6183ff345fe42
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.9 MB (29904916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13e34cefffcf1ef42f5bc12f108decf6d572e5812224b5f36b8008069927885c`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
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
# Sat, 18 Jan 2020 03:44:54 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 20 Feb 2020 21:54:14 GMT
ENV PHP_VERSION=7.4.3
# Thu, 20 Feb 2020 21:54:15 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.3.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.3.tar.xz.asc/from/this/mirror
# Thu, 20 Feb 2020 21:54:16 GMT
ENV PHP_SHA256=cf1f856d877c268124ded1ede40c9fb6142b125fdaafdc54f855120b8bc6982a PHP_MD5=
# Thu, 20 Feb 2020 21:54:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Feb 2020 21:54:23 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Feb 2020 21:58:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 20 Feb 2020 21:58:38 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Thu, 20 Feb 2020 21:58:41 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Feb 2020 21:58:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Feb 2020 21:58:43 GMT
WORKDIR /var/www/html
# Thu, 20 Feb 2020 21:58:45 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 20 Feb 2020 21:58:46 GMT
STOPSIGNAL SIGQUIT
# Thu, 20 Feb 2020 21:58:48 GMT
EXPOSE 9000
# Thu, 20 Feb 2020 21:58:49 GMT
CMD ["php-fpm"]
# Thu, 20 Feb 2020 23:47:03 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Thu, 20 Feb 2020 23:47:05 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 20 Feb 2020 23:47:07 GMT
RUN apk add --no-cache libpq
# Thu, 20 Feb 2020 23:47:34 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Thu, 20 Feb 2020 23:47:35 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Thu, 20 Feb 2020 23:47:35 GMT
ENV ADMINER_VERSION=4.7.6
# Thu, 20 Feb 2020 23:47:36 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Thu, 20 Feb 2020 23:47:37 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Thu, 20 Feb 2020 23:47:40 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Thu, 20 Feb 2020 23:47:41 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 20 Feb 2020 23:47:41 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Thu, 20 Feb 2020 23:47:42 GMT
USER adminer
# Thu, 20 Feb 2020 23:47:42 GMT
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
	-	`sha256:80ca3c99ad3f93290cc94e506f94e8b01e2bfe5d2901b45ad4fd1bf704e70ed7`  
		Last Modified: Thu, 20 Feb 2020 23:10:40 GMT  
		Size: 10.3 MB (10280253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f658c7e1eb0d0386247f8fa5f228f97f709e09b53982bd1ba92f38cad3803ec8`  
		Last Modified: Thu, 20 Feb 2020 23:10:36 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38dd2d597adffab2d9b483cfa2352a9413ca3868e55fccb30c7551e0c1a7cb57`  
		Last Modified: Thu, 20 Feb 2020 23:10:42 GMT  
		Size: 13.7 MB (13671450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bfdd3dff152326a8135a5747de2a94547b298afe86fe63946bb425bc30fba92`  
		Last Modified: Thu, 20 Feb 2020 23:10:36 GMT  
		Size: 2.2 KB (2213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5554b593396e1abf2813391b3b1c84e40383b0988321d2d63616a290aa7fed7d`  
		Last Modified: Thu, 20 Feb 2020 23:10:36 GMT  
		Size: 72.7 KB (72681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9159be50c0fe27b27be4abb997de85c54fd2d1308d35c5c6c97e4d118fdec6a0`  
		Last Modified: Thu, 20 Feb 2020 23:10:37 GMT  
		Size: 8.4 KB (8412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28aa812c7cc19a079c92c7f6eba0da1ecffdcf6f1fe4946898b7ec9ff1b6940a`  
		Last Modified: Thu, 20 Feb 2020 23:48:28 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a7c93eb4a00db350eb6b34997b1f9541d4851def62b039696d47ae3b25f55f8`  
		Last Modified: Thu, 20 Feb 2020 23:48:28 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:820825c9319f4e49d67cd84bb103b76d2cca8df1f674d7a84b6b5ef1f43afe3b`  
		Last Modified: Thu, 20 Feb 2020 23:48:23 GMT  
		Size: 1.2 MB (1234699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49c16bab556b699d17b5ef77dfbbc559d0fabd75d27f9eed069b3753331c0e5a`  
		Last Modified: Thu, 20 Feb 2020 23:48:23 GMT  
		Size: 120.1 KB (120098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1ec2a9c5203dcc61950a047d4f04c455f284b6062740fbc081a32c7fb5873b2`  
		Last Modified: Thu, 20 Feb 2020 23:48:23 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:295fdb00d23508c2695ae7402b772fdd479d44cd0f0a05c93b069242638a3e0f`  
		Last Modified: Thu, 20 Feb 2020 23:48:23 GMT  
		Size: 570.8 KB (570771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92b8b25d3ffd6ef7dd0976b4b19b04842ed268bfbc55452f5000ba913defa355`  
		Last Modified: Thu, 20 Feb 2020 23:48:23 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7.6-fastcgi` - linux; arm variant v7

```console
$ docker pull adminer@sha256:2f5f67a712318a2a917724f95730ad156ec7427834865497016e22de6541cc5c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.6 MB (28642438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c803a31f5e4241a9cb82515d1cc260871c3f62e3c30297d71a35973096a31e2`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
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
# Sat, 18 Jan 2020 05:28:02 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 20 Feb 2020 21:14:19 GMT
ENV PHP_VERSION=7.4.3
# Thu, 20 Feb 2020 21:14:19 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.3.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.3.tar.xz.asc/from/this/mirror
# Thu, 20 Feb 2020 21:14:20 GMT
ENV PHP_SHA256=cf1f856d877c268124ded1ede40c9fb6142b125fdaafdc54f855120b8bc6982a PHP_MD5=
# Thu, 20 Feb 2020 21:14:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Feb 2020 21:14:24 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Feb 2020 21:16:45 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 20 Feb 2020 21:16:46 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Thu, 20 Feb 2020 21:16:49 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Feb 2020 21:16:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Feb 2020 21:16:50 GMT
WORKDIR /var/www/html
# Thu, 20 Feb 2020 21:16:51 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 20 Feb 2020 21:16:52 GMT
STOPSIGNAL SIGQUIT
# Thu, 20 Feb 2020 21:16:53 GMT
EXPOSE 9000
# Thu, 20 Feb 2020 21:16:54 GMT
CMD ["php-fpm"]
# Thu, 20 Feb 2020 23:52:02 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Thu, 20 Feb 2020 23:52:05 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 20 Feb 2020 23:52:08 GMT
RUN apk add --no-cache libpq
# Thu, 20 Feb 2020 23:52:41 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Thu, 20 Feb 2020 23:52:43 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Thu, 20 Feb 2020 23:52:44 GMT
ENV ADMINER_VERSION=4.7.6
# Thu, 20 Feb 2020 23:52:45 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Thu, 20 Feb 2020 23:52:46 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Thu, 20 Feb 2020 23:52:49 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Thu, 20 Feb 2020 23:52:50 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 20 Feb 2020 23:52:51 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Thu, 20 Feb 2020 23:52:52 GMT
USER adminer
# Thu, 20 Feb 2020 23:52:54 GMT
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
	-	`sha256:0b327d731622fe78b5dce5377da7c2fa2a8f7f5bccb0851084b9329f9a570063`  
		Last Modified: Thu, 20 Feb 2020 23:26:52 GMT  
		Size: 10.3 MB (10280261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4b40e24dacf2616800de7bb9e410e263de6eccf4d1bfd5a22d32908c21b2361`  
		Last Modified: Thu, 20 Feb 2020 23:26:49 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e42a50422a3ffed17517bce0eb1fe538eea06417fdc672c4711d134108d7b0b4`  
		Last Modified: Thu, 20 Feb 2020 23:26:54 GMT  
		Size: 12.8 MB (12815724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5473e54c50261b361a070da14923a840b1c2155de57aacac9a8ff18575dd6e1a`  
		Last Modified: Thu, 20 Feb 2020 23:26:50 GMT  
		Size: 2.2 KB (2216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f939d7049d7edb45231e24fec17211f863a36748747b3121cc935b6760c86632`  
		Last Modified: Thu, 20 Feb 2020 23:26:49 GMT  
		Size: 72.7 KB (72680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e26488d2c5a3fcc5e1d56a02cd6a6755d2bf8a503dfb6bff0c265cedf52a11fa`  
		Last Modified: Thu, 20 Feb 2020 23:26:49 GMT  
		Size: 8.4 KB (8409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7b9f9e7ecb2380e21319c90bc307fa28a14061bc3b629ea3cafaebe8e7865e3`  
		Last Modified: Thu, 20 Feb 2020 23:53:39 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:214861e86ee457b4f34bad18e669992ef9dff229e599e0f7f15f41b926a9ec31`  
		Last Modified: Thu, 20 Feb 2020 23:53:39 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6f9a71b7d4f646e777f739107b1911cf18f3305a0f3348c54572385f6f5d71f`  
		Last Modified: Thu, 20 Feb 2020 23:53:37 GMT  
		Size: 1.1 MB (1124908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3757929f73de69aebca78a3f042c638bb48e703b5a1ce80fc02e2eae8b45cdf`  
		Last Modified: Thu, 20 Feb 2020 23:53:37 GMT  
		Size: 115.0 KB (114950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3151fc0a4ad4389a4655e265bca8650f675575130c4394907f6abe79dc4bacf3`  
		Last Modified: Thu, 20 Feb 2020 23:53:37 GMT  
		Size: 1.5 KB (1477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85281d825070bdddb16a2bacfad1baa7633a1a1e22d32c6ad458bbac70bc1737`  
		Last Modified: Thu, 20 Feb 2020 23:53:37 GMT  
		Size: 570.8 KB (570766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499386092f7399a059f809ff852ca1239313c7555831f07909a8cc81d06f386d`  
		Last Modified: Thu, 20 Feb 2020 23:53:37 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7.6-fastcgi` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:4f9923edd71c163c491fec06013c2c29c6c486e96f1a5a5fe9f6a15d7d0cdb08
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30872795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c607c25c09ed37fcb1262db44e11192f84fc037fe9d82ebbd207a31813123ff5`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
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
# Sat, 18 Jan 2020 02:36:11 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 24 Jan 2020 00:14:35 GMT
ENV PHP_VERSION=7.4.2
# Fri, 24 Jan 2020 00:14:36 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.2.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.2.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 00:14:38 GMT
ENV PHP_SHA256=98284deac017da0d426117ecae7599a1f1bf62ae3911e8bc16c4403a8f4bdf13 PHP_MD5=
# Fri, 24 Jan 2020 00:14:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 24 Jan 2020 00:14:45 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 00:18:29 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 00:18:32 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Fri, 24 Jan 2020 00:18:36 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 00:18:37 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 00:18:38 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 00:18:41 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 24 Jan 2020 00:18:42 GMT
STOPSIGNAL SIGQUIT
# Fri, 24 Jan 2020 00:18:44 GMT
EXPOSE 9000
# Fri, 24 Jan 2020 00:18:45 GMT
CMD ["php-fpm"]
# Fri, 24 Jan 2020 02:51:31 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 24 Jan 2020 02:51:33 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 24 Jan 2020 02:51:36 GMT
RUN apk add --no-cache libpq
# Fri, 24 Jan 2020 02:52:06 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Fri, 24 Jan 2020 02:52:07 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 31 Jan 2020 17:39:50 GMT
ENV ADMINER_VERSION=4.7.6
# Fri, 31 Jan 2020 17:39:51 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Fri, 31 Jan 2020 17:39:51 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Fri, 31 Jan 2020 17:39:54 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 31 Jan 2020 17:39:55 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 31 Jan 2020 17:39:55 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 31 Jan 2020 17:39:56 GMT
USER adminer
# Fri, 31 Jan 2020 17:39:57 GMT
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
	-	`sha256:031bf935aef9c8cf9a41b1dbd509b48db2ab230dae75e8d1f2f20c1713826cfa`  
		Last Modified: Fri, 24 Jan 2020 02:38:24 GMT  
		Size: 10.3 MB (10271108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd439e1038e9d42eab7437e8f85a4c7cd369089af8cb708e63e0c4388fdb1bf3`  
		Last Modified: Fri, 24 Jan 2020 02:38:16 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25ed1e9754e061a3e75c31e172b7e2ef4b7b5a8673a24423b2260a91000daed9`  
		Last Modified: Fri, 24 Jan 2020 02:38:20 GMT  
		Size: 14.4 MB (14435498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5801422dba8896819ba048a35c0da81a25eec8fb91c74ddc3da87bbbf13fd470`  
		Last Modified: Fri, 24 Jan 2020 02:38:16 GMT  
		Size: 2.2 KB (2217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d4f983059021c9010c5326e718d5870d3ed28a792a95b78f95399c93b6b963f`  
		Last Modified: Fri, 24 Jan 2020 02:38:16 GMT  
		Size: 72.7 KB (72672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:947d95e1f7678a8070ee18dba3cf26e07c11e7a0f1fed1885014776890783c64`  
		Last Modified: Fri, 24 Jan 2020 02:38:16 GMT  
		Size: 8.4 KB (8410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8246e4f25893c2c59d16a3a91eb0e024ee6b366eb1828d39c00069b0fe074821`  
		Last Modified: Fri, 24 Jan 2020 02:53:09 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153c72183d2af4959ab20862dab40a0a198583b2ed6460c78eb4b58afbe8099a`  
		Last Modified: Fri, 24 Jan 2020 02:53:08 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79ea398fe8d2d7940f02c220eac23b6e0b59f654452a7c2d784746f57264e66`  
		Last Modified: Fri, 24 Jan 2020 02:53:07 GMT  
		Size: 1.3 MB (1299219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a60c746308f1dc0af8f8ee2c44315d9bb1b416377a2938f63d9a70ab2d0f06ad`  
		Last Modified: Fri, 24 Jan 2020 02:53:07 GMT  
		Size: 124.7 KB (124702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca6bc7dce64e9b13729a1e1afd341a91788f4a0d94380b7cc81feec83f580bf6`  
		Last Modified: Fri, 24 Jan 2020 02:53:06 GMT  
		Size: 1.5 KB (1474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f1dac04eb03855c7c287673ef8e4c6d1c4915d3663f9376444abe8e8c3c1ed4`  
		Last Modified: Fri, 31 Jan 2020 17:40:25 GMT  
		Size: 570.8 KB (570773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44ddb8bdcd055db611ac57e0a6bc167bd231eaf893f9d7d11e3f0d13025cf98`  
		Last Modified: Fri, 31 Jan 2020 17:40:25 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7.6-fastcgi` - linux; 386

```console
$ docker pull adminer@sha256:46b8bb610eaaa99932c42a3352a7bb709eddd218944284a41d4a25ab9e2593db
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31762110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e5c58ebd525deeac88b11a3c516b9d22ac70308fcd0aeb5cc2624988423c31`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
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
# Sat, 18 Jan 2020 05:48:40 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 23 Jan 2020 23:22:10 GMT
ENV PHP_VERSION=7.4.2
# Thu, 23 Jan 2020 23:22:10 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.2.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.2.tar.xz.asc/from/this/mirror
# Thu, 23 Jan 2020 23:22:11 GMT
ENV PHP_SHA256=98284deac017da0d426117ecae7599a1f1bf62ae3911e8bc16c4403a8f4bdf13 PHP_MD5=
# Thu, 23 Jan 2020 23:22:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 23 Jan 2020 23:22:16 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Jan 2020 23:31:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 23 Jan 2020 23:31:14 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Thu, 23 Jan 2020 23:31:15 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Jan 2020 23:31:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Jan 2020 23:31:15 GMT
WORKDIR /var/www/html
# Thu, 23 Jan 2020 23:31:16 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 23 Jan 2020 23:31:16 GMT
STOPSIGNAL SIGQUIT
# Thu, 23 Jan 2020 23:31:16 GMT
EXPOSE 9000
# Thu, 23 Jan 2020 23:31:17 GMT
CMD ["php-fpm"]
# Fri, 24 Jan 2020 07:26:11 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 24 Jan 2020 07:26:12 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 24 Jan 2020 07:26:14 GMT
RUN apk add --no-cache libpq
# Fri, 24 Jan 2020 07:26:45 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Fri, 24 Jan 2020 07:26:45 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 31 Jan 2020 17:38:25 GMT
ENV ADMINER_VERSION=4.7.6
# Fri, 31 Jan 2020 17:38:25 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Fri, 31 Jan 2020 17:38:25 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Fri, 31 Jan 2020 17:38:26 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 31 Jan 2020 17:38:27 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 31 Jan 2020 17:38:27 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 31 Jan 2020 17:38:27 GMT
USER adminer
# Fri, 31 Jan 2020 17:38:27 GMT
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
	-	`sha256:7af2969e346cf39dce09953165d38ac70a637f81bf36a72173d23c8209522b1e`  
		Last Modified: Fri, 24 Jan 2020 02:36:49 GMT  
		Size: 10.3 MB (10271104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dffed627d6f3eb28e87526c201e8ae30d110efc1e7ae5b48646e1f322abddefd`  
		Last Modified: Fri, 24 Jan 2020 02:36:40 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44af2512ec067db56bee629528b24bfe54ad55f8f7064b2cf59f57868950482d`  
		Last Modified: Fri, 24 Jan 2020 02:36:51 GMT  
		Size: 15.0 MB (15044190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a34e204f3d52c0be6c78857ce18184fecbd91cf297cfb30bf15df00d78b1ff71`  
		Last Modified: Fri, 24 Jan 2020 02:36:40 GMT  
		Size: 2.2 KB (2217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c9a720f2eaf0aec04eabdd4c10f331bd1eb5e91bdf806ec43279ae4d9435107`  
		Last Modified: Fri, 24 Jan 2020 02:36:41 GMT  
		Size: 72.3 KB (72332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ce027d9508f9c2ba08e68a1cbef48753b345821147a4ec4dd52ced22ca8252`  
		Last Modified: Fri, 24 Jan 2020 02:36:40 GMT  
		Size: 8.4 KB (8413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:791ceb40ab90a13fa40d9a11daa5853b0d7c1f72f7fb2580891e34049e7be6ba`  
		Last Modified: Fri, 24 Jan 2020 07:27:33 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac79a09757dcd35db84f1d12d43f5d8f11408f92ee9e095c392eda59733b801a`  
		Last Modified: Fri, 24 Jan 2020 07:27:33 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b6beb85931082255a7f9048c7f337e1972e10ce8a02c86b86797e95922ad930`  
		Last Modified: Fri, 24 Jan 2020 07:27:34 GMT  
		Size: 1.4 MB (1397661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79d5b1485f733f60d9843f7e138f1fa150e42d713df194640dcc37931ec1c191`  
		Last Modified: Fri, 24 Jan 2020 07:27:31 GMT  
		Size: 130.8 KB (130793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:553d2e165ba3dd32a4a9a44d46fa13ec6552747310640f783b34255acfd961e2`  
		Last Modified: Fri, 24 Jan 2020 07:27:31 GMT  
		Size: 1.5 KB (1472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42e41cc3dbdf2dad75063abe783a7985dc9267ee1ee9bd5751bed6f0cba09c2b`  
		Last Modified: Fri, 31 Jan 2020 17:38:46 GMT  
		Size: 570.7 KB (570683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd7e34ec5637f78a0244c66e92539e53bcc0bc77fafc96f775c60a3dbfce14ef`  
		Last Modified: Fri, 31 Jan 2020 17:38:46 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7.6-fastcgi` - linux; ppc64le

```console
$ docker pull adminer@sha256:52c4be54d3cd71b8c7ef779124ae7e3796754fad9594b24584b157fe0d90ea88
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32259051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:058dcefad0447822a717afd8533b7ef7ac94f28229ce3c409df8c013633ad069`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
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
# Sat, 18 Jan 2020 03:29:20 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 23 Jan 2020 23:37:14 GMT
ENV PHP_VERSION=7.4.2
# Thu, 23 Jan 2020 23:37:17 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.2.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.2.tar.xz.asc/from/this/mirror
# Thu, 23 Jan 2020 23:37:18 GMT
ENV PHP_SHA256=98284deac017da0d426117ecae7599a1f1bf62ae3911e8bc16c4403a8f4bdf13 PHP_MD5=
# Thu, 23 Jan 2020 23:37:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 23 Jan 2020 23:37:30 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Jan 2020 23:41:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 23 Jan 2020 23:41:16 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Thu, 23 Jan 2020 23:41:21 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Jan 2020 23:41:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Jan 2020 23:41:25 GMT
WORKDIR /var/www/html
# Thu, 23 Jan 2020 23:41:31 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 23 Jan 2020 23:41:34 GMT
STOPSIGNAL SIGQUIT
# Thu, 23 Jan 2020 23:41:36 GMT
EXPOSE 9000
# Thu, 23 Jan 2020 23:41:37 GMT
CMD ["php-fpm"]
# Fri, 24 Jan 2020 05:52:24 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 24 Jan 2020 05:52:29 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 24 Jan 2020 05:52:35 GMT
RUN apk add --no-cache libpq
# Fri, 24 Jan 2020 05:53:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Fri, 24 Jan 2020 05:53:04 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 31 Jan 2020 17:17:22 GMT
ENV ADMINER_VERSION=4.7.6
# Fri, 31 Jan 2020 17:17:23 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Fri, 31 Jan 2020 17:17:24 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Fri, 31 Jan 2020 17:17:33 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 31 Jan 2020 17:17:35 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 31 Jan 2020 17:17:39 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 31 Jan 2020 17:17:42 GMT
USER adminer
# Fri, 31 Jan 2020 17:17:44 GMT
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
	-	`sha256:71750c6fa0607bea7a09ff35d6a1406245a40b8230624a3639b89d18db4394fe`  
		Last Modified: Fri, 24 Jan 2020 02:33:52 GMT  
		Size: 10.3 MB (10271124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9edfe3521268768bb7368d494a54a58f6ea37444d81365db80594ba5cf6723e`  
		Last Modified: Fri, 24 Jan 2020 02:33:41 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03d6040910816a926d5c549b0b705387c888406057cdb66956db3c32125ac16`  
		Last Modified: Fri, 24 Jan 2020 02:33:50 GMT  
		Size: 15.6 MB (15621302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60eae056a292b760c3cccf048be586d181427ad78105d2293c95ba02dbaf0ba1`  
		Last Modified: Fri, 24 Jan 2020 02:33:41 GMT  
		Size: 2.2 KB (2215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:728ffb10bff4c1ede1c201f677ecc8c6ad6fcaa32489ca45d7dc1ffb57804d89`  
		Last Modified: Fri, 24 Jan 2020 02:33:41 GMT  
		Size: 73.0 KB (72996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:348111edcf048b6a351ad6caed9d560f0dad7e6bbe2b76922a0648db42f74bcc`  
		Last Modified: Fri, 24 Jan 2020 02:33:42 GMT  
		Size: 8.4 KB (8409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b18f3572f56ef640587e5e01d586e9ac24e3c39688ad60eb7e2542c28330ef15`  
		Last Modified: Fri, 24 Jan 2020 05:54:24 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25b30d4afe834c4c6add7f1325d981a4767fe2d659474a4bcf07fe0982d30779`  
		Last Modified: Fri, 24 Jan 2020 05:54:23 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd12c1dc772a4360a1f25b4d61773bf85a5ce8636a383a26214f52199698c03a`  
		Last Modified: Fri, 24 Jan 2020 05:54:23 GMT  
		Size: 1.4 MB (1350625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc0b0a44d83a34b0167638ba083ff0f468a535b3a75087a1810e07394e5c6e8e`  
		Last Modified: Fri, 24 Jan 2020 05:54:20 GMT  
		Size: 135.9 KB (135904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1114f35e53ffc221921a3954ec43719e7f1e8adcc07c6b0f7b75364065ed97d7`  
		Last Modified: Fri, 24 Jan 2020 05:54:20 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:609b9a3cccb86ade52bbc4fb6a19223fa44f14509e75e7c2e4438278ef3a37b6`  
		Last Modified: Fri, 31 Jan 2020 17:18:36 GMT  
		Size: 570.8 KB (570772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b5ca04b772bc2f523594fd55735ad7e753da72ecf87478b23db102df001437`  
		Last Modified: Fri, 31 Jan 2020 17:18:36 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:4.7.6-standalone`

```console
$ docker pull adminer@sha256:c689401f4ee85e37ba2cd62d401af2d569833dd8efa2c338177889fa9c525882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `adminer:4.7.6-standalone` - linux; amd64

```console
$ docker pull adminer@sha256:6ceb642133ac56e267c50ae4bfb24ac0008b0eb02b772abae9059caa45211bee
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31058191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:259cc60bdb72538cffc06536d8bb73c3d9afd7156afc71b0c97fb1659917805e`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Sat, 18 Jan 2020 03:18:30 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:18:30 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:18:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 03:18:30 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 24 Jan 2020 07:05:12 GMT
ENV PHP_VERSION=7.4.2
# Fri, 24 Jan 2020 07:05:13 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.2.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.2.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 07:05:13 GMT
ENV PHP_SHA256=98284deac017da0d426117ecae7599a1f1bf62ae3911e8bc16c4403a8f4bdf13 PHP_MD5=
# Fri, 24 Jan 2020 07:05:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 24 Jan 2020 07:05:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 07:13:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 07:13:16 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Fri, 24 Jan 2020 07:13:17 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 07:13:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 07:13:17 GMT
CMD ["php" "-a"]
# Fri, 24 Jan 2020 10:52:17 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 24 Jan 2020 10:52:17 GMT
STOPSIGNAL SIGINT
# Fri, 24 Jan 2020 10:52:18 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 24 Jan 2020 10:52:18 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 10:52:19 GMT
RUN apk add --no-cache libpq
# Fri, 24 Jan 2020 10:52:38 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Fri, 24 Jan 2020 10:52:39 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 31 Jan 2020 17:19:26 GMT
ENV ADMINER_VERSION=4.7.6
# Fri, 31 Jan 2020 17:19:26 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Fri, 31 Jan 2020 17:19:26 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Fri, 31 Jan 2020 17:19:27 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 31 Jan 2020 17:19:28 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 31 Jan 2020 17:19:28 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 31 Jan 2020 17:19:28 GMT
USER adminer
# Fri, 31 Jan 2020 17:19:28 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 31 Jan 2020 17:19:28 GMT
EXPOSE 8080
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
	-	`sha256:5fa47f19b1e835f47f4c1273ccb215a42ee2aefafe300409d92b05b899a757d8`  
		Last Modified: Fri, 24 Jan 2020 10:39:33 GMT  
		Size: 10.3 MB (10271096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4556adb19ddcb43be3cd12b973f718e5edc74d6986ae4406a0c3011cbeb3dc93`  
		Last Modified: Fri, 24 Jan 2020 10:39:33 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:205de55b7ed0d389ac2c9777321f11ba9377a148002c2ef1d7b68d02a96472f3`  
		Last Modified: Fri, 24 Jan 2020 10:39:42 GMT  
		Size: 14.6 MB (14574023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c35aa7da966a732561c37c8b5d56949eedcb7865066b86da95c8bc58c18c48d2`  
		Last Modified: Fri, 24 Jan 2020 10:39:32 GMT  
		Size: 2.2 KB (2216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82a54ca6f814c156199e3266c4297efe2f54fb83bfb1645f53582eae3d1e222e`  
		Last Modified: Fri, 24 Jan 2020 10:39:33 GMT  
		Size: 73.1 KB (73145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e28f69f8cf7d397d8bd78cab68b9713275989e440016ec98580b94d0b0dc23f8`  
		Last Modified: Fri, 24 Jan 2020 10:53:42 GMT  
		Size: 306.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b527d0b89c2ea24dd10be7c18c1dcdf592fd4e1a5ff2c9da47fba2940fbb25a7`  
		Last Modified: Fri, 24 Jan 2020 10:53:42 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35b881820e3f1402cd2b2836dc6064db1b8ef029479448d5a058baa86b0f2e29`  
		Last Modified: Fri, 24 Jan 2020 10:53:41 GMT  
		Size: 1.3 MB (1277246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97e920225fdf7c9fc6bd8762ee3efbc9225341331c21812757347e46b22a2db3`  
		Last Modified: Fri, 24 Jan 2020 10:53:41 GMT  
		Size: 126.6 KB (126617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c8cde070aec4f16d202102cbdad6a161e48b4ffae4426da85717e9ee116fbec`  
		Last Modified: Fri, 24 Jan 2020 10:53:40 GMT  
		Size: 1.5 KB (1474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:028d5feebf26f852c8d09343a1b1ea1be953837a2f402743e1c021ea7b15ccee`  
		Last Modified: Fri, 31 Jan 2020 17:19:44 GMT  
		Size: 570.7 KB (570688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e0b9ec991cbee8b6377946c76367fcaa9782c4be8d265be834c5158b2638d40`  
		Last Modified: Fri, 31 Jan 2020 17:19:44 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7.6-standalone` - linux; arm variant v6

```console
$ docker pull adminer@sha256:086342d4149c1554e7c334711e0c6ccfa783ce0991cdd33d1687ca56e83020c7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.8 MB (29825140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08598589c478e6d488e3d5892d914c3ccac2ca333bf32b79046b127a04438a92`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Sat, 18 Jan 2020 03:40:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:40:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:40:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 03:40:19 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 20 Feb 2020 21:49:41 GMT
ENV PHP_VERSION=7.4.3
# Thu, 20 Feb 2020 21:49:43 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.3.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.3.tar.xz.asc/from/this/mirror
# Thu, 20 Feb 2020 21:49:44 GMT
ENV PHP_SHA256=cf1f856d877c268124ded1ede40c9fb6142b125fdaafdc54f855120b8bc6982a PHP_MD5=
# Thu, 20 Feb 2020 21:49:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Feb 2020 21:49:57 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Feb 2020 21:53:47 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 20 Feb 2020 21:53:50 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 20 Feb 2020 21:53:53 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Feb 2020 21:53:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Feb 2020 21:53:54 GMT
CMD ["php" "-a"]
# Thu, 20 Feb 2020 23:45:59 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Thu, 20 Feb 2020 23:45:59 GMT
STOPSIGNAL SIGINT
# Thu, 20 Feb 2020 23:46:02 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 20 Feb 2020 23:46:03 GMT
WORKDIR /var/www/html
# Thu, 20 Feb 2020 23:46:05 GMT
RUN apk add --no-cache libpq
# Thu, 20 Feb 2020 23:46:36 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Thu, 20 Feb 2020 23:46:39 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Thu, 20 Feb 2020 23:46:41 GMT
ENV ADMINER_VERSION=4.7.6
# Thu, 20 Feb 2020 23:46:41 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Thu, 20 Feb 2020 23:46:42 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Thu, 20 Feb 2020 23:46:45 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Thu, 20 Feb 2020 23:46:46 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 20 Feb 2020 23:46:46 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Thu, 20 Feb 2020 23:46:47 GMT
USER adminer
# Thu, 20 Feb 2020 23:46:48 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 20 Feb 2020 23:46:48 GMT
EXPOSE 8080
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
	-	`sha256:f246fe8b62d43a3f633a04898577258a2ce5dd84edf5fd464403b9a108b301e2`  
		Last Modified: Thu, 20 Feb 2020 23:10:06 GMT  
		Size: 10.3 MB (10280264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b4e0af10768397859f6f19eca4b17ee9f21d61a1cb06989aba861267cf1b6a`  
		Last Modified: Thu, 20 Feb 2020 23:10:05 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a228bdc8e070add11170637553b04b0eeab55a8af3159561b2878b3bcc00bbb`  
		Last Modified: Thu, 20 Feb 2020 23:10:11 GMT  
		Size: 13.6 MB (13600067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:936640ed543c6bb114e0374d4aa5d00b0ad989151337d4edfe6047bad672c605`  
		Last Modified: Thu, 20 Feb 2020 23:10:05 GMT  
		Size: 2.2 KB (2214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071eed09e44daa0c7c7d337a517208fa4a3c08e02029c0970082688456496bec`  
		Last Modified: Thu, 20 Feb 2020 23:10:05 GMT  
		Size: 72.7 KB (72679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:500b89ded2f6c4841beacd80fbbc9393d964cc71bd39c391faf7dc97822dbdb9`  
		Last Modified: Thu, 20 Feb 2020 23:47:57 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512f9b08d8b23f60cb6dff75b2270418b1aef35536dd655abbebc984b88a251b`  
		Last Modified: Thu, 20 Feb 2020 23:47:58 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c471a8e9c45607043e4014b7f0974b76407454a97e750d9055d0aa5e834e6739`  
		Last Modified: Thu, 20 Feb 2020 23:47:56 GMT  
		Size: 1.2 MB (1234698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7b673bbf243a89365a23ad683cd4498bf6d1d0ed02684c8a18d0a21cb8d178`  
		Last Modified: Thu, 20 Feb 2020 23:47:55 GMT  
		Size: 120.1 KB (120109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c24ab3064784c4410d659ea6e1f0df253d4425d982dc6458c3a3ba583e9b8ec5`  
		Last Modified: Thu, 20 Feb 2020 23:47:56 GMT  
		Size: 1.5 KB (1470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f98dd355d60f4139fe6bc5acd57c5dddf79d2130ae3198cc94d132632d3727`  
		Last Modified: Thu, 20 Feb 2020 23:47:56 GMT  
		Size: 570.8 KB (570766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9027f8cb6506a233c5d6eee529c13558fd054e963701cb92c8151588f40361cb`  
		Last Modified: Thu, 20 Feb 2020 23:47:55 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7.6-standalone` - linux; arm variant v7

```console
$ docker pull adminer@sha256:46b5ed40565812c4e0553a75ca1a4b5bffb897b489e88cb69626a97bb5de6a91
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.6 MB (28569758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f180ec2391291be9bea6f1f484659a40aa29806d769cebcb326e9b3da944208`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Sat, 18 Jan 2020 05:22:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 05:22:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 05:22:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 05:22:49 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 20 Feb 2020 21:11:31 GMT
ENV PHP_VERSION=7.4.3
# Thu, 20 Feb 2020 21:11:32 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.3.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.3.tar.xz.asc/from/this/mirror
# Thu, 20 Feb 2020 21:11:32 GMT
ENV PHP_SHA256=cf1f856d877c268124ded1ede40c9fb6142b125fdaafdc54f855120b8bc6982a PHP_MD5=
# Thu, 20 Feb 2020 21:11:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Feb 2020 21:11:37 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Feb 2020 21:13:57 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 20 Feb 2020 21:13:59 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 20 Feb 2020 21:14:01 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Feb 2020 21:14:02 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Feb 2020 21:14:02 GMT
CMD ["php" "-a"]
# Thu, 20 Feb 2020 23:50:58 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Thu, 20 Feb 2020 23:50:58 GMT
STOPSIGNAL SIGINT
# Thu, 20 Feb 2020 23:51:00 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 20 Feb 2020 23:51:02 GMT
WORKDIR /var/www/html
# Thu, 20 Feb 2020 23:51:04 GMT
RUN apk add --no-cache libpq
# Thu, 20 Feb 2020 23:51:35 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Thu, 20 Feb 2020 23:51:36 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Thu, 20 Feb 2020 23:51:37 GMT
ENV ADMINER_VERSION=4.7.6
# Thu, 20 Feb 2020 23:51:38 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Thu, 20 Feb 2020 23:51:39 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Thu, 20 Feb 2020 23:51:42 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Thu, 20 Feb 2020 23:51:43 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 20 Feb 2020 23:51:44 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Thu, 20 Feb 2020 23:51:45 GMT
USER adminer
# Thu, 20 Feb 2020 23:51:46 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 20 Feb 2020 23:51:47 GMT
EXPOSE 8080
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
	-	`sha256:6c492689366599e65cb0add947004a2dba1350bb15c7e6d5cf0926aba55ce6ec`  
		Last Modified: Thu, 20 Feb 2020 23:26:18 GMT  
		Size: 10.3 MB (10280256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e5617623e9ad0a01e633e336a37f6ff4d4a71c6cb1277692357d52303452d2f`  
		Last Modified: Thu, 20 Feb 2020 23:26:17 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4302d0c4f38943fda60770816f7eba1edb1d2f6a0c6f489e97ba67d9bdad574`  
		Last Modified: Thu, 20 Feb 2020 23:26:22 GMT  
		Size: 12.8 MB (12751449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc244875b6924b539df26879b4496e91b8eee4f5000e1ea5b774d83b9546b93`  
		Last Modified: Thu, 20 Feb 2020 23:26:18 GMT  
		Size: 2.2 KB (2214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04543010f9cd746143ced265c7b4b63d09ddc611588a131cbafe2099993fb5eb`  
		Last Modified: Thu, 20 Feb 2020 23:26:17 GMT  
		Size: 72.7 KB (72683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccb0170041c03fedc1121c07c7a06ee726f8a727c7c1eb5af04d1ee8f5654d5`  
		Last Modified: Thu, 20 Feb 2020 23:53:18 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1581d0fa71215a6ef8bb771f93fa001d361b8a02c3976b035408c6846e18be`  
		Last Modified: Thu, 20 Feb 2020 23:53:18 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f10e2f522b5d5b3116470d1761f55ab3feeb58372a087e3f6e80ea4f8f9dce7`  
		Last Modified: Thu, 20 Feb 2020 23:53:16 GMT  
		Size: 1.1 MB (1124902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c7b2368289baa2b3bc92adf31146c857cd78eecc8908bc78513c4f768c50323`  
		Last Modified: Thu, 20 Feb 2020 23:53:16 GMT  
		Size: 115.0 KB (114953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:765ac7cdcb3c5567be3929620bd1b2714a2af370ad604183f149ad40b19fd29c`  
		Last Modified: Thu, 20 Feb 2020 23:53:16 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45fe2c562cb0866875f0499d9583698863ee29b34a5a94406a42202b70885f6f`  
		Last Modified: Thu, 20 Feb 2020 23:53:16 GMT  
		Size: 570.8 KB (570772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e31dee670440ee2efcb54b84d9b9acccc709250fcb875c7ab9f31b21aded9fc`  
		Last Modified: Thu, 20 Feb 2020 23:53:16 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7.6-standalone` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:d6ac77d178d83433a94f4c1ac85d37eb6bde9a3b5e2ddd70510ab8366580d72d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 MB (30795142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59720519dbc2aaa04f42da6be01d883724212b4503025e14148efe901e90b553`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Sat, 18 Jan 2020 02:29:26 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 02:29:26 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 02:29:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 02:29:29 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 24 Jan 2020 00:09:58 GMT
ENV PHP_VERSION=7.4.2
# Fri, 24 Jan 2020 00:10:02 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.2.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.2.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 00:10:03 GMT
ENV PHP_SHA256=98284deac017da0d426117ecae7599a1f1bf62ae3911e8bc16c4403a8f4bdf13 PHP_MD5=
# Fri, 24 Jan 2020 00:10:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 24 Jan 2020 00:10:10 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 00:14:01 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 00:14:05 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Fri, 24 Jan 2020 00:14:09 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 00:14:10 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 00:14:11 GMT
CMD ["php" "-a"]
# Fri, 24 Jan 2020 02:50:27 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 24 Jan 2020 02:50:28 GMT
STOPSIGNAL SIGINT
# Fri, 24 Jan 2020 02:50:32 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 24 Jan 2020 02:50:32 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 02:50:36 GMT
RUN apk add --no-cache libpq
# Fri, 24 Jan 2020 02:51:09 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Fri, 24 Jan 2020 02:51:10 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 31 Jan 2020 17:39:37 GMT
ENV ADMINER_VERSION=4.7.6
# Fri, 31 Jan 2020 17:39:37 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Fri, 31 Jan 2020 17:39:38 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Fri, 31 Jan 2020 17:39:40 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 31 Jan 2020 17:39:41 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 31 Jan 2020 17:39:42 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 31 Jan 2020 17:39:42 GMT
USER adminer
# Fri, 31 Jan 2020 17:39:43 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 31 Jan 2020 17:39:44 GMT
EXPOSE 8080
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
	-	`sha256:aa724be546925194dbbb305717c1ec1404bd825d4e768f5fa30758fc836a1dda`  
		Last Modified: Fri, 24 Jan 2020 02:37:49 GMT  
		Size: 10.3 MB (10271109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b0bc8c61926931859ef4bf710fb73b709a407ca1086dfe704e7654934b4bdd`  
		Last Modified: Fri, 24 Jan 2020 02:37:45 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07be412705d63c11275e2018adae846b8861d4f678a21f2c43e2c22ae0bcee6d`  
		Last Modified: Fri, 24 Jan 2020 02:37:49 GMT  
		Size: 14.4 MB (14366228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73cafd3dde7ad30752409223dc0b26b0a5f4fa98d9a875225e2566bd99806655`  
		Last Modified: Fri, 24 Jan 2020 02:37:45 GMT  
		Size: 2.2 KB (2216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59195632759b7e9a57fb9ac253284ecbea9055d01c12f9caa49d23ca8f40bc1c`  
		Last Modified: Fri, 24 Jan 2020 02:37:45 GMT  
		Size: 72.7 KB (72676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6576a2f957338815a3fd8d1023a31cbb8ef8592406942ab75483b02adbe1c384`  
		Last Modified: Fri, 24 Jan 2020 02:52:47 GMT  
		Size: 310.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f6446e74a0df8b21f4f9ad86cf10fa3f6b6a9231d643d4174a5ddd3cf84f184`  
		Last Modified: Fri, 24 Jan 2020 02:52:47 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b69655ccf3f62cf1149958c93543bc91f9addef901545f4c74831b5c65b29039`  
		Last Modified: Fri, 24 Jan 2020 02:52:44 GMT  
		Size: 1.3 MB (1299236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:986406fbe9d0af0aeacc6c7cc032415d7552b4fd8f3fe60ea2313caa9193649c`  
		Last Modified: Fri, 24 Jan 2020 02:52:44 GMT  
		Size: 124.7 KB (124696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:382b47ced56d800090d03dff8f4d1183a7209bfd39013db12812d2efc2a39f54`  
		Last Modified: Fri, 24 Jan 2020 02:52:44 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23f30f175d57f1ffdc2f5c4308d886c2f842ce1a163c77b1747b628a89684ac`  
		Last Modified: Fri, 31 Jan 2020 17:40:10 GMT  
		Size: 570.8 KB (570779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d5044dac86a165d99ffacf0aaeb789461f31935ef0847d4e80ae612f101599`  
		Last Modified: Fri, 31 Jan 2020 17:40:10 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7.6-standalone` - linux; 386

```console
$ docker pull adminer@sha256:d094fa6fd940847cd20c8dd698284d004cf1d6a5fa23d777f0b19667afa76346
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31684075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed77c13afb1993912752a1a0383da2185144a458fde112b713496146d193cb19`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Sat, 18 Jan 2020 05:41:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 05:41:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 05:41:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 05:41:39 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 23 Jan 2020 23:13:49 GMT
ENV PHP_VERSION=7.4.2
# Thu, 23 Jan 2020 23:13:49 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.2.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.2.tar.xz.asc/from/this/mirror
# Thu, 23 Jan 2020 23:13:49 GMT
ENV PHP_SHA256=98284deac017da0d426117ecae7599a1f1bf62ae3911e8bc16c4403a8f4bdf13 PHP_MD5=
# Thu, 23 Jan 2020 23:13:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 23 Jan 2020 23:13:52 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Jan 2020 23:21:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 23 Jan 2020 23:21:57 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 23 Jan 2020 23:21:59 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Jan 2020 23:21:59 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Jan 2020 23:22:00 GMT
CMD ["php" "-a"]
# Fri, 24 Jan 2020 07:25:41 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 24 Jan 2020 07:25:41 GMT
STOPSIGNAL SIGINT
# Fri, 24 Jan 2020 07:25:42 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 24 Jan 2020 07:25:42 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 07:25:43 GMT
RUN apk add --no-cache libpq
# Fri, 24 Jan 2020 07:26:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Fri, 24 Jan 2020 07:26:02 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 31 Jan 2020 17:38:17 GMT
ENV ADMINER_VERSION=4.7.6
# Fri, 31 Jan 2020 17:38:18 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Fri, 31 Jan 2020 17:38:18 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Fri, 31 Jan 2020 17:38:19 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 31 Jan 2020 17:38:19 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 31 Jan 2020 17:38:20 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 31 Jan 2020 17:38:20 GMT
USER adminer
# Fri, 31 Jan 2020 17:38:20 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 31 Jan 2020 17:38:20 GMT
EXPOSE 8080
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
	-	`sha256:9f3628b223c4b093cf7c2d7723ccd39dfcb6977a659c9c183e7673f22f44865b`  
		Last Modified: Fri, 24 Jan 2020 02:36:11 GMT  
		Size: 10.3 MB (10271099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e167c61f346105deafdbe6bff7f521715a3d31cd4c9ca27d6dca67654d916c`  
		Last Modified: Fri, 24 Jan 2020 02:36:08 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53425617927914b1561c930b3ce2f90644de41394e731ca71a5d66feeba55d5b`  
		Last Modified: Fri, 24 Jan 2020 02:36:19 GMT  
		Size: 15.0 MB (14974599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809347a8b4ae69caee1b666ac61ec86e0f2dd5d64744592a59f65fd9bb49c7c9`  
		Last Modified: Fri, 24 Jan 2020 02:36:10 GMT  
		Size: 2.2 KB (2216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31917077d16c99b9c58e44f9267cbda55763d759a59379d7e4ca1f9fd6acf60a`  
		Last Modified: Fri, 24 Jan 2020 02:36:09 GMT  
		Size: 72.3 KB (72331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc6ba5ae7aae77ac94c185eef225136d01333d8840f8896b412e359fa89e3ae6`  
		Last Modified: Fri, 24 Jan 2020 07:27:19 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aab9a7fed181e4a8d1621cf6e92e6b4525a242e1c102cac7a259b3336202c16`  
		Last Modified: Fri, 24 Jan 2020 07:27:19 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1120969ea66ac41447ffffddcda8e8d389a0a1c0c7feb7d9d650117b973459d`  
		Last Modified: Fri, 24 Jan 2020 07:27:18 GMT  
		Size: 1.4 MB (1397662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cf37d29a0120ccd9ef7f4f99c6d10673cd93097ebe961c86faf275c144f5929`  
		Last Modified: Fri, 24 Jan 2020 07:27:18 GMT  
		Size: 130.8 KB (130760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf17f4f8d6baa9c93722150405686cf214bc377adbb7ff2b891efe5ca38809c9`  
		Last Modified: Fri, 24 Jan 2020 07:27:18 GMT  
		Size: 1.5 KB (1472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cac8221b3739531c0e54a60c4d8d795c187ce863f2fb79955540c1b62347fbc7`  
		Last Modified: Fri, 31 Jan 2020 17:38:36 GMT  
		Size: 570.7 KB (570691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8127a70cc3e20105c94ab16913cab965e775aaa7cb37cc6398e47d4a1830241e`  
		Last Modified: Fri, 31 Jan 2020 17:38:36 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7.6-standalone` - linux; ppc64le

```console
$ docker pull adminer@sha256:8906a11939b6681a5c547d8a1b3d8e58493fb85a66ef14177592239c9cd3ab6f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32169343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:251a9f8c0d32635a09c63fc8d5e5fbad2fee09cca0a4ea7cca903b5d9ac6f815`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Sat, 18 Jan 2020 03:24:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:24:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:24:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 03:24:34 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 23 Jan 2020 23:32:44 GMT
ENV PHP_VERSION=7.4.2
# Thu, 23 Jan 2020 23:32:47 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.2.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.2.tar.xz.asc/from/this/mirror
# Thu, 23 Jan 2020 23:32:50 GMT
ENV PHP_SHA256=98284deac017da0d426117ecae7599a1f1bf62ae3911e8bc16c4403a8f4bdf13 PHP_MD5=
# Thu, 23 Jan 2020 23:33:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 23 Jan 2020 23:33:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Jan 2020 23:36:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 23 Jan 2020 23:36:54 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 23 Jan 2020 23:37:00 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Jan 2020 23:37:02 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Jan 2020 23:37:04 GMT
CMD ["php" "-a"]
# Fri, 24 Jan 2020 05:51:10 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 24 Jan 2020 05:51:12 GMT
STOPSIGNAL SIGINT
# Fri, 24 Jan 2020 05:51:17 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 24 Jan 2020 05:51:19 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 05:51:23 GMT
RUN apk add --no-cache libpq
# Fri, 24 Jan 2020 05:51:48 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Fri, 24 Jan 2020 05:51:50 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 31 Jan 2020 17:16:45 GMT
ENV ADMINER_VERSION=4.7.6
# Fri, 31 Jan 2020 17:16:48 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Fri, 31 Jan 2020 17:16:51 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Fri, 31 Jan 2020 17:17:00 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 31 Jan 2020 17:17:01 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 31 Jan 2020 17:17:03 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 31 Jan 2020 17:17:05 GMT
USER adminer
# Fri, 31 Jan 2020 17:17:08 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 31 Jan 2020 17:17:10 GMT
EXPOSE 8080
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
	-	`sha256:c24c1e693453ad6efa656fcfa28e76c0786f80b4467d83c277d1116117942973`  
		Last Modified: Fri, 24 Jan 2020 02:32:44 GMT  
		Size: 10.3 MB (10271124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb71fc05f0fe0d365d8b9891f304e0cf2c1f6f0d2200ecdc0ea9a1c569117a1d`  
		Last Modified: Fri, 24 Jan 2020 02:32:41 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf26116548345ee1f676a6c1fabb768cd60750eb7a3a0ac7f09724350dde3b1`  
		Last Modified: Fri, 24 Jan 2020 02:32:54 GMT  
		Size: 15.5 MB (15539990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc4f870d6f2e6bbade33c0f28534b50765c4b56a093dc7565bd3ec3b37a7c603`  
		Last Modified: Fri, 24 Jan 2020 02:32:41 GMT  
		Size: 2.2 KB (2211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6a738ee51d709e4c4db983f9206a240500a2fc0dbaf3c76f6da2f99e5f6eb3b`  
		Last Modified: Fri, 24 Jan 2020 02:32:41 GMT  
		Size: 73.0 KB (72992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47bf1b73f7bf1089b7cf019ae582b63d77fa46e6c5b2b4efc16b0bf9d9b1ad9a`  
		Last Modified: Fri, 24 Jan 2020 05:53:47 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f984dcaccfb46a5cafd49380217e97342575055ceaaab4ff65a67f43af2da028`  
		Last Modified: Fri, 24 Jan 2020 05:53:47 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9e4520026a60556f0b631a13532b9a39d91d8eae94d4d3514359ef189ce4c94`  
		Last Modified: Fri, 24 Jan 2020 05:53:45 GMT  
		Size: 1.4 MB (1350626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba57cd117c3f571c3379a3fbb16d112291f4de925499dfeaad0bc7966c9483fb`  
		Last Modified: Fri, 24 Jan 2020 05:53:44 GMT  
		Size: 135.9 KB (135919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faef1730db86976915b65b75f76c1a057c321a983034e019f37ec833f5a1ffc9`  
		Last Modified: Fri, 24 Jan 2020 05:53:44 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:620c9c1b5881ba0a3be097e7cb57c695406737868e7b1adc02c5561c5f7b1649`  
		Last Modified: Fri, 31 Jan 2020 17:18:05 GMT  
		Size: 570.8 KB (570776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03e77753eec72902172405ef4c8c0c667bf7377cd0dc6cc1441afd0890991d43`  
		Last Modified: Fri, 31 Jan 2020 17:18:04 GMT  
		Size: 501.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:4.7-fastcgi`

```console
$ docker pull adminer@sha256:85ef53ce6942c89cdacf05991c16132da81d158741e42e2eef13b3c4111ba801
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `adminer:4.7-fastcgi` - linux; amd64

```console
$ docker pull adminer@sha256:3261472ab50e9daaf45a30818ad65311dc175417adf46363ecf18c7fb79f4048
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31132621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f894c56f8bea377d752a7839e5b2af6ffeab97af51d7b9b54e8c3113a954b088`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
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
# Sat, 18 Jan 2020 03:23:44 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 24 Jan 2020 07:13:33 GMT
ENV PHP_VERSION=7.4.2
# Fri, 24 Jan 2020 07:13:33 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.2.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.2.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 07:13:34 GMT
ENV PHP_SHA256=98284deac017da0d426117ecae7599a1f1bf62ae3911e8bc16c4403a8f4bdf13 PHP_MD5=
# Fri, 24 Jan 2020 07:13:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 24 Jan 2020 07:13:36 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 07:19:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 07:19:23 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Fri, 24 Jan 2020 07:19:24 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 07:19:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 07:19:24 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 07:19:25 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 24 Jan 2020 07:19:25 GMT
STOPSIGNAL SIGQUIT
# Fri, 24 Jan 2020 07:19:25 GMT
EXPOSE 9000
# Fri, 24 Jan 2020 07:19:25 GMT
CMD ["php-fpm"]
# Fri, 24 Jan 2020 10:52:50 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 24 Jan 2020 10:52:51 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 24 Jan 2020 10:52:52 GMT
RUN apk add --no-cache libpq
# Fri, 24 Jan 2020 10:53:11 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Fri, 24 Jan 2020 10:53:11 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 31 Jan 2020 17:19:33 GMT
ENV ADMINER_VERSION=4.7.6
# Fri, 31 Jan 2020 17:19:33 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Fri, 31 Jan 2020 17:19:33 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Fri, 31 Jan 2020 17:19:34 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 31 Jan 2020 17:19:34 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 31 Jan 2020 17:19:35 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 31 Jan 2020 17:19:35 GMT
USER adminer
# Fri, 31 Jan 2020 17:19:35 GMT
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
	-	`sha256:6e71cca12e10fbf7814b66f3f30f2c626a76931eb1658b35580520657aa1c472`  
		Last Modified: Fri, 24 Jan 2020 10:39:58 GMT  
		Size: 10.3 MB (10271098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed2310d2f7910e8f29ab569006386735c80fdb8d7a9f4b50c2233347335ef47e`  
		Last Modified: Fri, 24 Jan 2020 10:39:55 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:601ef2217a14892579aa55bfff77d380170c0c5b6bb97ba4275769e288cc008e`  
		Last Modified: Fri, 24 Jan 2020 10:40:00 GMT  
		Size: 14.6 MB (14640028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41dc18d982f54d4c5634f99e7933d9ad3069ef493b460cf998e1954caa2f24b7`  
		Last Modified: Fri, 24 Jan 2020 10:39:55 GMT  
		Size: 2.2 KB (2219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72be421f63f8c4ae023b97af91e72adcad7347edfff80e8fe6d0fea64be89f41`  
		Last Modified: Fri, 24 Jan 2020 10:39:56 GMT  
		Size: 73.1 KB (73144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f10dd871243fb2f678d5abcd0925bfc78bf759edf24b577c2aaaecce51ac30fb`  
		Last Modified: Fri, 24 Jan 2020 10:39:55 GMT  
		Size: 8.4 KB (8409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df30bf875af7c93a1a5f0231eb502f80916cc360f7bb5301af9fd174346bae03`  
		Last Modified: Fri, 24 Jan 2020 10:53:53 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb01654c81755c04f51d84470d9460f05137a60b5cb6af11a277b81ffdb12844`  
		Last Modified: Fri, 24 Jan 2020 10:53:53 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc08268651428df387dfafc653a2ce4c616f5eb02a72752692c59c871b99d37`  
		Last Modified: Fri, 24 Jan 2020 10:53:52 GMT  
		Size: 1.3 MB (1277248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ee28a212305aa260efa44f897f666e2d55a5c7b69b1eacb4913985baf64c9a`  
		Last Modified: Fri, 24 Jan 2020 10:53:52 GMT  
		Size: 126.6 KB (126627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60596dcdb9d8dba4d1f1beb1964daee86e4d999728581b4ed91e9edc6dd78a87`  
		Last Modified: Fri, 24 Jan 2020 10:53:52 GMT  
		Size: 1.5 KB (1474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30705479566e7b730c43bc045a5c98474f7fa05a827632e22deb9c00247a1792`  
		Last Modified: Fri, 31 Jan 2020 17:19:53 GMT  
		Size: 570.7 KB (570684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d656991abfa4ac7b964071b05e6a5c7e82cfb72e2de48fb119f733649768109`  
		Last Modified: Fri, 31 Jan 2020 17:19:53 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7-fastcgi` - linux; arm variant v6

```console
$ docker pull adminer@sha256:f3ef94b81d53fa10bdf91813ec1727746da25896c82eb5418da6183ff345fe42
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.9 MB (29904916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13e34cefffcf1ef42f5bc12f108decf6d572e5812224b5f36b8008069927885c`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
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
# Sat, 18 Jan 2020 03:44:54 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 20 Feb 2020 21:54:14 GMT
ENV PHP_VERSION=7.4.3
# Thu, 20 Feb 2020 21:54:15 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.3.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.3.tar.xz.asc/from/this/mirror
# Thu, 20 Feb 2020 21:54:16 GMT
ENV PHP_SHA256=cf1f856d877c268124ded1ede40c9fb6142b125fdaafdc54f855120b8bc6982a PHP_MD5=
# Thu, 20 Feb 2020 21:54:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Feb 2020 21:54:23 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Feb 2020 21:58:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 20 Feb 2020 21:58:38 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Thu, 20 Feb 2020 21:58:41 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Feb 2020 21:58:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Feb 2020 21:58:43 GMT
WORKDIR /var/www/html
# Thu, 20 Feb 2020 21:58:45 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 20 Feb 2020 21:58:46 GMT
STOPSIGNAL SIGQUIT
# Thu, 20 Feb 2020 21:58:48 GMT
EXPOSE 9000
# Thu, 20 Feb 2020 21:58:49 GMT
CMD ["php-fpm"]
# Thu, 20 Feb 2020 23:47:03 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Thu, 20 Feb 2020 23:47:05 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 20 Feb 2020 23:47:07 GMT
RUN apk add --no-cache libpq
# Thu, 20 Feb 2020 23:47:34 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Thu, 20 Feb 2020 23:47:35 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Thu, 20 Feb 2020 23:47:35 GMT
ENV ADMINER_VERSION=4.7.6
# Thu, 20 Feb 2020 23:47:36 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Thu, 20 Feb 2020 23:47:37 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Thu, 20 Feb 2020 23:47:40 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Thu, 20 Feb 2020 23:47:41 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 20 Feb 2020 23:47:41 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Thu, 20 Feb 2020 23:47:42 GMT
USER adminer
# Thu, 20 Feb 2020 23:47:42 GMT
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
	-	`sha256:80ca3c99ad3f93290cc94e506f94e8b01e2bfe5d2901b45ad4fd1bf704e70ed7`  
		Last Modified: Thu, 20 Feb 2020 23:10:40 GMT  
		Size: 10.3 MB (10280253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f658c7e1eb0d0386247f8fa5f228f97f709e09b53982bd1ba92f38cad3803ec8`  
		Last Modified: Thu, 20 Feb 2020 23:10:36 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38dd2d597adffab2d9b483cfa2352a9413ca3868e55fccb30c7551e0c1a7cb57`  
		Last Modified: Thu, 20 Feb 2020 23:10:42 GMT  
		Size: 13.7 MB (13671450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bfdd3dff152326a8135a5747de2a94547b298afe86fe63946bb425bc30fba92`  
		Last Modified: Thu, 20 Feb 2020 23:10:36 GMT  
		Size: 2.2 KB (2213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5554b593396e1abf2813391b3b1c84e40383b0988321d2d63616a290aa7fed7d`  
		Last Modified: Thu, 20 Feb 2020 23:10:36 GMT  
		Size: 72.7 KB (72681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9159be50c0fe27b27be4abb997de85c54fd2d1308d35c5c6c97e4d118fdec6a0`  
		Last Modified: Thu, 20 Feb 2020 23:10:37 GMT  
		Size: 8.4 KB (8412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28aa812c7cc19a079c92c7f6eba0da1ecffdcf6f1fe4946898b7ec9ff1b6940a`  
		Last Modified: Thu, 20 Feb 2020 23:48:28 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a7c93eb4a00db350eb6b34997b1f9541d4851def62b039696d47ae3b25f55f8`  
		Last Modified: Thu, 20 Feb 2020 23:48:28 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:820825c9319f4e49d67cd84bb103b76d2cca8df1f674d7a84b6b5ef1f43afe3b`  
		Last Modified: Thu, 20 Feb 2020 23:48:23 GMT  
		Size: 1.2 MB (1234699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49c16bab556b699d17b5ef77dfbbc559d0fabd75d27f9eed069b3753331c0e5a`  
		Last Modified: Thu, 20 Feb 2020 23:48:23 GMT  
		Size: 120.1 KB (120098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1ec2a9c5203dcc61950a047d4f04c455f284b6062740fbc081a32c7fb5873b2`  
		Last Modified: Thu, 20 Feb 2020 23:48:23 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:295fdb00d23508c2695ae7402b772fdd479d44cd0f0a05c93b069242638a3e0f`  
		Last Modified: Thu, 20 Feb 2020 23:48:23 GMT  
		Size: 570.8 KB (570771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92b8b25d3ffd6ef7dd0976b4b19b04842ed268bfbc55452f5000ba913defa355`  
		Last Modified: Thu, 20 Feb 2020 23:48:23 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7-fastcgi` - linux; arm variant v7

```console
$ docker pull adminer@sha256:2f5f67a712318a2a917724f95730ad156ec7427834865497016e22de6541cc5c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.6 MB (28642438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c803a31f5e4241a9cb82515d1cc260871c3f62e3c30297d71a35973096a31e2`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
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
# Sat, 18 Jan 2020 05:28:02 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 20 Feb 2020 21:14:19 GMT
ENV PHP_VERSION=7.4.3
# Thu, 20 Feb 2020 21:14:19 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.3.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.3.tar.xz.asc/from/this/mirror
# Thu, 20 Feb 2020 21:14:20 GMT
ENV PHP_SHA256=cf1f856d877c268124ded1ede40c9fb6142b125fdaafdc54f855120b8bc6982a PHP_MD5=
# Thu, 20 Feb 2020 21:14:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Feb 2020 21:14:24 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Feb 2020 21:16:45 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 20 Feb 2020 21:16:46 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Thu, 20 Feb 2020 21:16:49 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Feb 2020 21:16:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Feb 2020 21:16:50 GMT
WORKDIR /var/www/html
# Thu, 20 Feb 2020 21:16:51 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 20 Feb 2020 21:16:52 GMT
STOPSIGNAL SIGQUIT
# Thu, 20 Feb 2020 21:16:53 GMT
EXPOSE 9000
# Thu, 20 Feb 2020 21:16:54 GMT
CMD ["php-fpm"]
# Thu, 20 Feb 2020 23:52:02 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Thu, 20 Feb 2020 23:52:05 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 20 Feb 2020 23:52:08 GMT
RUN apk add --no-cache libpq
# Thu, 20 Feb 2020 23:52:41 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Thu, 20 Feb 2020 23:52:43 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Thu, 20 Feb 2020 23:52:44 GMT
ENV ADMINER_VERSION=4.7.6
# Thu, 20 Feb 2020 23:52:45 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Thu, 20 Feb 2020 23:52:46 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Thu, 20 Feb 2020 23:52:49 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Thu, 20 Feb 2020 23:52:50 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 20 Feb 2020 23:52:51 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Thu, 20 Feb 2020 23:52:52 GMT
USER adminer
# Thu, 20 Feb 2020 23:52:54 GMT
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
	-	`sha256:0b327d731622fe78b5dce5377da7c2fa2a8f7f5bccb0851084b9329f9a570063`  
		Last Modified: Thu, 20 Feb 2020 23:26:52 GMT  
		Size: 10.3 MB (10280261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4b40e24dacf2616800de7bb9e410e263de6eccf4d1bfd5a22d32908c21b2361`  
		Last Modified: Thu, 20 Feb 2020 23:26:49 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e42a50422a3ffed17517bce0eb1fe538eea06417fdc672c4711d134108d7b0b4`  
		Last Modified: Thu, 20 Feb 2020 23:26:54 GMT  
		Size: 12.8 MB (12815724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5473e54c50261b361a070da14923a840b1c2155de57aacac9a8ff18575dd6e1a`  
		Last Modified: Thu, 20 Feb 2020 23:26:50 GMT  
		Size: 2.2 KB (2216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f939d7049d7edb45231e24fec17211f863a36748747b3121cc935b6760c86632`  
		Last Modified: Thu, 20 Feb 2020 23:26:49 GMT  
		Size: 72.7 KB (72680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e26488d2c5a3fcc5e1d56a02cd6a6755d2bf8a503dfb6bff0c265cedf52a11fa`  
		Last Modified: Thu, 20 Feb 2020 23:26:49 GMT  
		Size: 8.4 KB (8409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7b9f9e7ecb2380e21319c90bc307fa28a14061bc3b629ea3cafaebe8e7865e3`  
		Last Modified: Thu, 20 Feb 2020 23:53:39 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:214861e86ee457b4f34bad18e669992ef9dff229e599e0f7f15f41b926a9ec31`  
		Last Modified: Thu, 20 Feb 2020 23:53:39 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6f9a71b7d4f646e777f739107b1911cf18f3305a0f3348c54572385f6f5d71f`  
		Last Modified: Thu, 20 Feb 2020 23:53:37 GMT  
		Size: 1.1 MB (1124908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3757929f73de69aebca78a3f042c638bb48e703b5a1ce80fc02e2eae8b45cdf`  
		Last Modified: Thu, 20 Feb 2020 23:53:37 GMT  
		Size: 115.0 KB (114950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3151fc0a4ad4389a4655e265bca8650f675575130c4394907f6abe79dc4bacf3`  
		Last Modified: Thu, 20 Feb 2020 23:53:37 GMT  
		Size: 1.5 KB (1477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85281d825070bdddb16a2bacfad1baa7633a1a1e22d32c6ad458bbac70bc1737`  
		Last Modified: Thu, 20 Feb 2020 23:53:37 GMT  
		Size: 570.8 KB (570766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499386092f7399a059f809ff852ca1239313c7555831f07909a8cc81d06f386d`  
		Last Modified: Thu, 20 Feb 2020 23:53:37 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7-fastcgi` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:4f9923edd71c163c491fec06013c2c29c6c486e96f1a5a5fe9f6a15d7d0cdb08
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30872795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c607c25c09ed37fcb1262db44e11192f84fc037fe9d82ebbd207a31813123ff5`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
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
# Sat, 18 Jan 2020 02:36:11 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 24 Jan 2020 00:14:35 GMT
ENV PHP_VERSION=7.4.2
# Fri, 24 Jan 2020 00:14:36 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.2.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.2.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 00:14:38 GMT
ENV PHP_SHA256=98284deac017da0d426117ecae7599a1f1bf62ae3911e8bc16c4403a8f4bdf13 PHP_MD5=
# Fri, 24 Jan 2020 00:14:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 24 Jan 2020 00:14:45 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 00:18:29 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 00:18:32 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Fri, 24 Jan 2020 00:18:36 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 00:18:37 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 00:18:38 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 00:18:41 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 24 Jan 2020 00:18:42 GMT
STOPSIGNAL SIGQUIT
# Fri, 24 Jan 2020 00:18:44 GMT
EXPOSE 9000
# Fri, 24 Jan 2020 00:18:45 GMT
CMD ["php-fpm"]
# Fri, 24 Jan 2020 02:51:31 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 24 Jan 2020 02:51:33 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 24 Jan 2020 02:51:36 GMT
RUN apk add --no-cache libpq
# Fri, 24 Jan 2020 02:52:06 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Fri, 24 Jan 2020 02:52:07 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 31 Jan 2020 17:39:50 GMT
ENV ADMINER_VERSION=4.7.6
# Fri, 31 Jan 2020 17:39:51 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Fri, 31 Jan 2020 17:39:51 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Fri, 31 Jan 2020 17:39:54 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 31 Jan 2020 17:39:55 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 31 Jan 2020 17:39:55 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 31 Jan 2020 17:39:56 GMT
USER adminer
# Fri, 31 Jan 2020 17:39:57 GMT
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
	-	`sha256:031bf935aef9c8cf9a41b1dbd509b48db2ab230dae75e8d1f2f20c1713826cfa`  
		Last Modified: Fri, 24 Jan 2020 02:38:24 GMT  
		Size: 10.3 MB (10271108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd439e1038e9d42eab7437e8f85a4c7cd369089af8cb708e63e0c4388fdb1bf3`  
		Last Modified: Fri, 24 Jan 2020 02:38:16 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25ed1e9754e061a3e75c31e172b7e2ef4b7b5a8673a24423b2260a91000daed9`  
		Last Modified: Fri, 24 Jan 2020 02:38:20 GMT  
		Size: 14.4 MB (14435498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5801422dba8896819ba048a35c0da81a25eec8fb91c74ddc3da87bbbf13fd470`  
		Last Modified: Fri, 24 Jan 2020 02:38:16 GMT  
		Size: 2.2 KB (2217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d4f983059021c9010c5326e718d5870d3ed28a792a95b78f95399c93b6b963f`  
		Last Modified: Fri, 24 Jan 2020 02:38:16 GMT  
		Size: 72.7 KB (72672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:947d95e1f7678a8070ee18dba3cf26e07c11e7a0f1fed1885014776890783c64`  
		Last Modified: Fri, 24 Jan 2020 02:38:16 GMT  
		Size: 8.4 KB (8410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8246e4f25893c2c59d16a3a91eb0e024ee6b366eb1828d39c00069b0fe074821`  
		Last Modified: Fri, 24 Jan 2020 02:53:09 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153c72183d2af4959ab20862dab40a0a198583b2ed6460c78eb4b58afbe8099a`  
		Last Modified: Fri, 24 Jan 2020 02:53:08 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79ea398fe8d2d7940f02c220eac23b6e0b59f654452a7c2d784746f57264e66`  
		Last Modified: Fri, 24 Jan 2020 02:53:07 GMT  
		Size: 1.3 MB (1299219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a60c746308f1dc0af8f8ee2c44315d9bb1b416377a2938f63d9a70ab2d0f06ad`  
		Last Modified: Fri, 24 Jan 2020 02:53:07 GMT  
		Size: 124.7 KB (124702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca6bc7dce64e9b13729a1e1afd341a91788f4a0d94380b7cc81feec83f580bf6`  
		Last Modified: Fri, 24 Jan 2020 02:53:06 GMT  
		Size: 1.5 KB (1474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f1dac04eb03855c7c287673ef8e4c6d1c4915d3663f9376444abe8e8c3c1ed4`  
		Last Modified: Fri, 31 Jan 2020 17:40:25 GMT  
		Size: 570.8 KB (570773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44ddb8bdcd055db611ac57e0a6bc167bd231eaf893f9d7d11e3f0d13025cf98`  
		Last Modified: Fri, 31 Jan 2020 17:40:25 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7-fastcgi` - linux; 386

```console
$ docker pull adminer@sha256:46b8bb610eaaa99932c42a3352a7bb709eddd218944284a41d4a25ab9e2593db
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31762110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e5c58ebd525deeac88b11a3c516b9d22ac70308fcd0aeb5cc2624988423c31`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
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
# Sat, 18 Jan 2020 05:48:40 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 23 Jan 2020 23:22:10 GMT
ENV PHP_VERSION=7.4.2
# Thu, 23 Jan 2020 23:22:10 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.2.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.2.tar.xz.asc/from/this/mirror
# Thu, 23 Jan 2020 23:22:11 GMT
ENV PHP_SHA256=98284deac017da0d426117ecae7599a1f1bf62ae3911e8bc16c4403a8f4bdf13 PHP_MD5=
# Thu, 23 Jan 2020 23:22:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 23 Jan 2020 23:22:16 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Jan 2020 23:31:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 23 Jan 2020 23:31:14 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Thu, 23 Jan 2020 23:31:15 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Jan 2020 23:31:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Jan 2020 23:31:15 GMT
WORKDIR /var/www/html
# Thu, 23 Jan 2020 23:31:16 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 23 Jan 2020 23:31:16 GMT
STOPSIGNAL SIGQUIT
# Thu, 23 Jan 2020 23:31:16 GMT
EXPOSE 9000
# Thu, 23 Jan 2020 23:31:17 GMT
CMD ["php-fpm"]
# Fri, 24 Jan 2020 07:26:11 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 24 Jan 2020 07:26:12 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 24 Jan 2020 07:26:14 GMT
RUN apk add --no-cache libpq
# Fri, 24 Jan 2020 07:26:45 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Fri, 24 Jan 2020 07:26:45 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 31 Jan 2020 17:38:25 GMT
ENV ADMINER_VERSION=4.7.6
# Fri, 31 Jan 2020 17:38:25 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Fri, 31 Jan 2020 17:38:25 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Fri, 31 Jan 2020 17:38:26 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 31 Jan 2020 17:38:27 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 31 Jan 2020 17:38:27 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 31 Jan 2020 17:38:27 GMT
USER adminer
# Fri, 31 Jan 2020 17:38:27 GMT
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
	-	`sha256:7af2969e346cf39dce09953165d38ac70a637f81bf36a72173d23c8209522b1e`  
		Last Modified: Fri, 24 Jan 2020 02:36:49 GMT  
		Size: 10.3 MB (10271104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dffed627d6f3eb28e87526c201e8ae30d110efc1e7ae5b48646e1f322abddefd`  
		Last Modified: Fri, 24 Jan 2020 02:36:40 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44af2512ec067db56bee629528b24bfe54ad55f8f7064b2cf59f57868950482d`  
		Last Modified: Fri, 24 Jan 2020 02:36:51 GMT  
		Size: 15.0 MB (15044190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a34e204f3d52c0be6c78857ce18184fecbd91cf297cfb30bf15df00d78b1ff71`  
		Last Modified: Fri, 24 Jan 2020 02:36:40 GMT  
		Size: 2.2 KB (2217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c9a720f2eaf0aec04eabdd4c10f331bd1eb5e91bdf806ec43279ae4d9435107`  
		Last Modified: Fri, 24 Jan 2020 02:36:41 GMT  
		Size: 72.3 KB (72332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ce027d9508f9c2ba08e68a1cbef48753b345821147a4ec4dd52ced22ca8252`  
		Last Modified: Fri, 24 Jan 2020 02:36:40 GMT  
		Size: 8.4 KB (8413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:791ceb40ab90a13fa40d9a11daa5853b0d7c1f72f7fb2580891e34049e7be6ba`  
		Last Modified: Fri, 24 Jan 2020 07:27:33 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac79a09757dcd35db84f1d12d43f5d8f11408f92ee9e095c392eda59733b801a`  
		Last Modified: Fri, 24 Jan 2020 07:27:33 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b6beb85931082255a7f9048c7f337e1972e10ce8a02c86b86797e95922ad930`  
		Last Modified: Fri, 24 Jan 2020 07:27:34 GMT  
		Size: 1.4 MB (1397661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79d5b1485f733f60d9843f7e138f1fa150e42d713df194640dcc37931ec1c191`  
		Last Modified: Fri, 24 Jan 2020 07:27:31 GMT  
		Size: 130.8 KB (130793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:553d2e165ba3dd32a4a9a44d46fa13ec6552747310640f783b34255acfd961e2`  
		Last Modified: Fri, 24 Jan 2020 07:27:31 GMT  
		Size: 1.5 KB (1472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42e41cc3dbdf2dad75063abe783a7985dc9267ee1ee9bd5751bed6f0cba09c2b`  
		Last Modified: Fri, 31 Jan 2020 17:38:46 GMT  
		Size: 570.7 KB (570683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd7e34ec5637f78a0244c66e92539e53bcc0bc77fafc96f775c60a3dbfce14ef`  
		Last Modified: Fri, 31 Jan 2020 17:38:46 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7-fastcgi` - linux; ppc64le

```console
$ docker pull adminer@sha256:52c4be54d3cd71b8c7ef779124ae7e3796754fad9594b24584b157fe0d90ea88
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32259051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:058dcefad0447822a717afd8533b7ef7ac94f28229ce3c409df8c013633ad069`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
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
# Sat, 18 Jan 2020 03:29:20 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 23 Jan 2020 23:37:14 GMT
ENV PHP_VERSION=7.4.2
# Thu, 23 Jan 2020 23:37:17 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.2.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.2.tar.xz.asc/from/this/mirror
# Thu, 23 Jan 2020 23:37:18 GMT
ENV PHP_SHA256=98284deac017da0d426117ecae7599a1f1bf62ae3911e8bc16c4403a8f4bdf13 PHP_MD5=
# Thu, 23 Jan 2020 23:37:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 23 Jan 2020 23:37:30 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Jan 2020 23:41:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 23 Jan 2020 23:41:16 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Thu, 23 Jan 2020 23:41:21 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Jan 2020 23:41:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Jan 2020 23:41:25 GMT
WORKDIR /var/www/html
# Thu, 23 Jan 2020 23:41:31 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 23 Jan 2020 23:41:34 GMT
STOPSIGNAL SIGQUIT
# Thu, 23 Jan 2020 23:41:36 GMT
EXPOSE 9000
# Thu, 23 Jan 2020 23:41:37 GMT
CMD ["php-fpm"]
# Fri, 24 Jan 2020 05:52:24 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 24 Jan 2020 05:52:29 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 24 Jan 2020 05:52:35 GMT
RUN apk add --no-cache libpq
# Fri, 24 Jan 2020 05:53:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Fri, 24 Jan 2020 05:53:04 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 31 Jan 2020 17:17:22 GMT
ENV ADMINER_VERSION=4.7.6
# Fri, 31 Jan 2020 17:17:23 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Fri, 31 Jan 2020 17:17:24 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Fri, 31 Jan 2020 17:17:33 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 31 Jan 2020 17:17:35 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 31 Jan 2020 17:17:39 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 31 Jan 2020 17:17:42 GMT
USER adminer
# Fri, 31 Jan 2020 17:17:44 GMT
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
	-	`sha256:71750c6fa0607bea7a09ff35d6a1406245a40b8230624a3639b89d18db4394fe`  
		Last Modified: Fri, 24 Jan 2020 02:33:52 GMT  
		Size: 10.3 MB (10271124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9edfe3521268768bb7368d494a54a58f6ea37444d81365db80594ba5cf6723e`  
		Last Modified: Fri, 24 Jan 2020 02:33:41 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03d6040910816a926d5c549b0b705387c888406057cdb66956db3c32125ac16`  
		Last Modified: Fri, 24 Jan 2020 02:33:50 GMT  
		Size: 15.6 MB (15621302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60eae056a292b760c3cccf048be586d181427ad78105d2293c95ba02dbaf0ba1`  
		Last Modified: Fri, 24 Jan 2020 02:33:41 GMT  
		Size: 2.2 KB (2215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:728ffb10bff4c1ede1c201f677ecc8c6ad6fcaa32489ca45d7dc1ffb57804d89`  
		Last Modified: Fri, 24 Jan 2020 02:33:41 GMT  
		Size: 73.0 KB (72996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:348111edcf048b6a351ad6caed9d560f0dad7e6bbe2b76922a0648db42f74bcc`  
		Last Modified: Fri, 24 Jan 2020 02:33:42 GMT  
		Size: 8.4 KB (8409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b18f3572f56ef640587e5e01d586e9ac24e3c39688ad60eb7e2542c28330ef15`  
		Last Modified: Fri, 24 Jan 2020 05:54:24 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25b30d4afe834c4c6add7f1325d981a4767fe2d659474a4bcf07fe0982d30779`  
		Last Modified: Fri, 24 Jan 2020 05:54:23 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd12c1dc772a4360a1f25b4d61773bf85a5ce8636a383a26214f52199698c03a`  
		Last Modified: Fri, 24 Jan 2020 05:54:23 GMT  
		Size: 1.4 MB (1350625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc0b0a44d83a34b0167638ba083ff0f468a535b3a75087a1810e07394e5c6e8e`  
		Last Modified: Fri, 24 Jan 2020 05:54:20 GMT  
		Size: 135.9 KB (135904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1114f35e53ffc221921a3954ec43719e7f1e8adcc07c6b0f7b75364065ed97d7`  
		Last Modified: Fri, 24 Jan 2020 05:54:20 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:609b9a3cccb86ade52bbc4fb6a19223fa44f14509e75e7c2e4438278ef3a37b6`  
		Last Modified: Fri, 31 Jan 2020 17:18:36 GMT  
		Size: 570.8 KB (570772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b5ca04b772bc2f523594fd55735ad7e753da72ecf87478b23db102df001437`  
		Last Modified: Fri, 31 Jan 2020 17:18:36 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:4.7-standalone`

```console
$ docker pull adminer@sha256:c689401f4ee85e37ba2cd62d401af2d569833dd8efa2c338177889fa9c525882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `adminer:4.7-standalone` - linux; amd64

```console
$ docker pull adminer@sha256:6ceb642133ac56e267c50ae4bfb24ac0008b0eb02b772abae9059caa45211bee
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31058191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:259cc60bdb72538cffc06536d8bb73c3d9afd7156afc71b0c97fb1659917805e`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Sat, 18 Jan 2020 03:18:30 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:18:30 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:18:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 03:18:30 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 24 Jan 2020 07:05:12 GMT
ENV PHP_VERSION=7.4.2
# Fri, 24 Jan 2020 07:05:13 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.2.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.2.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 07:05:13 GMT
ENV PHP_SHA256=98284deac017da0d426117ecae7599a1f1bf62ae3911e8bc16c4403a8f4bdf13 PHP_MD5=
# Fri, 24 Jan 2020 07:05:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 24 Jan 2020 07:05:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 07:13:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 07:13:16 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Fri, 24 Jan 2020 07:13:17 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 07:13:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 07:13:17 GMT
CMD ["php" "-a"]
# Fri, 24 Jan 2020 10:52:17 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 24 Jan 2020 10:52:17 GMT
STOPSIGNAL SIGINT
# Fri, 24 Jan 2020 10:52:18 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 24 Jan 2020 10:52:18 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 10:52:19 GMT
RUN apk add --no-cache libpq
# Fri, 24 Jan 2020 10:52:38 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Fri, 24 Jan 2020 10:52:39 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 31 Jan 2020 17:19:26 GMT
ENV ADMINER_VERSION=4.7.6
# Fri, 31 Jan 2020 17:19:26 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Fri, 31 Jan 2020 17:19:26 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Fri, 31 Jan 2020 17:19:27 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 31 Jan 2020 17:19:28 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 31 Jan 2020 17:19:28 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 31 Jan 2020 17:19:28 GMT
USER adminer
# Fri, 31 Jan 2020 17:19:28 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 31 Jan 2020 17:19:28 GMT
EXPOSE 8080
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
	-	`sha256:5fa47f19b1e835f47f4c1273ccb215a42ee2aefafe300409d92b05b899a757d8`  
		Last Modified: Fri, 24 Jan 2020 10:39:33 GMT  
		Size: 10.3 MB (10271096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4556adb19ddcb43be3cd12b973f718e5edc74d6986ae4406a0c3011cbeb3dc93`  
		Last Modified: Fri, 24 Jan 2020 10:39:33 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:205de55b7ed0d389ac2c9777321f11ba9377a148002c2ef1d7b68d02a96472f3`  
		Last Modified: Fri, 24 Jan 2020 10:39:42 GMT  
		Size: 14.6 MB (14574023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c35aa7da966a732561c37c8b5d56949eedcb7865066b86da95c8bc58c18c48d2`  
		Last Modified: Fri, 24 Jan 2020 10:39:32 GMT  
		Size: 2.2 KB (2216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82a54ca6f814c156199e3266c4297efe2f54fb83bfb1645f53582eae3d1e222e`  
		Last Modified: Fri, 24 Jan 2020 10:39:33 GMT  
		Size: 73.1 KB (73145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e28f69f8cf7d397d8bd78cab68b9713275989e440016ec98580b94d0b0dc23f8`  
		Last Modified: Fri, 24 Jan 2020 10:53:42 GMT  
		Size: 306.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b527d0b89c2ea24dd10be7c18c1dcdf592fd4e1a5ff2c9da47fba2940fbb25a7`  
		Last Modified: Fri, 24 Jan 2020 10:53:42 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35b881820e3f1402cd2b2836dc6064db1b8ef029479448d5a058baa86b0f2e29`  
		Last Modified: Fri, 24 Jan 2020 10:53:41 GMT  
		Size: 1.3 MB (1277246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97e920225fdf7c9fc6bd8762ee3efbc9225341331c21812757347e46b22a2db3`  
		Last Modified: Fri, 24 Jan 2020 10:53:41 GMT  
		Size: 126.6 KB (126617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c8cde070aec4f16d202102cbdad6a161e48b4ffae4426da85717e9ee116fbec`  
		Last Modified: Fri, 24 Jan 2020 10:53:40 GMT  
		Size: 1.5 KB (1474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:028d5feebf26f852c8d09343a1b1ea1be953837a2f402743e1c021ea7b15ccee`  
		Last Modified: Fri, 31 Jan 2020 17:19:44 GMT  
		Size: 570.7 KB (570688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e0b9ec991cbee8b6377946c76367fcaa9782c4be8d265be834c5158b2638d40`  
		Last Modified: Fri, 31 Jan 2020 17:19:44 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7-standalone` - linux; arm variant v6

```console
$ docker pull adminer@sha256:086342d4149c1554e7c334711e0c6ccfa783ce0991cdd33d1687ca56e83020c7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.8 MB (29825140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08598589c478e6d488e3d5892d914c3ccac2ca333bf32b79046b127a04438a92`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Sat, 18 Jan 2020 03:40:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:40:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:40:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 03:40:19 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 20 Feb 2020 21:49:41 GMT
ENV PHP_VERSION=7.4.3
# Thu, 20 Feb 2020 21:49:43 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.3.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.3.tar.xz.asc/from/this/mirror
# Thu, 20 Feb 2020 21:49:44 GMT
ENV PHP_SHA256=cf1f856d877c268124ded1ede40c9fb6142b125fdaafdc54f855120b8bc6982a PHP_MD5=
# Thu, 20 Feb 2020 21:49:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Feb 2020 21:49:57 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Feb 2020 21:53:47 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 20 Feb 2020 21:53:50 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 20 Feb 2020 21:53:53 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Feb 2020 21:53:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Feb 2020 21:53:54 GMT
CMD ["php" "-a"]
# Thu, 20 Feb 2020 23:45:59 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Thu, 20 Feb 2020 23:45:59 GMT
STOPSIGNAL SIGINT
# Thu, 20 Feb 2020 23:46:02 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 20 Feb 2020 23:46:03 GMT
WORKDIR /var/www/html
# Thu, 20 Feb 2020 23:46:05 GMT
RUN apk add --no-cache libpq
# Thu, 20 Feb 2020 23:46:36 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Thu, 20 Feb 2020 23:46:39 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Thu, 20 Feb 2020 23:46:41 GMT
ENV ADMINER_VERSION=4.7.6
# Thu, 20 Feb 2020 23:46:41 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Thu, 20 Feb 2020 23:46:42 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Thu, 20 Feb 2020 23:46:45 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Thu, 20 Feb 2020 23:46:46 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 20 Feb 2020 23:46:46 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Thu, 20 Feb 2020 23:46:47 GMT
USER adminer
# Thu, 20 Feb 2020 23:46:48 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 20 Feb 2020 23:46:48 GMT
EXPOSE 8080
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
	-	`sha256:f246fe8b62d43a3f633a04898577258a2ce5dd84edf5fd464403b9a108b301e2`  
		Last Modified: Thu, 20 Feb 2020 23:10:06 GMT  
		Size: 10.3 MB (10280264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b4e0af10768397859f6f19eca4b17ee9f21d61a1cb06989aba861267cf1b6a`  
		Last Modified: Thu, 20 Feb 2020 23:10:05 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a228bdc8e070add11170637553b04b0eeab55a8af3159561b2878b3bcc00bbb`  
		Last Modified: Thu, 20 Feb 2020 23:10:11 GMT  
		Size: 13.6 MB (13600067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:936640ed543c6bb114e0374d4aa5d00b0ad989151337d4edfe6047bad672c605`  
		Last Modified: Thu, 20 Feb 2020 23:10:05 GMT  
		Size: 2.2 KB (2214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071eed09e44daa0c7c7d337a517208fa4a3c08e02029c0970082688456496bec`  
		Last Modified: Thu, 20 Feb 2020 23:10:05 GMT  
		Size: 72.7 KB (72679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:500b89ded2f6c4841beacd80fbbc9393d964cc71bd39c391faf7dc97822dbdb9`  
		Last Modified: Thu, 20 Feb 2020 23:47:57 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512f9b08d8b23f60cb6dff75b2270418b1aef35536dd655abbebc984b88a251b`  
		Last Modified: Thu, 20 Feb 2020 23:47:58 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c471a8e9c45607043e4014b7f0974b76407454a97e750d9055d0aa5e834e6739`  
		Last Modified: Thu, 20 Feb 2020 23:47:56 GMT  
		Size: 1.2 MB (1234698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7b673bbf243a89365a23ad683cd4498bf6d1d0ed02684c8a18d0a21cb8d178`  
		Last Modified: Thu, 20 Feb 2020 23:47:55 GMT  
		Size: 120.1 KB (120109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c24ab3064784c4410d659ea6e1f0df253d4425d982dc6458c3a3ba583e9b8ec5`  
		Last Modified: Thu, 20 Feb 2020 23:47:56 GMT  
		Size: 1.5 KB (1470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f98dd355d60f4139fe6bc5acd57c5dddf79d2130ae3198cc94d132632d3727`  
		Last Modified: Thu, 20 Feb 2020 23:47:56 GMT  
		Size: 570.8 KB (570766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9027f8cb6506a233c5d6eee529c13558fd054e963701cb92c8151588f40361cb`  
		Last Modified: Thu, 20 Feb 2020 23:47:55 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7-standalone` - linux; arm variant v7

```console
$ docker pull adminer@sha256:46b5ed40565812c4e0553a75ca1a4b5bffb897b489e88cb69626a97bb5de6a91
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.6 MB (28569758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f180ec2391291be9bea6f1f484659a40aa29806d769cebcb326e9b3da944208`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Sat, 18 Jan 2020 05:22:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 05:22:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 05:22:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 05:22:49 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 20 Feb 2020 21:11:31 GMT
ENV PHP_VERSION=7.4.3
# Thu, 20 Feb 2020 21:11:32 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.3.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.3.tar.xz.asc/from/this/mirror
# Thu, 20 Feb 2020 21:11:32 GMT
ENV PHP_SHA256=cf1f856d877c268124ded1ede40c9fb6142b125fdaafdc54f855120b8bc6982a PHP_MD5=
# Thu, 20 Feb 2020 21:11:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Feb 2020 21:11:37 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Feb 2020 21:13:57 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 20 Feb 2020 21:13:59 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 20 Feb 2020 21:14:01 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Feb 2020 21:14:02 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Feb 2020 21:14:02 GMT
CMD ["php" "-a"]
# Thu, 20 Feb 2020 23:50:58 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Thu, 20 Feb 2020 23:50:58 GMT
STOPSIGNAL SIGINT
# Thu, 20 Feb 2020 23:51:00 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 20 Feb 2020 23:51:02 GMT
WORKDIR /var/www/html
# Thu, 20 Feb 2020 23:51:04 GMT
RUN apk add --no-cache libpq
# Thu, 20 Feb 2020 23:51:35 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Thu, 20 Feb 2020 23:51:36 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Thu, 20 Feb 2020 23:51:37 GMT
ENV ADMINER_VERSION=4.7.6
# Thu, 20 Feb 2020 23:51:38 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Thu, 20 Feb 2020 23:51:39 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Thu, 20 Feb 2020 23:51:42 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Thu, 20 Feb 2020 23:51:43 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 20 Feb 2020 23:51:44 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Thu, 20 Feb 2020 23:51:45 GMT
USER adminer
# Thu, 20 Feb 2020 23:51:46 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 20 Feb 2020 23:51:47 GMT
EXPOSE 8080
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
	-	`sha256:6c492689366599e65cb0add947004a2dba1350bb15c7e6d5cf0926aba55ce6ec`  
		Last Modified: Thu, 20 Feb 2020 23:26:18 GMT  
		Size: 10.3 MB (10280256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e5617623e9ad0a01e633e336a37f6ff4d4a71c6cb1277692357d52303452d2f`  
		Last Modified: Thu, 20 Feb 2020 23:26:17 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4302d0c4f38943fda60770816f7eba1edb1d2f6a0c6f489e97ba67d9bdad574`  
		Last Modified: Thu, 20 Feb 2020 23:26:22 GMT  
		Size: 12.8 MB (12751449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc244875b6924b539df26879b4496e91b8eee4f5000e1ea5b774d83b9546b93`  
		Last Modified: Thu, 20 Feb 2020 23:26:18 GMT  
		Size: 2.2 KB (2214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04543010f9cd746143ced265c7b4b63d09ddc611588a131cbafe2099993fb5eb`  
		Last Modified: Thu, 20 Feb 2020 23:26:17 GMT  
		Size: 72.7 KB (72683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccb0170041c03fedc1121c07c7a06ee726f8a727c7c1eb5af04d1ee8f5654d5`  
		Last Modified: Thu, 20 Feb 2020 23:53:18 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1581d0fa71215a6ef8bb771f93fa001d361b8a02c3976b035408c6846e18be`  
		Last Modified: Thu, 20 Feb 2020 23:53:18 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f10e2f522b5d5b3116470d1761f55ab3feeb58372a087e3f6e80ea4f8f9dce7`  
		Last Modified: Thu, 20 Feb 2020 23:53:16 GMT  
		Size: 1.1 MB (1124902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c7b2368289baa2b3bc92adf31146c857cd78eecc8908bc78513c4f768c50323`  
		Last Modified: Thu, 20 Feb 2020 23:53:16 GMT  
		Size: 115.0 KB (114953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:765ac7cdcb3c5567be3929620bd1b2714a2af370ad604183f149ad40b19fd29c`  
		Last Modified: Thu, 20 Feb 2020 23:53:16 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45fe2c562cb0866875f0499d9583698863ee29b34a5a94406a42202b70885f6f`  
		Last Modified: Thu, 20 Feb 2020 23:53:16 GMT  
		Size: 570.8 KB (570772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e31dee670440ee2efcb54b84d9b9acccc709250fcb875c7ab9f31b21aded9fc`  
		Last Modified: Thu, 20 Feb 2020 23:53:16 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7-standalone` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:d6ac77d178d83433a94f4c1ac85d37eb6bde9a3b5e2ddd70510ab8366580d72d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 MB (30795142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59720519dbc2aaa04f42da6be01d883724212b4503025e14148efe901e90b553`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Sat, 18 Jan 2020 02:29:26 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 02:29:26 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 02:29:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 02:29:29 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 24 Jan 2020 00:09:58 GMT
ENV PHP_VERSION=7.4.2
# Fri, 24 Jan 2020 00:10:02 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.2.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.2.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 00:10:03 GMT
ENV PHP_SHA256=98284deac017da0d426117ecae7599a1f1bf62ae3911e8bc16c4403a8f4bdf13 PHP_MD5=
# Fri, 24 Jan 2020 00:10:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 24 Jan 2020 00:10:10 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 00:14:01 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 00:14:05 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Fri, 24 Jan 2020 00:14:09 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 00:14:10 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 00:14:11 GMT
CMD ["php" "-a"]
# Fri, 24 Jan 2020 02:50:27 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 24 Jan 2020 02:50:28 GMT
STOPSIGNAL SIGINT
# Fri, 24 Jan 2020 02:50:32 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 24 Jan 2020 02:50:32 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 02:50:36 GMT
RUN apk add --no-cache libpq
# Fri, 24 Jan 2020 02:51:09 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Fri, 24 Jan 2020 02:51:10 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 31 Jan 2020 17:39:37 GMT
ENV ADMINER_VERSION=4.7.6
# Fri, 31 Jan 2020 17:39:37 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Fri, 31 Jan 2020 17:39:38 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Fri, 31 Jan 2020 17:39:40 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 31 Jan 2020 17:39:41 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 31 Jan 2020 17:39:42 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 31 Jan 2020 17:39:42 GMT
USER adminer
# Fri, 31 Jan 2020 17:39:43 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 31 Jan 2020 17:39:44 GMT
EXPOSE 8080
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
	-	`sha256:aa724be546925194dbbb305717c1ec1404bd825d4e768f5fa30758fc836a1dda`  
		Last Modified: Fri, 24 Jan 2020 02:37:49 GMT  
		Size: 10.3 MB (10271109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b0bc8c61926931859ef4bf710fb73b709a407ca1086dfe704e7654934b4bdd`  
		Last Modified: Fri, 24 Jan 2020 02:37:45 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07be412705d63c11275e2018adae846b8861d4f678a21f2c43e2c22ae0bcee6d`  
		Last Modified: Fri, 24 Jan 2020 02:37:49 GMT  
		Size: 14.4 MB (14366228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73cafd3dde7ad30752409223dc0b26b0a5f4fa98d9a875225e2566bd99806655`  
		Last Modified: Fri, 24 Jan 2020 02:37:45 GMT  
		Size: 2.2 KB (2216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59195632759b7e9a57fb9ac253284ecbea9055d01c12f9caa49d23ca8f40bc1c`  
		Last Modified: Fri, 24 Jan 2020 02:37:45 GMT  
		Size: 72.7 KB (72676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6576a2f957338815a3fd8d1023a31cbb8ef8592406942ab75483b02adbe1c384`  
		Last Modified: Fri, 24 Jan 2020 02:52:47 GMT  
		Size: 310.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f6446e74a0df8b21f4f9ad86cf10fa3f6b6a9231d643d4174a5ddd3cf84f184`  
		Last Modified: Fri, 24 Jan 2020 02:52:47 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b69655ccf3f62cf1149958c93543bc91f9addef901545f4c74831b5c65b29039`  
		Last Modified: Fri, 24 Jan 2020 02:52:44 GMT  
		Size: 1.3 MB (1299236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:986406fbe9d0af0aeacc6c7cc032415d7552b4fd8f3fe60ea2313caa9193649c`  
		Last Modified: Fri, 24 Jan 2020 02:52:44 GMT  
		Size: 124.7 KB (124696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:382b47ced56d800090d03dff8f4d1183a7209bfd39013db12812d2efc2a39f54`  
		Last Modified: Fri, 24 Jan 2020 02:52:44 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23f30f175d57f1ffdc2f5c4308d886c2f842ce1a163c77b1747b628a89684ac`  
		Last Modified: Fri, 31 Jan 2020 17:40:10 GMT  
		Size: 570.8 KB (570779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d5044dac86a165d99ffacf0aaeb789461f31935ef0847d4e80ae612f101599`  
		Last Modified: Fri, 31 Jan 2020 17:40:10 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7-standalone` - linux; 386

```console
$ docker pull adminer@sha256:d094fa6fd940847cd20c8dd698284d004cf1d6a5fa23d777f0b19667afa76346
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31684075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed77c13afb1993912752a1a0383da2185144a458fde112b713496146d193cb19`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Sat, 18 Jan 2020 05:41:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 05:41:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 05:41:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 05:41:39 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 23 Jan 2020 23:13:49 GMT
ENV PHP_VERSION=7.4.2
# Thu, 23 Jan 2020 23:13:49 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.2.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.2.tar.xz.asc/from/this/mirror
# Thu, 23 Jan 2020 23:13:49 GMT
ENV PHP_SHA256=98284deac017da0d426117ecae7599a1f1bf62ae3911e8bc16c4403a8f4bdf13 PHP_MD5=
# Thu, 23 Jan 2020 23:13:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 23 Jan 2020 23:13:52 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Jan 2020 23:21:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 23 Jan 2020 23:21:57 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 23 Jan 2020 23:21:59 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Jan 2020 23:21:59 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Jan 2020 23:22:00 GMT
CMD ["php" "-a"]
# Fri, 24 Jan 2020 07:25:41 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 24 Jan 2020 07:25:41 GMT
STOPSIGNAL SIGINT
# Fri, 24 Jan 2020 07:25:42 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 24 Jan 2020 07:25:42 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 07:25:43 GMT
RUN apk add --no-cache libpq
# Fri, 24 Jan 2020 07:26:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Fri, 24 Jan 2020 07:26:02 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 31 Jan 2020 17:38:17 GMT
ENV ADMINER_VERSION=4.7.6
# Fri, 31 Jan 2020 17:38:18 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Fri, 31 Jan 2020 17:38:18 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Fri, 31 Jan 2020 17:38:19 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 31 Jan 2020 17:38:19 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 31 Jan 2020 17:38:20 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 31 Jan 2020 17:38:20 GMT
USER adminer
# Fri, 31 Jan 2020 17:38:20 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 31 Jan 2020 17:38:20 GMT
EXPOSE 8080
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
	-	`sha256:9f3628b223c4b093cf7c2d7723ccd39dfcb6977a659c9c183e7673f22f44865b`  
		Last Modified: Fri, 24 Jan 2020 02:36:11 GMT  
		Size: 10.3 MB (10271099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e167c61f346105deafdbe6bff7f521715a3d31cd4c9ca27d6dca67654d916c`  
		Last Modified: Fri, 24 Jan 2020 02:36:08 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53425617927914b1561c930b3ce2f90644de41394e731ca71a5d66feeba55d5b`  
		Last Modified: Fri, 24 Jan 2020 02:36:19 GMT  
		Size: 15.0 MB (14974599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809347a8b4ae69caee1b666ac61ec86e0f2dd5d64744592a59f65fd9bb49c7c9`  
		Last Modified: Fri, 24 Jan 2020 02:36:10 GMT  
		Size: 2.2 KB (2216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31917077d16c99b9c58e44f9267cbda55763d759a59379d7e4ca1f9fd6acf60a`  
		Last Modified: Fri, 24 Jan 2020 02:36:09 GMT  
		Size: 72.3 KB (72331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc6ba5ae7aae77ac94c185eef225136d01333d8840f8896b412e359fa89e3ae6`  
		Last Modified: Fri, 24 Jan 2020 07:27:19 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aab9a7fed181e4a8d1621cf6e92e6b4525a242e1c102cac7a259b3336202c16`  
		Last Modified: Fri, 24 Jan 2020 07:27:19 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1120969ea66ac41447ffffddcda8e8d389a0a1c0c7feb7d9d650117b973459d`  
		Last Modified: Fri, 24 Jan 2020 07:27:18 GMT  
		Size: 1.4 MB (1397662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cf37d29a0120ccd9ef7f4f99c6d10673cd93097ebe961c86faf275c144f5929`  
		Last Modified: Fri, 24 Jan 2020 07:27:18 GMT  
		Size: 130.8 KB (130760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf17f4f8d6baa9c93722150405686cf214bc377adbb7ff2b891efe5ca38809c9`  
		Last Modified: Fri, 24 Jan 2020 07:27:18 GMT  
		Size: 1.5 KB (1472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cac8221b3739531c0e54a60c4d8d795c187ce863f2fb79955540c1b62347fbc7`  
		Last Modified: Fri, 31 Jan 2020 17:38:36 GMT  
		Size: 570.7 KB (570691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8127a70cc3e20105c94ab16913cab965e775aaa7cb37cc6398e47d4a1830241e`  
		Last Modified: Fri, 31 Jan 2020 17:38:36 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7-standalone` - linux; ppc64le

```console
$ docker pull adminer@sha256:8906a11939b6681a5c547d8a1b3d8e58493fb85a66ef14177592239c9cd3ab6f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32169343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:251a9f8c0d32635a09c63fc8d5e5fbad2fee09cca0a4ea7cca903b5d9ac6f815`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Sat, 18 Jan 2020 03:24:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:24:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:24:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 03:24:34 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 23 Jan 2020 23:32:44 GMT
ENV PHP_VERSION=7.4.2
# Thu, 23 Jan 2020 23:32:47 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.2.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.2.tar.xz.asc/from/this/mirror
# Thu, 23 Jan 2020 23:32:50 GMT
ENV PHP_SHA256=98284deac017da0d426117ecae7599a1f1bf62ae3911e8bc16c4403a8f4bdf13 PHP_MD5=
# Thu, 23 Jan 2020 23:33:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 23 Jan 2020 23:33:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Jan 2020 23:36:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 23 Jan 2020 23:36:54 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 23 Jan 2020 23:37:00 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Jan 2020 23:37:02 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Jan 2020 23:37:04 GMT
CMD ["php" "-a"]
# Fri, 24 Jan 2020 05:51:10 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 24 Jan 2020 05:51:12 GMT
STOPSIGNAL SIGINT
# Fri, 24 Jan 2020 05:51:17 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 24 Jan 2020 05:51:19 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 05:51:23 GMT
RUN apk add --no-cache libpq
# Fri, 24 Jan 2020 05:51:48 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Fri, 24 Jan 2020 05:51:50 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 31 Jan 2020 17:16:45 GMT
ENV ADMINER_VERSION=4.7.6
# Fri, 31 Jan 2020 17:16:48 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Fri, 31 Jan 2020 17:16:51 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Fri, 31 Jan 2020 17:17:00 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 31 Jan 2020 17:17:01 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 31 Jan 2020 17:17:03 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 31 Jan 2020 17:17:05 GMT
USER adminer
# Fri, 31 Jan 2020 17:17:08 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 31 Jan 2020 17:17:10 GMT
EXPOSE 8080
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
	-	`sha256:c24c1e693453ad6efa656fcfa28e76c0786f80b4467d83c277d1116117942973`  
		Last Modified: Fri, 24 Jan 2020 02:32:44 GMT  
		Size: 10.3 MB (10271124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb71fc05f0fe0d365d8b9891f304e0cf2c1f6f0d2200ecdc0ea9a1c569117a1d`  
		Last Modified: Fri, 24 Jan 2020 02:32:41 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf26116548345ee1f676a6c1fabb768cd60750eb7a3a0ac7f09724350dde3b1`  
		Last Modified: Fri, 24 Jan 2020 02:32:54 GMT  
		Size: 15.5 MB (15539990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc4f870d6f2e6bbade33c0f28534b50765c4b56a093dc7565bd3ec3b37a7c603`  
		Last Modified: Fri, 24 Jan 2020 02:32:41 GMT  
		Size: 2.2 KB (2211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6a738ee51d709e4c4db983f9206a240500a2fc0dbaf3c76f6da2f99e5f6eb3b`  
		Last Modified: Fri, 24 Jan 2020 02:32:41 GMT  
		Size: 73.0 KB (72992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47bf1b73f7bf1089b7cf019ae582b63d77fa46e6c5b2b4efc16b0bf9d9b1ad9a`  
		Last Modified: Fri, 24 Jan 2020 05:53:47 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f984dcaccfb46a5cafd49380217e97342575055ceaaab4ff65a67f43af2da028`  
		Last Modified: Fri, 24 Jan 2020 05:53:47 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9e4520026a60556f0b631a13532b9a39d91d8eae94d4d3514359ef189ce4c94`  
		Last Modified: Fri, 24 Jan 2020 05:53:45 GMT  
		Size: 1.4 MB (1350626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba57cd117c3f571c3379a3fbb16d112291f4de925499dfeaad0bc7966c9483fb`  
		Last Modified: Fri, 24 Jan 2020 05:53:44 GMT  
		Size: 135.9 KB (135919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faef1730db86976915b65b75f76c1a057c321a983034e019f37ec833f5a1ffc9`  
		Last Modified: Fri, 24 Jan 2020 05:53:44 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:620c9c1b5881ba0a3be097e7cb57c695406737868e7b1adc02c5561c5f7b1649`  
		Last Modified: Fri, 31 Jan 2020 17:18:05 GMT  
		Size: 570.8 KB (570776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03e77753eec72902172405ef4c8c0c667bf7377cd0dc6cc1441afd0890991d43`  
		Last Modified: Fri, 31 Jan 2020 17:18:04 GMT  
		Size: 501.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:4-fastcgi`

```console
$ docker pull adminer@sha256:85ef53ce6942c89cdacf05991c16132da81d158741e42e2eef13b3c4111ba801
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `adminer:4-fastcgi` - linux; amd64

```console
$ docker pull adminer@sha256:3261472ab50e9daaf45a30818ad65311dc175417adf46363ecf18c7fb79f4048
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31132621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f894c56f8bea377d752a7839e5b2af6ffeab97af51d7b9b54e8c3113a954b088`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
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
# Sat, 18 Jan 2020 03:23:44 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 24 Jan 2020 07:13:33 GMT
ENV PHP_VERSION=7.4.2
# Fri, 24 Jan 2020 07:13:33 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.2.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.2.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 07:13:34 GMT
ENV PHP_SHA256=98284deac017da0d426117ecae7599a1f1bf62ae3911e8bc16c4403a8f4bdf13 PHP_MD5=
# Fri, 24 Jan 2020 07:13:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 24 Jan 2020 07:13:36 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 07:19:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 07:19:23 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Fri, 24 Jan 2020 07:19:24 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 07:19:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 07:19:24 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 07:19:25 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 24 Jan 2020 07:19:25 GMT
STOPSIGNAL SIGQUIT
# Fri, 24 Jan 2020 07:19:25 GMT
EXPOSE 9000
# Fri, 24 Jan 2020 07:19:25 GMT
CMD ["php-fpm"]
# Fri, 24 Jan 2020 10:52:50 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 24 Jan 2020 10:52:51 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 24 Jan 2020 10:52:52 GMT
RUN apk add --no-cache libpq
# Fri, 24 Jan 2020 10:53:11 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Fri, 24 Jan 2020 10:53:11 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 31 Jan 2020 17:19:33 GMT
ENV ADMINER_VERSION=4.7.6
# Fri, 31 Jan 2020 17:19:33 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Fri, 31 Jan 2020 17:19:33 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Fri, 31 Jan 2020 17:19:34 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 31 Jan 2020 17:19:34 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 31 Jan 2020 17:19:35 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 31 Jan 2020 17:19:35 GMT
USER adminer
# Fri, 31 Jan 2020 17:19:35 GMT
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
	-	`sha256:6e71cca12e10fbf7814b66f3f30f2c626a76931eb1658b35580520657aa1c472`  
		Last Modified: Fri, 24 Jan 2020 10:39:58 GMT  
		Size: 10.3 MB (10271098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed2310d2f7910e8f29ab569006386735c80fdb8d7a9f4b50c2233347335ef47e`  
		Last Modified: Fri, 24 Jan 2020 10:39:55 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:601ef2217a14892579aa55bfff77d380170c0c5b6bb97ba4275769e288cc008e`  
		Last Modified: Fri, 24 Jan 2020 10:40:00 GMT  
		Size: 14.6 MB (14640028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41dc18d982f54d4c5634f99e7933d9ad3069ef493b460cf998e1954caa2f24b7`  
		Last Modified: Fri, 24 Jan 2020 10:39:55 GMT  
		Size: 2.2 KB (2219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72be421f63f8c4ae023b97af91e72adcad7347edfff80e8fe6d0fea64be89f41`  
		Last Modified: Fri, 24 Jan 2020 10:39:56 GMT  
		Size: 73.1 KB (73144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f10dd871243fb2f678d5abcd0925bfc78bf759edf24b577c2aaaecce51ac30fb`  
		Last Modified: Fri, 24 Jan 2020 10:39:55 GMT  
		Size: 8.4 KB (8409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df30bf875af7c93a1a5f0231eb502f80916cc360f7bb5301af9fd174346bae03`  
		Last Modified: Fri, 24 Jan 2020 10:53:53 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb01654c81755c04f51d84470d9460f05137a60b5cb6af11a277b81ffdb12844`  
		Last Modified: Fri, 24 Jan 2020 10:53:53 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc08268651428df387dfafc653a2ce4c616f5eb02a72752692c59c871b99d37`  
		Last Modified: Fri, 24 Jan 2020 10:53:52 GMT  
		Size: 1.3 MB (1277248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ee28a212305aa260efa44f897f666e2d55a5c7b69b1eacb4913985baf64c9a`  
		Last Modified: Fri, 24 Jan 2020 10:53:52 GMT  
		Size: 126.6 KB (126627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60596dcdb9d8dba4d1f1beb1964daee86e4d999728581b4ed91e9edc6dd78a87`  
		Last Modified: Fri, 24 Jan 2020 10:53:52 GMT  
		Size: 1.5 KB (1474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30705479566e7b730c43bc045a5c98474f7fa05a827632e22deb9c00247a1792`  
		Last Modified: Fri, 31 Jan 2020 17:19:53 GMT  
		Size: 570.7 KB (570684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d656991abfa4ac7b964071b05e6a5c7e82cfb72e2de48fb119f733649768109`  
		Last Modified: Fri, 31 Jan 2020 17:19:53 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; arm variant v6

```console
$ docker pull adminer@sha256:f3ef94b81d53fa10bdf91813ec1727746da25896c82eb5418da6183ff345fe42
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.9 MB (29904916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13e34cefffcf1ef42f5bc12f108decf6d572e5812224b5f36b8008069927885c`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
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
# Sat, 18 Jan 2020 03:44:54 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 20 Feb 2020 21:54:14 GMT
ENV PHP_VERSION=7.4.3
# Thu, 20 Feb 2020 21:54:15 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.3.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.3.tar.xz.asc/from/this/mirror
# Thu, 20 Feb 2020 21:54:16 GMT
ENV PHP_SHA256=cf1f856d877c268124ded1ede40c9fb6142b125fdaafdc54f855120b8bc6982a PHP_MD5=
# Thu, 20 Feb 2020 21:54:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Feb 2020 21:54:23 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Feb 2020 21:58:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 20 Feb 2020 21:58:38 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Thu, 20 Feb 2020 21:58:41 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Feb 2020 21:58:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Feb 2020 21:58:43 GMT
WORKDIR /var/www/html
# Thu, 20 Feb 2020 21:58:45 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 20 Feb 2020 21:58:46 GMT
STOPSIGNAL SIGQUIT
# Thu, 20 Feb 2020 21:58:48 GMT
EXPOSE 9000
# Thu, 20 Feb 2020 21:58:49 GMT
CMD ["php-fpm"]
# Thu, 20 Feb 2020 23:47:03 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Thu, 20 Feb 2020 23:47:05 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 20 Feb 2020 23:47:07 GMT
RUN apk add --no-cache libpq
# Thu, 20 Feb 2020 23:47:34 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Thu, 20 Feb 2020 23:47:35 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Thu, 20 Feb 2020 23:47:35 GMT
ENV ADMINER_VERSION=4.7.6
# Thu, 20 Feb 2020 23:47:36 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Thu, 20 Feb 2020 23:47:37 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Thu, 20 Feb 2020 23:47:40 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Thu, 20 Feb 2020 23:47:41 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 20 Feb 2020 23:47:41 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Thu, 20 Feb 2020 23:47:42 GMT
USER adminer
# Thu, 20 Feb 2020 23:47:42 GMT
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
	-	`sha256:80ca3c99ad3f93290cc94e506f94e8b01e2bfe5d2901b45ad4fd1bf704e70ed7`  
		Last Modified: Thu, 20 Feb 2020 23:10:40 GMT  
		Size: 10.3 MB (10280253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f658c7e1eb0d0386247f8fa5f228f97f709e09b53982bd1ba92f38cad3803ec8`  
		Last Modified: Thu, 20 Feb 2020 23:10:36 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38dd2d597adffab2d9b483cfa2352a9413ca3868e55fccb30c7551e0c1a7cb57`  
		Last Modified: Thu, 20 Feb 2020 23:10:42 GMT  
		Size: 13.7 MB (13671450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bfdd3dff152326a8135a5747de2a94547b298afe86fe63946bb425bc30fba92`  
		Last Modified: Thu, 20 Feb 2020 23:10:36 GMT  
		Size: 2.2 KB (2213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5554b593396e1abf2813391b3b1c84e40383b0988321d2d63616a290aa7fed7d`  
		Last Modified: Thu, 20 Feb 2020 23:10:36 GMT  
		Size: 72.7 KB (72681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9159be50c0fe27b27be4abb997de85c54fd2d1308d35c5c6c97e4d118fdec6a0`  
		Last Modified: Thu, 20 Feb 2020 23:10:37 GMT  
		Size: 8.4 KB (8412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28aa812c7cc19a079c92c7f6eba0da1ecffdcf6f1fe4946898b7ec9ff1b6940a`  
		Last Modified: Thu, 20 Feb 2020 23:48:28 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a7c93eb4a00db350eb6b34997b1f9541d4851def62b039696d47ae3b25f55f8`  
		Last Modified: Thu, 20 Feb 2020 23:48:28 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:820825c9319f4e49d67cd84bb103b76d2cca8df1f674d7a84b6b5ef1f43afe3b`  
		Last Modified: Thu, 20 Feb 2020 23:48:23 GMT  
		Size: 1.2 MB (1234699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49c16bab556b699d17b5ef77dfbbc559d0fabd75d27f9eed069b3753331c0e5a`  
		Last Modified: Thu, 20 Feb 2020 23:48:23 GMT  
		Size: 120.1 KB (120098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1ec2a9c5203dcc61950a047d4f04c455f284b6062740fbc081a32c7fb5873b2`  
		Last Modified: Thu, 20 Feb 2020 23:48:23 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:295fdb00d23508c2695ae7402b772fdd479d44cd0f0a05c93b069242638a3e0f`  
		Last Modified: Thu, 20 Feb 2020 23:48:23 GMT  
		Size: 570.8 KB (570771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92b8b25d3ffd6ef7dd0976b4b19b04842ed268bfbc55452f5000ba913defa355`  
		Last Modified: Thu, 20 Feb 2020 23:48:23 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; arm variant v7

```console
$ docker pull adminer@sha256:2f5f67a712318a2a917724f95730ad156ec7427834865497016e22de6541cc5c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.6 MB (28642438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c803a31f5e4241a9cb82515d1cc260871c3f62e3c30297d71a35973096a31e2`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
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
# Sat, 18 Jan 2020 05:28:02 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 20 Feb 2020 21:14:19 GMT
ENV PHP_VERSION=7.4.3
# Thu, 20 Feb 2020 21:14:19 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.3.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.3.tar.xz.asc/from/this/mirror
# Thu, 20 Feb 2020 21:14:20 GMT
ENV PHP_SHA256=cf1f856d877c268124ded1ede40c9fb6142b125fdaafdc54f855120b8bc6982a PHP_MD5=
# Thu, 20 Feb 2020 21:14:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Feb 2020 21:14:24 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Feb 2020 21:16:45 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 20 Feb 2020 21:16:46 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Thu, 20 Feb 2020 21:16:49 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Feb 2020 21:16:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Feb 2020 21:16:50 GMT
WORKDIR /var/www/html
# Thu, 20 Feb 2020 21:16:51 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 20 Feb 2020 21:16:52 GMT
STOPSIGNAL SIGQUIT
# Thu, 20 Feb 2020 21:16:53 GMT
EXPOSE 9000
# Thu, 20 Feb 2020 21:16:54 GMT
CMD ["php-fpm"]
# Thu, 20 Feb 2020 23:52:02 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Thu, 20 Feb 2020 23:52:05 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 20 Feb 2020 23:52:08 GMT
RUN apk add --no-cache libpq
# Thu, 20 Feb 2020 23:52:41 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Thu, 20 Feb 2020 23:52:43 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Thu, 20 Feb 2020 23:52:44 GMT
ENV ADMINER_VERSION=4.7.6
# Thu, 20 Feb 2020 23:52:45 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Thu, 20 Feb 2020 23:52:46 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Thu, 20 Feb 2020 23:52:49 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Thu, 20 Feb 2020 23:52:50 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 20 Feb 2020 23:52:51 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Thu, 20 Feb 2020 23:52:52 GMT
USER adminer
# Thu, 20 Feb 2020 23:52:54 GMT
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
	-	`sha256:0b327d731622fe78b5dce5377da7c2fa2a8f7f5bccb0851084b9329f9a570063`  
		Last Modified: Thu, 20 Feb 2020 23:26:52 GMT  
		Size: 10.3 MB (10280261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4b40e24dacf2616800de7bb9e410e263de6eccf4d1bfd5a22d32908c21b2361`  
		Last Modified: Thu, 20 Feb 2020 23:26:49 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e42a50422a3ffed17517bce0eb1fe538eea06417fdc672c4711d134108d7b0b4`  
		Last Modified: Thu, 20 Feb 2020 23:26:54 GMT  
		Size: 12.8 MB (12815724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5473e54c50261b361a070da14923a840b1c2155de57aacac9a8ff18575dd6e1a`  
		Last Modified: Thu, 20 Feb 2020 23:26:50 GMT  
		Size: 2.2 KB (2216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f939d7049d7edb45231e24fec17211f863a36748747b3121cc935b6760c86632`  
		Last Modified: Thu, 20 Feb 2020 23:26:49 GMT  
		Size: 72.7 KB (72680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e26488d2c5a3fcc5e1d56a02cd6a6755d2bf8a503dfb6bff0c265cedf52a11fa`  
		Last Modified: Thu, 20 Feb 2020 23:26:49 GMT  
		Size: 8.4 KB (8409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7b9f9e7ecb2380e21319c90bc307fa28a14061bc3b629ea3cafaebe8e7865e3`  
		Last Modified: Thu, 20 Feb 2020 23:53:39 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:214861e86ee457b4f34bad18e669992ef9dff229e599e0f7f15f41b926a9ec31`  
		Last Modified: Thu, 20 Feb 2020 23:53:39 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6f9a71b7d4f646e777f739107b1911cf18f3305a0f3348c54572385f6f5d71f`  
		Last Modified: Thu, 20 Feb 2020 23:53:37 GMT  
		Size: 1.1 MB (1124908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3757929f73de69aebca78a3f042c638bb48e703b5a1ce80fc02e2eae8b45cdf`  
		Last Modified: Thu, 20 Feb 2020 23:53:37 GMT  
		Size: 115.0 KB (114950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3151fc0a4ad4389a4655e265bca8650f675575130c4394907f6abe79dc4bacf3`  
		Last Modified: Thu, 20 Feb 2020 23:53:37 GMT  
		Size: 1.5 KB (1477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85281d825070bdddb16a2bacfad1baa7633a1a1e22d32c6ad458bbac70bc1737`  
		Last Modified: Thu, 20 Feb 2020 23:53:37 GMT  
		Size: 570.8 KB (570766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499386092f7399a059f809ff852ca1239313c7555831f07909a8cc81d06f386d`  
		Last Modified: Thu, 20 Feb 2020 23:53:37 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:4f9923edd71c163c491fec06013c2c29c6c486e96f1a5a5fe9f6a15d7d0cdb08
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30872795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c607c25c09ed37fcb1262db44e11192f84fc037fe9d82ebbd207a31813123ff5`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
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
# Sat, 18 Jan 2020 02:36:11 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 24 Jan 2020 00:14:35 GMT
ENV PHP_VERSION=7.4.2
# Fri, 24 Jan 2020 00:14:36 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.2.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.2.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 00:14:38 GMT
ENV PHP_SHA256=98284deac017da0d426117ecae7599a1f1bf62ae3911e8bc16c4403a8f4bdf13 PHP_MD5=
# Fri, 24 Jan 2020 00:14:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 24 Jan 2020 00:14:45 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 00:18:29 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 00:18:32 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Fri, 24 Jan 2020 00:18:36 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 00:18:37 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 00:18:38 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 00:18:41 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 24 Jan 2020 00:18:42 GMT
STOPSIGNAL SIGQUIT
# Fri, 24 Jan 2020 00:18:44 GMT
EXPOSE 9000
# Fri, 24 Jan 2020 00:18:45 GMT
CMD ["php-fpm"]
# Fri, 24 Jan 2020 02:51:31 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 24 Jan 2020 02:51:33 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 24 Jan 2020 02:51:36 GMT
RUN apk add --no-cache libpq
# Fri, 24 Jan 2020 02:52:06 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Fri, 24 Jan 2020 02:52:07 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 31 Jan 2020 17:39:50 GMT
ENV ADMINER_VERSION=4.7.6
# Fri, 31 Jan 2020 17:39:51 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Fri, 31 Jan 2020 17:39:51 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Fri, 31 Jan 2020 17:39:54 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 31 Jan 2020 17:39:55 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 31 Jan 2020 17:39:55 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 31 Jan 2020 17:39:56 GMT
USER adminer
# Fri, 31 Jan 2020 17:39:57 GMT
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
	-	`sha256:031bf935aef9c8cf9a41b1dbd509b48db2ab230dae75e8d1f2f20c1713826cfa`  
		Last Modified: Fri, 24 Jan 2020 02:38:24 GMT  
		Size: 10.3 MB (10271108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd439e1038e9d42eab7437e8f85a4c7cd369089af8cb708e63e0c4388fdb1bf3`  
		Last Modified: Fri, 24 Jan 2020 02:38:16 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25ed1e9754e061a3e75c31e172b7e2ef4b7b5a8673a24423b2260a91000daed9`  
		Last Modified: Fri, 24 Jan 2020 02:38:20 GMT  
		Size: 14.4 MB (14435498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5801422dba8896819ba048a35c0da81a25eec8fb91c74ddc3da87bbbf13fd470`  
		Last Modified: Fri, 24 Jan 2020 02:38:16 GMT  
		Size: 2.2 KB (2217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d4f983059021c9010c5326e718d5870d3ed28a792a95b78f95399c93b6b963f`  
		Last Modified: Fri, 24 Jan 2020 02:38:16 GMT  
		Size: 72.7 KB (72672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:947d95e1f7678a8070ee18dba3cf26e07c11e7a0f1fed1885014776890783c64`  
		Last Modified: Fri, 24 Jan 2020 02:38:16 GMT  
		Size: 8.4 KB (8410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8246e4f25893c2c59d16a3a91eb0e024ee6b366eb1828d39c00069b0fe074821`  
		Last Modified: Fri, 24 Jan 2020 02:53:09 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153c72183d2af4959ab20862dab40a0a198583b2ed6460c78eb4b58afbe8099a`  
		Last Modified: Fri, 24 Jan 2020 02:53:08 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79ea398fe8d2d7940f02c220eac23b6e0b59f654452a7c2d784746f57264e66`  
		Last Modified: Fri, 24 Jan 2020 02:53:07 GMT  
		Size: 1.3 MB (1299219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a60c746308f1dc0af8f8ee2c44315d9bb1b416377a2938f63d9a70ab2d0f06ad`  
		Last Modified: Fri, 24 Jan 2020 02:53:07 GMT  
		Size: 124.7 KB (124702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca6bc7dce64e9b13729a1e1afd341a91788f4a0d94380b7cc81feec83f580bf6`  
		Last Modified: Fri, 24 Jan 2020 02:53:06 GMT  
		Size: 1.5 KB (1474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f1dac04eb03855c7c287673ef8e4c6d1c4915d3663f9376444abe8e8c3c1ed4`  
		Last Modified: Fri, 31 Jan 2020 17:40:25 GMT  
		Size: 570.8 KB (570773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44ddb8bdcd055db611ac57e0a6bc167bd231eaf893f9d7d11e3f0d13025cf98`  
		Last Modified: Fri, 31 Jan 2020 17:40:25 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; 386

```console
$ docker pull adminer@sha256:46b8bb610eaaa99932c42a3352a7bb709eddd218944284a41d4a25ab9e2593db
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31762110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e5c58ebd525deeac88b11a3c516b9d22ac70308fcd0aeb5cc2624988423c31`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
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
# Sat, 18 Jan 2020 05:48:40 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 23 Jan 2020 23:22:10 GMT
ENV PHP_VERSION=7.4.2
# Thu, 23 Jan 2020 23:22:10 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.2.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.2.tar.xz.asc/from/this/mirror
# Thu, 23 Jan 2020 23:22:11 GMT
ENV PHP_SHA256=98284deac017da0d426117ecae7599a1f1bf62ae3911e8bc16c4403a8f4bdf13 PHP_MD5=
# Thu, 23 Jan 2020 23:22:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 23 Jan 2020 23:22:16 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Jan 2020 23:31:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 23 Jan 2020 23:31:14 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Thu, 23 Jan 2020 23:31:15 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Jan 2020 23:31:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Jan 2020 23:31:15 GMT
WORKDIR /var/www/html
# Thu, 23 Jan 2020 23:31:16 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 23 Jan 2020 23:31:16 GMT
STOPSIGNAL SIGQUIT
# Thu, 23 Jan 2020 23:31:16 GMT
EXPOSE 9000
# Thu, 23 Jan 2020 23:31:17 GMT
CMD ["php-fpm"]
# Fri, 24 Jan 2020 07:26:11 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 24 Jan 2020 07:26:12 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 24 Jan 2020 07:26:14 GMT
RUN apk add --no-cache libpq
# Fri, 24 Jan 2020 07:26:45 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Fri, 24 Jan 2020 07:26:45 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 31 Jan 2020 17:38:25 GMT
ENV ADMINER_VERSION=4.7.6
# Fri, 31 Jan 2020 17:38:25 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Fri, 31 Jan 2020 17:38:25 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Fri, 31 Jan 2020 17:38:26 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 31 Jan 2020 17:38:27 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 31 Jan 2020 17:38:27 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 31 Jan 2020 17:38:27 GMT
USER adminer
# Fri, 31 Jan 2020 17:38:27 GMT
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
	-	`sha256:7af2969e346cf39dce09953165d38ac70a637f81bf36a72173d23c8209522b1e`  
		Last Modified: Fri, 24 Jan 2020 02:36:49 GMT  
		Size: 10.3 MB (10271104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dffed627d6f3eb28e87526c201e8ae30d110efc1e7ae5b48646e1f322abddefd`  
		Last Modified: Fri, 24 Jan 2020 02:36:40 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44af2512ec067db56bee629528b24bfe54ad55f8f7064b2cf59f57868950482d`  
		Last Modified: Fri, 24 Jan 2020 02:36:51 GMT  
		Size: 15.0 MB (15044190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a34e204f3d52c0be6c78857ce18184fecbd91cf297cfb30bf15df00d78b1ff71`  
		Last Modified: Fri, 24 Jan 2020 02:36:40 GMT  
		Size: 2.2 KB (2217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c9a720f2eaf0aec04eabdd4c10f331bd1eb5e91bdf806ec43279ae4d9435107`  
		Last Modified: Fri, 24 Jan 2020 02:36:41 GMT  
		Size: 72.3 KB (72332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ce027d9508f9c2ba08e68a1cbef48753b345821147a4ec4dd52ced22ca8252`  
		Last Modified: Fri, 24 Jan 2020 02:36:40 GMT  
		Size: 8.4 KB (8413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:791ceb40ab90a13fa40d9a11daa5853b0d7c1f72f7fb2580891e34049e7be6ba`  
		Last Modified: Fri, 24 Jan 2020 07:27:33 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac79a09757dcd35db84f1d12d43f5d8f11408f92ee9e095c392eda59733b801a`  
		Last Modified: Fri, 24 Jan 2020 07:27:33 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b6beb85931082255a7f9048c7f337e1972e10ce8a02c86b86797e95922ad930`  
		Last Modified: Fri, 24 Jan 2020 07:27:34 GMT  
		Size: 1.4 MB (1397661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79d5b1485f733f60d9843f7e138f1fa150e42d713df194640dcc37931ec1c191`  
		Last Modified: Fri, 24 Jan 2020 07:27:31 GMT  
		Size: 130.8 KB (130793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:553d2e165ba3dd32a4a9a44d46fa13ec6552747310640f783b34255acfd961e2`  
		Last Modified: Fri, 24 Jan 2020 07:27:31 GMT  
		Size: 1.5 KB (1472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42e41cc3dbdf2dad75063abe783a7985dc9267ee1ee9bd5751bed6f0cba09c2b`  
		Last Modified: Fri, 31 Jan 2020 17:38:46 GMT  
		Size: 570.7 KB (570683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd7e34ec5637f78a0244c66e92539e53bcc0bc77fafc96f775c60a3dbfce14ef`  
		Last Modified: Fri, 31 Jan 2020 17:38:46 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; ppc64le

```console
$ docker pull adminer@sha256:52c4be54d3cd71b8c7ef779124ae7e3796754fad9594b24584b157fe0d90ea88
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32259051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:058dcefad0447822a717afd8533b7ef7ac94f28229ce3c409df8c013633ad069`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
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
# Sat, 18 Jan 2020 03:29:20 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 23 Jan 2020 23:37:14 GMT
ENV PHP_VERSION=7.4.2
# Thu, 23 Jan 2020 23:37:17 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.2.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.2.tar.xz.asc/from/this/mirror
# Thu, 23 Jan 2020 23:37:18 GMT
ENV PHP_SHA256=98284deac017da0d426117ecae7599a1f1bf62ae3911e8bc16c4403a8f4bdf13 PHP_MD5=
# Thu, 23 Jan 2020 23:37:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 23 Jan 2020 23:37:30 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Jan 2020 23:41:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 23 Jan 2020 23:41:16 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Thu, 23 Jan 2020 23:41:21 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Jan 2020 23:41:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Jan 2020 23:41:25 GMT
WORKDIR /var/www/html
# Thu, 23 Jan 2020 23:41:31 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 23 Jan 2020 23:41:34 GMT
STOPSIGNAL SIGQUIT
# Thu, 23 Jan 2020 23:41:36 GMT
EXPOSE 9000
# Thu, 23 Jan 2020 23:41:37 GMT
CMD ["php-fpm"]
# Fri, 24 Jan 2020 05:52:24 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 24 Jan 2020 05:52:29 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 24 Jan 2020 05:52:35 GMT
RUN apk add --no-cache libpq
# Fri, 24 Jan 2020 05:53:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Fri, 24 Jan 2020 05:53:04 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 31 Jan 2020 17:17:22 GMT
ENV ADMINER_VERSION=4.7.6
# Fri, 31 Jan 2020 17:17:23 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Fri, 31 Jan 2020 17:17:24 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Fri, 31 Jan 2020 17:17:33 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 31 Jan 2020 17:17:35 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 31 Jan 2020 17:17:39 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 31 Jan 2020 17:17:42 GMT
USER adminer
# Fri, 31 Jan 2020 17:17:44 GMT
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
	-	`sha256:71750c6fa0607bea7a09ff35d6a1406245a40b8230624a3639b89d18db4394fe`  
		Last Modified: Fri, 24 Jan 2020 02:33:52 GMT  
		Size: 10.3 MB (10271124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9edfe3521268768bb7368d494a54a58f6ea37444d81365db80594ba5cf6723e`  
		Last Modified: Fri, 24 Jan 2020 02:33:41 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03d6040910816a926d5c549b0b705387c888406057cdb66956db3c32125ac16`  
		Last Modified: Fri, 24 Jan 2020 02:33:50 GMT  
		Size: 15.6 MB (15621302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60eae056a292b760c3cccf048be586d181427ad78105d2293c95ba02dbaf0ba1`  
		Last Modified: Fri, 24 Jan 2020 02:33:41 GMT  
		Size: 2.2 KB (2215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:728ffb10bff4c1ede1c201f677ecc8c6ad6fcaa32489ca45d7dc1ffb57804d89`  
		Last Modified: Fri, 24 Jan 2020 02:33:41 GMT  
		Size: 73.0 KB (72996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:348111edcf048b6a351ad6caed9d560f0dad7e6bbe2b76922a0648db42f74bcc`  
		Last Modified: Fri, 24 Jan 2020 02:33:42 GMT  
		Size: 8.4 KB (8409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b18f3572f56ef640587e5e01d586e9ac24e3c39688ad60eb7e2542c28330ef15`  
		Last Modified: Fri, 24 Jan 2020 05:54:24 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25b30d4afe834c4c6add7f1325d981a4767fe2d659474a4bcf07fe0982d30779`  
		Last Modified: Fri, 24 Jan 2020 05:54:23 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd12c1dc772a4360a1f25b4d61773bf85a5ce8636a383a26214f52199698c03a`  
		Last Modified: Fri, 24 Jan 2020 05:54:23 GMT  
		Size: 1.4 MB (1350625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc0b0a44d83a34b0167638ba083ff0f468a535b3a75087a1810e07394e5c6e8e`  
		Last Modified: Fri, 24 Jan 2020 05:54:20 GMT  
		Size: 135.9 KB (135904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1114f35e53ffc221921a3954ec43719e7f1e8adcc07c6b0f7b75364065ed97d7`  
		Last Modified: Fri, 24 Jan 2020 05:54:20 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:609b9a3cccb86ade52bbc4fb6a19223fa44f14509e75e7c2e4438278ef3a37b6`  
		Last Modified: Fri, 31 Jan 2020 17:18:36 GMT  
		Size: 570.8 KB (570772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b5ca04b772bc2f523594fd55735ad7e753da72ecf87478b23db102df001437`  
		Last Modified: Fri, 31 Jan 2020 17:18:36 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:4-standalone`

```console
$ docker pull adminer@sha256:c689401f4ee85e37ba2cd62d401af2d569833dd8efa2c338177889fa9c525882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `adminer:4-standalone` - linux; amd64

```console
$ docker pull adminer@sha256:6ceb642133ac56e267c50ae4bfb24ac0008b0eb02b772abae9059caa45211bee
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31058191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:259cc60bdb72538cffc06536d8bb73c3d9afd7156afc71b0c97fb1659917805e`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Sat, 18 Jan 2020 03:18:30 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:18:30 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:18:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 03:18:30 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 24 Jan 2020 07:05:12 GMT
ENV PHP_VERSION=7.4.2
# Fri, 24 Jan 2020 07:05:13 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.2.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.2.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 07:05:13 GMT
ENV PHP_SHA256=98284deac017da0d426117ecae7599a1f1bf62ae3911e8bc16c4403a8f4bdf13 PHP_MD5=
# Fri, 24 Jan 2020 07:05:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 24 Jan 2020 07:05:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 07:13:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 07:13:16 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Fri, 24 Jan 2020 07:13:17 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 07:13:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 07:13:17 GMT
CMD ["php" "-a"]
# Fri, 24 Jan 2020 10:52:17 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 24 Jan 2020 10:52:17 GMT
STOPSIGNAL SIGINT
# Fri, 24 Jan 2020 10:52:18 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 24 Jan 2020 10:52:18 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 10:52:19 GMT
RUN apk add --no-cache libpq
# Fri, 24 Jan 2020 10:52:38 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Fri, 24 Jan 2020 10:52:39 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 31 Jan 2020 17:19:26 GMT
ENV ADMINER_VERSION=4.7.6
# Fri, 31 Jan 2020 17:19:26 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Fri, 31 Jan 2020 17:19:26 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Fri, 31 Jan 2020 17:19:27 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 31 Jan 2020 17:19:28 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 31 Jan 2020 17:19:28 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 31 Jan 2020 17:19:28 GMT
USER adminer
# Fri, 31 Jan 2020 17:19:28 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 31 Jan 2020 17:19:28 GMT
EXPOSE 8080
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
	-	`sha256:5fa47f19b1e835f47f4c1273ccb215a42ee2aefafe300409d92b05b899a757d8`  
		Last Modified: Fri, 24 Jan 2020 10:39:33 GMT  
		Size: 10.3 MB (10271096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4556adb19ddcb43be3cd12b973f718e5edc74d6986ae4406a0c3011cbeb3dc93`  
		Last Modified: Fri, 24 Jan 2020 10:39:33 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:205de55b7ed0d389ac2c9777321f11ba9377a148002c2ef1d7b68d02a96472f3`  
		Last Modified: Fri, 24 Jan 2020 10:39:42 GMT  
		Size: 14.6 MB (14574023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c35aa7da966a732561c37c8b5d56949eedcb7865066b86da95c8bc58c18c48d2`  
		Last Modified: Fri, 24 Jan 2020 10:39:32 GMT  
		Size: 2.2 KB (2216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82a54ca6f814c156199e3266c4297efe2f54fb83bfb1645f53582eae3d1e222e`  
		Last Modified: Fri, 24 Jan 2020 10:39:33 GMT  
		Size: 73.1 KB (73145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e28f69f8cf7d397d8bd78cab68b9713275989e440016ec98580b94d0b0dc23f8`  
		Last Modified: Fri, 24 Jan 2020 10:53:42 GMT  
		Size: 306.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b527d0b89c2ea24dd10be7c18c1dcdf592fd4e1a5ff2c9da47fba2940fbb25a7`  
		Last Modified: Fri, 24 Jan 2020 10:53:42 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35b881820e3f1402cd2b2836dc6064db1b8ef029479448d5a058baa86b0f2e29`  
		Last Modified: Fri, 24 Jan 2020 10:53:41 GMT  
		Size: 1.3 MB (1277246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97e920225fdf7c9fc6bd8762ee3efbc9225341331c21812757347e46b22a2db3`  
		Last Modified: Fri, 24 Jan 2020 10:53:41 GMT  
		Size: 126.6 KB (126617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c8cde070aec4f16d202102cbdad6a161e48b4ffae4426da85717e9ee116fbec`  
		Last Modified: Fri, 24 Jan 2020 10:53:40 GMT  
		Size: 1.5 KB (1474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:028d5feebf26f852c8d09343a1b1ea1be953837a2f402743e1c021ea7b15ccee`  
		Last Modified: Fri, 31 Jan 2020 17:19:44 GMT  
		Size: 570.7 KB (570688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e0b9ec991cbee8b6377946c76367fcaa9782c4be8d265be834c5158b2638d40`  
		Last Modified: Fri, 31 Jan 2020 17:19:44 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; arm variant v6

```console
$ docker pull adminer@sha256:086342d4149c1554e7c334711e0c6ccfa783ce0991cdd33d1687ca56e83020c7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.8 MB (29825140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08598589c478e6d488e3d5892d914c3ccac2ca333bf32b79046b127a04438a92`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Sat, 18 Jan 2020 03:40:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:40:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:40:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 03:40:19 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 20 Feb 2020 21:49:41 GMT
ENV PHP_VERSION=7.4.3
# Thu, 20 Feb 2020 21:49:43 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.3.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.3.tar.xz.asc/from/this/mirror
# Thu, 20 Feb 2020 21:49:44 GMT
ENV PHP_SHA256=cf1f856d877c268124ded1ede40c9fb6142b125fdaafdc54f855120b8bc6982a PHP_MD5=
# Thu, 20 Feb 2020 21:49:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Feb 2020 21:49:57 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Feb 2020 21:53:47 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 20 Feb 2020 21:53:50 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 20 Feb 2020 21:53:53 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Feb 2020 21:53:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Feb 2020 21:53:54 GMT
CMD ["php" "-a"]
# Thu, 20 Feb 2020 23:45:59 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Thu, 20 Feb 2020 23:45:59 GMT
STOPSIGNAL SIGINT
# Thu, 20 Feb 2020 23:46:02 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 20 Feb 2020 23:46:03 GMT
WORKDIR /var/www/html
# Thu, 20 Feb 2020 23:46:05 GMT
RUN apk add --no-cache libpq
# Thu, 20 Feb 2020 23:46:36 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Thu, 20 Feb 2020 23:46:39 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Thu, 20 Feb 2020 23:46:41 GMT
ENV ADMINER_VERSION=4.7.6
# Thu, 20 Feb 2020 23:46:41 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Thu, 20 Feb 2020 23:46:42 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Thu, 20 Feb 2020 23:46:45 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Thu, 20 Feb 2020 23:46:46 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 20 Feb 2020 23:46:46 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Thu, 20 Feb 2020 23:46:47 GMT
USER adminer
# Thu, 20 Feb 2020 23:46:48 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 20 Feb 2020 23:46:48 GMT
EXPOSE 8080
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
	-	`sha256:f246fe8b62d43a3f633a04898577258a2ce5dd84edf5fd464403b9a108b301e2`  
		Last Modified: Thu, 20 Feb 2020 23:10:06 GMT  
		Size: 10.3 MB (10280264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b4e0af10768397859f6f19eca4b17ee9f21d61a1cb06989aba861267cf1b6a`  
		Last Modified: Thu, 20 Feb 2020 23:10:05 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a228bdc8e070add11170637553b04b0eeab55a8af3159561b2878b3bcc00bbb`  
		Last Modified: Thu, 20 Feb 2020 23:10:11 GMT  
		Size: 13.6 MB (13600067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:936640ed543c6bb114e0374d4aa5d00b0ad989151337d4edfe6047bad672c605`  
		Last Modified: Thu, 20 Feb 2020 23:10:05 GMT  
		Size: 2.2 KB (2214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071eed09e44daa0c7c7d337a517208fa4a3c08e02029c0970082688456496bec`  
		Last Modified: Thu, 20 Feb 2020 23:10:05 GMT  
		Size: 72.7 KB (72679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:500b89ded2f6c4841beacd80fbbc9393d964cc71bd39c391faf7dc97822dbdb9`  
		Last Modified: Thu, 20 Feb 2020 23:47:57 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512f9b08d8b23f60cb6dff75b2270418b1aef35536dd655abbebc984b88a251b`  
		Last Modified: Thu, 20 Feb 2020 23:47:58 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c471a8e9c45607043e4014b7f0974b76407454a97e750d9055d0aa5e834e6739`  
		Last Modified: Thu, 20 Feb 2020 23:47:56 GMT  
		Size: 1.2 MB (1234698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7b673bbf243a89365a23ad683cd4498bf6d1d0ed02684c8a18d0a21cb8d178`  
		Last Modified: Thu, 20 Feb 2020 23:47:55 GMT  
		Size: 120.1 KB (120109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c24ab3064784c4410d659ea6e1f0df253d4425d982dc6458c3a3ba583e9b8ec5`  
		Last Modified: Thu, 20 Feb 2020 23:47:56 GMT  
		Size: 1.5 KB (1470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f98dd355d60f4139fe6bc5acd57c5dddf79d2130ae3198cc94d132632d3727`  
		Last Modified: Thu, 20 Feb 2020 23:47:56 GMT  
		Size: 570.8 KB (570766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9027f8cb6506a233c5d6eee529c13558fd054e963701cb92c8151588f40361cb`  
		Last Modified: Thu, 20 Feb 2020 23:47:55 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; arm variant v7

```console
$ docker pull adminer@sha256:46b5ed40565812c4e0553a75ca1a4b5bffb897b489e88cb69626a97bb5de6a91
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.6 MB (28569758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f180ec2391291be9bea6f1f484659a40aa29806d769cebcb326e9b3da944208`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Sat, 18 Jan 2020 05:22:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 05:22:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 05:22:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 05:22:49 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 20 Feb 2020 21:11:31 GMT
ENV PHP_VERSION=7.4.3
# Thu, 20 Feb 2020 21:11:32 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.3.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.3.tar.xz.asc/from/this/mirror
# Thu, 20 Feb 2020 21:11:32 GMT
ENV PHP_SHA256=cf1f856d877c268124ded1ede40c9fb6142b125fdaafdc54f855120b8bc6982a PHP_MD5=
# Thu, 20 Feb 2020 21:11:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Feb 2020 21:11:37 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Feb 2020 21:13:57 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 20 Feb 2020 21:13:59 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 20 Feb 2020 21:14:01 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Feb 2020 21:14:02 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Feb 2020 21:14:02 GMT
CMD ["php" "-a"]
# Thu, 20 Feb 2020 23:50:58 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Thu, 20 Feb 2020 23:50:58 GMT
STOPSIGNAL SIGINT
# Thu, 20 Feb 2020 23:51:00 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 20 Feb 2020 23:51:02 GMT
WORKDIR /var/www/html
# Thu, 20 Feb 2020 23:51:04 GMT
RUN apk add --no-cache libpq
# Thu, 20 Feb 2020 23:51:35 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Thu, 20 Feb 2020 23:51:36 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Thu, 20 Feb 2020 23:51:37 GMT
ENV ADMINER_VERSION=4.7.6
# Thu, 20 Feb 2020 23:51:38 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Thu, 20 Feb 2020 23:51:39 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Thu, 20 Feb 2020 23:51:42 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Thu, 20 Feb 2020 23:51:43 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 20 Feb 2020 23:51:44 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Thu, 20 Feb 2020 23:51:45 GMT
USER adminer
# Thu, 20 Feb 2020 23:51:46 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 20 Feb 2020 23:51:47 GMT
EXPOSE 8080
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
	-	`sha256:6c492689366599e65cb0add947004a2dba1350bb15c7e6d5cf0926aba55ce6ec`  
		Last Modified: Thu, 20 Feb 2020 23:26:18 GMT  
		Size: 10.3 MB (10280256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e5617623e9ad0a01e633e336a37f6ff4d4a71c6cb1277692357d52303452d2f`  
		Last Modified: Thu, 20 Feb 2020 23:26:17 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4302d0c4f38943fda60770816f7eba1edb1d2f6a0c6f489e97ba67d9bdad574`  
		Last Modified: Thu, 20 Feb 2020 23:26:22 GMT  
		Size: 12.8 MB (12751449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc244875b6924b539df26879b4496e91b8eee4f5000e1ea5b774d83b9546b93`  
		Last Modified: Thu, 20 Feb 2020 23:26:18 GMT  
		Size: 2.2 KB (2214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04543010f9cd746143ced265c7b4b63d09ddc611588a131cbafe2099993fb5eb`  
		Last Modified: Thu, 20 Feb 2020 23:26:17 GMT  
		Size: 72.7 KB (72683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccb0170041c03fedc1121c07c7a06ee726f8a727c7c1eb5af04d1ee8f5654d5`  
		Last Modified: Thu, 20 Feb 2020 23:53:18 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1581d0fa71215a6ef8bb771f93fa001d361b8a02c3976b035408c6846e18be`  
		Last Modified: Thu, 20 Feb 2020 23:53:18 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f10e2f522b5d5b3116470d1761f55ab3feeb58372a087e3f6e80ea4f8f9dce7`  
		Last Modified: Thu, 20 Feb 2020 23:53:16 GMT  
		Size: 1.1 MB (1124902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c7b2368289baa2b3bc92adf31146c857cd78eecc8908bc78513c4f768c50323`  
		Last Modified: Thu, 20 Feb 2020 23:53:16 GMT  
		Size: 115.0 KB (114953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:765ac7cdcb3c5567be3929620bd1b2714a2af370ad604183f149ad40b19fd29c`  
		Last Modified: Thu, 20 Feb 2020 23:53:16 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45fe2c562cb0866875f0499d9583698863ee29b34a5a94406a42202b70885f6f`  
		Last Modified: Thu, 20 Feb 2020 23:53:16 GMT  
		Size: 570.8 KB (570772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e31dee670440ee2efcb54b84d9b9acccc709250fcb875c7ab9f31b21aded9fc`  
		Last Modified: Thu, 20 Feb 2020 23:53:16 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:d6ac77d178d83433a94f4c1ac85d37eb6bde9a3b5e2ddd70510ab8366580d72d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 MB (30795142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59720519dbc2aaa04f42da6be01d883724212b4503025e14148efe901e90b553`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Sat, 18 Jan 2020 02:29:26 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 02:29:26 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 02:29:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 02:29:29 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 24 Jan 2020 00:09:58 GMT
ENV PHP_VERSION=7.4.2
# Fri, 24 Jan 2020 00:10:02 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.2.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.2.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 00:10:03 GMT
ENV PHP_SHA256=98284deac017da0d426117ecae7599a1f1bf62ae3911e8bc16c4403a8f4bdf13 PHP_MD5=
# Fri, 24 Jan 2020 00:10:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 24 Jan 2020 00:10:10 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 00:14:01 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 00:14:05 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Fri, 24 Jan 2020 00:14:09 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 00:14:10 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 00:14:11 GMT
CMD ["php" "-a"]
# Fri, 24 Jan 2020 02:50:27 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 24 Jan 2020 02:50:28 GMT
STOPSIGNAL SIGINT
# Fri, 24 Jan 2020 02:50:32 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 24 Jan 2020 02:50:32 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 02:50:36 GMT
RUN apk add --no-cache libpq
# Fri, 24 Jan 2020 02:51:09 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Fri, 24 Jan 2020 02:51:10 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 31 Jan 2020 17:39:37 GMT
ENV ADMINER_VERSION=4.7.6
# Fri, 31 Jan 2020 17:39:37 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Fri, 31 Jan 2020 17:39:38 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Fri, 31 Jan 2020 17:39:40 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 31 Jan 2020 17:39:41 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 31 Jan 2020 17:39:42 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 31 Jan 2020 17:39:42 GMT
USER adminer
# Fri, 31 Jan 2020 17:39:43 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 31 Jan 2020 17:39:44 GMT
EXPOSE 8080
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
	-	`sha256:aa724be546925194dbbb305717c1ec1404bd825d4e768f5fa30758fc836a1dda`  
		Last Modified: Fri, 24 Jan 2020 02:37:49 GMT  
		Size: 10.3 MB (10271109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b0bc8c61926931859ef4bf710fb73b709a407ca1086dfe704e7654934b4bdd`  
		Last Modified: Fri, 24 Jan 2020 02:37:45 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07be412705d63c11275e2018adae846b8861d4f678a21f2c43e2c22ae0bcee6d`  
		Last Modified: Fri, 24 Jan 2020 02:37:49 GMT  
		Size: 14.4 MB (14366228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73cafd3dde7ad30752409223dc0b26b0a5f4fa98d9a875225e2566bd99806655`  
		Last Modified: Fri, 24 Jan 2020 02:37:45 GMT  
		Size: 2.2 KB (2216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59195632759b7e9a57fb9ac253284ecbea9055d01c12f9caa49d23ca8f40bc1c`  
		Last Modified: Fri, 24 Jan 2020 02:37:45 GMT  
		Size: 72.7 KB (72676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6576a2f957338815a3fd8d1023a31cbb8ef8592406942ab75483b02adbe1c384`  
		Last Modified: Fri, 24 Jan 2020 02:52:47 GMT  
		Size: 310.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f6446e74a0df8b21f4f9ad86cf10fa3f6b6a9231d643d4174a5ddd3cf84f184`  
		Last Modified: Fri, 24 Jan 2020 02:52:47 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b69655ccf3f62cf1149958c93543bc91f9addef901545f4c74831b5c65b29039`  
		Last Modified: Fri, 24 Jan 2020 02:52:44 GMT  
		Size: 1.3 MB (1299236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:986406fbe9d0af0aeacc6c7cc032415d7552b4fd8f3fe60ea2313caa9193649c`  
		Last Modified: Fri, 24 Jan 2020 02:52:44 GMT  
		Size: 124.7 KB (124696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:382b47ced56d800090d03dff8f4d1183a7209bfd39013db12812d2efc2a39f54`  
		Last Modified: Fri, 24 Jan 2020 02:52:44 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23f30f175d57f1ffdc2f5c4308d886c2f842ce1a163c77b1747b628a89684ac`  
		Last Modified: Fri, 31 Jan 2020 17:40:10 GMT  
		Size: 570.8 KB (570779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d5044dac86a165d99ffacf0aaeb789461f31935ef0847d4e80ae612f101599`  
		Last Modified: Fri, 31 Jan 2020 17:40:10 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; 386

```console
$ docker pull adminer@sha256:d094fa6fd940847cd20c8dd698284d004cf1d6a5fa23d777f0b19667afa76346
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31684075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed77c13afb1993912752a1a0383da2185144a458fde112b713496146d193cb19`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Sat, 18 Jan 2020 05:41:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 05:41:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 05:41:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 05:41:39 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 23 Jan 2020 23:13:49 GMT
ENV PHP_VERSION=7.4.2
# Thu, 23 Jan 2020 23:13:49 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.2.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.2.tar.xz.asc/from/this/mirror
# Thu, 23 Jan 2020 23:13:49 GMT
ENV PHP_SHA256=98284deac017da0d426117ecae7599a1f1bf62ae3911e8bc16c4403a8f4bdf13 PHP_MD5=
# Thu, 23 Jan 2020 23:13:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 23 Jan 2020 23:13:52 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Jan 2020 23:21:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 23 Jan 2020 23:21:57 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 23 Jan 2020 23:21:59 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Jan 2020 23:21:59 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Jan 2020 23:22:00 GMT
CMD ["php" "-a"]
# Fri, 24 Jan 2020 07:25:41 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 24 Jan 2020 07:25:41 GMT
STOPSIGNAL SIGINT
# Fri, 24 Jan 2020 07:25:42 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 24 Jan 2020 07:25:42 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 07:25:43 GMT
RUN apk add --no-cache libpq
# Fri, 24 Jan 2020 07:26:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Fri, 24 Jan 2020 07:26:02 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 31 Jan 2020 17:38:17 GMT
ENV ADMINER_VERSION=4.7.6
# Fri, 31 Jan 2020 17:38:18 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Fri, 31 Jan 2020 17:38:18 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Fri, 31 Jan 2020 17:38:19 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 31 Jan 2020 17:38:19 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 31 Jan 2020 17:38:20 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 31 Jan 2020 17:38:20 GMT
USER adminer
# Fri, 31 Jan 2020 17:38:20 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 31 Jan 2020 17:38:20 GMT
EXPOSE 8080
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
	-	`sha256:9f3628b223c4b093cf7c2d7723ccd39dfcb6977a659c9c183e7673f22f44865b`  
		Last Modified: Fri, 24 Jan 2020 02:36:11 GMT  
		Size: 10.3 MB (10271099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e167c61f346105deafdbe6bff7f521715a3d31cd4c9ca27d6dca67654d916c`  
		Last Modified: Fri, 24 Jan 2020 02:36:08 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53425617927914b1561c930b3ce2f90644de41394e731ca71a5d66feeba55d5b`  
		Last Modified: Fri, 24 Jan 2020 02:36:19 GMT  
		Size: 15.0 MB (14974599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809347a8b4ae69caee1b666ac61ec86e0f2dd5d64744592a59f65fd9bb49c7c9`  
		Last Modified: Fri, 24 Jan 2020 02:36:10 GMT  
		Size: 2.2 KB (2216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31917077d16c99b9c58e44f9267cbda55763d759a59379d7e4ca1f9fd6acf60a`  
		Last Modified: Fri, 24 Jan 2020 02:36:09 GMT  
		Size: 72.3 KB (72331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc6ba5ae7aae77ac94c185eef225136d01333d8840f8896b412e359fa89e3ae6`  
		Last Modified: Fri, 24 Jan 2020 07:27:19 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aab9a7fed181e4a8d1621cf6e92e6b4525a242e1c102cac7a259b3336202c16`  
		Last Modified: Fri, 24 Jan 2020 07:27:19 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1120969ea66ac41447ffffddcda8e8d389a0a1c0c7feb7d9d650117b973459d`  
		Last Modified: Fri, 24 Jan 2020 07:27:18 GMT  
		Size: 1.4 MB (1397662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cf37d29a0120ccd9ef7f4f99c6d10673cd93097ebe961c86faf275c144f5929`  
		Last Modified: Fri, 24 Jan 2020 07:27:18 GMT  
		Size: 130.8 KB (130760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf17f4f8d6baa9c93722150405686cf214bc377adbb7ff2b891efe5ca38809c9`  
		Last Modified: Fri, 24 Jan 2020 07:27:18 GMT  
		Size: 1.5 KB (1472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cac8221b3739531c0e54a60c4d8d795c187ce863f2fb79955540c1b62347fbc7`  
		Last Modified: Fri, 31 Jan 2020 17:38:36 GMT  
		Size: 570.7 KB (570691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8127a70cc3e20105c94ab16913cab965e775aaa7cb37cc6398e47d4a1830241e`  
		Last Modified: Fri, 31 Jan 2020 17:38:36 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; ppc64le

```console
$ docker pull adminer@sha256:8906a11939b6681a5c547d8a1b3d8e58493fb85a66ef14177592239c9cd3ab6f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32169343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:251a9f8c0d32635a09c63fc8d5e5fbad2fee09cca0a4ea7cca903b5d9ac6f815`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Sat, 18 Jan 2020 03:24:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:24:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:24:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 03:24:34 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 23 Jan 2020 23:32:44 GMT
ENV PHP_VERSION=7.4.2
# Thu, 23 Jan 2020 23:32:47 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.2.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.2.tar.xz.asc/from/this/mirror
# Thu, 23 Jan 2020 23:32:50 GMT
ENV PHP_SHA256=98284deac017da0d426117ecae7599a1f1bf62ae3911e8bc16c4403a8f4bdf13 PHP_MD5=
# Thu, 23 Jan 2020 23:33:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 23 Jan 2020 23:33:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Jan 2020 23:36:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 23 Jan 2020 23:36:54 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 23 Jan 2020 23:37:00 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Jan 2020 23:37:02 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Jan 2020 23:37:04 GMT
CMD ["php" "-a"]
# Fri, 24 Jan 2020 05:51:10 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 24 Jan 2020 05:51:12 GMT
STOPSIGNAL SIGINT
# Fri, 24 Jan 2020 05:51:17 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 24 Jan 2020 05:51:19 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 05:51:23 GMT
RUN apk add --no-cache libpq
# Fri, 24 Jan 2020 05:51:48 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Fri, 24 Jan 2020 05:51:50 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 31 Jan 2020 17:16:45 GMT
ENV ADMINER_VERSION=4.7.6
# Fri, 31 Jan 2020 17:16:48 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Fri, 31 Jan 2020 17:16:51 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Fri, 31 Jan 2020 17:17:00 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 31 Jan 2020 17:17:01 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 31 Jan 2020 17:17:03 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 31 Jan 2020 17:17:05 GMT
USER adminer
# Fri, 31 Jan 2020 17:17:08 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 31 Jan 2020 17:17:10 GMT
EXPOSE 8080
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
	-	`sha256:c24c1e693453ad6efa656fcfa28e76c0786f80b4467d83c277d1116117942973`  
		Last Modified: Fri, 24 Jan 2020 02:32:44 GMT  
		Size: 10.3 MB (10271124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb71fc05f0fe0d365d8b9891f304e0cf2c1f6f0d2200ecdc0ea9a1c569117a1d`  
		Last Modified: Fri, 24 Jan 2020 02:32:41 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf26116548345ee1f676a6c1fabb768cd60750eb7a3a0ac7f09724350dde3b1`  
		Last Modified: Fri, 24 Jan 2020 02:32:54 GMT  
		Size: 15.5 MB (15539990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc4f870d6f2e6bbade33c0f28534b50765c4b56a093dc7565bd3ec3b37a7c603`  
		Last Modified: Fri, 24 Jan 2020 02:32:41 GMT  
		Size: 2.2 KB (2211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6a738ee51d709e4c4db983f9206a240500a2fc0dbaf3c76f6da2f99e5f6eb3b`  
		Last Modified: Fri, 24 Jan 2020 02:32:41 GMT  
		Size: 73.0 KB (72992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47bf1b73f7bf1089b7cf019ae582b63d77fa46e6c5b2b4efc16b0bf9d9b1ad9a`  
		Last Modified: Fri, 24 Jan 2020 05:53:47 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f984dcaccfb46a5cafd49380217e97342575055ceaaab4ff65a67f43af2da028`  
		Last Modified: Fri, 24 Jan 2020 05:53:47 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9e4520026a60556f0b631a13532b9a39d91d8eae94d4d3514359ef189ce4c94`  
		Last Modified: Fri, 24 Jan 2020 05:53:45 GMT  
		Size: 1.4 MB (1350626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba57cd117c3f571c3379a3fbb16d112291f4de925499dfeaad0bc7966c9483fb`  
		Last Modified: Fri, 24 Jan 2020 05:53:44 GMT  
		Size: 135.9 KB (135919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faef1730db86976915b65b75f76c1a057c321a983034e019f37ec833f5a1ffc9`  
		Last Modified: Fri, 24 Jan 2020 05:53:44 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:620c9c1b5881ba0a3be097e7cb57c695406737868e7b1adc02c5561c5f7b1649`  
		Last Modified: Fri, 31 Jan 2020 17:18:05 GMT  
		Size: 570.8 KB (570776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03e77753eec72902172405ef4c8c0c667bf7377cd0dc6cc1441afd0890991d43`  
		Last Modified: Fri, 31 Jan 2020 17:18:04 GMT  
		Size: 501.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:fastcgi`

```console
$ docker pull adminer@sha256:85ef53ce6942c89cdacf05991c16132da81d158741e42e2eef13b3c4111ba801
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `adminer:fastcgi` - linux; amd64

```console
$ docker pull adminer@sha256:3261472ab50e9daaf45a30818ad65311dc175417adf46363ecf18c7fb79f4048
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31132621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f894c56f8bea377d752a7839e5b2af6ffeab97af51d7b9b54e8c3113a954b088`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
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
# Sat, 18 Jan 2020 03:23:44 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 24 Jan 2020 07:13:33 GMT
ENV PHP_VERSION=7.4.2
# Fri, 24 Jan 2020 07:13:33 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.2.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.2.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 07:13:34 GMT
ENV PHP_SHA256=98284deac017da0d426117ecae7599a1f1bf62ae3911e8bc16c4403a8f4bdf13 PHP_MD5=
# Fri, 24 Jan 2020 07:13:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 24 Jan 2020 07:13:36 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 07:19:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 07:19:23 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Fri, 24 Jan 2020 07:19:24 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 07:19:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 07:19:24 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 07:19:25 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 24 Jan 2020 07:19:25 GMT
STOPSIGNAL SIGQUIT
# Fri, 24 Jan 2020 07:19:25 GMT
EXPOSE 9000
# Fri, 24 Jan 2020 07:19:25 GMT
CMD ["php-fpm"]
# Fri, 24 Jan 2020 10:52:50 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 24 Jan 2020 10:52:51 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 24 Jan 2020 10:52:52 GMT
RUN apk add --no-cache libpq
# Fri, 24 Jan 2020 10:53:11 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Fri, 24 Jan 2020 10:53:11 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 31 Jan 2020 17:19:33 GMT
ENV ADMINER_VERSION=4.7.6
# Fri, 31 Jan 2020 17:19:33 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Fri, 31 Jan 2020 17:19:33 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Fri, 31 Jan 2020 17:19:34 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 31 Jan 2020 17:19:34 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 31 Jan 2020 17:19:35 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 31 Jan 2020 17:19:35 GMT
USER adminer
# Fri, 31 Jan 2020 17:19:35 GMT
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
	-	`sha256:6e71cca12e10fbf7814b66f3f30f2c626a76931eb1658b35580520657aa1c472`  
		Last Modified: Fri, 24 Jan 2020 10:39:58 GMT  
		Size: 10.3 MB (10271098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed2310d2f7910e8f29ab569006386735c80fdb8d7a9f4b50c2233347335ef47e`  
		Last Modified: Fri, 24 Jan 2020 10:39:55 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:601ef2217a14892579aa55bfff77d380170c0c5b6bb97ba4275769e288cc008e`  
		Last Modified: Fri, 24 Jan 2020 10:40:00 GMT  
		Size: 14.6 MB (14640028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41dc18d982f54d4c5634f99e7933d9ad3069ef493b460cf998e1954caa2f24b7`  
		Last Modified: Fri, 24 Jan 2020 10:39:55 GMT  
		Size: 2.2 KB (2219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72be421f63f8c4ae023b97af91e72adcad7347edfff80e8fe6d0fea64be89f41`  
		Last Modified: Fri, 24 Jan 2020 10:39:56 GMT  
		Size: 73.1 KB (73144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f10dd871243fb2f678d5abcd0925bfc78bf759edf24b577c2aaaecce51ac30fb`  
		Last Modified: Fri, 24 Jan 2020 10:39:55 GMT  
		Size: 8.4 KB (8409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df30bf875af7c93a1a5f0231eb502f80916cc360f7bb5301af9fd174346bae03`  
		Last Modified: Fri, 24 Jan 2020 10:53:53 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb01654c81755c04f51d84470d9460f05137a60b5cb6af11a277b81ffdb12844`  
		Last Modified: Fri, 24 Jan 2020 10:53:53 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc08268651428df387dfafc653a2ce4c616f5eb02a72752692c59c871b99d37`  
		Last Modified: Fri, 24 Jan 2020 10:53:52 GMT  
		Size: 1.3 MB (1277248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ee28a212305aa260efa44f897f666e2d55a5c7b69b1eacb4913985baf64c9a`  
		Last Modified: Fri, 24 Jan 2020 10:53:52 GMT  
		Size: 126.6 KB (126627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60596dcdb9d8dba4d1f1beb1964daee86e4d999728581b4ed91e9edc6dd78a87`  
		Last Modified: Fri, 24 Jan 2020 10:53:52 GMT  
		Size: 1.5 KB (1474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30705479566e7b730c43bc045a5c98474f7fa05a827632e22deb9c00247a1792`  
		Last Modified: Fri, 31 Jan 2020 17:19:53 GMT  
		Size: 570.7 KB (570684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d656991abfa4ac7b964071b05e6a5c7e82cfb72e2de48fb119f733649768109`  
		Last Modified: Fri, 31 Jan 2020 17:19:53 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; arm variant v6

```console
$ docker pull adminer@sha256:f3ef94b81d53fa10bdf91813ec1727746da25896c82eb5418da6183ff345fe42
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.9 MB (29904916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13e34cefffcf1ef42f5bc12f108decf6d572e5812224b5f36b8008069927885c`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
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
# Sat, 18 Jan 2020 03:44:54 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 20 Feb 2020 21:54:14 GMT
ENV PHP_VERSION=7.4.3
# Thu, 20 Feb 2020 21:54:15 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.3.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.3.tar.xz.asc/from/this/mirror
# Thu, 20 Feb 2020 21:54:16 GMT
ENV PHP_SHA256=cf1f856d877c268124ded1ede40c9fb6142b125fdaafdc54f855120b8bc6982a PHP_MD5=
# Thu, 20 Feb 2020 21:54:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Feb 2020 21:54:23 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Feb 2020 21:58:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 20 Feb 2020 21:58:38 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Thu, 20 Feb 2020 21:58:41 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Feb 2020 21:58:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Feb 2020 21:58:43 GMT
WORKDIR /var/www/html
# Thu, 20 Feb 2020 21:58:45 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 20 Feb 2020 21:58:46 GMT
STOPSIGNAL SIGQUIT
# Thu, 20 Feb 2020 21:58:48 GMT
EXPOSE 9000
# Thu, 20 Feb 2020 21:58:49 GMT
CMD ["php-fpm"]
# Thu, 20 Feb 2020 23:47:03 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Thu, 20 Feb 2020 23:47:05 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 20 Feb 2020 23:47:07 GMT
RUN apk add --no-cache libpq
# Thu, 20 Feb 2020 23:47:34 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Thu, 20 Feb 2020 23:47:35 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Thu, 20 Feb 2020 23:47:35 GMT
ENV ADMINER_VERSION=4.7.6
# Thu, 20 Feb 2020 23:47:36 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Thu, 20 Feb 2020 23:47:37 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Thu, 20 Feb 2020 23:47:40 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Thu, 20 Feb 2020 23:47:41 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 20 Feb 2020 23:47:41 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Thu, 20 Feb 2020 23:47:42 GMT
USER adminer
# Thu, 20 Feb 2020 23:47:42 GMT
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
	-	`sha256:80ca3c99ad3f93290cc94e506f94e8b01e2bfe5d2901b45ad4fd1bf704e70ed7`  
		Last Modified: Thu, 20 Feb 2020 23:10:40 GMT  
		Size: 10.3 MB (10280253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f658c7e1eb0d0386247f8fa5f228f97f709e09b53982bd1ba92f38cad3803ec8`  
		Last Modified: Thu, 20 Feb 2020 23:10:36 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38dd2d597adffab2d9b483cfa2352a9413ca3868e55fccb30c7551e0c1a7cb57`  
		Last Modified: Thu, 20 Feb 2020 23:10:42 GMT  
		Size: 13.7 MB (13671450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bfdd3dff152326a8135a5747de2a94547b298afe86fe63946bb425bc30fba92`  
		Last Modified: Thu, 20 Feb 2020 23:10:36 GMT  
		Size: 2.2 KB (2213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5554b593396e1abf2813391b3b1c84e40383b0988321d2d63616a290aa7fed7d`  
		Last Modified: Thu, 20 Feb 2020 23:10:36 GMT  
		Size: 72.7 KB (72681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9159be50c0fe27b27be4abb997de85c54fd2d1308d35c5c6c97e4d118fdec6a0`  
		Last Modified: Thu, 20 Feb 2020 23:10:37 GMT  
		Size: 8.4 KB (8412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28aa812c7cc19a079c92c7f6eba0da1ecffdcf6f1fe4946898b7ec9ff1b6940a`  
		Last Modified: Thu, 20 Feb 2020 23:48:28 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a7c93eb4a00db350eb6b34997b1f9541d4851def62b039696d47ae3b25f55f8`  
		Last Modified: Thu, 20 Feb 2020 23:48:28 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:820825c9319f4e49d67cd84bb103b76d2cca8df1f674d7a84b6b5ef1f43afe3b`  
		Last Modified: Thu, 20 Feb 2020 23:48:23 GMT  
		Size: 1.2 MB (1234699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49c16bab556b699d17b5ef77dfbbc559d0fabd75d27f9eed069b3753331c0e5a`  
		Last Modified: Thu, 20 Feb 2020 23:48:23 GMT  
		Size: 120.1 KB (120098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1ec2a9c5203dcc61950a047d4f04c455f284b6062740fbc081a32c7fb5873b2`  
		Last Modified: Thu, 20 Feb 2020 23:48:23 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:295fdb00d23508c2695ae7402b772fdd479d44cd0f0a05c93b069242638a3e0f`  
		Last Modified: Thu, 20 Feb 2020 23:48:23 GMT  
		Size: 570.8 KB (570771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92b8b25d3ffd6ef7dd0976b4b19b04842ed268bfbc55452f5000ba913defa355`  
		Last Modified: Thu, 20 Feb 2020 23:48:23 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; arm variant v7

```console
$ docker pull adminer@sha256:2f5f67a712318a2a917724f95730ad156ec7427834865497016e22de6541cc5c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.6 MB (28642438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c803a31f5e4241a9cb82515d1cc260871c3f62e3c30297d71a35973096a31e2`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
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
# Sat, 18 Jan 2020 05:28:02 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 20 Feb 2020 21:14:19 GMT
ENV PHP_VERSION=7.4.3
# Thu, 20 Feb 2020 21:14:19 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.3.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.3.tar.xz.asc/from/this/mirror
# Thu, 20 Feb 2020 21:14:20 GMT
ENV PHP_SHA256=cf1f856d877c268124ded1ede40c9fb6142b125fdaafdc54f855120b8bc6982a PHP_MD5=
# Thu, 20 Feb 2020 21:14:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Feb 2020 21:14:24 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Feb 2020 21:16:45 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 20 Feb 2020 21:16:46 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Thu, 20 Feb 2020 21:16:49 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Feb 2020 21:16:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Feb 2020 21:16:50 GMT
WORKDIR /var/www/html
# Thu, 20 Feb 2020 21:16:51 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 20 Feb 2020 21:16:52 GMT
STOPSIGNAL SIGQUIT
# Thu, 20 Feb 2020 21:16:53 GMT
EXPOSE 9000
# Thu, 20 Feb 2020 21:16:54 GMT
CMD ["php-fpm"]
# Thu, 20 Feb 2020 23:52:02 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Thu, 20 Feb 2020 23:52:05 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 20 Feb 2020 23:52:08 GMT
RUN apk add --no-cache libpq
# Thu, 20 Feb 2020 23:52:41 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Thu, 20 Feb 2020 23:52:43 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Thu, 20 Feb 2020 23:52:44 GMT
ENV ADMINER_VERSION=4.7.6
# Thu, 20 Feb 2020 23:52:45 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Thu, 20 Feb 2020 23:52:46 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Thu, 20 Feb 2020 23:52:49 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Thu, 20 Feb 2020 23:52:50 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 20 Feb 2020 23:52:51 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Thu, 20 Feb 2020 23:52:52 GMT
USER adminer
# Thu, 20 Feb 2020 23:52:54 GMT
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
	-	`sha256:0b327d731622fe78b5dce5377da7c2fa2a8f7f5bccb0851084b9329f9a570063`  
		Last Modified: Thu, 20 Feb 2020 23:26:52 GMT  
		Size: 10.3 MB (10280261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4b40e24dacf2616800de7bb9e410e263de6eccf4d1bfd5a22d32908c21b2361`  
		Last Modified: Thu, 20 Feb 2020 23:26:49 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e42a50422a3ffed17517bce0eb1fe538eea06417fdc672c4711d134108d7b0b4`  
		Last Modified: Thu, 20 Feb 2020 23:26:54 GMT  
		Size: 12.8 MB (12815724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5473e54c50261b361a070da14923a840b1c2155de57aacac9a8ff18575dd6e1a`  
		Last Modified: Thu, 20 Feb 2020 23:26:50 GMT  
		Size: 2.2 KB (2216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f939d7049d7edb45231e24fec17211f863a36748747b3121cc935b6760c86632`  
		Last Modified: Thu, 20 Feb 2020 23:26:49 GMT  
		Size: 72.7 KB (72680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e26488d2c5a3fcc5e1d56a02cd6a6755d2bf8a503dfb6bff0c265cedf52a11fa`  
		Last Modified: Thu, 20 Feb 2020 23:26:49 GMT  
		Size: 8.4 KB (8409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7b9f9e7ecb2380e21319c90bc307fa28a14061bc3b629ea3cafaebe8e7865e3`  
		Last Modified: Thu, 20 Feb 2020 23:53:39 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:214861e86ee457b4f34bad18e669992ef9dff229e599e0f7f15f41b926a9ec31`  
		Last Modified: Thu, 20 Feb 2020 23:53:39 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6f9a71b7d4f646e777f739107b1911cf18f3305a0f3348c54572385f6f5d71f`  
		Last Modified: Thu, 20 Feb 2020 23:53:37 GMT  
		Size: 1.1 MB (1124908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3757929f73de69aebca78a3f042c638bb48e703b5a1ce80fc02e2eae8b45cdf`  
		Last Modified: Thu, 20 Feb 2020 23:53:37 GMT  
		Size: 115.0 KB (114950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3151fc0a4ad4389a4655e265bca8650f675575130c4394907f6abe79dc4bacf3`  
		Last Modified: Thu, 20 Feb 2020 23:53:37 GMT  
		Size: 1.5 KB (1477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85281d825070bdddb16a2bacfad1baa7633a1a1e22d32c6ad458bbac70bc1737`  
		Last Modified: Thu, 20 Feb 2020 23:53:37 GMT  
		Size: 570.8 KB (570766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499386092f7399a059f809ff852ca1239313c7555831f07909a8cc81d06f386d`  
		Last Modified: Thu, 20 Feb 2020 23:53:37 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:4f9923edd71c163c491fec06013c2c29c6c486e96f1a5a5fe9f6a15d7d0cdb08
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30872795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c607c25c09ed37fcb1262db44e11192f84fc037fe9d82ebbd207a31813123ff5`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
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
# Sat, 18 Jan 2020 02:36:11 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 24 Jan 2020 00:14:35 GMT
ENV PHP_VERSION=7.4.2
# Fri, 24 Jan 2020 00:14:36 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.2.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.2.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 00:14:38 GMT
ENV PHP_SHA256=98284deac017da0d426117ecae7599a1f1bf62ae3911e8bc16c4403a8f4bdf13 PHP_MD5=
# Fri, 24 Jan 2020 00:14:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 24 Jan 2020 00:14:45 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 00:18:29 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 00:18:32 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Fri, 24 Jan 2020 00:18:36 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 00:18:37 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 00:18:38 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 00:18:41 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 24 Jan 2020 00:18:42 GMT
STOPSIGNAL SIGQUIT
# Fri, 24 Jan 2020 00:18:44 GMT
EXPOSE 9000
# Fri, 24 Jan 2020 00:18:45 GMT
CMD ["php-fpm"]
# Fri, 24 Jan 2020 02:51:31 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 24 Jan 2020 02:51:33 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 24 Jan 2020 02:51:36 GMT
RUN apk add --no-cache libpq
# Fri, 24 Jan 2020 02:52:06 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Fri, 24 Jan 2020 02:52:07 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 31 Jan 2020 17:39:50 GMT
ENV ADMINER_VERSION=4.7.6
# Fri, 31 Jan 2020 17:39:51 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Fri, 31 Jan 2020 17:39:51 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Fri, 31 Jan 2020 17:39:54 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 31 Jan 2020 17:39:55 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 31 Jan 2020 17:39:55 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 31 Jan 2020 17:39:56 GMT
USER adminer
# Fri, 31 Jan 2020 17:39:57 GMT
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
	-	`sha256:031bf935aef9c8cf9a41b1dbd509b48db2ab230dae75e8d1f2f20c1713826cfa`  
		Last Modified: Fri, 24 Jan 2020 02:38:24 GMT  
		Size: 10.3 MB (10271108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd439e1038e9d42eab7437e8f85a4c7cd369089af8cb708e63e0c4388fdb1bf3`  
		Last Modified: Fri, 24 Jan 2020 02:38:16 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25ed1e9754e061a3e75c31e172b7e2ef4b7b5a8673a24423b2260a91000daed9`  
		Last Modified: Fri, 24 Jan 2020 02:38:20 GMT  
		Size: 14.4 MB (14435498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5801422dba8896819ba048a35c0da81a25eec8fb91c74ddc3da87bbbf13fd470`  
		Last Modified: Fri, 24 Jan 2020 02:38:16 GMT  
		Size: 2.2 KB (2217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d4f983059021c9010c5326e718d5870d3ed28a792a95b78f95399c93b6b963f`  
		Last Modified: Fri, 24 Jan 2020 02:38:16 GMT  
		Size: 72.7 KB (72672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:947d95e1f7678a8070ee18dba3cf26e07c11e7a0f1fed1885014776890783c64`  
		Last Modified: Fri, 24 Jan 2020 02:38:16 GMT  
		Size: 8.4 KB (8410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8246e4f25893c2c59d16a3a91eb0e024ee6b366eb1828d39c00069b0fe074821`  
		Last Modified: Fri, 24 Jan 2020 02:53:09 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153c72183d2af4959ab20862dab40a0a198583b2ed6460c78eb4b58afbe8099a`  
		Last Modified: Fri, 24 Jan 2020 02:53:08 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79ea398fe8d2d7940f02c220eac23b6e0b59f654452a7c2d784746f57264e66`  
		Last Modified: Fri, 24 Jan 2020 02:53:07 GMT  
		Size: 1.3 MB (1299219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a60c746308f1dc0af8f8ee2c44315d9bb1b416377a2938f63d9a70ab2d0f06ad`  
		Last Modified: Fri, 24 Jan 2020 02:53:07 GMT  
		Size: 124.7 KB (124702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca6bc7dce64e9b13729a1e1afd341a91788f4a0d94380b7cc81feec83f580bf6`  
		Last Modified: Fri, 24 Jan 2020 02:53:06 GMT  
		Size: 1.5 KB (1474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f1dac04eb03855c7c287673ef8e4c6d1c4915d3663f9376444abe8e8c3c1ed4`  
		Last Modified: Fri, 31 Jan 2020 17:40:25 GMT  
		Size: 570.8 KB (570773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44ddb8bdcd055db611ac57e0a6bc167bd231eaf893f9d7d11e3f0d13025cf98`  
		Last Modified: Fri, 31 Jan 2020 17:40:25 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; 386

```console
$ docker pull adminer@sha256:46b8bb610eaaa99932c42a3352a7bb709eddd218944284a41d4a25ab9e2593db
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31762110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e5c58ebd525deeac88b11a3c516b9d22ac70308fcd0aeb5cc2624988423c31`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
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
# Sat, 18 Jan 2020 05:48:40 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 23 Jan 2020 23:22:10 GMT
ENV PHP_VERSION=7.4.2
# Thu, 23 Jan 2020 23:22:10 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.2.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.2.tar.xz.asc/from/this/mirror
# Thu, 23 Jan 2020 23:22:11 GMT
ENV PHP_SHA256=98284deac017da0d426117ecae7599a1f1bf62ae3911e8bc16c4403a8f4bdf13 PHP_MD5=
# Thu, 23 Jan 2020 23:22:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 23 Jan 2020 23:22:16 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Jan 2020 23:31:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 23 Jan 2020 23:31:14 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Thu, 23 Jan 2020 23:31:15 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Jan 2020 23:31:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Jan 2020 23:31:15 GMT
WORKDIR /var/www/html
# Thu, 23 Jan 2020 23:31:16 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 23 Jan 2020 23:31:16 GMT
STOPSIGNAL SIGQUIT
# Thu, 23 Jan 2020 23:31:16 GMT
EXPOSE 9000
# Thu, 23 Jan 2020 23:31:17 GMT
CMD ["php-fpm"]
# Fri, 24 Jan 2020 07:26:11 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 24 Jan 2020 07:26:12 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 24 Jan 2020 07:26:14 GMT
RUN apk add --no-cache libpq
# Fri, 24 Jan 2020 07:26:45 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Fri, 24 Jan 2020 07:26:45 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 31 Jan 2020 17:38:25 GMT
ENV ADMINER_VERSION=4.7.6
# Fri, 31 Jan 2020 17:38:25 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Fri, 31 Jan 2020 17:38:25 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Fri, 31 Jan 2020 17:38:26 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 31 Jan 2020 17:38:27 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 31 Jan 2020 17:38:27 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 31 Jan 2020 17:38:27 GMT
USER adminer
# Fri, 31 Jan 2020 17:38:27 GMT
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
	-	`sha256:7af2969e346cf39dce09953165d38ac70a637f81bf36a72173d23c8209522b1e`  
		Last Modified: Fri, 24 Jan 2020 02:36:49 GMT  
		Size: 10.3 MB (10271104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dffed627d6f3eb28e87526c201e8ae30d110efc1e7ae5b48646e1f322abddefd`  
		Last Modified: Fri, 24 Jan 2020 02:36:40 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44af2512ec067db56bee629528b24bfe54ad55f8f7064b2cf59f57868950482d`  
		Last Modified: Fri, 24 Jan 2020 02:36:51 GMT  
		Size: 15.0 MB (15044190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a34e204f3d52c0be6c78857ce18184fecbd91cf297cfb30bf15df00d78b1ff71`  
		Last Modified: Fri, 24 Jan 2020 02:36:40 GMT  
		Size: 2.2 KB (2217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c9a720f2eaf0aec04eabdd4c10f331bd1eb5e91bdf806ec43279ae4d9435107`  
		Last Modified: Fri, 24 Jan 2020 02:36:41 GMT  
		Size: 72.3 KB (72332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ce027d9508f9c2ba08e68a1cbef48753b345821147a4ec4dd52ced22ca8252`  
		Last Modified: Fri, 24 Jan 2020 02:36:40 GMT  
		Size: 8.4 KB (8413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:791ceb40ab90a13fa40d9a11daa5853b0d7c1f72f7fb2580891e34049e7be6ba`  
		Last Modified: Fri, 24 Jan 2020 07:27:33 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac79a09757dcd35db84f1d12d43f5d8f11408f92ee9e095c392eda59733b801a`  
		Last Modified: Fri, 24 Jan 2020 07:27:33 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b6beb85931082255a7f9048c7f337e1972e10ce8a02c86b86797e95922ad930`  
		Last Modified: Fri, 24 Jan 2020 07:27:34 GMT  
		Size: 1.4 MB (1397661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79d5b1485f733f60d9843f7e138f1fa150e42d713df194640dcc37931ec1c191`  
		Last Modified: Fri, 24 Jan 2020 07:27:31 GMT  
		Size: 130.8 KB (130793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:553d2e165ba3dd32a4a9a44d46fa13ec6552747310640f783b34255acfd961e2`  
		Last Modified: Fri, 24 Jan 2020 07:27:31 GMT  
		Size: 1.5 KB (1472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42e41cc3dbdf2dad75063abe783a7985dc9267ee1ee9bd5751bed6f0cba09c2b`  
		Last Modified: Fri, 31 Jan 2020 17:38:46 GMT  
		Size: 570.7 KB (570683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd7e34ec5637f78a0244c66e92539e53bcc0bc77fafc96f775c60a3dbfce14ef`  
		Last Modified: Fri, 31 Jan 2020 17:38:46 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; ppc64le

```console
$ docker pull adminer@sha256:52c4be54d3cd71b8c7ef779124ae7e3796754fad9594b24584b157fe0d90ea88
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32259051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:058dcefad0447822a717afd8533b7ef7ac94f28229ce3c409df8c013633ad069`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
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
# Sat, 18 Jan 2020 03:29:20 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 23 Jan 2020 23:37:14 GMT
ENV PHP_VERSION=7.4.2
# Thu, 23 Jan 2020 23:37:17 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.2.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.2.tar.xz.asc/from/this/mirror
# Thu, 23 Jan 2020 23:37:18 GMT
ENV PHP_SHA256=98284deac017da0d426117ecae7599a1f1bf62ae3911e8bc16c4403a8f4bdf13 PHP_MD5=
# Thu, 23 Jan 2020 23:37:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 23 Jan 2020 23:37:30 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Jan 2020 23:41:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 23 Jan 2020 23:41:16 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Thu, 23 Jan 2020 23:41:21 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Jan 2020 23:41:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Jan 2020 23:41:25 GMT
WORKDIR /var/www/html
# Thu, 23 Jan 2020 23:41:31 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 23 Jan 2020 23:41:34 GMT
STOPSIGNAL SIGQUIT
# Thu, 23 Jan 2020 23:41:36 GMT
EXPOSE 9000
# Thu, 23 Jan 2020 23:41:37 GMT
CMD ["php-fpm"]
# Fri, 24 Jan 2020 05:52:24 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 24 Jan 2020 05:52:29 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 24 Jan 2020 05:52:35 GMT
RUN apk add --no-cache libpq
# Fri, 24 Jan 2020 05:53:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Fri, 24 Jan 2020 05:53:04 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 31 Jan 2020 17:17:22 GMT
ENV ADMINER_VERSION=4.7.6
# Fri, 31 Jan 2020 17:17:23 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Fri, 31 Jan 2020 17:17:24 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Fri, 31 Jan 2020 17:17:33 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 31 Jan 2020 17:17:35 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 31 Jan 2020 17:17:39 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 31 Jan 2020 17:17:42 GMT
USER adminer
# Fri, 31 Jan 2020 17:17:44 GMT
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
	-	`sha256:71750c6fa0607bea7a09ff35d6a1406245a40b8230624a3639b89d18db4394fe`  
		Last Modified: Fri, 24 Jan 2020 02:33:52 GMT  
		Size: 10.3 MB (10271124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9edfe3521268768bb7368d494a54a58f6ea37444d81365db80594ba5cf6723e`  
		Last Modified: Fri, 24 Jan 2020 02:33:41 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03d6040910816a926d5c549b0b705387c888406057cdb66956db3c32125ac16`  
		Last Modified: Fri, 24 Jan 2020 02:33:50 GMT  
		Size: 15.6 MB (15621302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60eae056a292b760c3cccf048be586d181427ad78105d2293c95ba02dbaf0ba1`  
		Last Modified: Fri, 24 Jan 2020 02:33:41 GMT  
		Size: 2.2 KB (2215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:728ffb10bff4c1ede1c201f677ecc8c6ad6fcaa32489ca45d7dc1ffb57804d89`  
		Last Modified: Fri, 24 Jan 2020 02:33:41 GMT  
		Size: 73.0 KB (72996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:348111edcf048b6a351ad6caed9d560f0dad7e6bbe2b76922a0648db42f74bcc`  
		Last Modified: Fri, 24 Jan 2020 02:33:42 GMT  
		Size: 8.4 KB (8409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b18f3572f56ef640587e5e01d586e9ac24e3c39688ad60eb7e2542c28330ef15`  
		Last Modified: Fri, 24 Jan 2020 05:54:24 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25b30d4afe834c4c6add7f1325d981a4767fe2d659474a4bcf07fe0982d30779`  
		Last Modified: Fri, 24 Jan 2020 05:54:23 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd12c1dc772a4360a1f25b4d61773bf85a5ce8636a383a26214f52199698c03a`  
		Last Modified: Fri, 24 Jan 2020 05:54:23 GMT  
		Size: 1.4 MB (1350625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc0b0a44d83a34b0167638ba083ff0f468a535b3a75087a1810e07394e5c6e8e`  
		Last Modified: Fri, 24 Jan 2020 05:54:20 GMT  
		Size: 135.9 KB (135904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1114f35e53ffc221921a3954ec43719e7f1e8adcc07c6b0f7b75364065ed97d7`  
		Last Modified: Fri, 24 Jan 2020 05:54:20 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:609b9a3cccb86ade52bbc4fb6a19223fa44f14509e75e7c2e4438278ef3a37b6`  
		Last Modified: Fri, 31 Jan 2020 17:18:36 GMT  
		Size: 570.8 KB (570772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b5ca04b772bc2f523594fd55735ad7e753da72ecf87478b23db102df001437`  
		Last Modified: Fri, 31 Jan 2020 17:18:36 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:latest`

```console
$ docker pull adminer@sha256:c689401f4ee85e37ba2cd62d401af2d569833dd8efa2c338177889fa9c525882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `adminer:latest` - linux; amd64

```console
$ docker pull adminer@sha256:6ceb642133ac56e267c50ae4bfb24ac0008b0eb02b772abae9059caa45211bee
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31058191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:259cc60bdb72538cffc06536d8bb73c3d9afd7156afc71b0c97fb1659917805e`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Sat, 18 Jan 2020 03:18:30 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:18:30 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:18:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 03:18:30 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 24 Jan 2020 07:05:12 GMT
ENV PHP_VERSION=7.4.2
# Fri, 24 Jan 2020 07:05:13 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.2.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.2.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 07:05:13 GMT
ENV PHP_SHA256=98284deac017da0d426117ecae7599a1f1bf62ae3911e8bc16c4403a8f4bdf13 PHP_MD5=
# Fri, 24 Jan 2020 07:05:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 24 Jan 2020 07:05:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 07:13:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 07:13:16 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Fri, 24 Jan 2020 07:13:17 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 07:13:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 07:13:17 GMT
CMD ["php" "-a"]
# Fri, 24 Jan 2020 10:52:17 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 24 Jan 2020 10:52:17 GMT
STOPSIGNAL SIGINT
# Fri, 24 Jan 2020 10:52:18 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 24 Jan 2020 10:52:18 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 10:52:19 GMT
RUN apk add --no-cache libpq
# Fri, 24 Jan 2020 10:52:38 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Fri, 24 Jan 2020 10:52:39 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 31 Jan 2020 17:19:26 GMT
ENV ADMINER_VERSION=4.7.6
# Fri, 31 Jan 2020 17:19:26 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Fri, 31 Jan 2020 17:19:26 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Fri, 31 Jan 2020 17:19:27 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 31 Jan 2020 17:19:28 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 31 Jan 2020 17:19:28 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 31 Jan 2020 17:19:28 GMT
USER adminer
# Fri, 31 Jan 2020 17:19:28 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 31 Jan 2020 17:19:28 GMT
EXPOSE 8080
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
	-	`sha256:5fa47f19b1e835f47f4c1273ccb215a42ee2aefafe300409d92b05b899a757d8`  
		Last Modified: Fri, 24 Jan 2020 10:39:33 GMT  
		Size: 10.3 MB (10271096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4556adb19ddcb43be3cd12b973f718e5edc74d6986ae4406a0c3011cbeb3dc93`  
		Last Modified: Fri, 24 Jan 2020 10:39:33 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:205de55b7ed0d389ac2c9777321f11ba9377a148002c2ef1d7b68d02a96472f3`  
		Last Modified: Fri, 24 Jan 2020 10:39:42 GMT  
		Size: 14.6 MB (14574023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c35aa7da966a732561c37c8b5d56949eedcb7865066b86da95c8bc58c18c48d2`  
		Last Modified: Fri, 24 Jan 2020 10:39:32 GMT  
		Size: 2.2 KB (2216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82a54ca6f814c156199e3266c4297efe2f54fb83bfb1645f53582eae3d1e222e`  
		Last Modified: Fri, 24 Jan 2020 10:39:33 GMT  
		Size: 73.1 KB (73145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e28f69f8cf7d397d8bd78cab68b9713275989e440016ec98580b94d0b0dc23f8`  
		Last Modified: Fri, 24 Jan 2020 10:53:42 GMT  
		Size: 306.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b527d0b89c2ea24dd10be7c18c1dcdf592fd4e1a5ff2c9da47fba2940fbb25a7`  
		Last Modified: Fri, 24 Jan 2020 10:53:42 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35b881820e3f1402cd2b2836dc6064db1b8ef029479448d5a058baa86b0f2e29`  
		Last Modified: Fri, 24 Jan 2020 10:53:41 GMT  
		Size: 1.3 MB (1277246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97e920225fdf7c9fc6bd8762ee3efbc9225341331c21812757347e46b22a2db3`  
		Last Modified: Fri, 24 Jan 2020 10:53:41 GMT  
		Size: 126.6 KB (126617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c8cde070aec4f16d202102cbdad6a161e48b4ffae4426da85717e9ee116fbec`  
		Last Modified: Fri, 24 Jan 2020 10:53:40 GMT  
		Size: 1.5 KB (1474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:028d5feebf26f852c8d09343a1b1ea1be953837a2f402743e1c021ea7b15ccee`  
		Last Modified: Fri, 31 Jan 2020 17:19:44 GMT  
		Size: 570.7 KB (570688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e0b9ec991cbee8b6377946c76367fcaa9782c4be8d265be834c5158b2638d40`  
		Last Modified: Fri, 31 Jan 2020 17:19:44 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; arm variant v6

```console
$ docker pull adminer@sha256:086342d4149c1554e7c334711e0c6ccfa783ce0991cdd33d1687ca56e83020c7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.8 MB (29825140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08598589c478e6d488e3d5892d914c3ccac2ca333bf32b79046b127a04438a92`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Sat, 18 Jan 2020 03:40:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:40:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:40:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 03:40:19 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 20 Feb 2020 21:49:41 GMT
ENV PHP_VERSION=7.4.3
# Thu, 20 Feb 2020 21:49:43 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.3.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.3.tar.xz.asc/from/this/mirror
# Thu, 20 Feb 2020 21:49:44 GMT
ENV PHP_SHA256=cf1f856d877c268124ded1ede40c9fb6142b125fdaafdc54f855120b8bc6982a PHP_MD5=
# Thu, 20 Feb 2020 21:49:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Feb 2020 21:49:57 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Feb 2020 21:53:47 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 20 Feb 2020 21:53:50 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 20 Feb 2020 21:53:53 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Feb 2020 21:53:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Feb 2020 21:53:54 GMT
CMD ["php" "-a"]
# Thu, 20 Feb 2020 23:45:59 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Thu, 20 Feb 2020 23:45:59 GMT
STOPSIGNAL SIGINT
# Thu, 20 Feb 2020 23:46:02 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 20 Feb 2020 23:46:03 GMT
WORKDIR /var/www/html
# Thu, 20 Feb 2020 23:46:05 GMT
RUN apk add --no-cache libpq
# Thu, 20 Feb 2020 23:46:36 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Thu, 20 Feb 2020 23:46:39 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Thu, 20 Feb 2020 23:46:41 GMT
ENV ADMINER_VERSION=4.7.6
# Thu, 20 Feb 2020 23:46:41 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Thu, 20 Feb 2020 23:46:42 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Thu, 20 Feb 2020 23:46:45 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Thu, 20 Feb 2020 23:46:46 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 20 Feb 2020 23:46:46 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Thu, 20 Feb 2020 23:46:47 GMT
USER adminer
# Thu, 20 Feb 2020 23:46:48 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 20 Feb 2020 23:46:48 GMT
EXPOSE 8080
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
	-	`sha256:f246fe8b62d43a3f633a04898577258a2ce5dd84edf5fd464403b9a108b301e2`  
		Last Modified: Thu, 20 Feb 2020 23:10:06 GMT  
		Size: 10.3 MB (10280264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b4e0af10768397859f6f19eca4b17ee9f21d61a1cb06989aba861267cf1b6a`  
		Last Modified: Thu, 20 Feb 2020 23:10:05 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a228bdc8e070add11170637553b04b0eeab55a8af3159561b2878b3bcc00bbb`  
		Last Modified: Thu, 20 Feb 2020 23:10:11 GMT  
		Size: 13.6 MB (13600067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:936640ed543c6bb114e0374d4aa5d00b0ad989151337d4edfe6047bad672c605`  
		Last Modified: Thu, 20 Feb 2020 23:10:05 GMT  
		Size: 2.2 KB (2214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071eed09e44daa0c7c7d337a517208fa4a3c08e02029c0970082688456496bec`  
		Last Modified: Thu, 20 Feb 2020 23:10:05 GMT  
		Size: 72.7 KB (72679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:500b89ded2f6c4841beacd80fbbc9393d964cc71bd39c391faf7dc97822dbdb9`  
		Last Modified: Thu, 20 Feb 2020 23:47:57 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512f9b08d8b23f60cb6dff75b2270418b1aef35536dd655abbebc984b88a251b`  
		Last Modified: Thu, 20 Feb 2020 23:47:58 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c471a8e9c45607043e4014b7f0974b76407454a97e750d9055d0aa5e834e6739`  
		Last Modified: Thu, 20 Feb 2020 23:47:56 GMT  
		Size: 1.2 MB (1234698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7b673bbf243a89365a23ad683cd4498bf6d1d0ed02684c8a18d0a21cb8d178`  
		Last Modified: Thu, 20 Feb 2020 23:47:55 GMT  
		Size: 120.1 KB (120109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c24ab3064784c4410d659ea6e1f0df253d4425d982dc6458c3a3ba583e9b8ec5`  
		Last Modified: Thu, 20 Feb 2020 23:47:56 GMT  
		Size: 1.5 KB (1470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f98dd355d60f4139fe6bc5acd57c5dddf79d2130ae3198cc94d132632d3727`  
		Last Modified: Thu, 20 Feb 2020 23:47:56 GMT  
		Size: 570.8 KB (570766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9027f8cb6506a233c5d6eee529c13558fd054e963701cb92c8151588f40361cb`  
		Last Modified: Thu, 20 Feb 2020 23:47:55 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; arm variant v7

```console
$ docker pull adminer@sha256:46b5ed40565812c4e0553a75ca1a4b5bffb897b489e88cb69626a97bb5de6a91
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.6 MB (28569758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f180ec2391291be9bea6f1f484659a40aa29806d769cebcb326e9b3da944208`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Sat, 18 Jan 2020 05:22:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 05:22:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 05:22:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 05:22:49 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 20 Feb 2020 21:11:31 GMT
ENV PHP_VERSION=7.4.3
# Thu, 20 Feb 2020 21:11:32 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.3.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.3.tar.xz.asc/from/this/mirror
# Thu, 20 Feb 2020 21:11:32 GMT
ENV PHP_SHA256=cf1f856d877c268124ded1ede40c9fb6142b125fdaafdc54f855120b8bc6982a PHP_MD5=
# Thu, 20 Feb 2020 21:11:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Feb 2020 21:11:37 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Feb 2020 21:13:57 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 20 Feb 2020 21:13:59 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 20 Feb 2020 21:14:01 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Feb 2020 21:14:02 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Feb 2020 21:14:02 GMT
CMD ["php" "-a"]
# Thu, 20 Feb 2020 23:50:58 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Thu, 20 Feb 2020 23:50:58 GMT
STOPSIGNAL SIGINT
# Thu, 20 Feb 2020 23:51:00 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 20 Feb 2020 23:51:02 GMT
WORKDIR /var/www/html
# Thu, 20 Feb 2020 23:51:04 GMT
RUN apk add --no-cache libpq
# Thu, 20 Feb 2020 23:51:35 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Thu, 20 Feb 2020 23:51:36 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Thu, 20 Feb 2020 23:51:37 GMT
ENV ADMINER_VERSION=4.7.6
# Thu, 20 Feb 2020 23:51:38 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Thu, 20 Feb 2020 23:51:39 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Thu, 20 Feb 2020 23:51:42 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Thu, 20 Feb 2020 23:51:43 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 20 Feb 2020 23:51:44 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Thu, 20 Feb 2020 23:51:45 GMT
USER adminer
# Thu, 20 Feb 2020 23:51:46 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 20 Feb 2020 23:51:47 GMT
EXPOSE 8080
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
	-	`sha256:6c492689366599e65cb0add947004a2dba1350bb15c7e6d5cf0926aba55ce6ec`  
		Last Modified: Thu, 20 Feb 2020 23:26:18 GMT  
		Size: 10.3 MB (10280256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e5617623e9ad0a01e633e336a37f6ff4d4a71c6cb1277692357d52303452d2f`  
		Last Modified: Thu, 20 Feb 2020 23:26:17 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4302d0c4f38943fda60770816f7eba1edb1d2f6a0c6f489e97ba67d9bdad574`  
		Last Modified: Thu, 20 Feb 2020 23:26:22 GMT  
		Size: 12.8 MB (12751449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc244875b6924b539df26879b4496e91b8eee4f5000e1ea5b774d83b9546b93`  
		Last Modified: Thu, 20 Feb 2020 23:26:18 GMT  
		Size: 2.2 KB (2214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04543010f9cd746143ced265c7b4b63d09ddc611588a131cbafe2099993fb5eb`  
		Last Modified: Thu, 20 Feb 2020 23:26:17 GMT  
		Size: 72.7 KB (72683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccb0170041c03fedc1121c07c7a06ee726f8a727c7c1eb5af04d1ee8f5654d5`  
		Last Modified: Thu, 20 Feb 2020 23:53:18 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1581d0fa71215a6ef8bb771f93fa001d361b8a02c3976b035408c6846e18be`  
		Last Modified: Thu, 20 Feb 2020 23:53:18 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f10e2f522b5d5b3116470d1761f55ab3feeb58372a087e3f6e80ea4f8f9dce7`  
		Last Modified: Thu, 20 Feb 2020 23:53:16 GMT  
		Size: 1.1 MB (1124902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c7b2368289baa2b3bc92adf31146c857cd78eecc8908bc78513c4f768c50323`  
		Last Modified: Thu, 20 Feb 2020 23:53:16 GMT  
		Size: 115.0 KB (114953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:765ac7cdcb3c5567be3929620bd1b2714a2af370ad604183f149ad40b19fd29c`  
		Last Modified: Thu, 20 Feb 2020 23:53:16 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45fe2c562cb0866875f0499d9583698863ee29b34a5a94406a42202b70885f6f`  
		Last Modified: Thu, 20 Feb 2020 23:53:16 GMT  
		Size: 570.8 KB (570772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e31dee670440ee2efcb54b84d9b9acccc709250fcb875c7ab9f31b21aded9fc`  
		Last Modified: Thu, 20 Feb 2020 23:53:16 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:d6ac77d178d83433a94f4c1ac85d37eb6bde9a3b5e2ddd70510ab8366580d72d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 MB (30795142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59720519dbc2aaa04f42da6be01d883724212b4503025e14148efe901e90b553`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Sat, 18 Jan 2020 02:29:26 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 02:29:26 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 02:29:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 02:29:29 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 24 Jan 2020 00:09:58 GMT
ENV PHP_VERSION=7.4.2
# Fri, 24 Jan 2020 00:10:02 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.2.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.2.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 00:10:03 GMT
ENV PHP_SHA256=98284deac017da0d426117ecae7599a1f1bf62ae3911e8bc16c4403a8f4bdf13 PHP_MD5=
# Fri, 24 Jan 2020 00:10:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 24 Jan 2020 00:10:10 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 00:14:01 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 00:14:05 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Fri, 24 Jan 2020 00:14:09 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 00:14:10 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 00:14:11 GMT
CMD ["php" "-a"]
# Fri, 24 Jan 2020 02:50:27 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 24 Jan 2020 02:50:28 GMT
STOPSIGNAL SIGINT
# Fri, 24 Jan 2020 02:50:32 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 24 Jan 2020 02:50:32 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 02:50:36 GMT
RUN apk add --no-cache libpq
# Fri, 24 Jan 2020 02:51:09 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Fri, 24 Jan 2020 02:51:10 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 31 Jan 2020 17:39:37 GMT
ENV ADMINER_VERSION=4.7.6
# Fri, 31 Jan 2020 17:39:37 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Fri, 31 Jan 2020 17:39:38 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Fri, 31 Jan 2020 17:39:40 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 31 Jan 2020 17:39:41 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 31 Jan 2020 17:39:42 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 31 Jan 2020 17:39:42 GMT
USER adminer
# Fri, 31 Jan 2020 17:39:43 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 31 Jan 2020 17:39:44 GMT
EXPOSE 8080
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
	-	`sha256:aa724be546925194dbbb305717c1ec1404bd825d4e768f5fa30758fc836a1dda`  
		Last Modified: Fri, 24 Jan 2020 02:37:49 GMT  
		Size: 10.3 MB (10271109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b0bc8c61926931859ef4bf710fb73b709a407ca1086dfe704e7654934b4bdd`  
		Last Modified: Fri, 24 Jan 2020 02:37:45 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07be412705d63c11275e2018adae846b8861d4f678a21f2c43e2c22ae0bcee6d`  
		Last Modified: Fri, 24 Jan 2020 02:37:49 GMT  
		Size: 14.4 MB (14366228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73cafd3dde7ad30752409223dc0b26b0a5f4fa98d9a875225e2566bd99806655`  
		Last Modified: Fri, 24 Jan 2020 02:37:45 GMT  
		Size: 2.2 KB (2216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59195632759b7e9a57fb9ac253284ecbea9055d01c12f9caa49d23ca8f40bc1c`  
		Last Modified: Fri, 24 Jan 2020 02:37:45 GMT  
		Size: 72.7 KB (72676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6576a2f957338815a3fd8d1023a31cbb8ef8592406942ab75483b02adbe1c384`  
		Last Modified: Fri, 24 Jan 2020 02:52:47 GMT  
		Size: 310.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f6446e74a0df8b21f4f9ad86cf10fa3f6b6a9231d643d4174a5ddd3cf84f184`  
		Last Modified: Fri, 24 Jan 2020 02:52:47 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b69655ccf3f62cf1149958c93543bc91f9addef901545f4c74831b5c65b29039`  
		Last Modified: Fri, 24 Jan 2020 02:52:44 GMT  
		Size: 1.3 MB (1299236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:986406fbe9d0af0aeacc6c7cc032415d7552b4fd8f3fe60ea2313caa9193649c`  
		Last Modified: Fri, 24 Jan 2020 02:52:44 GMT  
		Size: 124.7 KB (124696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:382b47ced56d800090d03dff8f4d1183a7209bfd39013db12812d2efc2a39f54`  
		Last Modified: Fri, 24 Jan 2020 02:52:44 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23f30f175d57f1ffdc2f5c4308d886c2f842ce1a163c77b1747b628a89684ac`  
		Last Modified: Fri, 31 Jan 2020 17:40:10 GMT  
		Size: 570.8 KB (570779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d5044dac86a165d99ffacf0aaeb789461f31935ef0847d4e80ae612f101599`  
		Last Modified: Fri, 31 Jan 2020 17:40:10 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; 386

```console
$ docker pull adminer@sha256:d094fa6fd940847cd20c8dd698284d004cf1d6a5fa23d777f0b19667afa76346
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31684075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed77c13afb1993912752a1a0383da2185144a458fde112b713496146d193cb19`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Sat, 18 Jan 2020 05:41:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 05:41:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 05:41:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 05:41:39 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 23 Jan 2020 23:13:49 GMT
ENV PHP_VERSION=7.4.2
# Thu, 23 Jan 2020 23:13:49 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.2.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.2.tar.xz.asc/from/this/mirror
# Thu, 23 Jan 2020 23:13:49 GMT
ENV PHP_SHA256=98284deac017da0d426117ecae7599a1f1bf62ae3911e8bc16c4403a8f4bdf13 PHP_MD5=
# Thu, 23 Jan 2020 23:13:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 23 Jan 2020 23:13:52 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Jan 2020 23:21:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 23 Jan 2020 23:21:57 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 23 Jan 2020 23:21:59 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Jan 2020 23:21:59 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Jan 2020 23:22:00 GMT
CMD ["php" "-a"]
# Fri, 24 Jan 2020 07:25:41 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 24 Jan 2020 07:25:41 GMT
STOPSIGNAL SIGINT
# Fri, 24 Jan 2020 07:25:42 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 24 Jan 2020 07:25:42 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 07:25:43 GMT
RUN apk add --no-cache libpq
# Fri, 24 Jan 2020 07:26:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Fri, 24 Jan 2020 07:26:02 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 31 Jan 2020 17:38:17 GMT
ENV ADMINER_VERSION=4.7.6
# Fri, 31 Jan 2020 17:38:18 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Fri, 31 Jan 2020 17:38:18 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Fri, 31 Jan 2020 17:38:19 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 31 Jan 2020 17:38:19 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 31 Jan 2020 17:38:20 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 31 Jan 2020 17:38:20 GMT
USER adminer
# Fri, 31 Jan 2020 17:38:20 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 31 Jan 2020 17:38:20 GMT
EXPOSE 8080
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
	-	`sha256:9f3628b223c4b093cf7c2d7723ccd39dfcb6977a659c9c183e7673f22f44865b`  
		Last Modified: Fri, 24 Jan 2020 02:36:11 GMT  
		Size: 10.3 MB (10271099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e167c61f346105deafdbe6bff7f521715a3d31cd4c9ca27d6dca67654d916c`  
		Last Modified: Fri, 24 Jan 2020 02:36:08 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53425617927914b1561c930b3ce2f90644de41394e731ca71a5d66feeba55d5b`  
		Last Modified: Fri, 24 Jan 2020 02:36:19 GMT  
		Size: 15.0 MB (14974599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809347a8b4ae69caee1b666ac61ec86e0f2dd5d64744592a59f65fd9bb49c7c9`  
		Last Modified: Fri, 24 Jan 2020 02:36:10 GMT  
		Size: 2.2 KB (2216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31917077d16c99b9c58e44f9267cbda55763d759a59379d7e4ca1f9fd6acf60a`  
		Last Modified: Fri, 24 Jan 2020 02:36:09 GMT  
		Size: 72.3 KB (72331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc6ba5ae7aae77ac94c185eef225136d01333d8840f8896b412e359fa89e3ae6`  
		Last Modified: Fri, 24 Jan 2020 07:27:19 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aab9a7fed181e4a8d1621cf6e92e6b4525a242e1c102cac7a259b3336202c16`  
		Last Modified: Fri, 24 Jan 2020 07:27:19 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1120969ea66ac41447ffffddcda8e8d389a0a1c0c7feb7d9d650117b973459d`  
		Last Modified: Fri, 24 Jan 2020 07:27:18 GMT  
		Size: 1.4 MB (1397662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cf37d29a0120ccd9ef7f4f99c6d10673cd93097ebe961c86faf275c144f5929`  
		Last Modified: Fri, 24 Jan 2020 07:27:18 GMT  
		Size: 130.8 KB (130760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf17f4f8d6baa9c93722150405686cf214bc377adbb7ff2b891efe5ca38809c9`  
		Last Modified: Fri, 24 Jan 2020 07:27:18 GMT  
		Size: 1.5 KB (1472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cac8221b3739531c0e54a60c4d8d795c187ce863f2fb79955540c1b62347fbc7`  
		Last Modified: Fri, 31 Jan 2020 17:38:36 GMT  
		Size: 570.7 KB (570691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8127a70cc3e20105c94ab16913cab965e775aaa7cb37cc6398e47d4a1830241e`  
		Last Modified: Fri, 31 Jan 2020 17:38:36 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; ppc64le

```console
$ docker pull adminer@sha256:8906a11939b6681a5c547d8a1b3d8e58493fb85a66ef14177592239c9cd3ab6f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32169343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:251a9f8c0d32635a09c63fc8d5e5fbad2fee09cca0a4ea7cca903b5d9ac6f815`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Sat, 18 Jan 2020 03:24:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:24:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:24:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 03:24:34 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 23 Jan 2020 23:32:44 GMT
ENV PHP_VERSION=7.4.2
# Thu, 23 Jan 2020 23:32:47 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.2.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.2.tar.xz.asc/from/this/mirror
# Thu, 23 Jan 2020 23:32:50 GMT
ENV PHP_SHA256=98284deac017da0d426117ecae7599a1f1bf62ae3911e8bc16c4403a8f4bdf13 PHP_MD5=
# Thu, 23 Jan 2020 23:33:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 23 Jan 2020 23:33:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Jan 2020 23:36:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 23 Jan 2020 23:36:54 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 23 Jan 2020 23:37:00 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Jan 2020 23:37:02 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Jan 2020 23:37:04 GMT
CMD ["php" "-a"]
# Fri, 24 Jan 2020 05:51:10 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 24 Jan 2020 05:51:12 GMT
STOPSIGNAL SIGINT
# Fri, 24 Jan 2020 05:51:17 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 24 Jan 2020 05:51:19 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 05:51:23 GMT
RUN apk add --no-cache libpq
# Fri, 24 Jan 2020 05:51:48 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Fri, 24 Jan 2020 05:51:50 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 31 Jan 2020 17:16:45 GMT
ENV ADMINER_VERSION=4.7.6
# Fri, 31 Jan 2020 17:16:48 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Fri, 31 Jan 2020 17:16:51 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Fri, 31 Jan 2020 17:17:00 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 31 Jan 2020 17:17:01 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 31 Jan 2020 17:17:03 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 31 Jan 2020 17:17:05 GMT
USER adminer
# Fri, 31 Jan 2020 17:17:08 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 31 Jan 2020 17:17:10 GMT
EXPOSE 8080
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
	-	`sha256:c24c1e693453ad6efa656fcfa28e76c0786f80b4467d83c277d1116117942973`  
		Last Modified: Fri, 24 Jan 2020 02:32:44 GMT  
		Size: 10.3 MB (10271124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb71fc05f0fe0d365d8b9891f304e0cf2c1f6f0d2200ecdc0ea9a1c569117a1d`  
		Last Modified: Fri, 24 Jan 2020 02:32:41 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf26116548345ee1f676a6c1fabb768cd60750eb7a3a0ac7f09724350dde3b1`  
		Last Modified: Fri, 24 Jan 2020 02:32:54 GMT  
		Size: 15.5 MB (15539990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc4f870d6f2e6bbade33c0f28534b50765c4b56a093dc7565bd3ec3b37a7c603`  
		Last Modified: Fri, 24 Jan 2020 02:32:41 GMT  
		Size: 2.2 KB (2211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6a738ee51d709e4c4db983f9206a240500a2fc0dbaf3c76f6da2f99e5f6eb3b`  
		Last Modified: Fri, 24 Jan 2020 02:32:41 GMT  
		Size: 73.0 KB (72992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47bf1b73f7bf1089b7cf019ae582b63d77fa46e6c5b2b4efc16b0bf9d9b1ad9a`  
		Last Modified: Fri, 24 Jan 2020 05:53:47 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f984dcaccfb46a5cafd49380217e97342575055ceaaab4ff65a67f43af2da028`  
		Last Modified: Fri, 24 Jan 2020 05:53:47 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9e4520026a60556f0b631a13532b9a39d91d8eae94d4d3514359ef189ce4c94`  
		Last Modified: Fri, 24 Jan 2020 05:53:45 GMT  
		Size: 1.4 MB (1350626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba57cd117c3f571c3379a3fbb16d112291f4de925499dfeaad0bc7966c9483fb`  
		Last Modified: Fri, 24 Jan 2020 05:53:44 GMT  
		Size: 135.9 KB (135919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faef1730db86976915b65b75f76c1a057c321a983034e019f37ec833f5a1ffc9`  
		Last Modified: Fri, 24 Jan 2020 05:53:44 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:620c9c1b5881ba0a3be097e7cb57c695406737868e7b1adc02c5561c5f7b1649`  
		Last Modified: Fri, 31 Jan 2020 17:18:05 GMT  
		Size: 570.8 KB (570776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03e77753eec72902172405ef4c8c0c667bf7377cd0dc6cc1441afd0890991d43`  
		Last Modified: Fri, 31 Jan 2020 17:18:04 GMT  
		Size: 501.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:standalone`

```console
$ docker pull adminer@sha256:c689401f4ee85e37ba2cd62d401af2d569833dd8efa2c338177889fa9c525882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `adminer:standalone` - linux; amd64

```console
$ docker pull adminer@sha256:6ceb642133ac56e267c50ae4bfb24ac0008b0eb02b772abae9059caa45211bee
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31058191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:259cc60bdb72538cffc06536d8bb73c3d9afd7156afc71b0c97fb1659917805e`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Sat, 18 Jan 2020 03:18:30 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:18:30 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:18:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 03:18:30 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 24 Jan 2020 07:05:12 GMT
ENV PHP_VERSION=7.4.2
# Fri, 24 Jan 2020 07:05:13 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.2.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.2.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 07:05:13 GMT
ENV PHP_SHA256=98284deac017da0d426117ecae7599a1f1bf62ae3911e8bc16c4403a8f4bdf13 PHP_MD5=
# Fri, 24 Jan 2020 07:05:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 24 Jan 2020 07:05:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 07:13:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 07:13:16 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Fri, 24 Jan 2020 07:13:17 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 07:13:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 07:13:17 GMT
CMD ["php" "-a"]
# Fri, 24 Jan 2020 10:52:17 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 24 Jan 2020 10:52:17 GMT
STOPSIGNAL SIGINT
# Fri, 24 Jan 2020 10:52:18 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 24 Jan 2020 10:52:18 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 10:52:19 GMT
RUN apk add --no-cache libpq
# Fri, 24 Jan 2020 10:52:38 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Fri, 24 Jan 2020 10:52:39 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 31 Jan 2020 17:19:26 GMT
ENV ADMINER_VERSION=4.7.6
# Fri, 31 Jan 2020 17:19:26 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Fri, 31 Jan 2020 17:19:26 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Fri, 31 Jan 2020 17:19:27 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 31 Jan 2020 17:19:28 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 31 Jan 2020 17:19:28 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 31 Jan 2020 17:19:28 GMT
USER adminer
# Fri, 31 Jan 2020 17:19:28 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 31 Jan 2020 17:19:28 GMT
EXPOSE 8080
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
	-	`sha256:5fa47f19b1e835f47f4c1273ccb215a42ee2aefafe300409d92b05b899a757d8`  
		Last Modified: Fri, 24 Jan 2020 10:39:33 GMT  
		Size: 10.3 MB (10271096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4556adb19ddcb43be3cd12b973f718e5edc74d6986ae4406a0c3011cbeb3dc93`  
		Last Modified: Fri, 24 Jan 2020 10:39:33 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:205de55b7ed0d389ac2c9777321f11ba9377a148002c2ef1d7b68d02a96472f3`  
		Last Modified: Fri, 24 Jan 2020 10:39:42 GMT  
		Size: 14.6 MB (14574023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c35aa7da966a732561c37c8b5d56949eedcb7865066b86da95c8bc58c18c48d2`  
		Last Modified: Fri, 24 Jan 2020 10:39:32 GMT  
		Size: 2.2 KB (2216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82a54ca6f814c156199e3266c4297efe2f54fb83bfb1645f53582eae3d1e222e`  
		Last Modified: Fri, 24 Jan 2020 10:39:33 GMT  
		Size: 73.1 KB (73145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e28f69f8cf7d397d8bd78cab68b9713275989e440016ec98580b94d0b0dc23f8`  
		Last Modified: Fri, 24 Jan 2020 10:53:42 GMT  
		Size: 306.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b527d0b89c2ea24dd10be7c18c1dcdf592fd4e1a5ff2c9da47fba2940fbb25a7`  
		Last Modified: Fri, 24 Jan 2020 10:53:42 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35b881820e3f1402cd2b2836dc6064db1b8ef029479448d5a058baa86b0f2e29`  
		Last Modified: Fri, 24 Jan 2020 10:53:41 GMT  
		Size: 1.3 MB (1277246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97e920225fdf7c9fc6bd8762ee3efbc9225341331c21812757347e46b22a2db3`  
		Last Modified: Fri, 24 Jan 2020 10:53:41 GMT  
		Size: 126.6 KB (126617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c8cde070aec4f16d202102cbdad6a161e48b4ffae4426da85717e9ee116fbec`  
		Last Modified: Fri, 24 Jan 2020 10:53:40 GMT  
		Size: 1.5 KB (1474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:028d5feebf26f852c8d09343a1b1ea1be953837a2f402743e1c021ea7b15ccee`  
		Last Modified: Fri, 31 Jan 2020 17:19:44 GMT  
		Size: 570.7 KB (570688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e0b9ec991cbee8b6377946c76367fcaa9782c4be8d265be834c5158b2638d40`  
		Last Modified: Fri, 31 Jan 2020 17:19:44 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:standalone` - linux; arm variant v6

```console
$ docker pull adminer@sha256:086342d4149c1554e7c334711e0c6ccfa783ce0991cdd33d1687ca56e83020c7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.8 MB (29825140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08598589c478e6d488e3d5892d914c3ccac2ca333bf32b79046b127a04438a92`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Sat, 18 Jan 2020 03:40:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:40:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:40:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 03:40:19 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 20 Feb 2020 21:49:41 GMT
ENV PHP_VERSION=7.4.3
# Thu, 20 Feb 2020 21:49:43 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.3.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.3.tar.xz.asc/from/this/mirror
# Thu, 20 Feb 2020 21:49:44 GMT
ENV PHP_SHA256=cf1f856d877c268124ded1ede40c9fb6142b125fdaafdc54f855120b8bc6982a PHP_MD5=
# Thu, 20 Feb 2020 21:49:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Feb 2020 21:49:57 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Feb 2020 21:53:47 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 20 Feb 2020 21:53:50 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 20 Feb 2020 21:53:53 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Feb 2020 21:53:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Feb 2020 21:53:54 GMT
CMD ["php" "-a"]
# Thu, 20 Feb 2020 23:45:59 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Thu, 20 Feb 2020 23:45:59 GMT
STOPSIGNAL SIGINT
# Thu, 20 Feb 2020 23:46:02 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 20 Feb 2020 23:46:03 GMT
WORKDIR /var/www/html
# Thu, 20 Feb 2020 23:46:05 GMT
RUN apk add --no-cache libpq
# Thu, 20 Feb 2020 23:46:36 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Thu, 20 Feb 2020 23:46:39 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Thu, 20 Feb 2020 23:46:41 GMT
ENV ADMINER_VERSION=4.7.6
# Thu, 20 Feb 2020 23:46:41 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Thu, 20 Feb 2020 23:46:42 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Thu, 20 Feb 2020 23:46:45 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Thu, 20 Feb 2020 23:46:46 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 20 Feb 2020 23:46:46 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Thu, 20 Feb 2020 23:46:47 GMT
USER adminer
# Thu, 20 Feb 2020 23:46:48 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 20 Feb 2020 23:46:48 GMT
EXPOSE 8080
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
	-	`sha256:f246fe8b62d43a3f633a04898577258a2ce5dd84edf5fd464403b9a108b301e2`  
		Last Modified: Thu, 20 Feb 2020 23:10:06 GMT  
		Size: 10.3 MB (10280264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b4e0af10768397859f6f19eca4b17ee9f21d61a1cb06989aba861267cf1b6a`  
		Last Modified: Thu, 20 Feb 2020 23:10:05 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a228bdc8e070add11170637553b04b0eeab55a8af3159561b2878b3bcc00bbb`  
		Last Modified: Thu, 20 Feb 2020 23:10:11 GMT  
		Size: 13.6 MB (13600067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:936640ed543c6bb114e0374d4aa5d00b0ad989151337d4edfe6047bad672c605`  
		Last Modified: Thu, 20 Feb 2020 23:10:05 GMT  
		Size: 2.2 KB (2214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071eed09e44daa0c7c7d337a517208fa4a3c08e02029c0970082688456496bec`  
		Last Modified: Thu, 20 Feb 2020 23:10:05 GMT  
		Size: 72.7 KB (72679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:500b89ded2f6c4841beacd80fbbc9393d964cc71bd39c391faf7dc97822dbdb9`  
		Last Modified: Thu, 20 Feb 2020 23:47:57 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512f9b08d8b23f60cb6dff75b2270418b1aef35536dd655abbebc984b88a251b`  
		Last Modified: Thu, 20 Feb 2020 23:47:58 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c471a8e9c45607043e4014b7f0974b76407454a97e750d9055d0aa5e834e6739`  
		Last Modified: Thu, 20 Feb 2020 23:47:56 GMT  
		Size: 1.2 MB (1234698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7b673bbf243a89365a23ad683cd4498bf6d1d0ed02684c8a18d0a21cb8d178`  
		Last Modified: Thu, 20 Feb 2020 23:47:55 GMT  
		Size: 120.1 KB (120109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c24ab3064784c4410d659ea6e1f0df253d4425d982dc6458c3a3ba583e9b8ec5`  
		Last Modified: Thu, 20 Feb 2020 23:47:56 GMT  
		Size: 1.5 KB (1470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f98dd355d60f4139fe6bc5acd57c5dddf79d2130ae3198cc94d132632d3727`  
		Last Modified: Thu, 20 Feb 2020 23:47:56 GMT  
		Size: 570.8 KB (570766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9027f8cb6506a233c5d6eee529c13558fd054e963701cb92c8151588f40361cb`  
		Last Modified: Thu, 20 Feb 2020 23:47:55 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:standalone` - linux; arm variant v7

```console
$ docker pull adminer@sha256:46b5ed40565812c4e0553a75ca1a4b5bffb897b489e88cb69626a97bb5de6a91
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.6 MB (28569758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f180ec2391291be9bea6f1f484659a40aa29806d769cebcb326e9b3da944208`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Sat, 18 Jan 2020 05:22:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 05:22:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 05:22:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 05:22:49 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 20 Feb 2020 21:11:31 GMT
ENV PHP_VERSION=7.4.3
# Thu, 20 Feb 2020 21:11:32 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.3.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.3.tar.xz.asc/from/this/mirror
# Thu, 20 Feb 2020 21:11:32 GMT
ENV PHP_SHA256=cf1f856d877c268124ded1ede40c9fb6142b125fdaafdc54f855120b8bc6982a PHP_MD5=
# Thu, 20 Feb 2020 21:11:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Feb 2020 21:11:37 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Feb 2020 21:13:57 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 20 Feb 2020 21:13:59 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 20 Feb 2020 21:14:01 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Feb 2020 21:14:02 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Feb 2020 21:14:02 GMT
CMD ["php" "-a"]
# Thu, 20 Feb 2020 23:50:58 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Thu, 20 Feb 2020 23:50:58 GMT
STOPSIGNAL SIGINT
# Thu, 20 Feb 2020 23:51:00 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 20 Feb 2020 23:51:02 GMT
WORKDIR /var/www/html
# Thu, 20 Feb 2020 23:51:04 GMT
RUN apk add --no-cache libpq
# Thu, 20 Feb 2020 23:51:35 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Thu, 20 Feb 2020 23:51:36 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Thu, 20 Feb 2020 23:51:37 GMT
ENV ADMINER_VERSION=4.7.6
# Thu, 20 Feb 2020 23:51:38 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Thu, 20 Feb 2020 23:51:39 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Thu, 20 Feb 2020 23:51:42 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Thu, 20 Feb 2020 23:51:43 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 20 Feb 2020 23:51:44 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Thu, 20 Feb 2020 23:51:45 GMT
USER adminer
# Thu, 20 Feb 2020 23:51:46 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 20 Feb 2020 23:51:47 GMT
EXPOSE 8080
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
	-	`sha256:6c492689366599e65cb0add947004a2dba1350bb15c7e6d5cf0926aba55ce6ec`  
		Last Modified: Thu, 20 Feb 2020 23:26:18 GMT  
		Size: 10.3 MB (10280256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e5617623e9ad0a01e633e336a37f6ff4d4a71c6cb1277692357d52303452d2f`  
		Last Modified: Thu, 20 Feb 2020 23:26:17 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4302d0c4f38943fda60770816f7eba1edb1d2f6a0c6f489e97ba67d9bdad574`  
		Last Modified: Thu, 20 Feb 2020 23:26:22 GMT  
		Size: 12.8 MB (12751449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc244875b6924b539df26879b4496e91b8eee4f5000e1ea5b774d83b9546b93`  
		Last Modified: Thu, 20 Feb 2020 23:26:18 GMT  
		Size: 2.2 KB (2214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04543010f9cd746143ced265c7b4b63d09ddc611588a131cbafe2099993fb5eb`  
		Last Modified: Thu, 20 Feb 2020 23:26:17 GMT  
		Size: 72.7 KB (72683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccb0170041c03fedc1121c07c7a06ee726f8a727c7c1eb5af04d1ee8f5654d5`  
		Last Modified: Thu, 20 Feb 2020 23:53:18 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1581d0fa71215a6ef8bb771f93fa001d361b8a02c3976b035408c6846e18be`  
		Last Modified: Thu, 20 Feb 2020 23:53:18 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f10e2f522b5d5b3116470d1761f55ab3feeb58372a087e3f6e80ea4f8f9dce7`  
		Last Modified: Thu, 20 Feb 2020 23:53:16 GMT  
		Size: 1.1 MB (1124902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c7b2368289baa2b3bc92adf31146c857cd78eecc8908bc78513c4f768c50323`  
		Last Modified: Thu, 20 Feb 2020 23:53:16 GMT  
		Size: 115.0 KB (114953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:765ac7cdcb3c5567be3929620bd1b2714a2af370ad604183f149ad40b19fd29c`  
		Last Modified: Thu, 20 Feb 2020 23:53:16 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45fe2c562cb0866875f0499d9583698863ee29b34a5a94406a42202b70885f6f`  
		Last Modified: Thu, 20 Feb 2020 23:53:16 GMT  
		Size: 570.8 KB (570772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e31dee670440ee2efcb54b84d9b9acccc709250fcb875c7ab9f31b21aded9fc`  
		Last Modified: Thu, 20 Feb 2020 23:53:16 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:standalone` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:d6ac77d178d83433a94f4c1ac85d37eb6bde9a3b5e2ddd70510ab8366580d72d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 MB (30795142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59720519dbc2aaa04f42da6be01d883724212b4503025e14148efe901e90b553`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Sat, 18 Jan 2020 02:29:26 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 02:29:26 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 02:29:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 02:29:29 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 24 Jan 2020 00:09:58 GMT
ENV PHP_VERSION=7.4.2
# Fri, 24 Jan 2020 00:10:02 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.2.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.2.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 00:10:03 GMT
ENV PHP_SHA256=98284deac017da0d426117ecae7599a1f1bf62ae3911e8bc16c4403a8f4bdf13 PHP_MD5=
# Fri, 24 Jan 2020 00:10:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 24 Jan 2020 00:10:10 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 00:14:01 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 00:14:05 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Fri, 24 Jan 2020 00:14:09 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 00:14:10 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 00:14:11 GMT
CMD ["php" "-a"]
# Fri, 24 Jan 2020 02:50:27 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 24 Jan 2020 02:50:28 GMT
STOPSIGNAL SIGINT
# Fri, 24 Jan 2020 02:50:32 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 24 Jan 2020 02:50:32 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 02:50:36 GMT
RUN apk add --no-cache libpq
# Fri, 24 Jan 2020 02:51:09 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Fri, 24 Jan 2020 02:51:10 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 31 Jan 2020 17:39:37 GMT
ENV ADMINER_VERSION=4.7.6
# Fri, 31 Jan 2020 17:39:37 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Fri, 31 Jan 2020 17:39:38 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Fri, 31 Jan 2020 17:39:40 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 31 Jan 2020 17:39:41 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 31 Jan 2020 17:39:42 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 31 Jan 2020 17:39:42 GMT
USER adminer
# Fri, 31 Jan 2020 17:39:43 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 31 Jan 2020 17:39:44 GMT
EXPOSE 8080
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
	-	`sha256:aa724be546925194dbbb305717c1ec1404bd825d4e768f5fa30758fc836a1dda`  
		Last Modified: Fri, 24 Jan 2020 02:37:49 GMT  
		Size: 10.3 MB (10271109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b0bc8c61926931859ef4bf710fb73b709a407ca1086dfe704e7654934b4bdd`  
		Last Modified: Fri, 24 Jan 2020 02:37:45 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07be412705d63c11275e2018adae846b8861d4f678a21f2c43e2c22ae0bcee6d`  
		Last Modified: Fri, 24 Jan 2020 02:37:49 GMT  
		Size: 14.4 MB (14366228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73cafd3dde7ad30752409223dc0b26b0a5f4fa98d9a875225e2566bd99806655`  
		Last Modified: Fri, 24 Jan 2020 02:37:45 GMT  
		Size: 2.2 KB (2216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59195632759b7e9a57fb9ac253284ecbea9055d01c12f9caa49d23ca8f40bc1c`  
		Last Modified: Fri, 24 Jan 2020 02:37:45 GMT  
		Size: 72.7 KB (72676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6576a2f957338815a3fd8d1023a31cbb8ef8592406942ab75483b02adbe1c384`  
		Last Modified: Fri, 24 Jan 2020 02:52:47 GMT  
		Size: 310.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f6446e74a0df8b21f4f9ad86cf10fa3f6b6a9231d643d4174a5ddd3cf84f184`  
		Last Modified: Fri, 24 Jan 2020 02:52:47 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b69655ccf3f62cf1149958c93543bc91f9addef901545f4c74831b5c65b29039`  
		Last Modified: Fri, 24 Jan 2020 02:52:44 GMT  
		Size: 1.3 MB (1299236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:986406fbe9d0af0aeacc6c7cc032415d7552b4fd8f3fe60ea2313caa9193649c`  
		Last Modified: Fri, 24 Jan 2020 02:52:44 GMT  
		Size: 124.7 KB (124696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:382b47ced56d800090d03dff8f4d1183a7209bfd39013db12812d2efc2a39f54`  
		Last Modified: Fri, 24 Jan 2020 02:52:44 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23f30f175d57f1ffdc2f5c4308d886c2f842ce1a163c77b1747b628a89684ac`  
		Last Modified: Fri, 31 Jan 2020 17:40:10 GMT  
		Size: 570.8 KB (570779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d5044dac86a165d99ffacf0aaeb789461f31935ef0847d4e80ae612f101599`  
		Last Modified: Fri, 31 Jan 2020 17:40:10 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:standalone` - linux; 386

```console
$ docker pull adminer@sha256:d094fa6fd940847cd20c8dd698284d004cf1d6a5fa23d777f0b19667afa76346
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31684075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed77c13afb1993912752a1a0383da2185144a458fde112b713496146d193cb19`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Sat, 18 Jan 2020 05:41:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 05:41:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 05:41:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 05:41:39 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 23 Jan 2020 23:13:49 GMT
ENV PHP_VERSION=7.4.2
# Thu, 23 Jan 2020 23:13:49 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.2.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.2.tar.xz.asc/from/this/mirror
# Thu, 23 Jan 2020 23:13:49 GMT
ENV PHP_SHA256=98284deac017da0d426117ecae7599a1f1bf62ae3911e8bc16c4403a8f4bdf13 PHP_MD5=
# Thu, 23 Jan 2020 23:13:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 23 Jan 2020 23:13:52 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Jan 2020 23:21:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 23 Jan 2020 23:21:57 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 23 Jan 2020 23:21:59 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Jan 2020 23:21:59 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Jan 2020 23:22:00 GMT
CMD ["php" "-a"]
# Fri, 24 Jan 2020 07:25:41 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 24 Jan 2020 07:25:41 GMT
STOPSIGNAL SIGINT
# Fri, 24 Jan 2020 07:25:42 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 24 Jan 2020 07:25:42 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 07:25:43 GMT
RUN apk add --no-cache libpq
# Fri, 24 Jan 2020 07:26:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Fri, 24 Jan 2020 07:26:02 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 31 Jan 2020 17:38:17 GMT
ENV ADMINER_VERSION=4.7.6
# Fri, 31 Jan 2020 17:38:18 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Fri, 31 Jan 2020 17:38:18 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Fri, 31 Jan 2020 17:38:19 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 31 Jan 2020 17:38:19 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 31 Jan 2020 17:38:20 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 31 Jan 2020 17:38:20 GMT
USER adminer
# Fri, 31 Jan 2020 17:38:20 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 31 Jan 2020 17:38:20 GMT
EXPOSE 8080
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
	-	`sha256:9f3628b223c4b093cf7c2d7723ccd39dfcb6977a659c9c183e7673f22f44865b`  
		Last Modified: Fri, 24 Jan 2020 02:36:11 GMT  
		Size: 10.3 MB (10271099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e167c61f346105deafdbe6bff7f521715a3d31cd4c9ca27d6dca67654d916c`  
		Last Modified: Fri, 24 Jan 2020 02:36:08 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53425617927914b1561c930b3ce2f90644de41394e731ca71a5d66feeba55d5b`  
		Last Modified: Fri, 24 Jan 2020 02:36:19 GMT  
		Size: 15.0 MB (14974599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809347a8b4ae69caee1b666ac61ec86e0f2dd5d64744592a59f65fd9bb49c7c9`  
		Last Modified: Fri, 24 Jan 2020 02:36:10 GMT  
		Size: 2.2 KB (2216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31917077d16c99b9c58e44f9267cbda55763d759a59379d7e4ca1f9fd6acf60a`  
		Last Modified: Fri, 24 Jan 2020 02:36:09 GMT  
		Size: 72.3 KB (72331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc6ba5ae7aae77ac94c185eef225136d01333d8840f8896b412e359fa89e3ae6`  
		Last Modified: Fri, 24 Jan 2020 07:27:19 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aab9a7fed181e4a8d1621cf6e92e6b4525a242e1c102cac7a259b3336202c16`  
		Last Modified: Fri, 24 Jan 2020 07:27:19 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1120969ea66ac41447ffffddcda8e8d389a0a1c0c7feb7d9d650117b973459d`  
		Last Modified: Fri, 24 Jan 2020 07:27:18 GMT  
		Size: 1.4 MB (1397662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cf37d29a0120ccd9ef7f4f99c6d10673cd93097ebe961c86faf275c144f5929`  
		Last Modified: Fri, 24 Jan 2020 07:27:18 GMT  
		Size: 130.8 KB (130760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf17f4f8d6baa9c93722150405686cf214bc377adbb7ff2b891efe5ca38809c9`  
		Last Modified: Fri, 24 Jan 2020 07:27:18 GMT  
		Size: 1.5 KB (1472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cac8221b3739531c0e54a60c4d8d795c187ce863f2fb79955540c1b62347fbc7`  
		Last Modified: Fri, 31 Jan 2020 17:38:36 GMT  
		Size: 570.7 KB (570691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8127a70cc3e20105c94ab16913cab965e775aaa7cb37cc6398e47d4a1830241e`  
		Last Modified: Fri, 31 Jan 2020 17:38:36 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:standalone` - linux; ppc64le

```console
$ docker pull adminer@sha256:8906a11939b6681a5c547d8a1b3d8e58493fb85a66ef14177592239c9cd3ab6f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32169343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:251a9f8c0d32635a09c63fc8d5e5fbad2fee09cca0a4ea7cca903b5d9ac6f815`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Sat, 18 Jan 2020 03:24:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:24:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Jan 2020 03:24:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 18 Jan 2020 03:24:34 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 23 Jan 2020 23:32:44 GMT
ENV PHP_VERSION=7.4.2
# Thu, 23 Jan 2020 23:32:47 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.2.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.2.tar.xz.asc/from/this/mirror
# Thu, 23 Jan 2020 23:32:50 GMT
ENV PHP_SHA256=98284deac017da0d426117ecae7599a1f1bf62ae3911e8bc16c4403a8f4bdf13 PHP_MD5=
# Thu, 23 Jan 2020 23:33:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 23 Jan 2020 23:33:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Jan 2020 23:36:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 23 Jan 2020 23:36:54 GMT
COPY multi:0b7e4a1b9cd5748d214539db3c6bee9b30805d1933690492830b56ffcd31f68d in /usr/local/bin/ 
# Thu, 23 Jan 2020 23:37:00 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Jan 2020 23:37:02 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Jan 2020 23:37:04 GMT
CMD ["php" "-a"]
# Fri, 24 Jan 2020 05:51:10 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 24 Jan 2020 05:51:12 GMT
STOPSIGNAL SIGINT
# Fri, 24 Jan 2020 05:51:17 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 24 Jan 2020 05:51:19 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 05:51:23 GMT
RUN apk add --no-cache libpq
# Fri, 24 Jan 2020 05:51:48 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev &&	docker-php-ext-install pdo_mysql pdo_pgsql pdo_sqlite &&	apk del .build-deps
# Fri, 24 Jan 2020 05:51:50 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 31 Jan 2020 17:16:45 GMT
ENV ADMINER_VERSION=4.7.6
# Fri, 31 Jan 2020 17:16:48 GMT
ENV ADMINER_DOWNLOAD_SHA256=78f718f3b60faa1d1765af6c0010465f8d780fcaf8990a9e9223ce9c716de2d2
# Fri, 31 Jan 2020 17:16:51 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=d1fafc6090ca1c1b2f350a5872af0d397f7eed96f34ab829ef859405aab90618
# Fri, 31 Jan 2020 17:17:00 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 31 Jan 2020 17:17:01 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 31 Jan 2020 17:17:03 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 31 Jan 2020 17:17:05 GMT
USER adminer
# Fri, 31 Jan 2020 17:17:08 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 31 Jan 2020 17:17:10 GMT
EXPOSE 8080
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
	-	`sha256:c24c1e693453ad6efa656fcfa28e76c0786f80b4467d83c277d1116117942973`  
		Last Modified: Fri, 24 Jan 2020 02:32:44 GMT  
		Size: 10.3 MB (10271124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb71fc05f0fe0d365d8b9891f304e0cf2c1f6f0d2200ecdc0ea9a1c569117a1d`  
		Last Modified: Fri, 24 Jan 2020 02:32:41 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf26116548345ee1f676a6c1fabb768cd60750eb7a3a0ac7f09724350dde3b1`  
		Last Modified: Fri, 24 Jan 2020 02:32:54 GMT  
		Size: 15.5 MB (15539990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc4f870d6f2e6bbade33c0f28534b50765c4b56a093dc7565bd3ec3b37a7c603`  
		Last Modified: Fri, 24 Jan 2020 02:32:41 GMT  
		Size: 2.2 KB (2211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6a738ee51d709e4c4db983f9206a240500a2fc0dbaf3c76f6da2f99e5f6eb3b`  
		Last Modified: Fri, 24 Jan 2020 02:32:41 GMT  
		Size: 73.0 KB (72992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47bf1b73f7bf1089b7cf019ae582b63d77fa46e6c5b2b4efc16b0bf9d9b1ad9a`  
		Last Modified: Fri, 24 Jan 2020 05:53:47 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f984dcaccfb46a5cafd49380217e97342575055ceaaab4ff65a67f43af2da028`  
		Last Modified: Fri, 24 Jan 2020 05:53:47 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9e4520026a60556f0b631a13532b9a39d91d8eae94d4d3514359ef189ce4c94`  
		Last Modified: Fri, 24 Jan 2020 05:53:45 GMT  
		Size: 1.4 MB (1350626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba57cd117c3f571c3379a3fbb16d112291f4de925499dfeaad0bc7966c9483fb`  
		Last Modified: Fri, 24 Jan 2020 05:53:44 GMT  
		Size: 135.9 KB (135919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faef1730db86976915b65b75f76c1a057c321a983034e019f37ec833f5a1ffc9`  
		Last Modified: Fri, 24 Jan 2020 05:53:44 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:620c9c1b5881ba0a3be097e7cb57c695406737868e7b1adc02c5561c5f7b1649`  
		Last Modified: Fri, 31 Jan 2020 17:18:05 GMT  
		Size: 570.8 KB (570776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03e77753eec72902172405ef4c8c0c667bf7377cd0dc6cc1441afd0890991d43`  
		Last Modified: Fri, 31 Jan 2020 17:18:04 GMT  
		Size: 501.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
