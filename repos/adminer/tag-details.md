<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `adminer`

-	[`adminer:4`](#adminer4)
-	[`adminer:4.7`](#adminer47)
-	[`adminer:4.7.8`](#adminer478)
-	[`adminer:4.7.8-fastcgi`](#adminer478-fastcgi)
-	[`adminer:4.7.8-standalone`](#adminer478-standalone)
-	[`adminer:4.7-fastcgi`](#adminer47-fastcgi)
-	[`adminer:4.7-standalone`](#adminer47-standalone)
-	[`adminer:4-fastcgi`](#adminer4-fastcgi)
-	[`adminer:4-standalone`](#adminer4-standalone)
-	[`adminer:fastcgi`](#adminerfastcgi)
-	[`adminer:latest`](#adminerlatest)
-	[`adminer:standalone`](#adminerstandalone)

## `adminer:4`

```console
$ docker pull adminer@sha256:4600f2453f7c9f3ee8179016a65d0b49a8dfb89467ac0947a6245e62e7f81fb1
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

### `adminer:4` - linux; amd64

```console
$ docker pull adminer@sha256:4b087576de7b4ca7c60bb3558f0b5ee30f496cee10fa19ea0a9f0e071c72b1f5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (33965375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2db7241b0f1461d8707525832e608fe513453f99c11beed9413194f7519e05`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 06:30:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 22 Oct 2020 06:30:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 22 Oct 2020 06:30:15 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 22 Oct 2020 06:30:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 22 Oct 2020 06:30:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 22 Oct 2020 06:30:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 06:30:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 06:30:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 22 Oct 2020 06:43:41 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 01 Dec 2020 04:36:20 GMT
ENV PHP_VERSION=7.4.13
# Tue, 01 Dec 2020 04:36:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Tue, 01 Dec 2020 04:36:21 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Tue, 01 Dec 2020 04:36:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 01 Dec 2020 04:36:27 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 01 Dec 2020 04:44:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 01 Dec 2020 04:44:54 GMT
COPY multi:afab483600631d4d87fe030871bbb016f1c2b73c0b72609d857bace419af7f5d in /usr/local/bin/ 
# Tue, 01 Dec 2020 04:44:57 GMT
RUN docker-php-ext-enable sodium
# Tue, 01 Dec 2020 04:44:57 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 01 Dec 2020 04:44:57 GMT
CMD ["php" "-a"]
# Tue, 01 Dec 2020 07:46:46 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Tue, 01 Dec 2020 07:46:46 GMT
STOPSIGNAL SIGINT
# Tue, 01 Dec 2020 07:46:47 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 01 Dec 2020 07:46:48 GMT
WORKDIR /var/www/html
# Tue, 01 Dec 2020 07:47:15 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Tue, 01 Dec 2020 07:47:15 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Tue, 08 Dec 2020 00:19:24 GMT
ENV ADMINER_VERSION=4.7.8
# Tue, 08 Dec 2020 00:19:24 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Tue, 08 Dec 2020 00:19:24 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Tue, 08 Dec 2020 00:19:26 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Tue, 08 Dec 2020 00:19:26 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 08 Dec 2020 00:19:26 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Tue, 08 Dec 2020 00:19:26 GMT
USER adminer
# Tue, 08 Dec 2020 00:19:27 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 08 Dec 2020 00:19:27 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f8bf6cfdbe614fef94f982905079c16e27b3de2d24eb1ff513d3d83e656ca2`  
		Last Modified: Thu, 22 Oct 2020 07:36:55 GMT  
		Size: 1.3 MB (1340771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce5be79740125b9e74a77885bf6ee2b0d25ac7ed9e9432c5aa7210bb3b00458a`  
		Last Modified: Thu, 22 Oct 2020 07:36:55 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99dd6507fe563b66ba35badf706e1bbb2d39eb5d0a3c0d5a86a45d2af7e89c1`  
		Last Modified: Thu, 22 Oct 2020 07:36:55 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c513a1b503cf7c9f18fa014dada9744070ded92dc9ad548cd056c4f56dc1a9`  
		Last Modified: Tue, 01 Dec 2020 07:27:10 GMT  
		Size: 10.3 MB (10338569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff080eafb4c0518981fca6aef4d239863fc59195f41ce7c440b2c6c518f2ac79`  
		Last Modified: Tue, 01 Dec 2020 07:27:09 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e818119992b11dbf09b710066a78920985b9ea1310fc8272df816e0884985f44`  
		Last Modified: Tue, 01 Dec 2020 07:27:13 GMT  
		Size: 14.6 MB (14572037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba3c14a67f95ae52ebfb558ab6b5d87687a05ce41c8df0a618ff42b73204e40`  
		Last Modified: Tue, 01 Dec 2020 07:27:09 GMT  
		Size: 2.3 KB (2257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbb0285b7ad2b170e4ed2cffbe0f16ba55d689c056ff43767834783eab7b8261`  
		Last Modified: Tue, 01 Dec 2020 07:27:09 GMT  
		Size: 17.0 KB (16987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae324cfad8acf03b3a98a15e963b7046404a7da3a6bbf68fd65d37f899f194d`  
		Last Modified: Tue, 01 Dec 2020 07:48:25 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb51158f683d66315de6fa572f7ea13d8ffb71ac85faa20c8578edb11678f37d`  
		Last Modified: Tue, 01 Dec 2020 07:48:23 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71ac21b64d1d63d967acb13664404babd0ef86fc896c484ce28cccf70001d0f1`  
		Last Modified: Tue, 01 Dec 2020 07:48:24 GMT  
		Size: 4.3 MB (4321455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2170e09d39d861e9bb7a5da5def906b44153b6c481fe17925ba82d1f1f78eec`  
		Last Modified: Tue, 01 Dec 2020 07:48:24 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d95b48dfa11f7f5c061f6522f6ff5d574452b8f321c6075455da2643b1967a`  
		Last Modified: Tue, 08 Dec 2020 00:19:45 GMT  
		Size: 570.9 KB (570860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3bb2b5e72bf0dbd4b855ddf65aaf9c0d077703804bdbdc9ea3ea98cbbfceaf6`  
		Last Modified: Tue, 08 Dec 2020 00:19:44 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4` - linux; arm variant v6

```console
$ docker pull adminer@sha256:7e114494e5e3a8ece382083d27c33f6c993695f0ff6c92c235ced149177f5da9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32073857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9cfa5ccbab063435267257cf4c761402c956233cf22775ed1c774b53a045715`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 11 Dec 2020 02:17:15 GMT
ADD file:1a9c0a67560d338c0c0e7005d8915d998fc9cf3e9f53bfd7e42e8391f0a39bce in / 
# Fri, 11 Dec 2020 02:17:15 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 07:04:50 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 11 Dec 2020 07:04:53 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 11 Dec 2020 07:04:55 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 11 Dec 2020 07:04:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 11 Dec 2020 07:04:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 11 Dec 2020 07:05:00 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Dec 2020 07:05:01 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Dec 2020 07:05:02 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 11 Dec 2020 07:13:50 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 11 Dec 2020 07:13:54 GMT
ENV PHP_VERSION=7.4.13
# Fri, 11 Dec 2020 07:13:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Fri, 11 Dec 2020 07:13:56 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Fri, 11 Dec 2020 07:14:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 11 Dec 2020 07:14:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Dec 2020 07:17:37 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Dec 2020 07:17:39 GMT
COPY multi:afab483600631d4d87fe030871bbb016f1c2b73c0b72609d857bace419af7f5d in /usr/local/bin/ 
# Fri, 11 Dec 2020 07:17:42 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Dec 2020 07:17:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Dec 2020 07:17:43 GMT
CMD ["php" "-a"]
# Fri, 11 Dec 2020 09:04:18 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 11 Dec 2020 09:04:19 GMT
STOPSIGNAL SIGINT
# Fri, 11 Dec 2020 09:04:21 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 11 Dec 2020 09:04:22 GMT
WORKDIR /var/www/html
# Fri, 11 Dec 2020 09:05:06 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 11 Dec 2020 09:05:08 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 11 Dec 2020 09:05:08 GMT
ENV ADMINER_VERSION=4.7.8
# Fri, 11 Dec 2020 09:05:09 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Fri, 11 Dec 2020 09:05:11 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Fri, 11 Dec 2020 09:05:14 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 11 Dec 2020 09:05:15 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 11 Dec 2020 09:05:16 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 11 Dec 2020 09:05:17 GMT
USER adminer
# Fri, 11 Dec 2020 09:05:18 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 11 Dec 2020 09:05:19 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:f1c16df8fee33d421d08790b17ca2af67a3fe49e77b6b991dd0c30631f5d1baf`  
		Last Modified: Fri, 11 Dec 2020 02:17:57 GMT  
		Size: 2.6 MB (2601992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623cc08cbe035cf15859e57a83e2243620418da06e1905d1875a46bec901e540`  
		Last Modified: Fri, 11 Dec 2020 07:56:49 GMT  
		Size: 1.3 MB (1310156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3a7aacff9b7ccf646f2bdbbc8d40bbb304550e813876049e721abd35461df9`  
		Last Modified: Fri, 11 Dec 2020 07:56:49 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d3214ea6f418597f370177309be7728f94481030c9cba6e45c4b74cfd04cc0`  
		Last Modified: Fri, 11 Dec 2020 07:56:49 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64de18534c9c3dd7212eceb5a285d571df578238ca4684a2e922b131e9947d79`  
		Last Modified: Fri, 11 Dec 2020 07:57:40 GMT  
		Size: 10.3 MB (10338603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d60b5c1c75b96676e4154f74a500fdd4a2645d4c51e189b0bdd18e06f26c3143`  
		Last Modified: Fri, 11 Dec 2020 07:57:39 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee32c3be90bc13cb4b3406c492ec35d5c211ac42b25e536939fb3220aea672b`  
		Last Modified: Fri, 11 Dec 2020 07:57:44 GMT  
		Size: 13.2 MB (13201116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e71cdda7d8acfe2fe1a6263c1b004b3ae972d7ce1c0ac95fec09aa0c0ba1f7fd`  
		Last Modified: Fri, 11 Dec 2020 07:57:39 GMT  
		Size: 2.3 KB (2258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec74a6ee1beba601eed5abe261394c8ddfa2d53093a1f6768356ec5891066746`  
		Last Modified: Fri, 11 Dec 2020 07:57:40 GMT  
		Size: 16.9 KB (16889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b84bf5ad218839b4e8156c322c5611b3c26167141a7c1e8049055deeda8b1ed5`  
		Last Modified: Fri, 11 Dec 2020 09:07:23 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0113ef6e65685219488d6543639cff152292617519f4649a6d7c8e4bbf03322b`  
		Last Modified: Fri, 11 Dec 2020 09:07:21 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2501c821a30d874046f30dd9d3947aa9f82cca3e9d39eb18214a765744e0b24`  
		Last Modified: Fri, 11 Dec 2020 09:07:21 GMT  
		Size: 4.0 MB (4026242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:945b172c5cf67a28a59e5b25cfed08871f360f551a912c8d7f64c096d6554812`  
		Last Modified: Fri, 11 Dec 2020 09:07:20 GMT  
		Size: 1.5 KB (1473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df40a3aa85441cb471ce645d5a0a2564fb9e2f042e078b8f04dd343488863a4`  
		Last Modified: Fri, 11 Dec 2020 09:07:20 GMT  
		Size: 570.9 KB (570917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90644dda17e22024741efd92b2987150a52659ae6bb25b7ea232e9b72d3b1d83`  
		Last Modified: Fri, 11 Dec 2020 09:07:20 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4` - linux; arm variant v7

```console
$ docker pull adminer@sha256:39b988e9485b8f06142e8584a4764c3c32159d51377eab0739b1cf794f701d1a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31186995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d4ed3310dfe2d29dd9a809a5ea826952ac518c5d93ab5e12054d9b7560791f7`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 22 Oct 2020 01:58:13 GMT
ADD file:46f89172426e9f5b1d669a2ca7ab218fc2deaef1caeeab88f2b5bd443ac9773d in / 
# Thu, 22 Oct 2020 01:58:14 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 06:47:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 22 Oct 2020 06:47:37 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 22 Oct 2020 06:47:45 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 22 Oct 2020 06:47:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 22 Oct 2020 06:47:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 22 Oct 2020 06:47:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 06:47:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 06:48:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 22 Oct 2020 06:56:26 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 01 Dec 2020 02:39:45 GMT
ENV PHP_VERSION=7.4.13
# Tue, 01 Dec 2020 02:39:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Tue, 01 Dec 2020 02:39:46 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Tue, 01 Dec 2020 02:39:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 01 Dec 2020 02:39:53 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 01 Dec 2020 02:42:30 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 01 Dec 2020 02:42:32 GMT
COPY multi:afab483600631d4d87fe030871bbb016f1c2b73c0b72609d857bace419af7f5d in /usr/local/bin/ 
# Tue, 01 Dec 2020 02:42:37 GMT
RUN docker-php-ext-enable sodium
# Tue, 01 Dec 2020 02:42:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 01 Dec 2020 02:42:40 GMT
CMD ["php" "-a"]
# Tue, 01 Dec 2020 04:28:04 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Tue, 01 Dec 2020 04:28:05 GMT
STOPSIGNAL SIGINT
# Tue, 01 Dec 2020 04:28:12 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 01 Dec 2020 04:28:14 GMT
WORKDIR /var/www/html
# Tue, 01 Dec 2020 04:29:07 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Tue, 01 Dec 2020 04:29:08 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Tue, 08 Dec 2020 00:00:44 GMT
ENV ADMINER_VERSION=4.7.8
# Tue, 08 Dec 2020 00:00:49 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Tue, 08 Dec 2020 00:00:52 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Tue, 08 Dec 2020 00:00:57 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Tue, 08 Dec 2020 00:00:58 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 08 Dec 2020 00:00:59 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Tue, 08 Dec 2020 00:00:59 GMT
USER adminer
# Tue, 08 Dec 2020 00:01:00 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 08 Dec 2020 00:01:01 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:5f2023fd85a4e68f37fe41421fd89f30e69b98a645613521c57c01317561eee3`  
		Last Modified: Thu, 22 Oct 2020 01:58:45 GMT  
		Size: 2.4 MB (2405675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60b50c98f8a8e2c6a27378dfa0f44df1844ac67c6981303675f138a42679f25`  
		Last Modified: Thu, 22 Oct 2020 07:35:57 GMT  
		Size: 1.2 MB (1214265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b472094d673b7c272085505c976192b9aaafa3157c99bade9755fbca18a24071`  
		Last Modified: Thu, 22 Oct 2020 07:35:56 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc39e5d916c11e7eb158e72d14ab981eb45ccc7b6451c1d6d3cb627b71cdbb6`  
		Last Modified: Thu, 22 Oct 2020 07:35:55 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e834fd39435ea86b08faf9b3af2e2623e0a247fa06dfe096decdf80f7a986a`  
		Last Modified: Tue, 01 Dec 2020 04:00:44 GMT  
		Size: 10.3 MB (10338583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a458e4d5704bca7330dbfab239f74ff255f4813b58f19f50a4ad7fd7087f0c8`  
		Last Modified: Tue, 01 Dec 2020 04:00:43 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a500121bbd97abb5116b6e95bdaa9aed74160334e46aadaabef548dca0edce6`  
		Last Modified: Tue, 01 Dec 2020 04:00:46 GMT  
		Size: 12.7 MB (12706582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3321b09ca6255e6f5cb4dce9057df675dd4644a3654424c7ee95fbdcb083e9c`  
		Last Modified: Tue, 01 Dec 2020 04:00:42 GMT  
		Size: 2.3 KB (2257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:345450fde280cf49e34f7246cebd38e311d4b7bebe22415a6126c18e67899f91`  
		Last Modified: Tue, 01 Dec 2020 04:00:42 GMT  
		Size: 16.9 KB (16903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:520112c186c5f2a097e8056a524b7c35704923ebeb6247e924ca839fe6e5b343`  
		Last Modified: Tue, 01 Dec 2020 04:31:36 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d98e04775b392470b2f426804979b34d740103414161d9c89f4df0d0b086e51`  
		Last Modified: Tue, 01 Dec 2020 04:31:34 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c074206a89c8b669d116ecf57544d500dcdc5379828bb10e531adf7af19b658a`  
		Last Modified: Tue, 01 Dec 2020 04:31:34 GMT  
		Size: 3.9 MB (3926108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137384dc891a62af154426c4b36cb9192967da61547507bc1b95301727f85c39`  
		Last Modified: Tue, 01 Dec 2020 04:31:34 GMT  
		Size: 1.5 KB (1473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfdcb3be5430d4c822996a4b1f107a12cafae7d60cc6faf1f7a7cdd8dacaab94`  
		Last Modified: Tue, 08 Dec 2020 00:01:41 GMT  
		Size: 570.9 KB (570924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e55c2ae42163732e674f91058ca3617c71403e138adb01dd23c943ad95d6b0`  
		Last Modified: Tue, 08 Dec 2020 00:01:41 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:b1e09cd04824b43f07df33154a383bc15923451af616eaaae657aca0620d729f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33702279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea6b86a866d797b65cc54d7527a70e1a5e91bf21ecc1ee3fd22b2a2c18d7f6ed`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 07:18:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 22 Oct 2020 07:18:56 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 22 Oct 2020 07:18:59 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 22 Oct 2020 07:19:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 22 Oct 2020 07:19:04 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 22 Oct 2020 07:19:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 07:19:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 07:19:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 22 Oct 2020 07:27:59 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 01 Dec 2020 03:27:01 GMT
ENV PHP_VERSION=7.4.13
# Tue, 01 Dec 2020 03:27:02 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Tue, 01 Dec 2020 03:27:03 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Tue, 01 Dec 2020 03:27:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 01 Dec 2020 03:27:09 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 01 Dec 2020 03:30:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 01 Dec 2020 03:30:42 GMT
COPY multi:afab483600631d4d87fe030871bbb016f1c2b73c0b72609d857bace419af7f5d in /usr/local/bin/ 
# Tue, 01 Dec 2020 03:30:50 GMT
RUN docker-php-ext-enable sodium
# Tue, 01 Dec 2020 03:30:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 01 Dec 2020 03:30:56 GMT
CMD ["php" "-a"]
# Tue, 01 Dec 2020 08:12:36 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Tue, 01 Dec 2020 08:12:37 GMT
STOPSIGNAL SIGINT
# Tue, 01 Dec 2020 08:12:39 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 01 Dec 2020 08:12:40 GMT
WORKDIR /var/www/html
# Tue, 01 Dec 2020 08:13:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Tue, 01 Dec 2020 08:13:23 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Mon, 07 Dec 2020 23:39:52 GMT
ENV ADMINER_VERSION=4.7.8
# Mon, 07 Dec 2020 23:39:53 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Mon, 07 Dec 2020 23:39:54 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Mon, 07 Dec 2020 23:39:56 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Mon, 07 Dec 2020 23:39:57 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Mon, 07 Dec 2020 23:39:58 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Mon, 07 Dec 2020 23:39:58 GMT
USER adminer
# Mon, 07 Dec 2020 23:39:59 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Mon, 07 Dec 2020 23:40:00 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d57dba23203172f8fffd1379aef0307e782178b62dfc684d43c546f7e874ed`  
		Last Modified: Thu, 22 Oct 2020 08:06:21 GMT  
		Size: 1.3 MB (1342784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8414edb0c9c2f7472bb6228bf691a2ddac19ddad7bad789c7cbdc147aded711`  
		Last Modified: Thu, 22 Oct 2020 08:06:20 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d26eeef0db35b2328adae38a8490c7403844452c3606dd17fbe68216f98e82`  
		Last Modified: Thu, 22 Oct 2020 08:06:19 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29be11fa56be3ca1af1498b259f3d5e058a869970cac6d670cf4ca1502485810`  
		Last Modified: Tue, 01 Dec 2020 04:53:56 GMT  
		Size: 10.3 MB (10338597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a553892b0358f6f72064d4dd5e727b686c4461cca7ea8a1211cc86adddb2cb`  
		Last Modified: Tue, 01 Dec 2020 04:53:56 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:828f98d07be67a182899230fc7e38e513de6ce85178d60116c765e90ffbc4119`  
		Last Modified: Tue, 01 Dec 2020 04:54:00 GMT  
		Size: 14.4 MB (14386945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec168016016eef2bef46796f7d7ec48af2459e14d65b9fc2871e756fe3e14d6a`  
		Last Modified: Tue, 01 Dec 2020 04:53:56 GMT  
		Size: 2.3 KB (2260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca32a186f8576115bc6fffe021ff54c52337662fa3cdb51c863d12d20ba02de`  
		Last Modified: Tue, 01 Dec 2020 04:53:55 GMT  
		Size: 17.0 KB (16976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b859cea4a3bb568911dd8f097b1a684daef31726fc5a591b4d9cd57b35187f`  
		Last Modified: Tue, 01 Dec 2020 08:14:59 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e97602a3ba690a845f8ecfaabcff93f82efc85a36445f6413d26f2482987638`  
		Last Modified: Tue, 01 Dec 2020 08:14:56 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6067b9bb9a3850bc39e227d17ab5df99a9bbe61e6d9933fc63c85e464f4aedf5`  
		Last Modified: Tue, 01 Dec 2020 08:14:57 GMT  
		Size: 4.3 MB (4331540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c677bbe386af33259d80d8f4d08a7147fef67adf472b9d841dac1a4a118c7f`  
		Last Modified: Tue, 01 Dec 2020 08:14:57 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4763c08ec3b1c7b68505b48ed92faf18a62525f8ce02d4fba750c232c1826aa9`  
		Last Modified: Mon, 07 Dec 2020 23:40:27 GMT  
		Size: 570.9 KB (570924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:983b1fb60b2afcee1aa424434071184fe8cf507838ac872e30e48755b41f1232`  
		Last Modified: Mon, 07 Dec 2020 23:40:28 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4` - linux; 386

```console
$ docker pull adminer@sha256:13a4c7ddafd6d4d6a5ee85529f6fa01ebe99d5c5bc1bcafafc85425658693817
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34626966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bb37df3c96977a9c7d5bcff85e2f3904eb30a1d4e2358f0c1644fae769a3ea7`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 22 Oct 2020 02:00:33 GMT
ADD file:46ad43b4984bcf49c5a888ff3628f23161f55cd1fb062f469e707100c97fa254 in / 
# Thu, 22 Oct 2020 02:00:33 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:36:23 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 22 Oct 2020 03:36:26 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 22 Oct 2020 03:36:27 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 22 Oct 2020 03:36:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 22 Oct 2020 03:36:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 22 Oct 2020 03:36:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 03:36:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 03:36:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 22 Oct 2020 03:55:07 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 01 Dec 2020 04:01:21 GMT
ENV PHP_VERSION=7.4.13
# Tue, 01 Dec 2020 04:01:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Tue, 01 Dec 2020 04:01:22 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Tue, 01 Dec 2020 04:01:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 01 Dec 2020 04:01:40 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 01 Dec 2020 04:10:51 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 01 Dec 2020 04:10:52 GMT
COPY multi:afab483600631d4d87fe030871bbb016f1c2b73c0b72609d857bace419af7f5d in /usr/local/bin/ 
# Tue, 01 Dec 2020 04:10:54 GMT
RUN docker-php-ext-enable sodium
# Tue, 01 Dec 2020 04:10:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 01 Dec 2020 04:10:55 GMT
CMD ["php" "-a"]
# Tue, 01 Dec 2020 09:24:38 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Tue, 01 Dec 2020 09:24:38 GMT
STOPSIGNAL SIGINT
# Tue, 01 Dec 2020 09:24:39 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 01 Dec 2020 09:24:39 GMT
WORKDIR /var/www/html
# Tue, 01 Dec 2020 09:25:13 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Tue, 01 Dec 2020 09:25:13 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Mon, 07 Dec 2020 23:38:24 GMT
ENV ADMINER_VERSION=4.7.8
# Mon, 07 Dec 2020 23:38:24 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Mon, 07 Dec 2020 23:38:24 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Mon, 07 Dec 2020 23:38:26 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Mon, 07 Dec 2020 23:38:26 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Mon, 07 Dec 2020 23:38:26 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Mon, 07 Dec 2020 23:38:26 GMT
USER adminer
# Mon, 07 Dec 2020 23:38:26 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Mon, 07 Dec 2020 23:38:27 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:d6ca64ac6f4b6382142ce9a3501652938130a6ec4bb02f3f455ee1f980834cfe`  
		Last Modified: Thu, 22 Oct 2020 02:00:57 GMT  
		Size: 2.8 MB (2791407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30be8ffd290910905a5fb7cbb70252eb0f59edb09db20bdc21f3b65456acc28f`  
		Last Modified: Thu, 22 Oct 2020 05:10:23 GMT  
		Size: 1.4 MB (1439641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d58e2433b13446c863e85b34f8e4c93ca9d5b3b93d2bac415fd9cdf77bcec4`  
		Last Modified: Thu, 22 Oct 2020 05:10:21 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5729dcb8d303f82a7f8cf3df49048e34ce8ee89f79155fb08a475da46b64308`  
		Last Modified: Thu, 22 Oct 2020 05:10:21 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ffdca9b500ff910069fefe63b455206db2cf0fa00dc6b7c7d53219dfaf7f5b`  
		Last Modified: Tue, 01 Dec 2020 07:15:13 GMT  
		Size: 10.3 MB (10338561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c682383cda14fca62843652d7478a26995cfbbfbcb457985de4ca5cfb77de751`  
		Last Modified: Tue, 01 Dec 2020 07:15:12 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57833a53685f649182bdbb4194ba35390c17fa65a6b09c4e377a42a5f9aaca30`  
		Last Modified: Tue, 01 Dec 2020 07:15:18 GMT  
		Size: 14.9 MB (14942640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7003874a29c37e250b24c310b448d1c36607cdb1b43128071780d5fd0a0dc3e1`  
		Last Modified: Tue, 01 Dec 2020 07:15:12 GMT  
		Size: 2.3 KB (2259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fcfab619124f72931608ea142c1cd80a26871e1631380720b6be739170e21b6`  
		Last Modified: Tue, 01 Dec 2020 07:15:12 GMT  
		Size: 16.9 KB (16924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055719a49e04df90bb23499c98da9779637e3b44446a60f202283f57e4b29b04`  
		Last Modified: Tue, 01 Dec 2020 09:26:14 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2b0f52d9f107a35a34b4f8c69abbdf24f2de8a0431c812d74cb6dd3cbf8bf2`  
		Last Modified: Tue, 01 Dec 2020 09:26:13 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4edb5ffb9c3f753b4991debfaeef5c535ae5d689a18b7fff9f0b042c5883865`  
		Last Modified: Tue, 01 Dec 2020 09:26:14 GMT  
		Size: 4.5 MB (4519100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9258866f679eb2cbc89aa311d5d2dad0c146a7e9f61c9e805b63d7f324d2afb0`  
		Last Modified: Tue, 01 Dec 2020 09:26:13 GMT  
		Size: 1.5 KB (1472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:904e3ae5079e7cd06213e6912d4237663cff97a37e1ed247e24b7f455951eafe`  
		Last Modified: Mon, 07 Dec 2020 23:38:45 GMT  
		Size: 570.9 KB (570859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:362b319c8a865e06c57265a80b857954a02a4e09ffe3eda699eede128dcdef90`  
		Last Modified: Mon, 07 Dec 2020 23:38:45 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4` - linux; ppc64le

```console
$ docker pull adminer@sha256:73feff7b317d1078b173d0c1dc928c14bf61e94b4562a0a79132b9dac74739aa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 MB (35029016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2bacaef82d901426ed9bf50182af16a98e04172b1d2dac51b87db0885487f72`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 22 Oct 2020 11:00:06 GMT
ADD file:176e047fab2c1828575bffa6b14773efa297b7ecf312d86103c5dd4f78ec8027 in / 
# Thu, 22 Oct 2020 11:00:17 GMT
CMD ["/bin/sh"]
# Fri, 23 Oct 2020 00:21:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 23 Oct 2020 00:21:18 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 23 Oct 2020 00:21:30 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 23 Oct 2020 00:21:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 23 Oct 2020 00:21:44 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 23 Oct 2020 00:21:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 23 Oct 2020 00:21:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 23 Oct 2020 00:21:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 23 Oct 2020 00:34:37 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 01 Dec 2020 03:52:39 GMT
ENV PHP_VERSION=7.4.13
# Tue, 01 Dec 2020 03:52:44 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Tue, 01 Dec 2020 03:52:51 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Tue, 01 Dec 2020 03:53:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 01 Dec 2020 03:53:13 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 01 Dec 2020 03:57:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 01 Dec 2020 03:57:24 GMT
COPY multi:afab483600631d4d87fe030871bbb016f1c2b73c0b72609d857bace419af7f5d in /usr/local/bin/ 
# Tue, 01 Dec 2020 03:57:33 GMT
RUN docker-php-ext-enable sodium
# Tue, 01 Dec 2020 03:57:36 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 01 Dec 2020 03:57:39 GMT
CMD ["php" "-a"]
# Tue, 01 Dec 2020 07:09:03 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Tue, 01 Dec 2020 07:09:12 GMT
STOPSIGNAL SIGINT
# Tue, 01 Dec 2020 07:09:25 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 01 Dec 2020 07:09:32 GMT
WORKDIR /var/www/html
# Tue, 01 Dec 2020 07:10:30 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Tue, 01 Dec 2020 07:10:33 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Tue, 08 Dec 2020 00:16:36 GMT
ENV ADMINER_VERSION=4.7.8
# Tue, 08 Dec 2020 00:16:38 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Tue, 08 Dec 2020 00:16:41 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Tue, 08 Dec 2020 00:16:53 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Tue, 08 Dec 2020 00:16:54 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 08 Dec 2020 00:16:58 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Tue, 08 Dec 2020 00:17:11 GMT
USER adminer
# Tue, 08 Dec 2020 00:17:16 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 08 Dec 2020 00:17:18 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:692a9d763e196c85d79fc3e45b316b1bb557c93ba88a3c8ebf679a585d1efe73`  
		Last Modified: Thu, 22 Oct 2020 11:02:06 GMT  
		Size: 2.8 MB (2803218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0285d6f06f3beb1c140c055210664c441b93dd4f2037177a5396bce94ca16ce5`  
		Last Modified: Fri, 23 Oct 2020 01:34:08 GMT  
		Size: 1.4 MB (1383187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a6459a3bf272daa53ff4ba97cc849676f497de9f78d8e9378ec02552293f175`  
		Last Modified: Fri, 23 Oct 2020 01:34:07 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16cff6064dc29d3f629d353736c1cac074caa5b50738422adb84de99a019bb32`  
		Last Modified: Fri, 23 Oct 2020 01:34:08 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0baf560776c5dd75b5673be3d73b900119615cfc4e4fe24414486e3d1f11920`  
		Last Modified: Tue, 01 Dec 2020 05:50:29 GMT  
		Size: 10.3 MB (10338609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4d8083b683ead9a591a00aff14c8d0091665e1433d301a027b214f19cbe23f`  
		Last Modified: Tue, 01 Dec 2020 05:50:29 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7381e6ce3e117510e5a2bf102da48e3cc1b5fd3414651ec324bbe759d367be`  
		Last Modified: Tue, 01 Dec 2020 05:50:32 GMT  
		Size: 15.5 MB (15548036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8328c4e67c6b29f383993d05557e298bc834c18c00961b9ab2a1c4e4eb05b4fd`  
		Last Modified: Tue, 01 Dec 2020 05:50:28 GMT  
		Size: 2.3 KB (2259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:236813d0f57da4fa9c0d5938846f85e82a0a01ce89ca208916b8f649c0ee99fd`  
		Last Modified: Tue, 01 Dec 2020 05:50:28 GMT  
		Size: 17.0 KB (16965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acf7ec6b5baaa9faab722bfc6a7098e0871e3edb42be513e64fe8e06bc7edec1`  
		Last Modified: Tue, 01 Dec 2020 07:14:36 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c17363dc3aab754805ecdc74f39535a73cfc5f3cebe72a4cb18fdc97df1ef9fa`  
		Last Modified: Tue, 01 Dec 2020 07:14:33 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95753fdce29daf55de647d3a29a8cc07941f7bf95fec4a560b0d698478b782f3`  
		Last Modified: Tue, 01 Dec 2020 07:14:34 GMT  
		Size: 4.4 MB (4360119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cad5fcb53526734d41770680ea56047b6e13c767960fc1d0a0b8de7c7030c75`  
		Last Modified: Tue, 01 Dec 2020 07:14:33 GMT  
		Size: 1.5 KB (1474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b231a33566f06d48010343aac194149b1ce1613cf2397c67cf1be2984295f133`  
		Last Modified: Tue, 08 Dec 2020 00:18:38 GMT  
		Size: 570.9 KB (570925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628d0ad1cc992636ad6e5a1f0cf7de70d844c7cccb85cda16205dc67b167e131`  
		Last Modified: Tue, 08 Dec 2020 00:18:38 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4` - linux; s390x

```console
$ docker pull adminer@sha256:6b00709e793594a51832541158adeb2ae42e00829dbfb77a54bc0eef7fd1668d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32521955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f75d1bfddd1544fe2cddf65f0baa090dfb992c4a38b43b24670dc3b1ce037d7`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 11 Dec 2020 02:09:52 GMT
ADD file:c9395a36a4e03768aabd282eb1f31705cc00181d3147222d9c940eaa5a8fd511 in / 
# Fri, 11 Dec 2020 02:09:53 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 11:30:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 11 Dec 2020 11:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 11 Dec 2020 11:30:56 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 11 Dec 2020 11:30:57 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 11 Dec 2020 11:30:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 11 Dec 2020 11:30:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Dec 2020 11:31:00 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Dec 2020 11:31:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 11 Dec 2020 12:01:46 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 11 Dec 2020 12:01:46 GMT
ENV PHP_VERSION=7.4.13
# Fri, 11 Dec 2020 12:01:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Fri, 11 Dec 2020 12:01:48 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Fri, 11 Dec 2020 12:01:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 11 Dec 2020 12:01:54 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Dec 2020 12:08:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Dec 2020 12:08:47 GMT
COPY multi:afab483600631d4d87fe030871bbb016f1c2b73c0b72609d857bace419af7f5d in /usr/local/bin/ 
# Fri, 11 Dec 2020 12:08:49 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Dec 2020 12:08:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Dec 2020 12:08:50 GMT
CMD ["php" "-a"]
# Fri, 11 Dec 2020 18:43:30 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 11 Dec 2020 18:43:31 GMT
STOPSIGNAL SIGINT
# Fri, 11 Dec 2020 18:43:33 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 11 Dec 2020 18:43:33 GMT
WORKDIR /var/www/html
# Fri, 11 Dec 2020 18:44:50 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 11 Dec 2020 18:44:50 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 11 Dec 2020 18:44:51 GMT
ENV ADMINER_VERSION=4.7.8
# Fri, 11 Dec 2020 18:44:52 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Fri, 11 Dec 2020 18:44:52 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Fri, 11 Dec 2020 18:44:56 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 11 Dec 2020 18:44:57 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 11 Dec 2020 18:44:57 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 11 Dec 2020 18:44:58 GMT
USER adminer
# Fri, 11 Dec 2020 18:44:59 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 11 Dec 2020 18:44:59 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:7c2470fe3d16cb70fca0826168095a96838b1322a8cd1502b28284ee8561b491`  
		Last Modified: Fri, 11 Dec 2020 02:10:27 GMT  
		Size: 2.6 MB (2565988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a23c8359d30ae261ad953f292e6681a71ebc7388607b74d901bbc07f71e1311`  
		Last Modified: Fri, 11 Dec 2020 13:48:01 GMT  
		Size: 1.4 MB (1382587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01422c3e898d3241d4134256bf0d911b0752823227af04614187c79c187e2843`  
		Last Modified: Fri, 11 Dec 2020 13:48:03 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a0be2077abd44f96e50bdebb1ed93a6e2b8d504761c23fa0e5e9b87045ca38`  
		Last Modified: Fri, 11 Dec 2020 13:48:01 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267bafe0bb23009994a23ad5cdcc3b4d425f186f0e488b5f7461463ad1b53814`  
		Last Modified: Fri, 11 Dec 2020 13:50:24 GMT  
		Size: 10.3 MB (10338590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36304b0fbddac7ce44edacaedb902676688cfc3bb7082576f6b57eed0ccc133e`  
		Last Modified: Fri, 11 Dec 2020 13:50:25 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fa33489075ff6318ffc5a7cf5c94cb4ce65ccfc82b5970cc91628780c130aae`  
		Last Modified: Fri, 11 Dec 2020 13:50:26 GMT  
		Size: 13.5 MB (13485898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155ae451461e50390ae0db27a78a329e87a86b9f9eb04f6db81fcc27430f2d51`  
		Last Modified: Fri, 11 Dec 2020 13:50:24 GMT  
		Size: 2.3 KB (2257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b379111cc7023c652243c4d9234de47984fa307030d667bf14e5d12889ec8180`  
		Last Modified: Fri, 11 Dec 2020 13:50:24 GMT  
		Size: 16.9 KB (16879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a18e16d8efd7f249149e2d38813d86590cc4a55f23d8c5bbba970725422ea51`  
		Last Modified: Fri, 11 Dec 2020 18:47:13 GMT  
		Size: 310.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ba44137233477a93edb1e0cc94bee3ce4dafaed9ff932d21594190f861ef75`  
		Last Modified: Fri, 11 Dec 2020 18:47:13 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cba732448866bbb0e567b7510578f951e9cf0bc258588c8e898be1606e3a3eb`  
		Last Modified: Fri, 11 Dec 2020 18:47:11 GMT  
		Size: 4.2 MB (4153155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8faf5f39c5d146bc658625977adca6ce417bb45b9683bb1767b99abfea6d3d56`  
		Last Modified: Fri, 11 Dec 2020 18:47:11 GMT  
		Size: 1.5 KB (1473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008d2a285f2f6bcf687be0cb08b167a975a4d7534a16435da10ba2b75b2e2d73`  
		Last Modified: Fri, 11 Dec 2020 18:47:11 GMT  
		Size: 570.9 KB (570918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6852608d1b2324d98a56de31e6fc11ac1fe8e95f605b50c9f72db2bd5cd092`  
		Last Modified: Fri, 11 Dec 2020 18:47:12 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:4.7`

```console
$ docker pull adminer@sha256:4600f2453f7c9f3ee8179016a65d0b49a8dfb89467ac0947a6245e62e7f81fb1
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

### `adminer:4.7` - linux; amd64

```console
$ docker pull adminer@sha256:4b087576de7b4ca7c60bb3558f0b5ee30f496cee10fa19ea0a9f0e071c72b1f5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (33965375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2db7241b0f1461d8707525832e608fe513453f99c11beed9413194f7519e05`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 06:30:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 22 Oct 2020 06:30:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 22 Oct 2020 06:30:15 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 22 Oct 2020 06:30:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 22 Oct 2020 06:30:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 22 Oct 2020 06:30:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 06:30:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 06:30:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 22 Oct 2020 06:43:41 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 01 Dec 2020 04:36:20 GMT
ENV PHP_VERSION=7.4.13
# Tue, 01 Dec 2020 04:36:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Tue, 01 Dec 2020 04:36:21 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Tue, 01 Dec 2020 04:36:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 01 Dec 2020 04:36:27 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 01 Dec 2020 04:44:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 01 Dec 2020 04:44:54 GMT
COPY multi:afab483600631d4d87fe030871bbb016f1c2b73c0b72609d857bace419af7f5d in /usr/local/bin/ 
# Tue, 01 Dec 2020 04:44:57 GMT
RUN docker-php-ext-enable sodium
# Tue, 01 Dec 2020 04:44:57 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 01 Dec 2020 04:44:57 GMT
CMD ["php" "-a"]
# Tue, 01 Dec 2020 07:46:46 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Tue, 01 Dec 2020 07:46:46 GMT
STOPSIGNAL SIGINT
# Tue, 01 Dec 2020 07:46:47 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 01 Dec 2020 07:46:48 GMT
WORKDIR /var/www/html
# Tue, 01 Dec 2020 07:47:15 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Tue, 01 Dec 2020 07:47:15 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Tue, 08 Dec 2020 00:19:24 GMT
ENV ADMINER_VERSION=4.7.8
# Tue, 08 Dec 2020 00:19:24 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Tue, 08 Dec 2020 00:19:24 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Tue, 08 Dec 2020 00:19:26 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Tue, 08 Dec 2020 00:19:26 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 08 Dec 2020 00:19:26 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Tue, 08 Dec 2020 00:19:26 GMT
USER adminer
# Tue, 08 Dec 2020 00:19:27 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 08 Dec 2020 00:19:27 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f8bf6cfdbe614fef94f982905079c16e27b3de2d24eb1ff513d3d83e656ca2`  
		Last Modified: Thu, 22 Oct 2020 07:36:55 GMT  
		Size: 1.3 MB (1340771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce5be79740125b9e74a77885bf6ee2b0d25ac7ed9e9432c5aa7210bb3b00458a`  
		Last Modified: Thu, 22 Oct 2020 07:36:55 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99dd6507fe563b66ba35badf706e1bbb2d39eb5d0a3c0d5a86a45d2af7e89c1`  
		Last Modified: Thu, 22 Oct 2020 07:36:55 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c513a1b503cf7c9f18fa014dada9744070ded92dc9ad548cd056c4f56dc1a9`  
		Last Modified: Tue, 01 Dec 2020 07:27:10 GMT  
		Size: 10.3 MB (10338569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff080eafb4c0518981fca6aef4d239863fc59195f41ce7c440b2c6c518f2ac79`  
		Last Modified: Tue, 01 Dec 2020 07:27:09 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e818119992b11dbf09b710066a78920985b9ea1310fc8272df816e0884985f44`  
		Last Modified: Tue, 01 Dec 2020 07:27:13 GMT  
		Size: 14.6 MB (14572037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba3c14a67f95ae52ebfb558ab6b5d87687a05ce41c8df0a618ff42b73204e40`  
		Last Modified: Tue, 01 Dec 2020 07:27:09 GMT  
		Size: 2.3 KB (2257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbb0285b7ad2b170e4ed2cffbe0f16ba55d689c056ff43767834783eab7b8261`  
		Last Modified: Tue, 01 Dec 2020 07:27:09 GMT  
		Size: 17.0 KB (16987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae324cfad8acf03b3a98a15e963b7046404a7da3a6bbf68fd65d37f899f194d`  
		Last Modified: Tue, 01 Dec 2020 07:48:25 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb51158f683d66315de6fa572f7ea13d8ffb71ac85faa20c8578edb11678f37d`  
		Last Modified: Tue, 01 Dec 2020 07:48:23 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71ac21b64d1d63d967acb13664404babd0ef86fc896c484ce28cccf70001d0f1`  
		Last Modified: Tue, 01 Dec 2020 07:48:24 GMT  
		Size: 4.3 MB (4321455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2170e09d39d861e9bb7a5da5def906b44153b6c481fe17925ba82d1f1f78eec`  
		Last Modified: Tue, 01 Dec 2020 07:48:24 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d95b48dfa11f7f5c061f6522f6ff5d574452b8f321c6075455da2643b1967a`  
		Last Modified: Tue, 08 Dec 2020 00:19:45 GMT  
		Size: 570.9 KB (570860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3bb2b5e72bf0dbd4b855ddf65aaf9c0d077703804bdbdc9ea3ea98cbbfceaf6`  
		Last Modified: Tue, 08 Dec 2020 00:19:44 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7` - linux; arm variant v6

```console
$ docker pull adminer@sha256:7e114494e5e3a8ece382083d27c33f6c993695f0ff6c92c235ced149177f5da9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32073857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9cfa5ccbab063435267257cf4c761402c956233cf22775ed1c774b53a045715`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 11 Dec 2020 02:17:15 GMT
ADD file:1a9c0a67560d338c0c0e7005d8915d998fc9cf3e9f53bfd7e42e8391f0a39bce in / 
# Fri, 11 Dec 2020 02:17:15 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 07:04:50 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 11 Dec 2020 07:04:53 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 11 Dec 2020 07:04:55 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 11 Dec 2020 07:04:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 11 Dec 2020 07:04:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 11 Dec 2020 07:05:00 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Dec 2020 07:05:01 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Dec 2020 07:05:02 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 11 Dec 2020 07:13:50 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 11 Dec 2020 07:13:54 GMT
ENV PHP_VERSION=7.4.13
# Fri, 11 Dec 2020 07:13:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Fri, 11 Dec 2020 07:13:56 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Fri, 11 Dec 2020 07:14:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 11 Dec 2020 07:14:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Dec 2020 07:17:37 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Dec 2020 07:17:39 GMT
COPY multi:afab483600631d4d87fe030871bbb016f1c2b73c0b72609d857bace419af7f5d in /usr/local/bin/ 
# Fri, 11 Dec 2020 07:17:42 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Dec 2020 07:17:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Dec 2020 07:17:43 GMT
CMD ["php" "-a"]
# Fri, 11 Dec 2020 09:04:18 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 11 Dec 2020 09:04:19 GMT
STOPSIGNAL SIGINT
# Fri, 11 Dec 2020 09:04:21 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 11 Dec 2020 09:04:22 GMT
WORKDIR /var/www/html
# Fri, 11 Dec 2020 09:05:06 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 11 Dec 2020 09:05:08 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 11 Dec 2020 09:05:08 GMT
ENV ADMINER_VERSION=4.7.8
# Fri, 11 Dec 2020 09:05:09 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Fri, 11 Dec 2020 09:05:11 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Fri, 11 Dec 2020 09:05:14 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 11 Dec 2020 09:05:15 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 11 Dec 2020 09:05:16 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 11 Dec 2020 09:05:17 GMT
USER adminer
# Fri, 11 Dec 2020 09:05:18 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 11 Dec 2020 09:05:19 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:f1c16df8fee33d421d08790b17ca2af67a3fe49e77b6b991dd0c30631f5d1baf`  
		Last Modified: Fri, 11 Dec 2020 02:17:57 GMT  
		Size: 2.6 MB (2601992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623cc08cbe035cf15859e57a83e2243620418da06e1905d1875a46bec901e540`  
		Last Modified: Fri, 11 Dec 2020 07:56:49 GMT  
		Size: 1.3 MB (1310156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3a7aacff9b7ccf646f2bdbbc8d40bbb304550e813876049e721abd35461df9`  
		Last Modified: Fri, 11 Dec 2020 07:56:49 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d3214ea6f418597f370177309be7728f94481030c9cba6e45c4b74cfd04cc0`  
		Last Modified: Fri, 11 Dec 2020 07:56:49 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64de18534c9c3dd7212eceb5a285d571df578238ca4684a2e922b131e9947d79`  
		Last Modified: Fri, 11 Dec 2020 07:57:40 GMT  
		Size: 10.3 MB (10338603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d60b5c1c75b96676e4154f74a500fdd4a2645d4c51e189b0bdd18e06f26c3143`  
		Last Modified: Fri, 11 Dec 2020 07:57:39 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee32c3be90bc13cb4b3406c492ec35d5c211ac42b25e536939fb3220aea672b`  
		Last Modified: Fri, 11 Dec 2020 07:57:44 GMT  
		Size: 13.2 MB (13201116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e71cdda7d8acfe2fe1a6263c1b004b3ae972d7ce1c0ac95fec09aa0c0ba1f7fd`  
		Last Modified: Fri, 11 Dec 2020 07:57:39 GMT  
		Size: 2.3 KB (2258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec74a6ee1beba601eed5abe261394c8ddfa2d53093a1f6768356ec5891066746`  
		Last Modified: Fri, 11 Dec 2020 07:57:40 GMT  
		Size: 16.9 KB (16889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b84bf5ad218839b4e8156c322c5611b3c26167141a7c1e8049055deeda8b1ed5`  
		Last Modified: Fri, 11 Dec 2020 09:07:23 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0113ef6e65685219488d6543639cff152292617519f4649a6d7c8e4bbf03322b`  
		Last Modified: Fri, 11 Dec 2020 09:07:21 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2501c821a30d874046f30dd9d3947aa9f82cca3e9d39eb18214a765744e0b24`  
		Last Modified: Fri, 11 Dec 2020 09:07:21 GMT  
		Size: 4.0 MB (4026242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:945b172c5cf67a28a59e5b25cfed08871f360f551a912c8d7f64c096d6554812`  
		Last Modified: Fri, 11 Dec 2020 09:07:20 GMT  
		Size: 1.5 KB (1473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df40a3aa85441cb471ce645d5a0a2564fb9e2f042e078b8f04dd343488863a4`  
		Last Modified: Fri, 11 Dec 2020 09:07:20 GMT  
		Size: 570.9 KB (570917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90644dda17e22024741efd92b2987150a52659ae6bb25b7ea232e9b72d3b1d83`  
		Last Modified: Fri, 11 Dec 2020 09:07:20 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7` - linux; arm variant v7

```console
$ docker pull adminer@sha256:39b988e9485b8f06142e8584a4764c3c32159d51377eab0739b1cf794f701d1a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31186995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d4ed3310dfe2d29dd9a809a5ea826952ac518c5d93ab5e12054d9b7560791f7`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 22 Oct 2020 01:58:13 GMT
ADD file:46f89172426e9f5b1d669a2ca7ab218fc2deaef1caeeab88f2b5bd443ac9773d in / 
# Thu, 22 Oct 2020 01:58:14 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 06:47:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 22 Oct 2020 06:47:37 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 22 Oct 2020 06:47:45 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 22 Oct 2020 06:47:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 22 Oct 2020 06:47:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 22 Oct 2020 06:47:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 06:47:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 06:48:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 22 Oct 2020 06:56:26 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 01 Dec 2020 02:39:45 GMT
ENV PHP_VERSION=7.4.13
# Tue, 01 Dec 2020 02:39:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Tue, 01 Dec 2020 02:39:46 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Tue, 01 Dec 2020 02:39:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 01 Dec 2020 02:39:53 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 01 Dec 2020 02:42:30 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 01 Dec 2020 02:42:32 GMT
COPY multi:afab483600631d4d87fe030871bbb016f1c2b73c0b72609d857bace419af7f5d in /usr/local/bin/ 
# Tue, 01 Dec 2020 02:42:37 GMT
RUN docker-php-ext-enable sodium
# Tue, 01 Dec 2020 02:42:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 01 Dec 2020 02:42:40 GMT
CMD ["php" "-a"]
# Tue, 01 Dec 2020 04:28:04 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Tue, 01 Dec 2020 04:28:05 GMT
STOPSIGNAL SIGINT
# Tue, 01 Dec 2020 04:28:12 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 01 Dec 2020 04:28:14 GMT
WORKDIR /var/www/html
# Tue, 01 Dec 2020 04:29:07 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Tue, 01 Dec 2020 04:29:08 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Tue, 08 Dec 2020 00:00:44 GMT
ENV ADMINER_VERSION=4.7.8
# Tue, 08 Dec 2020 00:00:49 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Tue, 08 Dec 2020 00:00:52 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Tue, 08 Dec 2020 00:00:57 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Tue, 08 Dec 2020 00:00:58 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 08 Dec 2020 00:00:59 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Tue, 08 Dec 2020 00:00:59 GMT
USER adminer
# Tue, 08 Dec 2020 00:01:00 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 08 Dec 2020 00:01:01 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:5f2023fd85a4e68f37fe41421fd89f30e69b98a645613521c57c01317561eee3`  
		Last Modified: Thu, 22 Oct 2020 01:58:45 GMT  
		Size: 2.4 MB (2405675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60b50c98f8a8e2c6a27378dfa0f44df1844ac67c6981303675f138a42679f25`  
		Last Modified: Thu, 22 Oct 2020 07:35:57 GMT  
		Size: 1.2 MB (1214265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b472094d673b7c272085505c976192b9aaafa3157c99bade9755fbca18a24071`  
		Last Modified: Thu, 22 Oct 2020 07:35:56 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc39e5d916c11e7eb158e72d14ab981eb45ccc7b6451c1d6d3cb627b71cdbb6`  
		Last Modified: Thu, 22 Oct 2020 07:35:55 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e834fd39435ea86b08faf9b3af2e2623e0a247fa06dfe096decdf80f7a986a`  
		Last Modified: Tue, 01 Dec 2020 04:00:44 GMT  
		Size: 10.3 MB (10338583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a458e4d5704bca7330dbfab239f74ff255f4813b58f19f50a4ad7fd7087f0c8`  
		Last Modified: Tue, 01 Dec 2020 04:00:43 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a500121bbd97abb5116b6e95bdaa9aed74160334e46aadaabef548dca0edce6`  
		Last Modified: Tue, 01 Dec 2020 04:00:46 GMT  
		Size: 12.7 MB (12706582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3321b09ca6255e6f5cb4dce9057df675dd4644a3654424c7ee95fbdcb083e9c`  
		Last Modified: Tue, 01 Dec 2020 04:00:42 GMT  
		Size: 2.3 KB (2257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:345450fde280cf49e34f7246cebd38e311d4b7bebe22415a6126c18e67899f91`  
		Last Modified: Tue, 01 Dec 2020 04:00:42 GMT  
		Size: 16.9 KB (16903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:520112c186c5f2a097e8056a524b7c35704923ebeb6247e924ca839fe6e5b343`  
		Last Modified: Tue, 01 Dec 2020 04:31:36 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d98e04775b392470b2f426804979b34d740103414161d9c89f4df0d0b086e51`  
		Last Modified: Tue, 01 Dec 2020 04:31:34 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c074206a89c8b669d116ecf57544d500dcdc5379828bb10e531adf7af19b658a`  
		Last Modified: Tue, 01 Dec 2020 04:31:34 GMT  
		Size: 3.9 MB (3926108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137384dc891a62af154426c4b36cb9192967da61547507bc1b95301727f85c39`  
		Last Modified: Tue, 01 Dec 2020 04:31:34 GMT  
		Size: 1.5 KB (1473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfdcb3be5430d4c822996a4b1f107a12cafae7d60cc6faf1f7a7cdd8dacaab94`  
		Last Modified: Tue, 08 Dec 2020 00:01:41 GMT  
		Size: 570.9 KB (570924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e55c2ae42163732e674f91058ca3617c71403e138adb01dd23c943ad95d6b0`  
		Last Modified: Tue, 08 Dec 2020 00:01:41 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:b1e09cd04824b43f07df33154a383bc15923451af616eaaae657aca0620d729f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33702279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea6b86a866d797b65cc54d7527a70e1a5e91bf21ecc1ee3fd22b2a2c18d7f6ed`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 07:18:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 22 Oct 2020 07:18:56 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 22 Oct 2020 07:18:59 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 22 Oct 2020 07:19:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 22 Oct 2020 07:19:04 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 22 Oct 2020 07:19:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 07:19:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 07:19:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 22 Oct 2020 07:27:59 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 01 Dec 2020 03:27:01 GMT
ENV PHP_VERSION=7.4.13
# Tue, 01 Dec 2020 03:27:02 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Tue, 01 Dec 2020 03:27:03 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Tue, 01 Dec 2020 03:27:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 01 Dec 2020 03:27:09 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 01 Dec 2020 03:30:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 01 Dec 2020 03:30:42 GMT
COPY multi:afab483600631d4d87fe030871bbb016f1c2b73c0b72609d857bace419af7f5d in /usr/local/bin/ 
# Tue, 01 Dec 2020 03:30:50 GMT
RUN docker-php-ext-enable sodium
# Tue, 01 Dec 2020 03:30:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 01 Dec 2020 03:30:56 GMT
CMD ["php" "-a"]
# Tue, 01 Dec 2020 08:12:36 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Tue, 01 Dec 2020 08:12:37 GMT
STOPSIGNAL SIGINT
# Tue, 01 Dec 2020 08:12:39 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 01 Dec 2020 08:12:40 GMT
WORKDIR /var/www/html
# Tue, 01 Dec 2020 08:13:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Tue, 01 Dec 2020 08:13:23 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Mon, 07 Dec 2020 23:39:52 GMT
ENV ADMINER_VERSION=4.7.8
# Mon, 07 Dec 2020 23:39:53 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Mon, 07 Dec 2020 23:39:54 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Mon, 07 Dec 2020 23:39:56 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Mon, 07 Dec 2020 23:39:57 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Mon, 07 Dec 2020 23:39:58 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Mon, 07 Dec 2020 23:39:58 GMT
USER adminer
# Mon, 07 Dec 2020 23:39:59 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Mon, 07 Dec 2020 23:40:00 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d57dba23203172f8fffd1379aef0307e782178b62dfc684d43c546f7e874ed`  
		Last Modified: Thu, 22 Oct 2020 08:06:21 GMT  
		Size: 1.3 MB (1342784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8414edb0c9c2f7472bb6228bf691a2ddac19ddad7bad789c7cbdc147aded711`  
		Last Modified: Thu, 22 Oct 2020 08:06:20 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d26eeef0db35b2328adae38a8490c7403844452c3606dd17fbe68216f98e82`  
		Last Modified: Thu, 22 Oct 2020 08:06:19 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29be11fa56be3ca1af1498b259f3d5e058a869970cac6d670cf4ca1502485810`  
		Last Modified: Tue, 01 Dec 2020 04:53:56 GMT  
		Size: 10.3 MB (10338597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a553892b0358f6f72064d4dd5e727b686c4461cca7ea8a1211cc86adddb2cb`  
		Last Modified: Tue, 01 Dec 2020 04:53:56 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:828f98d07be67a182899230fc7e38e513de6ce85178d60116c765e90ffbc4119`  
		Last Modified: Tue, 01 Dec 2020 04:54:00 GMT  
		Size: 14.4 MB (14386945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec168016016eef2bef46796f7d7ec48af2459e14d65b9fc2871e756fe3e14d6a`  
		Last Modified: Tue, 01 Dec 2020 04:53:56 GMT  
		Size: 2.3 KB (2260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca32a186f8576115bc6fffe021ff54c52337662fa3cdb51c863d12d20ba02de`  
		Last Modified: Tue, 01 Dec 2020 04:53:55 GMT  
		Size: 17.0 KB (16976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b859cea4a3bb568911dd8f097b1a684daef31726fc5a591b4d9cd57b35187f`  
		Last Modified: Tue, 01 Dec 2020 08:14:59 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e97602a3ba690a845f8ecfaabcff93f82efc85a36445f6413d26f2482987638`  
		Last Modified: Tue, 01 Dec 2020 08:14:56 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6067b9bb9a3850bc39e227d17ab5df99a9bbe61e6d9933fc63c85e464f4aedf5`  
		Last Modified: Tue, 01 Dec 2020 08:14:57 GMT  
		Size: 4.3 MB (4331540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c677bbe386af33259d80d8f4d08a7147fef67adf472b9d841dac1a4a118c7f`  
		Last Modified: Tue, 01 Dec 2020 08:14:57 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4763c08ec3b1c7b68505b48ed92faf18a62525f8ce02d4fba750c232c1826aa9`  
		Last Modified: Mon, 07 Dec 2020 23:40:27 GMT  
		Size: 570.9 KB (570924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:983b1fb60b2afcee1aa424434071184fe8cf507838ac872e30e48755b41f1232`  
		Last Modified: Mon, 07 Dec 2020 23:40:28 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7` - linux; 386

```console
$ docker pull adminer@sha256:13a4c7ddafd6d4d6a5ee85529f6fa01ebe99d5c5bc1bcafafc85425658693817
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34626966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bb37df3c96977a9c7d5bcff85e2f3904eb30a1d4e2358f0c1644fae769a3ea7`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 22 Oct 2020 02:00:33 GMT
ADD file:46ad43b4984bcf49c5a888ff3628f23161f55cd1fb062f469e707100c97fa254 in / 
# Thu, 22 Oct 2020 02:00:33 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:36:23 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 22 Oct 2020 03:36:26 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 22 Oct 2020 03:36:27 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 22 Oct 2020 03:36:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 22 Oct 2020 03:36:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 22 Oct 2020 03:36:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 03:36:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 03:36:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 22 Oct 2020 03:55:07 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 01 Dec 2020 04:01:21 GMT
ENV PHP_VERSION=7.4.13
# Tue, 01 Dec 2020 04:01:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Tue, 01 Dec 2020 04:01:22 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Tue, 01 Dec 2020 04:01:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 01 Dec 2020 04:01:40 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 01 Dec 2020 04:10:51 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 01 Dec 2020 04:10:52 GMT
COPY multi:afab483600631d4d87fe030871bbb016f1c2b73c0b72609d857bace419af7f5d in /usr/local/bin/ 
# Tue, 01 Dec 2020 04:10:54 GMT
RUN docker-php-ext-enable sodium
# Tue, 01 Dec 2020 04:10:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 01 Dec 2020 04:10:55 GMT
CMD ["php" "-a"]
# Tue, 01 Dec 2020 09:24:38 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Tue, 01 Dec 2020 09:24:38 GMT
STOPSIGNAL SIGINT
# Tue, 01 Dec 2020 09:24:39 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 01 Dec 2020 09:24:39 GMT
WORKDIR /var/www/html
# Tue, 01 Dec 2020 09:25:13 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Tue, 01 Dec 2020 09:25:13 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Mon, 07 Dec 2020 23:38:24 GMT
ENV ADMINER_VERSION=4.7.8
# Mon, 07 Dec 2020 23:38:24 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Mon, 07 Dec 2020 23:38:24 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Mon, 07 Dec 2020 23:38:26 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Mon, 07 Dec 2020 23:38:26 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Mon, 07 Dec 2020 23:38:26 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Mon, 07 Dec 2020 23:38:26 GMT
USER adminer
# Mon, 07 Dec 2020 23:38:26 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Mon, 07 Dec 2020 23:38:27 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:d6ca64ac6f4b6382142ce9a3501652938130a6ec4bb02f3f455ee1f980834cfe`  
		Last Modified: Thu, 22 Oct 2020 02:00:57 GMT  
		Size: 2.8 MB (2791407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30be8ffd290910905a5fb7cbb70252eb0f59edb09db20bdc21f3b65456acc28f`  
		Last Modified: Thu, 22 Oct 2020 05:10:23 GMT  
		Size: 1.4 MB (1439641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d58e2433b13446c863e85b34f8e4c93ca9d5b3b93d2bac415fd9cdf77bcec4`  
		Last Modified: Thu, 22 Oct 2020 05:10:21 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5729dcb8d303f82a7f8cf3df49048e34ce8ee89f79155fb08a475da46b64308`  
		Last Modified: Thu, 22 Oct 2020 05:10:21 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ffdca9b500ff910069fefe63b455206db2cf0fa00dc6b7c7d53219dfaf7f5b`  
		Last Modified: Tue, 01 Dec 2020 07:15:13 GMT  
		Size: 10.3 MB (10338561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c682383cda14fca62843652d7478a26995cfbbfbcb457985de4ca5cfb77de751`  
		Last Modified: Tue, 01 Dec 2020 07:15:12 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57833a53685f649182bdbb4194ba35390c17fa65a6b09c4e377a42a5f9aaca30`  
		Last Modified: Tue, 01 Dec 2020 07:15:18 GMT  
		Size: 14.9 MB (14942640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7003874a29c37e250b24c310b448d1c36607cdb1b43128071780d5fd0a0dc3e1`  
		Last Modified: Tue, 01 Dec 2020 07:15:12 GMT  
		Size: 2.3 KB (2259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fcfab619124f72931608ea142c1cd80a26871e1631380720b6be739170e21b6`  
		Last Modified: Tue, 01 Dec 2020 07:15:12 GMT  
		Size: 16.9 KB (16924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055719a49e04df90bb23499c98da9779637e3b44446a60f202283f57e4b29b04`  
		Last Modified: Tue, 01 Dec 2020 09:26:14 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2b0f52d9f107a35a34b4f8c69abbdf24f2de8a0431c812d74cb6dd3cbf8bf2`  
		Last Modified: Tue, 01 Dec 2020 09:26:13 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4edb5ffb9c3f753b4991debfaeef5c535ae5d689a18b7fff9f0b042c5883865`  
		Last Modified: Tue, 01 Dec 2020 09:26:14 GMT  
		Size: 4.5 MB (4519100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9258866f679eb2cbc89aa311d5d2dad0c146a7e9f61c9e805b63d7f324d2afb0`  
		Last Modified: Tue, 01 Dec 2020 09:26:13 GMT  
		Size: 1.5 KB (1472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:904e3ae5079e7cd06213e6912d4237663cff97a37e1ed247e24b7f455951eafe`  
		Last Modified: Mon, 07 Dec 2020 23:38:45 GMT  
		Size: 570.9 KB (570859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:362b319c8a865e06c57265a80b857954a02a4e09ffe3eda699eede128dcdef90`  
		Last Modified: Mon, 07 Dec 2020 23:38:45 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7` - linux; ppc64le

```console
$ docker pull adminer@sha256:73feff7b317d1078b173d0c1dc928c14bf61e94b4562a0a79132b9dac74739aa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 MB (35029016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2bacaef82d901426ed9bf50182af16a98e04172b1d2dac51b87db0885487f72`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 22 Oct 2020 11:00:06 GMT
ADD file:176e047fab2c1828575bffa6b14773efa297b7ecf312d86103c5dd4f78ec8027 in / 
# Thu, 22 Oct 2020 11:00:17 GMT
CMD ["/bin/sh"]
# Fri, 23 Oct 2020 00:21:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 23 Oct 2020 00:21:18 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 23 Oct 2020 00:21:30 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 23 Oct 2020 00:21:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 23 Oct 2020 00:21:44 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 23 Oct 2020 00:21:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 23 Oct 2020 00:21:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 23 Oct 2020 00:21:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 23 Oct 2020 00:34:37 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 01 Dec 2020 03:52:39 GMT
ENV PHP_VERSION=7.4.13
# Tue, 01 Dec 2020 03:52:44 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Tue, 01 Dec 2020 03:52:51 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Tue, 01 Dec 2020 03:53:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 01 Dec 2020 03:53:13 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 01 Dec 2020 03:57:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 01 Dec 2020 03:57:24 GMT
COPY multi:afab483600631d4d87fe030871bbb016f1c2b73c0b72609d857bace419af7f5d in /usr/local/bin/ 
# Tue, 01 Dec 2020 03:57:33 GMT
RUN docker-php-ext-enable sodium
# Tue, 01 Dec 2020 03:57:36 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 01 Dec 2020 03:57:39 GMT
CMD ["php" "-a"]
# Tue, 01 Dec 2020 07:09:03 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Tue, 01 Dec 2020 07:09:12 GMT
STOPSIGNAL SIGINT
# Tue, 01 Dec 2020 07:09:25 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 01 Dec 2020 07:09:32 GMT
WORKDIR /var/www/html
# Tue, 01 Dec 2020 07:10:30 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Tue, 01 Dec 2020 07:10:33 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Tue, 08 Dec 2020 00:16:36 GMT
ENV ADMINER_VERSION=4.7.8
# Tue, 08 Dec 2020 00:16:38 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Tue, 08 Dec 2020 00:16:41 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Tue, 08 Dec 2020 00:16:53 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Tue, 08 Dec 2020 00:16:54 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 08 Dec 2020 00:16:58 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Tue, 08 Dec 2020 00:17:11 GMT
USER adminer
# Tue, 08 Dec 2020 00:17:16 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 08 Dec 2020 00:17:18 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:692a9d763e196c85d79fc3e45b316b1bb557c93ba88a3c8ebf679a585d1efe73`  
		Last Modified: Thu, 22 Oct 2020 11:02:06 GMT  
		Size: 2.8 MB (2803218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0285d6f06f3beb1c140c055210664c441b93dd4f2037177a5396bce94ca16ce5`  
		Last Modified: Fri, 23 Oct 2020 01:34:08 GMT  
		Size: 1.4 MB (1383187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a6459a3bf272daa53ff4ba97cc849676f497de9f78d8e9378ec02552293f175`  
		Last Modified: Fri, 23 Oct 2020 01:34:07 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16cff6064dc29d3f629d353736c1cac074caa5b50738422adb84de99a019bb32`  
		Last Modified: Fri, 23 Oct 2020 01:34:08 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0baf560776c5dd75b5673be3d73b900119615cfc4e4fe24414486e3d1f11920`  
		Last Modified: Tue, 01 Dec 2020 05:50:29 GMT  
		Size: 10.3 MB (10338609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4d8083b683ead9a591a00aff14c8d0091665e1433d301a027b214f19cbe23f`  
		Last Modified: Tue, 01 Dec 2020 05:50:29 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7381e6ce3e117510e5a2bf102da48e3cc1b5fd3414651ec324bbe759d367be`  
		Last Modified: Tue, 01 Dec 2020 05:50:32 GMT  
		Size: 15.5 MB (15548036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8328c4e67c6b29f383993d05557e298bc834c18c00961b9ab2a1c4e4eb05b4fd`  
		Last Modified: Tue, 01 Dec 2020 05:50:28 GMT  
		Size: 2.3 KB (2259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:236813d0f57da4fa9c0d5938846f85e82a0a01ce89ca208916b8f649c0ee99fd`  
		Last Modified: Tue, 01 Dec 2020 05:50:28 GMT  
		Size: 17.0 KB (16965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acf7ec6b5baaa9faab722bfc6a7098e0871e3edb42be513e64fe8e06bc7edec1`  
		Last Modified: Tue, 01 Dec 2020 07:14:36 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c17363dc3aab754805ecdc74f39535a73cfc5f3cebe72a4cb18fdc97df1ef9fa`  
		Last Modified: Tue, 01 Dec 2020 07:14:33 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95753fdce29daf55de647d3a29a8cc07941f7bf95fec4a560b0d698478b782f3`  
		Last Modified: Tue, 01 Dec 2020 07:14:34 GMT  
		Size: 4.4 MB (4360119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cad5fcb53526734d41770680ea56047b6e13c767960fc1d0a0b8de7c7030c75`  
		Last Modified: Tue, 01 Dec 2020 07:14:33 GMT  
		Size: 1.5 KB (1474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b231a33566f06d48010343aac194149b1ce1613cf2397c67cf1be2984295f133`  
		Last Modified: Tue, 08 Dec 2020 00:18:38 GMT  
		Size: 570.9 KB (570925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628d0ad1cc992636ad6e5a1f0cf7de70d844c7cccb85cda16205dc67b167e131`  
		Last Modified: Tue, 08 Dec 2020 00:18:38 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7` - linux; s390x

```console
$ docker pull adminer@sha256:6b00709e793594a51832541158adeb2ae42e00829dbfb77a54bc0eef7fd1668d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32521955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f75d1bfddd1544fe2cddf65f0baa090dfb992c4a38b43b24670dc3b1ce037d7`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 11 Dec 2020 02:09:52 GMT
ADD file:c9395a36a4e03768aabd282eb1f31705cc00181d3147222d9c940eaa5a8fd511 in / 
# Fri, 11 Dec 2020 02:09:53 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 11:30:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 11 Dec 2020 11:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 11 Dec 2020 11:30:56 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 11 Dec 2020 11:30:57 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 11 Dec 2020 11:30:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 11 Dec 2020 11:30:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Dec 2020 11:31:00 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Dec 2020 11:31:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 11 Dec 2020 12:01:46 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 11 Dec 2020 12:01:46 GMT
ENV PHP_VERSION=7.4.13
# Fri, 11 Dec 2020 12:01:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Fri, 11 Dec 2020 12:01:48 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Fri, 11 Dec 2020 12:01:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 11 Dec 2020 12:01:54 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Dec 2020 12:08:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Dec 2020 12:08:47 GMT
COPY multi:afab483600631d4d87fe030871bbb016f1c2b73c0b72609d857bace419af7f5d in /usr/local/bin/ 
# Fri, 11 Dec 2020 12:08:49 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Dec 2020 12:08:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Dec 2020 12:08:50 GMT
CMD ["php" "-a"]
# Fri, 11 Dec 2020 18:43:30 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 11 Dec 2020 18:43:31 GMT
STOPSIGNAL SIGINT
# Fri, 11 Dec 2020 18:43:33 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 11 Dec 2020 18:43:33 GMT
WORKDIR /var/www/html
# Fri, 11 Dec 2020 18:44:50 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 11 Dec 2020 18:44:50 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 11 Dec 2020 18:44:51 GMT
ENV ADMINER_VERSION=4.7.8
# Fri, 11 Dec 2020 18:44:52 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Fri, 11 Dec 2020 18:44:52 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Fri, 11 Dec 2020 18:44:56 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 11 Dec 2020 18:44:57 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 11 Dec 2020 18:44:57 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 11 Dec 2020 18:44:58 GMT
USER adminer
# Fri, 11 Dec 2020 18:44:59 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 11 Dec 2020 18:44:59 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:7c2470fe3d16cb70fca0826168095a96838b1322a8cd1502b28284ee8561b491`  
		Last Modified: Fri, 11 Dec 2020 02:10:27 GMT  
		Size: 2.6 MB (2565988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a23c8359d30ae261ad953f292e6681a71ebc7388607b74d901bbc07f71e1311`  
		Last Modified: Fri, 11 Dec 2020 13:48:01 GMT  
		Size: 1.4 MB (1382587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01422c3e898d3241d4134256bf0d911b0752823227af04614187c79c187e2843`  
		Last Modified: Fri, 11 Dec 2020 13:48:03 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a0be2077abd44f96e50bdebb1ed93a6e2b8d504761c23fa0e5e9b87045ca38`  
		Last Modified: Fri, 11 Dec 2020 13:48:01 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267bafe0bb23009994a23ad5cdcc3b4d425f186f0e488b5f7461463ad1b53814`  
		Last Modified: Fri, 11 Dec 2020 13:50:24 GMT  
		Size: 10.3 MB (10338590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36304b0fbddac7ce44edacaedb902676688cfc3bb7082576f6b57eed0ccc133e`  
		Last Modified: Fri, 11 Dec 2020 13:50:25 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fa33489075ff6318ffc5a7cf5c94cb4ce65ccfc82b5970cc91628780c130aae`  
		Last Modified: Fri, 11 Dec 2020 13:50:26 GMT  
		Size: 13.5 MB (13485898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155ae451461e50390ae0db27a78a329e87a86b9f9eb04f6db81fcc27430f2d51`  
		Last Modified: Fri, 11 Dec 2020 13:50:24 GMT  
		Size: 2.3 KB (2257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b379111cc7023c652243c4d9234de47984fa307030d667bf14e5d12889ec8180`  
		Last Modified: Fri, 11 Dec 2020 13:50:24 GMT  
		Size: 16.9 KB (16879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a18e16d8efd7f249149e2d38813d86590cc4a55f23d8c5bbba970725422ea51`  
		Last Modified: Fri, 11 Dec 2020 18:47:13 GMT  
		Size: 310.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ba44137233477a93edb1e0cc94bee3ce4dafaed9ff932d21594190f861ef75`  
		Last Modified: Fri, 11 Dec 2020 18:47:13 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cba732448866bbb0e567b7510578f951e9cf0bc258588c8e898be1606e3a3eb`  
		Last Modified: Fri, 11 Dec 2020 18:47:11 GMT  
		Size: 4.2 MB (4153155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8faf5f39c5d146bc658625977adca6ce417bb45b9683bb1767b99abfea6d3d56`  
		Last Modified: Fri, 11 Dec 2020 18:47:11 GMT  
		Size: 1.5 KB (1473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008d2a285f2f6bcf687be0cb08b167a975a4d7534a16435da10ba2b75b2e2d73`  
		Last Modified: Fri, 11 Dec 2020 18:47:11 GMT  
		Size: 570.9 KB (570918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6852608d1b2324d98a56de31e6fc11ac1fe8e95f605b50c9f72db2bd5cd092`  
		Last Modified: Fri, 11 Dec 2020 18:47:12 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:4.7.8`

```console
$ docker pull adminer@sha256:4600f2453f7c9f3ee8179016a65d0b49a8dfb89467ac0947a6245e62e7f81fb1
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

### `adminer:4.7.8` - linux; amd64

```console
$ docker pull adminer@sha256:4b087576de7b4ca7c60bb3558f0b5ee30f496cee10fa19ea0a9f0e071c72b1f5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (33965375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2db7241b0f1461d8707525832e608fe513453f99c11beed9413194f7519e05`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 06:30:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 22 Oct 2020 06:30:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 22 Oct 2020 06:30:15 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 22 Oct 2020 06:30:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 22 Oct 2020 06:30:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 22 Oct 2020 06:30:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 06:30:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 06:30:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 22 Oct 2020 06:43:41 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 01 Dec 2020 04:36:20 GMT
ENV PHP_VERSION=7.4.13
# Tue, 01 Dec 2020 04:36:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Tue, 01 Dec 2020 04:36:21 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Tue, 01 Dec 2020 04:36:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 01 Dec 2020 04:36:27 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 01 Dec 2020 04:44:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 01 Dec 2020 04:44:54 GMT
COPY multi:afab483600631d4d87fe030871bbb016f1c2b73c0b72609d857bace419af7f5d in /usr/local/bin/ 
# Tue, 01 Dec 2020 04:44:57 GMT
RUN docker-php-ext-enable sodium
# Tue, 01 Dec 2020 04:44:57 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 01 Dec 2020 04:44:57 GMT
CMD ["php" "-a"]
# Tue, 01 Dec 2020 07:46:46 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Tue, 01 Dec 2020 07:46:46 GMT
STOPSIGNAL SIGINT
# Tue, 01 Dec 2020 07:46:47 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 01 Dec 2020 07:46:48 GMT
WORKDIR /var/www/html
# Tue, 01 Dec 2020 07:47:15 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Tue, 01 Dec 2020 07:47:15 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Tue, 08 Dec 2020 00:19:24 GMT
ENV ADMINER_VERSION=4.7.8
# Tue, 08 Dec 2020 00:19:24 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Tue, 08 Dec 2020 00:19:24 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Tue, 08 Dec 2020 00:19:26 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Tue, 08 Dec 2020 00:19:26 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 08 Dec 2020 00:19:26 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Tue, 08 Dec 2020 00:19:26 GMT
USER adminer
# Tue, 08 Dec 2020 00:19:27 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 08 Dec 2020 00:19:27 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f8bf6cfdbe614fef94f982905079c16e27b3de2d24eb1ff513d3d83e656ca2`  
		Last Modified: Thu, 22 Oct 2020 07:36:55 GMT  
		Size: 1.3 MB (1340771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce5be79740125b9e74a77885bf6ee2b0d25ac7ed9e9432c5aa7210bb3b00458a`  
		Last Modified: Thu, 22 Oct 2020 07:36:55 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99dd6507fe563b66ba35badf706e1bbb2d39eb5d0a3c0d5a86a45d2af7e89c1`  
		Last Modified: Thu, 22 Oct 2020 07:36:55 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c513a1b503cf7c9f18fa014dada9744070ded92dc9ad548cd056c4f56dc1a9`  
		Last Modified: Tue, 01 Dec 2020 07:27:10 GMT  
		Size: 10.3 MB (10338569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff080eafb4c0518981fca6aef4d239863fc59195f41ce7c440b2c6c518f2ac79`  
		Last Modified: Tue, 01 Dec 2020 07:27:09 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e818119992b11dbf09b710066a78920985b9ea1310fc8272df816e0884985f44`  
		Last Modified: Tue, 01 Dec 2020 07:27:13 GMT  
		Size: 14.6 MB (14572037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba3c14a67f95ae52ebfb558ab6b5d87687a05ce41c8df0a618ff42b73204e40`  
		Last Modified: Tue, 01 Dec 2020 07:27:09 GMT  
		Size: 2.3 KB (2257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbb0285b7ad2b170e4ed2cffbe0f16ba55d689c056ff43767834783eab7b8261`  
		Last Modified: Tue, 01 Dec 2020 07:27:09 GMT  
		Size: 17.0 KB (16987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae324cfad8acf03b3a98a15e963b7046404a7da3a6bbf68fd65d37f899f194d`  
		Last Modified: Tue, 01 Dec 2020 07:48:25 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb51158f683d66315de6fa572f7ea13d8ffb71ac85faa20c8578edb11678f37d`  
		Last Modified: Tue, 01 Dec 2020 07:48:23 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71ac21b64d1d63d967acb13664404babd0ef86fc896c484ce28cccf70001d0f1`  
		Last Modified: Tue, 01 Dec 2020 07:48:24 GMT  
		Size: 4.3 MB (4321455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2170e09d39d861e9bb7a5da5def906b44153b6c481fe17925ba82d1f1f78eec`  
		Last Modified: Tue, 01 Dec 2020 07:48:24 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d95b48dfa11f7f5c061f6522f6ff5d574452b8f321c6075455da2643b1967a`  
		Last Modified: Tue, 08 Dec 2020 00:19:45 GMT  
		Size: 570.9 KB (570860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3bb2b5e72bf0dbd4b855ddf65aaf9c0d077703804bdbdc9ea3ea98cbbfceaf6`  
		Last Modified: Tue, 08 Dec 2020 00:19:44 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7.8` - linux; arm variant v6

```console
$ docker pull adminer@sha256:7e114494e5e3a8ece382083d27c33f6c993695f0ff6c92c235ced149177f5da9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32073857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9cfa5ccbab063435267257cf4c761402c956233cf22775ed1c774b53a045715`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 11 Dec 2020 02:17:15 GMT
ADD file:1a9c0a67560d338c0c0e7005d8915d998fc9cf3e9f53bfd7e42e8391f0a39bce in / 
# Fri, 11 Dec 2020 02:17:15 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 07:04:50 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 11 Dec 2020 07:04:53 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 11 Dec 2020 07:04:55 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 11 Dec 2020 07:04:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 11 Dec 2020 07:04:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 11 Dec 2020 07:05:00 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Dec 2020 07:05:01 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Dec 2020 07:05:02 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 11 Dec 2020 07:13:50 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 11 Dec 2020 07:13:54 GMT
ENV PHP_VERSION=7.4.13
# Fri, 11 Dec 2020 07:13:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Fri, 11 Dec 2020 07:13:56 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Fri, 11 Dec 2020 07:14:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 11 Dec 2020 07:14:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Dec 2020 07:17:37 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Dec 2020 07:17:39 GMT
COPY multi:afab483600631d4d87fe030871bbb016f1c2b73c0b72609d857bace419af7f5d in /usr/local/bin/ 
# Fri, 11 Dec 2020 07:17:42 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Dec 2020 07:17:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Dec 2020 07:17:43 GMT
CMD ["php" "-a"]
# Fri, 11 Dec 2020 09:04:18 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 11 Dec 2020 09:04:19 GMT
STOPSIGNAL SIGINT
# Fri, 11 Dec 2020 09:04:21 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 11 Dec 2020 09:04:22 GMT
WORKDIR /var/www/html
# Fri, 11 Dec 2020 09:05:06 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 11 Dec 2020 09:05:08 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 11 Dec 2020 09:05:08 GMT
ENV ADMINER_VERSION=4.7.8
# Fri, 11 Dec 2020 09:05:09 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Fri, 11 Dec 2020 09:05:11 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Fri, 11 Dec 2020 09:05:14 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 11 Dec 2020 09:05:15 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 11 Dec 2020 09:05:16 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 11 Dec 2020 09:05:17 GMT
USER adminer
# Fri, 11 Dec 2020 09:05:18 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 11 Dec 2020 09:05:19 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:f1c16df8fee33d421d08790b17ca2af67a3fe49e77b6b991dd0c30631f5d1baf`  
		Last Modified: Fri, 11 Dec 2020 02:17:57 GMT  
		Size: 2.6 MB (2601992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623cc08cbe035cf15859e57a83e2243620418da06e1905d1875a46bec901e540`  
		Last Modified: Fri, 11 Dec 2020 07:56:49 GMT  
		Size: 1.3 MB (1310156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3a7aacff9b7ccf646f2bdbbc8d40bbb304550e813876049e721abd35461df9`  
		Last Modified: Fri, 11 Dec 2020 07:56:49 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d3214ea6f418597f370177309be7728f94481030c9cba6e45c4b74cfd04cc0`  
		Last Modified: Fri, 11 Dec 2020 07:56:49 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64de18534c9c3dd7212eceb5a285d571df578238ca4684a2e922b131e9947d79`  
		Last Modified: Fri, 11 Dec 2020 07:57:40 GMT  
		Size: 10.3 MB (10338603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d60b5c1c75b96676e4154f74a500fdd4a2645d4c51e189b0bdd18e06f26c3143`  
		Last Modified: Fri, 11 Dec 2020 07:57:39 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee32c3be90bc13cb4b3406c492ec35d5c211ac42b25e536939fb3220aea672b`  
		Last Modified: Fri, 11 Dec 2020 07:57:44 GMT  
		Size: 13.2 MB (13201116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e71cdda7d8acfe2fe1a6263c1b004b3ae972d7ce1c0ac95fec09aa0c0ba1f7fd`  
		Last Modified: Fri, 11 Dec 2020 07:57:39 GMT  
		Size: 2.3 KB (2258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec74a6ee1beba601eed5abe261394c8ddfa2d53093a1f6768356ec5891066746`  
		Last Modified: Fri, 11 Dec 2020 07:57:40 GMT  
		Size: 16.9 KB (16889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b84bf5ad218839b4e8156c322c5611b3c26167141a7c1e8049055deeda8b1ed5`  
		Last Modified: Fri, 11 Dec 2020 09:07:23 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0113ef6e65685219488d6543639cff152292617519f4649a6d7c8e4bbf03322b`  
		Last Modified: Fri, 11 Dec 2020 09:07:21 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2501c821a30d874046f30dd9d3947aa9f82cca3e9d39eb18214a765744e0b24`  
		Last Modified: Fri, 11 Dec 2020 09:07:21 GMT  
		Size: 4.0 MB (4026242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:945b172c5cf67a28a59e5b25cfed08871f360f551a912c8d7f64c096d6554812`  
		Last Modified: Fri, 11 Dec 2020 09:07:20 GMT  
		Size: 1.5 KB (1473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df40a3aa85441cb471ce645d5a0a2564fb9e2f042e078b8f04dd343488863a4`  
		Last Modified: Fri, 11 Dec 2020 09:07:20 GMT  
		Size: 570.9 KB (570917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90644dda17e22024741efd92b2987150a52659ae6bb25b7ea232e9b72d3b1d83`  
		Last Modified: Fri, 11 Dec 2020 09:07:20 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7.8` - linux; arm variant v7

```console
$ docker pull adminer@sha256:39b988e9485b8f06142e8584a4764c3c32159d51377eab0739b1cf794f701d1a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31186995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d4ed3310dfe2d29dd9a809a5ea826952ac518c5d93ab5e12054d9b7560791f7`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 22 Oct 2020 01:58:13 GMT
ADD file:46f89172426e9f5b1d669a2ca7ab218fc2deaef1caeeab88f2b5bd443ac9773d in / 
# Thu, 22 Oct 2020 01:58:14 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 06:47:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 22 Oct 2020 06:47:37 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 22 Oct 2020 06:47:45 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 22 Oct 2020 06:47:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 22 Oct 2020 06:47:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 22 Oct 2020 06:47:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 06:47:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 06:48:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 22 Oct 2020 06:56:26 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 01 Dec 2020 02:39:45 GMT
ENV PHP_VERSION=7.4.13
# Tue, 01 Dec 2020 02:39:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Tue, 01 Dec 2020 02:39:46 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Tue, 01 Dec 2020 02:39:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 01 Dec 2020 02:39:53 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 01 Dec 2020 02:42:30 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 01 Dec 2020 02:42:32 GMT
COPY multi:afab483600631d4d87fe030871bbb016f1c2b73c0b72609d857bace419af7f5d in /usr/local/bin/ 
# Tue, 01 Dec 2020 02:42:37 GMT
RUN docker-php-ext-enable sodium
# Tue, 01 Dec 2020 02:42:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 01 Dec 2020 02:42:40 GMT
CMD ["php" "-a"]
# Tue, 01 Dec 2020 04:28:04 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Tue, 01 Dec 2020 04:28:05 GMT
STOPSIGNAL SIGINT
# Tue, 01 Dec 2020 04:28:12 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 01 Dec 2020 04:28:14 GMT
WORKDIR /var/www/html
# Tue, 01 Dec 2020 04:29:07 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Tue, 01 Dec 2020 04:29:08 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Tue, 08 Dec 2020 00:00:44 GMT
ENV ADMINER_VERSION=4.7.8
# Tue, 08 Dec 2020 00:00:49 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Tue, 08 Dec 2020 00:00:52 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Tue, 08 Dec 2020 00:00:57 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Tue, 08 Dec 2020 00:00:58 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 08 Dec 2020 00:00:59 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Tue, 08 Dec 2020 00:00:59 GMT
USER adminer
# Tue, 08 Dec 2020 00:01:00 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 08 Dec 2020 00:01:01 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:5f2023fd85a4e68f37fe41421fd89f30e69b98a645613521c57c01317561eee3`  
		Last Modified: Thu, 22 Oct 2020 01:58:45 GMT  
		Size: 2.4 MB (2405675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60b50c98f8a8e2c6a27378dfa0f44df1844ac67c6981303675f138a42679f25`  
		Last Modified: Thu, 22 Oct 2020 07:35:57 GMT  
		Size: 1.2 MB (1214265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b472094d673b7c272085505c976192b9aaafa3157c99bade9755fbca18a24071`  
		Last Modified: Thu, 22 Oct 2020 07:35:56 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc39e5d916c11e7eb158e72d14ab981eb45ccc7b6451c1d6d3cb627b71cdbb6`  
		Last Modified: Thu, 22 Oct 2020 07:35:55 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e834fd39435ea86b08faf9b3af2e2623e0a247fa06dfe096decdf80f7a986a`  
		Last Modified: Tue, 01 Dec 2020 04:00:44 GMT  
		Size: 10.3 MB (10338583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a458e4d5704bca7330dbfab239f74ff255f4813b58f19f50a4ad7fd7087f0c8`  
		Last Modified: Tue, 01 Dec 2020 04:00:43 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a500121bbd97abb5116b6e95bdaa9aed74160334e46aadaabef548dca0edce6`  
		Last Modified: Tue, 01 Dec 2020 04:00:46 GMT  
		Size: 12.7 MB (12706582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3321b09ca6255e6f5cb4dce9057df675dd4644a3654424c7ee95fbdcb083e9c`  
		Last Modified: Tue, 01 Dec 2020 04:00:42 GMT  
		Size: 2.3 KB (2257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:345450fde280cf49e34f7246cebd38e311d4b7bebe22415a6126c18e67899f91`  
		Last Modified: Tue, 01 Dec 2020 04:00:42 GMT  
		Size: 16.9 KB (16903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:520112c186c5f2a097e8056a524b7c35704923ebeb6247e924ca839fe6e5b343`  
		Last Modified: Tue, 01 Dec 2020 04:31:36 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d98e04775b392470b2f426804979b34d740103414161d9c89f4df0d0b086e51`  
		Last Modified: Tue, 01 Dec 2020 04:31:34 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c074206a89c8b669d116ecf57544d500dcdc5379828bb10e531adf7af19b658a`  
		Last Modified: Tue, 01 Dec 2020 04:31:34 GMT  
		Size: 3.9 MB (3926108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137384dc891a62af154426c4b36cb9192967da61547507bc1b95301727f85c39`  
		Last Modified: Tue, 01 Dec 2020 04:31:34 GMT  
		Size: 1.5 KB (1473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfdcb3be5430d4c822996a4b1f107a12cafae7d60cc6faf1f7a7cdd8dacaab94`  
		Last Modified: Tue, 08 Dec 2020 00:01:41 GMT  
		Size: 570.9 KB (570924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e55c2ae42163732e674f91058ca3617c71403e138adb01dd23c943ad95d6b0`  
		Last Modified: Tue, 08 Dec 2020 00:01:41 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7.8` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:b1e09cd04824b43f07df33154a383bc15923451af616eaaae657aca0620d729f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33702279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea6b86a866d797b65cc54d7527a70e1a5e91bf21ecc1ee3fd22b2a2c18d7f6ed`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 07:18:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 22 Oct 2020 07:18:56 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 22 Oct 2020 07:18:59 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 22 Oct 2020 07:19:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 22 Oct 2020 07:19:04 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 22 Oct 2020 07:19:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 07:19:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 07:19:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 22 Oct 2020 07:27:59 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 01 Dec 2020 03:27:01 GMT
ENV PHP_VERSION=7.4.13
# Tue, 01 Dec 2020 03:27:02 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Tue, 01 Dec 2020 03:27:03 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Tue, 01 Dec 2020 03:27:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 01 Dec 2020 03:27:09 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 01 Dec 2020 03:30:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 01 Dec 2020 03:30:42 GMT
COPY multi:afab483600631d4d87fe030871bbb016f1c2b73c0b72609d857bace419af7f5d in /usr/local/bin/ 
# Tue, 01 Dec 2020 03:30:50 GMT
RUN docker-php-ext-enable sodium
# Tue, 01 Dec 2020 03:30:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 01 Dec 2020 03:30:56 GMT
CMD ["php" "-a"]
# Tue, 01 Dec 2020 08:12:36 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Tue, 01 Dec 2020 08:12:37 GMT
STOPSIGNAL SIGINT
# Tue, 01 Dec 2020 08:12:39 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 01 Dec 2020 08:12:40 GMT
WORKDIR /var/www/html
# Tue, 01 Dec 2020 08:13:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Tue, 01 Dec 2020 08:13:23 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Mon, 07 Dec 2020 23:39:52 GMT
ENV ADMINER_VERSION=4.7.8
# Mon, 07 Dec 2020 23:39:53 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Mon, 07 Dec 2020 23:39:54 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Mon, 07 Dec 2020 23:39:56 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Mon, 07 Dec 2020 23:39:57 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Mon, 07 Dec 2020 23:39:58 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Mon, 07 Dec 2020 23:39:58 GMT
USER adminer
# Mon, 07 Dec 2020 23:39:59 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Mon, 07 Dec 2020 23:40:00 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d57dba23203172f8fffd1379aef0307e782178b62dfc684d43c546f7e874ed`  
		Last Modified: Thu, 22 Oct 2020 08:06:21 GMT  
		Size: 1.3 MB (1342784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8414edb0c9c2f7472bb6228bf691a2ddac19ddad7bad789c7cbdc147aded711`  
		Last Modified: Thu, 22 Oct 2020 08:06:20 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d26eeef0db35b2328adae38a8490c7403844452c3606dd17fbe68216f98e82`  
		Last Modified: Thu, 22 Oct 2020 08:06:19 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29be11fa56be3ca1af1498b259f3d5e058a869970cac6d670cf4ca1502485810`  
		Last Modified: Tue, 01 Dec 2020 04:53:56 GMT  
		Size: 10.3 MB (10338597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a553892b0358f6f72064d4dd5e727b686c4461cca7ea8a1211cc86adddb2cb`  
		Last Modified: Tue, 01 Dec 2020 04:53:56 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:828f98d07be67a182899230fc7e38e513de6ce85178d60116c765e90ffbc4119`  
		Last Modified: Tue, 01 Dec 2020 04:54:00 GMT  
		Size: 14.4 MB (14386945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec168016016eef2bef46796f7d7ec48af2459e14d65b9fc2871e756fe3e14d6a`  
		Last Modified: Tue, 01 Dec 2020 04:53:56 GMT  
		Size: 2.3 KB (2260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca32a186f8576115bc6fffe021ff54c52337662fa3cdb51c863d12d20ba02de`  
		Last Modified: Tue, 01 Dec 2020 04:53:55 GMT  
		Size: 17.0 KB (16976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b859cea4a3bb568911dd8f097b1a684daef31726fc5a591b4d9cd57b35187f`  
		Last Modified: Tue, 01 Dec 2020 08:14:59 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e97602a3ba690a845f8ecfaabcff93f82efc85a36445f6413d26f2482987638`  
		Last Modified: Tue, 01 Dec 2020 08:14:56 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6067b9bb9a3850bc39e227d17ab5df99a9bbe61e6d9933fc63c85e464f4aedf5`  
		Last Modified: Tue, 01 Dec 2020 08:14:57 GMT  
		Size: 4.3 MB (4331540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c677bbe386af33259d80d8f4d08a7147fef67adf472b9d841dac1a4a118c7f`  
		Last Modified: Tue, 01 Dec 2020 08:14:57 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4763c08ec3b1c7b68505b48ed92faf18a62525f8ce02d4fba750c232c1826aa9`  
		Last Modified: Mon, 07 Dec 2020 23:40:27 GMT  
		Size: 570.9 KB (570924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:983b1fb60b2afcee1aa424434071184fe8cf507838ac872e30e48755b41f1232`  
		Last Modified: Mon, 07 Dec 2020 23:40:28 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7.8` - linux; 386

```console
$ docker pull adminer@sha256:13a4c7ddafd6d4d6a5ee85529f6fa01ebe99d5c5bc1bcafafc85425658693817
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34626966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bb37df3c96977a9c7d5bcff85e2f3904eb30a1d4e2358f0c1644fae769a3ea7`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 22 Oct 2020 02:00:33 GMT
ADD file:46ad43b4984bcf49c5a888ff3628f23161f55cd1fb062f469e707100c97fa254 in / 
# Thu, 22 Oct 2020 02:00:33 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:36:23 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 22 Oct 2020 03:36:26 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 22 Oct 2020 03:36:27 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 22 Oct 2020 03:36:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 22 Oct 2020 03:36:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 22 Oct 2020 03:36:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 03:36:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 03:36:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 22 Oct 2020 03:55:07 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 01 Dec 2020 04:01:21 GMT
ENV PHP_VERSION=7.4.13
# Tue, 01 Dec 2020 04:01:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Tue, 01 Dec 2020 04:01:22 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Tue, 01 Dec 2020 04:01:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 01 Dec 2020 04:01:40 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 01 Dec 2020 04:10:51 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 01 Dec 2020 04:10:52 GMT
COPY multi:afab483600631d4d87fe030871bbb016f1c2b73c0b72609d857bace419af7f5d in /usr/local/bin/ 
# Tue, 01 Dec 2020 04:10:54 GMT
RUN docker-php-ext-enable sodium
# Tue, 01 Dec 2020 04:10:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 01 Dec 2020 04:10:55 GMT
CMD ["php" "-a"]
# Tue, 01 Dec 2020 09:24:38 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Tue, 01 Dec 2020 09:24:38 GMT
STOPSIGNAL SIGINT
# Tue, 01 Dec 2020 09:24:39 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 01 Dec 2020 09:24:39 GMT
WORKDIR /var/www/html
# Tue, 01 Dec 2020 09:25:13 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Tue, 01 Dec 2020 09:25:13 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Mon, 07 Dec 2020 23:38:24 GMT
ENV ADMINER_VERSION=4.7.8
# Mon, 07 Dec 2020 23:38:24 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Mon, 07 Dec 2020 23:38:24 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Mon, 07 Dec 2020 23:38:26 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Mon, 07 Dec 2020 23:38:26 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Mon, 07 Dec 2020 23:38:26 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Mon, 07 Dec 2020 23:38:26 GMT
USER adminer
# Mon, 07 Dec 2020 23:38:26 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Mon, 07 Dec 2020 23:38:27 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:d6ca64ac6f4b6382142ce9a3501652938130a6ec4bb02f3f455ee1f980834cfe`  
		Last Modified: Thu, 22 Oct 2020 02:00:57 GMT  
		Size: 2.8 MB (2791407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30be8ffd290910905a5fb7cbb70252eb0f59edb09db20bdc21f3b65456acc28f`  
		Last Modified: Thu, 22 Oct 2020 05:10:23 GMT  
		Size: 1.4 MB (1439641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d58e2433b13446c863e85b34f8e4c93ca9d5b3b93d2bac415fd9cdf77bcec4`  
		Last Modified: Thu, 22 Oct 2020 05:10:21 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5729dcb8d303f82a7f8cf3df49048e34ce8ee89f79155fb08a475da46b64308`  
		Last Modified: Thu, 22 Oct 2020 05:10:21 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ffdca9b500ff910069fefe63b455206db2cf0fa00dc6b7c7d53219dfaf7f5b`  
		Last Modified: Tue, 01 Dec 2020 07:15:13 GMT  
		Size: 10.3 MB (10338561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c682383cda14fca62843652d7478a26995cfbbfbcb457985de4ca5cfb77de751`  
		Last Modified: Tue, 01 Dec 2020 07:15:12 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57833a53685f649182bdbb4194ba35390c17fa65a6b09c4e377a42a5f9aaca30`  
		Last Modified: Tue, 01 Dec 2020 07:15:18 GMT  
		Size: 14.9 MB (14942640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7003874a29c37e250b24c310b448d1c36607cdb1b43128071780d5fd0a0dc3e1`  
		Last Modified: Tue, 01 Dec 2020 07:15:12 GMT  
		Size: 2.3 KB (2259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fcfab619124f72931608ea142c1cd80a26871e1631380720b6be739170e21b6`  
		Last Modified: Tue, 01 Dec 2020 07:15:12 GMT  
		Size: 16.9 KB (16924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055719a49e04df90bb23499c98da9779637e3b44446a60f202283f57e4b29b04`  
		Last Modified: Tue, 01 Dec 2020 09:26:14 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2b0f52d9f107a35a34b4f8c69abbdf24f2de8a0431c812d74cb6dd3cbf8bf2`  
		Last Modified: Tue, 01 Dec 2020 09:26:13 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4edb5ffb9c3f753b4991debfaeef5c535ae5d689a18b7fff9f0b042c5883865`  
		Last Modified: Tue, 01 Dec 2020 09:26:14 GMT  
		Size: 4.5 MB (4519100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9258866f679eb2cbc89aa311d5d2dad0c146a7e9f61c9e805b63d7f324d2afb0`  
		Last Modified: Tue, 01 Dec 2020 09:26:13 GMT  
		Size: 1.5 KB (1472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:904e3ae5079e7cd06213e6912d4237663cff97a37e1ed247e24b7f455951eafe`  
		Last Modified: Mon, 07 Dec 2020 23:38:45 GMT  
		Size: 570.9 KB (570859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:362b319c8a865e06c57265a80b857954a02a4e09ffe3eda699eede128dcdef90`  
		Last Modified: Mon, 07 Dec 2020 23:38:45 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7.8` - linux; ppc64le

```console
$ docker pull adminer@sha256:73feff7b317d1078b173d0c1dc928c14bf61e94b4562a0a79132b9dac74739aa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 MB (35029016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2bacaef82d901426ed9bf50182af16a98e04172b1d2dac51b87db0885487f72`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 22 Oct 2020 11:00:06 GMT
ADD file:176e047fab2c1828575bffa6b14773efa297b7ecf312d86103c5dd4f78ec8027 in / 
# Thu, 22 Oct 2020 11:00:17 GMT
CMD ["/bin/sh"]
# Fri, 23 Oct 2020 00:21:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 23 Oct 2020 00:21:18 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 23 Oct 2020 00:21:30 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 23 Oct 2020 00:21:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 23 Oct 2020 00:21:44 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 23 Oct 2020 00:21:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 23 Oct 2020 00:21:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 23 Oct 2020 00:21:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 23 Oct 2020 00:34:37 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 01 Dec 2020 03:52:39 GMT
ENV PHP_VERSION=7.4.13
# Tue, 01 Dec 2020 03:52:44 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Tue, 01 Dec 2020 03:52:51 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Tue, 01 Dec 2020 03:53:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 01 Dec 2020 03:53:13 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 01 Dec 2020 03:57:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 01 Dec 2020 03:57:24 GMT
COPY multi:afab483600631d4d87fe030871bbb016f1c2b73c0b72609d857bace419af7f5d in /usr/local/bin/ 
# Tue, 01 Dec 2020 03:57:33 GMT
RUN docker-php-ext-enable sodium
# Tue, 01 Dec 2020 03:57:36 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 01 Dec 2020 03:57:39 GMT
CMD ["php" "-a"]
# Tue, 01 Dec 2020 07:09:03 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Tue, 01 Dec 2020 07:09:12 GMT
STOPSIGNAL SIGINT
# Tue, 01 Dec 2020 07:09:25 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 01 Dec 2020 07:09:32 GMT
WORKDIR /var/www/html
# Tue, 01 Dec 2020 07:10:30 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Tue, 01 Dec 2020 07:10:33 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Tue, 08 Dec 2020 00:16:36 GMT
ENV ADMINER_VERSION=4.7.8
# Tue, 08 Dec 2020 00:16:38 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Tue, 08 Dec 2020 00:16:41 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Tue, 08 Dec 2020 00:16:53 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Tue, 08 Dec 2020 00:16:54 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 08 Dec 2020 00:16:58 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Tue, 08 Dec 2020 00:17:11 GMT
USER adminer
# Tue, 08 Dec 2020 00:17:16 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 08 Dec 2020 00:17:18 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:692a9d763e196c85d79fc3e45b316b1bb557c93ba88a3c8ebf679a585d1efe73`  
		Last Modified: Thu, 22 Oct 2020 11:02:06 GMT  
		Size: 2.8 MB (2803218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0285d6f06f3beb1c140c055210664c441b93dd4f2037177a5396bce94ca16ce5`  
		Last Modified: Fri, 23 Oct 2020 01:34:08 GMT  
		Size: 1.4 MB (1383187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a6459a3bf272daa53ff4ba97cc849676f497de9f78d8e9378ec02552293f175`  
		Last Modified: Fri, 23 Oct 2020 01:34:07 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16cff6064dc29d3f629d353736c1cac074caa5b50738422adb84de99a019bb32`  
		Last Modified: Fri, 23 Oct 2020 01:34:08 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0baf560776c5dd75b5673be3d73b900119615cfc4e4fe24414486e3d1f11920`  
		Last Modified: Tue, 01 Dec 2020 05:50:29 GMT  
		Size: 10.3 MB (10338609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4d8083b683ead9a591a00aff14c8d0091665e1433d301a027b214f19cbe23f`  
		Last Modified: Tue, 01 Dec 2020 05:50:29 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7381e6ce3e117510e5a2bf102da48e3cc1b5fd3414651ec324bbe759d367be`  
		Last Modified: Tue, 01 Dec 2020 05:50:32 GMT  
		Size: 15.5 MB (15548036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8328c4e67c6b29f383993d05557e298bc834c18c00961b9ab2a1c4e4eb05b4fd`  
		Last Modified: Tue, 01 Dec 2020 05:50:28 GMT  
		Size: 2.3 KB (2259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:236813d0f57da4fa9c0d5938846f85e82a0a01ce89ca208916b8f649c0ee99fd`  
		Last Modified: Tue, 01 Dec 2020 05:50:28 GMT  
		Size: 17.0 KB (16965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acf7ec6b5baaa9faab722bfc6a7098e0871e3edb42be513e64fe8e06bc7edec1`  
		Last Modified: Tue, 01 Dec 2020 07:14:36 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c17363dc3aab754805ecdc74f39535a73cfc5f3cebe72a4cb18fdc97df1ef9fa`  
		Last Modified: Tue, 01 Dec 2020 07:14:33 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95753fdce29daf55de647d3a29a8cc07941f7bf95fec4a560b0d698478b782f3`  
		Last Modified: Tue, 01 Dec 2020 07:14:34 GMT  
		Size: 4.4 MB (4360119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cad5fcb53526734d41770680ea56047b6e13c767960fc1d0a0b8de7c7030c75`  
		Last Modified: Tue, 01 Dec 2020 07:14:33 GMT  
		Size: 1.5 KB (1474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b231a33566f06d48010343aac194149b1ce1613cf2397c67cf1be2984295f133`  
		Last Modified: Tue, 08 Dec 2020 00:18:38 GMT  
		Size: 570.9 KB (570925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628d0ad1cc992636ad6e5a1f0cf7de70d844c7cccb85cda16205dc67b167e131`  
		Last Modified: Tue, 08 Dec 2020 00:18:38 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7.8` - linux; s390x

```console
$ docker pull adminer@sha256:6b00709e793594a51832541158adeb2ae42e00829dbfb77a54bc0eef7fd1668d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32521955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f75d1bfddd1544fe2cddf65f0baa090dfb992c4a38b43b24670dc3b1ce037d7`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 11 Dec 2020 02:09:52 GMT
ADD file:c9395a36a4e03768aabd282eb1f31705cc00181d3147222d9c940eaa5a8fd511 in / 
# Fri, 11 Dec 2020 02:09:53 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 11:30:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 11 Dec 2020 11:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 11 Dec 2020 11:30:56 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 11 Dec 2020 11:30:57 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 11 Dec 2020 11:30:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 11 Dec 2020 11:30:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Dec 2020 11:31:00 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Dec 2020 11:31:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 11 Dec 2020 12:01:46 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 11 Dec 2020 12:01:46 GMT
ENV PHP_VERSION=7.4.13
# Fri, 11 Dec 2020 12:01:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Fri, 11 Dec 2020 12:01:48 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Fri, 11 Dec 2020 12:01:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 11 Dec 2020 12:01:54 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Dec 2020 12:08:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Dec 2020 12:08:47 GMT
COPY multi:afab483600631d4d87fe030871bbb016f1c2b73c0b72609d857bace419af7f5d in /usr/local/bin/ 
# Fri, 11 Dec 2020 12:08:49 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Dec 2020 12:08:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Dec 2020 12:08:50 GMT
CMD ["php" "-a"]
# Fri, 11 Dec 2020 18:43:30 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 11 Dec 2020 18:43:31 GMT
STOPSIGNAL SIGINT
# Fri, 11 Dec 2020 18:43:33 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 11 Dec 2020 18:43:33 GMT
WORKDIR /var/www/html
# Fri, 11 Dec 2020 18:44:50 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 11 Dec 2020 18:44:50 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 11 Dec 2020 18:44:51 GMT
ENV ADMINER_VERSION=4.7.8
# Fri, 11 Dec 2020 18:44:52 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Fri, 11 Dec 2020 18:44:52 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Fri, 11 Dec 2020 18:44:56 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 11 Dec 2020 18:44:57 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 11 Dec 2020 18:44:57 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 11 Dec 2020 18:44:58 GMT
USER adminer
# Fri, 11 Dec 2020 18:44:59 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 11 Dec 2020 18:44:59 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:7c2470fe3d16cb70fca0826168095a96838b1322a8cd1502b28284ee8561b491`  
		Last Modified: Fri, 11 Dec 2020 02:10:27 GMT  
		Size: 2.6 MB (2565988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a23c8359d30ae261ad953f292e6681a71ebc7388607b74d901bbc07f71e1311`  
		Last Modified: Fri, 11 Dec 2020 13:48:01 GMT  
		Size: 1.4 MB (1382587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01422c3e898d3241d4134256bf0d911b0752823227af04614187c79c187e2843`  
		Last Modified: Fri, 11 Dec 2020 13:48:03 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a0be2077abd44f96e50bdebb1ed93a6e2b8d504761c23fa0e5e9b87045ca38`  
		Last Modified: Fri, 11 Dec 2020 13:48:01 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267bafe0bb23009994a23ad5cdcc3b4d425f186f0e488b5f7461463ad1b53814`  
		Last Modified: Fri, 11 Dec 2020 13:50:24 GMT  
		Size: 10.3 MB (10338590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36304b0fbddac7ce44edacaedb902676688cfc3bb7082576f6b57eed0ccc133e`  
		Last Modified: Fri, 11 Dec 2020 13:50:25 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fa33489075ff6318ffc5a7cf5c94cb4ce65ccfc82b5970cc91628780c130aae`  
		Last Modified: Fri, 11 Dec 2020 13:50:26 GMT  
		Size: 13.5 MB (13485898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155ae451461e50390ae0db27a78a329e87a86b9f9eb04f6db81fcc27430f2d51`  
		Last Modified: Fri, 11 Dec 2020 13:50:24 GMT  
		Size: 2.3 KB (2257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b379111cc7023c652243c4d9234de47984fa307030d667bf14e5d12889ec8180`  
		Last Modified: Fri, 11 Dec 2020 13:50:24 GMT  
		Size: 16.9 KB (16879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a18e16d8efd7f249149e2d38813d86590cc4a55f23d8c5bbba970725422ea51`  
		Last Modified: Fri, 11 Dec 2020 18:47:13 GMT  
		Size: 310.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ba44137233477a93edb1e0cc94bee3ce4dafaed9ff932d21594190f861ef75`  
		Last Modified: Fri, 11 Dec 2020 18:47:13 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cba732448866bbb0e567b7510578f951e9cf0bc258588c8e898be1606e3a3eb`  
		Last Modified: Fri, 11 Dec 2020 18:47:11 GMT  
		Size: 4.2 MB (4153155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8faf5f39c5d146bc658625977adca6ce417bb45b9683bb1767b99abfea6d3d56`  
		Last Modified: Fri, 11 Dec 2020 18:47:11 GMT  
		Size: 1.5 KB (1473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008d2a285f2f6bcf687be0cb08b167a975a4d7534a16435da10ba2b75b2e2d73`  
		Last Modified: Fri, 11 Dec 2020 18:47:11 GMT  
		Size: 570.9 KB (570918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6852608d1b2324d98a56de31e6fc11ac1fe8e95f605b50c9f72db2bd5cd092`  
		Last Modified: Fri, 11 Dec 2020 18:47:12 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:4.7.8-fastcgi`

```console
$ docker pull adminer@sha256:c0bcea38afeb9296d883e7371a4b83a97384f02ed2d2c3e71a6823267d6f0bac
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

### `adminer:4.7.8-fastcgi` - linux; amd64

```console
$ docker pull adminer@sha256:fb2f45c8e550ba3d59351c5ab1ac746adcab7dfb5e2d0b2a27531d2b664f598b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (34042656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff0774240cbda9b72e1940dc60ecd8366d3b4df4e789a7284078c8698364477`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 06:30:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 22 Oct 2020 06:30:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 22 Oct 2020 06:30:15 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 22 Oct 2020 06:30:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 22 Oct 2020 06:30:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 22 Oct 2020 06:37:19 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Thu, 22 Oct 2020 06:37:19 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 06:37:19 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 06:37:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 22 Oct 2020 06:49:00 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 01 Dec 2020 04:45:15 GMT
ENV PHP_VERSION=7.4.13
# Tue, 01 Dec 2020 04:45:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Tue, 01 Dec 2020 04:45:15 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Tue, 01 Dec 2020 04:45:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 01 Dec 2020 04:45:21 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 01 Dec 2020 04:54:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 01 Dec 2020 04:54:04 GMT
COPY multi:ebc915bbde1078ce3122b918e2e4c7726858af785343ade1a8d1a94f1052a4c7 in /usr/local/bin/ 
# Tue, 01 Dec 2020 04:54:07 GMT
RUN docker-php-ext-enable sodium
# Tue, 01 Dec 2020 04:54:07 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 01 Dec 2020 04:54:08 GMT
WORKDIR /var/www/html
# Tue, 01 Dec 2020 04:54:09 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Tue, 01 Dec 2020 04:54:10 GMT
STOPSIGNAL SIGQUIT
# Tue, 01 Dec 2020 04:54:10 GMT
EXPOSE 9000
# Tue, 01 Dec 2020 04:54:11 GMT
CMD ["php-fpm"]
# Tue, 01 Dec 2020 07:47:26 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Tue, 01 Dec 2020 07:47:28 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 01 Dec 2020 07:48:01 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Tue, 01 Dec 2020 07:48:01 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Tue, 08 Dec 2020 00:19:31 GMT
ENV ADMINER_VERSION=4.7.8
# Tue, 08 Dec 2020 00:19:31 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Tue, 08 Dec 2020 00:19:31 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Tue, 08 Dec 2020 00:19:33 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Tue, 08 Dec 2020 00:19:33 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 08 Dec 2020 00:19:33 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Tue, 08 Dec 2020 00:19:33 GMT
USER adminer
# Tue, 08 Dec 2020 00:19:33 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f8bf6cfdbe614fef94f982905079c16e27b3de2d24eb1ff513d3d83e656ca2`  
		Last Modified: Thu, 22 Oct 2020 07:36:55 GMT  
		Size: 1.3 MB (1340771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce5be79740125b9e74a77885bf6ee2b0d25ac7ed9e9432c5aa7210bb3b00458a`  
		Last Modified: Thu, 22 Oct 2020 07:36:55 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99dd6507fe563b66ba35badf706e1bbb2d39eb5d0a3c0d5a86a45d2af7e89c1`  
		Last Modified: Thu, 22 Oct 2020 07:36:55 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c3b45daa37929dd9a002107adb1299c5b070bbba60b73cf9ecc2d9fd6e78f9`  
		Last Modified: Tue, 01 Dec 2020 07:27:28 GMT  
		Size: 10.3 MB (10338571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6afb095daafcd5f742a42ee6dbf8f6d03fdca63c22071198f243df20ecef1db9`  
		Last Modified: Tue, 01 Dec 2020 07:27:25 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838cecfde999e9ecf65003522df2ce13e12fa5190e2336ffb1d16da9a787ead4`  
		Last Modified: Tue, 01 Dec 2020 07:27:29 GMT  
		Size: 14.6 MB (14640876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a46b7ab0f2d19433340bdeca3307275efd3188c446a3c739c1196c9bd05a0e`  
		Last Modified: Tue, 01 Dec 2020 07:27:26 GMT  
		Size: 2.3 KB (2255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d2139a9b9d18bdd892644fe463b368727e54ba53b145694a26f4cfe3f8e61d1`  
		Last Modified: Tue, 01 Dec 2020 07:27:26 GMT  
		Size: 17.0 KB (16987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f68d34619f5f9cff2cfac13cfa06e31e832bf261751b75ee11561cd3375e0207`  
		Last Modified: Tue, 01 Dec 2020 07:27:26 GMT  
		Size: 8.4 KB (8446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6bf2c8a87f5c9551aa94f68cd8ea11b9fb2f222d8cd8cdaf96b58fe86c98897`  
		Last Modified: Tue, 01 Dec 2020 07:48:39 GMT  
		Size: 310.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f16b55f73f8f895e7f07bc76cbc0c40ed52e4032e2129a9dbf41c7cb907c9e`  
		Last Modified: Tue, 01 Dec 2020 07:48:37 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a4fbbf03b1e145da6329a1d517b4ddaafee96bc3623a9dea8fcf2d3b1309ce4`  
		Last Modified: Tue, 01 Dec 2020 07:48:38 GMT  
		Size: 4.3 MB (4321450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b75ee2a57910d59b9ac6cb6de554264966343ef9391893d44eaf344ebca1bdc`  
		Last Modified: Tue, 01 Dec 2020 07:48:38 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12530476c9fea755fef449d62308ae3022da470522b4598087fcd3eb5bf68f7d`  
		Last Modified: Tue, 08 Dec 2020 00:19:56 GMT  
		Size: 570.9 KB (570859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5723a03bb2a4c99d35468a1f3e68d687f33c81fdce68c56aac53b1c689b5542`  
		Last Modified: Tue, 08 Dec 2020 00:19:55 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7.8-fastcgi` - linux; arm variant v6

```console
$ docker pull adminer@sha256:689204154221d2e4a097c834af056b991f880aed7a5a4a1e54d6c4422d965a6f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32149046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bb1805eba8cd29a4f28de65c3c539bac32ead0206c065984c55d1a699fd3b81`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 11 Dec 2020 02:17:15 GMT
ADD file:1a9c0a67560d338c0c0e7005d8915d998fc9cf3e9f53bfd7e42e8391f0a39bce in / 
# Fri, 11 Dec 2020 02:17:15 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 07:04:50 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 11 Dec 2020 07:04:53 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 11 Dec 2020 07:04:55 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 11 Dec 2020 07:04:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 11 Dec 2020 07:04:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 11 Dec 2020 07:09:12 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Fri, 11 Dec 2020 07:09:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Dec 2020 07:09:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Dec 2020 07:09:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 11 Dec 2020 07:17:56 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 11 Dec 2020 07:17:57 GMT
ENV PHP_VERSION=7.4.13
# Fri, 11 Dec 2020 07:17:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Fri, 11 Dec 2020 07:17:58 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Fri, 11 Dec 2020 07:18:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 11 Dec 2020 07:18:05 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Dec 2020 07:21:46 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Dec 2020 07:21:47 GMT
COPY multi:ebc915bbde1078ce3122b918e2e4c7726858af785343ade1a8d1a94f1052a4c7 in /usr/local/bin/ 
# Fri, 11 Dec 2020 07:21:51 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Dec 2020 07:21:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Dec 2020 07:21:53 GMT
WORKDIR /var/www/html
# Fri, 11 Dec 2020 07:21:56 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 11 Dec 2020 07:21:57 GMT
STOPSIGNAL SIGQUIT
# Fri, 11 Dec 2020 07:21:58 GMT
EXPOSE 9000
# Fri, 11 Dec 2020 07:21:59 GMT
CMD ["php-fpm"]
# Fri, 11 Dec 2020 09:05:35 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 11 Dec 2020 09:05:38 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 11 Dec 2020 09:06:36 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 11 Dec 2020 09:06:37 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 11 Dec 2020 09:06:38 GMT
ENV ADMINER_VERSION=4.7.8
# Fri, 11 Dec 2020 09:06:40 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Fri, 11 Dec 2020 09:06:41 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Fri, 11 Dec 2020 09:06:45 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 11 Dec 2020 09:06:46 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 11 Dec 2020 09:06:48 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 11 Dec 2020 09:06:50 GMT
USER adminer
# Fri, 11 Dec 2020 09:06:52 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:f1c16df8fee33d421d08790b17ca2af67a3fe49e77b6b991dd0c30631f5d1baf`  
		Last Modified: Fri, 11 Dec 2020 02:17:57 GMT  
		Size: 2.6 MB (2601992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623cc08cbe035cf15859e57a83e2243620418da06e1905d1875a46bec901e540`  
		Last Modified: Fri, 11 Dec 2020 07:56:49 GMT  
		Size: 1.3 MB (1310156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3a7aacff9b7ccf646f2bdbbc8d40bbb304550e813876049e721abd35461df9`  
		Last Modified: Fri, 11 Dec 2020 07:56:49 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d3214ea6f418597f370177309be7728f94481030c9cba6e45c4b74cfd04cc0`  
		Last Modified: Fri, 11 Dec 2020 07:56:49 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dff7159949c3c97335dda12e61ad77a87a4125ef93f88655500f4b8057cd38ca`  
		Last Modified: Fri, 11 Dec 2020 07:58:09 GMT  
		Size: 10.3 MB (10338600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c2c2f22a036ec3f2efaed4fd97c10faee4bbf539b56bf2e11b84a7c05b78fa`  
		Last Modified: Fri, 11 Dec 2020 07:58:05 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae33a5a224fa1ee298562bc31d50c9f804652bf619e4836e852c8860c5c49318`  
		Last Modified: Fri, 11 Dec 2020 07:58:09 GMT  
		Size: 13.3 MB (13267849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53c09a76a513338db42015101706a8bf9c7309d298d0a3329dee74810ea39db7`  
		Last Modified: Fri, 11 Dec 2020 07:58:05 GMT  
		Size: 2.3 KB (2260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e47c9c32a85f1170c19a3745c3a661a3a3c13e50daddef9919f624a52a70bc30`  
		Last Modified: Fri, 11 Dec 2020 07:58:05 GMT  
		Size: 16.9 KB (16891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbe39bbdfd22c5c467c010b89eb9561741273f56a2f378e08f2e055ef9ed919`  
		Last Modified: Fri, 11 Dec 2020 07:58:05 GMT  
		Size: 8.4 KB (8446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb3c1470d540138d5b667c3d6e30a34a3b783541ba0dc69a9714fa432a923970`  
		Last Modified: Fri, 11 Dec 2020 09:07:48 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f70879cf7eb8183ab6f68ad5f05f07b3e91a88ca27f7d935e91892073b1376`  
		Last Modified: Fri, 11 Dec 2020 09:07:46 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f69f96ec941427956045eb3c5673c21715d1878daf9035b7d11122c8cf62ed0c`  
		Last Modified: Fri, 11 Dec 2020 09:07:46 GMT  
		Size: 4.0 MB (4026251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a629622e0e5f22c28c625e3b6a9bef5d2136d403a64f88e8a44b1f1088caec2d`  
		Last Modified: Fri, 11 Dec 2020 09:07:45 GMT  
		Size: 1.5 KB (1470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec25251b0aa5ef178648ab40613c0031a55f133641f36b6c6e74dc5e79e4764`  
		Last Modified: Fri, 11 Dec 2020 09:07:46 GMT  
		Size: 570.9 KB (570918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71d17d806f1955405b240a9ef740c540c9e8ec5ceb8686ec081fda180677e50c`  
		Last Modified: Fri, 11 Dec 2020 09:07:45 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7.8-fastcgi` - linux; arm variant v7

```console
$ docker pull adminer@sha256:226eabf37d80fa4c86dc5fd621ba0b5c211967752c3e972a3929b9ffc4f4387c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31261925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efcd4d51f3642b6795c4c7140eaab8183af5f3b781a9099b95e1eba7d94d5683`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 22 Oct 2020 01:58:13 GMT
ADD file:46f89172426e9f5b1d669a2ca7ab218fc2deaef1caeeab88f2b5bd443ac9773d in / 
# Thu, 22 Oct 2020 01:58:14 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 06:47:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 22 Oct 2020 06:47:37 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 22 Oct 2020 06:47:45 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 22 Oct 2020 06:47:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 22 Oct 2020 06:47:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 22 Oct 2020 06:51:33 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Thu, 22 Oct 2020 06:51:36 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 06:51:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 06:51:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 22 Oct 2020 07:01:44 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 01 Dec 2020 02:43:04 GMT
ENV PHP_VERSION=7.4.13
# Tue, 01 Dec 2020 02:43:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Tue, 01 Dec 2020 02:43:24 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Tue, 01 Dec 2020 02:43:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 01 Dec 2020 02:43:39 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 01 Dec 2020 02:46:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 01 Dec 2020 02:46:34 GMT
COPY multi:ebc915bbde1078ce3122b918e2e4c7726858af785343ade1a8d1a94f1052a4c7 in /usr/local/bin/ 
# Tue, 01 Dec 2020 02:46:37 GMT
RUN docker-php-ext-enable sodium
# Tue, 01 Dec 2020 02:46:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 01 Dec 2020 02:46:39 GMT
WORKDIR /var/www/html
# Tue, 01 Dec 2020 02:46:42 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Tue, 01 Dec 2020 02:46:44 GMT
STOPSIGNAL SIGQUIT
# Tue, 01 Dec 2020 02:46:45 GMT
EXPOSE 9000
# Tue, 01 Dec 2020 02:46:46 GMT
CMD ["php-fpm"]
# Tue, 01 Dec 2020 04:29:50 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Tue, 01 Dec 2020 04:29:56 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 01 Dec 2020 04:30:45 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Tue, 01 Dec 2020 04:30:48 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Tue, 08 Dec 2020 00:01:12 GMT
ENV ADMINER_VERSION=4.7.8
# Tue, 08 Dec 2020 00:01:13 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Tue, 08 Dec 2020 00:01:14 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Tue, 08 Dec 2020 00:01:18 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Tue, 08 Dec 2020 00:01:20 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 08 Dec 2020 00:01:24 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Tue, 08 Dec 2020 00:01:25 GMT
USER adminer
# Tue, 08 Dec 2020 00:01:26 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:5f2023fd85a4e68f37fe41421fd89f30e69b98a645613521c57c01317561eee3`  
		Last Modified: Thu, 22 Oct 2020 01:58:45 GMT  
		Size: 2.4 MB (2405675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60b50c98f8a8e2c6a27378dfa0f44df1844ac67c6981303675f138a42679f25`  
		Last Modified: Thu, 22 Oct 2020 07:35:57 GMT  
		Size: 1.2 MB (1214265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b472094d673b7c272085505c976192b9aaafa3157c99bade9755fbca18a24071`  
		Last Modified: Thu, 22 Oct 2020 07:35:56 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc39e5d916c11e7eb158e72d14ab981eb45ccc7b6451c1d6d3cb627b71cdbb6`  
		Last Modified: Thu, 22 Oct 2020 07:35:55 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad5979536683af238cd5c6e9e7ee5171a2f468ba42667525bcf73dfbd4442d5c`  
		Last Modified: Tue, 01 Dec 2020 04:01:12 GMT  
		Size: 10.3 MB (10338579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83bfa48b04ad972c7ddc62f60703fd345236339c894ee5e02487d0a6912eec44`  
		Last Modified: Tue, 01 Dec 2020 04:01:08 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d500723729ab98b41c43300141cf87ecedf3122e848cb7f2871a8a18b472c9`  
		Last Modified: Tue, 01 Dec 2020 04:01:12 GMT  
		Size: 12.8 MB (12773054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ffe3faddffbb23fc7ec2b0ac5897aa6700b295f1129a52a58322108a7d7146`  
		Last Modified: Tue, 01 Dec 2020 04:01:08 GMT  
		Size: 2.3 KB (2260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c6599d32683be6cd2106e34a046a0a556bffd2baac97299eb69df7408f682be`  
		Last Modified: Tue, 01 Dec 2020 04:01:08 GMT  
		Size: 16.9 KB (16903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7158f5b17b11ddb8f243be54e5fc6112f6017d46780577a568a72e2e7d3f2cb1`  
		Last Modified: Tue, 01 Dec 2020 04:01:08 GMT  
		Size: 8.4 KB (8446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba8645bc546fe074d817500743f03a6b6b287793cee19306e5267095e410e7e`  
		Last Modified: Tue, 01 Dec 2020 04:32:00 GMT  
		Size: 310.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae84262bbd09928c80ab09696b0c7d2d57c5b58e28e089d2be9aae62bd0c7d0e`  
		Last Modified: Tue, 01 Dec 2020 04:31:59 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d45b8aa81cac48a3b6f2953fa3ad9d6047d134f7b76cbb3e05cbde0d6e0c7fc1`  
		Last Modified: Tue, 01 Dec 2020 04:31:59 GMT  
		Size: 3.9 MB (3926120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b483e9859bacb3a5557c81eda83e17a2559203c0979dcdd57bdcbe5729404c0f`  
		Last Modified: Tue, 01 Dec 2020 04:31:58 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7022a91847b0aaf7d1e067b9c3fa7620f93f349b64d2d7ebe0e816598a47fed2`  
		Last Modified: Tue, 08 Dec 2020 00:01:58 GMT  
		Size: 570.9 KB (570923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562e2ad43a7b07e5427acd85e75ec18c9dc4b21fe0a10fac08b447cfa140187f`  
		Last Modified: Tue, 08 Dec 2020 00:01:58 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7.8-fastcgi` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:89498585a4df7bcfaecdaadf8bee7b0b21018e861c1357c5826273c129cea8c1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.8 MB (33782483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57bc4d4eb9fffe27cb455d6f0c04677fd0798704e2673ac9c281b492fa593f03`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 07:18:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 22 Oct 2020 07:18:56 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 22 Oct 2020 07:18:59 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 22 Oct 2020 07:19:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 22 Oct 2020 07:19:04 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 22 Oct 2020 07:23:16 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Thu, 22 Oct 2020 07:23:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 07:23:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 07:23:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 22 Oct 2020 07:32:38 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 01 Dec 2020 03:31:07 GMT
ENV PHP_VERSION=7.4.13
# Tue, 01 Dec 2020 03:31:08 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Tue, 01 Dec 2020 03:31:09 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Tue, 01 Dec 2020 03:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 01 Dec 2020 03:31:15 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 01 Dec 2020 03:34:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 01 Dec 2020 03:35:01 GMT
COPY multi:ebc915bbde1078ce3122b918e2e4c7726858af785343ade1a8d1a94f1052a4c7 in /usr/local/bin/ 
# Tue, 01 Dec 2020 03:35:06 GMT
RUN docker-php-ext-enable sodium
# Tue, 01 Dec 2020 03:35:06 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 01 Dec 2020 03:35:08 GMT
WORKDIR /var/www/html
# Tue, 01 Dec 2020 03:35:10 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Tue, 01 Dec 2020 03:35:11 GMT
STOPSIGNAL SIGQUIT
# Tue, 01 Dec 2020 03:35:12 GMT
EXPOSE 9000
# Tue, 01 Dec 2020 03:35:13 GMT
CMD ["php-fpm"]
# Tue, 01 Dec 2020 08:13:43 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Tue, 01 Dec 2020 08:13:46 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 01 Dec 2020 08:14:29 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Tue, 01 Dec 2020 08:14:30 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Mon, 07 Dec 2020 23:40:07 GMT
ENV ADMINER_VERSION=4.7.8
# Mon, 07 Dec 2020 23:40:07 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Mon, 07 Dec 2020 23:40:08 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Mon, 07 Dec 2020 23:40:11 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Mon, 07 Dec 2020 23:40:12 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Mon, 07 Dec 2020 23:40:13 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Mon, 07 Dec 2020 23:40:14 GMT
USER adminer
# Mon, 07 Dec 2020 23:40:15 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d57dba23203172f8fffd1379aef0307e782178b62dfc684d43c546f7e874ed`  
		Last Modified: Thu, 22 Oct 2020 08:06:21 GMT  
		Size: 1.3 MB (1342784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8414edb0c9c2f7472bb6228bf691a2ddac19ddad7bad789c7cbdc147aded711`  
		Last Modified: Thu, 22 Oct 2020 08:06:20 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d26eeef0db35b2328adae38a8490c7403844452c3606dd17fbe68216f98e82`  
		Last Modified: Thu, 22 Oct 2020 08:06:19 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b747a72bda51ef2a52afed0eef10b56786e7c76ab30913f0e650a83b66935e4f`  
		Last Modified: Tue, 01 Dec 2020 04:54:24 GMT  
		Size: 10.3 MB (10338600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c684293922e5efaae5d67a6b158f6e54284e91081dda97b306a74ce97c9d0738`  
		Last Modified: Tue, 01 Dec 2020 04:54:21 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acdf0cad2cf9d86164e334858db58328dc251f08abe9d0841cc1bf520748163e`  
		Last Modified: Tue, 01 Dec 2020 04:54:25 GMT  
		Size: 14.5 MB (14458713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3417ec8fcb1bd4b4d3f295b89316912d8e33667e645450c3d0a2694887fea5da`  
		Last Modified: Tue, 01 Dec 2020 04:54:21 GMT  
		Size: 2.3 KB (2256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96e2c572c8bf97a5e221afc68cec20acaad7e29b919f242c6cb085234693b08`  
		Last Modified: Tue, 01 Dec 2020 04:54:22 GMT  
		Size: 17.0 KB (16978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:732bd773818e9fef29ad5ba55c5ddd1638077be22b0fd0a8f3a8bee4b600da11`  
		Last Modified: Tue, 01 Dec 2020 04:54:21 GMT  
		Size: 8.4 KB (8444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1886aa9fc4a1ad175dc4689b2f38537f04a005774f1c34b08ae3b8c3158fe5f8`  
		Last Modified: Tue, 01 Dec 2020 08:15:16 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf4e7f82086c970c52f8f544137e3286e990df9f19ad8567bba476226b12f61`  
		Last Modified: Tue, 01 Dec 2020 08:15:15 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4acc32056dfd0cd70bbc78cdfb34f2c627a433caff773366ad168a4945db066`  
		Last Modified: Tue, 01 Dec 2020 08:15:15 GMT  
		Size: 4.3 MB (4331531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb34a16b4bdb5625d39f3ef20da17bfecf2156cf9f3a647b4c4c26497af56b7`  
		Last Modified: Tue, 01 Dec 2020 08:15:15 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857d9231bfb81ba8cc071fbdcccdb6f9189f8e56d09ce9396b85b4e88b412b53`  
		Last Modified: Mon, 07 Dec 2020 23:40:43 GMT  
		Size: 570.9 KB (570920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a854be7b56f0667067e2d5d43ed47f9f068cb0e3f7976910fb604dda911121db`  
		Last Modified: Mon, 07 Dec 2020 23:40:43 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7.8-fastcgi` - linux; 386

```console
$ docker pull adminer@sha256:4f5fe39f0929ce4ac634729677768b268b328437e602e5a286881bb683086a5f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34705084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c8aa440257abba5e8b17a4be7767c0c3b8fc17f455e445f561495f8d394f849`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 22 Oct 2020 02:00:33 GMT
ADD file:46ad43b4984bcf49c5a888ff3628f23161f55cd1fb062f469e707100c97fa254 in / 
# Thu, 22 Oct 2020 02:00:33 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:36:23 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 22 Oct 2020 03:36:26 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 22 Oct 2020 03:36:27 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 22 Oct 2020 03:36:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 22 Oct 2020 03:36:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 22 Oct 2020 03:45:17 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Thu, 22 Oct 2020 03:45:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 03:45:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 03:45:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 22 Oct 2020 04:01:27 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 01 Dec 2020 04:11:03 GMT
ENV PHP_VERSION=7.4.13
# Tue, 01 Dec 2020 04:11:04 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Tue, 01 Dec 2020 04:11:04 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Tue, 01 Dec 2020 04:11:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 01 Dec 2020 04:11:13 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 01 Dec 2020 04:19:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 01 Dec 2020 04:19:54 GMT
COPY multi:ebc915bbde1078ce3122b918e2e4c7726858af785343ade1a8d1a94f1052a4c7 in /usr/local/bin/ 
# Tue, 01 Dec 2020 04:19:56 GMT
RUN docker-php-ext-enable sodium
# Tue, 01 Dec 2020 04:19:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 01 Dec 2020 04:19:56 GMT
WORKDIR /var/www/html
# Tue, 01 Dec 2020 04:19:57 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Tue, 01 Dec 2020 04:19:57 GMT
STOPSIGNAL SIGQUIT
# Tue, 01 Dec 2020 04:19:58 GMT
EXPOSE 9000
# Tue, 01 Dec 2020 04:19:58 GMT
CMD ["php-fpm"]
# Tue, 01 Dec 2020 09:25:25 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Tue, 01 Dec 2020 09:25:26 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 01 Dec 2020 09:25:53 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Tue, 01 Dec 2020 09:25:54 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Mon, 07 Dec 2020 23:38:31 GMT
ENV ADMINER_VERSION=4.7.8
# Mon, 07 Dec 2020 23:38:32 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Mon, 07 Dec 2020 23:38:32 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Mon, 07 Dec 2020 23:38:33 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Mon, 07 Dec 2020 23:38:33 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Mon, 07 Dec 2020 23:38:33 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Mon, 07 Dec 2020 23:38:34 GMT
USER adminer
# Mon, 07 Dec 2020 23:38:34 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:d6ca64ac6f4b6382142ce9a3501652938130a6ec4bb02f3f455ee1f980834cfe`  
		Last Modified: Thu, 22 Oct 2020 02:00:57 GMT  
		Size: 2.8 MB (2791407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30be8ffd290910905a5fb7cbb70252eb0f59edb09db20bdc21f3b65456acc28f`  
		Last Modified: Thu, 22 Oct 2020 05:10:23 GMT  
		Size: 1.4 MB (1439641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d58e2433b13446c863e85b34f8e4c93ca9d5b3b93d2bac415fd9cdf77bcec4`  
		Last Modified: Thu, 22 Oct 2020 05:10:21 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5729dcb8d303f82a7f8cf3df49048e34ce8ee89f79155fb08a475da46b64308`  
		Last Modified: Thu, 22 Oct 2020 05:10:21 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73c975f14cba63719b1acf30eb48c56e9ff5ab3ba3c93cc300551ed40f30ac4`  
		Last Modified: Tue, 01 Dec 2020 07:15:32 GMT  
		Size: 10.3 MB (10338565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8926789263a06364cefc6d6aee50b84a30291d014d2029ca669cb556f4c2bb1`  
		Last Modified: Tue, 01 Dec 2020 07:15:30 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcbe8e9cc07ddaae06ed92974d6d0a5249cac41ebb54331b56fc5c9e240eb993`  
		Last Modified: Tue, 01 Dec 2020 07:15:35 GMT  
		Size: 15.0 MB (15012323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e40c7a669cd74ab9dc3e2874416646f823f63c10d9b9a952a55dc1ad5bac9d`  
		Last Modified: Tue, 01 Dec 2020 07:15:30 GMT  
		Size: 2.3 KB (2260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed001fb8127577a70da6914dcf10ccb5d90ed9cf2a1cd3272618748f6b111d03`  
		Last Modified: Tue, 01 Dec 2020 07:15:29 GMT  
		Size: 16.9 KB (16920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90867a60ecf180a61e2ada4f0842adc2c2e44685c28753a5bed45de997db01e7`  
		Last Modified: Tue, 01 Dec 2020 07:15:29 GMT  
		Size: 8.4 KB (8442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3ce5df361365526e71aaf6df13804b7dedc099dd67740782cc739e0613eb110`  
		Last Modified: Tue, 01 Dec 2020 09:26:27 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a789bbdaebdf4bde2f5038d3a2a626522e4b2edc239b954288d23175ee69042`  
		Last Modified: Tue, 01 Dec 2020 09:26:26 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a79d0d02c93a44d0f6d1145f6ae0a0333e71fe94bfa8c63bd24354761d9587`  
		Last Modified: Tue, 01 Dec 2020 09:26:27 GMT  
		Size: 4.5 MB (4519093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85c74143366ffd582b27ed81dd1f35e4e314799a0de720b613b98b88ce787c77`  
		Last Modified: Tue, 01 Dec 2020 09:26:25 GMT  
		Size: 1.5 KB (1472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3529b652f01c65456c39d33fd9d239949548a0442b8a1fa9d2bf0a1c1f74b968`  
		Last Modified: Mon, 07 Dec 2020 23:38:54 GMT  
		Size: 570.9 KB (570861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a79e9613d8243f31a29bb14c13abf1a73d577720e86547b01bdef2bf8f9296bd`  
		Last Modified: Mon, 07 Dec 2020 23:38:54 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7.8-fastcgi` - linux; ppc64le

```console
$ docker pull adminer@sha256:0671ac686df177a55af6924323ebcc05a17cb4bf61a6372df21a1a0c22487346
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.1 MB (35117996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:959c6c5b577d14c45504ecdd9a75e110b1afb1e5e8651a224075e4784c97c07c`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 22 Oct 2020 11:00:06 GMT
ADD file:176e047fab2c1828575bffa6b14773efa297b7ecf312d86103c5dd4f78ec8027 in / 
# Thu, 22 Oct 2020 11:00:17 GMT
CMD ["/bin/sh"]
# Fri, 23 Oct 2020 00:21:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 23 Oct 2020 00:21:18 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 23 Oct 2020 00:21:30 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 23 Oct 2020 00:21:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 23 Oct 2020 00:21:44 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 23 Oct 2020 00:27:50 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Fri, 23 Oct 2020 00:27:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 23 Oct 2020 00:28:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 23 Oct 2020 00:28:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 23 Oct 2020 00:39:53 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 01 Dec 2020 03:57:52 GMT
ENV PHP_VERSION=7.4.13
# Tue, 01 Dec 2020 03:57:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Tue, 01 Dec 2020 03:58:02 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Tue, 01 Dec 2020 03:58:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 01 Dec 2020 03:58:37 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 01 Dec 2020 04:02:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 01 Dec 2020 04:02:41 GMT
COPY multi:ebc915bbde1078ce3122b918e2e4c7726858af785343ade1a8d1a94f1052a4c7 in /usr/local/bin/ 
# Tue, 01 Dec 2020 04:02:55 GMT
RUN docker-php-ext-enable sodium
# Tue, 01 Dec 2020 04:02:59 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 01 Dec 2020 04:03:05 GMT
WORKDIR /var/www/html
# Tue, 01 Dec 2020 04:03:27 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Tue, 01 Dec 2020 04:03:33 GMT
STOPSIGNAL SIGQUIT
# Tue, 01 Dec 2020 04:03:40 GMT
EXPOSE 9000
# Tue, 01 Dec 2020 04:03:44 GMT
CMD ["php-fpm"]
# Tue, 01 Dec 2020 07:11:43 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Tue, 01 Dec 2020 07:11:59 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 01 Dec 2020 07:12:55 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Tue, 01 Dec 2020 07:12:59 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Tue, 08 Dec 2020 00:17:37 GMT
ENV ADMINER_VERSION=4.7.8
# Tue, 08 Dec 2020 00:17:44 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Tue, 08 Dec 2020 00:17:47 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Tue, 08 Dec 2020 00:17:56 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Tue, 08 Dec 2020 00:17:59 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 08 Dec 2020 00:18:03 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Tue, 08 Dec 2020 00:18:08 GMT
USER adminer
# Tue, 08 Dec 2020 00:18:15 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:692a9d763e196c85d79fc3e45b316b1bb557c93ba88a3c8ebf679a585d1efe73`  
		Last Modified: Thu, 22 Oct 2020 11:02:06 GMT  
		Size: 2.8 MB (2803218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0285d6f06f3beb1c140c055210664c441b93dd4f2037177a5396bce94ca16ce5`  
		Last Modified: Fri, 23 Oct 2020 01:34:08 GMT  
		Size: 1.4 MB (1383187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a6459a3bf272daa53ff4ba97cc849676f497de9f78d8e9378ec02552293f175`  
		Last Modified: Fri, 23 Oct 2020 01:34:07 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16cff6064dc29d3f629d353736c1cac074caa5b50738422adb84de99a019bb32`  
		Last Modified: Fri, 23 Oct 2020 01:34:08 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67dcc2a717f8153769df04bd895be154aca7c3fc20560f37da5b36e0fbd9efbd`  
		Last Modified: Tue, 01 Dec 2020 05:51:15 GMT  
		Size: 10.3 MB (10338603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9502fa9f26f9855ddcfd4309edb7c16ce7517f1c88a60155b169e6182acbdd17`  
		Last Modified: Tue, 01 Dec 2020 05:51:09 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf065529921adbb64e6889d9cfa225de7f8aa65204f3ec400330d4fc989de4d8`  
		Last Modified: Tue, 01 Dec 2020 05:51:13 GMT  
		Size: 15.6 MB (15628567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e91de5593ec1aa89d021215583d63f94d4f36d9608f29dd460ede4c7290ebb7`  
		Last Modified: Tue, 01 Dec 2020 05:51:09 GMT  
		Size: 2.3 KB (2255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede5b0209a637a8111ae77c919a561733c6e703c97333ecea99a4abbecf8a2c5`  
		Last Modified: Tue, 01 Dec 2020 05:51:09 GMT  
		Size: 17.0 KB (16968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e851350ac3fff1de99c14298cb35f46c409629186a85f22c22a0be19f4f7cd`  
		Last Modified: Tue, 01 Dec 2020 05:51:09 GMT  
		Size: 8.4 KB (8441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df2bf3b8e2936ee1044358dfd1700fce3f08592b60bac9086d1d4677f3de8ca9`  
		Last Modified: Tue, 01 Dec 2020 07:15:16 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bcb7b3aa24f4c386111b1860808ec662939186fbbf6ea9be1a4309880e34a17`  
		Last Modified: Tue, 01 Dec 2020 07:15:13 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:088e76bc30b441c5832343aa548abe6c770bd754156485a0b235f1cf92cac64e`  
		Last Modified: Tue, 01 Dec 2020 07:15:14 GMT  
		Size: 4.4 MB (4360124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:587c025ae0482b8d3b5e8fc26b4af5eae6dc22c5c3da95ca52fbfc9c9a5b2f3a`  
		Last Modified: Tue, 01 Dec 2020 07:15:12 GMT  
		Size: 1.5 KB (1479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45314773dc31f89543794af67d864efadc99ec57ce116a3760d41a4c207f6f30`  
		Last Modified: Tue, 08 Dec 2020 00:19:11 GMT  
		Size: 570.9 KB (570925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4283c4537d91df6ad82cb299758a89bc3a5d2a8f42ddfe40ea81b189e8d6fb0`  
		Last Modified: Tue, 08 Dec 2020 00:19:11 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7.8-fastcgi` - linux; s390x

```console
$ docker pull adminer@sha256:1f93751408862e70ce3d4b81bd3d7bdb4e2ecac81606992543e7bbfdbf90f96b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32598207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9061e3e2134cb0ffa169546bbf7624fe55bbea5f40e1b70016744979434fcc7d`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 11 Dec 2020 02:09:52 GMT
ADD file:c9395a36a4e03768aabd282eb1f31705cc00181d3147222d9c940eaa5a8fd511 in / 
# Fri, 11 Dec 2020 02:09:53 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 11:30:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 11 Dec 2020 11:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 11 Dec 2020 11:30:56 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 11 Dec 2020 11:30:57 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 11 Dec 2020 11:30:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 11 Dec 2020 11:36:17 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Fri, 11 Dec 2020 11:36:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Dec 2020 11:36:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Dec 2020 11:36:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 11 Dec 2020 12:09:03 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 11 Dec 2020 12:09:04 GMT
ENV PHP_VERSION=7.4.13
# Fri, 11 Dec 2020 12:09:04 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Fri, 11 Dec 2020 12:09:05 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Fri, 11 Dec 2020 12:09:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 11 Dec 2020 12:09:12 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Dec 2020 12:13:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Dec 2020 12:13:55 GMT
COPY multi:ebc915bbde1078ce3122b918e2e4c7726858af785343ade1a8d1a94f1052a4c7 in /usr/local/bin/ 
# Fri, 11 Dec 2020 12:13:57 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Dec 2020 12:13:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Dec 2020 12:13:59 GMT
WORKDIR /var/www/html
# Fri, 11 Dec 2020 12:14:00 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 11 Dec 2020 12:14:01 GMT
STOPSIGNAL SIGQUIT
# Fri, 11 Dec 2020 12:14:01 GMT
EXPOSE 9000
# Fri, 11 Dec 2020 12:14:02 GMT
CMD ["php-fpm"]
# Fri, 11 Dec 2020 18:45:19 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 11 Dec 2020 18:45:21 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 11 Dec 2020 18:46:30 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 11 Dec 2020 18:46:31 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 11 Dec 2020 18:46:32 GMT
ENV ADMINER_VERSION=4.7.8
# Fri, 11 Dec 2020 18:46:32 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Fri, 11 Dec 2020 18:46:33 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Fri, 11 Dec 2020 18:46:36 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 11 Dec 2020 18:46:37 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 11 Dec 2020 18:46:38 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 11 Dec 2020 18:46:38 GMT
USER adminer
# Fri, 11 Dec 2020 18:46:39 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:7c2470fe3d16cb70fca0826168095a96838b1322a8cd1502b28284ee8561b491`  
		Last Modified: Fri, 11 Dec 2020 02:10:27 GMT  
		Size: 2.6 MB (2565988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a23c8359d30ae261ad953f292e6681a71ebc7388607b74d901bbc07f71e1311`  
		Last Modified: Fri, 11 Dec 2020 13:48:01 GMT  
		Size: 1.4 MB (1382587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01422c3e898d3241d4134256bf0d911b0752823227af04614187c79c187e2843`  
		Last Modified: Fri, 11 Dec 2020 13:48:03 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a0be2077abd44f96e50bdebb1ed93a6e2b8d504761c23fa0e5e9b87045ca38`  
		Last Modified: Fri, 11 Dec 2020 13:48:01 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:797fc05bf988e85a5cf643f2d07a0b08a36e3f1529c75c41a2460041b6ee0f43`  
		Last Modified: Fri, 11 Dec 2020 13:50:52 GMT  
		Size: 10.3 MB (10338591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e11bb5dc7804a50c805852fbe653bb133478f5005e8c78c1d712af0d5bd6db4`  
		Last Modified: Fri, 11 Dec 2020 13:50:49 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:311bfe9de08521ea35d7a1520e00de8215315e5a8144a4335f1313ad7f6593de`  
		Last Modified: Fri, 11 Dec 2020 13:50:51 GMT  
		Size: 13.6 MB (13553700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59a788dffbadef519f959d8de10a3156add64ed4e15c8e96045a3bebf9ef316`  
		Last Modified: Fri, 11 Dec 2020 13:50:49 GMT  
		Size: 2.3 KB (2260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:898ee507348c01a8028e7ad08c8af3edde13cd884ffdfd990ad679df9b004552`  
		Last Modified: Fri, 11 Dec 2020 13:50:49 GMT  
		Size: 16.9 KB (16883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a7bec784d5537500a8f385256905e367037e6e1ae365f119cf3a305c384338f`  
		Last Modified: Fri, 11 Dec 2020 13:50:50 GMT  
		Size: 8.4 KB (8445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aacad6fcb4ce89b6aebc70fa08e0aeaf4004bdfd4288064a050ae7a6b6a1ca5`  
		Last Modified: Fri, 11 Dec 2020 18:47:37 GMT  
		Size: 310.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed17bffefe5fed1ad7e5ba183155f268ef4c6f19e11ce2b4d2b51a756f56e38`  
		Last Modified: Fri, 11 Dec 2020 18:47:32 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:195c8eb0f725b2189839adb7a0fec2e91f3b597dcf7a9a35cdb3cde9beea8e03`  
		Last Modified: Fri, 11 Dec 2020 18:47:33 GMT  
		Size: 4.2 MB (4153144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dd4956eb56581838eebbd42956889e3cc9dd1e7526a1282b8075c4c7daf28d1`  
		Last Modified: Fri, 11 Dec 2020 18:47:33 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a7b5a1b8dcaeb2cdc7acda96210109729ec955718cf8d30f683176a9ecf87be`  
		Last Modified: Fri, 11 Dec 2020 18:47:32 GMT  
		Size: 570.9 KB (570919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a3464ffffa7b21ee6c5a53d2f9143c982205d77f77a55bf9ec4ebb2cdff801`  
		Last Modified: Fri, 11 Dec 2020 18:47:33 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:4.7.8-standalone`

```console
$ docker pull adminer@sha256:4600f2453f7c9f3ee8179016a65d0b49a8dfb89467ac0947a6245e62e7f81fb1
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

### `adminer:4.7.8-standalone` - linux; amd64

```console
$ docker pull adminer@sha256:4b087576de7b4ca7c60bb3558f0b5ee30f496cee10fa19ea0a9f0e071c72b1f5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (33965375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2db7241b0f1461d8707525832e608fe513453f99c11beed9413194f7519e05`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 06:30:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 22 Oct 2020 06:30:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 22 Oct 2020 06:30:15 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 22 Oct 2020 06:30:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 22 Oct 2020 06:30:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 22 Oct 2020 06:30:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 06:30:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 06:30:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 22 Oct 2020 06:43:41 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 01 Dec 2020 04:36:20 GMT
ENV PHP_VERSION=7.4.13
# Tue, 01 Dec 2020 04:36:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Tue, 01 Dec 2020 04:36:21 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Tue, 01 Dec 2020 04:36:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 01 Dec 2020 04:36:27 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 01 Dec 2020 04:44:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 01 Dec 2020 04:44:54 GMT
COPY multi:afab483600631d4d87fe030871bbb016f1c2b73c0b72609d857bace419af7f5d in /usr/local/bin/ 
# Tue, 01 Dec 2020 04:44:57 GMT
RUN docker-php-ext-enable sodium
# Tue, 01 Dec 2020 04:44:57 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 01 Dec 2020 04:44:57 GMT
CMD ["php" "-a"]
# Tue, 01 Dec 2020 07:46:46 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Tue, 01 Dec 2020 07:46:46 GMT
STOPSIGNAL SIGINT
# Tue, 01 Dec 2020 07:46:47 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 01 Dec 2020 07:46:48 GMT
WORKDIR /var/www/html
# Tue, 01 Dec 2020 07:47:15 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Tue, 01 Dec 2020 07:47:15 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Tue, 08 Dec 2020 00:19:24 GMT
ENV ADMINER_VERSION=4.7.8
# Tue, 08 Dec 2020 00:19:24 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Tue, 08 Dec 2020 00:19:24 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Tue, 08 Dec 2020 00:19:26 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Tue, 08 Dec 2020 00:19:26 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 08 Dec 2020 00:19:26 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Tue, 08 Dec 2020 00:19:26 GMT
USER adminer
# Tue, 08 Dec 2020 00:19:27 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 08 Dec 2020 00:19:27 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f8bf6cfdbe614fef94f982905079c16e27b3de2d24eb1ff513d3d83e656ca2`  
		Last Modified: Thu, 22 Oct 2020 07:36:55 GMT  
		Size: 1.3 MB (1340771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce5be79740125b9e74a77885bf6ee2b0d25ac7ed9e9432c5aa7210bb3b00458a`  
		Last Modified: Thu, 22 Oct 2020 07:36:55 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99dd6507fe563b66ba35badf706e1bbb2d39eb5d0a3c0d5a86a45d2af7e89c1`  
		Last Modified: Thu, 22 Oct 2020 07:36:55 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c513a1b503cf7c9f18fa014dada9744070ded92dc9ad548cd056c4f56dc1a9`  
		Last Modified: Tue, 01 Dec 2020 07:27:10 GMT  
		Size: 10.3 MB (10338569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff080eafb4c0518981fca6aef4d239863fc59195f41ce7c440b2c6c518f2ac79`  
		Last Modified: Tue, 01 Dec 2020 07:27:09 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e818119992b11dbf09b710066a78920985b9ea1310fc8272df816e0884985f44`  
		Last Modified: Tue, 01 Dec 2020 07:27:13 GMT  
		Size: 14.6 MB (14572037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba3c14a67f95ae52ebfb558ab6b5d87687a05ce41c8df0a618ff42b73204e40`  
		Last Modified: Tue, 01 Dec 2020 07:27:09 GMT  
		Size: 2.3 KB (2257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbb0285b7ad2b170e4ed2cffbe0f16ba55d689c056ff43767834783eab7b8261`  
		Last Modified: Tue, 01 Dec 2020 07:27:09 GMT  
		Size: 17.0 KB (16987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae324cfad8acf03b3a98a15e963b7046404a7da3a6bbf68fd65d37f899f194d`  
		Last Modified: Tue, 01 Dec 2020 07:48:25 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb51158f683d66315de6fa572f7ea13d8ffb71ac85faa20c8578edb11678f37d`  
		Last Modified: Tue, 01 Dec 2020 07:48:23 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71ac21b64d1d63d967acb13664404babd0ef86fc896c484ce28cccf70001d0f1`  
		Last Modified: Tue, 01 Dec 2020 07:48:24 GMT  
		Size: 4.3 MB (4321455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2170e09d39d861e9bb7a5da5def906b44153b6c481fe17925ba82d1f1f78eec`  
		Last Modified: Tue, 01 Dec 2020 07:48:24 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d95b48dfa11f7f5c061f6522f6ff5d574452b8f321c6075455da2643b1967a`  
		Last Modified: Tue, 08 Dec 2020 00:19:45 GMT  
		Size: 570.9 KB (570860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3bb2b5e72bf0dbd4b855ddf65aaf9c0d077703804bdbdc9ea3ea98cbbfceaf6`  
		Last Modified: Tue, 08 Dec 2020 00:19:44 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7.8-standalone` - linux; arm variant v6

```console
$ docker pull adminer@sha256:7e114494e5e3a8ece382083d27c33f6c993695f0ff6c92c235ced149177f5da9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32073857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9cfa5ccbab063435267257cf4c761402c956233cf22775ed1c774b53a045715`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 11 Dec 2020 02:17:15 GMT
ADD file:1a9c0a67560d338c0c0e7005d8915d998fc9cf3e9f53bfd7e42e8391f0a39bce in / 
# Fri, 11 Dec 2020 02:17:15 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 07:04:50 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 11 Dec 2020 07:04:53 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 11 Dec 2020 07:04:55 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 11 Dec 2020 07:04:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 11 Dec 2020 07:04:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 11 Dec 2020 07:05:00 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Dec 2020 07:05:01 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Dec 2020 07:05:02 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 11 Dec 2020 07:13:50 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 11 Dec 2020 07:13:54 GMT
ENV PHP_VERSION=7.4.13
# Fri, 11 Dec 2020 07:13:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Fri, 11 Dec 2020 07:13:56 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Fri, 11 Dec 2020 07:14:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 11 Dec 2020 07:14:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Dec 2020 07:17:37 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Dec 2020 07:17:39 GMT
COPY multi:afab483600631d4d87fe030871bbb016f1c2b73c0b72609d857bace419af7f5d in /usr/local/bin/ 
# Fri, 11 Dec 2020 07:17:42 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Dec 2020 07:17:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Dec 2020 07:17:43 GMT
CMD ["php" "-a"]
# Fri, 11 Dec 2020 09:04:18 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 11 Dec 2020 09:04:19 GMT
STOPSIGNAL SIGINT
# Fri, 11 Dec 2020 09:04:21 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 11 Dec 2020 09:04:22 GMT
WORKDIR /var/www/html
# Fri, 11 Dec 2020 09:05:06 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 11 Dec 2020 09:05:08 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 11 Dec 2020 09:05:08 GMT
ENV ADMINER_VERSION=4.7.8
# Fri, 11 Dec 2020 09:05:09 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Fri, 11 Dec 2020 09:05:11 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Fri, 11 Dec 2020 09:05:14 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 11 Dec 2020 09:05:15 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 11 Dec 2020 09:05:16 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 11 Dec 2020 09:05:17 GMT
USER adminer
# Fri, 11 Dec 2020 09:05:18 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 11 Dec 2020 09:05:19 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:f1c16df8fee33d421d08790b17ca2af67a3fe49e77b6b991dd0c30631f5d1baf`  
		Last Modified: Fri, 11 Dec 2020 02:17:57 GMT  
		Size: 2.6 MB (2601992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623cc08cbe035cf15859e57a83e2243620418da06e1905d1875a46bec901e540`  
		Last Modified: Fri, 11 Dec 2020 07:56:49 GMT  
		Size: 1.3 MB (1310156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3a7aacff9b7ccf646f2bdbbc8d40bbb304550e813876049e721abd35461df9`  
		Last Modified: Fri, 11 Dec 2020 07:56:49 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d3214ea6f418597f370177309be7728f94481030c9cba6e45c4b74cfd04cc0`  
		Last Modified: Fri, 11 Dec 2020 07:56:49 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64de18534c9c3dd7212eceb5a285d571df578238ca4684a2e922b131e9947d79`  
		Last Modified: Fri, 11 Dec 2020 07:57:40 GMT  
		Size: 10.3 MB (10338603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d60b5c1c75b96676e4154f74a500fdd4a2645d4c51e189b0bdd18e06f26c3143`  
		Last Modified: Fri, 11 Dec 2020 07:57:39 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee32c3be90bc13cb4b3406c492ec35d5c211ac42b25e536939fb3220aea672b`  
		Last Modified: Fri, 11 Dec 2020 07:57:44 GMT  
		Size: 13.2 MB (13201116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e71cdda7d8acfe2fe1a6263c1b004b3ae972d7ce1c0ac95fec09aa0c0ba1f7fd`  
		Last Modified: Fri, 11 Dec 2020 07:57:39 GMT  
		Size: 2.3 KB (2258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec74a6ee1beba601eed5abe261394c8ddfa2d53093a1f6768356ec5891066746`  
		Last Modified: Fri, 11 Dec 2020 07:57:40 GMT  
		Size: 16.9 KB (16889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b84bf5ad218839b4e8156c322c5611b3c26167141a7c1e8049055deeda8b1ed5`  
		Last Modified: Fri, 11 Dec 2020 09:07:23 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0113ef6e65685219488d6543639cff152292617519f4649a6d7c8e4bbf03322b`  
		Last Modified: Fri, 11 Dec 2020 09:07:21 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2501c821a30d874046f30dd9d3947aa9f82cca3e9d39eb18214a765744e0b24`  
		Last Modified: Fri, 11 Dec 2020 09:07:21 GMT  
		Size: 4.0 MB (4026242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:945b172c5cf67a28a59e5b25cfed08871f360f551a912c8d7f64c096d6554812`  
		Last Modified: Fri, 11 Dec 2020 09:07:20 GMT  
		Size: 1.5 KB (1473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df40a3aa85441cb471ce645d5a0a2564fb9e2f042e078b8f04dd343488863a4`  
		Last Modified: Fri, 11 Dec 2020 09:07:20 GMT  
		Size: 570.9 KB (570917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90644dda17e22024741efd92b2987150a52659ae6bb25b7ea232e9b72d3b1d83`  
		Last Modified: Fri, 11 Dec 2020 09:07:20 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7.8-standalone` - linux; arm variant v7

```console
$ docker pull adminer@sha256:39b988e9485b8f06142e8584a4764c3c32159d51377eab0739b1cf794f701d1a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31186995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d4ed3310dfe2d29dd9a809a5ea826952ac518c5d93ab5e12054d9b7560791f7`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 22 Oct 2020 01:58:13 GMT
ADD file:46f89172426e9f5b1d669a2ca7ab218fc2deaef1caeeab88f2b5bd443ac9773d in / 
# Thu, 22 Oct 2020 01:58:14 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 06:47:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 22 Oct 2020 06:47:37 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 22 Oct 2020 06:47:45 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 22 Oct 2020 06:47:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 22 Oct 2020 06:47:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 22 Oct 2020 06:47:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 06:47:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 06:48:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 22 Oct 2020 06:56:26 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 01 Dec 2020 02:39:45 GMT
ENV PHP_VERSION=7.4.13
# Tue, 01 Dec 2020 02:39:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Tue, 01 Dec 2020 02:39:46 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Tue, 01 Dec 2020 02:39:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 01 Dec 2020 02:39:53 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 01 Dec 2020 02:42:30 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 01 Dec 2020 02:42:32 GMT
COPY multi:afab483600631d4d87fe030871bbb016f1c2b73c0b72609d857bace419af7f5d in /usr/local/bin/ 
# Tue, 01 Dec 2020 02:42:37 GMT
RUN docker-php-ext-enable sodium
# Tue, 01 Dec 2020 02:42:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 01 Dec 2020 02:42:40 GMT
CMD ["php" "-a"]
# Tue, 01 Dec 2020 04:28:04 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Tue, 01 Dec 2020 04:28:05 GMT
STOPSIGNAL SIGINT
# Tue, 01 Dec 2020 04:28:12 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 01 Dec 2020 04:28:14 GMT
WORKDIR /var/www/html
# Tue, 01 Dec 2020 04:29:07 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Tue, 01 Dec 2020 04:29:08 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Tue, 08 Dec 2020 00:00:44 GMT
ENV ADMINER_VERSION=4.7.8
# Tue, 08 Dec 2020 00:00:49 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Tue, 08 Dec 2020 00:00:52 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Tue, 08 Dec 2020 00:00:57 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Tue, 08 Dec 2020 00:00:58 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 08 Dec 2020 00:00:59 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Tue, 08 Dec 2020 00:00:59 GMT
USER adminer
# Tue, 08 Dec 2020 00:01:00 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 08 Dec 2020 00:01:01 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:5f2023fd85a4e68f37fe41421fd89f30e69b98a645613521c57c01317561eee3`  
		Last Modified: Thu, 22 Oct 2020 01:58:45 GMT  
		Size: 2.4 MB (2405675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60b50c98f8a8e2c6a27378dfa0f44df1844ac67c6981303675f138a42679f25`  
		Last Modified: Thu, 22 Oct 2020 07:35:57 GMT  
		Size: 1.2 MB (1214265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b472094d673b7c272085505c976192b9aaafa3157c99bade9755fbca18a24071`  
		Last Modified: Thu, 22 Oct 2020 07:35:56 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc39e5d916c11e7eb158e72d14ab981eb45ccc7b6451c1d6d3cb627b71cdbb6`  
		Last Modified: Thu, 22 Oct 2020 07:35:55 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e834fd39435ea86b08faf9b3af2e2623e0a247fa06dfe096decdf80f7a986a`  
		Last Modified: Tue, 01 Dec 2020 04:00:44 GMT  
		Size: 10.3 MB (10338583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a458e4d5704bca7330dbfab239f74ff255f4813b58f19f50a4ad7fd7087f0c8`  
		Last Modified: Tue, 01 Dec 2020 04:00:43 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a500121bbd97abb5116b6e95bdaa9aed74160334e46aadaabef548dca0edce6`  
		Last Modified: Tue, 01 Dec 2020 04:00:46 GMT  
		Size: 12.7 MB (12706582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3321b09ca6255e6f5cb4dce9057df675dd4644a3654424c7ee95fbdcb083e9c`  
		Last Modified: Tue, 01 Dec 2020 04:00:42 GMT  
		Size: 2.3 KB (2257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:345450fde280cf49e34f7246cebd38e311d4b7bebe22415a6126c18e67899f91`  
		Last Modified: Tue, 01 Dec 2020 04:00:42 GMT  
		Size: 16.9 KB (16903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:520112c186c5f2a097e8056a524b7c35704923ebeb6247e924ca839fe6e5b343`  
		Last Modified: Tue, 01 Dec 2020 04:31:36 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d98e04775b392470b2f426804979b34d740103414161d9c89f4df0d0b086e51`  
		Last Modified: Tue, 01 Dec 2020 04:31:34 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c074206a89c8b669d116ecf57544d500dcdc5379828bb10e531adf7af19b658a`  
		Last Modified: Tue, 01 Dec 2020 04:31:34 GMT  
		Size: 3.9 MB (3926108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137384dc891a62af154426c4b36cb9192967da61547507bc1b95301727f85c39`  
		Last Modified: Tue, 01 Dec 2020 04:31:34 GMT  
		Size: 1.5 KB (1473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfdcb3be5430d4c822996a4b1f107a12cafae7d60cc6faf1f7a7cdd8dacaab94`  
		Last Modified: Tue, 08 Dec 2020 00:01:41 GMT  
		Size: 570.9 KB (570924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e55c2ae42163732e674f91058ca3617c71403e138adb01dd23c943ad95d6b0`  
		Last Modified: Tue, 08 Dec 2020 00:01:41 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7.8-standalone` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:b1e09cd04824b43f07df33154a383bc15923451af616eaaae657aca0620d729f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33702279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea6b86a866d797b65cc54d7527a70e1a5e91bf21ecc1ee3fd22b2a2c18d7f6ed`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 07:18:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 22 Oct 2020 07:18:56 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 22 Oct 2020 07:18:59 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 22 Oct 2020 07:19:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 22 Oct 2020 07:19:04 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 22 Oct 2020 07:19:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 07:19:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 07:19:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 22 Oct 2020 07:27:59 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 01 Dec 2020 03:27:01 GMT
ENV PHP_VERSION=7.4.13
# Tue, 01 Dec 2020 03:27:02 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Tue, 01 Dec 2020 03:27:03 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Tue, 01 Dec 2020 03:27:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 01 Dec 2020 03:27:09 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 01 Dec 2020 03:30:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 01 Dec 2020 03:30:42 GMT
COPY multi:afab483600631d4d87fe030871bbb016f1c2b73c0b72609d857bace419af7f5d in /usr/local/bin/ 
# Tue, 01 Dec 2020 03:30:50 GMT
RUN docker-php-ext-enable sodium
# Tue, 01 Dec 2020 03:30:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 01 Dec 2020 03:30:56 GMT
CMD ["php" "-a"]
# Tue, 01 Dec 2020 08:12:36 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Tue, 01 Dec 2020 08:12:37 GMT
STOPSIGNAL SIGINT
# Tue, 01 Dec 2020 08:12:39 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 01 Dec 2020 08:12:40 GMT
WORKDIR /var/www/html
# Tue, 01 Dec 2020 08:13:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Tue, 01 Dec 2020 08:13:23 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Mon, 07 Dec 2020 23:39:52 GMT
ENV ADMINER_VERSION=4.7.8
# Mon, 07 Dec 2020 23:39:53 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Mon, 07 Dec 2020 23:39:54 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Mon, 07 Dec 2020 23:39:56 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Mon, 07 Dec 2020 23:39:57 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Mon, 07 Dec 2020 23:39:58 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Mon, 07 Dec 2020 23:39:58 GMT
USER adminer
# Mon, 07 Dec 2020 23:39:59 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Mon, 07 Dec 2020 23:40:00 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d57dba23203172f8fffd1379aef0307e782178b62dfc684d43c546f7e874ed`  
		Last Modified: Thu, 22 Oct 2020 08:06:21 GMT  
		Size: 1.3 MB (1342784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8414edb0c9c2f7472bb6228bf691a2ddac19ddad7bad789c7cbdc147aded711`  
		Last Modified: Thu, 22 Oct 2020 08:06:20 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d26eeef0db35b2328adae38a8490c7403844452c3606dd17fbe68216f98e82`  
		Last Modified: Thu, 22 Oct 2020 08:06:19 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29be11fa56be3ca1af1498b259f3d5e058a869970cac6d670cf4ca1502485810`  
		Last Modified: Tue, 01 Dec 2020 04:53:56 GMT  
		Size: 10.3 MB (10338597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a553892b0358f6f72064d4dd5e727b686c4461cca7ea8a1211cc86adddb2cb`  
		Last Modified: Tue, 01 Dec 2020 04:53:56 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:828f98d07be67a182899230fc7e38e513de6ce85178d60116c765e90ffbc4119`  
		Last Modified: Tue, 01 Dec 2020 04:54:00 GMT  
		Size: 14.4 MB (14386945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec168016016eef2bef46796f7d7ec48af2459e14d65b9fc2871e756fe3e14d6a`  
		Last Modified: Tue, 01 Dec 2020 04:53:56 GMT  
		Size: 2.3 KB (2260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca32a186f8576115bc6fffe021ff54c52337662fa3cdb51c863d12d20ba02de`  
		Last Modified: Tue, 01 Dec 2020 04:53:55 GMT  
		Size: 17.0 KB (16976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b859cea4a3bb568911dd8f097b1a684daef31726fc5a591b4d9cd57b35187f`  
		Last Modified: Tue, 01 Dec 2020 08:14:59 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e97602a3ba690a845f8ecfaabcff93f82efc85a36445f6413d26f2482987638`  
		Last Modified: Tue, 01 Dec 2020 08:14:56 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6067b9bb9a3850bc39e227d17ab5df99a9bbe61e6d9933fc63c85e464f4aedf5`  
		Last Modified: Tue, 01 Dec 2020 08:14:57 GMT  
		Size: 4.3 MB (4331540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c677bbe386af33259d80d8f4d08a7147fef67adf472b9d841dac1a4a118c7f`  
		Last Modified: Tue, 01 Dec 2020 08:14:57 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4763c08ec3b1c7b68505b48ed92faf18a62525f8ce02d4fba750c232c1826aa9`  
		Last Modified: Mon, 07 Dec 2020 23:40:27 GMT  
		Size: 570.9 KB (570924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:983b1fb60b2afcee1aa424434071184fe8cf507838ac872e30e48755b41f1232`  
		Last Modified: Mon, 07 Dec 2020 23:40:28 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7.8-standalone` - linux; 386

```console
$ docker pull adminer@sha256:13a4c7ddafd6d4d6a5ee85529f6fa01ebe99d5c5bc1bcafafc85425658693817
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34626966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bb37df3c96977a9c7d5bcff85e2f3904eb30a1d4e2358f0c1644fae769a3ea7`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 22 Oct 2020 02:00:33 GMT
ADD file:46ad43b4984bcf49c5a888ff3628f23161f55cd1fb062f469e707100c97fa254 in / 
# Thu, 22 Oct 2020 02:00:33 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:36:23 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 22 Oct 2020 03:36:26 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 22 Oct 2020 03:36:27 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 22 Oct 2020 03:36:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 22 Oct 2020 03:36:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 22 Oct 2020 03:36:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 03:36:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 03:36:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 22 Oct 2020 03:55:07 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 01 Dec 2020 04:01:21 GMT
ENV PHP_VERSION=7.4.13
# Tue, 01 Dec 2020 04:01:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Tue, 01 Dec 2020 04:01:22 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Tue, 01 Dec 2020 04:01:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 01 Dec 2020 04:01:40 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 01 Dec 2020 04:10:51 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 01 Dec 2020 04:10:52 GMT
COPY multi:afab483600631d4d87fe030871bbb016f1c2b73c0b72609d857bace419af7f5d in /usr/local/bin/ 
# Tue, 01 Dec 2020 04:10:54 GMT
RUN docker-php-ext-enable sodium
# Tue, 01 Dec 2020 04:10:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 01 Dec 2020 04:10:55 GMT
CMD ["php" "-a"]
# Tue, 01 Dec 2020 09:24:38 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Tue, 01 Dec 2020 09:24:38 GMT
STOPSIGNAL SIGINT
# Tue, 01 Dec 2020 09:24:39 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 01 Dec 2020 09:24:39 GMT
WORKDIR /var/www/html
# Tue, 01 Dec 2020 09:25:13 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Tue, 01 Dec 2020 09:25:13 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Mon, 07 Dec 2020 23:38:24 GMT
ENV ADMINER_VERSION=4.7.8
# Mon, 07 Dec 2020 23:38:24 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Mon, 07 Dec 2020 23:38:24 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Mon, 07 Dec 2020 23:38:26 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Mon, 07 Dec 2020 23:38:26 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Mon, 07 Dec 2020 23:38:26 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Mon, 07 Dec 2020 23:38:26 GMT
USER adminer
# Mon, 07 Dec 2020 23:38:26 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Mon, 07 Dec 2020 23:38:27 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:d6ca64ac6f4b6382142ce9a3501652938130a6ec4bb02f3f455ee1f980834cfe`  
		Last Modified: Thu, 22 Oct 2020 02:00:57 GMT  
		Size: 2.8 MB (2791407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30be8ffd290910905a5fb7cbb70252eb0f59edb09db20bdc21f3b65456acc28f`  
		Last Modified: Thu, 22 Oct 2020 05:10:23 GMT  
		Size: 1.4 MB (1439641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d58e2433b13446c863e85b34f8e4c93ca9d5b3b93d2bac415fd9cdf77bcec4`  
		Last Modified: Thu, 22 Oct 2020 05:10:21 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5729dcb8d303f82a7f8cf3df49048e34ce8ee89f79155fb08a475da46b64308`  
		Last Modified: Thu, 22 Oct 2020 05:10:21 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ffdca9b500ff910069fefe63b455206db2cf0fa00dc6b7c7d53219dfaf7f5b`  
		Last Modified: Tue, 01 Dec 2020 07:15:13 GMT  
		Size: 10.3 MB (10338561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c682383cda14fca62843652d7478a26995cfbbfbcb457985de4ca5cfb77de751`  
		Last Modified: Tue, 01 Dec 2020 07:15:12 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57833a53685f649182bdbb4194ba35390c17fa65a6b09c4e377a42a5f9aaca30`  
		Last Modified: Tue, 01 Dec 2020 07:15:18 GMT  
		Size: 14.9 MB (14942640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7003874a29c37e250b24c310b448d1c36607cdb1b43128071780d5fd0a0dc3e1`  
		Last Modified: Tue, 01 Dec 2020 07:15:12 GMT  
		Size: 2.3 KB (2259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fcfab619124f72931608ea142c1cd80a26871e1631380720b6be739170e21b6`  
		Last Modified: Tue, 01 Dec 2020 07:15:12 GMT  
		Size: 16.9 KB (16924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055719a49e04df90bb23499c98da9779637e3b44446a60f202283f57e4b29b04`  
		Last Modified: Tue, 01 Dec 2020 09:26:14 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2b0f52d9f107a35a34b4f8c69abbdf24f2de8a0431c812d74cb6dd3cbf8bf2`  
		Last Modified: Tue, 01 Dec 2020 09:26:13 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4edb5ffb9c3f753b4991debfaeef5c535ae5d689a18b7fff9f0b042c5883865`  
		Last Modified: Tue, 01 Dec 2020 09:26:14 GMT  
		Size: 4.5 MB (4519100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9258866f679eb2cbc89aa311d5d2dad0c146a7e9f61c9e805b63d7f324d2afb0`  
		Last Modified: Tue, 01 Dec 2020 09:26:13 GMT  
		Size: 1.5 KB (1472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:904e3ae5079e7cd06213e6912d4237663cff97a37e1ed247e24b7f455951eafe`  
		Last Modified: Mon, 07 Dec 2020 23:38:45 GMT  
		Size: 570.9 KB (570859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:362b319c8a865e06c57265a80b857954a02a4e09ffe3eda699eede128dcdef90`  
		Last Modified: Mon, 07 Dec 2020 23:38:45 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7.8-standalone` - linux; ppc64le

```console
$ docker pull adminer@sha256:73feff7b317d1078b173d0c1dc928c14bf61e94b4562a0a79132b9dac74739aa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 MB (35029016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2bacaef82d901426ed9bf50182af16a98e04172b1d2dac51b87db0885487f72`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 22 Oct 2020 11:00:06 GMT
ADD file:176e047fab2c1828575bffa6b14773efa297b7ecf312d86103c5dd4f78ec8027 in / 
# Thu, 22 Oct 2020 11:00:17 GMT
CMD ["/bin/sh"]
# Fri, 23 Oct 2020 00:21:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 23 Oct 2020 00:21:18 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 23 Oct 2020 00:21:30 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 23 Oct 2020 00:21:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 23 Oct 2020 00:21:44 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 23 Oct 2020 00:21:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 23 Oct 2020 00:21:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 23 Oct 2020 00:21:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 23 Oct 2020 00:34:37 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 01 Dec 2020 03:52:39 GMT
ENV PHP_VERSION=7.4.13
# Tue, 01 Dec 2020 03:52:44 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Tue, 01 Dec 2020 03:52:51 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Tue, 01 Dec 2020 03:53:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 01 Dec 2020 03:53:13 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 01 Dec 2020 03:57:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 01 Dec 2020 03:57:24 GMT
COPY multi:afab483600631d4d87fe030871bbb016f1c2b73c0b72609d857bace419af7f5d in /usr/local/bin/ 
# Tue, 01 Dec 2020 03:57:33 GMT
RUN docker-php-ext-enable sodium
# Tue, 01 Dec 2020 03:57:36 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 01 Dec 2020 03:57:39 GMT
CMD ["php" "-a"]
# Tue, 01 Dec 2020 07:09:03 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Tue, 01 Dec 2020 07:09:12 GMT
STOPSIGNAL SIGINT
# Tue, 01 Dec 2020 07:09:25 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 01 Dec 2020 07:09:32 GMT
WORKDIR /var/www/html
# Tue, 01 Dec 2020 07:10:30 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Tue, 01 Dec 2020 07:10:33 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Tue, 08 Dec 2020 00:16:36 GMT
ENV ADMINER_VERSION=4.7.8
# Tue, 08 Dec 2020 00:16:38 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Tue, 08 Dec 2020 00:16:41 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Tue, 08 Dec 2020 00:16:53 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Tue, 08 Dec 2020 00:16:54 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 08 Dec 2020 00:16:58 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Tue, 08 Dec 2020 00:17:11 GMT
USER adminer
# Tue, 08 Dec 2020 00:17:16 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 08 Dec 2020 00:17:18 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:692a9d763e196c85d79fc3e45b316b1bb557c93ba88a3c8ebf679a585d1efe73`  
		Last Modified: Thu, 22 Oct 2020 11:02:06 GMT  
		Size: 2.8 MB (2803218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0285d6f06f3beb1c140c055210664c441b93dd4f2037177a5396bce94ca16ce5`  
		Last Modified: Fri, 23 Oct 2020 01:34:08 GMT  
		Size: 1.4 MB (1383187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a6459a3bf272daa53ff4ba97cc849676f497de9f78d8e9378ec02552293f175`  
		Last Modified: Fri, 23 Oct 2020 01:34:07 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16cff6064dc29d3f629d353736c1cac074caa5b50738422adb84de99a019bb32`  
		Last Modified: Fri, 23 Oct 2020 01:34:08 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0baf560776c5dd75b5673be3d73b900119615cfc4e4fe24414486e3d1f11920`  
		Last Modified: Tue, 01 Dec 2020 05:50:29 GMT  
		Size: 10.3 MB (10338609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4d8083b683ead9a591a00aff14c8d0091665e1433d301a027b214f19cbe23f`  
		Last Modified: Tue, 01 Dec 2020 05:50:29 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7381e6ce3e117510e5a2bf102da48e3cc1b5fd3414651ec324bbe759d367be`  
		Last Modified: Tue, 01 Dec 2020 05:50:32 GMT  
		Size: 15.5 MB (15548036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8328c4e67c6b29f383993d05557e298bc834c18c00961b9ab2a1c4e4eb05b4fd`  
		Last Modified: Tue, 01 Dec 2020 05:50:28 GMT  
		Size: 2.3 KB (2259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:236813d0f57da4fa9c0d5938846f85e82a0a01ce89ca208916b8f649c0ee99fd`  
		Last Modified: Tue, 01 Dec 2020 05:50:28 GMT  
		Size: 17.0 KB (16965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acf7ec6b5baaa9faab722bfc6a7098e0871e3edb42be513e64fe8e06bc7edec1`  
		Last Modified: Tue, 01 Dec 2020 07:14:36 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c17363dc3aab754805ecdc74f39535a73cfc5f3cebe72a4cb18fdc97df1ef9fa`  
		Last Modified: Tue, 01 Dec 2020 07:14:33 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95753fdce29daf55de647d3a29a8cc07941f7bf95fec4a560b0d698478b782f3`  
		Last Modified: Tue, 01 Dec 2020 07:14:34 GMT  
		Size: 4.4 MB (4360119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cad5fcb53526734d41770680ea56047b6e13c767960fc1d0a0b8de7c7030c75`  
		Last Modified: Tue, 01 Dec 2020 07:14:33 GMT  
		Size: 1.5 KB (1474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b231a33566f06d48010343aac194149b1ce1613cf2397c67cf1be2984295f133`  
		Last Modified: Tue, 08 Dec 2020 00:18:38 GMT  
		Size: 570.9 KB (570925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628d0ad1cc992636ad6e5a1f0cf7de70d844c7cccb85cda16205dc67b167e131`  
		Last Modified: Tue, 08 Dec 2020 00:18:38 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7.8-standalone` - linux; s390x

```console
$ docker pull adminer@sha256:6b00709e793594a51832541158adeb2ae42e00829dbfb77a54bc0eef7fd1668d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32521955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f75d1bfddd1544fe2cddf65f0baa090dfb992c4a38b43b24670dc3b1ce037d7`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 11 Dec 2020 02:09:52 GMT
ADD file:c9395a36a4e03768aabd282eb1f31705cc00181d3147222d9c940eaa5a8fd511 in / 
# Fri, 11 Dec 2020 02:09:53 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 11:30:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 11 Dec 2020 11:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 11 Dec 2020 11:30:56 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 11 Dec 2020 11:30:57 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 11 Dec 2020 11:30:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 11 Dec 2020 11:30:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Dec 2020 11:31:00 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Dec 2020 11:31:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 11 Dec 2020 12:01:46 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 11 Dec 2020 12:01:46 GMT
ENV PHP_VERSION=7.4.13
# Fri, 11 Dec 2020 12:01:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Fri, 11 Dec 2020 12:01:48 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Fri, 11 Dec 2020 12:01:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 11 Dec 2020 12:01:54 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Dec 2020 12:08:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Dec 2020 12:08:47 GMT
COPY multi:afab483600631d4d87fe030871bbb016f1c2b73c0b72609d857bace419af7f5d in /usr/local/bin/ 
# Fri, 11 Dec 2020 12:08:49 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Dec 2020 12:08:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Dec 2020 12:08:50 GMT
CMD ["php" "-a"]
# Fri, 11 Dec 2020 18:43:30 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 11 Dec 2020 18:43:31 GMT
STOPSIGNAL SIGINT
# Fri, 11 Dec 2020 18:43:33 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 11 Dec 2020 18:43:33 GMT
WORKDIR /var/www/html
# Fri, 11 Dec 2020 18:44:50 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 11 Dec 2020 18:44:50 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 11 Dec 2020 18:44:51 GMT
ENV ADMINER_VERSION=4.7.8
# Fri, 11 Dec 2020 18:44:52 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Fri, 11 Dec 2020 18:44:52 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Fri, 11 Dec 2020 18:44:56 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 11 Dec 2020 18:44:57 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 11 Dec 2020 18:44:57 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 11 Dec 2020 18:44:58 GMT
USER adminer
# Fri, 11 Dec 2020 18:44:59 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 11 Dec 2020 18:44:59 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:7c2470fe3d16cb70fca0826168095a96838b1322a8cd1502b28284ee8561b491`  
		Last Modified: Fri, 11 Dec 2020 02:10:27 GMT  
		Size: 2.6 MB (2565988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a23c8359d30ae261ad953f292e6681a71ebc7388607b74d901bbc07f71e1311`  
		Last Modified: Fri, 11 Dec 2020 13:48:01 GMT  
		Size: 1.4 MB (1382587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01422c3e898d3241d4134256bf0d911b0752823227af04614187c79c187e2843`  
		Last Modified: Fri, 11 Dec 2020 13:48:03 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a0be2077abd44f96e50bdebb1ed93a6e2b8d504761c23fa0e5e9b87045ca38`  
		Last Modified: Fri, 11 Dec 2020 13:48:01 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267bafe0bb23009994a23ad5cdcc3b4d425f186f0e488b5f7461463ad1b53814`  
		Last Modified: Fri, 11 Dec 2020 13:50:24 GMT  
		Size: 10.3 MB (10338590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36304b0fbddac7ce44edacaedb902676688cfc3bb7082576f6b57eed0ccc133e`  
		Last Modified: Fri, 11 Dec 2020 13:50:25 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fa33489075ff6318ffc5a7cf5c94cb4ce65ccfc82b5970cc91628780c130aae`  
		Last Modified: Fri, 11 Dec 2020 13:50:26 GMT  
		Size: 13.5 MB (13485898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155ae451461e50390ae0db27a78a329e87a86b9f9eb04f6db81fcc27430f2d51`  
		Last Modified: Fri, 11 Dec 2020 13:50:24 GMT  
		Size: 2.3 KB (2257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b379111cc7023c652243c4d9234de47984fa307030d667bf14e5d12889ec8180`  
		Last Modified: Fri, 11 Dec 2020 13:50:24 GMT  
		Size: 16.9 KB (16879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a18e16d8efd7f249149e2d38813d86590cc4a55f23d8c5bbba970725422ea51`  
		Last Modified: Fri, 11 Dec 2020 18:47:13 GMT  
		Size: 310.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ba44137233477a93edb1e0cc94bee3ce4dafaed9ff932d21594190f861ef75`  
		Last Modified: Fri, 11 Dec 2020 18:47:13 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cba732448866bbb0e567b7510578f951e9cf0bc258588c8e898be1606e3a3eb`  
		Last Modified: Fri, 11 Dec 2020 18:47:11 GMT  
		Size: 4.2 MB (4153155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8faf5f39c5d146bc658625977adca6ce417bb45b9683bb1767b99abfea6d3d56`  
		Last Modified: Fri, 11 Dec 2020 18:47:11 GMT  
		Size: 1.5 KB (1473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008d2a285f2f6bcf687be0cb08b167a975a4d7534a16435da10ba2b75b2e2d73`  
		Last Modified: Fri, 11 Dec 2020 18:47:11 GMT  
		Size: 570.9 KB (570918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6852608d1b2324d98a56de31e6fc11ac1fe8e95f605b50c9f72db2bd5cd092`  
		Last Modified: Fri, 11 Dec 2020 18:47:12 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:4.7-fastcgi`

```console
$ docker pull adminer@sha256:c0bcea38afeb9296d883e7371a4b83a97384f02ed2d2c3e71a6823267d6f0bac
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

### `adminer:4.7-fastcgi` - linux; amd64

```console
$ docker pull adminer@sha256:fb2f45c8e550ba3d59351c5ab1ac746adcab7dfb5e2d0b2a27531d2b664f598b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (34042656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff0774240cbda9b72e1940dc60ecd8366d3b4df4e789a7284078c8698364477`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 06:30:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 22 Oct 2020 06:30:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 22 Oct 2020 06:30:15 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 22 Oct 2020 06:30:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 22 Oct 2020 06:30:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 22 Oct 2020 06:37:19 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Thu, 22 Oct 2020 06:37:19 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 06:37:19 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 06:37:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 22 Oct 2020 06:49:00 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 01 Dec 2020 04:45:15 GMT
ENV PHP_VERSION=7.4.13
# Tue, 01 Dec 2020 04:45:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Tue, 01 Dec 2020 04:45:15 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Tue, 01 Dec 2020 04:45:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 01 Dec 2020 04:45:21 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 01 Dec 2020 04:54:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 01 Dec 2020 04:54:04 GMT
COPY multi:ebc915bbde1078ce3122b918e2e4c7726858af785343ade1a8d1a94f1052a4c7 in /usr/local/bin/ 
# Tue, 01 Dec 2020 04:54:07 GMT
RUN docker-php-ext-enable sodium
# Tue, 01 Dec 2020 04:54:07 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 01 Dec 2020 04:54:08 GMT
WORKDIR /var/www/html
# Tue, 01 Dec 2020 04:54:09 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Tue, 01 Dec 2020 04:54:10 GMT
STOPSIGNAL SIGQUIT
# Tue, 01 Dec 2020 04:54:10 GMT
EXPOSE 9000
# Tue, 01 Dec 2020 04:54:11 GMT
CMD ["php-fpm"]
# Tue, 01 Dec 2020 07:47:26 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Tue, 01 Dec 2020 07:47:28 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 01 Dec 2020 07:48:01 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Tue, 01 Dec 2020 07:48:01 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Tue, 08 Dec 2020 00:19:31 GMT
ENV ADMINER_VERSION=4.7.8
# Tue, 08 Dec 2020 00:19:31 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Tue, 08 Dec 2020 00:19:31 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Tue, 08 Dec 2020 00:19:33 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Tue, 08 Dec 2020 00:19:33 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 08 Dec 2020 00:19:33 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Tue, 08 Dec 2020 00:19:33 GMT
USER adminer
# Tue, 08 Dec 2020 00:19:33 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f8bf6cfdbe614fef94f982905079c16e27b3de2d24eb1ff513d3d83e656ca2`  
		Last Modified: Thu, 22 Oct 2020 07:36:55 GMT  
		Size: 1.3 MB (1340771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce5be79740125b9e74a77885bf6ee2b0d25ac7ed9e9432c5aa7210bb3b00458a`  
		Last Modified: Thu, 22 Oct 2020 07:36:55 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99dd6507fe563b66ba35badf706e1bbb2d39eb5d0a3c0d5a86a45d2af7e89c1`  
		Last Modified: Thu, 22 Oct 2020 07:36:55 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c3b45daa37929dd9a002107adb1299c5b070bbba60b73cf9ecc2d9fd6e78f9`  
		Last Modified: Tue, 01 Dec 2020 07:27:28 GMT  
		Size: 10.3 MB (10338571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6afb095daafcd5f742a42ee6dbf8f6d03fdca63c22071198f243df20ecef1db9`  
		Last Modified: Tue, 01 Dec 2020 07:27:25 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838cecfde999e9ecf65003522df2ce13e12fa5190e2336ffb1d16da9a787ead4`  
		Last Modified: Tue, 01 Dec 2020 07:27:29 GMT  
		Size: 14.6 MB (14640876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a46b7ab0f2d19433340bdeca3307275efd3188c446a3c739c1196c9bd05a0e`  
		Last Modified: Tue, 01 Dec 2020 07:27:26 GMT  
		Size: 2.3 KB (2255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d2139a9b9d18bdd892644fe463b368727e54ba53b145694a26f4cfe3f8e61d1`  
		Last Modified: Tue, 01 Dec 2020 07:27:26 GMT  
		Size: 17.0 KB (16987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f68d34619f5f9cff2cfac13cfa06e31e832bf261751b75ee11561cd3375e0207`  
		Last Modified: Tue, 01 Dec 2020 07:27:26 GMT  
		Size: 8.4 KB (8446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6bf2c8a87f5c9551aa94f68cd8ea11b9fb2f222d8cd8cdaf96b58fe86c98897`  
		Last Modified: Tue, 01 Dec 2020 07:48:39 GMT  
		Size: 310.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f16b55f73f8f895e7f07bc76cbc0c40ed52e4032e2129a9dbf41c7cb907c9e`  
		Last Modified: Tue, 01 Dec 2020 07:48:37 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a4fbbf03b1e145da6329a1d517b4ddaafee96bc3623a9dea8fcf2d3b1309ce4`  
		Last Modified: Tue, 01 Dec 2020 07:48:38 GMT  
		Size: 4.3 MB (4321450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b75ee2a57910d59b9ac6cb6de554264966343ef9391893d44eaf344ebca1bdc`  
		Last Modified: Tue, 01 Dec 2020 07:48:38 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12530476c9fea755fef449d62308ae3022da470522b4598087fcd3eb5bf68f7d`  
		Last Modified: Tue, 08 Dec 2020 00:19:56 GMT  
		Size: 570.9 KB (570859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5723a03bb2a4c99d35468a1f3e68d687f33c81fdce68c56aac53b1c689b5542`  
		Last Modified: Tue, 08 Dec 2020 00:19:55 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7-fastcgi` - linux; arm variant v6

```console
$ docker pull adminer@sha256:689204154221d2e4a097c834af056b991f880aed7a5a4a1e54d6c4422d965a6f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32149046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bb1805eba8cd29a4f28de65c3c539bac32ead0206c065984c55d1a699fd3b81`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 11 Dec 2020 02:17:15 GMT
ADD file:1a9c0a67560d338c0c0e7005d8915d998fc9cf3e9f53bfd7e42e8391f0a39bce in / 
# Fri, 11 Dec 2020 02:17:15 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 07:04:50 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 11 Dec 2020 07:04:53 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 11 Dec 2020 07:04:55 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 11 Dec 2020 07:04:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 11 Dec 2020 07:04:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 11 Dec 2020 07:09:12 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Fri, 11 Dec 2020 07:09:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Dec 2020 07:09:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Dec 2020 07:09:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 11 Dec 2020 07:17:56 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 11 Dec 2020 07:17:57 GMT
ENV PHP_VERSION=7.4.13
# Fri, 11 Dec 2020 07:17:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Fri, 11 Dec 2020 07:17:58 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Fri, 11 Dec 2020 07:18:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 11 Dec 2020 07:18:05 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Dec 2020 07:21:46 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Dec 2020 07:21:47 GMT
COPY multi:ebc915bbde1078ce3122b918e2e4c7726858af785343ade1a8d1a94f1052a4c7 in /usr/local/bin/ 
# Fri, 11 Dec 2020 07:21:51 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Dec 2020 07:21:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Dec 2020 07:21:53 GMT
WORKDIR /var/www/html
# Fri, 11 Dec 2020 07:21:56 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 11 Dec 2020 07:21:57 GMT
STOPSIGNAL SIGQUIT
# Fri, 11 Dec 2020 07:21:58 GMT
EXPOSE 9000
# Fri, 11 Dec 2020 07:21:59 GMT
CMD ["php-fpm"]
# Fri, 11 Dec 2020 09:05:35 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 11 Dec 2020 09:05:38 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 11 Dec 2020 09:06:36 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 11 Dec 2020 09:06:37 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 11 Dec 2020 09:06:38 GMT
ENV ADMINER_VERSION=4.7.8
# Fri, 11 Dec 2020 09:06:40 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Fri, 11 Dec 2020 09:06:41 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Fri, 11 Dec 2020 09:06:45 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 11 Dec 2020 09:06:46 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 11 Dec 2020 09:06:48 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 11 Dec 2020 09:06:50 GMT
USER adminer
# Fri, 11 Dec 2020 09:06:52 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:f1c16df8fee33d421d08790b17ca2af67a3fe49e77b6b991dd0c30631f5d1baf`  
		Last Modified: Fri, 11 Dec 2020 02:17:57 GMT  
		Size: 2.6 MB (2601992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623cc08cbe035cf15859e57a83e2243620418da06e1905d1875a46bec901e540`  
		Last Modified: Fri, 11 Dec 2020 07:56:49 GMT  
		Size: 1.3 MB (1310156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3a7aacff9b7ccf646f2bdbbc8d40bbb304550e813876049e721abd35461df9`  
		Last Modified: Fri, 11 Dec 2020 07:56:49 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d3214ea6f418597f370177309be7728f94481030c9cba6e45c4b74cfd04cc0`  
		Last Modified: Fri, 11 Dec 2020 07:56:49 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dff7159949c3c97335dda12e61ad77a87a4125ef93f88655500f4b8057cd38ca`  
		Last Modified: Fri, 11 Dec 2020 07:58:09 GMT  
		Size: 10.3 MB (10338600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c2c2f22a036ec3f2efaed4fd97c10faee4bbf539b56bf2e11b84a7c05b78fa`  
		Last Modified: Fri, 11 Dec 2020 07:58:05 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae33a5a224fa1ee298562bc31d50c9f804652bf619e4836e852c8860c5c49318`  
		Last Modified: Fri, 11 Dec 2020 07:58:09 GMT  
		Size: 13.3 MB (13267849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53c09a76a513338db42015101706a8bf9c7309d298d0a3329dee74810ea39db7`  
		Last Modified: Fri, 11 Dec 2020 07:58:05 GMT  
		Size: 2.3 KB (2260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e47c9c32a85f1170c19a3745c3a661a3a3c13e50daddef9919f624a52a70bc30`  
		Last Modified: Fri, 11 Dec 2020 07:58:05 GMT  
		Size: 16.9 KB (16891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbe39bbdfd22c5c467c010b89eb9561741273f56a2f378e08f2e055ef9ed919`  
		Last Modified: Fri, 11 Dec 2020 07:58:05 GMT  
		Size: 8.4 KB (8446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb3c1470d540138d5b667c3d6e30a34a3b783541ba0dc69a9714fa432a923970`  
		Last Modified: Fri, 11 Dec 2020 09:07:48 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f70879cf7eb8183ab6f68ad5f05f07b3e91a88ca27f7d935e91892073b1376`  
		Last Modified: Fri, 11 Dec 2020 09:07:46 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f69f96ec941427956045eb3c5673c21715d1878daf9035b7d11122c8cf62ed0c`  
		Last Modified: Fri, 11 Dec 2020 09:07:46 GMT  
		Size: 4.0 MB (4026251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a629622e0e5f22c28c625e3b6a9bef5d2136d403a64f88e8a44b1f1088caec2d`  
		Last Modified: Fri, 11 Dec 2020 09:07:45 GMT  
		Size: 1.5 KB (1470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec25251b0aa5ef178648ab40613c0031a55f133641f36b6c6e74dc5e79e4764`  
		Last Modified: Fri, 11 Dec 2020 09:07:46 GMT  
		Size: 570.9 KB (570918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71d17d806f1955405b240a9ef740c540c9e8ec5ceb8686ec081fda180677e50c`  
		Last Modified: Fri, 11 Dec 2020 09:07:45 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7-fastcgi` - linux; arm variant v7

```console
$ docker pull adminer@sha256:226eabf37d80fa4c86dc5fd621ba0b5c211967752c3e972a3929b9ffc4f4387c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31261925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efcd4d51f3642b6795c4c7140eaab8183af5f3b781a9099b95e1eba7d94d5683`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 22 Oct 2020 01:58:13 GMT
ADD file:46f89172426e9f5b1d669a2ca7ab218fc2deaef1caeeab88f2b5bd443ac9773d in / 
# Thu, 22 Oct 2020 01:58:14 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 06:47:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 22 Oct 2020 06:47:37 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 22 Oct 2020 06:47:45 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 22 Oct 2020 06:47:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 22 Oct 2020 06:47:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 22 Oct 2020 06:51:33 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Thu, 22 Oct 2020 06:51:36 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 06:51:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 06:51:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 22 Oct 2020 07:01:44 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 01 Dec 2020 02:43:04 GMT
ENV PHP_VERSION=7.4.13
# Tue, 01 Dec 2020 02:43:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Tue, 01 Dec 2020 02:43:24 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Tue, 01 Dec 2020 02:43:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 01 Dec 2020 02:43:39 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 01 Dec 2020 02:46:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 01 Dec 2020 02:46:34 GMT
COPY multi:ebc915bbde1078ce3122b918e2e4c7726858af785343ade1a8d1a94f1052a4c7 in /usr/local/bin/ 
# Tue, 01 Dec 2020 02:46:37 GMT
RUN docker-php-ext-enable sodium
# Tue, 01 Dec 2020 02:46:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 01 Dec 2020 02:46:39 GMT
WORKDIR /var/www/html
# Tue, 01 Dec 2020 02:46:42 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Tue, 01 Dec 2020 02:46:44 GMT
STOPSIGNAL SIGQUIT
# Tue, 01 Dec 2020 02:46:45 GMT
EXPOSE 9000
# Tue, 01 Dec 2020 02:46:46 GMT
CMD ["php-fpm"]
# Tue, 01 Dec 2020 04:29:50 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Tue, 01 Dec 2020 04:29:56 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 01 Dec 2020 04:30:45 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Tue, 01 Dec 2020 04:30:48 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Tue, 08 Dec 2020 00:01:12 GMT
ENV ADMINER_VERSION=4.7.8
# Tue, 08 Dec 2020 00:01:13 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Tue, 08 Dec 2020 00:01:14 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Tue, 08 Dec 2020 00:01:18 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Tue, 08 Dec 2020 00:01:20 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 08 Dec 2020 00:01:24 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Tue, 08 Dec 2020 00:01:25 GMT
USER adminer
# Tue, 08 Dec 2020 00:01:26 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:5f2023fd85a4e68f37fe41421fd89f30e69b98a645613521c57c01317561eee3`  
		Last Modified: Thu, 22 Oct 2020 01:58:45 GMT  
		Size: 2.4 MB (2405675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60b50c98f8a8e2c6a27378dfa0f44df1844ac67c6981303675f138a42679f25`  
		Last Modified: Thu, 22 Oct 2020 07:35:57 GMT  
		Size: 1.2 MB (1214265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b472094d673b7c272085505c976192b9aaafa3157c99bade9755fbca18a24071`  
		Last Modified: Thu, 22 Oct 2020 07:35:56 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc39e5d916c11e7eb158e72d14ab981eb45ccc7b6451c1d6d3cb627b71cdbb6`  
		Last Modified: Thu, 22 Oct 2020 07:35:55 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad5979536683af238cd5c6e9e7ee5171a2f468ba42667525bcf73dfbd4442d5c`  
		Last Modified: Tue, 01 Dec 2020 04:01:12 GMT  
		Size: 10.3 MB (10338579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83bfa48b04ad972c7ddc62f60703fd345236339c894ee5e02487d0a6912eec44`  
		Last Modified: Tue, 01 Dec 2020 04:01:08 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d500723729ab98b41c43300141cf87ecedf3122e848cb7f2871a8a18b472c9`  
		Last Modified: Tue, 01 Dec 2020 04:01:12 GMT  
		Size: 12.8 MB (12773054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ffe3faddffbb23fc7ec2b0ac5897aa6700b295f1129a52a58322108a7d7146`  
		Last Modified: Tue, 01 Dec 2020 04:01:08 GMT  
		Size: 2.3 KB (2260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c6599d32683be6cd2106e34a046a0a556bffd2baac97299eb69df7408f682be`  
		Last Modified: Tue, 01 Dec 2020 04:01:08 GMT  
		Size: 16.9 KB (16903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7158f5b17b11ddb8f243be54e5fc6112f6017d46780577a568a72e2e7d3f2cb1`  
		Last Modified: Tue, 01 Dec 2020 04:01:08 GMT  
		Size: 8.4 KB (8446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba8645bc546fe074d817500743f03a6b6b287793cee19306e5267095e410e7e`  
		Last Modified: Tue, 01 Dec 2020 04:32:00 GMT  
		Size: 310.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae84262bbd09928c80ab09696b0c7d2d57c5b58e28e089d2be9aae62bd0c7d0e`  
		Last Modified: Tue, 01 Dec 2020 04:31:59 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d45b8aa81cac48a3b6f2953fa3ad9d6047d134f7b76cbb3e05cbde0d6e0c7fc1`  
		Last Modified: Tue, 01 Dec 2020 04:31:59 GMT  
		Size: 3.9 MB (3926120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b483e9859bacb3a5557c81eda83e17a2559203c0979dcdd57bdcbe5729404c0f`  
		Last Modified: Tue, 01 Dec 2020 04:31:58 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7022a91847b0aaf7d1e067b9c3fa7620f93f349b64d2d7ebe0e816598a47fed2`  
		Last Modified: Tue, 08 Dec 2020 00:01:58 GMT  
		Size: 570.9 KB (570923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562e2ad43a7b07e5427acd85e75ec18c9dc4b21fe0a10fac08b447cfa140187f`  
		Last Modified: Tue, 08 Dec 2020 00:01:58 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7-fastcgi` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:89498585a4df7bcfaecdaadf8bee7b0b21018e861c1357c5826273c129cea8c1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.8 MB (33782483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57bc4d4eb9fffe27cb455d6f0c04677fd0798704e2673ac9c281b492fa593f03`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 07:18:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 22 Oct 2020 07:18:56 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 22 Oct 2020 07:18:59 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 22 Oct 2020 07:19:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 22 Oct 2020 07:19:04 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 22 Oct 2020 07:23:16 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Thu, 22 Oct 2020 07:23:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 07:23:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 07:23:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 22 Oct 2020 07:32:38 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 01 Dec 2020 03:31:07 GMT
ENV PHP_VERSION=7.4.13
# Tue, 01 Dec 2020 03:31:08 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Tue, 01 Dec 2020 03:31:09 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Tue, 01 Dec 2020 03:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 01 Dec 2020 03:31:15 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 01 Dec 2020 03:34:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 01 Dec 2020 03:35:01 GMT
COPY multi:ebc915bbde1078ce3122b918e2e4c7726858af785343ade1a8d1a94f1052a4c7 in /usr/local/bin/ 
# Tue, 01 Dec 2020 03:35:06 GMT
RUN docker-php-ext-enable sodium
# Tue, 01 Dec 2020 03:35:06 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 01 Dec 2020 03:35:08 GMT
WORKDIR /var/www/html
# Tue, 01 Dec 2020 03:35:10 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Tue, 01 Dec 2020 03:35:11 GMT
STOPSIGNAL SIGQUIT
# Tue, 01 Dec 2020 03:35:12 GMT
EXPOSE 9000
# Tue, 01 Dec 2020 03:35:13 GMT
CMD ["php-fpm"]
# Tue, 01 Dec 2020 08:13:43 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Tue, 01 Dec 2020 08:13:46 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 01 Dec 2020 08:14:29 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Tue, 01 Dec 2020 08:14:30 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Mon, 07 Dec 2020 23:40:07 GMT
ENV ADMINER_VERSION=4.7.8
# Mon, 07 Dec 2020 23:40:07 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Mon, 07 Dec 2020 23:40:08 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Mon, 07 Dec 2020 23:40:11 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Mon, 07 Dec 2020 23:40:12 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Mon, 07 Dec 2020 23:40:13 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Mon, 07 Dec 2020 23:40:14 GMT
USER adminer
# Mon, 07 Dec 2020 23:40:15 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d57dba23203172f8fffd1379aef0307e782178b62dfc684d43c546f7e874ed`  
		Last Modified: Thu, 22 Oct 2020 08:06:21 GMT  
		Size: 1.3 MB (1342784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8414edb0c9c2f7472bb6228bf691a2ddac19ddad7bad789c7cbdc147aded711`  
		Last Modified: Thu, 22 Oct 2020 08:06:20 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d26eeef0db35b2328adae38a8490c7403844452c3606dd17fbe68216f98e82`  
		Last Modified: Thu, 22 Oct 2020 08:06:19 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b747a72bda51ef2a52afed0eef10b56786e7c76ab30913f0e650a83b66935e4f`  
		Last Modified: Tue, 01 Dec 2020 04:54:24 GMT  
		Size: 10.3 MB (10338600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c684293922e5efaae5d67a6b158f6e54284e91081dda97b306a74ce97c9d0738`  
		Last Modified: Tue, 01 Dec 2020 04:54:21 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acdf0cad2cf9d86164e334858db58328dc251f08abe9d0841cc1bf520748163e`  
		Last Modified: Tue, 01 Dec 2020 04:54:25 GMT  
		Size: 14.5 MB (14458713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3417ec8fcb1bd4b4d3f295b89316912d8e33667e645450c3d0a2694887fea5da`  
		Last Modified: Tue, 01 Dec 2020 04:54:21 GMT  
		Size: 2.3 KB (2256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96e2c572c8bf97a5e221afc68cec20acaad7e29b919f242c6cb085234693b08`  
		Last Modified: Tue, 01 Dec 2020 04:54:22 GMT  
		Size: 17.0 KB (16978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:732bd773818e9fef29ad5ba55c5ddd1638077be22b0fd0a8f3a8bee4b600da11`  
		Last Modified: Tue, 01 Dec 2020 04:54:21 GMT  
		Size: 8.4 KB (8444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1886aa9fc4a1ad175dc4689b2f38537f04a005774f1c34b08ae3b8c3158fe5f8`  
		Last Modified: Tue, 01 Dec 2020 08:15:16 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf4e7f82086c970c52f8f544137e3286e990df9f19ad8567bba476226b12f61`  
		Last Modified: Tue, 01 Dec 2020 08:15:15 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4acc32056dfd0cd70bbc78cdfb34f2c627a433caff773366ad168a4945db066`  
		Last Modified: Tue, 01 Dec 2020 08:15:15 GMT  
		Size: 4.3 MB (4331531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb34a16b4bdb5625d39f3ef20da17bfecf2156cf9f3a647b4c4c26497af56b7`  
		Last Modified: Tue, 01 Dec 2020 08:15:15 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857d9231bfb81ba8cc071fbdcccdb6f9189f8e56d09ce9396b85b4e88b412b53`  
		Last Modified: Mon, 07 Dec 2020 23:40:43 GMT  
		Size: 570.9 KB (570920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a854be7b56f0667067e2d5d43ed47f9f068cb0e3f7976910fb604dda911121db`  
		Last Modified: Mon, 07 Dec 2020 23:40:43 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7-fastcgi` - linux; 386

```console
$ docker pull adminer@sha256:4f5fe39f0929ce4ac634729677768b268b328437e602e5a286881bb683086a5f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34705084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c8aa440257abba5e8b17a4be7767c0c3b8fc17f455e445f561495f8d394f849`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 22 Oct 2020 02:00:33 GMT
ADD file:46ad43b4984bcf49c5a888ff3628f23161f55cd1fb062f469e707100c97fa254 in / 
# Thu, 22 Oct 2020 02:00:33 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:36:23 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 22 Oct 2020 03:36:26 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 22 Oct 2020 03:36:27 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 22 Oct 2020 03:36:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 22 Oct 2020 03:36:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 22 Oct 2020 03:45:17 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Thu, 22 Oct 2020 03:45:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 03:45:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 03:45:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 22 Oct 2020 04:01:27 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 01 Dec 2020 04:11:03 GMT
ENV PHP_VERSION=7.4.13
# Tue, 01 Dec 2020 04:11:04 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Tue, 01 Dec 2020 04:11:04 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Tue, 01 Dec 2020 04:11:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 01 Dec 2020 04:11:13 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 01 Dec 2020 04:19:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 01 Dec 2020 04:19:54 GMT
COPY multi:ebc915bbde1078ce3122b918e2e4c7726858af785343ade1a8d1a94f1052a4c7 in /usr/local/bin/ 
# Tue, 01 Dec 2020 04:19:56 GMT
RUN docker-php-ext-enable sodium
# Tue, 01 Dec 2020 04:19:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 01 Dec 2020 04:19:56 GMT
WORKDIR /var/www/html
# Tue, 01 Dec 2020 04:19:57 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Tue, 01 Dec 2020 04:19:57 GMT
STOPSIGNAL SIGQUIT
# Tue, 01 Dec 2020 04:19:58 GMT
EXPOSE 9000
# Tue, 01 Dec 2020 04:19:58 GMT
CMD ["php-fpm"]
# Tue, 01 Dec 2020 09:25:25 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Tue, 01 Dec 2020 09:25:26 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 01 Dec 2020 09:25:53 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Tue, 01 Dec 2020 09:25:54 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Mon, 07 Dec 2020 23:38:31 GMT
ENV ADMINER_VERSION=4.7.8
# Mon, 07 Dec 2020 23:38:32 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Mon, 07 Dec 2020 23:38:32 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Mon, 07 Dec 2020 23:38:33 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Mon, 07 Dec 2020 23:38:33 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Mon, 07 Dec 2020 23:38:33 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Mon, 07 Dec 2020 23:38:34 GMT
USER adminer
# Mon, 07 Dec 2020 23:38:34 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:d6ca64ac6f4b6382142ce9a3501652938130a6ec4bb02f3f455ee1f980834cfe`  
		Last Modified: Thu, 22 Oct 2020 02:00:57 GMT  
		Size: 2.8 MB (2791407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30be8ffd290910905a5fb7cbb70252eb0f59edb09db20bdc21f3b65456acc28f`  
		Last Modified: Thu, 22 Oct 2020 05:10:23 GMT  
		Size: 1.4 MB (1439641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d58e2433b13446c863e85b34f8e4c93ca9d5b3b93d2bac415fd9cdf77bcec4`  
		Last Modified: Thu, 22 Oct 2020 05:10:21 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5729dcb8d303f82a7f8cf3df49048e34ce8ee89f79155fb08a475da46b64308`  
		Last Modified: Thu, 22 Oct 2020 05:10:21 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73c975f14cba63719b1acf30eb48c56e9ff5ab3ba3c93cc300551ed40f30ac4`  
		Last Modified: Tue, 01 Dec 2020 07:15:32 GMT  
		Size: 10.3 MB (10338565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8926789263a06364cefc6d6aee50b84a30291d014d2029ca669cb556f4c2bb1`  
		Last Modified: Tue, 01 Dec 2020 07:15:30 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcbe8e9cc07ddaae06ed92974d6d0a5249cac41ebb54331b56fc5c9e240eb993`  
		Last Modified: Tue, 01 Dec 2020 07:15:35 GMT  
		Size: 15.0 MB (15012323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e40c7a669cd74ab9dc3e2874416646f823f63c10d9b9a952a55dc1ad5bac9d`  
		Last Modified: Tue, 01 Dec 2020 07:15:30 GMT  
		Size: 2.3 KB (2260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed001fb8127577a70da6914dcf10ccb5d90ed9cf2a1cd3272618748f6b111d03`  
		Last Modified: Tue, 01 Dec 2020 07:15:29 GMT  
		Size: 16.9 KB (16920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90867a60ecf180a61e2ada4f0842adc2c2e44685c28753a5bed45de997db01e7`  
		Last Modified: Tue, 01 Dec 2020 07:15:29 GMT  
		Size: 8.4 KB (8442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3ce5df361365526e71aaf6df13804b7dedc099dd67740782cc739e0613eb110`  
		Last Modified: Tue, 01 Dec 2020 09:26:27 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a789bbdaebdf4bde2f5038d3a2a626522e4b2edc239b954288d23175ee69042`  
		Last Modified: Tue, 01 Dec 2020 09:26:26 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a79d0d02c93a44d0f6d1145f6ae0a0333e71fe94bfa8c63bd24354761d9587`  
		Last Modified: Tue, 01 Dec 2020 09:26:27 GMT  
		Size: 4.5 MB (4519093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85c74143366ffd582b27ed81dd1f35e4e314799a0de720b613b98b88ce787c77`  
		Last Modified: Tue, 01 Dec 2020 09:26:25 GMT  
		Size: 1.5 KB (1472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3529b652f01c65456c39d33fd9d239949548a0442b8a1fa9d2bf0a1c1f74b968`  
		Last Modified: Mon, 07 Dec 2020 23:38:54 GMT  
		Size: 570.9 KB (570861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a79e9613d8243f31a29bb14c13abf1a73d577720e86547b01bdef2bf8f9296bd`  
		Last Modified: Mon, 07 Dec 2020 23:38:54 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7-fastcgi` - linux; ppc64le

```console
$ docker pull adminer@sha256:0671ac686df177a55af6924323ebcc05a17cb4bf61a6372df21a1a0c22487346
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.1 MB (35117996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:959c6c5b577d14c45504ecdd9a75e110b1afb1e5e8651a224075e4784c97c07c`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 22 Oct 2020 11:00:06 GMT
ADD file:176e047fab2c1828575bffa6b14773efa297b7ecf312d86103c5dd4f78ec8027 in / 
# Thu, 22 Oct 2020 11:00:17 GMT
CMD ["/bin/sh"]
# Fri, 23 Oct 2020 00:21:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 23 Oct 2020 00:21:18 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 23 Oct 2020 00:21:30 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 23 Oct 2020 00:21:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 23 Oct 2020 00:21:44 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 23 Oct 2020 00:27:50 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Fri, 23 Oct 2020 00:27:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 23 Oct 2020 00:28:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 23 Oct 2020 00:28:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 23 Oct 2020 00:39:53 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 01 Dec 2020 03:57:52 GMT
ENV PHP_VERSION=7.4.13
# Tue, 01 Dec 2020 03:57:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Tue, 01 Dec 2020 03:58:02 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Tue, 01 Dec 2020 03:58:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 01 Dec 2020 03:58:37 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 01 Dec 2020 04:02:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 01 Dec 2020 04:02:41 GMT
COPY multi:ebc915bbde1078ce3122b918e2e4c7726858af785343ade1a8d1a94f1052a4c7 in /usr/local/bin/ 
# Tue, 01 Dec 2020 04:02:55 GMT
RUN docker-php-ext-enable sodium
# Tue, 01 Dec 2020 04:02:59 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 01 Dec 2020 04:03:05 GMT
WORKDIR /var/www/html
# Tue, 01 Dec 2020 04:03:27 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Tue, 01 Dec 2020 04:03:33 GMT
STOPSIGNAL SIGQUIT
# Tue, 01 Dec 2020 04:03:40 GMT
EXPOSE 9000
# Tue, 01 Dec 2020 04:03:44 GMT
CMD ["php-fpm"]
# Tue, 01 Dec 2020 07:11:43 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Tue, 01 Dec 2020 07:11:59 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 01 Dec 2020 07:12:55 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Tue, 01 Dec 2020 07:12:59 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Tue, 08 Dec 2020 00:17:37 GMT
ENV ADMINER_VERSION=4.7.8
# Tue, 08 Dec 2020 00:17:44 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Tue, 08 Dec 2020 00:17:47 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Tue, 08 Dec 2020 00:17:56 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Tue, 08 Dec 2020 00:17:59 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 08 Dec 2020 00:18:03 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Tue, 08 Dec 2020 00:18:08 GMT
USER adminer
# Tue, 08 Dec 2020 00:18:15 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:692a9d763e196c85d79fc3e45b316b1bb557c93ba88a3c8ebf679a585d1efe73`  
		Last Modified: Thu, 22 Oct 2020 11:02:06 GMT  
		Size: 2.8 MB (2803218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0285d6f06f3beb1c140c055210664c441b93dd4f2037177a5396bce94ca16ce5`  
		Last Modified: Fri, 23 Oct 2020 01:34:08 GMT  
		Size: 1.4 MB (1383187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a6459a3bf272daa53ff4ba97cc849676f497de9f78d8e9378ec02552293f175`  
		Last Modified: Fri, 23 Oct 2020 01:34:07 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16cff6064dc29d3f629d353736c1cac074caa5b50738422adb84de99a019bb32`  
		Last Modified: Fri, 23 Oct 2020 01:34:08 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67dcc2a717f8153769df04bd895be154aca7c3fc20560f37da5b36e0fbd9efbd`  
		Last Modified: Tue, 01 Dec 2020 05:51:15 GMT  
		Size: 10.3 MB (10338603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9502fa9f26f9855ddcfd4309edb7c16ce7517f1c88a60155b169e6182acbdd17`  
		Last Modified: Tue, 01 Dec 2020 05:51:09 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf065529921adbb64e6889d9cfa225de7f8aa65204f3ec400330d4fc989de4d8`  
		Last Modified: Tue, 01 Dec 2020 05:51:13 GMT  
		Size: 15.6 MB (15628567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e91de5593ec1aa89d021215583d63f94d4f36d9608f29dd460ede4c7290ebb7`  
		Last Modified: Tue, 01 Dec 2020 05:51:09 GMT  
		Size: 2.3 KB (2255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede5b0209a637a8111ae77c919a561733c6e703c97333ecea99a4abbecf8a2c5`  
		Last Modified: Tue, 01 Dec 2020 05:51:09 GMT  
		Size: 17.0 KB (16968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e851350ac3fff1de99c14298cb35f46c409629186a85f22c22a0be19f4f7cd`  
		Last Modified: Tue, 01 Dec 2020 05:51:09 GMT  
		Size: 8.4 KB (8441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df2bf3b8e2936ee1044358dfd1700fce3f08592b60bac9086d1d4677f3de8ca9`  
		Last Modified: Tue, 01 Dec 2020 07:15:16 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bcb7b3aa24f4c386111b1860808ec662939186fbbf6ea9be1a4309880e34a17`  
		Last Modified: Tue, 01 Dec 2020 07:15:13 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:088e76bc30b441c5832343aa548abe6c770bd754156485a0b235f1cf92cac64e`  
		Last Modified: Tue, 01 Dec 2020 07:15:14 GMT  
		Size: 4.4 MB (4360124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:587c025ae0482b8d3b5e8fc26b4af5eae6dc22c5c3da95ca52fbfc9c9a5b2f3a`  
		Last Modified: Tue, 01 Dec 2020 07:15:12 GMT  
		Size: 1.5 KB (1479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45314773dc31f89543794af67d864efadc99ec57ce116a3760d41a4c207f6f30`  
		Last Modified: Tue, 08 Dec 2020 00:19:11 GMT  
		Size: 570.9 KB (570925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4283c4537d91df6ad82cb299758a89bc3a5d2a8f42ddfe40ea81b189e8d6fb0`  
		Last Modified: Tue, 08 Dec 2020 00:19:11 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7-fastcgi` - linux; s390x

```console
$ docker pull adminer@sha256:1f93751408862e70ce3d4b81bd3d7bdb4e2ecac81606992543e7bbfdbf90f96b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32598207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9061e3e2134cb0ffa169546bbf7624fe55bbea5f40e1b70016744979434fcc7d`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 11 Dec 2020 02:09:52 GMT
ADD file:c9395a36a4e03768aabd282eb1f31705cc00181d3147222d9c940eaa5a8fd511 in / 
# Fri, 11 Dec 2020 02:09:53 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 11:30:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 11 Dec 2020 11:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 11 Dec 2020 11:30:56 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 11 Dec 2020 11:30:57 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 11 Dec 2020 11:30:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 11 Dec 2020 11:36:17 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Fri, 11 Dec 2020 11:36:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Dec 2020 11:36:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Dec 2020 11:36:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 11 Dec 2020 12:09:03 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 11 Dec 2020 12:09:04 GMT
ENV PHP_VERSION=7.4.13
# Fri, 11 Dec 2020 12:09:04 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Fri, 11 Dec 2020 12:09:05 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Fri, 11 Dec 2020 12:09:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 11 Dec 2020 12:09:12 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Dec 2020 12:13:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Dec 2020 12:13:55 GMT
COPY multi:ebc915bbde1078ce3122b918e2e4c7726858af785343ade1a8d1a94f1052a4c7 in /usr/local/bin/ 
# Fri, 11 Dec 2020 12:13:57 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Dec 2020 12:13:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Dec 2020 12:13:59 GMT
WORKDIR /var/www/html
# Fri, 11 Dec 2020 12:14:00 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 11 Dec 2020 12:14:01 GMT
STOPSIGNAL SIGQUIT
# Fri, 11 Dec 2020 12:14:01 GMT
EXPOSE 9000
# Fri, 11 Dec 2020 12:14:02 GMT
CMD ["php-fpm"]
# Fri, 11 Dec 2020 18:45:19 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 11 Dec 2020 18:45:21 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 11 Dec 2020 18:46:30 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 11 Dec 2020 18:46:31 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 11 Dec 2020 18:46:32 GMT
ENV ADMINER_VERSION=4.7.8
# Fri, 11 Dec 2020 18:46:32 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Fri, 11 Dec 2020 18:46:33 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Fri, 11 Dec 2020 18:46:36 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 11 Dec 2020 18:46:37 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 11 Dec 2020 18:46:38 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 11 Dec 2020 18:46:38 GMT
USER adminer
# Fri, 11 Dec 2020 18:46:39 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:7c2470fe3d16cb70fca0826168095a96838b1322a8cd1502b28284ee8561b491`  
		Last Modified: Fri, 11 Dec 2020 02:10:27 GMT  
		Size: 2.6 MB (2565988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a23c8359d30ae261ad953f292e6681a71ebc7388607b74d901bbc07f71e1311`  
		Last Modified: Fri, 11 Dec 2020 13:48:01 GMT  
		Size: 1.4 MB (1382587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01422c3e898d3241d4134256bf0d911b0752823227af04614187c79c187e2843`  
		Last Modified: Fri, 11 Dec 2020 13:48:03 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a0be2077abd44f96e50bdebb1ed93a6e2b8d504761c23fa0e5e9b87045ca38`  
		Last Modified: Fri, 11 Dec 2020 13:48:01 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:797fc05bf988e85a5cf643f2d07a0b08a36e3f1529c75c41a2460041b6ee0f43`  
		Last Modified: Fri, 11 Dec 2020 13:50:52 GMT  
		Size: 10.3 MB (10338591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e11bb5dc7804a50c805852fbe653bb133478f5005e8c78c1d712af0d5bd6db4`  
		Last Modified: Fri, 11 Dec 2020 13:50:49 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:311bfe9de08521ea35d7a1520e00de8215315e5a8144a4335f1313ad7f6593de`  
		Last Modified: Fri, 11 Dec 2020 13:50:51 GMT  
		Size: 13.6 MB (13553700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59a788dffbadef519f959d8de10a3156add64ed4e15c8e96045a3bebf9ef316`  
		Last Modified: Fri, 11 Dec 2020 13:50:49 GMT  
		Size: 2.3 KB (2260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:898ee507348c01a8028e7ad08c8af3edde13cd884ffdfd990ad679df9b004552`  
		Last Modified: Fri, 11 Dec 2020 13:50:49 GMT  
		Size: 16.9 KB (16883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a7bec784d5537500a8f385256905e367037e6e1ae365f119cf3a305c384338f`  
		Last Modified: Fri, 11 Dec 2020 13:50:50 GMT  
		Size: 8.4 KB (8445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aacad6fcb4ce89b6aebc70fa08e0aeaf4004bdfd4288064a050ae7a6b6a1ca5`  
		Last Modified: Fri, 11 Dec 2020 18:47:37 GMT  
		Size: 310.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed17bffefe5fed1ad7e5ba183155f268ef4c6f19e11ce2b4d2b51a756f56e38`  
		Last Modified: Fri, 11 Dec 2020 18:47:32 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:195c8eb0f725b2189839adb7a0fec2e91f3b597dcf7a9a35cdb3cde9beea8e03`  
		Last Modified: Fri, 11 Dec 2020 18:47:33 GMT  
		Size: 4.2 MB (4153144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dd4956eb56581838eebbd42956889e3cc9dd1e7526a1282b8075c4c7daf28d1`  
		Last Modified: Fri, 11 Dec 2020 18:47:33 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a7b5a1b8dcaeb2cdc7acda96210109729ec955718cf8d30f683176a9ecf87be`  
		Last Modified: Fri, 11 Dec 2020 18:47:32 GMT  
		Size: 570.9 KB (570919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a3464ffffa7b21ee6c5a53d2f9143c982205d77f77a55bf9ec4ebb2cdff801`  
		Last Modified: Fri, 11 Dec 2020 18:47:33 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:4.7-standalone`

```console
$ docker pull adminer@sha256:4600f2453f7c9f3ee8179016a65d0b49a8dfb89467ac0947a6245e62e7f81fb1
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

### `adminer:4.7-standalone` - linux; amd64

```console
$ docker pull adminer@sha256:4b087576de7b4ca7c60bb3558f0b5ee30f496cee10fa19ea0a9f0e071c72b1f5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (33965375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2db7241b0f1461d8707525832e608fe513453f99c11beed9413194f7519e05`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 06:30:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 22 Oct 2020 06:30:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 22 Oct 2020 06:30:15 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 22 Oct 2020 06:30:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 22 Oct 2020 06:30:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 22 Oct 2020 06:30:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 06:30:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 06:30:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 22 Oct 2020 06:43:41 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 01 Dec 2020 04:36:20 GMT
ENV PHP_VERSION=7.4.13
# Tue, 01 Dec 2020 04:36:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Tue, 01 Dec 2020 04:36:21 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Tue, 01 Dec 2020 04:36:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 01 Dec 2020 04:36:27 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 01 Dec 2020 04:44:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 01 Dec 2020 04:44:54 GMT
COPY multi:afab483600631d4d87fe030871bbb016f1c2b73c0b72609d857bace419af7f5d in /usr/local/bin/ 
# Tue, 01 Dec 2020 04:44:57 GMT
RUN docker-php-ext-enable sodium
# Tue, 01 Dec 2020 04:44:57 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 01 Dec 2020 04:44:57 GMT
CMD ["php" "-a"]
# Tue, 01 Dec 2020 07:46:46 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Tue, 01 Dec 2020 07:46:46 GMT
STOPSIGNAL SIGINT
# Tue, 01 Dec 2020 07:46:47 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 01 Dec 2020 07:46:48 GMT
WORKDIR /var/www/html
# Tue, 01 Dec 2020 07:47:15 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Tue, 01 Dec 2020 07:47:15 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Tue, 08 Dec 2020 00:19:24 GMT
ENV ADMINER_VERSION=4.7.8
# Tue, 08 Dec 2020 00:19:24 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Tue, 08 Dec 2020 00:19:24 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Tue, 08 Dec 2020 00:19:26 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Tue, 08 Dec 2020 00:19:26 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 08 Dec 2020 00:19:26 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Tue, 08 Dec 2020 00:19:26 GMT
USER adminer
# Tue, 08 Dec 2020 00:19:27 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 08 Dec 2020 00:19:27 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f8bf6cfdbe614fef94f982905079c16e27b3de2d24eb1ff513d3d83e656ca2`  
		Last Modified: Thu, 22 Oct 2020 07:36:55 GMT  
		Size: 1.3 MB (1340771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce5be79740125b9e74a77885bf6ee2b0d25ac7ed9e9432c5aa7210bb3b00458a`  
		Last Modified: Thu, 22 Oct 2020 07:36:55 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99dd6507fe563b66ba35badf706e1bbb2d39eb5d0a3c0d5a86a45d2af7e89c1`  
		Last Modified: Thu, 22 Oct 2020 07:36:55 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c513a1b503cf7c9f18fa014dada9744070ded92dc9ad548cd056c4f56dc1a9`  
		Last Modified: Tue, 01 Dec 2020 07:27:10 GMT  
		Size: 10.3 MB (10338569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff080eafb4c0518981fca6aef4d239863fc59195f41ce7c440b2c6c518f2ac79`  
		Last Modified: Tue, 01 Dec 2020 07:27:09 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e818119992b11dbf09b710066a78920985b9ea1310fc8272df816e0884985f44`  
		Last Modified: Tue, 01 Dec 2020 07:27:13 GMT  
		Size: 14.6 MB (14572037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba3c14a67f95ae52ebfb558ab6b5d87687a05ce41c8df0a618ff42b73204e40`  
		Last Modified: Tue, 01 Dec 2020 07:27:09 GMT  
		Size: 2.3 KB (2257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbb0285b7ad2b170e4ed2cffbe0f16ba55d689c056ff43767834783eab7b8261`  
		Last Modified: Tue, 01 Dec 2020 07:27:09 GMT  
		Size: 17.0 KB (16987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae324cfad8acf03b3a98a15e963b7046404a7da3a6bbf68fd65d37f899f194d`  
		Last Modified: Tue, 01 Dec 2020 07:48:25 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb51158f683d66315de6fa572f7ea13d8ffb71ac85faa20c8578edb11678f37d`  
		Last Modified: Tue, 01 Dec 2020 07:48:23 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71ac21b64d1d63d967acb13664404babd0ef86fc896c484ce28cccf70001d0f1`  
		Last Modified: Tue, 01 Dec 2020 07:48:24 GMT  
		Size: 4.3 MB (4321455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2170e09d39d861e9bb7a5da5def906b44153b6c481fe17925ba82d1f1f78eec`  
		Last Modified: Tue, 01 Dec 2020 07:48:24 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d95b48dfa11f7f5c061f6522f6ff5d574452b8f321c6075455da2643b1967a`  
		Last Modified: Tue, 08 Dec 2020 00:19:45 GMT  
		Size: 570.9 KB (570860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3bb2b5e72bf0dbd4b855ddf65aaf9c0d077703804bdbdc9ea3ea98cbbfceaf6`  
		Last Modified: Tue, 08 Dec 2020 00:19:44 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7-standalone` - linux; arm variant v6

```console
$ docker pull adminer@sha256:7e114494e5e3a8ece382083d27c33f6c993695f0ff6c92c235ced149177f5da9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32073857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9cfa5ccbab063435267257cf4c761402c956233cf22775ed1c774b53a045715`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 11 Dec 2020 02:17:15 GMT
ADD file:1a9c0a67560d338c0c0e7005d8915d998fc9cf3e9f53bfd7e42e8391f0a39bce in / 
# Fri, 11 Dec 2020 02:17:15 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 07:04:50 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 11 Dec 2020 07:04:53 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 11 Dec 2020 07:04:55 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 11 Dec 2020 07:04:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 11 Dec 2020 07:04:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 11 Dec 2020 07:05:00 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Dec 2020 07:05:01 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Dec 2020 07:05:02 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 11 Dec 2020 07:13:50 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 11 Dec 2020 07:13:54 GMT
ENV PHP_VERSION=7.4.13
# Fri, 11 Dec 2020 07:13:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Fri, 11 Dec 2020 07:13:56 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Fri, 11 Dec 2020 07:14:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 11 Dec 2020 07:14:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Dec 2020 07:17:37 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Dec 2020 07:17:39 GMT
COPY multi:afab483600631d4d87fe030871bbb016f1c2b73c0b72609d857bace419af7f5d in /usr/local/bin/ 
# Fri, 11 Dec 2020 07:17:42 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Dec 2020 07:17:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Dec 2020 07:17:43 GMT
CMD ["php" "-a"]
# Fri, 11 Dec 2020 09:04:18 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 11 Dec 2020 09:04:19 GMT
STOPSIGNAL SIGINT
# Fri, 11 Dec 2020 09:04:21 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 11 Dec 2020 09:04:22 GMT
WORKDIR /var/www/html
# Fri, 11 Dec 2020 09:05:06 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 11 Dec 2020 09:05:08 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 11 Dec 2020 09:05:08 GMT
ENV ADMINER_VERSION=4.7.8
# Fri, 11 Dec 2020 09:05:09 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Fri, 11 Dec 2020 09:05:11 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Fri, 11 Dec 2020 09:05:14 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 11 Dec 2020 09:05:15 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 11 Dec 2020 09:05:16 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 11 Dec 2020 09:05:17 GMT
USER adminer
# Fri, 11 Dec 2020 09:05:18 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 11 Dec 2020 09:05:19 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:f1c16df8fee33d421d08790b17ca2af67a3fe49e77b6b991dd0c30631f5d1baf`  
		Last Modified: Fri, 11 Dec 2020 02:17:57 GMT  
		Size: 2.6 MB (2601992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623cc08cbe035cf15859e57a83e2243620418da06e1905d1875a46bec901e540`  
		Last Modified: Fri, 11 Dec 2020 07:56:49 GMT  
		Size: 1.3 MB (1310156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3a7aacff9b7ccf646f2bdbbc8d40bbb304550e813876049e721abd35461df9`  
		Last Modified: Fri, 11 Dec 2020 07:56:49 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d3214ea6f418597f370177309be7728f94481030c9cba6e45c4b74cfd04cc0`  
		Last Modified: Fri, 11 Dec 2020 07:56:49 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64de18534c9c3dd7212eceb5a285d571df578238ca4684a2e922b131e9947d79`  
		Last Modified: Fri, 11 Dec 2020 07:57:40 GMT  
		Size: 10.3 MB (10338603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d60b5c1c75b96676e4154f74a500fdd4a2645d4c51e189b0bdd18e06f26c3143`  
		Last Modified: Fri, 11 Dec 2020 07:57:39 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee32c3be90bc13cb4b3406c492ec35d5c211ac42b25e536939fb3220aea672b`  
		Last Modified: Fri, 11 Dec 2020 07:57:44 GMT  
		Size: 13.2 MB (13201116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e71cdda7d8acfe2fe1a6263c1b004b3ae972d7ce1c0ac95fec09aa0c0ba1f7fd`  
		Last Modified: Fri, 11 Dec 2020 07:57:39 GMT  
		Size: 2.3 KB (2258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec74a6ee1beba601eed5abe261394c8ddfa2d53093a1f6768356ec5891066746`  
		Last Modified: Fri, 11 Dec 2020 07:57:40 GMT  
		Size: 16.9 KB (16889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b84bf5ad218839b4e8156c322c5611b3c26167141a7c1e8049055deeda8b1ed5`  
		Last Modified: Fri, 11 Dec 2020 09:07:23 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0113ef6e65685219488d6543639cff152292617519f4649a6d7c8e4bbf03322b`  
		Last Modified: Fri, 11 Dec 2020 09:07:21 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2501c821a30d874046f30dd9d3947aa9f82cca3e9d39eb18214a765744e0b24`  
		Last Modified: Fri, 11 Dec 2020 09:07:21 GMT  
		Size: 4.0 MB (4026242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:945b172c5cf67a28a59e5b25cfed08871f360f551a912c8d7f64c096d6554812`  
		Last Modified: Fri, 11 Dec 2020 09:07:20 GMT  
		Size: 1.5 KB (1473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df40a3aa85441cb471ce645d5a0a2564fb9e2f042e078b8f04dd343488863a4`  
		Last Modified: Fri, 11 Dec 2020 09:07:20 GMT  
		Size: 570.9 KB (570917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90644dda17e22024741efd92b2987150a52659ae6bb25b7ea232e9b72d3b1d83`  
		Last Modified: Fri, 11 Dec 2020 09:07:20 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7-standalone` - linux; arm variant v7

```console
$ docker pull adminer@sha256:39b988e9485b8f06142e8584a4764c3c32159d51377eab0739b1cf794f701d1a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31186995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d4ed3310dfe2d29dd9a809a5ea826952ac518c5d93ab5e12054d9b7560791f7`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 22 Oct 2020 01:58:13 GMT
ADD file:46f89172426e9f5b1d669a2ca7ab218fc2deaef1caeeab88f2b5bd443ac9773d in / 
# Thu, 22 Oct 2020 01:58:14 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 06:47:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 22 Oct 2020 06:47:37 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 22 Oct 2020 06:47:45 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 22 Oct 2020 06:47:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 22 Oct 2020 06:47:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 22 Oct 2020 06:47:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 06:47:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 06:48:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 22 Oct 2020 06:56:26 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 01 Dec 2020 02:39:45 GMT
ENV PHP_VERSION=7.4.13
# Tue, 01 Dec 2020 02:39:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Tue, 01 Dec 2020 02:39:46 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Tue, 01 Dec 2020 02:39:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 01 Dec 2020 02:39:53 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 01 Dec 2020 02:42:30 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 01 Dec 2020 02:42:32 GMT
COPY multi:afab483600631d4d87fe030871bbb016f1c2b73c0b72609d857bace419af7f5d in /usr/local/bin/ 
# Tue, 01 Dec 2020 02:42:37 GMT
RUN docker-php-ext-enable sodium
# Tue, 01 Dec 2020 02:42:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 01 Dec 2020 02:42:40 GMT
CMD ["php" "-a"]
# Tue, 01 Dec 2020 04:28:04 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Tue, 01 Dec 2020 04:28:05 GMT
STOPSIGNAL SIGINT
# Tue, 01 Dec 2020 04:28:12 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 01 Dec 2020 04:28:14 GMT
WORKDIR /var/www/html
# Tue, 01 Dec 2020 04:29:07 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Tue, 01 Dec 2020 04:29:08 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Tue, 08 Dec 2020 00:00:44 GMT
ENV ADMINER_VERSION=4.7.8
# Tue, 08 Dec 2020 00:00:49 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Tue, 08 Dec 2020 00:00:52 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Tue, 08 Dec 2020 00:00:57 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Tue, 08 Dec 2020 00:00:58 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 08 Dec 2020 00:00:59 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Tue, 08 Dec 2020 00:00:59 GMT
USER adminer
# Tue, 08 Dec 2020 00:01:00 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 08 Dec 2020 00:01:01 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:5f2023fd85a4e68f37fe41421fd89f30e69b98a645613521c57c01317561eee3`  
		Last Modified: Thu, 22 Oct 2020 01:58:45 GMT  
		Size: 2.4 MB (2405675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60b50c98f8a8e2c6a27378dfa0f44df1844ac67c6981303675f138a42679f25`  
		Last Modified: Thu, 22 Oct 2020 07:35:57 GMT  
		Size: 1.2 MB (1214265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b472094d673b7c272085505c976192b9aaafa3157c99bade9755fbca18a24071`  
		Last Modified: Thu, 22 Oct 2020 07:35:56 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc39e5d916c11e7eb158e72d14ab981eb45ccc7b6451c1d6d3cb627b71cdbb6`  
		Last Modified: Thu, 22 Oct 2020 07:35:55 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e834fd39435ea86b08faf9b3af2e2623e0a247fa06dfe096decdf80f7a986a`  
		Last Modified: Tue, 01 Dec 2020 04:00:44 GMT  
		Size: 10.3 MB (10338583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a458e4d5704bca7330dbfab239f74ff255f4813b58f19f50a4ad7fd7087f0c8`  
		Last Modified: Tue, 01 Dec 2020 04:00:43 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a500121bbd97abb5116b6e95bdaa9aed74160334e46aadaabef548dca0edce6`  
		Last Modified: Tue, 01 Dec 2020 04:00:46 GMT  
		Size: 12.7 MB (12706582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3321b09ca6255e6f5cb4dce9057df675dd4644a3654424c7ee95fbdcb083e9c`  
		Last Modified: Tue, 01 Dec 2020 04:00:42 GMT  
		Size: 2.3 KB (2257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:345450fde280cf49e34f7246cebd38e311d4b7bebe22415a6126c18e67899f91`  
		Last Modified: Tue, 01 Dec 2020 04:00:42 GMT  
		Size: 16.9 KB (16903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:520112c186c5f2a097e8056a524b7c35704923ebeb6247e924ca839fe6e5b343`  
		Last Modified: Tue, 01 Dec 2020 04:31:36 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d98e04775b392470b2f426804979b34d740103414161d9c89f4df0d0b086e51`  
		Last Modified: Tue, 01 Dec 2020 04:31:34 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c074206a89c8b669d116ecf57544d500dcdc5379828bb10e531adf7af19b658a`  
		Last Modified: Tue, 01 Dec 2020 04:31:34 GMT  
		Size: 3.9 MB (3926108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137384dc891a62af154426c4b36cb9192967da61547507bc1b95301727f85c39`  
		Last Modified: Tue, 01 Dec 2020 04:31:34 GMT  
		Size: 1.5 KB (1473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfdcb3be5430d4c822996a4b1f107a12cafae7d60cc6faf1f7a7cdd8dacaab94`  
		Last Modified: Tue, 08 Dec 2020 00:01:41 GMT  
		Size: 570.9 KB (570924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e55c2ae42163732e674f91058ca3617c71403e138adb01dd23c943ad95d6b0`  
		Last Modified: Tue, 08 Dec 2020 00:01:41 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7-standalone` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:b1e09cd04824b43f07df33154a383bc15923451af616eaaae657aca0620d729f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33702279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea6b86a866d797b65cc54d7527a70e1a5e91bf21ecc1ee3fd22b2a2c18d7f6ed`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 07:18:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 22 Oct 2020 07:18:56 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 22 Oct 2020 07:18:59 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 22 Oct 2020 07:19:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 22 Oct 2020 07:19:04 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 22 Oct 2020 07:19:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 07:19:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 07:19:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 22 Oct 2020 07:27:59 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 01 Dec 2020 03:27:01 GMT
ENV PHP_VERSION=7.4.13
# Tue, 01 Dec 2020 03:27:02 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Tue, 01 Dec 2020 03:27:03 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Tue, 01 Dec 2020 03:27:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 01 Dec 2020 03:27:09 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 01 Dec 2020 03:30:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 01 Dec 2020 03:30:42 GMT
COPY multi:afab483600631d4d87fe030871bbb016f1c2b73c0b72609d857bace419af7f5d in /usr/local/bin/ 
# Tue, 01 Dec 2020 03:30:50 GMT
RUN docker-php-ext-enable sodium
# Tue, 01 Dec 2020 03:30:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 01 Dec 2020 03:30:56 GMT
CMD ["php" "-a"]
# Tue, 01 Dec 2020 08:12:36 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Tue, 01 Dec 2020 08:12:37 GMT
STOPSIGNAL SIGINT
# Tue, 01 Dec 2020 08:12:39 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 01 Dec 2020 08:12:40 GMT
WORKDIR /var/www/html
# Tue, 01 Dec 2020 08:13:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Tue, 01 Dec 2020 08:13:23 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Mon, 07 Dec 2020 23:39:52 GMT
ENV ADMINER_VERSION=4.7.8
# Mon, 07 Dec 2020 23:39:53 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Mon, 07 Dec 2020 23:39:54 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Mon, 07 Dec 2020 23:39:56 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Mon, 07 Dec 2020 23:39:57 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Mon, 07 Dec 2020 23:39:58 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Mon, 07 Dec 2020 23:39:58 GMT
USER adminer
# Mon, 07 Dec 2020 23:39:59 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Mon, 07 Dec 2020 23:40:00 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d57dba23203172f8fffd1379aef0307e782178b62dfc684d43c546f7e874ed`  
		Last Modified: Thu, 22 Oct 2020 08:06:21 GMT  
		Size: 1.3 MB (1342784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8414edb0c9c2f7472bb6228bf691a2ddac19ddad7bad789c7cbdc147aded711`  
		Last Modified: Thu, 22 Oct 2020 08:06:20 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d26eeef0db35b2328adae38a8490c7403844452c3606dd17fbe68216f98e82`  
		Last Modified: Thu, 22 Oct 2020 08:06:19 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29be11fa56be3ca1af1498b259f3d5e058a869970cac6d670cf4ca1502485810`  
		Last Modified: Tue, 01 Dec 2020 04:53:56 GMT  
		Size: 10.3 MB (10338597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a553892b0358f6f72064d4dd5e727b686c4461cca7ea8a1211cc86adddb2cb`  
		Last Modified: Tue, 01 Dec 2020 04:53:56 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:828f98d07be67a182899230fc7e38e513de6ce85178d60116c765e90ffbc4119`  
		Last Modified: Tue, 01 Dec 2020 04:54:00 GMT  
		Size: 14.4 MB (14386945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec168016016eef2bef46796f7d7ec48af2459e14d65b9fc2871e756fe3e14d6a`  
		Last Modified: Tue, 01 Dec 2020 04:53:56 GMT  
		Size: 2.3 KB (2260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca32a186f8576115bc6fffe021ff54c52337662fa3cdb51c863d12d20ba02de`  
		Last Modified: Tue, 01 Dec 2020 04:53:55 GMT  
		Size: 17.0 KB (16976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b859cea4a3bb568911dd8f097b1a684daef31726fc5a591b4d9cd57b35187f`  
		Last Modified: Tue, 01 Dec 2020 08:14:59 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e97602a3ba690a845f8ecfaabcff93f82efc85a36445f6413d26f2482987638`  
		Last Modified: Tue, 01 Dec 2020 08:14:56 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6067b9bb9a3850bc39e227d17ab5df99a9bbe61e6d9933fc63c85e464f4aedf5`  
		Last Modified: Tue, 01 Dec 2020 08:14:57 GMT  
		Size: 4.3 MB (4331540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c677bbe386af33259d80d8f4d08a7147fef67adf472b9d841dac1a4a118c7f`  
		Last Modified: Tue, 01 Dec 2020 08:14:57 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4763c08ec3b1c7b68505b48ed92faf18a62525f8ce02d4fba750c232c1826aa9`  
		Last Modified: Mon, 07 Dec 2020 23:40:27 GMT  
		Size: 570.9 KB (570924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:983b1fb60b2afcee1aa424434071184fe8cf507838ac872e30e48755b41f1232`  
		Last Modified: Mon, 07 Dec 2020 23:40:28 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7-standalone` - linux; 386

```console
$ docker pull adminer@sha256:13a4c7ddafd6d4d6a5ee85529f6fa01ebe99d5c5bc1bcafafc85425658693817
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34626966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bb37df3c96977a9c7d5bcff85e2f3904eb30a1d4e2358f0c1644fae769a3ea7`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 22 Oct 2020 02:00:33 GMT
ADD file:46ad43b4984bcf49c5a888ff3628f23161f55cd1fb062f469e707100c97fa254 in / 
# Thu, 22 Oct 2020 02:00:33 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:36:23 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 22 Oct 2020 03:36:26 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 22 Oct 2020 03:36:27 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 22 Oct 2020 03:36:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 22 Oct 2020 03:36:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 22 Oct 2020 03:36:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 03:36:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 03:36:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 22 Oct 2020 03:55:07 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 01 Dec 2020 04:01:21 GMT
ENV PHP_VERSION=7.4.13
# Tue, 01 Dec 2020 04:01:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Tue, 01 Dec 2020 04:01:22 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Tue, 01 Dec 2020 04:01:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 01 Dec 2020 04:01:40 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 01 Dec 2020 04:10:51 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 01 Dec 2020 04:10:52 GMT
COPY multi:afab483600631d4d87fe030871bbb016f1c2b73c0b72609d857bace419af7f5d in /usr/local/bin/ 
# Tue, 01 Dec 2020 04:10:54 GMT
RUN docker-php-ext-enable sodium
# Tue, 01 Dec 2020 04:10:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 01 Dec 2020 04:10:55 GMT
CMD ["php" "-a"]
# Tue, 01 Dec 2020 09:24:38 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Tue, 01 Dec 2020 09:24:38 GMT
STOPSIGNAL SIGINT
# Tue, 01 Dec 2020 09:24:39 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 01 Dec 2020 09:24:39 GMT
WORKDIR /var/www/html
# Tue, 01 Dec 2020 09:25:13 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Tue, 01 Dec 2020 09:25:13 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Mon, 07 Dec 2020 23:38:24 GMT
ENV ADMINER_VERSION=4.7.8
# Mon, 07 Dec 2020 23:38:24 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Mon, 07 Dec 2020 23:38:24 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Mon, 07 Dec 2020 23:38:26 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Mon, 07 Dec 2020 23:38:26 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Mon, 07 Dec 2020 23:38:26 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Mon, 07 Dec 2020 23:38:26 GMT
USER adminer
# Mon, 07 Dec 2020 23:38:26 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Mon, 07 Dec 2020 23:38:27 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:d6ca64ac6f4b6382142ce9a3501652938130a6ec4bb02f3f455ee1f980834cfe`  
		Last Modified: Thu, 22 Oct 2020 02:00:57 GMT  
		Size: 2.8 MB (2791407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30be8ffd290910905a5fb7cbb70252eb0f59edb09db20bdc21f3b65456acc28f`  
		Last Modified: Thu, 22 Oct 2020 05:10:23 GMT  
		Size: 1.4 MB (1439641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d58e2433b13446c863e85b34f8e4c93ca9d5b3b93d2bac415fd9cdf77bcec4`  
		Last Modified: Thu, 22 Oct 2020 05:10:21 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5729dcb8d303f82a7f8cf3df49048e34ce8ee89f79155fb08a475da46b64308`  
		Last Modified: Thu, 22 Oct 2020 05:10:21 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ffdca9b500ff910069fefe63b455206db2cf0fa00dc6b7c7d53219dfaf7f5b`  
		Last Modified: Tue, 01 Dec 2020 07:15:13 GMT  
		Size: 10.3 MB (10338561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c682383cda14fca62843652d7478a26995cfbbfbcb457985de4ca5cfb77de751`  
		Last Modified: Tue, 01 Dec 2020 07:15:12 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57833a53685f649182bdbb4194ba35390c17fa65a6b09c4e377a42a5f9aaca30`  
		Last Modified: Tue, 01 Dec 2020 07:15:18 GMT  
		Size: 14.9 MB (14942640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7003874a29c37e250b24c310b448d1c36607cdb1b43128071780d5fd0a0dc3e1`  
		Last Modified: Tue, 01 Dec 2020 07:15:12 GMT  
		Size: 2.3 KB (2259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fcfab619124f72931608ea142c1cd80a26871e1631380720b6be739170e21b6`  
		Last Modified: Tue, 01 Dec 2020 07:15:12 GMT  
		Size: 16.9 KB (16924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055719a49e04df90bb23499c98da9779637e3b44446a60f202283f57e4b29b04`  
		Last Modified: Tue, 01 Dec 2020 09:26:14 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2b0f52d9f107a35a34b4f8c69abbdf24f2de8a0431c812d74cb6dd3cbf8bf2`  
		Last Modified: Tue, 01 Dec 2020 09:26:13 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4edb5ffb9c3f753b4991debfaeef5c535ae5d689a18b7fff9f0b042c5883865`  
		Last Modified: Tue, 01 Dec 2020 09:26:14 GMT  
		Size: 4.5 MB (4519100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9258866f679eb2cbc89aa311d5d2dad0c146a7e9f61c9e805b63d7f324d2afb0`  
		Last Modified: Tue, 01 Dec 2020 09:26:13 GMT  
		Size: 1.5 KB (1472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:904e3ae5079e7cd06213e6912d4237663cff97a37e1ed247e24b7f455951eafe`  
		Last Modified: Mon, 07 Dec 2020 23:38:45 GMT  
		Size: 570.9 KB (570859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:362b319c8a865e06c57265a80b857954a02a4e09ffe3eda699eede128dcdef90`  
		Last Modified: Mon, 07 Dec 2020 23:38:45 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7-standalone` - linux; ppc64le

```console
$ docker pull adminer@sha256:73feff7b317d1078b173d0c1dc928c14bf61e94b4562a0a79132b9dac74739aa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 MB (35029016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2bacaef82d901426ed9bf50182af16a98e04172b1d2dac51b87db0885487f72`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 22 Oct 2020 11:00:06 GMT
ADD file:176e047fab2c1828575bffa6b14773efa297b7ecf312d86103c5dd4f78ec8027 in / 
# Thu, 22 Oct 2020 11:00:17 GMT
CMD ["/bin/sh"]
# Fri, 23 Oct 2020 00:21:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 23 Oct 2020 00:21:18 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 23 Oct 2020 00:21:30 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 23 Oct 2020 00:21:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 23 Oct 2020 00:21:44 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 23 Oct 2020 00:21:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 23 Oct 2020 00:21:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 23 Oct 2020 00:21:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 23 Oct 2020 00:34:37 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 01 Dec 2020 03:52:39 GMT
ENV PHP_VERSION=7.4.13
# Tue, 01 Dec 2020 03:52:44 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Tue, 01 Dec 2020 03:52:51 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Tue, 01 Dec 2020 03:53:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 01 Dec 2020 03:53:13 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 01 Dec 2020 03:57:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 01 Dec 2020 03:57:24 GMT
COPY multi:afab483600631d4d87fe030871bbb016f1c2b73c0b72609d857bace419af7f5d in /usr/local/bin/ 
# Tue, 01 Dec 2020 03:57:33 GMT
RUN docker-php-ext-enable sodium
# Tue, 01 Dec 2020 03:57:36 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 01 Dec 2020 03:57:39 GMT
CMD ["php" "-a"]
# Tue, 01 Dec 2020 07:09:03 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Tue, 01 Dec 2020 07:09:12 GMT
STOPSIGNAL SIGINT
# Tue, 01 Dec 2020 07:09:25 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 01 Dec 2020 07:09:32 GMT
WORKDIR /var/www/html
# Tue, 01 Dec 2020 07:10:30 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Tue, 01 Dec 2020 07:10:33 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Tue, 08 Dec 2020 00:16:36 GMT
ENV ADMINER_VERSION=4.7.8
# Tue, 08 Dec 2020 00:16:38 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Tue, 08 Dec 2020 00:16:41 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Tue, 08 Dec 2020 00:16:53 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Tue, 08 Dec 2020 00:16:54 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 08 Dec 2020 00:16:58 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Tue, 08 Dec 2020 00:17:11 GMT
USER adminer
# Tue, 08 Dec 2020 00:17:16 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 08 Dec 2020 00:17:18 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:692a9d763e196c85d79fc3e45b316b1bb557c93ba88a3c8ebf679a585d1efe73`  
		Last Modified: Thu, 22 Oct 2020 11:02:06 GMT  
		Size: 2.8 MB (2803218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0285d6f06f3beb1c140c055210664c441b93dd4f2037177a5396bce94ca16ce5`  
		Last Modified: Fri, 23 Oct 2020 01:34:08 GMT  
		Size: 1.4 MB (1383187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a6459a3bf272daa53ff4ba97cc849676f497de9f78d8e9378ec02552293f175`  
		Last Modified: Fri, 23 Oct 2020 01:34:07 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16cff6064dc29d3f629d353736c1cac074caa5b50738422adb84de99a019bb32`  
		Last Modified: Fri, 23 Oct 2020 01:34:08 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0baf560776c5dd75b5673be3d73b900119615cfc4e4fe24414486e3d1f11920`  
		Last Modified: Tue, 01 Dec 2020 05:50:29 GMT  
		Size: 10.3 MB (10338609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4d8083b683ead9a591a00aff14c8d0091665e1433d301a027b214f19cbe23f`  
		Last Modified: Tue, 01 Dec 2020 05:50:29 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7381e6ce3e117510e5a2bf102da48e3cc1b5fd3414651ec324bbe759d367be`  
		Last Modified: Tue, 01 Dec 2020 05:50:32 GMT  
		Size: 15.5 MB (15548036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8328c4e67c6b29f383993d05557e298bc834c18c00961b9ab2a1c4e4eb05b4fd`  
		Last Modified: Tue, 01 Dec 2020 05:50:28 GMT  
		Size: 2.3 KB (2259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:236813d0f57da4fa9c0d5938846f85e82a0a01ce89ca208916b8f649c0ee99fd`  
		Last Modified: Tue, 01 Dec 2020 05:50:28 GMT  
		Size: 17.0 KB (16965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acf7ec6b5baaa9faab722bfc6a7098e0871e3edb42be513e64fe8e06bc7edec1`  
		Last Modified: Tue, 01 Dec 2020 07:14:36 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c17363dc3aab754805ecdc74f39535a73cfc5f3cebe72a4cb18fdc97df1ef9fa`  
		Last Modified: Tue, 01 Dec 2020 07:14:33 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95753fdce29daf55de647d3a29a8cc07941f7bf95fec4a560b0d698478b782f3`  
		Last Modified: Tue, 01 Dec 2020 07:14:34 GMT  
		Size: 4.4 MB (4360119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cad5fcb53526734d41770680ea56047b6e13c767960fc1d0a0b8de7c7030c75`  
		Last Modified: Tue, 01 Dec 2020 07:14:33 GMT  
		Size: 1.5 KB (1474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b231a33566f06d48010343aac194149b1ce1613cf2397c67cf1be2984295f133`  
		Last Modified: Tue, 08 Dec 2020 00:18:38 GMT  
		Size: 570.9 KB (570925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628d0ad1cc992636ad6e5a1f0cf7de70d844c7cccb85cda16205dc67b167e131`  
		Last Modified: Tue, 08 Dec 2020 00:18:38 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.7-standalone` - linux; s390x

```console
$ docker pull adminer@sha256:6b00709e793594a51832541158adeb2ae42e00829dbfb77a54bc0eef7fd1668d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32521955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f75d1bfddd1544fe2cddf65f0baa090dfb992c4a38b43b24670dc3b1ce037d7`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 11 Dec 2020 02:09:52 GMT
ADD file:c9395a36a4e03768aabd282eb1f31705cc00181d3147222d9c940eaa5a8fd511 in / 
# Fri, 11 Dec 2020 02:09:53 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 11:30:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 11 Dec 2020 11:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 11 Dec 2020 11:30:56 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 11 Dec 2020 11:30:57 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 11 Dec 2020 11:30:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 11 Dec 2020 11:30:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Dec 2020 11:31:00 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Dec 2020 11:31:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 11 Dec 2020 12:01:46 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 11 Dec 2020 12:01:46 GMT
ENV PHP_VERSION=7.4.13
# Fri, 11 Dec 2020 12:01:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Fri, 11 Dec 2020 12:01:48 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Fri, 11 Dec 2020 12:01:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 11 Dec 2020 12:01:54 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Dec 2020 12:08:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Dec 2020 12:08:47 GMT
COPY multi:afab483600631d4d87fe030871bbb016f1c2b73c0b72609d857bace419af7f5d in /usr/local/bin/ 
# Fri, 11 Dec 2020 12:08:49 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Dec 2020 12:08:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Dec 2020 12:08:50 GMT
CMD ["php" "-a"]
# Fri, 11 Dec 2020 18:43:30 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 11 Dec 2020 18:43:31 GMT
STOPSIGNAL SIGINT
# Fri, 11 Dec 2020 18:43:33 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 11 Dec 2020 18:43:33 GMT
WORKDIR /var/www/html
# Fri, 11 Dec 2020 18:44:50 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 11 Dec 2020 18:44:50 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 11 Dec 2020 18:44:51 GMT
ENV ADMINER_VERSION=4.7.8
# Fri, 11 Dec 2020 18:44:52 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Fri, 11 Dec 2020 18:44:52 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Fri, 11 Dec 2020 18:44:56 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 11 Dec 2020 18:44:57 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 11 Dec 2020 18:44:57 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 11 Dec 2020 18:44:58 GMT
USER adminer
# Fri, 11 Dec 2020 18:44:59 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 11 Dec 2020 18:44:59 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:7c2470fe3d16cb70fca0826168095a96838b1322a8cd1502b28284ee8561b491`  
		Last Modified: Fri, 11 Dec 2020 02:10:27 GMT  
		Size: 2.6 MB (2565988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a23c8359d30ae261ad953f292e6681a71ebc7388607b74d901bbc07f71e1311`  
		Last Modified: Fri, 11 Dec 2020 13:48:01 GMT  
		Size: 1.4 MB (1382587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01422c3e898d3241d4134256bf0d911b0752823227af04614187c79c187e2843`  
		Last Modified: Fri, 11 Dec 2020 13:48:03 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a0be2077abd44f96e50bdebb1ed93a6e2b8d504761c23fa0e5e9b87045ca38`  
		Last Modified: Fri, 11 Dec 2020 13:48:01 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267bafe0bb23009994a23ad5cdcc3b4d425f186f0e488b5f7461463ad1b53814`  
		Last Modified: Fri, 11 Dec 2020 13:50:24 GMT  
		Size: 10.3 MB (10338590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36304b0fbddac7ce44edacaedb902676688cfc3bb7082576f6b57eed0ccc133e`  
		Last Modified: Fri, 11 Dec 2020 13:50:25 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fa33489075ff6318ffc5a7cf5c94cb4ce65ccfc82b5970cc91628780c130aae`  
		Last Modified: Fri, 11 Dec 2020 13:50:26 GMT  
		Size: 13.5 MB (13485898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155ae451461e50390ae0db27a78a329e87a86b9f9eb04f6db81fcc27430f2d51`  
		Last Modified: Fri, 11 Dec 2020 13:50:24 GMT  
		Size: 2.3 KB (2257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b379111cc7023c652243c4d9234de47984fa307030d667bf14e5d12889ec8180`  
		Last Modified: Fri, 11 Dec 2020 13:50:24 GMT  
		Size: 16.9 KB (16879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a18e16d8efd7f249149e2d38813d86590cc4a55f23d8c5bbba970725422ea51`  
		Last Modified: Fri, 11 Dec 2020 18:47:13 GMT  
		Size: 310.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ba44137233477a93edb1e0cc94bee3ce4dafaed9ff932d21594190f861ef75`  
		Last Modified: Fri, 11 Dec 2020 18:47:13 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cba732448866bbb0e567b7510578f951e9cf0bc258588c8e898be1606e3a3eb`  
		Last Modified: Fri, 11 Dec 2020 18:47:11 GMT  
		Size: 4.2 MB (4153155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8faf5f39c5d146bc658625977adca6ce417bb45b9683bb1767b99abfea6d3d56`  
		Last Modified: Fri, 11 Dec 2020 18:47:11 GMT  
		Size: 1.5 KB (1473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008d2a285f2f6bcf687be0cb08b167a975a4d7534a16435da10ba2b75b2e2d73`  
		Last Modified: Fri, 11 Dec 2020 18:47:11 GMT  
		Size: 570.9 KB (570918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6852608d1b2324d98a56de31e6fc11ac1fe8e95f605b50c9f72db2bd5cd092`  
		Last Modified: Fri, 11 Dec 2020 18:47:12 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:4-fastcgi`

```console
$ docker pull adminer@sha256:c0bcea38afeb9296d883e7371a4b83a97384f02ed2d2c3e71a6823267d6f0bac
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

### `adminer:4-fastcgi` - linux; amd64

```console
$ docker pull adminer@sha256:fb2f45c8e550ba3d59351c5ab1ac746adcab7dfb5e2d0b2a27531d2b664f598b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (34042656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff0774240cbda9b72e1940dc60ecd8366d3b4df4e789a7284078c8698364477`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 06:30:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 22 Oct 2020 06:30:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 22 Oct 2020 06:30:15 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 22 Oct 2020 06:30:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 22 Oct 2020 06:30:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 22 Oct 2020 06:37:19 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Thu, 22 Oct 2020 06:37:19 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 06:37:19 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 06:37:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 22 Oct 2020 06:49:00 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 01 Dec 2020 04:45:15 GMT
ENV PHP_VERSION=7.4.13
# Tue, 01 Dec 2020 04:45:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Tue, 01 Dec 2020 04:45:15 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Tue, 01 Dec 2020 04:45:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 01 Dec 2020 04:45:21 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 01 Dec 2020 04:54:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 01 Dec 2020 04:54:04 GMT
COPY multi:ebc915bbde1078ce3122b918e2e4c7726858af785343ade1a8d1a94f1052a4c7 in /usr/local/bin/ 
# Tue, 01 Dec 2020 04:54:07 GMT
RUN docker-php-ext-enable sodium
# Tue, 01 Dec 2020 04:54:07 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 01 Dec 2020 04:54:08 GMT
WORKDIR /var/www/html
# Tue, 01 Dec 2020 04:54:09 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Tue, 01 Dec 2020 04:54:10 GMT
STOPSIGNAL SIGQUIT
# Tue, 01 Dec 2020 04:54:10 GMT
EXPOSE 9000
# Tue, 01 Dec 2020 04:54:11 GMT
CMD ["php-fpm"]
# Tue, 01 Dec 2020 07:47:26 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Tue, 01 Dec 2020 07:47:28 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 01 Dec 2020 07:48:01 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Tue, 01 Dec 2020 07:48:01 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Tue, 08 Dec 2020 00:19:31 GMT
ENV ADMINER_VERSION=4.7.8
# Tue, 08 Dec 2020 00:19:31 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Tue, 08 Dec 2020 00:19:31 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Tue, 08 Dec 2020 00:19:33 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Tue, 08 Dec 2020 00:19:33 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 08 Dec 2020 00:19:33 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Tue, 08 Dec 2020 00:19:33 GMT
USER adminer
# Tue, 08 Dec 2020 00:19:33 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f8bf6cfdbe614fef94f982905079c16e27b3de2d24eb1ff513d3d83e656ca2`  
		Last Modified: Thu, 22 Oct 2020 07:36:55 GMT  
		Size: 1.3 MB (1340771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce5be79740125b9e74a77885bf6ee2b0d25ac7ed9e9432c5aa7210bb3b00458a`  
		Last Modified: Thu, 22 Oct 2020 07:36:55 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99dd6507fe563b66ba35badf706e1bbb2d39eb5d0a3c0d5a86a45d2af7e89c1`  
		Last Modified: Thu, 22 Oct 2020 07:36:55 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c3b45daa37929dd9a002107adb1299c5b070bbba60b73cf9ecc2d9fd6e78f9`  
		Last Modified: Tue, 01 Dec 2020 07:27:28 GMT  
		Size: 10.3 MB (10338571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6afb095daafcd5f742a42ee6dbf8f6d03fdca63c22071198f243df20ecef1db9`  
		Last Modified: Tue, 01 Dec 2020 07:27:25 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838cecfde999e9ecf65003522df2ce13e12fa5190e2336ffb1d16da9a787ead4`  
		Last Modified: Tue, 01 Dec 2020 07:27:29 GMT  
		Size: 14.6 MB (14640876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a46b7ab0f2d19433340bdeca3307275efd3188c446a3c739c1196c9bd05a0e`  
		Last Modified: Tue, 01 Dec 2020 07:27:26 GMT  
		Size: 2.3 KB (2255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d2139a9b9d18bdd892644fe463b368727e54ba53b145694a26f4cfe3f8e61d1`  
		Last Modified: Tue, 01 Dec 2020 07:27:26 GMT  
		Size: 17.0 KB (16987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f68d34619f5f9cff2cfac13cfa06e31e832bf261751b75ee11561cd3375e0207`  
		Last Modified: Tue, 01 Dec 2020 07:27:26 GMT  
		Size: 8.4 KB (8446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6bf2c8a87f5c9551aa94f68cd8ea11b9fb2f222d8cd8cdaf96b58fe86c98897`  
		Last Modified: Tue, 01 Dec 2020 07:48:39 GMT  
		Size: 310.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f16b55f73f8f895e7f07bc76cbc0c40ed52e4032e2129a9dbf41c7cb907c9e`  
		Last Modified: Tue, 01 Dec 2020 07:48:37 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a4fbbf03b1e145da6329a1d517b4ddaafee96bc3623a9dea8fcf2d3b1309ce4`  
		Last Modified: Tue, 01 Dec 2020 07:48:38 GMT  
		Size: 4.3 MB (4321450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b75ee2a57910d59b9ac6cb6de554264966343ef9391893d44eaf344ebca1bdc`  
		Last Modified: Tue, 01 Dec 2020 07:48:38 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12530476c9fea755fef449d62308ae3022da470522b4598087fcd3eb5bf68f7d`  
		Last Modified: Tue, 08 Dec 2020 00:19:56 GMT  
		Size: 570.9 KB (570859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5723a03bb2a4c99d35468a1f3e68d687f33c81fdce68c56aac53b1c689b5542`  
		Last Modified: Tue, 08 Dec 2020 00:19:55 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; arm variant v6

```console
$ docker pull adminer@sha256:689204154221d2e4a097c834af056b991f880aed7a5a4a1e54d6c4422d965a6f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32149046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bb1805eba8cd29a4f28de65c3c539bac32ead0206c065984c55d1a699fd3b81`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 11 Dec 2020 02:17:15 GMT
ADD file:1a9c0a67560d338c0c0e7005d8915d998fc9cf3e9f53bfd7e42e8391f0a39bce in / 
# Fri, 11 Dec 2020 02:17:15 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 07:04:50 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 11 Dec 2020 07:04:53 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 11 Dec 2020 07:04:55 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 11 Dec 2020 07:04:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 11 Dec 2020 07:04:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 11 Dec 2020 07:09:12 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Fri, 11 Dec 2020 07:09:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Dec 2020 07:09:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Dec 2020 07:09:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 11 Dec 2020 07:17:56 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 11 Dec 2020 07:17:57 GMT
ENV PHP_VERSION=7.4.13
# Fri, 11 Dec 2020 07:17:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Fri, 11 Dec 2020 07:17:58 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Fri, 11 Dec 2020 07:18:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 11 Dec 2020 07:18:05 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Dec 2020 07:21:46 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Dec 2020 07:21:47 GMT
COPY multi:ebc915bbde1078ce3122b918e2e4c7726858af785343ade1a8d1a94f1052a4c7 in /usr/local/bin/ 
# Fri, 11 Dec 2020 07:21:51 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Dec 2020 07:21:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Dec 2020 07:21:53 GMT
WORKDIR /var/www/html
# Fri, 11 Dec 2020 07:21:56 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 11 Dec 2020 07:21:57 GMT
STOPSIGNAL SIGQUIT
# Fri, 11 Dec 2020 07:21:58 GMT
EXPOSE 9000
# Fri, 11 Dec 2020 07:21:59 GMT
CMD ["php-fpm"]
# Fri, 11 Dec 2020 09:05:35 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 11 Dec 2020 09:05:38 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 11 Dec 2020 09:06:36 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 11 Dec 2020 09:06:37 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 11 Dec 2020 09:06:38 GMT
ENV ADMINER_VERSION=4.7.8
# Fri, 11 Dec 2020 09:06:40 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Fri, 11 Dec 2020 09:06:41 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Fri, 11 Dec 2020 09:06:45 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 11 Dec 2020 09:06:46 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 11 Dec 2020 09:06:48 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 11 Dec 2020 09:06:50 GMT
USER adminer
# Fri, 11 Dec 2020 09:06:52 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:f1c16df8fee33d421d08790b17ca2af67a3fe49e77b6b991dd0c30631f5d1baf`  
		Last Modified: Fri, 11 Dec 2020 02:17:57 GMT  
		Size: 2.6 MB (2601992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623cc08cbe035cf15859e57a83e2243620418da06e1905d1875a46bec901e540`  
		Last Modified: Fri, 11 Dec 2020 07:56:49 GMT  
		Size: 1.3 MB (1310156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3a7aacff9b7ccf646f2bdbbc8d40bbb304550e813876049e721abd35461df9`  
		Last Modified: Fri, 11 Dec 2020 07:56:49 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d3214ea6f418597f370177309be7728f94481030c9cba6e45c4b74cfd04cc0`  
		Last Modified: Fri, 11 Dec 2020 07:56:49 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dff7159949c3c97335dda12e61ad77a87a4125ef93f88655500f4b8057cd38ca`  
		Last Modified: Fri, 11 Dec 2020 07:58:09 GMT  
		Size: 10.3 MB (10338600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c2c2f22a036ec3f2efaed4fd97c10faee4bbf539b56bf2e11b84a7c05b78fa`  
		Last Modified: Fri, 11 Dec 2020 07:58:05 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae33a5a224fa1ee298562bc31d50c9f804652bf619e4836e852c8860c5c49318`  
		Last Modified: Fri, 11 Dec 2020 07:58:09 GMT  
		Size: 13.3 MB (13267849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53c09a76a513338db42015101706a8bf9c7309d298d0a3329dee74810ea39db7`  
		Last Modified: Fri, 11 Dec 2020 07:58:05 GMT  
		Size: 2.3 KB (2260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e47c9c32a85f1170c19a3745c3a661a3a3c13e50daddef9919f624a52a70bc30`  
		Last Modified: Fri, 11 Dec 2020 07:58:05 GMT  
		Size: 16.9 KB (16891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbe39bbdfd22c5c467c010b89eb9561741273f56a2f378e08f2e055ef9ed919`  
		Last Modified: Fri, 11 Dec 2020 07:58:05 GMT  
		Size: 8.4 KB (8446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb3c1470d540138d5b667c3d6e30a34a3b783541ba0dc69a9714fa432a923970`  
		Last Modified: Fri, 11 Dec 2020 09:07:48 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f70879cf7eb8183ab6f68ad5f05f07b3e91a88ca27f7d935e91892073b1376`  
		Last Modified: Fri, 11 Dec 2020 09:07:46 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f69f96ec941427956045eb3c5673c21715d1878daf9035b7d11122c8cf62ed0c`  
		Last Modified: Fri, 11 Dec 2020 09:07:46 GMT  
		Size: 4.0 MB (4026251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a629622e0e5f22c28c625e3b6a9bef5d2136d403a64f88e8a44b1f1088caec2d`  
		Last Modified: Fri, 11 Dec 2020 09:07:45 GMT  
		Size: 1.5 KB (1470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec25251b0aa5ef178648ab40613c0031a55f133641f36b6c6e74dc5e79e4764`  
		Last Modified: Fri, 11 Dec 2020 09:07:46 GMT  
		Size: 570.9 KB (570918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71d17d806f1955405b240a9ef740c540c9e8ec5ceb8686ec081fda180677e50c`  
		Last Modified: Fri, 11 Dec 2020 09:07:45 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; arm variant v7

```console
$ docker pull adminer@sha256:226eabf37d80fa4c86dc5fd621ba0b5c211967752c3e972a3929b9ffc4f4387c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31261925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efcd4d51f3642b6795c4c7140eaab8183af5f3b781a9099b95e1eba7d94d5683`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 22 Oct 2020 01:58:13 GMT
ADD file:46f89172426e9f5b1d669a2ca7ab218fc2deaef1caeeab88f2b5bd443ac9773d in / 
# Thu, 22 Oct 2020 01:58:14 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 06:47:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 22 Oct 2020 06:47:37 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 22 Oct 2020 06:47:45 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 22 Oct 2020 06:47:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 22 Oct 2020 06:47:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 22 Oct 2020 06:51:33 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Thu, 22 Oct 2020 06:51:36 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 06:51:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 06:51:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 22 Oct 2020 07:01:44 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 01 Dec 2020 02:43:04 GMT
ENV PHP_VERSION=7.4.13
# Tue, 01 Dec 2020 02:43:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Tue, 01 Dec 2020 02:43:24 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Tue, 01 Dec 2020 02:43:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 01 Dec 2020 02:43:39 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 01 Dec 2020 02:46:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 01 Dec 2020 02:46:34 GMT
COPY multi:ebc915bbde1078ce3122b918e2e4c7726858af785343ade1a8d1a94f1052a4c7 in /usr/local/bin/ 
# Tue, 01 Dec 2020 02:46:37 GMT
RUN docker-php-ext-enable sodium
# Tue, 01 Dec 2020 02:46:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 01 Dec 2020 02:46:39 GMT
WORKDIR /var/www/html
# Tue, 01 Dec 2020 02:46:42 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Tue, 01 Dec 2020 02:46:44 GMT
STOPSIGNAL SIGQUIT
# Tue, 01 Dec 2020 02:46:45 GMT
EXPOSE 9000
# Tue, 01 Dec 2020 02:46:46 GMT
CMD ["php-fpm"]
# Tue, 01 Dec 2020 04:29:50 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Tue, 01 Dec 2020 04:29:56 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 01 Dec 2020 04:30:45 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Tue, 01 Dec 2020 04:30:48 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Tue, 08 Dec 2020 00:01:12 GMT
ENV ADMINER_VERSION=4.7.8
# Tue, 08 Dec 2020 00:01:13 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Tue, 08 Dec 2020 00:01:14 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Tue, 08 Dec 2020 00:01:18 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Tue, 08 Dec 2020 00:01:20 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 08 Dec 2020 00:01:24 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Tue, 08 Dec 2020 00:01:25 GMT
USER adminer
# Tue, 08 Dec 2020 00:01:26 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:5f2023fd85a4e68f37fe41421fd89f30e69b98a645613521c57c01317561eee3`  
		Last Modified: Thu, 22 Oct 2020 01:58:45 GMT  
		Size: 2.4 MB (2405675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60b50c98f8a8e2c6a27378dfa0f44df1844ac67c6981303675f138a42679f25`  
		Last Modified: Thu, 22 Oct 2020 07:35:57 GMT  
		Size: 1.2 MB (1214265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b472094d673b7c272085505c976192b9aaafa3157c99bade9755fbca18a24071`  
		Last Modified: Thu, 22 Oct 2020 07:35:56 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc39e5d916c11e7eb158e72d14ab981eb45ccc7b6451c1d6d3cb627b71cdbb6`  
		Last Modified: Thu, 22 Oct 2020 07:35:55 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad5979536683af238cd5c6e9e7ee5171a2f468ba42667525bcf73dfbd4442d5c`  
		Last Modified: Tue, 01 Dec 2020 04:01:12 GMT  
		Size: 10.3 MB (10338579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83bfa48b04ad972c7ddc62f60703fd345236339c894ee5e02487d0a6912eec44`  
		Last Modified: Tue, 01 Dec 2020 04:01:08 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d500723729ab98b41c43300141cf87ecedf3122e848cb7f2871a8a18b472c9`  
		Last Modified: Tue, 01 Dec 2020 04:01:12 GMT  
		Size: 12.8 MB (12773054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ffe3faddffbb23fc7ec2b0ac5897aa6700b295f1129a52a58322108a7d7146`  
		Last Modified: Tue, 01 Dec 2020 04:01:08 GMT  
		Size: 2.3 KB (2260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c6599d32683be6cd2106e34a046a0a556bffd2baac97299eb69df7408f682be`  
		Last Modified: Tue, 01 Dec 2020 04:01:08 GMT  
		Size: 16.9 KB (16903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7158f5b17b11ddb8f243be54e5fc6112f6017d46780577a568a72e2e7d3f2cb1`  
		Last Modified: Tue, 01 Dec 2020 04:01:08 GMT  
		Size: 8.4 KB (8446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba8645bc546fe074d817500743f03a6b6b287793cee19306e5267095e410e7e`  
		Last Modified: Tue, 01 Dec 2020 04:32:00 GMT  
		Size: 310.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae84262bbd09928c80ab09696b0c7d2d57c5b58e28e089d2be9aae62bd0c7d0e`  
		Last Modified: Tue, 01 Dec 2020 04:31:59 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d45b8aa81cac48a3b6f2953fa3ad9d6047d134f7b76cbb3e05cbde0d6e0c7fc1`  
		Last Modified: Tue, 01 Dec 2020 04:31:59 GMT  
		Size: 3.9 MB (3926120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b483e9859bacb3a5557c81eda83e17a2559203c0979dcdd57bdcbe5729404c0f`  
		Last Modified: Tue, 01 Dec 2020 04:31:58 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7022a91847b0aaf7d1e067b9c3fa7620f93f349b64d2d7ebe0e816598a47fed2`  
		Last Modified: Tue, 08 Dec 2020 00:01:58 GMT  
		Size: 570.9 KB (570923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562e2ad43a7b07e5427acd85e75ec18c9dc4b21fe0a10fac08b447cfa140187f`  
		Last Modified: Tue, 08 Dec 2020 00:01:58 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:89498585a4df7bcfaecdaadf8bee7b0b21018e861c1357c5826273c129cea8c1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.8 MB (33782483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57bc4d4eb9fffe27cb455d6f0c04677fd0798704e2673ac9c281b492fa593f03`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 07:18:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 22 Oct 2020 07:18:56 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 22 Oct 2020 07:18:59 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 22 Oct 2020 07:19:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 22 Oct 2020 07:19:04 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 22 Oct 2020 07:23:16 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Thu, 22 Oct 2020 07:23:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 07:23:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 07:23:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 22 Oct 2020 07:32:38 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 01 Dec 2020 03:31:07 GMT
ENV PHP_VERSION=7.4.13
# Tue, 01 Dec 2020 03:31:08 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Tue, 01 Dec 2020 03:31:09 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Tue, 01 Dec 2020 03:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 01 Dec 2020 03:31:15 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 01 Dec 2020 03:34:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 01 Dec 2020 03:35:01 GMT
COPY multi:ebc915bbde1078ce3122b918e2e4c7726858af785343ade1a8d1a94f1052a4c7 in /usr/local/bin/ 
# Tue, 01 Dec 2020 03:35:06 GMT
RUN docker-php-ext-enable sodium
# Tue, 01 Dec 2020 03:35:06 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 01 Dec 2020 03:35:08 GMT
WORKDIR /var/www/html
# Tue, 01 Dec 2020 03:35:10 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Tue, 01 Dec 2020 03:35:11 GMT
STOPSIGNAL SIGQUIT
# Tue, 01 Dec 2020 03:35:12 GMT
EXPOSE 9000
# Tue, 01 Dec 2020 03:35:13 GMT
CMD ["php-fpm"]
# Tue, 01 Dec 2020 08:13:43 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Tue, 01 Dec 2020 08:13:46 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 01 Dec 2020 08:14:29 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Tue, 01 Dec 2020 08:14:30 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Mon, 07 Dec 2020 23:40:07 GMT
ENV ADMINER_VERSION=4.7.8
# Mon, 07 Dec 2020 23:40:07 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Mon, 07 Dec 2020 23:40:08 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Mon, 07 Dec 2020 23:40:11 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Mon, 07 Dec 2020 23:40:12 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Mon, 07 Dec 2020 23:40:13 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Mon, 07 Dec 2020 23:40:14 GMT
USER adminer
# Mon, 07 Dec 2020 23:40:15 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d57dba23203172f8fffd1379aef0307e782178b62dfc684d43c546f7e874ed`  
		Last Modified: Thu, 22 Oct 2020 08:06:21 GMT  
		Size: 1.3 MB (1342784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8414edb0c9c2f7472bb6228bf691a2ddac19ddad7bad789c7cbdc147aded711`  
		Last Modified: Thu, 22 Oct 2020 08:06:20 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d26eeef0db35b2328adae38a8490c7403844452c3606dd17fbe68216f98e82`  
		Last Modified: Thu, 22 Oct 2020 08:06:19 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b747a72bda51ef2a52afed0eef10b56786e7c76ab30913f0e650a83b66935e4f`  
		Last Modified: Tue, 01 Dec 2020 04:54:24 GMT  
		Size: 10.3 MB (10338600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c684293922e5efaae5d67a6b158f6e54284e91081dda97b306a74ce97c9d0738`  
		Last Modified: Tue, 01 Dec 2020 04:54:21 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acdf0cad2cf9d86164e334858db58328dc251f08abe9d0841cc1bf520748163e`  
		Last Modified: Tue, 01 Dec 2020 04:54:25 GMT  
		Size: 14.5 MB (14458713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3417ec8fcb1bd4b4d3f295b89316912d8e33667e645450c3d0a2694887fea5da`  
		Last Modified: Tue, 01 Dec 2020 04:54:21 GMT  
		Size: 2.3 KB (2256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96e2c572c8bf97a5e221afc68cec20acaad7e29b919f242c6cb085234693b08`  
		Last Modified: Tue, 01 Dec 2020 04:54:22 GMT  
		Size: 17.0 KB (16978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:732bd773818e9fef29ad5ba55c5ddd1638077be22b0fd0a8f3a8bee4b600da11`  
		Last Modified: Tue, 01 Dec 2020 04:54:21 GMT  
		Size: 8.4 KB (8444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1886aa9fc4a1ad175dc4689b2f38537f04a005774f1c34b08ae3b8c3158fe5f8`  
		Last Modified: Tue, 01 Dec 2020 08:15:16 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf4e7f82086c970c52f8f544137e3286e990df9f19ad8567bba476226b12f61`  
		Last Modified: Tue, 01 Dec 2020 08:15:15 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4acc32056dfd0cd70bbc78cdfb34f2c627a433caff773366ad168a4945db066`  
		Last Modified: Tue, 01 Dec 2020 08:15:15 GMT  
		Size: 4.3 MB (4331531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb34a16b4bdb5625d39f3ef20da17bfecf2156cf9f3a647b4c4c26497af56b7`  
		Last Modified: Tue, 01 Dec 2020 08:15:15 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857d9231bfb81ba8cc071fbdcccdb6f9189f8e56d09ce9396b85b4e88b412b53`  
		Last Modified: Mon, 07 Dec 2020 23:40:43 GMT  
		Size: 570.9 KB (570920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a854be7b56f0667067e2d5d43ed47f9f068cb0e3f7976910fb604dda911121db`  
		Last Modified: Mon, 07 Dec 2020 23:40:43 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; 386

```console
$ docker pull adminer@sha256:4f5fe39f0929ce4ac634729677768b268b328437e602e5a286881bb683086a5f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34705084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c8aa440257abba5e8b17a4be7767c0c3b8fc17f455e445f561495f8d394f849`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 22 Oct 2020 02:00:33 GMT
ADD file:46ad43b4984bcf49c5a888ff3628f23161f55cd1fb062f469e707100c97fa254 in / 
# Thu, 22 Oct 2020 02:00:33 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:36:23 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 22 Oct 2020 03:36:26 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 22 Oct 2020 03:36:27 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 22 Oct 2020 03:36:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 22 Oct 2020 03:36:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 22 Oct 2020 03:45:17 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Thu, 22 Oct 2020 03:45:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 03:45:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 03:45:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 22 Oct 2020 04:01:27 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 01 Dec 2020 04:11:03 GMT
ENV PHP_VERSION=7.4.13
# Tue, 01 Dec 2020 04:11:04 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Tue, 01 Dec 2020 04:11:04 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Tue, 01 Dec 2020 04:11:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 01 Dec 2020 04:11:13 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 01 Dec 2020 04:19:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 01 Dec 2020 04:19:54 GMT
COPY multi:ebc915bbde1078ce3122b918e2e4c7726858af785343ade1a8d1a94f1052a4c7 in /usr/local/bin/ 
# Tue, 01 Dec 2020 04:19:56 GMT
RUN docker-php-ext-enable sodium
# Tue, 01 Dec 2020 04:19:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 01 Dec 2020 04:19:56 GMT
WORKDIR /var/www/html
# Tue, 01 Dec 2020 04:19:57 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Tue, 01 Dec 2020 04:19:57 GMT
STOPSIGNAL SIGQUIT
# Tue, 01 Dec 2020 04:19:58 GMT
EXPOSE 9000
# Tue, 01 Dec 2020 04:19:58 GMT
CMD ["php-fpm"]
# Tue, 01 Dec 2020 09:25:25 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Tue, 01 Dec 2020 09:25:26 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 01 Dec 2020 09:25:53 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Tue, 01 Dec 2020 09:25:54 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Mon, 07 Dec 2020 23:38:31 GMT
ENV ADMINER_VERSION=4.7.8
# Mon, 07 Dec 2020 23:38:32 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Mon, 07 Dec 2020 23:38:32 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Mon, 07 Dec 2020 23:38:33 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Mon, 07 Dec 2020 23:38:33 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Mon, 07 Dec 2020 23:38:33 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Mon, 07 Dec 2020 23:38:34 GMT
USER adminer
# Mon, 07 Dec 2020 23:38:34 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:d6ca64ac6f4b6382142ce9a3501652938130a6ec4bb02f3f455ee1f980834cfe`  
		Last Modified: Thu, 22 Oct 2020 02:00:57 GMT  
		Size: 2.8 MB (2791407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30be8ffd290910905a5fb7cbb70252eb0f59edb09db20bdc21f3b65456acc28f`  
		Last Modified: Thu, 22 Oct 2020 05:10:23 GMT  
		Size: 1.4 MB (1439641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d58e2433b13446c863e85b34f8e4c93ca9d5b3b93d2bac415fd9cdf77bcec4`  
		Last Modified: Thu, 22 Oct 2020 05:10:21 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5729dcb8d303f82a7f8cf3df49048e34ce8ee89f79155fb08a475da46b64308`  
		Last Modified: Thu, 22 Oct 2020 05:10:21 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73c975f14cba63719b1acf30eb48c56e9ff5ab3ba3c93cc300551ed40f30ac4`  
		Last Modified: Tue, 01 Dec 2020 07:15:32 GMT  
		Size: 10.3 MB (10338565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8926789263a06364cefc6d6aee50b84a30291d014d2029ca669cb556f4c2bb1`  
		Last Modified: Tue, 01 Dec 2020 07:15:30 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcbe8e9cc07ddaae06ed92974d6d0a5249cac41ebb54331b56fc5c9e240eb993`  
		Last Modified: Tue, 01 Dec 2020 07:15:35 GMT  
		Size: 15.0 MB (15012323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e40c7a669cd74ab9dc3e2874416646f823f63c10d9b9a952a55dc1ad5bac9d`  
		Last Modified: Tue, 01 Dec 2020 07:15:30 GMT  
		Size: 2.3 KB (2260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed001fb8127577a70da6914dcf10ccb5d90ed9cf2a1cd3272618748f6b111d03`  
		Last Modified: Tue, 01 Dec 2020 07:15:29 GMT  
		Size: 16.9 KB (16920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90867a60ecf180a61e2ada4f0842adc2c2e44685c28753a5bed45de997db01e7`  
		Last Modified: Tue, 01 Dec 2020 07:15:29 GMT  
		Size: 8.4 KB (8442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3ce5df361365526e71aaf6df13804b7dedc099dd67740782cc739e0613eb110`  
		Last Modified: Tue, 01 Dec 2020 09:26:27 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a789bbdaebdf4bde2f5038d3a2a626522e4b2edc239b954288d23175ee69042`  
		Last Modified: Tue, 01 Dec 2020 09:26:26 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a79d0d02c93a44d0f6d1145f6ae0a0333e71fe94bfa8c63bd24354761d9587`  
		Last Modified: Tue, 01 Dec 2020 09:26:27 GMT  
		Size: 4.5 MB (4519093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85c74143366ffd582b27ed81dd1f35e4e314799a0de720b613b98b88ce787c77`  
		Last Modified: Tue, 01 Dec 2020 09:26:25 GMT  
		Size: 1.5 KB (1472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3529b652f01c65456c39d33fd9d239949548a0442b8a1fa9d2bf0a1c1f74b968`  
		Last Modified: Mon, 07 Dec 2020 23:38:54 GMT  
		Size: 570.9 KB (570861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a79e9613d8243f31a29bb14c13abf1a73d577720e86547b01bdef2bf8f9296bd`  
		Last Modified: Mon, 07 Dec 2020 23:38:54 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; ppc64le

```console
$ docker pull adminer@sha256:0671ac686df177a55af6924323ebcc05a17cb4bf61a6372df21a1a0c22487346
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.1 MB (35117996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:959c6c5b577d14c45504ecdd9a75e110b1afb1e5e8651a224075e4784c97c07c`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 22 Oct 2020 11:00:06 GMT
ADD file:176e047fab2c1828575bffa6b14773efa297b7ecf312d86103c5dd4f78ec8027 in / 
# Thu, 22 Oct 2020 11:00:17 GMT
CMD ["/bin/sh"]
# Fri, 23 Oct 2020 00:21:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 23 Oct 2020 00:21:18 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 23 Oct 2020 00:21:30 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 23 Oct 2020 00:21:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 23 Oct 2020 00:21:44 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 23 Oct 2020 00:27:50 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Fri, 23 Oct 2020 00:27:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 23 Oct 2020 00:28:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 23 Oct 2020 00:28:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 23 Oct 2020 00:39:53 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 01 Dec 2020 03:57:52 GMT
ENV PHP_VERSION=7.4.13
# Tue, 01 Dec 2020 03:57:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Tue, 01 Dec 2020 03:58:02 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Tue, 01 Dec 2020 03:58:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 01 Dec 2020 03:58:37 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 01 Dec 2020 04:02:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 01 Dec 2020 04:02:41 GMT
COPY multi:ebc915bbde1078ce3122b918e2e4c7726858af785343ade1a8d1a94f1052a4c7 in /usr/local/bin/ 
# Tue, 01 Dec 2020 04:02:55 GMT
RUN docker-php-ext-enable sodium
# Tue, 01 Dec 2020 04:02:59 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 01 Dec 2020 04:03:05 GMT
WORKDIR /var/www/html
# Tue, 01 Dec 2020 04:03:27 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Tue, 01 Dec 2020 04:03:33 GMT
STOPSIGNAL SIGQUIT
# Tue, 01 Dec 2020 04:03:40 GMT
EXPOSE 9000
# Tue, 01 Dec 2020 04:03:44 GMT
CMD ["php-fpm"]
# Tue, 01 Dec 2020 07:11:43 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Tue, 01 Dec 2020 07:11:59 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 01 Dec 2020 07:12:55 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Tue, 01 Dec 2020 07:12:59 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Tue, 08 Dec 2020 00:17:37 GMT
ENV ADMINER_VERSION=4.7.8
# Tue, 08 Dec 2020 00:17:44 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Tue, 08 Dec 2020 00:17:47 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Tue, 08 Dec 2020 00:17:56 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Tue, 08 Dec 2020 00:17:59 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 08 Dec 2020 00:18:03 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Tue, 08 Dec 2020 00:18:08 GMT
USER adminer
# Tue, 08 Dec 2020 00:18:15 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:692a9d763e196c85d79fc3e45b316b1bb557c93ba88a3c8ebf679a585d1efe73`  
		Last Modified: Thu, 22 Oct 2020 11:02:06 GMT  
		Size: 2.8 MB (2803218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0285d6f06f3beb1c140c055210664c441b93dd4f2037177a5396bce94ca16ce5`  
		Last Modified: Fri, 23 Oct 2020 01:34:08 GMT  
		Size: 1.4 MB (1383187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a6459a3bf272daa53ff4ba97cc849676f497de9f78d8e9378ec02552293f175`  
		Last Modified: Fri, 23 Oct 2020 01:34:07 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16cff6064dc29d3f629d353736c1cac074caa5b50738422adb84de99a019bb32`  
		Last Modified: Fri, 23 Oct 2020 01:34:08 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67dcc2a717f8153769df04bd895be154aca7c3fc20560f37da5b36e0fbd9efbd`  
		Last Modified: Tue, 01 Dec 2020 05:51:15 GMT  
		Size: 10.3 MB (10338603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9502fa9f26f9855ddcfd4309edb7c16ce7517f1c88a60155b169e6182acbdd17`  
		Last Modified: Tue, 01 Dec 2020 05:51:09 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf065529921adbb64e6889d9cfa225de7f8aa65204f3ec400330d4fc989de4d8`  
		Last Modified: Tue, 01 Dec 2020 05:51:13 GMT  
		Size: 15.6 MB (15628567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e91de5593ec1aa89d021215583d63f94d4f36d9608f29dd460ede4c7290ebb7`  
		Last Modified: Tue, 01 Dec 2020 05:51:09 GMT  
		Size: 2.3 KB (2255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede5b0209a637a8111ae77c919a561733c6e703c97333ecea99a4abbecf8a2c5`  
		Last Modified: Tue, 01 Dec 2020 05:51:09 GMT  
		Size: 17.0 KB (16968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e851350ac3fff1de99c14298cb35f46c409629186a85f22c22a0be19f4f7cd`  
		Last Modified: Tue, 01 Dec 2020 05:51:09 GMT  
		Size: 8.4 KB (8441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df2bf3b8e2936ee1044358dfd1700fce3f08592b60bac9086d1d4677f3de8ca9`  
		Last Modified: Tue, 01 Dec 2020 07:15:16 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bcb7b3aa24f4c386111b1860808ec662939186fbbf6ea9be1a4309880e34a17`  
		Last Modified: Tue, 01 Dec 2020 07:15:13 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:088e76bc30b441c5832343aa548abe6c770bd754156485a0b235f1cf92cac64e`  
		Last Modified: Tue, 01 Dec 2020 07:15:14 GMT  
		Size: 4.4 MB (4360124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:587c025ae0482b8d3b5e8fc26b4af5eae6dc22c5c3da95ca52fbfc9c9a5b2f3a`  
		Last Modified: Tue, 01 Dec 2020 07:15:12 GMT  
		Size: 1.5 KB (1479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45314773dc31f89543794af67d864efadc99ec57ce116a3760d41a4c207f6f30`  
		Last Modified: Tue, 08 Dec 2020 00:19:11 GMT  
		Size: 570.9 KB (570925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4283c4537d91df6ad82cb299758a89bc3a5d2a8f42ddfe40ea81b189e8d6fb0`  
		Last Modified: Tue, 08 Dec 2020 00:19:11 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; s390x

```console
$ docker pull adminer@sha256:1f93751408862e70ce3d4b81bd3d7bdb4e2ecac81606992543e7bbfdbf90f96b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32598207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9061e3e2134cb0ffa169546bbf7624fe55bbea5f40e1b70016744979434fcc7d`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 11 Dec 2020 02:09:52 GMT
ADD file:c9395a36a4e03768aabd282eb1f31705cc00181d3147222d9c940eaa5a8fd511 in / 
# Fri, 11 Dec 2020 02:09:53 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 11:30:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 11 Dec 2020 11:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 11 Dec 2020 11:30:56 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 11 Dec 2020 11:30:57 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 11 Dec 2020 11:30:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 11 Dec 2020 11:36:17 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Fri, 11 Dec 2020 11:36:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Dec 2020 11:36:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Dec 2020 11:36:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 11 Dec 2020 12:09:03 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 11 Dec 2020 12:09:04 GMT
ENV PHP_VERSION=7.4.13
# Fri, 11 Dec 2020 12:09:04 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Fri, 11 Dec 2020 12:09:05 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Fri, 11 Dec 2020 12:09:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 11 Dec 2020 12:09:12 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Dec 2020 12:13:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Dec 2020 12:13:55 GMT
COPY multi:ebc915bbde1078ce3122b918e2e4c7726858af785343ade1a8d1a94f1052a4c7 in /usr/local/bin/ 
# Fri, 11 Dec 2020 12:13:57 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Dec 2020 12:13:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Dec 2020 12:13:59 GMT
WORKDIR /var/www/html
# Fri, 11 Dec 2020 12:14:00 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 11 Dec 2020 12:14:01 GMT
STOPSIGNAL SIGQUIT
# Fri, 11 Dec 2020 12:14:01 GMT
EXPOSE 9000
# Fri, 11 Dec 2020 12:14:02 GMT
CMD ["php-fpm"]
# Fri, 11 Dec 2020 18:45:19 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 11 Dec 2020 18:45:21 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 11 Dec 2020 18:46:30 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 11 Dec 2020 18:46:31 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 11 Dec 2020 18:46:32 GMT
ENV ADMINER_VERSION=4.7.8
# Fri, 11 Dec 2020 18:46:32 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Fri, 11 Dec 2020 18:46:33 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Fri, 11 Dec 2020 18:46:36 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 11 Dec 2020 18:46:37 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 11 Dec 2020 18:46:38 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 11 Dec 2020 18:46:38 GMT
USER adminer
# Fri, 11 Dec 2020 18:46:39 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:7c2470fe3d16cb70fca0826168095a96838b1322a8cd1502b28284ee8561b491`  
		Last Modified: Fri, 11 Dec 2020 02:10:27 GMT  
		Size: 2.6 MB (2565988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a23c8359d30ae261ad953f292e6681a71ebc7388607b74d901bbc07f71e1311`  
		Last Modified: Fri, 11 Dec 2020 13:48:01 GMT  
		Size: 1.4 MB (1382587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01422c3e898d3241d4134256bf0d911b0752823227af04614187c79c187e2843`  
		Last Modified: Fri, 11 Dec 2020 13:48:03 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a0be2077abd44f96e50bdebb1ed93a6e2b8d504761c23fa0e5e9b87045ca38`  
		Last Modified: Fri, 11 Dec 2020 13:48:01 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:797fc05bf988e85a5cf643f2d07a0b08a36e3f1529c75c41a2460041b6ee0f43`  
		Last Modified: Fri, 11 Dec 2020 13:50:52 GMT  
		Size: 10.3 MB (10338591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e11bb5dc7804a50c805852fbe653bb133478f5005e8c78c1d712af0d5bd6db4`  
		Last Modified: Fri, 11 Dec 2020 13:50:49 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:311bfe9de08521ea35d7a1520e00de8215315e5a8144a4335f1313ad7f6593de`  
		Last Modified: Fri, 11 Dec 2020 13:50:51 GMT  
		Size: 13.6 MB (13553700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59a788dffbadef519f959d8de10a3156add64ed4e15c8e96045a3bebf9ef316`  
		Last Modified: Fri, 11 Dec 2020 13:50:49 GMT  
		Size: 2.3 KB (2260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:898ee507348c01a8028e7ad08c8af3edde13cd884ffdfd990ad679df9b004552`  
		Last Modified: Fri, 11 Dec 2020 13:50:49 GMT  
		Size: 16.9 KB (16883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a7bec784d5537500a8f385256905e367037e6e1ae365f119cf3a305c384338f`  
		Last Modified: Fri, 11 Dec 2020 13:50:50 GMT  
		Size: 8.4 KB (8445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aacad6fcb4ce89b6aebc70fa08e0aeaf4004bdfd4288064a050ae7a6b6a1ca5`  
		Last Modified: Fri, 11 Dec 2020 18:47:37 GMT  
		Size: 310.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed17bffefe5fed1ad7e5ba183155f268ef4c6f19e11ce2b4d2b51a756f56e38`  
		Last Modified: Fri, 11 Dec 2020 18:47:32 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:195c8eb0f725b2189839adb7a0fec2e91f3b597dcf7a9a35cdb3cde9beea8e03`  
		Last Modified: Fri, 11 Dec 2020 18:47:33 GMT  
		Size: 4.2 MB (4153144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dd4956eb56581838eebbd42956889e3cc9dd1e7526a1282b8075c4c7daf28d1`  
		Last Modified: Fri, 11 Dec 2020 18:47:33 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a7b5a1b8dcaeb2cdc7acda96210109729ec955718cf8d30f683176a9ecf87be`  
		Last Modified: Fri, 11 Dec 2020 18:47:32 GMT  
		Size: 570.9 KB (570919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a3464ffffa7b21ee6c5a53d2f9143c982205d77f77a55bf9ec4ebb2cdff801`  
		Last Modified: Fri, 11 Dec 2020 18:47:33 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:4-standalone`

```console
$ docker pull adminer@sha256:4600f2453f7c9f3ee8179016a65d0b49a8dfb89467ac0947a6245e62e7f81fb1
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

### `adminer:4-standalone` - linux; amd64

```console
$ docker pull adminer@sha256:4b087576de7b4ca7c60bb3558f0b5ee30f496cee10fa19ea0a9f0e071c72b1f5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (33965375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2db7241b0f1461d8707525832e608fe513453f99c11beed9413194f7519e05`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 06:30:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 22 Oct 2020 06:30:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 22 Oct 2020 06:30:15 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 22 Oct 2020 06:30:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 22 Oct 2020 06:30:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 22 Oct 2020 06:30:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 06:30:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 06:30:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 22 Oct 2020 06:43:41 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 01 Dec 2020 04:36:20 GMT
ENV PHP_VERSION=7.4.13
# Tue, 01 Dec 2020 04:36:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Tue, 01 Dec 2020 04:36:21 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Tue, 01 Dec 2020 04:36:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 01 Dec 2020 04:36:27 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 01 Dec 2020 04:44:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 01 Dec 2020 04:44:54 GMT
COPY multi:afab483600631d4d87fe030871bbb016f1c2b73c0b72609d857bace419af7f5d in /usr/local/bin/ 
# Tue, 01 Dec 2020 04:44:57 GMT
RUN docker-php-ext-enable sodium
# Tue, 01 Dec 2020 04:44:57 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 01 Dec 2020 04:44:57 GMT
CMD ["php" "-a"]
# Tue, 01 Dec 2020 07:46:46 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Tue, 01 Dec 2020 07:46:46 GMT
STOPSIGNAL SIGINT
# Tue, 01 Dec 2020 07:46:47 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 01 Dec 2020 07:46:48 GMT
WORKDIR /var/www/html
# Tue, 01 Dec 2020 07:47:15 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Tue, 01 Dec 2020 07:47:15 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Tue, 08 Dec 2020 00:19:24 GMT
ENV ADMINER_VERSION=4.7.8
# Tue, 08 Dec 2020 00:19:24 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Tue, 08 Dec 2020 00:19:24 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Tue, 08 Dec 2020 00:19:26 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Tue, 08 Dec 2020 00:19:26 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 08 Dec 2020 00:19:26 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Tue, 08 Dec 2020 00:19:26 GMT
USER adminer
# Tue, 08 Dec 2020 00:19:27 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 08 Dec 2020 00:19:27 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f8bf6cfdbe614fef94f982905079c16e27b3de2d24eb1ff513d3d83e656ca2`  
		Last Modified: Thu, 22 Oct 2020 07:36:55 GMT  
		Size: 1.3 MB (1340771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce5be79740125b9e74a77885bf6ee2b0d25ac7ed9e9432c5aa7210bb3b00458a`  
		Last Modified: Thu, 22 Oct 2020 07:36:55 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99dd6507fe563b66ba35badf706e1bbb2d39eb5d0a3c0d5a86a45d2af7e89c1`  
		Last Modified: Thu, 22 Oct 2020 07:36:55 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c513a1b503cf7c9f18fa014dada9744070ded92dc9ad548cd056c4f56dc1a9`  
		Last Modified: Tue, 01 Dec 2020 07:27:10 GMT  
		Size: 10.3 MB (10338569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff080eafb4c0518981fca6aef4d239863fc59195f41ce7c440b2c6c518f2ac79`  
		Last Modified: Tue, 01 Dec 2020 07:27:09 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e818119992b11dbf09b710066a78920985b9ea1310fc8272df816e0884985f44`  
		Last Modified: Tue, 01 Dec 2020 07:27:13 GMT  
		Size: 14.6 MB (14572037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba3c14a67f95ae52ebfb558ab6b5d87687a05ce41c8df0a618ff42b73204e40`  
		Last Modified: Tue, 01 Dec 2020 07:27:09 GMT  
		Size: 2.3 KB (2257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbb0285b7ad2b170e4ed2cffbe0f16ba55d689c056ff43767834783eab7b8261`  
		Last Modified: Tue, 01 Dec 2020 07:27:09 GMT  
		Size: 17.0 KB (16987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae324cfad8acf03b3a98a15e963b7046404a7da3a6bbf68fd65d37f899f194d`  
		Last Modified: Tue, 01 Dec 2020 07:48:25 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb51158f683d66315de6fa572f7ea13d8ffb71ac85faa20c8578edb11678f37d`  
		Last Modified: Tue, 01 Dec 2020 07:48:23 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71ac21b64d1d63d967acb13664404babd0ef86fc896c484ce28cccf70001d0f1`  
		Last Modified: Tue, 01 Dec 2020 07:48:24 GMT  
		Size: 4.3 MB (4321455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2170e09d39d861e9bb7a5da5def906b44153b6c481fe17925ba82d1f1f78eec`  
		Last Modified: Tue, 01 Dec 2020 07:48:24 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d95b48dfa11f7f5c061f6522f6ff5d574452b8f321c6075455da2643b1967a`  
		Last Modified: Tue, 08 Dec 2020 00:19:45 GMT  
		Size: 570.9 KB (570860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3bb2b5e72bf0dbd4b855ddf65aaf9c0d077703804bdbdc9ea3ea98cbbfceaf6`  
		Last Modified: Tue, 08 Dec 2020 00:19:44 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; arm variant v6

```console
$ docker pull adminer@sha256:7e114494e5e3a8ece382083d27c33f6c993695f0ff6c92c235ced149177f5da9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32073857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9cfa5ccbab063435267257cf4c761402c956233cf22775ed1c774b53a045715`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 11 Dec 2020 02:17:15 GMT
ADD file:1a9c0a67560d338c0c0e7005d8915d998fc9cf3e9f53bfd7e42e8391f0a39bce in / 
# Fri, 11 Dec 2020 02:17:15 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 07:04:50 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 11 Dec 2020 07:04:53 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 11 Dec 2020 07:04:55 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 11 Dec 2020 07:04:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 11 Dec 2020 07:04:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 11 Dec 2020 07:05:00 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Dec 2020 07:05:01 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Dec 2020 07:05:02 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 11 Dec 2020 07:13:50 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 11 Dec 2020 07:13:54 GMT
ENV PHP_VERSION=7.4.13
# Fri, 11 Dec 2020 07:13:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Fri, 11 Dec 2020 07:13:56 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Fri, 11 Dec 2020 07:14:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 11 Dec 2020 07:14:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Dec 2020 07:17:37 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Dec 2020 07:17:39 GMT
COPY multi:afab483600631d4d87fe030871bbb016f1c2b73c0b72609d857bace419af7f5d in /usr/local/bin/ 
# Fri, 11 Dec 2020 07:17:42 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Dec 2020 07:17:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Dec 2020 07:17:43 GMT
CMD ["php" "-a"]
# Fri, 11 Dec 2020 09:04:18 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 11 Dec 2020 09:04:19 GMT
STOPSIGNAL SIGINT
# Fri, 11 Dec 2020 09:04:21 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 11 Dec 2020 09:04:22 GMT
WORKDIR /var/www/html
# Fri, 11 Dec 2020 09:05:06 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 11 Dec 2020 09:05:08 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 11 Dec 2020 09:05:08 GMT
ENV ADMINER_VERSION=4.7.8
# Fri, 11 Dec 2020 09:05:09 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Fri, 11 Dec 2020 09:05:11 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Fri, 11 Dec 2020 09:05:14 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 11 Dec 2020 09:05:15 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 11 Dec 2020 09:05:16 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 11 Dec 2020 09:05:17 GMT
USER adminer
# Fri, 11 Dec 2020 09:05:18 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 11 Dec 2020 09:05:19 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:f1c16df8fee33d421d08790b17ca2af67a3fe49e77b6b991dd0c30631f5d1baf`  
		Last Modified: Fri, 11 Dec 2020 02:17:57 GMT  
		Size: 2.6 MB (2601992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623cc08cbe035cf15859e57a83e2243620418da06e1905d1875a46bec901e540`  
		Last Modified: Fri, 11 Dec 2020 07:56:49 GMT  
		Size: 1.3 MB (1310156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3a7aacff9b7ccf646f2bdbbc8d40bbb304550e813876049e721abd35461df9`  
		Last Modified: Fri, 11 Dec 2020 07:56:49 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d3214ea6f418597f370177309be7728f94481030c9cba6e45c4b74cfd04cc0`  
		Last Modified: Fri, 11 Dec 2020 07:56:49 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64de18534c9c3dd7212eceb5a285d571df578238ca4684a2e922b131e9947d79`  
		Last Modified: Fri, 11 Dec 2020 07:57:40 GMT  
		Size: 10.3 MB (10338603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d60b5c1c75b96676e4154f74a500fdd4a2645d4c51e189b0bdd18e06f26c3143`  
		Last Modified: Fri, 11 Dec 2020 07:57:39 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee32c3be90bc13cb4b3406c492ec35d5c211ac42b25e536939fb3220aea672b`  
		Last Modified: Fri, 11 Dec 2020 07:57:44 GMT  
		Size: 13.2 MB (13201116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e71cdda7d8acfe2fe1a6263c1b004b3ae972d7ce1c0ac95fec09aa0c0ba1f7fd`  
		Last Modified: Fri, 11 Dec 2020 07:57:39 GMT  
		Size: 2.3 KB (2258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec74a6ee1beba601eed5abe261394c8ddfa2d53093a1f6768356ec5891066746`  
		Last Modified: Fri, 11 Dec 2020 07:57:40 GMT  
		Size: 16.9 KB (16889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b84bf5ad218839b4e8156c322c5611b3c26167141a7c1e8049055deeda8b1ed5`  
		Last Modified: Fri, 11 Dec 2020 09:07:23 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0113ef6e65685219488d6543639cff152292617519f4649a6d7c8e4bbf03322b`  
		Last Modified: Fri, 11 Dec 2020 09:07:21 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2501c821a30d874046f30dd9d3947aa9f82cca3e9d39eb18214a765744e0b24`  
		Last Modified: Fri, 11 Dec 2020 09:07:21 GMT  
		Size: 4.0 MB (4026242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:945b172c5cf67a28a59e5b25cfed08871f360f551a912c8d7f64c096d6554812`  
		Last Modified: Fri, 11 Dec 2020 09:07:20 GMT  
		Size: 1.5 KB (1473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df40a3aa85441cb471ce645d5a0a2564fb9e2f042e078b8f04dd343488863a4`  
		Last Modified: Fri, 11 Dec 2020 09:07:20 GMT  
		Size: 570.9 KB (570917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90644dda17e22024741efd92b2987150a52659ae6bb25b7ea232e9b72d3b1d83`  
		Last Modified: Fri, 11 Dec 2020 09:07:20 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; arm variant v7

```console
$ docker pull adminer@sha256:39b988e9485b8f06142e8584a4764c3c32159d51377eab0739b1cf794f701d1a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31186995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d4ed3310dfe2d29dd9a809a5ea826952ac518c5d93ab5e12054d9b7560791f7`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 22 Oct 2020 01:58:13 GMT
ADD file:46f89172426e9f5b1d669a2ca7ab218fc2deaef1caeeab88f2b5bd443ac9773d in / 
# Thu, 22 Oct 2020 01:58:14 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 06:47:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 22 Oct 2020 06:47:37 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 22 Oct 2020 06:47:45 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 22 Oct 2020 06:47:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 22 Oct 2020 06:47:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 22 Oct 2020 06:47:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 06:47:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 06:48:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 22 Oct 2020 06:56:26 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 01 Dec 2020 02:39:45 GMT
ENV PHP_VERSION=7.4.13
# Tue, 01 Dec 2020 02:39:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Tue, 01 Dec 2020 02:39:46 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Tue, 01 Dec 2020 02:39:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 01 Dec 2020 02:39:53 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 01 Dec 2020 02:42:30 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 01 Dec 2020 02:42:32 GMT
COPY multi:afab483600631d4d87fe030871bbb016f1c2b73c0b72609d857bace419af7f5d in /usr/local/bin/ 
# Tue, 01 Dec 2020 02:42:37 GMT
RUN docker-php-ext-enable sodium
# Tue, 01 Dec 2020 02:42:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 01 Dec 2020 02:42:40 GMT
CMD ["php" "-a"]
# Tue, 01 Dec 2020 04:28:04 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Tue, 01 Dec 2020 04:28:05 GMT
STOPSIGNAL SIGINT
# Tue, 01 Dec 2020 04:28:12 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 01 Dec 2020 04:28:14 GMT
WORKDIR /var/www/html
# Tue, 01 Dec 2020 04:29:07 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Tue, 01 Dec 2020 04:29:08 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Tue, 08 Dec 2020 00:00:44 GMT
ENV ADMINER_VERSION=4.7.8
# Tue, 08 Dec 2020 00:00:49 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Tue, 08 Dec 2020 00:00:52 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Tue, 08 Dec 2020 00:00:57 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Tue, 08 Dec 2020 00:00:58 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 08 Dec 2020 00:00:59 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Tue, 08 Dec 2020 00:00:59 GMT
USER adminer
# Tue, 08 Dec 2020 00:01:00 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 08 Dec 2020 00:01:01 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:5f2023fd85a4e68f37fe41421fd89f30e69b98a645613521c57c01317561eee3`  
		Last Modified: Thu, 22 Oct 2020 01:58:45 GMT  
		Size: 2.4 MB (2405675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60b50c98f8a8e2c6a27378dfa0f44df1844ac67c6981303675f138a42679f25`  
		Last Modified: Thu, 22 Oct 2020 07:35:57 GMT  
		Size: 1.2 MB (1214265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b472094d673b7c272085505c976192b9aaafa3157c99bade9755fbca18a24071`  
		Last Modified: Thu, 22 Oct 2020 07:35:56 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc39e5d916c11e7eb158e72d14ab981eb45ccc7b6451c1d6d3cb627b71cdbb6`  
		Last Modified: Thu, 22 Oct 2020 07:35:55 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e834fd39435ea86b08faf9b3af2e2623e0a247fa06dfe096decdf80f7a986a`  
		Last Modified: Tue, 01 Dec 2020 04:00:44 GMT  
		Size: 10.3 MB (10338583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a458e4d5704bca7330dbfab239f74ff255f4813b58f19f50a4ad7fd7087f0c8`  
		Last Modified: Tue, 01 Dec 2020 04:00:43 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a500121bbd97abb5116b6e95bdaa9aed74160334e46aadaabef548dca0edce6`  
		Last Modified: Tue, 01 Dec 2020 04:00:46 GMT  
		Size: 12.7 MB (12706582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3321b09ca6255e6f5cb4dce9057df675dd4644a3654424c7ee95fbdcb083e9c`  
		Last Modified: Tue, 01 Dec 2020 04:00:42 GMT  
		Size: 2.3 KB (2257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:345450fde280cf49e34f7246cebd38e311d4b7bebe22415a6126c18e67899f91`  
		Last Modified: Tue, 01 Dec 2020 04:00:42 GMT  
		Size: 16.9 KB (16903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:520112c186c5f2a097e8056a524b7c35704923ebeb6247e924ca839fe6e5b343`  
		Last Modified: Tue, 01 Dec 2020 04:31:36 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d98e04775b392470b2f426804979b34d740103414161d9c89f4df0d0b086e51`  
		Last Modified: Tue, 01 Dec 2020 04:31:34 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c074206a89c8b669d116ecf57544d500dcdc5379828bb10e531adf7af19b658a`  
		Last Modified: Tue, 01 Dec 2020 04:31:34 GMT  
		Size: 3.9 MB (3926108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137384dc891a62af154426c4b36cb9192967da61547507bc1b95301727f85c39`  
		Last Modified: Tue, 01 Dec 2020 04:31:34 GMT  
		Size: 1.5 KB (1473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfdcb3be5430d4c822996a4b1f107a12cafae7d60cc6faf1f7a7cdd8dacaab94`  
		Last Modified: Tue, 08 Dec 2020 00:01:41 GMT  
		Size: 570.9 KB (570924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e55c2ae42163732e674f91058ca3617c71403e138adb01dd23c943ad95d6b0`  
		Last Modified: Tue, 08 Dec 2020 00:01:41 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:b1e09cd04824b43f07df33154a383bc15923451af616eaaae657aca0620d729f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33702279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea6b86a866d797b65cc54d7527a70e1a5e91bf21ecc1ee3fd22b2a2c18d7f6ed`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 07:18:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 22 Oct 2020 07:18:56 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 22 Oct 2020 07:18:59 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 22 Oct 2020 07:19:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 22 Oct 2020 07:19:04 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 22 Oct 2020 07:19:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 07:19:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 07:19:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 22 Oct 2020 07:27:59 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 01 Dec 2020 03:27:01 GMT
ENV PHP_VERSION=7.4.13
# Tue, 01 Dec 2020 03:27:02 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Tue, 01 Dec 2020 03:27:03 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Tue, 01 Dec 2020 03:27:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 01 Dec 2020 03:27:09 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 01 Dec 2020 03:30:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 01 Dec 2020 03:30:42 GMT
COPY multi:afab483600631d4d87fe030871bbb016f1c2b73c0b72609d857bace419af7f5d in /usr/local/bin/ 
# Tue, 01 Dec 2020 03:30:50 GMT
RUN docker-php-ext-enable sodium
# Tue, 01 Dec 2020 03:30:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 01 Dec 2020 03:30:56 GMT
CMD ["php" "-a"]
# Tue, 01 Dec 2020 08:12:36 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Tue, 01 Dec 2020 08:12:37 GMT
STOPSIGNAL SIGINT
# Tue, 01 Dec 2020 08:12:39 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 01 Dec 2020 08:12:40 GMT
WORKDIR /var/www/html
# Tue, 01 Dec 2020 08:13:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Tue, 01 Dec 2020 08:13:23 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Mon, 07 Dec 2020 23:39:52 GMT
ENV ADMINER_VERSION=4.7.8
# Mon, 07 Dec 2020 23:39:53 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Mon, 07 Dec 2020 23:39:54 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Mon, 07 Dec 2020 23:39:56 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Mon, 07 Dec 2020 23:39:57 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Mon, 07 Dec 2020 23:39:58 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Mon, 07 Dec 2020 23:39:58 GMT
USER adminer
# Mon, 07 Dec 2020 23:39:59 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Mon, 07 Dec 2020 23:40:00 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d57dba23203172f8fffd1379aef0307e782178b62dfc684d43c546f7e874ed`  
		Last Modified: Thu, 22 Oct 2020 08:06:21 GMT  
		Size: 1.3 MB (1342784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8414edb0c9c2f7472bb6228bf691a2ddac19ddad7bad789c7cbdc147aded711`  
		Last Modified: Thu, 22 Oct 2020 08:06:20 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d26eeef0db35b2328adae38a8490c7403844452c3606dd17fbe68216f98e82`  
		Last Modified: Thu, 22 Oct 2020 08:06:19 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29be11fa56be3ca1af1498b259f3d5e058a869970cac6d670cf4ca1502485810`  
		Last Modified: Tue, 01 Dec 2020 04:53:56 GMT  
		Size: 10.3 MB (10338597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a553892b0358f6f72064d4dd5e727b686c4461cca7ea8a1211cc86adddb2cb`  
		Last Modified: Tue, 01 Dec 2020 04:53:56 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:828f98d07be67a182899230fc7e38e513de6ce85178d60116c765e90ffbc4119`  
		Last Modified: Tue, 01 Dec 2020 04:54:00 GMT  
		Size: 14.4 MB (14386945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec168016016eef2bef46796f7d7ec48af2459e14d65b9fc2871e756fe3e14d6a`  
		Last Modified: Tue, 01 Dec 2020 04:53:56 GMT  
		Size: 2.3 KB (2260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca32a186f8576115bc6fffe021ff54c52337662fa3cdb51c863d12d20ba02de`  
		Last Modified: Tue, 01 Dec 2020 04:53:55 GMT  
		Size: 17.0 KB (16976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b859cea4a3bb568911dd8f097b1a684daef31726fc5a591b4d9cd57b35187f`  
		Last Modified: Tue, 01 Dec 2020 08:14:59 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e97602a3ba690a845f8ecfaabcff93f82efc85a36445f6413d26f2482987638`  
		Last Modified: Tue, 01 Dec 2020 08:14:56 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6067b9bb9a3850bc39e227d17ab5df99a9bbe61e6d9933fc63c85e464f4aedf5`  
		Last Modified: Tue, 01 Dec 2020 08:14:57 GMT  
		Size: 4.3 MB (4331540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c677bbe386af33259d80d8f4d08a7147fef67adf472b9d841dac1a4a118c7f`  
		Last Modified: Tue, 01 Dec 2020 08:14:57 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4763c08ec3b1c7b68505b48ed92faf18a62525f8ce02d4fba750c232c1826aa9`  
		Last Modified: Mon, 07 Dec 2020 23:40:27 GMT  
		Size: 570.9 KB (570924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:983b1fb60b2afcee1aa424434071184fe8cf507838ac872e30e48755b41f1232`  
		Last Modified: Mon, 07 Dec 2020 23:40:28 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; 386

```console
$ docker pull adminer@sha256:13a4c7ddafd6d4d6a5ee85529f6fa01ebe99d5c5bc1bcafafc85425658693817
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34626966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bb37df3c96977a9c7d5bcff85e2f3904eb30a1d4e2358f0c1644fae769a3ea7`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 22 Oct 2020 02:00:33 GMT
ADD file:46ad43b4984bcf49c5a888ff3628f23161f55cd1fb062f469e707100c97fa254 in / 
# Thu, 22 Oct 2020 02:00:33 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:36:23 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 22 Oct 2020 03:36:26 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 22 Oct 2020 03:36:27 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 22 Oct 2020 03:36:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 22 Oct 2020 03:36:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 22 Oct 2020 03:36:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 03:36:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 03:36:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 22 Oct 2020 03:55:07 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 01 Dec 2020 04:01:21 GMT
ENV PHP_VERSION=7.4.13
# Tue, 01 Dec 2020 04:01:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Tue, 01 Dec 2020 04:01:22 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Tue, 01 Dec 2020 04:01:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 01 Dec 2020 04:01:40 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 01 Dec 2020 04:10:51 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 01 Dec 2020 04:10:52 GMT
COPY multi:afab483600631d4d87fe030871bbb016f1c2b73c0b72609d857bace419af7f5d in /usr/local/bin/ 
# Tue, 01 Dec 2020 04:10:54 GMT
RUN docker-php-ext-enable sodium
# Tue, 01 Dec 2020 04:10:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 01 Dec 2020 04:10:55 GMT
CMD ["php" "-a"]
# Tue, 01 Dec 2020 09:24:38 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Tue, 01 Dec 2020 09:24:38 GMT
STOPSIGNAL SIGINT
# Tue, 01 Dec 2020 09:24:39 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 01 Dec 2020 09:24:39 GMT
WORKDIR /var/www/html
# Tue, 01 Dec 2020 09:25:13 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Tue, 01 Dec 2020 09:25:13 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Mon, 07 Dec 2020 23:38:24 GMT
ENV ADMINER_VERSION=4.7.8
# Mon, 07 Dec 2020 23:38:24 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Mon, 07 Dec 2020 23:38:24 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Mon, 07 Dec 2020 23:38:26 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Mon, 07 Dec 2020 23:38:26 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Mon, 07 Dec 2020 23:38:26 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Mon, 07 Dec 2020 23:38:26 GMT
USER adminer
# Mon, 07 Dec 2020 23:38:26 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Mon, 07 Dec 2020 23:38:27 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:d6ca64ac6f4b6382142ce9a3501652938130a6ec4bb02f3f455ee1f980834cfe`  
		Last Modified: Thu, 22 Oct 2020 02:00:57 GMT  
		Size: 2.8 MB (2791407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30be8ffd290910905a5fb7cbb70252eb0f59edb09db20bdc21f3b65456acc28f`  
		Last Modified: Thu, 22 Oct 2020 05:10:23 GMT  
		Size: 1.4 MB (1439641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d58e2433b13446c863e85b34f8e4c93ca9d5b3b93d2bac415fd9cdf77bcec4`  
		Last Modified: Thu, 22 Oct 2020 05:10:21 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5729dcb8d303f82a7f8cf3df49048e34ce8ee89f79155fb08a475da46b64308`  
		Last Modified: Thu, 22 Oct 2020 05:10:21 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ffdca9b500ff910069fefe63b455206db2cf0fa00dc6b7c7d53219dfaf7f5b`  
		Last Modified: Tue, 01 Dec 2020 07:15:13 GMT  
		Size: 10.3 MB (10338561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c682383cda14fca62843652d7478a26995cfbbfbcb457985de4ca5cfb77de751`  
		Last Modified: Tue, 01 Dec 2020 07:15:12 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57833a53685f649182bdbb4194ba35390c17fa65a6b09c4e377a42a5f9aaca30`  
		Last Modified: Tue, 01 Dec 2020 07:15:18 GMT  
		Size: 14.9 MB (14942640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7003874a29c37e250b24c310b448d1c36607cdb1b43128071780d5fd0a0dc3e1`  
		Last Modified: Tue, 01 Dec 2020 07:15:12 GMT  
		Size: 2.3 KB (2259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fcfab619124f72931608ea142c1cd80a26871e1631380720b6be739170e21b6`  
		Last Modified: Tue, 01 Dec 2020 07:15:12 GMT  
		Size: 16.9 KB (16924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055719a49e04df90bb23499c98da9779637e3b44446a60f202283f57e4b29b04`  
		Last Modified: Tue, 01 Dec 2020 09:26:14 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2b0f52d9f107a35a34b4f8c69abbdf24f2de8a0431c812d74cb6dd3cbf8bf2`  
		Last Modified: Tue, 01 Dec 2020 09:26:13 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4edb5ffb9c3f753b4991debfaeef5c535ae5d689a18b7fff9f0b042c5883865`  
		Last Modified: Tue, 01 Dec 2020 09:26:14 GMT  
		Size: 4.5 MB (4519100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9258866f679eb2cbc89aa311d5d2dad0c146a7e9f61c9e805b63d7f324d2afb0`  
		Last Modified: Tue, 01 Dec 2020 09:26:13 GMT  
		Size: 1.5 KB (1472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:904e3ae5079e7cd06213e6912d4237663cff97a37e1ed247e24b7f455951eafe`  
		Last Modified: Mon, 07 Dec 2020 23:38:45 GMT  
		Size: 570.9 KB (570859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:362b319c8a865e06c57265a80b857954a02a4e09ffe3eda699eede128dcdef90`  
		Last Modified: Mon, 07 Dec 2020 23:38:45 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; ppc64le

```console
$ docker pull adminer@sha256:73feff7b317d1078b173d0c1dc928c14bf61e94b4562a0a79132b9dac74739aa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 MB (35029016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2bacaef82d901426ed9bf50182af16a98e04172b1d2dac51b87db0885487f72`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 22 Oct 2020 11:00:06 GMT
ADD file:176e047fab2c1828575bffa6b14773efa297b7ecf312d86103c5dd4f78ec8027 in / 
# Thu, 22 Oct 2020 11:00:17 GMT
CMD ["/bin/sh"]
# Fri, 23 Oct 2020 00:21:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 23 Oct 2020 00:21:18 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 23 Oct 2020 00:21:30 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 23 Oct 2020 00:21:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 23 Oct 2020 00:21:44 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 23 Oct 2020 00:21:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 23 Oct 2020 00:21:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 23 Oct 2020 00:21:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 23 Oct 2020 00:34:37 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 01 Dec 2020 03:52:39 GMT
ENV PHP_VERSION=7.4.13
# Tue, 01 Dec 2020 03:52:44 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Tue, 01 Dec 2020 03:52:51 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Tue, 01 Dec 2020 03:53:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 01 Dec 2020 03:53:13 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 01 Dec 2020 03:57:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 01 Dec 2020 03:57:24 GMT
COPY multi:afab483600631d4d87fe030871bbb016f1c2b73c0b72609d857bace419af7f5d in /usr/local/bin/ 
# Tue, 01 Dec 2020 03:57:33 GMT
RUN docker-php-ext-enable sodium
# Tue, 01 Dec 2020 03:57:36 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 01 Dec 2020 03:57:39 GMT
CMD ["php" "-a"]
# Tue, 01 Dec 2020 07:09:03 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Tue, 01 Dec 2020 07:09:12 GMT
STOPSIGNAL SIGINT
# Tue, 01 Dec 2020 07:09:25 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 01 Dec 2020 07:09:32 GMT
WORKDIR /var/www/html
# Tue, 01 Dec 2020 07:10:30 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Tue, 01 Dec 2020 07:10:33 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Tue, 08 Dec 2020 00:16:36 GMT
ENV ADMINER_VERSION=4.7.8
# Tue, 08 Dec 2020 00:16:38 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Tue, 08 Dec 2020 00:16:41 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Tue, 08 Dec 2020 00:16:53 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Tue, 08 Dec 2020 00:16:54 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 08 Dec 2020 00:16:58 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Tue, 08 Dec 2020 00:17:11 GMT
USER adminer
# Tue, 08 Dec 2020 00:17:16 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 08 Dec 2020 00:17:18 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:692a9d763e196c85d79fc3e45b316b1bb557c93ba88a3c8ebf679a585d1efe73`  
		Last Modified: Thu, 22 Oct 2020 11:02:06 GMT  
		Size: 2.8 MB (2803218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0285d6f06f3beb1c140c055210664c441b93dd4f2037177a5396bce94ca16ce5`  
		Last Modified: Fri, 23 Oct 2020 01:34:08 GMT  
		Size: 1.4 MB (1383187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a6459a3bf272daa53ff4ba97cc849676f497de9f78d8e9378ec02552293f175`  
		Last Modified: Fri, 23 Oct 2020 01:34:07 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16cff6064dc29d3f629d353736c1cac074caa5b50738422adb84de99a019bb32`  
		Last Modified: Fri, 23 Oct 2020 01:34:08 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0baf560776c5dd75b5673be3d73b900119615cfc4e4fe24414486e3d1f11920`  
		Last Modified: Tue, 01 Dec 2020 05:50:29 GMT  
		Size: 10.3 MB (10338609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4d8083b683ead9a591a00aff14c8d0091665e1433d301a027b214f19cbe23f`  
		Last Modified: Tue, 01 Dec 2020 05:50:29 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7381e6ce3e117510e5a2bf102da48e3cc1b5fd3414651ec324bbe759d367be`  
		Last Modified: Tue, 01 Dec 2020 05:50:32 GMT  
		Size: 15.5 MB (15548036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8328c4e67c6b29f383993d05557e298bc834c18c00961b9ab2a1c4e4eb05b4fd`  
		Last Modified: Tue, 01 Dec 2020 05:50:28 GMT  
		Size: 2.3 KB (2259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:236813d0f57da4fa9c0d5938846f85e82a0a01ce89ca208916b8f649c0ee99fd`  
		Last Modified: Tue, 01 Dec 2020 05:50:28 GMT  
		Size: 17.0 KB (16965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acf7ec6b5baaa9faab722bfc6a7098e0871e3edb42be513e64fe8e06bc7edec1`  
		Last Modified: Tue, 01 Dec 2020 07:14:36 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c17363dc3aab754805ecdc74f39535a73cfc5f3cebe72a4cb18fdc97df1ef9fa`  
		Last Modified: Tue, 01 Dec 2020 07:14:33 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95753fdce29daf55de647d3a29a8cc07941f7bf95fec4a560b0d698478b782f3`  
		Last Modified: Tue, 01 Dec 2020 07:14:34 GMT  
		Size: 4.4 MB (4360119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cad5fcb53526734d41770680ea56047b6e13c767960fc1d0a0b8de7c7030c75`  
		Last Modified: Tue, 01 Dec 2020 07:14:33 GMT  
		Size: 1.5 KB (1474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b231a33566f06d48010343aac194149b1ce1613cf2397c67cf1be2984295f133`  
		Last Modified: Tue, 08 Dec 2020 00:18:38 GMT  
		Size: 570.9 KB (570925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628d0ad1cc992636ad6e5a1f0cf7de70d844c7cccb85cda16205dc67b167e131`  
		Last Modified: Tue, 08 Dec 2020 00:18:38 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; s390x

```console
$ docker pull adminer@sha256:6b00709e793594a51832541158adeb2ae42e00829dbfb77a54bc0eef7fd1668d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32521955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f75d1bfddd1544fe2cddf65f0baa090dfb992c4a38b43b24670dc3b1ce037d7`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 11 Dec 2020 02:09:52 GMT
ADD file:c9395a36a4e03768aabd282eb1f31705cc00181d3147222d9c940eaa5a8fd511 in / 
# Fri, 11 Dec 2020 02:09:53 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 11:30:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 11 Dec 2020 11:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 11 Dec 2020 11:30:56 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 11 Dec 2020 11:30:57 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 11 Dec 2020 11:30:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 11 Dec 2020 11:30:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Dec 2020 11:31:00 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Dec 2020 11:31:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 11 Dec 2020 12:01:46 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 11 Dec 2020 12:01:46 GMT
ENV PHP_VERSION=7.4.13
# Fri, 11 Dec 2020 12:01:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Fri, 11 Dec 2020 12:01:48 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Fri, 11 Dec 2020 12:01:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 11 Dec 2020 12:01:54 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Dec 2020 12:08:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Dec 2020 12:08:47 GMT
COPY multi:afab483600631d4d87fe030871bbb016f1c2b73c0b72609d857bace419af7f5d in /usr/local/bin/ 
# Fri, 11 Dec 2020 12:08:49 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Dec 2020 12:08:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Dec 2020 12:08:50 GMT
CMD ["php" "-a"]
# Fri, 11 Dec 2020 18:43:30 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 11 Dec 2020 18:43:31 GMT
STOPSIGNAL SIGINT
# Fri, 11 Dec 2020 18:43:33 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 11 Dec 2020 18:43:33 GMT
WORKDIR /var/www/html
# Fri, 11 Dec 2020 18:44:50 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 11 Dec 2020 18:44:50 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 11 Dec 2020 18:44:51 GMT
ENV ADMINER_VERSION=4.7.8
# Fri, 11 Dec 2020 18:44:52 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Fri, 11 Dec 2020 18:44:52 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Fri, 11 Dec 2020 18:44:56 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 11 Dec 2020 18:44:57 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 11 Dec 2020 18:44:57 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 11 Dec 2020 18:44:58 GMT
USER adminer
# Fri, 11 Dec 2020 18:44:59 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 11 Dec 2020 18:44:59 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:7c2470fe3d16cb70fca0826168095a96838b1322a8cd1502b28284ee8561b491`  
		Last Modified: Fri, 11 Dec 2020 02:10:27 GMT  
		Size: 2.6 MB (2565988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a23c8359d30ae261ad953f292e6681a71ebc7388607b74d901bbc07f71e1311`  
		Last Modified: Fri, 11 Dec 2020 13:48:01 GMT  
		Size: 1.4 MB (1382587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01422c3e898d3241d4134256bf0d911b0752823227af04614187c79c187e2843`  
		Last Modified: Fri, 11 Dec 2020 13:48:03 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a0be2077abd44f96e50bdebb1ed93a6e2b8d504761c23fa0e5e9b87045ca38`  
		Last Modified: Fri, 11 Dec 2020 13:48:01 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267bafe0bb23009994a23ad5cdcc3b4d425f186f0e488b5f7461463ad1b53814`  
		Last Modified: Fri, 11 Dec 2020 13:50:24 GMT  
		Size: 10.3 MB (10338590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36304b0fbddac7ce44edacaedb902676688cfc3bb7082576f6b57eed0ccc133e`  
		Last Modified: Fri, 11 Dec 2020 13:50:25 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fa33489075ff6318ffc5a7cf5c94cb4ce65ccfc82b5970cc91628780c130aae`  
		Last Modified: Fri, 11 Dec 2020 13:50:26 GMT  
		Size: 13.5 MB (13485898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155ae451461e50390ae0db27a78a329e87a86b9f9eb04f6db81fcc27430f2d51`  
		Last Modified: Fri, 11 Dec 2020 13:50:24 GMT  
		Size: 2.3 KB (2257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b379111cc7023c652243c4d9234de47984fa307030d667bf14e5d12889ec8180`  
		Last Modified: Fri, 11 Dec 2020 13:50:24 GMT  
		Size: 16.9 KB (16879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a18e16d8efd7f249149e2d38813d86590cc4a55f23d8c5bbba970725422ea51`  
		Last Modified: Fri, 11 Dec 2020 18:47:13 GMT  
		Size: 310.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ba44137233477a93edb1e0cc94bee3ce4dafaed9ff932d21594190f861ef75`  
		Last Modified: Fri, 11 Dec 2020 18:47:13 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cba732448866bbb0e567b7510578f951e9cf0bc258588c8e898be1606e3a3eb`  
		Last Modified: Fri, 11 Dec 2020 18:47:11 GMT  
		Size: 4.2 MB (4153155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8faf5f39c5d146bc658625977adca6ce417bb45b9683bb1767b99abfea6d3d56`  
		Last Modified: Fri, 11 Dec 2020 18:47:11 GMT  
		Size: 1.5 KB (1473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008d2a285f2f6bcf687be0cb08b167a975a4d7534a16435da10ba2b75b2e2d73`  
		Last Modified: Fri, 11 Dec 2020 18:47:11 GMT  
		Size: 570.9 KB (570918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6852608d1b2324d98a56de31e6fc11ac1fe8e95f605b50c9f72db2bd5cd092`  
		Last Modified: Fri, 11 Dec 2020 18:47:12 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:fastcgi`

```console
$ docker pull adminer@sha256:c0bcea38afeb9296d883e7371a4b83a97384f02ed2d2c3e71a6823267d6f0bac
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

### `adminer:fastcgi` - linux; amd64

```console
$ docker pull adminer@sha256:fb2f45c8e550ba3d59351c5ab1ac746adcab7dfb5e2d0b2a27531d2b664f598b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (34042656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff0774240cbda9b72e1940dc60ecd8366d3b4df4e789a7284078c8698364477`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 06:30:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 22 Oct 2020 06:30:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 22 Oct 2020 06:30:15 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 22 Oct 2020 06:30:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 22 Oct 2020 06:30:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 22 Oct 2020 06:37:19 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Thu, 22 Oct 2020 06:37:19 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 06:37:19 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 06:37:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 22 Oct 2020 06:49:00 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 01 Dec 2020 04:45:15 GMT
ENV PHP_VERSION=7.4.13
# Tue, 01 Dec 2020 04:45:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Tue, 01 Dec 2020 04:45:15 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Tue, 01 Dec 2020 04:45:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 01 Dec 2020 04:45:21 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 01 Dec 2020 04:54:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 01 Dec 2020 04:54:04 GMT
COPY multi:ebc915bbde1078ce3122b918e2e4c7726858af785343ade1a8d1a94f1052a4c7 in /usr/local/bin/ 
# Tue, 01 Dec 2020 04:54:07 GMT
RUN docker-php-ext-enable sodium
# Tue, 01 Dec 2020 04:54:07 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 01 Dec 2020 04:54:08 GMT
WORKDIR /var/www/html
# Tue, 01 Dec 2020 04:54:09 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Tue, 01 Dec 2020 04:54:10 GMT
STOPSIGNAL SIGQUIT
# Tue, 01 Dec 2020 04:54:10 GMT
EXPOSE 9000
# Tue, 01 Dec 2020 04:54:11 GMT
CMD ["php-fpm"]
# Tue, 01 Dec 2020 07:47:26 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Tue, 01 Dec 2020 07:47:28 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 01 Dec 2020 07:48:01 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Tue, 01 Dec 2020 07:48:01 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Tue, 08 Dec 2020 00:19:31 GMT
ENV ADMINER_VERSION=4.7.8
# Tue, 08 Dec 2020 00:19:31 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Tue, 08 Dec 2020 00:19:31 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Tue, 08 Dec 2020 00:19:33 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Tue, 08 Dec 2020 00:19:33 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 08 Dec 2020 00:19:33 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Tue, 08 Dec 2020 00:19:33 GMT
USER adminer
# Tue, 08 Dec 2020 00:19:33 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f8bf6cfdbe614fef94f982905079c16e27b3de2d24eb1ff513d3d83e656ca2`  
		Last Modified: Thu, 22 Oct 2020 07:36:55 GMT  
		Size: 1.3 MB (1340771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce5be79740125b9e74a77885bf6ee2b0d25ac7ed9e9432c5aa7210bb3b00458a`  
		Last Modified: Thu, 22 Oct 2020 07:36:55 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99dd6507fe563b66ba35badf706e1bbb2d39eb5d0a3c0d5a86a45d2af7e89c1`  
		Last Modified: Thu, 22 Oct 2020 07:36:55 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c3b45daa37929dd9a002107adb1299c5b070bbba60b73cf9ecc2d9fd6e78f9`  
		Last Modified: Tue, 01 Dec 2020 07:27:28 GMT  
		Size: 10.3 MB (10338571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6afb095daafcd5f742a42ee6dbf8f6d03fdca63c22071198f243df20ecef1db9`  
		Last Modified: Tue, 01 Dec 2020 07:27:25 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838cecfde999e9ecf65003522df2ce13e12fa5190e2336ffb1d16da9a787ead4`  
		Last Modified: Tue, 01 Dec 2020 07:27:29 GMT  
		Size: 14.6 MB (14640876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a46b7ab0f2d19433340bdeca3307275efd3188c446a3c739c1196c9bd05a0e`  
		Last Modified: Tue, 01 Dec 2020 07:27:26 GMT  
		Size: 2.3 KB (2255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d2139a9b9d18bdd892644fe463b368727e54ba53b145694a26f4cfe3f8e61d1`  
		Last Modified: Tue, 01 Dec 2020 07:27:26 GMT  
		Size: 17.0 KB (16987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f68d34619f5f9cff2cfac13cfa06e31e832bf261751b75ee11561cd3375e0207`  
		Last Modified: Tue, 01 Dec 2020 07:27:26 GMT  
		Size: 8.4 KB (8446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6bf2c8a87f5c9551aa94f68cd8ea11b9fb2f222d8cd8cdaf96b58fe86c98897`  
		Last Modified: Tue, 01 Dec 2020 07:48:39 GMT  
		Size: 310.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f16b55f73f8f895e7f07bc76cbc0c40ed52e4032e2129a9dbf41c7cb907c9e`  
		Last Modified: Tue, 01 Dec 2020 07:48:37 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a4fbbf03b1e145da6329a1d517b4ddaafee96bc3623a9dea8fcf2d3b1309ce4`  
		Last Modified: Tue, 01 Dec 2020 07:48:38 GMT  
		Size: 4.3 MB (4321450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b75ee2a57910d59b9ac6cb6de554264966343ef9391893d44eaf344ebca1bdc`  
		Last Modified: Tue, 01 Dec 2020 07:48:38 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12530476c9fea755fef449d62308ae3022da470522b4598087fcd3eb5bf68f7d`  
		Last Modified: Tue, 08 Dec 2020 00:19:56 GMT  
		Size: 570.9 KB (570859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5723a03bb2a4c99d35468a1f3e68d687f33c81fdce68c56aac53b1c689b5542`  
		Last Modified: Tue, 08 Dec 2020 00:19:55 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; arm variant v6

```console
$ docker pull adminer@sha256:689204154221d2e4a097c834af056b991f880aed7a5a4a1e54d6c4422d965a6f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32149046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bb1805eba8cd29a4f28de65c3c539bac32ead0206c065984c55d1a699fd3b81`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 11 Dec 2020 02:17:15 GMT
ADD file:1a9c0a67560d338c0c0e7005d8915d998fc9cf3e9f53bfd7e42e8391f0a39bce in / 
# Fri, 11 Dec 2020 02:17:15 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 07:04:50 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 11 Dec 2020 07:04:53 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 11 Dec 2020 07:04:55 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 11 Dec 2020 07:04:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 11 Dec 2020 07:04:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 11 Dec 2020 07:09:12 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Fri, 11 Dec 2020 07:09:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Dec 2020 07:09:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Dec 2020 07:09:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 11 Dec 2020 07:17:56 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 11 Dec 2020 07:17:57 GMT
ENV PHP_VERSION=7.4.13
# Fri, 11 Dec 2020 07:17:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Fri, 11 Dec 2020 07:17:58 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Fri, 11 Dec 2020 07:18:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 11 Dec 2020 07:18:05 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Dec 2020 07:21:46 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Dec 2020 07:21:47 GMT
COPY multi:ebc915bbde1078ce3122b918e2e4c7726858af785343ade1a8d1a94f1052a4c7 in /usr/local/bin/ 
# Fri, 11 Dec 2020 07:21:51 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Dec 2020 07:21:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Dec 2020 07:21:53 GMT
WORKDIR /var/www/html
# Fri, 11 Dec 2020 07:21:56 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 11 Dec 2020 07:21:57 GMT
STOPSIGNAL SIGQUIT
# Fri, 11 Dec 2020 07:21:58 GMT
EXPOSE 9000
# Fri, 11 Dec 2020 07:21:59 GMT
CMD ["php-fpm"]
# Fri, 11 Dec 2020 09:05:35 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 11 Dec 2020 09:05:38 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 11 Dec 2020 09:06:36 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 11 Dec 2020 09:06:37 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 11 Dec 2020 09:06:38 GMT
ENV ADMINER_VERSION=4.7.8
# Fri, 11 Dec 2020 09:06:40 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Fri, 11 Dec 2020 09:06:41 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Fri, 11 Dec 2020 09:06:45 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 11 Dec 2020 09:06:46 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 11 Dec 2020 09:06:48 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 11 Dec 2020 09:06:50 GMT
USER adminer
# Fri, 11 Dec 2020 09:06:52 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:f1c16df8fee33d421d08790b17ca2af67a3fe49e77b6b991dd0c30631f5d1baf`  
		Last Modified: Fri, 11 Dec 2020 02:17:57 GMT  
		Size: 2.6 MB (2601992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623cc08cbe035cf15859e57a83e2243620418da06e1905d1875a46bec901e540`  
		Last Modified: Fri, 11 Dec 2020 07:56:49 GMT  
		Size: 1.3 MB (1310156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3a7aacff9b7ccf646f2bdbbc8d40bbb304550e813876049e721abd35461df9`  
		Last Modified: Fri, 11 Dec 2020 07:56:49 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d3214ea6f418597f370177309be7728f94481030c9cba6e45c4b74cfd04cc0`  
		Last Modified: Fri, 11 Dec 2020 07:56:49 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dff7159949c3c97335dda12e61ad77a87a4125ef93f88655500f4b8057cd38ca`  
		Last Modified: Fri, 11 Dec 2020 07:58:09 GMT  
		Size: 10.3 MB (10338600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c2c2f22a036ec3f2efaed4fd97c10faee4bbf539b56bf2e11b84a7c05b78fa`  
		Last Modified: Fri, 11 Dec 2020 07:58:05 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae33a5a224fa1ee298562bc31d50c9f804652bf619e4836e852c8860c5c49318`  
		Last Modified: Fri, 11 Dec 2020 07:58:09 GMT  
		Size: 13.3 MB (13267849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53c09a76a513338db42015101706a8bf9c7309d298d0a3329dee74810ea39db7`  
		Last Modified: Fri, 11 Dec 2020 07:58:05 GMT  
		Size: 2.3 KB (2260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e47c9c32a85f1170c19a3745c3a661a3a3c13e50daddef9919f624a52a70bc30`  
		Last Modified: Fri, 11 Dec 2020 07:58:05 GMT  
		Size: 16.9 KB (16891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbe39bbdfd22c5c467c010b89eb9561741273f56a2f378e08f2e055ef9ed919`  
		Last Modified: Fri, 11 Dec 2020 07:58:05 GMT  
		Size: 8.4 KB (8446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb3c1470d540138d5b667c3d6e30a34a3b783541ba0dc69a9714fa432a923970`  
		Last Modified: Fri, 11 Dec 2020 09:07:48 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f70879cf7eb8183ab6f68ad5f05f07b3e91a88ca27f7d935e91892073b1376`  
		Last Modified: Fri, 11 Dec 2020 09:07:46 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f69f96ec941427956045eb3c5673c21715d1878daf9035b7d11122c8cf62ed0c`  
		Last Modified: Fri, 11 Dec 2020 09:07:46 GMT  
		Size: 4.0 MB (4026251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a629622e0e5f22c28c625e3b6a9bef5d2136d403a64f88e8a44b1f1088caec2d`  
		Last Modified: Fri, 11 Dec 2020 09:07:45 GMT  
		Size: 1.5 KB (1470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec25251b0aa5ef178648ab40613c0031a55f133641f36b6c6e74dc5e79e4764`  
		Last Modified: Fri, 11 Dec 2020 09:07:46 GMT  
		Size: 570.9 KB (570918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71d17d806f1955405b240a9ef740c540c9e8ec5ceb8686ec081fda180677e50c`  
		Last Modified: Fri, 11 Dec 2020 09:07:45 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; arm variant v7

```console
$ docker pull adminer@sha256:226eabf37d80fa4c86dc5fd621ba0b5c211967752c3e972a3929b9ffc4f4387c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31261925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efcd4d51f3642b6795c4c7140eaab8183af5f3b781a9099b95e1eba7d94d5683`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 22 Oct 2020 01:58:13 GMT
ADD file:46f89172426e9f5b1d669a2ca7ab218fc2deaef1caeeab88f2b5bd443ac9773d in / 
# Thu, 22 Oct 2020 01:58:14 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 06:47:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 22 Oct 2020 06:47:37 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 22 Oct 2020 06:47:45 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 22 Oct 2020 06:47:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 22 Oct 2020 06:47:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 22 Oct 2020 06:51:33 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Thu, 22 Oct 2020 06:51:36 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 06:51:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 06:51:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 22 Oct 2020 07:01:44 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 01 Dec 2020 02:43:04 GMT
ENV PHP_VERSION=7.4.13
# Tue, 01 Dec 2020 02:43:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Tue, 01 Dec 2020 02:43:24 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Tue, 01 Dec 2020 02:43:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 01 Dec 2020 02:43:39 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 01 Dec 2020 02:46:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 01 Dec 2020 02:46:34 GMT
COPY multi:ebc915bbde1078ce3122b918e2e4c7726858af785343ade1a8d1a94f1052a4c7 in /usr/local/bin/ 
# Tue, 01 Dec 2020 02:46:37 GMT
RUN docker-php-ext-enable sodium
# Tue, 01 Dec 2020 02:46:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 01 Dec 2020 02:46:39 GMT
WORKDIR /var/www/html
# Tue, 01 Dec 2020 02:46:42 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Tue, 01 Dec 2020 02:46:44 GMT
STOPSIGNAL SIGQUIT
# Tue, 01 Dec 2020 02:46:45 GMT
EXPOSE 9000
# Tue, 01 Dec 2020 02:46:46 GMT
CMD ["php-fpm"]
# Tue, 01 Dec 2020 04:29:50 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Tue, 01 Dec 2020 04:29:56 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 01 Dec 2020 04:30:45 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Tue, 01 Dec 2020 04:30:48 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Tue, 08 Dec 2020 00:01:12 GMT
ENV ADMINER_VERSION=4.7.8
# Tue, 08 Dec 2020 00:01:13 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Tue, 08 Dec 2020 00:01:14 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Tue, 08 Dec 2020 00:01:18 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Tue, 08 Dec 2020 00:01:20 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 08 Dec 2020 00:01:24 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Tue, 08 Dec 2020 00:01:25 GMT
USER adminer
# Tue, 08 Dec 2020 00:01:26 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:5f2023fd85a4e68f37fe41421fd89f30e69b98a645613521c57c01317561eee3`  
		Last Modified: Thu, 22 Oct 2020 01:58:45 GMT  
		Size: 2.4 MB (2405675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60b50c98f8a8e2c6a27378dfa0f44df1844ac67c6981303675f138a42679f25`  
		Last Modified: Thu, 22 Oct 2020 07:35:57 GMT  
		Size: 1.2 MB (1214265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b472094d673b7c272085505c976192b9aaafa3157c99bade9755fbca18a24071`  
		Last Modified: Thu, 22 Oct 2020 07:35:56 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc39e5d916c11e7eb158e72d14ab981eb45ccc7b6451c1d6d3cb627b71cdbb6`  
		Last Modified: Thu, 22 Oct 2020 07:35:55 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad5979536683af238cd5c6e9e7ee5171a2f468ba42667525bcf73dfbd4442d5c`  
		Last Modified: Tue, 01 Dec 2020 04:01:12 GMT  
		Size: 10.3 MB (10338579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83bfa48b04ad972c7ddc62f60703fd345236339c894ee5e02487d0a6912eec44`  
		Last Modified: Tue, 01 Dec 2020 04:01:08 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d500723729ab98b41c43300141cf87ecedf3122e848cb7f2871a8a18b472c9`  
		Last Modified: Tue, 01 Dec 2020 04:01:12 GMT  
		Size: 12.8 MB (12773054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ffe3faddffbb23fc7ec2b0ac5897aa6700b295f1129a52a58322108a7d7146`  
		Last Modified: Tue, 01 Dec 2020 04:01:08 GMT  
		Size: 2.3 KB (2260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c6599d32683be6cd2106e34a046a0a556bffd2baac97299eb69df7408f682be`  
		Last Modified: Tue, 01 Dec 2020 04:01:08 GMT  
		Size: 16.9 KB (16903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7158f5b17b11ddb8f243be54e5fc6112f6017d46780577a568a72e2e7d3f2cb1`  
		Last Modified: Tue, 01 Dec 2020 04:01:08 GMT  
		Size: 8.4 KB (8446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba8645bc546fe074d817500743f03a6b6b287793cee19306e5267095e410e7e`  
		Last Modified: Tue, 01 Dec 2020 04:32:00 GMT  
		Size: 310.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae84262bbd09928c80ab09696b0c7d2d57c5b58e28e089d2be9aae62bd0c7d0e`  
		Last Modified: Tue, 01 Dec 2020 04:31:59 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d45b8aa81cac48a3b6f2953fa3ad9d6047d134f7b76cbb3e05cbde0d6e0c7fc1`  
		Last Modified: Tue, 01 Dec 2020 04:31:59 GMT  
		Size: 3.9 MB (3926120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b483e9859bacb3a5557c81eda83e17a2559203c0979dcdd57bdcbe5729404c0f`  
		Last Modified: Tue, 01 Dec 2020 04:31:58 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7022a91847b0aaf7d1e067b9c3fa7620f93f349b64d2d7ebe0e816598a47fed2`  
		Last Modified: Tue, 08 Dec 2020 00:01:58 GMT  
		Size: 570.9 KB (570923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562e2ad43a7b07e5427acd85e75ec18c9dc4b21fe0a10fac08b447cfa140187f`  
		Last Modified: Tue, 08 Dec 2020 00:01:58 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:89498585a4df7bcfaecdaadf8bee7b0b21018e861c1357c5826273c129cea8c1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.8 MB (33782483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57bc4d4eb9fffe27cb455d6f0c04677fd0798704e2673ac9c281b492fa593f03`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 07:18:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 22 Oct 2020 07:18:56 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 22 Oct 2020 07:18:59 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 22 Oct 2020 07:19:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 22 Oct 2020 07:19:04 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 22 Oct 2020 07:23:16 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Thu, 22 Oct 2020 07:23:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 07:23:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 07:23:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 22 Oct 2020 07:32:38 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 01 Dec 2020 03:31:07 GMT
ENV PHP_VERSION=7.4.13
# Tue, 01 Dec 2020 03:31:08 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Tue, 01 Dec 2020 03:31:09 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Tue, 01 Dec 2020 03:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 01 Dec 2020 03:31:15 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 01 Dec 2020 03:34:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 01 Dec 2020 03:35:01 GMT
COPY multi:ebc915bbde1078ce3122b918e2e4c7726858af785343ade1a8d1a94f1052a4c7 in /usr/local/bin/ 
# Tue, 01 Dec 2020 03:35:06 GMT
RUN docker-php-ext-enable sodium
# Tue, 01 Dec 2020 03:35:06 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 01 Dec 2020 03:35:08 GMT
WORKDIR /var/www/html
# Tue, 01 Dec 2020 03:35:10 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Tue, 01 Dec 2020 03:35:11 GMT
STOPSIGNAL SIGQUIT
# Tue, 01 Dec 2020 03:35:12 GMT
EXPOSE 9000
# Tue, 01 Dec 2020 03:35:13 GMT
CMD ["php-fpm"]
# Tue, 01 Dec 2020 08:13:43 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Tue, 01 Dec 2020 08:13:46 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 01 Dec 2020 08:14:29 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Tue, 01 Dec 2020 08:14:30 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Mon, 07 Dec 2020 23:40:07 GMT
ENV ADMINER_VERSION=4.7.8
# Mon, 07 Dec 2020 23:40:07 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Mon, 07 Dec 2020 23:40:08 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Mon, 07 Dec 2020 23:40:11 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Mon, 07 Dec 2020 23:40:12 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Mon, 07 Dec 2020 23:40:13 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Mon, 07 Dec 2020 23:40:14 GMT
USER adminer
# Mon, 07 Dec 2020 23:40:15 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d57dba23203172f8fffd1379aef0307e782178b62dfc684d43c546f7e874ed`  
		Last Modified: Thu, 22 Oct 2020 08:06:21 GMT  
		Size: 1.3 MB (1342784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8414edb0c9c2f7472bb6228bf691a2ddac19ddad7bad789c7cbdc147aded711`  
		Last Modified: Thu, 22 Oct 2020 08:06:20 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d26eeef0db35b2328adae38a8490c7403844452c3606dd17fbe68216f98e82`  
		Last Modified: Thu, 22 Oct 2020 08:06:19 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b747a72bda51ef2a52afed0eef10b56786e7c76ab30913f0e650a83b66935e4f`  
		Last Modified: Tue, 01 Dec 2020 04:54:24 GMT  
		Size: 10.3 MB (10338600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c684293922e5efaae5d67a6b158f6e54284e91081dda97b306a74ce97c9d0738`  
		Last Modified: Tue, 01 Dec 2020 04:54:21 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acdf0cad2cf9d86164e334858db58328dc251f08abe9d0841cc1bf520748163e`  
		Last Modified: Tue, 01 Dec 2020 04:54:25 GMT  
		Size: 14.5 MB (14458713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3417ec8fcb1bd4b4d3f295b89316912d8e33667e645450c3d0a2694887fea5da`  
		Last Modified: Tue, 01 Dec 2020 04:54:21 GMT  
		Size: 2.3 KB (2256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96e2c572c8bf97a5e221afc68cec20acaad7e29b919f242c6cb085234693b08`  
		Last Modified: Tue, 01 Dec 2020 04:54:22 GMT  
		Size: 17.0 KB (16978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:732bd773818e9fef29ad5ba55c5ddd1638077be22b0fd0a8f3a8bee4b600da11`  
		Last Modified: Tue, 01 Dec 2020 04:54:21 GMT  
		Size: 8.4 KB (8444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1886aa9fc4a1ad175dc4689b2f38537f04a005774f1c34b08ae3b8c3158fe5f8`  
		Last Modified: Tue, 01 Dec 2020 08:15:16 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf4e7f82086c970c52f8f544137e3286e990df9f19ad8567bba476226b12f61`  
		Last Modified: Tue, 01 Dec 2020 08:15:15 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4acc32056dfd0cd70bbc78cdfb34f2c627a433caff773366ad168a4945db066`  
		Last Modified: Tue, 01 Dec 2020 08:15:15 GMT  
		Size: 4.3 MB (4331531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb34a16b4bdb5625d39f3ef20da17bfecf2156cf9f3a647b4c4c26497af56b7`  
		Last Modified: Tue, 01 Dec 2020 08:15:15 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857d9231bfb81ba8cc071fbdcccdb6f9189f8e56d09ce9396b85b4e88b412b53`  
		Last Modified: Mon, 07 Dec 2020 23:40:43 GMT  
		Size: 570.9 KB (570920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a854be7b56f0667067e2d5d43ed47f9f068cb0e3f7976910fb604dda911121db`  
		Last Modified: Mon, 07 Dec 2020 23:40:43 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; 386

```console
$ docker pull adminer@sha256:4f5fe39f0929ce4ac634729677768b268b328437e602e5a286881bb683086a5f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34705084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c8aa440257abba5e8b17a4be7767c0c3b8fc17f455e445f561495f8d394f849`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 22 Oct 2020 02:00:33 GMT
ADD file:46ad43b4984bcf49c5a888ff3628f23161f55cd1fb062f469e707100c97fa254 in / 
# Thu, 22 Oct 2020 02:00:33 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:36:23 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 22 Oct 2020 03:36:26 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 22 Oct 2020 03:36:27 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 22 Oct 2020 03:36:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 22 Oct 2020 03:36:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 22 Oct 2020 03:45:17 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Thu, 22 Oct 2020 03:45:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 03:45:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 03:45:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 22 Oct 2020 04:01:27 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 01 Dec 2020 04:11:03 GMT
ENV PHP_VERSION=7.4.13
# Tue, 01 Dec 2020 04:11:04 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Tue, 01 Dec 2020 04:11:04 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Tue, 01 Dec 2020 04:11:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 01 Dec 2020 04:11:13 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 01 Dec 2020 04:19:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 01 Dec 2020 04:19:54 GMT
COPY multi:ebc915bbde1078ce3122b918e2e4c7726858af785343ade1a8d1a94f1052a4c7 in /usr/local/bin/ 
# Tue, 01 Dec 2020 04:19:56 GMT
RUN docker-php-ext-enable sodium
# Tue, 01 Dec 2020 04:19:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 01 Dec 2020 04:19:56 GMT
WORKDIR /var/www/html
# Tue, 01 Dec 2020 04:19:57 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Tue, 01 Dec 2020 04:19:57 GMT
STOPSIGNAL SIGQUIT
# Tue, 01 Dec 2020 04:19:58 GMT
EXPOSE 9000
# Tue, 01 Dec 2020 04:19:58 GMT
CMD ["php-fpm"]
# Tue, 01 Dec 2020 09:25:25 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Tue, 01 Dec 2020 09:25:26 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 01 Dec 2020 09:25:53 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Tue, 01 Dec 2020 09:25:54 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Mon, 07 Dec 2020 23:38:31 GMT
ENV ADMINER_VERSION=4.7.8
# Mon, 07 Dec 2020 23:38:32 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Mon, 07 Dec 2020 23:38:32 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Mon, 07 Dec 2020 23:38:33 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Mon, 07 Dec 2020 23:38:33 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Mon, 07 Dec 2020 23:38:33 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Mon, 07 Dec 2020 23:38:34 GMT
USER adminer
# Mon, 07 Dec 2020 23:38:34 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:d6ca64ac6f4b6382142ce9a3501652938130a6ec4bb02f3f455ee1f980834cfe`  
		Last Modified: Thu, 22 Oct 2020 02:00:57 GMT  
		Size: 2.8 MB (2791407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30be8ffd290910905a5fb7cbb70252eb0f59edb09db20bdc21f3b65456acc28f`  
		Last Modified: Thu, 22 Oct 2020 05:10:23 GMT  
		Size: 1.4 MB (1439641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d58e2433b13446c863e85b34f8e4c93ca9d5b3b93d2bac415fd9cdf77bcec4`  
		Last Modified: Thu, 22 Oct 2020 05:10:21 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5729dcb8d303f82a7f8cf3df49048e34ce8ee89f79155fb08a475da46b64308`  
		Last Modified: Thu, 22 Oct 2020 05:10:21 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73c975f14cba63719b1acf30eb48c56e9ff5ab3ba3c93cc300551ed40f30ac4`  
		Last Modified: Tue, 01 Dec 2020 07:15:32 GMT  
		Size: 10.3 MB (10338565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8926789263a06364cefc6d6aee50b84a30291d014d2029ca669cb556f4c2bb1`  
		Last Modified: Tue, 01 Dec 2020 07:15:30 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcbe8e9cc07ddaae06ed92974d6d0a5249cac41ebb54331b56fc5c9e240eb993`  
		Last Modified: Tue, 01 Dec 2020 07:15:35 GMT  
		Size: 15.0 MB (15012323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e40c7a669cd74ab9dc3e2874416646f823f63c10d9b9a952a55dc1ad5bac9d`  
		Last Modified: Tue, 01 Dec 2020 07:15:30 GMT  
		Size: 2.3 KB (2260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed001fb8127577a70da6914dcf10ccb5d90ed9cf2a1cd3272618748f6b111d03`  
		Last Modified: Tue, 01 Dec 2020 07:15:29 GMT  
		Size: 16.9 KB (16920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90867a60ecf180a61e2ada4f0842adc2c2e44685c28753a5bed45de997db01e7`  
		Last Modified: Tue, 01 Dec 2020 07:15:29 GMT  
		Size: 8.4 KB (8442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3ce5df361365526e71aaf6df13804b7dedc099dd67740782cc739e0613eb110`  
		Last Modified: Tue, 01 Dec 2020 09:26:27 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a789bbdaebdf4bde2f5038d3a2a626522e4b2edc239b954288d23175ee69042`  
		Last Modified: Tue, 01 Dec 2020 09:26:26 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a79d0d02c93a44d0f6d1145f6ae0a0333e71fe94bfa8c63bd24354761d9587`  
		Last Modified: Tue, 01 Dec 2020 09:26:27 GMT  
		Size: 4.5 MB (4519093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85c74143366ffd582b27ed81dd1f35e4e314799a0de720b613b98b88ce787c77`  
		Last Modified: Tue, 01 Dec 2020 09:26:25 GMT  
		Size: 1.5 KB (1472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3529b652f01c65456c39d33fd9d239949548a0442b8a1fa9d2bf0a1c1f74b968`  
		Last Modified: Mon, 07 Dec 2020 23:38:54 GMT  
		Size: 570.9 KB (570861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a79e9613d8243f31a29bb14c13abf1a73d577720e86547b01bdef2bf8f9296bd`  
		Last Modified: Mon, 07 Dec 2020 23:38:54 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; ppc64le

```console
$ docker pull adminer@sha256:0671ac686df177a55af6924323ebcc05a17cb4bf61a6372df21a1a0c22487346
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.1 MB (35117996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:959c6c5b577d14c45504ecdd9a75e110b1afb1e5e8651a224075e4784c97c07c`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 22 Oct 2020 11:00:06 GMT
ADD file:176e047fab2c1828575bffa6b14773efa297b7ecf312d86103c5dd4f78ec8027 in / 
# Thu, 22 Oct 2020 11:00:17 GMT
CMD ["/bin/sh"]
# Fri, 23 Oct 2020 00:21:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 23 Oct 2020 00:21:18 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 23 Oct 2020 00:21:30 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 23 Oct 2020 00:21:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 23 Oct 2020 00:21:44 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 23 Oct 2020 00:27:50 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Fri, 23 Oct 2020 00:27:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 23 Oct 2020 00:28:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 23 Oct 2020 00:28:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 23 Oct 2020 00:39:53 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 01 Dec 2020 03:57:52 GMT
ENV PHP_VERSION=7.4.13
# Tue, 01 Dec 2020 03:57:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Tue, 01 Dec 2020 03:58:02 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Tue, 01 Dec 2020 03:58:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 01 Dec 2020 03:58:37 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 01 Dec 2020 04:02:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 01 Dec 2020 04:02:41 GMT
COPY multi:ebc915bbde1078ce3122b918e2e4c7726858af785343ade1a8d1a94f1052a4c7 in /usr/local/bin/ 
# Tue, 01 Dec 2020 04:02:55 GMT
RUN docker-php-ext-enable sodium
# Tue, 01 Dec 2020 04:02:59 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 01 Dec 2020 04:03:05 GMT
WORKDIR /var/www/html
# Tue, 01 Dec 2020 04:03:27 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Tue, 01 Dec 2020 04:03:33 GMT
STOPSIGNAL SIGQUIT
# Tue, 01 Dec 2020 04:03:40 GMT
EXPOSE 9000
# Tue, 01 Dec 2020 04:03:44 GMT
CMD ["php-fpm"]
# Tue, 01 Dec 2020 07:11:43 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Tue, 01 Dec 2020 07:11:59 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 01 Dec 2020 07:12:55 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Tue, 01 Dec 2020 07:12:59 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Tue, 08 Dec 2020 00:17:37 GMT
ENV ADMINER_VERSION=4.7.8
# Tue, 08 Dec 2020 00:17:44 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Tue, 08 Dec 2020 00:17:47 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Tue, 08 Dec 2020 00:17:56 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Tue, 08 Dec 2020 00:17:59 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 08 Dec 2020 00:18:03 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Tue, 08 Dec 2020 00:18:08 GMT
USER adminer
# Tue, 08 Dec 2020 00:18:15 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:692a9d763e196c85d79fc3e45b316b1bb557c93ba88a3c8ebf679a585d1efe73`  
		Last Modified: Thu, 22 Oct 2020 11:02:06 GMT  
		Size: 2.8 MB (2803218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0285d6f06f3beb1c140c055210664c441b93dd4f2037177a5396bce94ca16ce5`  
		Last Modified: Fri, 23 Oct 2020 01:34:08 GMT  
		Size: 1.4 MB (1383187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a6459a3bf272daa53ff4ba97cc849676f497de9f78d8e9378ec02552293f175`  
		Last Modified: Fri, 23 Oct 2020 01:34:07 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16cff6064dc29d3f629d353736c1cac074caa5b50738422adb84de99a019bb32`  
		Last Modified: Fri, 23 Oct 2020 01:34:08 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67dcc2a717f8153769df04bd895be154aca7c3fc20560f37da5b36e0fbd9efbd`  
		Last Modified: Tue, 01 Dec 2020 05:51:15 GMT  
		Size: 10.3 MB (10338603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9502fa9f26f9855ddcfd4309edb7c16ce7517f1c88a60155b169e6182acbdd17`  
		Last Modified: Tue, 01 Dec 2020 05:51:09 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf065529921adbb64e6889d9cfa225de7f8aa65204f3ec400330d4fc989de4d8`  
		Last Modified: Tue, 01 Dec 2020 05:51:13 GMT  
		Size: 15.6 MB (15628567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e91de5593ec1aa89d021215583d63f94d4f36d9608f29dd460ede4c7290ebb7`  
		Last Modified: Tue, 01 Dec 2020 05:51:09 GMT  
		Size: 2.3 KB (2255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede5b0209a637a8111ae77c919a561733c6e703c97333ecea99a4abbecf8a2c5`  
		Last Modified: Tue, 01 Dec 2020 05:51:09 GMT  
		Size: 17.0 KB (16968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e851350ac3fff1de99c14298cb35f46c409629186a85f22c22a0be19f4f7cd`  
		Last Modified: Tue, 01 Dec 2020 05:51:09 GMT  
		Size: 8.4 KB (8441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df2bf3b8e2936ee1044358dfd1700fce3f08592b60bac9086d1d4677f3de8ca9`  
		Last Modified: Tue, 01 Dec 2020 07:15:16 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bcb7b3aa24f4c386111b1860808ec662939186fbbf6ea9be1a4309880e34a17`  
		Last Modified: Tue, 01 Dec 2020 07:15:13 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:088e76bc30b441c5832343aa548abe6c770bd754156485a0b235f1cf92cac64e`  
		Last Modified: Tue, 01 Dec 2020 07:15:14 GMT  
		Size: 4.4 MB (4360124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:587c025ae0482b8d3b5e8fc26b4af5eae6dc22c5c3da95ca52fbfc9c9a5b2f3a`  
		Last Modified: Tue, 01 Dec 2020 07:15:12 GMT  
		Size: 1.5 KB (1479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45314773dc31f89543794af67d864efadc99ec57ce116a3760d41a4c207f6f30`  
		Last Modified: Tue, 08 Dec 2020 00:19:11 GMT  
		Size: 570.9 KB (570925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4283c4537d91df6ad82cb299758a89bc3a5d2a8f42ddfe40ea81b189e8d6fb0`  
		Last Modified: Tue, 08 Dec 2020 00:19:11 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; s390x

```console
$ docker pull adminer@sha256:1f93751408862e70ce3d4b81bd3d7bdb4e2ecac81606992543e7bbfdbf90f96b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32598207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9061e3e2134cb0ffa169546bbf7624fe55bbea5f40e1b70016744979434fcc7d`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 11 Dec 2020 02:09:52 GMT
ADD file:c9395a36a4e03768aabd282eb1f31705cc00181d3147222d9c940eaa5a8fd511 in / 
# Fri, 11 Dec 2020 02:09:53 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 11:30:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 11 Dec 2020 11:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 11 Dec 2020 11:30:56 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 11 Dec 2020 11:30:57 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 11 Dec 2020 11:30:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 11 Dec 2020 11:36:17 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Fri, 11 Dec 2020 11:36:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Dec 2020 11:36:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Dec 2020 11:36:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 11 Dec 2020 12:09:03 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 11 Dec 2020 12:09:04 GMT
ENV PHP_VERSION=7.4.13
# Fri, 11 Dec 2020 12:09:04 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Fri, 11 Dec 2020 12:09:05 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Fri, 11 Dec 2020 12:09:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 11 Dec 2020 12:09:12 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Dec 2020 12:13:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Dec 2020 12:13:55 GMT
COPY multi:ebc915bbde1078ce3122b918e2e4c7726858af785343ade1a8d1a94f1052a4c7 in /usr/local/bin/ 
# Fri, 11 Dec 2020 12:13:57 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Dec 2020 12:13:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Dec 2020 12:13:59 GMT
WORKDIR /var/www/html
# Fri, 11 Dec 2020 12:14:00 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 11 Dec 2020 12:14:01 GMT
STOPSIGNAL SIGQUIT
# Fri, 11 Dec 2020 12:14:01 GMT
EXPOSE 9000
# Fri, 11 Dec 2020 12:14:02 GMT
CMD ["php-fpm"]
# Fri, 11 Dec 2020 18:45:19 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 11 Dec 2020 18:45:21 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 11 Dec 2020 18:46:30 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 11 Dec 2020 18:46:31 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 11 Dec 2020 18:46:32 GMT
ENV ADMINER_VERSION=4.7.8
# Fri, 11 Dec 2020 18:46:32 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Fri, 11 Dec 2020 18:46:33 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Fri, 11 Dec 2020 18:46:36 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 11 Dec 2020 18:46:37 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 11 Dec 2020 18:46:38 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 11 Dec 2020 18:46:38 GMT
USER adminer
# Fri, 11 Dec 2020 18:46:39 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:7c2470fe3d16cb70fca0826168095a96838b1322a8cd1502b28284ee8561b491`  
		Last Modified: Fri, 11 Dec 2020 02:10:27 GMT  
		Size: 2.6 MB (2565988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a23c8359d30ae261ad953f292e6681a71ebc7388607b74d901bbc07f71e1311`  
		Last Modified: Fri, 11 Dec 2020 13:48:01 GMT  
		Size: 1.4 MB (1382587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01422c3e898d3241d4134256bf0d911b0752823227af04614187c79c187e2843`  
		Last Modified: Fri, 11 Dec 2020 13:48:03 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a0be2077abd44f96e50bdebb1ed93a6e2b8d504761c23fa0e5e9b87045ca38`  
		Last Modified: Fri, 11 Dec 2020 13:48:01 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:797fc05bf988e85a5cf643f2d07a0b08a36e3f1529c75c41a2460041b6ee0f43`  
		Last Modified: Fri, 11 Dec 2020 13:50:52 GMT  
		Size: 10.3 MB (10338591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e11bb5dc7804a50c805852fbe653bb133478f5005e8c78c1d712af0d5bd6db4`  
		Last Modified: Fri, 11 Dec 2020 13:50:49 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:311bfe9de08521ea35d7a1520e00de8215315e5a8144a4335f1313ad7f6593de`  
		Last Modified: Fri, 11 Dec 2020 13:50:51 GMT  
		Size: 13.6 MB (13553700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59a788dffbadef519f959d8de10a3156add64ed4e15c8e96045a3bebf9ef316`  
		Last Modified: Fri, 11 Dec 2020 13:50:49 GMT  
		Size: 2.3 KB (2260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:898ee507348c01a8028e7ad08c8af3edde13cd884ffdfd990ad679df9b004552`  
		Last Modified: Fri, 11 Dec 2020 13:50:49 GMT  
		Size: 16.9 KB (16883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a7bec784d5537500a8f385256905e367037e6e1ae365f119cf3a305c384338f`  
		Last Modified: Fri, 11 Dec 2020 13:50:50 GMT  
		Size: 8.4 KB (8445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aacad6fcb4ce89b6aebc70fa08e0aeaf4004bdfd4288064a050ae7a6b6a1ca5`  
		Last Modified: Fri, 11 Dec 2020 18:47:37 GMT  
		Size: 310.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed17bffefe5fed1ad7e5ba183155f268ef4c6f19e11ce2b4d2b51a756f56e38`  
		Last Modified: Fri, 11 Dec 2020 18:47:32 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:195c8eb0f725b2189839adb7a0fec2e91f3b597dcf7a9a35cdb3cde9beea8e03`  
		Last Modified: Fri, 11 Dec 2020 18:47:33 GMT  
		Size: 4.2 MB (4153144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dd4956eb56581838eebbd42956889e3cc9dd1e7526a1282b8075c4c7daf28d1`  
		Last Modified: Fri, 11 Dec 2020 18:47:33 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a7b5a1b8dcaeb2cdc7acda96210109729ec955718cf8d30f683176a9ecf87be`  
		Last Modified: Fri, 11 Dec 2020 18:47:32 GMT  
		Size: 570.9 KB (570919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a3464ffffa7b21ee6c5a53d2f9143c982205d77f77a55bf9ec4ebb2cdff801`  
		Last Modified: Fri, 11 Dec 2020 18:47:33 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:latest`

```console
$ docker pull adminer@sha256:4600f2453f7c9f3ee8179016a65d0b49a8dfb89467ac0947a6245e62e7f81fb1
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

### `adminer:latest` - linux; amd64

```console
$ docker pull adminer@sha256:4b087576de7b4ca7c60bb3558f0b5ee30f496cee10fa19ea0a9f0e071c72b1f5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (33965375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2db7241b0f1461d8707525832e608fe513453f99c11beed9413194f7519e05`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 06:30:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 22 Oct 2020 06:30:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 22 Oct 2020 06:30:15 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 22 Oct 2020 06:30:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 22 Oct 2020 06:30:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 22 Oct 2020 06:30:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 06:30:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 06:30:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 22 Oct 2020 06:43:41 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 01 Dec 2020 04:36:20 GMT
ENV PHP_VERSION=7.4.13
# Tue, 01 Dec 2020 04:36:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Tue, 01 Dec 2020 04:36:21 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Tue, 01 Dec 2020 04:36:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 01 Dec 2020 04:36:27 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 01 Dec 2020 04:44:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 01 Dec 2020 04:44:54 GMT
COPY multi:afab483600631d4d87fe030871bbb016f1c2b73c0b72609d857bace419af7f5d in /usr/local/bin/ 
# Tue, 01 Dec 2020 04:44:57 GMT
RUN docker-php-ext-enable sodium
# Tue, 01 Dec 2020 04:44:57 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 01 Dec 2020 04:44:57 GMT
CMD ["php" "-a"]
# Tue, 01 Dec 2020 07:46:46 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Tue, 01 Dec 2020 07:46:46 GMT
STOPSIGNAL SIGINT
# Tue, 01 Dec 2020 07:46:47 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 01 Dec 2020 07:46:48 GMT
WORKDIR /var/www/html
# Tue, 01 Dec 2020 07:47:15 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Tue, 01 Dec 2020 07:47:15 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Tue, 08 Dec 2020 00:19:24 GMT
ENV ADMINER_VERSION=4.7.8
# Tue, 08 Dec 2020 00:19:24 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Tue, 08 Dec 2020 00:19:24 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Tue, 08 Dec 2020 00:19:26 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Tue, 08 Dec 2020 00:19:26 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 08 Dec 2020 00:19:26 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Tue, 08 Dec 2020 00:19:26 GMT
USER adminer
# Tue, 08 Dec 2020 00:19:27 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 08 Dec 2020 00:19:27 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f8bf6cfdbe614fef94f982905079c16e27b3de2d24eb1ff513d3d83e656ca2`  
		Last Modified: Thu, 22 Oct 2020 07:36:55 GMT  
		Size: 1.3 MB (1340771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce5be79740125b9e74a77885bf6ee2b0d25ac7ed9e9432c5aa7210bb3b00458a`  
		Last Modified: Thu, 22 Oct 2020 07:36:55 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99dd6507fe563b66ba35badf706e1bbb2d39eb5d0a3c0d5a86a45d2af7e89c1`  
		Last Modified: Thu, 22 Oct 2020 07:36:55 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c513a1b503cf7c9f18fa014dada9744070ded92dc9ad548cd056c4f56dc1a9`  
		Last Modified: Tue, 01 Dec 2020 07:27:10 GMT  
		Size: 10.3 MB (10338569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff080eafb4c0518981fca6aef4d239863fc59195f41ce7c440b2c6c518f2ac79`  
		Last Modified: Tue, 01 Dec 2020 07:27:09 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e818119992b11dbf09b710066a78920985b9ea1310fc8272df816e0884985f44`  
		Last Modified: Tue, 01 Dec 2020 07:27:13 GMT  
		Size: 14.6 MB (14572037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba3c14a67f95ae52ebfb558ab6b5d87687a05ce41c8df0a618ff42b73204e40`  
		Last Modified: Tue, 01 Dec 2020 07:27:09 GMT  
		Size: 2.3 KB (2257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbb0285b7ad2b170e4ed2cffbe0f16ba55d689c056ff43767834783eab7b8261`  
		Last Modified: Tue, 01 Dec 2020 07:27:09 GMT  
		Size: 17.0 KB (16987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae324cfad8acf03b3a98a15e963b7046404a7da3a6bbf68fd65d37f899f194d`  
		Last Modified: Tue, 01 Dec 2020 07:48:25 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb51158f683d66315de6fa572f7ea13d8ffb71ac85faa20c8578edb11678f37d`  
		Last Modified: Tue, 01 Dec 2020 07:48:23 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71ac21b64d1d63d967acb13664404babd0ef86fc896c484ce28cccf70001d0f1`  
		Last Modified: Tue, 01 Dec 2020 07:48:24 GMT  
		Size: 4.3 MB (4321455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2170e09d39d861e9bb7a5da5def906b44153b6c481fe17925ba82d1f1f78eec`  
		Last Modified: Tue, 01 Dec 2020 07:48:24 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d95b48dfa11f7f5c061f6522f6ff5d574452b8f321c6075455da2643b1967a`  
		Last Modified: Tue, 08 Dec 2020 00:19:45 GMT  
		Size: 570.9 KB (570860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3bb2b5e72bf0dbd4b855ddf65aaf9c0d077703804bdbdc9ea3ea98cbbfceaf6`  
		Last Modified: Tue, 08 Dec 2020 00:19:44 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; arm variant v6

```console
$ docker pull adminer@sha256:7e114494e5e3a8ece382083d27c33f6c993695f0ff6c92c235ced149177f5da9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32073857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9cfa5ccbab063435267257cf4c761402c956233cf22775ed1c774b53a045715`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 11 Dec 2020 02:17:15 GMT
ADD file:1a9c0a67560d338c0c0e7005d8915d998fc9cf3e9f53bfd7e42e8391f0a39bce in / 
# Fri, 11 Dec 2020 02:17:15 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 07:04:50 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 11 Dec 2020 07:04:53 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 11 Dec 2020 07:04:55 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 11 Dec 2020 07:04:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 11 Dec 2020 07:04:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 11 Dec 2020 07:05:00 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Dec 2020 07:05:01 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Dec 2020 07:05:02 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 11 Dec 2020 07:13:50 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 11 Dec 2020 07:13:54 GMT
ENV PHP_VERSION=7.4.13
# Fri, 11 Dec 2020 07:13:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Fri, 11 Dec 2020 07:13:56 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Fri, 11 Dec 2020 07:14:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 11 Dec 2020 07:14:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Dec 2020 07:17:37 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Dec 2020 07:17:39 GMT
COPY multi:afab483600631d4d87fe030871bbb016f1c2b73c0b72609d857bace419af7f5d in /usr/local/bin/ 
# Fri, 11 Dec 2020 07:17:42 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Dec 2020 07:17:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Dec 2020 07:17:43 GMT
CMD ["php" "-a"]
# Fri, 11 Dec 2020 09:04:18 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 11 Dec 2020 09:04:19 GMT
STOPSIGNAL SIGINT
# Fri, 11 Dec 2020 09:04:21 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 11 Dec 2020 09:04:22 GMT
WORKDIR /var/www/html
# Fri, 11 Dec 2020 09:05:06 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 11 Dec 2020 09:05:08 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 11 Dec 2020 09:05:08 GMT
ENV ADMINER_VERSION=4.7.8
# Fri, 11 Dec 2020 09:05:09 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Fri, 11 Dec 2020 09:05:11 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Fri, 11 Dec 2020 09:05:14 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 11 Dec 2020 09:05:15 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 11 Dec 2020 09:05:16 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 11 Dec 2020 09:05:17 GMT
USER adminer
# Fri, 11 Dec 2020 09:05:18 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 11 Dec 2020 09:05:19 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:f1c16df8fee33d421d08790b17ca2af67a3fe49e77b6b991dd0c30631f5d1baf`  
		Last Modified: Fri, 11 Dec 2020 02:17:57 GMT  
		Size: 2.6 MB (2601992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623cc08cbe035cf15859e57a83e2243620418da06e1905d1875a46bec901e540`  
		Last Modified: Fri, 11 Dec 2020 07:56:49 GMT  
		Size: 1.3 MB (1310156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3a7aacff9b7ccf646f2bdbbc8d40bbb304550e813876049e721abd35461df9`  
		Last Modified: Fri, 11 Dec 2020 07:56:49 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d3214ea6f418597f370177309be7728f94481030c9cba6e45c4b74cfd04cc0`  
		Last Modified: Fri, 11 Dec 2020 07:56:49 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64de18534c9c3dd7212eceb5a285d571df578238ca4684a2e922b131e9947d79`  
		Last Modified: Fri, 11 Dec 2020 07:57:40 GMT  
		Size: 10.3 MB (10338603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d60b5c1c75b96676e4154f74a500fdd4a2645d4c51e189b0bdd18e06f26c3143`  
		Last Modified: Fri, 11 Dec 2020 07:57:39 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee32c3be90bc13cb4b3406c492ec35d5c211ac42b25e536939fb3220aea672b`  
		Last Modified: Fri, 11 Dec 2020 07:57:44 GMT  
		Size: 13.2 MB (13201116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e71cdda7d8acfe2fe1a6263c1b004b3ae972d7ce1c0ac95fec09aa0c0ba1f7fd`  
		Last Modified: Fri, 11 Dec 2020 07:57:39 GMT  
		Size: 2.3 KB (2258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec74a6ee1beba601eed5abe261394c8ddfa2d53093a1f6768356ec5891066746`  
		Last Modified: Fri, 11 Dec 2020 07:57:40 GMT  
		Size: 16.9 KB (16889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b84bf5ad218839b4e8156c322c5611b3c26167141a7c1e8049055deeda8b1ed5`  
		Last Modified: Fri, 11 Dec 2020 09:07:23 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0113ef6e65685219488d6543639cff152292617519f4649a6d7c8e4bbf03322b`  
		Last Modified: Fri, 11 Dec 2020 09:07:21 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2501c821a30d874046f30dd9d3947aa9f82cca3e9d39eb18214a765744e0b24`  
		Last Modified: Fri, 11 Dec 2020 09:07:21 GMT  
		Size: 4.0 MB (4026242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:945b172c5cf67a28a59e5b25cfed08871f360f551a912c8d7f64c096d6554812`  
		Last Modified: Fri, 11 Dec 2020 09:07:20 GMT  
		Size: 1.5 KB (1473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df40a3aa85441cb471ce645d5a0a2564fb9e2f042e078b8f04dd343488863a4`  
		Last Modified: Fri, 11 Dec 2020 09:07:20 GMT  
		Size: 570.9 KB (570917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90644dda17e22024741efd92b2987150a52659ae6bb25b7ea232e9b72d3b1d83`  
		Last Modified: Fri, 11 Dec 2020 09:07:20 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; arm variant v7

```console
$ docker pull adminer@sha256:39b988e9485b8f06142e8584a4764c3c32159d51377eab0739b1cf794f701d1a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31186995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d4ed3310dfe2d29dd9a809a5ea826952ac518c5d93ab5e12054d9b7560791f7`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 22 Oct 2020 01:58:13 GMT
ADD file:46f89172426e9f5b1d669a2ca7ab218fc2deaef1caeeab88f2b5bd443ac9773d in / 
# Thu, 22 Oct 2020 01:58:14 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 06:47:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 22 Oct 2020 06:47:37 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 22 Oct 2020 06:47:45 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 22 Oct 2020 06:47:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 22 Oct 2020 06:47:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 22 Oct 2020 06:47:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 06:47:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 06:48:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 22 Oct 2020 06:56:26 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 01 Dec 2020 02:39:45 GMT
ENV PHP_VERSION=7.4.13
# Tue, 01 Dec 2020 02:39:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Tue, 01 Dec 2020 02:39:46 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Tue, 01 Dec 2020 02:39:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 01 Dec 2020 02:39:53 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 01 Dec 2020 02:42:30 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 01 Dec 2020 02:42:32 GMT
COPY multi:afab483600631d4d87fe030871bbb016f1c2b73c0b72609d857bace419af7f5d in /usr/local/bin/ 
# Tue, 01 Dec 2020 02:42:37 GMT
RUN docker-php-ext-enable sodium
# Tue, 01 Dec 2020 02:42:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 01 Dec 2020 02:42:40 GMT
CMD ["php" "-a"]
# Tue, 01 Dec 2020 04:28:04 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Tue, 01 Dec 2020 04:28:05 GMT
STOPSIGNAL SIGINT
# Tue, 01 Dec 2020 04:28:12 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 01 Dec 2020 04:28:14 GMT
WORKDIR /var/www/html
# Tue, 01 Dec 2020 04:29:07 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Tue, 01 Dec 2020 04:29:08 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Tue, 08 Dec 2020 00:00:44 GMT
ENV ADMINER_VERSION=4.7.8
# Tue, 08 Dec 2020 00:00:49 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Tue, 08 Dec 2020 00:00:52 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Tue, 08 Dec 2020 00:00:57 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Tue, 08 Dec 2020 00:00:58 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 08 Dec 2020 00:00:59 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Tue, 08 Dec 2020 00:00:59 GMT
USER adminer
# Tue, 08 Dec 2020 00:01:00 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 08 Dec 2020 00:01:01 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:5f2023fd85a4e68f37fe41421fd89f30e69b98a645613521c57c01317561eee3`  
		Last Modified: Thu, 22 Oct 2020 01:58:45 GMT  
		Size: 2.4 MB (2405675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60b50c98f8a8e2c6a27378dfa0f44df1844ac67c6981303675f138a42679f25`  
		Last Modified: Thu, 22 Oct 2020 07:35:57 GMT  
		Size: 1.2 MB (1214265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b472094d673b7c272085505c976192b9aaafa3157c99bade9755fbca18a24071`  
		Last Modified: Thu, 22 Oct 2020 07:35:56 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc39e5d916c11e7eb158e72d14ab981eb45ccc7b6451c1d6d3cb627b71cdbb6`  
		Last Modified: Thu, 22 Oct 2020 07:35:55 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e834fd39435ea86b08faf9b3af2e2623e0a247fa06dfe096decdf80f7a986a`  
		Last Modified: Tue, 01 Dec 2020 04:00:44 GMT  
		Size: 10.3 MB (10338583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a458e4d5704bca7330dbfab239f74ff255f4813b58f19f50a4ad7fd7087f0c8`  
		Last Modified: Tue, 01 Dec 2020 04:00:43 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a500121bbd97abb5116b6e95bdaa9aed74160334e46aadaabef548dca0edce6`  
		Last Modified: Tue, 01 Dec 2020 04:00:46 GMT  
		Size: 12.7 MB (12706582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3321b09ca6255e6f5cb4dce9057df675dd4644a3654424c7ee95fbdcb083e9c`  
		Last Modified: Tue, 01 Dec 2020 04:00:42 GMT  
		Size: 2.3 KB (2257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:345450fde280cf49e34f7246cebd38e311d4b7bebe22415a6126c18e67899f91`  
		Last Modified: Tue, 01 Dec 2020 04:00:42 GMT  
		Size: 16.9 KB (16903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:520112c186c5f2a097e8056a524b7c35704923ebeb6247e924ca839fe6e5b343`  
		Last Modified: Tue, 01 Dec 2020 04:31:36 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d98e04775b392470b2f426804979b34d740103414161d9c89f4df0d0b086e51`  
		Last Modified: Tue, 01 Dec 2020 04:31:34 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c074206a89c8b669d116ecf57544d500dcdc5379828bb10e531adf7af19b658a`  
		Last Modified: Tue, 01 Dec 2020 04:31:34 GMT  
		Size: 3.9 MB (3926108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137384dc891a62af154426c4b36cb9192967da61547507bc1b95301727f85c39`  
		Last Modified: Tue, 01 Dec 2020 04:31:34 GMT  
		Size: 1.5 KB (1473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfdcb3be5430d4c822996a4b1f107a12cafae7d60cc6faf1f7a7cdd8dacaab94`  
		Last Modified: Tue, 08 Dec 2020 00:01:41 GMT  
		Size: 570.9 KB (570924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e55c2ae42163732e674f91058ca3617c71403e138adb01dd23c943ad95d6b0`  
		Last Modified: Tue, 08 Dec 2020 00:01:41 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:b1e09cd04824b43f07df33154a383bc15923451af616eaaae657aca0620d729f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33702279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea6b86a866d797b65cc54d7527a70e1a5e91bf21ecc1ee3fd22b2a2c18d7f6ed`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 07:18:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 22 Oct 2020 07:18:56 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 22 Oct 2020 07:18:59 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 22 Oct 2020 07:19:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 22 Oct 2020 07:19:04 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 22 Oct 2020 07:19:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 07:19:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 07:19:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 22 Oct 2020 07:27:59 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 01 Dec 2020 03:27:01 GMT
ENV PHP_VERSION=7.4.13
# Tue, 01 Dec 2020 03:27:02 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Tue, 01 Dec 2020 03:27:03 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Tue, 01 Dec 2020 03:27:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 01 Dec 2020 03:27:09 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 01 Dec 2020 03:30:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 01 Dec 2020 03:30:42 GMT
COPY multi:afab483600631d4d87fe030871bbb016f1c2b73c0b72609d857bace419af7f5d in /usr/local/bin/ 
# Tue, 01 Dec 2020 03:30:50 GMT
RUN docker-php-ext-enable sodium
# Tue, 01 Dec 2020 03:30:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 01 Dec 2020 03:30:56 GMT
CMD ["php" "-a"]
# Tue, 01 Dec 2020 08:12:36 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Tue, 01 Dec 2020 08:12:37 GMT
STOPSIGNAL SIGINT
# Tue, 01 Dec 2020 08:12:39 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 01 Dec 2020 08:12:40 GMT
WORKDIR /var/www/html
# Tue, 01 Dec 2020 08:13:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Tue, 01 Dec 2020 08:13:23 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Mon, 07 Dec 2020 23:39:52 GMT
ENV ADMINER_VERSION=4.7.8
# Mon, 07 Dec 2020 23:39:53 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Mon, 07 Dec 2020 23:39:54 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Mon, 07 Dec 2020 23:39:56 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Mon, 07 Dec 2020 23:39:57 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Mon, 07 Dec 2020 23:39:58 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Mon, 07 Dec 2020 23:39:58 GMT
USER adminer
# Mon, 07 Dec 2020 23:39:59 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Mon, 07 Dec 2020 23:40:00 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d57dba23203172f8fffd1379aef0307e782178b62dfc684d43c546f7e874ed`  
		Last Modified: Thu, 22 Oct 2020 08:06:21 GMT  
		Size: 1.3 MB (1342784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8414edb0c9c2f7472bb6228bf691a2ddac19ddad7bad789c7cbdc147aded711`  
		Last Modified: Thu, 22 Oct 2020 08:06:20 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d26eeef0db35b2328adae38a8490c7403844452c3606dd17fbe68216f98e82`  
		Last Modified: Thu, 22 Oct 2020 08:06:19 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29be11fa56be3ca1af1498b259f3d5e058a869970cac6d670cf4ca1502485810`  
		Last Modified: Tue, 01 Dec 2020 04:53:56 GMT  
		Size: 10.3 MB (10338597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a553892b0358f6f72064d4dd5e727b686c4461cca7ea8a1211cc86adddb2cb`  
		Last Modified: Tue, 01 Dec 2020 04:53:56 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:828f98d07be67a182899230fc7e38e513de6ce85178d60116c765e90ffbc4119`  
		Last Modified: Tue, 01 Dec 2020 04:54:00 GMT  
		Size: 14.4 MB (14386945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec168016016eef2bef46796f7d7ec48af2459e14d65b9fc2871e756fe3e14d6a`  
		Last Modified: Tue, 01 Dec 2020 04:53:56 GMT  
		Size: 2.3 KB (2260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca32a186f8576115bc6fffe021ff54c52337662fa3cdb51c863d12d20ba02de`  
		Last Modified: Tue, 01 Dec 2020 04:53:55 GMT  
		Size: 17.0 KB (16976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b859cea4a3bb568911dd8f097b1a684daef31726fc5a591b4d9cd57b35187f`  
		Last Modified: Tue, 01 Dec 2020 08:14:59 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e97602a3ba690a845f8ecfaabcff93f82efc85a36445f6413d26f2482987638`  
		Last Modified: Tue, 01 Dec 2020 08:14:56 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6067b9bb9a3850bc39e227d17ab5df99a9bbe61e6d9933fc63c85e464f4aedf5`  
		Last Modified: Tue, 01 Dec 2020 08:14:57 GMT  
		Size: 4.3 MB (4331540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c677bbe386af33259d80d8f4d08a7147fef67adf472b9d841dac1a4a118c7f`  
		Last Modified: Tue, 01 Dec 2020 08:14:57 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4763c08ec3b1c7b68505b48ed92faf18a62525f8ce02d4fba750c232c1826aa9`  
		Last Modified: Mon, 07 Dec 2020 23:40:27 GMT  
		Size: 570.9 KB (570924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:983b1fb60b2afcee1aa424434071184fe8cf507838ac872e30e48755b41f1232`  
		Last Modified: Mon, 07 Dec 2020 23:40:28 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; 386

```console
$ docker pull adminer@sha256:13a4c7ddafd6d4d6a5ee85529f6fa01ebe99d5c5bc1bcafafc85425658693817
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34626966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bb37df3c96977a9c7d5bcff85e2f3904eb30a1d4e2358f0c1644fae769a3ea7`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 22 Oct 2020 02:00:33 GMT
ADD file:46ad43b4984bcf49c5a888ff3628f23161f55cd1fb062f469e707100c97fa254 in / 
# Thu, 22 Oct 2020 02:00:33 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:36:23 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 22 Oct 2020 03:36:26 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 22 Oct 2020 03:36:27 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 22 Oct 2020 03:36:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 22 Oct 2020 03:36:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 22 Oct 2020 03:36:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 03:36:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 03:36:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 22 Oct 2020 03:55:07 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 01 Dec 2020 04:01:21 GMT
ENV PHP_VERSION=7.4.13
# Tue, 01 Dec 2020 04:01:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Tue, 01 Dec 2020 04:01:22 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Tue, 01 Dec 2020 04:01:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 01 Dec 2020 04:01:40 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 01 Dec 2020 04:10:51 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 01 Dec 2020 04:10:52 GMT
COPY multi:afab483600631d4d87fe030871bbb016f1c2b73c0b72609d857bace419af7f5d in /usr/local/bin/ 
# Tue, 01 Dec 2020 04:10:54 GMT
RUN docker-php-ext-enable sodium
# Tue, 01 Dec 2020 04:10:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 01 Dec 2020 04:10:55 GMT
CMD ["php" "-a"]
# Tue, 01 Dec 2020 09:24:38 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Tue, 01 Dec 2020 09:24:38 GMT
STOPSIGNAL SIGINT
# Tue, 01 Dec 2020 09:24:39 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 01 Dec 2020 09:24:39 GMT
WORKDIR /var/www/html
# Tue, 01 Dec 2020 09:25:13 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Tue, 01 Dec 2020 09:25:13 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Mon, 07 Dec 2020 23:38:24 GMT
ENV ADMINER_VERSION=4.7.8
# Mon, 07 Dec 2020 23:38:24 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Mon, 07 Dec 2020 23:38:24 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Mon, 07 Dec 2020 23:38:26 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Mon, 07 Dec 2020 23:38:26 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Mon, 07 Dec 2020 23:38:26 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Mon, 07 Dec 2020 23:38:26 GMT
USER adminer
# Mon, 07 Dec 2020 23:38:26 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Mon, 07 Dec 2020 23:38:27 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:d6ca64ac6f4b6382142ce9a3501652938130a6ec4bb02f3f455ee1f980834cfe`  
		Last Modified: Thu, 22 Oct 2020 02:00:57 GMT  
		Size: 2.8 MB (2791407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30be8ffd290910905a5fb7cbb70252eb0f59edb09db20bdc21f3b65456acc28f`  
		Last Modified: Thu, 22 Oct 2020 05:10:23 GMT  
		Size: 1.4 MB (1439641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d58e2433b13446c863e85b34f8e4c93ca9d5b3b93d2bac415fd9cdf77bcec4`  
		Last Modified: Thu, 22 Oct 2020 05:10:21 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5729dcb8d303f82a7f8cf3df49048e34ce8ee89f79155fb08a475da46b64308`  
		Last Modified: Thu, 22 Oct 2020 05:10:21 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ffdca9b500ff910069fefe63b455206db2cf0fa00dc6b7c7d53219dfaf7f5b`  
		Last Modified: Tue, 01 Dec 2020 07:15:13 GMT  
		Size: 10.3 MB (10338561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c682383cda14fca62843652d7478a26995cfbbfbcb457985de4ca5cfb77de751`  
		Last Modified: Tue, 01 Dec 2020 07:15:12 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57833a53685f649182bdbb4194ba35390c17fa65a6b09c4e377a42a5f9aaca30`  
		Last Modified: Tue, 01 Dec 2020 07:15:18 GMT  
		Size: 14.9 MB (14942640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7003874a29c37e250b24c310b448d1c36607cdb1b43128071780d5fd0a0dc3e1`  
		Last Modified: Tue, 01 Dec 2020 07:15:12 GMT  
		Size: 2.3 KB (2259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fcfab619124f72931608ea142c1cd80a26871e1631380720b6be739170e21b6`  
		Last Modified: Tue, 01 Dec 2020 07:15:12 GMT  
		Size: 16.9 KB (16924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055719a49e04df90bb23499c98da9779637e3b44446a60f202283f57e4b29b04`  
		Last Modified: Tue, 01 Dec 2020 09:26:14 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2b0f52d9f107a35a34b4f8c69abbdf24f2de8a0431c812d74cb6dd3cbf8bf2`  
		Last Modified: Tue, 01 Dec 2020 09:26:13 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4edb5ffb9c3f753b4991debfaeef5c535ae5d689a18b7fff9f0b042c5883865`  
		Last Modified: Tue, 01 Dec 2020 09:26:14 GMT  
		Size: 4.5 MB (4519100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9258866f679eb2cbc89aa311d5d2dad0c146a7e9f61c9e805b63d7f324d2afb0`  
		Last Modified: Tue, 01 Dec 2020 09:26:13 GMT  
		Size: 1.5 KB (1472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:904e3ae5079e7cd06213e6912d4237663cff97a37e1ed247e24b7f455951eafe`  
		Last Modified: Mon, 07 Dec 2020 23:38:45 GMT  
		Size: 570.9 KB (570859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:362b319c8a865e06c57265a80b857954a02a4e09ffe3eda699eede128dcdef90`  
		Last Modified: Mon, 07 Dec 2020 23:38:45 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; ppc64le

```console
$ docker pull adminer@sha256:73feff7b317d1078b173d0c1dc928c14bf61e94b4562a0a79132b9dac74739aa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 MB (35029016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2bacaef82d901426ed9bf50182af16a98e04172b1d2dac51b87db0885487f72`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 22 Oct 2020 11:00:06 GMT
ADD file:176e047fab2c1828575bffa6b14773efa297b7ecf312d86103c5dd4f78ec8027 in / 
# Thu, 22 Oct 2020 11:00:17 GMT
CMD ["/bin/sh"]
# Fri, 23 Oct 2020 00:21:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 23 Oct 2020 00:21:18 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 23 Oct 2020 00:21:30 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 23 Oct 2020 00:21:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 23 Oct 2020 00:21:44 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 23 Oct 2020 00:21:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 23 Oct 2020 00:21:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 23 Oct 2020 00:21:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 23 Oct 2020 00:34:37 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 01 Dec 2020 03:52:39 GMT
ENV PHP_VERSION=7.4.13
# Tue, 01 Dec 2020 03:52:44 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Tue, 01 Dec 2020 03:52:51 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Tue, 01 Dec 2020 03:53:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 01 Dec 2020 03:53:13 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 01 Dec 2020 03:57:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 01 Dec 2020 03:57:24 GMT
COPY multi:afab483600631d4d87fe030871bbb016f1c2b73c0b72609d857bace419af7f5d in /usr/local/bin/ 
# Tue, 01 Dec 2020 03:57:33 GMT
RUN docker-php-ext-enable sodium
# Tue, 01 Dec 2020 03:57:36 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 01 Dec 2020 03:57:39 GMT
CMD ["php" "-a"]
# Tue, 01 Dec 2020 07:09:03 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Tue, 01 Dec 2020 07:09:12 GMT
STOPSIGNAL SIGINT
# Tue, 01 Dec 2020 07:09:25 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 01 Dec 2020 07:09:32 GMT
WORKDIR /var/www/html
# Tue, 01 Dec 2020 07:10:30 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Tue, 01 Dec 2020 07:10:33 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Tue, 08 Dec 2020 00:16:36 GMT
ENV ADMINER_VERSION=4.7.8
# Tue, 08 Dec 2020 00:16:38 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Tue, 08 Dec 2020 00:16:41 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Tue, 08 Dec 2020 00:16:53 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Tue, 08 Dec 2020 00:16:54 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 08 Dec 2020 00:16:58 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Tue, 08 Dec 2020 00:17:11 GMT
USER adminer
# Tue, 08 Dec 2020 00:17:16 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 08 Dec 2020 00:17:18 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:692a9d763e196c85d79fc3e45b316b1bb557c93ba88a3c8ebf679a585d1efe73`  
		Last Modified: Thu, 22 Oct 2020 11:02:06 GMT  
		Size: 2.8 MB (2803218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0285d6f06f3beb1c140c055210664c441b93dd4f2037177a5396bce94ca16ce5`  
		Last Modified: Fri, 23 Oct 2020 01:34:08 GMT  
		Size: 1.4 MB (1383187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a6459a3bf272daa53ff4ba97cc849676f497de9f78d8e9378ec02552293f175`  
		Last Modified: Fri, 23 Oct 2020 01:34:07 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16cff6064dc29d3f629d353736c1cac074caa5b50738422adb84de99a019bb32`  
		Last Modified: Fri, 23 Oct 2020 01:34:08 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0baf560776c5dd75b5673be3d73b900119615cfc4e4fe24414486e3d1f11920`  
		Last Modified: Tue, 01 Dec 2020 05:50:29 GMT  
		Size: 10.3 MB (10338609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4d8083b683ead9a591a00aff14c8d0091665e1433d301a027b214f19cbe23f`  
		Last Modified: Tue, 01 Dec 2020 05:50:29 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7381e6ce3e117510e5a2bf102da48e3cc1b5fd3414651ec324bbe759d367be`  
		Last Modified: Tue, 01 Dec 2020 05:50:32 GMT  
		Size: 15.5 MB (15548036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8328c4e67c6b29f383993d05557e298bc834c18c00961b9ab2a1c4e4eb05b4fd`  
		Last Modified: Tue, 01 Dec 2020 05:50:28 GMT  
		Size: 2.3 KB (2259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:236813d0f57da4fa9c0d5938846f85e82a0a01ce89ca208916b8f649c0ee99fd`  
		Last Modified: Tue, 01 Dec 2020 05:50:28 GMT  
		Size: 17.0 KB (16965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acf7ec6b5baaa9faab722bfc6a7098e0871e3edb42be513e64fe8e06bc7edec1`  
		Last Modified: Tue, 01 Dec 2020 07:14:36 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c17363dc3aab754805ecdc74f39535a73cfc5f3cebe72a4cb18fdc97df1ef9fa`  
		Last Modified: Tue, 01 Dec 2020 07:14:33 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95753fdce29daf55de647d3a29a8cc07941f7bf95fec4a560b0d698478b782f3`  
		Last Modified: Tue, 01 Dec 2020 07:14:34 GMT  
		Size: 4.4 MB (4360119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cad5fcb53526734d41770680ea56047b6e13c767960fc1d0a0b8de7c7030c75`  
		Last Modified: Tue, 01 Dec 2020 07:14:33 GMT  
		Size: 1.5 KB (1474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b231a33566f06d48010343aac194149b1ce1613cf2397c67cf1be2984295f133`  
		Last Modified: Tue, 08 Dec 2020 00:18:38 GMT  
		Size: 570.9 KB (570925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628d0ad1cc992636ad6e5a1f0cf7de70d844c7cccb85cda16205dc67b167e131`  
		Last Modified: Tue, 08 Dec 2020 00:18:38 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; s390x

```console
$ docker pull adminer@sha256:6b00709e793594a51832541158adeb2ae42e00829dbfb77a54bc0eef7fd1668d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32521955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f75d1bfddd1544fe2cddf65f0baa090dfb992c4a38b43b24670dc3b1ce037d7`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 11 Dec 2020 02:09:52 GMT
ADD file:c9395a36a4e03768aabd282eb1f31705cc00181d3147222d9c940eaa5a8fd511 in / 
# Fri, 11 Dec 2020 02:09:53 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 11:30:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 11 Dec 2020 11:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 11 Dec 2020 11:30:56 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 11 Dec 2020 11:30:57 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 11 Dec 2020 11:30:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 11 Dec 2020 11:30:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Dec 2020 11:31:00 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Dec 2020 11:31:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 11 Dec 2020 12:01:46 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 11 Dec 2020 12:01:46 GMT
ENV PHP_VERSION=7.4.13
# Fri, 11 Dec 2020 12:01:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Fri, 11 Dec 2020 12:01:48 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Fri, 11 Dec 2020 12:01:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 11 Dec 2020 12:01:54 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Dec 2020 12:08:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Dec 2020 12:08:47 GMT
COPY multi:afab483600631d4d87fe030871bbb016f1c2b73c0b72609d857bace419af7f5d in /usr/local/bin/ 
# Fri, 11 Dec 2020 12:08:49 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Dec 2020 12:08:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Dec 2020 12:08:50 GMT
CMD ["php" "-a"]
# Fri, 11 Dec 2020 18:43:30 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 11 Dec 2020 18:43:31 GMT
STOPSIGNAL SIGINT
# Fri, 11 Dec 2020 18:43:33 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 11 Dec 2020 18:43:33 GMT
WORKDIR /var/www/html
# Fri, 11 Dec 2020 18:44:50 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 11 Dec 2020 18:44:50 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 11 Dec 2020 18:44:51 GMT
ENV ADMINER_VERSION=4.7.8
# Fri, 11 Dec 2020 18:44:52 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Fri, 11 Dec 2020 18:44:52 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Fri, 11 Dec 2020 18:44:56 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 11 Dec 2020 18:44:57 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 11 Dec 2020 18:44:57 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 11 Dec 2020 18:44:58 GMT
USER adminer
# Fri, 11 Dec 2020 18:44:59 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 11 Dec 2020 18:44:59 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:7c2470fe3d16cb70fca0826168095a96838b1322a8cd1502b28284ee8561b491`  
		Last Modified: Fri, 11 Dec 2020 02:10:27 GMT  
		Size: 2.6 MB (2565988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a23c8359d30ae261ad953f292e6681a71ebc7388607b74d901bbc07f71e1311`  
		Last Modified: Fri, 11 Dec 2020 13:48:01 GMT  
		Size: 1.4 MB (1382587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01422c3e898d3241d4134256bf0d911b0752823227af04614187c79c187e2843`  
		Last Modified: Fri, 11 Dec 2020 13:48:03 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a0be2077abd44f96e50bdebb1ed93a6e2b8d504761c23fa0e5e9b87045ca38`  
		Last Modified: Fri, 11 Dec 2020 13:48:01 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267bafe0bb23009994a23ad5cdcc3b4d425f186f0e488b5f7461463ad1b53814`  
		Last Modified: Fri, 11 Dec 2020 13:50:24 GMT  
		Size: 10.3 MB (10338590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36304b0fbddac7ce44edacaedb902676688cfc3bb7082576f6b57eed0ccc133e`  
		Last Modified: Fri, 11 Dec 2020 13:50:25 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fa33489075ff6318ffc5a7cf5c94cb4ce65ccfc82b5970cc91628780c130aae`  
		Last Modified: Fri, 11 Dec 2020 13:50:26 GMT  
		Size: 13.5 MB (13485898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155ae451461e50390ae0db27a78a329e87a86b9f9eb04f6db81fcc27430f2d51`  
		Last Modified: Fri, 11 Dec 2020 13:50:24 GMT  
		Size: 2.3 KB (2257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b379111cc7023c652243c4d9234de47984fa307030d667bf14e5d12889ec8180`  
		Last Modified: Fri, 11 Dec 2020 13:50:24 GMT  
		Size: 16.9 KB (16879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a18e16d8efd7f249149e2d38813d86590cc4a55f23d8c5bbba970725422ea51`  
		Last Modified: Fri, 11 Dec 2020 18:47:13 GMT  
		Size: 310.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ba44137233477a93edb1e0cc94bee3ce4dafaed9ff932d21594190f861ef75`  
		Last Modified: Fri, 11 Dec 2020 18:47:13 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cba732448866bbb0e567b7510578f951e9cf0bc258588c8e898be1606e3a3eb`  
		Last Modified: Fri, 11 Dec 2020 18:47:11 GMT  
		Size: 4.2 MB (4153155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8faf5f39c5d146bc658625977adca6ce417bb45b9683bb1767b99abfea6d3d56`  
		Last Modified: Fri, 11 Dec 2020 18:47:11 GMT  
		Size: 1.5 KB (1473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008d2a285f2f6bcf687be0cb08b167a975a4d7534a16435da10ba2b75b2e2d73`  
		Last Modified: Fri, 11 Dec 2020 18:47:11 GMT  
		Size: 570.9 KB (570918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6852608d1b2324d98a56de31e6fc11ac1fe8e95f605b50c9f72db2bd5cd092`  
		Last Modified: Fri, 11 Dec 2020 18:47:12 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:standalone`

```console
$ docker pull adminer@sha256:4600f2453f7c9f3ee8179016a65d0b49a8dfb89467ac0947a6245e62e7f81fb1
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

### `adminer:standalone` - linux; amd64

```console
$ docker pull adminer@sha256:4b087576de7b4ca7c60bb3558f0b5ee30f496cee10fa19ea0a9f0e071c72b1f5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (33965375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2db7241b0f1461d8707525832e608fe513453f99c11beed9413194f7519e05`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 06:30:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 22 Oct 2020 06:30:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 22 Oct 2020 06:30:15 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 22 Oct 2020 06:30:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 22 Oct 2020 06:30:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 22 Oct 2020 06:30:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 06:30:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 06:30:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 22 Oct 2020 06:43:41 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 01 Dec 2020 04:36:20 GMT
ENV PHP_VERSION=7.4.13
# Tue, 01 Dec 2020 04:36:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Tue, 01 Dec 2020 04:36:21 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Tue, 01 Dec 2020 04:36:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 01 Dec 2020 04:36:27 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 01 Dec 2020 04:44:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 01 Dec 2020 04:44:54 GMT
COPY multi:afab483600631d4d87fe030871bbb016f1c2b73c0b72609d857bace419af7f5d in /usr/local/bin/ 
# Tue, 01 Dec 2020 04:44:57 GMT
RUN docker-php-ext-enable sodium
# Tue, 01 Dec 2020 04:44:57 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 01 Dec 2020 04:44:57 GMT
CMD ["php" "-a"]
# Tue, 01 Dec 2020 07:46:46 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Tue, 01 Dec 2020 07:46:46 GMT
STOPSIGNAL SIGINT
# Tue, 01 Dec 2020 07:46:47 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 01 Dec 2020 07:46:48 GMT
WORKDIR /var/www/html
# Tue, 01 Dec 2020 07:47:15 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Tue, 01 Dec 2020 07:47:15 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Tue, 08 Dec 2020 00:19:24 GMT
ENV ADMINER_VERSION=4.7.8
# Tue, 08 Dec 2020 00:19:24 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Tue, 08 Dec 2020 00:19:24 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Tue, 08 Dec 2020 00:19:26 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Tue, 08 Dec 2020 00:19:26 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 08 Dec 2020 00:19:26 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Tue, 08 Dec 2020 00:19:26 GMT
USER adminer
# Tue, 08 Dec 2020 00:19:27 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 08 Dec 2020 00:19:27 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f8bf6cfdbe614fef94f982905079c16e27b3de2d24eb1ff513d3d83e656ca2`  
		Last Modified: Thu, 22 Oct 2020 07:36:55 GMT  
		Size: 1.3 MB (1340771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce5be79740125b9e74a77885bf6ee2b0d25ac7ed9e9432c5aa7210bb3b00458a`  
		Last Modified: Thu, 22 Oct 2020 07:36:55 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99dd6507fe563b66ba35badf706e1bbb2d39eb5d0a3c0d5a86a45d2af7e89c1`  
		Last Modified: Thu, 22 Oct 2020 07:36:55 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c513a1b503cf7c9f18fa014dada9744070ded92dc9ad548cd056c4f56dc1a9`  
		Last Modified: Tue, 01 Dec 2020 07:27:10 GMT  
		Size: 10.3 MB (10338569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff080eafb4c0518981fca6aef4d239863fc59195f41ce7c440b2c6c518f2ac79`  
		Last Modified: Tue, 01 Dec 2020 07:27:09 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e818119992b11dbf09b710066a78920985b9ea1310fc8272df816e0884985f44`  
		Last Modified: Tue, 01 Dec 2020 07:27:13 GMT  
		Size: 14.6 MB (14572037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba3c14a67f95ae52ebfb558ab6b5d87687a05ce41c8df0a618ff42b73204e40`  
		Last Modified: Tue, 01 Dec 2020 07:27:09 GMT  
		Size: 2.3 KB (2257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbb0285b7ad2b170e4ed2cffbe0f16ba55d689c056ff43767834783eab7b8261`  
		Last Modified: Tue, 01 Dec 2020 07:27:09 GMT  
		Size: 17.0 KB (16987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae324cfad8acf03b3a98a15e963b7046404a7da3a6bbf68fd65d37f899f194d`  
		Last Modified: Tue, 01 Dec 2020 07:48:25 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb51158f683d66315de6fa572f7ea13d8ffb71ac85faa20c8578edb11678f37d`  
		Last Modified: Tue, 01 Dec 2020 07:48:23 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71ac21b64d1d63d967acb13664404babd0ef86fc896c484ce28cccf70001d0f1`  
		Last Modified: Tue, 01 Dec 2020 07:48:24 GMT  
		Size: 4.3 MB (4321455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2170e09d39d861e9bb7a5da5def906b44153b6c481fe17925ba82d1f1f78eec`  
		Last Modified: Tue, 01 Dec 2020 07:48:24 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d95b48dfa11f7f5c061f6522f6ff5d574452b8f321c6075455da2643b1967a`  
		Last Modified: Tue, 08 Dec 2020 00:19:45 GMT  
		Size: 570.9 KB (570860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3bb2b5e72bf0dbd4b855ddf65aaf9c0d077703804bdbdc9ea3ea98cbbfceaf6`  
		Last Modified: Tue, 08 Dec 2020 00:19:44 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:standalone` - linux; arm variant v6

```console
$ docker pull adminer@sha256:7e114494e5e3a8ece382083d27c33f6c993695f0ff6c92c235ced149177f5da9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32073857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9cfa5ccbab063435267257cf4c761402c956233cf22775ed1c774b53a045715`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 11 Dec 2020 02:17:15 GMT
ADD file:1a9c0a67560d338c0c0e7005d8915d998fc9cf3e9f53bfd7e42e8391f0a39bce in / 
# Fri, 11 Dec 2020 02:17:15 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 07:04:50 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 11 Dec 2020 07:04:53 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 11 Dec 2020 07:04:55 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 11 Dec 2020 07:04:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 11 Dec 2020 07:04:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 11 Dec 2020 07:05:00 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Dec 2020 07:05:01 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Dec 2020 07:05:02 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 11 Dec 2020 07:13:50 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 11 Dec 2020 07:13:54 GMT
ENV PHP_VERSION=7.4.13
# Fri, 11 Dec 2020 07:13:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Fri, 11 Dec 2020 07:13:56 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Fri, 11 Dec 2020 07:14:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 11 Dec 2020 07:14:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Dec 2020 07:17:37 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Dec 2020 07:17:39 GMT
COPY multi:afab483600631d4d87fe030871bbb016f1c2b73c0b72609d857bace419af7f5d in /usr/local/bin/ 
# Fri, 11 Dec 2020 07:17:42 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Dec 2020 07:17:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Dec 2020 07:17:43 GMT
CMD ["php" "-a"]
# Fri, 11 Dec 2020 09:04:18 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 11 Dec 2020 09:04:19 GMT
STOPSIGNAL SIGINT
# Fri, 11 Dec 2020 09:04:21 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 11 Dec 2020 09:04:22 GMT
WORKDIR /var/www/html
# Fri, 11 Dec 2020 09:05:06 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 11 Dec 2020 09:05:08 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 11 Dec 2020 09:05:08 GMT
ENV ADMINER_VERSION=4.7.8
# Fri, 11 Dec 2020 09:05:09 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Fri, 11 Dec 2020 09:05:11 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Fri, 11 Dec 2020 09:05:14 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 11 Dec 2020 09:05:15 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 11 Dec 2020 09:05:16 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 11 Dec 2020 09:05:17 GMT
USER adminer
# Fri, 11 Dec 2020 09:05:18 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 11 Dec 2020 09:05:19 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:f1c16df8fee33d421d08790b17ca2af67a3fe49e77b6b991dd0c30631f5d1baf`  
		Last Modified: Fri, 11 Dec 2020 02:17:57 GMT  
		Size: 2.6 MB (2601992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623cc08cbe035cf15859e57a83e2243620418da06e1905d1875a46bec901e540`  
		Last Modified: Fri, 11 Dec 2020 07:56:49 GMT  
		Size: 1.3 MB (1310156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3a7aacff9b7ccf646f2bdbbc8d40bbb304550e813876049e721abd35461df9`  
		Last Modified: Fri, 11 Dec 2020 07:56:49 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d3214ea6f418597f370177309be7728f94481030c9cba6e45c4b74cfd04cc0`  
		Last Modified: Fri, 11 Dec 2020 07:56:49 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64de18534c9c3dd7212eceb5a285d571df578238ca4684a2e922b131e9947d79`  
		Last Modified: Fri, 11 Dec 2020 07:57:40 GMT  
		Size: 10.3 MB (10338603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d60b5c1c75b96676e4154f74a500fdd4a2645d4c51e189b0bdd18e06f26c3143`  
		Last Modified: Fri, 11 Dec 2020 07:57:39 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee32c3be90bc13cb4b3406c492ec35d5c211ac42b25e536939fb3220aea672b`  
		Last Modified: Fri, 11 Dec 2020 07:57:44 GMT  
		Size: 13.2 MB (13201116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e71cdda7d8acfe2fe1a6263c1b004b3ae972d7ce1c0ac95fec09aa0c0ba1f7fd`  
		Last Modified: Fri, 11 Dec 2020 07:57:39 GMT  
		Size: 2.3 KB (2258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec74a6ee1beba601eed5abe261394c8ddfa2d53093a1f6768356ec5891066746`  
		Last Modified: Fri, 11 Dec 2020 07:57:40 GMT  
		Size: 16.9 KB (16889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b84bf5ad218839b4e8156c322c5611b3c26167141a7c1e8049055deeda8b1ed5`  
		Last Modified: Fri, 11 Dec 2020 09:07:23 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0113ef6e65685219488d6543639cff152292617519f4649a6d7c8e4bbf03322b`  
		Last Modified: Fri, 11 Dec 2020 09:07:21 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2501c821a30d874046f30dd9d3947aa9f82cca3e9d39eb18214a765744e0b24`  
		Last Modified: Fri, 11 Dec 2020 09:07:21 GMT  
		Size: 4.0 MB (4026242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:945b172c5cf67a28a59e5b25cfed08871f360f551a912c8d7f64c096d6554812`  
		Last Modified: Fri, 11 Dec 2020 09:07:20 GMT  
		Size: 1.5 KB (1473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df40a3aa85441cb471ce645d5a0a2564fb9e2f042e078b8f04dd343488863a4`  
		Last Modified: Fri, 11 Dec 2020 09:07:20 GMT  
		Size: 570.9 KB (570917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90644dda17e22024741efd92b2987150a52659ae6bb25b7ea232e9b72d3b1d83`  
		Last Modified: Fri, 11 Dec 2020 09:07:20 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:standalone` - linux; arm variant v7

```console
$ docker pull adminer@sha256:39b988e9485b8f06142e8584a4764c3c32159d51377eab0739b1cf794f701d1a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31186995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d4ed3310dfe2d29dd9a809a5ea826952ac518c5d93ab5e12054d9b7560791f7`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 22 Oct 2020 01:58:13 GMT
ADD file:46f89172426e9f5b1d669a2ca7ab218fc2deaef1caeeab88f2b5bd443ac9773d in / 
# Thu, 22 Oct 2020 01:58:14 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 06:47:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 22 Oct 2020 06:47:37 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 22 Oct 2020 06:47:45 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 22 Oct 2020 06:47:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 22 Oct 2020 06:47:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 22 Oct 2020 06:47:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 06:47:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 06:48:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 22 Oct 2020 06:56:26 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 01 Dec 2020 02:39:45 GMT
ENV PHP_VERSION=7.4.13
# Tue, 01 Dec 2020 02:39:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Tue, 01 Dec 2020 02:39:46 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Tue, 01 Dec 2020 02:39:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 01 Dec 2020 02:39:53 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 01 Dec 2020 02:42:30 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 01 Dec 2020 02:42:32 GMT
COPY multi:afab483600631d4d87fe030871bbb016f1c2b73c0b72609d857bace419af7f5d in /usr/local/bin/ 
# Tue, 01 Dec 2020 02:42:37 GMT
RUN docker-php-ext-enable sodium
# Tue, 01 Dec 2020 02:42:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 01 Dec 2020 02:42:40 GMT
CMD ["php" "-a"]
# Tue, 01 Dec 2020 04:28:04 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Tue, 01 Dec 2020 04:28:05 GMT
STOPSIGNAL SIGINT
# Tue, 01 Dec 2020 04:28:12 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 01 Dec 2020 04:28:14 GMT
WORKDIR /var/www/html
# Tue, 01 Dec 2020 04:29:07 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Tue, 01 Dec 2020 04:29:08 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Tue, 08 Dec 2020 00:00:44 GMT
ENV ADMINER_VERSION=4.7.8
# Tue, 08 Dec 2020 00:00:49 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Tue, 08 Dec 2020 00:00:52 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Tue, 08 Dec 2020 00:00:57 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Tue, 08 Dec 2020 00:00:58 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 08 Dec 2020 00:00:59 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Tue, 08 Dec 2020 00:00:59 GMT
USER adminer
# Tue, 08 Dec 2020 00:01:00 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 08 Dec 2020 00:01:01 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:5f2023fd85a4e68f37fe41421fd89f30e69b98a645613521c57c01317561eee3`  
		Last Modified: Thu, 22 Oct 2020 01:58:45 GMT  
		Size: 2.4 MB (2405675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60b50c98f8a8e2c6a27378dfa0f44df1844ac67c6981303675f138a42679f25`  
		Last Modified: Thu, 22 Oct 2020 07:35:57 GMT  
		Size: 1.2 MB (1214265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b472094d673b7c272085505c976192b9aaafa3157c99bade9755fbca18a24071`  
		Last Modified: Thu, 22 Oct 2020 07:35:56 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc39e5d916c11e7eb158e72d14ab981eb45ccc7b6451c1d6d3cb627b71cdbb6`  
		Last Modified: Thu, 22 Oct 2020 07:35:55 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e834fd39435ea86b08faf9b3af2e2623e0a247fa06dfe096decdf80f7a986a`  
		Last Modified: Tue, 01 Dec 2020 04:00:44 GMT  
		Size: 10.3 MB (10338583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a458e4d5704bca7330dbfab239f74ff255f4813b58f19f50a4ad7fd7087f0c8`  
		Last Modified: Tue, 01 Dec 2020 04:00:43 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a500121bbd97abb5116b6e95bdaa9aed74160334e46aadaabef548dca0edce6`  
		Last Modified: Tue, 01 Dec 2020 04:00:46 GMT  
		Size: 12.7 MB (12706582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3321b09ca6255e6f5cb4dce9057df675dd4644a3654424c7ee95fbdcb083e9c`  
		Last Modified: Tue, 01 Dec 2020 04:00:42 GMT  
		Size: 2.3 KB (2257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:345450fde280cf49e34f7246cebd38e311d4b7bebe22415a6126c18e67899f91`  
		Last Modified: Tue, 01 Dec 2020 04:00:42 GMT  
		Size: 16.9 KB (16903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:520112c186c5f2a097e8056a524b7c35704923ebeb6247e924ca839fe6e5b343`  
		Last Modified: Tue, 01 Dec 2020 04:31:36 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d98e04775b392470b2f426804979b34d740103414161d9c89f4df0d0b086e51`  
		Last Modified: Tue, 01 Dec 2020 04:31:34 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c074206a89c8b669d116ecf57544d500dcdc5379828bb10e531adf7af19b658a`  
		Last Modified: Tue, 01 Dec 2020 04:31:34 GMT  
		Size: 3.9 MB (3926108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137384dc891a62af154426c4b36cb9192967da61547507bc1b95301727f85c39`  
		Last Modified: Tue, 01 Dec 2020 04:31:34 GMT  
		Size: 1.5 KB (1473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfdcb3be5430d4c822996a4b1f107a12cafae7d60cc6faf1f7a7cdd8dacaab94`  
		Last Modified: Tue, 08 Dec 2020 00:01:41 GMT  
		Size: 570.9 KB (570924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e55c2ae42163732e674f91058ca3617c71403e138adb01dd23c943ad95d6b0`  
		Last Modified: Tue, 08 Dec 2020 00:01:41 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:standalone` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:b1e09cd04824b43f07df33154a383bc15923451af616eaaae657aca0620d729f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33702279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea6b86a866d797b65cc54d7527a70e1a5e91bf21ecc1ee3fd22b2a2c18d7f6ed`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 07:18:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 22 Oct 2020 07:18:56 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 22 Oct 2020 07:18:59 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 22 Oct 2020 07:19:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 22 Oct 2020 07:19:04 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 22 Oct 2020 07:19:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 07:19:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 07:19:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 22 Oct 2020 07:27:59 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 01 Dec 2020 03:27:01 GMT
ENV PHP_VERSION=7.4.13
# Tue, 01 Dec 2020 03:27:02 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Tue, 01 Dec 2020 03:27:03 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Tue, 01 Dec 2020 03:27:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 01 Dec 2020 03:27:09 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 01 Dec 2020 03:30:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 01 Dec 2020 03:30:42 GMT
COPY multi:afab483600631d4d87fe030871bbb016f1c2b73c0b72609d857bace419af7f5d in /usr/local/bin/ 
# Tue, 01 Dec 2020 03:30:50 GMT
RUN docker-php-ext-enable sodium
# Tue, 01 Dec 2020 03:30:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 01 Dec 2020 03:30:56 GMT
CMD ["php" "-a"]
# Tue, 01 Dec 2020 08:12:36 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Tue, 01 Dec 2020 08:12:37 GMT
STOPSIGNAL SIGINT
# Tue, 01 Dec 2020 08:12:39 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 01 Dec 2020 08:12:40 GMT
WORKDIR /var/www/html
# Tue, 01 Dec 2020 08:13:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Tue, 01 Dec 2020 08:13:23 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Mon, 07 Dec 2020 23:39:52 GMT
ENV ADMINER_VERSION=4.7.8
# Mon, 07 Dec 2020 23:39:53 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Mon, 07 Dec 2020 23:39:54 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Mon, 07 Dec 2020 23:39:56 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Mon, 07 Dec 2020 23:39:57 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Mon, 07 Dec 2020 23:39:58 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Mon, 07 Dec 2020 23:39:58 GMT
USER adminer
# Mon, 07 Dec 2020 23:39:59 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Mon, 07 Dec 2020 23:40:00 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d57dba23203172f8fffd1379aef0307e782178b62dfc684d43c546f7e874ed`  
		Last Modified: Thu, 22 Oct 2020 08:06:21 GMT  
		Size: 1.3 MB (1342784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8414edb0c9c2f7472bb6228bf691a2ddac19ddad7bad789c7cbdc147aded711`  
		Last Modified: Thu, 22 Oct 2020 08:06:20 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d26eeef0db35b2328adae38a8490c7403844452c3606dd17fbe68216f98e82`  
		Last Modified: Thu, 22 Oct 2020 08:06:19 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29be11fa56be3ca1af1498b259f3d5e058a869970cac6d670cf4ca1502485810`  
		Last Modified: Tue, 01 Dec 2020 04:53:56 GMT  
		Size: 10.3 MB (10338597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a553892b0358f6f72064d4dd5e727b686c4461cca7ea8a1211cc86adddb2cb`  
		Last Modified: Tue, 01 Dec 2020 04:53:56 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:828f98d07be67a182899230fc7e38e513de6ce85178d60116c765e90ffbc4119`  
		Last Modified: Tue, 01 Dec 2020 04:54:00 GMT  
		Size: 14.4 MB (14386945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec168016016eef2bef46796f7d7ec48af2459e14d65b9fc2871e756fe3e14d6a`  
		Last Modified: Tue, 01 Dec 2020 04:53:56 GMT  
		Size: 2.3 KB (2260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca32a186f8576115bc6fffe021ff54c52337662fa3cdb51c863d12d20ba02de`  
		Last Modified: Tue, 01 Dec 2020 04:53:55 GMT  
		Size: 17.0 KB (16976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b859cea4a3bb568911dd8f097b1a684daef31726fc5a591b4d9cd57b35187f`  
		Last Modified: Tue, 01 Dec 2020 08:14:59 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e97602a3ba690a845f8ecfaabcff93f82efc85a36445f6413d26f2482987638`  
		Last Modified: Tue, 01 Dec 2020 08:14:56 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6067b9bb9a3850bc39e227d17ab5df99a9bbe61e6d9933fc63c85e464f4aedf5`  
		Last Modified: Tue, 01 Dec 2020 08:14:57 GMT  
		Size: 4.3 MB (4331540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c677bbe386af33259d80d8f4d08a7147fef67adf472b9d841dac1a4a118c7f`  
		Last Modified: Tue, 01 Dec 2020 08:14:57 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4763c08ec3b1c7b68505b48ed92faf18a62525f8ce02d4fba750c232c1826aa9`  
		Last Modified: Mon, 07 Dec 2020 23:40:27 GMT  
		Size: 570.9 KB (570924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:983b1fb60b2afcee1aa424434071184fe8cf507838ac872e30e48755b41f1232`  
		Last Modified: Mon, 07 Dec 2020 23:40:28 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:standalone` - linux; 386

```console
$ docker pull adminer@sha256:13a4c7ddafd6d4d6a5ee85529f6fa01ebe99d5c5bc1bcafafc85425658693817
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34626966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bb37df3c96977a9c7d5bcff85e2f3904eb30a1d4e2358f0c1644fae769a3ea7`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 22 Oct 2020 02:00:33 GMT
ADD file:46ad43b4984bcf49c5a888ff3628f23161f55cd1fb062f469e707100c97fa254 in / 
# Thu, 22 Oct 2020 02:00:33 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:36:23 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 22 Oct 2020 03:36:26 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 22 Oct 2020 03:36:27 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 22 Oct 2020 03:36:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 22 Oct 2020 03:36:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 22 Oct 2020 03:36:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 03:36:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 03:36:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 22 Oct 2020 03:55:07 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 01 Dec 2020 04:01:21 GMT
ENV PHP_VERSION=7.4.13
# Tue, 01 Dec 2020 04:01:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Tue, 01 Dec 2020 04:01:22 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Tue, 01 Dec 2020 04:01:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 01 Dec 2020 04:01:40 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 01 Dec 2020 04:10:51 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 01 Dec 2020 04:10:52 GMT
COPY multi:afab483600631d4d87fe030871bbb016f1c2b73c0b72609d857bace419af7f5d in /usr/local/bin/ 
# Tue, 01 Dec 2020 04:10:54 GMT
RUN docker-php-ext-enable sodium
# Tue, 01 Dec 2020 04:10:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 01 Dec 2020 04:10:55 GMT
CMD ["php" "-a"]
# Tue, 01 Dec 2020 09:24:38 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Tue, 01 Dec 2020 09:24:38 GMT
STOPSIGNAL SIGINT
# Tue, 01 Dec 2020 09:24:39 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 01 Dec 2020 09:24:39 GMT
WORKDIR /var/www/html
# Tue, 01 Dec 2020 09:25:13 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Tue, 01 Dec 2020 09:25:13 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Mon, 07 Dec 2020 23:38:24 GMT
ENV ADMINER_VERSION=4.7.8
# Mon, 07 Dec 2020 23:38:24 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Mon, 07 Dec 2020 23:38:24 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Mon, 07 Dec 2020 23:38:26 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Mon, 07 Dec 2020 23:38:26 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Mon, 07 Dec 2020 23:38:26 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Mon, 07 Dec 2020 23:38:26 GMT
USER adminer
# Mon, 07 Dec 2020 23:38:26 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Mon, 07 Dec 2020 23:38:27 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:d6ca64ac6f4b6382142ce9a3501652938130a6ec4bb02f3f455ee1f980834cfe`  
		Last Modified: Thu, 22 Oct 2020 02:00:57 GMT  
		Size: 2.8 MB (2791407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30be8ffd290910905a5fb7cbb70252eb0f59edb09db20bdc21f3b65456acc28f`  
		Last Modified: Thu, 22 Oct 2020 05:10:23 GMT  
		Size: 1.4 MB (1439641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d58e2433b13446c863e85b34f8e4c93ca9d5b3b93d2bac415fd9cdf77bcec4`  
		Last Modified: Thu, 22 Oct 2020 05:10:21 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5729dcb8d303f82a7f8cf3df49048e34ce8ee89f79155fb08a475da46b64308`  
		Last Modified: Thu, 22 Oct 2020 05:10:21 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ffdca9b500ff910069fefe63b455206db2cf0fa00dc6b7c7d53219dfaf7f5b`  
		Last Modified: Tue, 01 Dec 2020 07:15:13 GMT  
		Size: 10.3 MB (10338561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c682383cda14fca62843652d7478a26995cfbbfbcb457985de4ca5cfb77de751`  
		Last Modified: Tue, 01 Dec 2020 07:15:12 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57833a53685f649182bdbb4194ba35390c17fa65a6b09c4e377a42a5f9aaca30`  
		Last Modified: Tue, 01 Dec 2020 07:15:18 GMT  
		Size: 14.9 MB (14942640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7003874a29c37e250b24c310b448d1c36607cdb1b43128071780d5fd0a0dc3e1`  
		Last Modified: Tue, 01 Dec 2020 07:15:12 GMT  
		Size: 2.3 KB (2259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fcfab619124f72931608ea142c1cd80a26871e1631380720b6be739170e21b6`  
		Last Modified: Tue, 01 Dec 2020 07:15:12 GMT  
		Size: 16.9 KB (16924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055719a49e04df90bb23499c98da9779637e3b44446a60f202283f57e4b29b04`  
		Last Modified: Tue, 01 Dec 2020 09:26:14 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2b0f52d9f107a35a34b4f8c69abbdf24f2de8a0431c812d74cb6dd3cbf8bf2`  
		Last Modified: Tue, 01 Dec 2020 09:26:13 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4edb5ffb9c3f753b4991debfaeef5c535ae5d689a18b7fff9f0b042c5883865`  
		Last Modified: Tue, 01 Dec 2020 09:26:14 GMT  
		Size: 4.5 MB (4519100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9258866f679eb2cbc89aa311d5d2dad0c146a7e9f61c9e805b63d7f324d2afb0`  
		Last Modified: Tue, 01 Dec 2020 09:26:13 GMT  
		Size: 1.5 KB (1472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:904e3ae5079e7cd06213e6912d4237663cff97a37e1ed247e24b7f455951eafe`  
		Last Modified: Mon, 07 Dec 2020 23:38:45 GMT  
		Size: 570.9 KB (570859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:362b319c8a865e06c57265a80b857954a02a4e09ffe3eda699eede128dcdef90`  
		Last Modified: Mon, 07 Dec 2020 23:38:45 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:standalone` - linux; ppc64le

```console
$ docker pull adminer@sha256:73feff7b317d1078b173d0c1dc928c14bf61e94b4562a0a79132b9dac74739aa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 MB (35029016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2bacaef82d901426ed9bf50182af16a98e04172b1d2dac51b87db0885487f72`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 22 Oct 2020 11:00:06 GMT
ADD file:176e047fab2c1828575bffa6b14773efa297b7ecf312d86103c5dd4f78ec8027 in / 
# Thu, 22 Oct 2020 11:00:17 GMT
CMD ["/bin/sh"]
# Fri, 23 Oct 2020 00:21:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 23 Oct 2020 00:21:18 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 23 Oct 2020 00:21:30 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 23 Oct 2020 00:21:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 23 Oct 2020 00:21:44 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 23 Oct 2020 00:21:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 23 Oct 2020 00:21:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 23 Oct 2020 00:21:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 23 Oct 2020 00:34:37 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 01 Dec 2020 03:52:39 GMT
ENV PHP_VERSION=7.4.13
# Tue, 01 Dec 2020 03:52:44 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Tue, 01 Dec 2020 03:52:51 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Tue, 01 Dec 2020 03:53:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 01 Dec 2020 03:53:13 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 01 Dec 2020 03:57:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 01 Dec 2020 03:57:24 GMT
COPY multi:afab483600631d4d87fe030871bbb016f1c2b73c0b72609d857bace419af7f5d in /usr/local/bin/ 
# Tue, 01 Dec 2020 03:57:33 GMT
RUN docker-php-ext-enable sodium
# Tue, 01 Dec 2020 03:57:36 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 01 Dec 2020 03:57:39 GMT
CMD ["php" "-a"]
# Tue, 01 Dec 2020 07:09:03 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Tue, 01 Dec 2020 07:09:12 GMT
STOPSIGNAL SIGINT
# Tue, 01 Dec 2020 07:09:25 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 01 Dec 2020 07:09:32 GMT
WORKDIR /var/www/html
# Tue, 01 Dec 2020 07:10:30 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Tue, 01 Dec 2020 07:10:33 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Tue, 08 Dec 2020 00:16:36 GMT
ENV ADMINER_VERSION=4.7.8
# Tue, 08 Dec 2020 00:16:38 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Tue, 08 Dec 2020 00:16:41 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Tue, 08 Dec 2020 00:16:53 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Tue, 08 Dec 2020 00:16:54 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 08 Dec 2020 00:16:58 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Tue, 08 Dec 2020 00:17:11 GMT
USER adminer
# Tue, 08 Dec 2020 00:17:16 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 08 Dec 2020 00:17:18 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:692a9d763e196c85d79fc3e45b316b1bb557c93ba88a3c8ebf679a585d1efe73`  
		Last Modified: Thu, 22 Oct 2020 11:02:06 GMT  
		Size: 2.8 MB (2803218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0285d6f06f3beb1c140c055210664c441b93dd4f2037177a5396bce94ca16ce5`  
		Last Modified: Fri, 23 Oct 2020 01:34:08 GMT  
		Size: 1.4 MB (1383187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a6459a3bf272daa53ff4ba97cc849676f497de9f78d8e9378ec02552293f175`  
		Last Modified: Fri, 23 Oct 2020 01:34:07 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16cff6064dc29d3f629d353736c1cac074caa5b50738422adb84de99a019bb32`  
		Last Modified: Fri, 23 Oct 2020 01:34:08 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0baf560776c5dd75b5673be3d73b900119615cfc4e4fe24414486e3d1f11920`  
		Last Modified: Tue, 01 Dec 2020 05:50:29 GMT  
		Size: 10.3 MB (10338609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4d8083b683ead9a591a00aff14c8d0091665e1433d301a027b214f19cbe23f`  
		Last Modified: Tue, 01 Dec 2020 05:50:29 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7381e6ce3e117510e5a2bf102da48e3cc1b5fd3414651ec324bbe759d367be`  
		Last Modified: Tue, 01 Dec 2020 05:50:32 GMT  
		Size: 15.5 MB (15548036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8328c4e67c6b29f383993d05557e298bc834c18c00961b9ab2a1c4e4eb05b4fd`  
		Last Modified: Tue, 01 Dec 2020 05:50:28 GMT  
		Size: 2.3 KB (2259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:236813d0f57da4fa9c0d5938846f85e82a0a01ce89ca208916b8f649c0ee99fd`  
		Last Modified: Tue, 01 Dec 2020 05:50:28 GMT  
		Size: 17.0 KB (16965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acf7ec6b5baaa9faab722bfc6a7098e0871e3edb42be513e64fe8e06bc7edec1`  
		Last Modified: Tue, 01 Dec 2020 07:14:36 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c17363dc3aab754805ecdc74f39535a73cfc5f3cebe72a4cb18fdc97df1ef9fa`  
		Last Modified: Tue, 01 Dec 2020 07:14:33 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95753fdce29daf55de647d3a29a8cc07941f7bf95fec4a560b0d698478b782f3`  
		Last Modified: Tue, 01 Dec 2020 07:14:34 GMT  
		Size: 4.4 MB (4360119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cad5fcb53526734d41770680ea56047b6e13c767960fc1d0a0b8de7c7030c75`  
		Last Modified: Tue, 01 Dec 2020 07:14:33 GMT  
		Size: 1.5 KB (1474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b231a33566f06d48010343aac194149b1ce1613cf2397c67cf1be2984295f133`  
		Last Modified: Tue, 08 Dec 2020 00:18:38 GMT  
		Size: 570.9 KB (570925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628d0ad1cc992636ad6e5a1f0cf7de70d844c7cccb85cda16205dc67b167e131`  
		Last Modified: Tue, 08 Dec 2020 00:18:38 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:standalone` - linux; s390x

```console
$ docker pull adminer@sha256:6b00709e793594a51832541158adeb2ae42e00829dbfb77a54bc0eef7fd1668d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32521955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f75d1bfddd1544fe2cddf65f0baa090dfb992c4a38b43b24670dc3b1ce037d7`
-	Entrypoint: `["entrypoint.sh","docker-php-entrypoint"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Fri, 11 Dec 2020 02:09:52 GMT
ADD file:c9395a36a4e03768aabd282eb1f31705cc00181d3147222d9c940eaa5a8fd511 in / 
# Fri, 11 Dec 2020 02:09:53 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 11:30:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 11 Dec 2020 11:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 11 Dec 2020 11:30:56 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 11 Dec 2020 11:30:57 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 11 Dec 2020 11:30:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 11 Dec 2020 11:30:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Dec 2020 11:31:00 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Dec 2020 11:31:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 11 Dec 2020 12:01:46 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 11 Dec 2020 12:01:46 GMT
ENV PHP_VERSION=7.4.13
# Fri, 11 Dec 2020 12:01:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.13.tar.xz.asc
# Fri, 11 Dec 2020 12:01:48 GMT
ENV PHP_SHA256=aead303e3abac23106529560547baebbedba0bb2943b91d5aa08fff1f41680f4
# Fri, 11 Dec 2020 12:01:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 11 Dec 2020 12:01:54 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Dec 2020 12:08:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Dec 2020 12:08:47 GMT
COPY multi:afab483600631d4d87fe030871bbb016f1c2b73c0b72609d857bace419af7f5d in /usr/local/bin/ 
# Fri, 11 Dec 2020 12:08:49 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Dec 2020 12:08:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Dec 2020 12:08:50 GMT
CMD ["php" "-a"]
# Fri, 11 Dec 2020 18:43:30 GMT
RUN echo "upload_max_filesize = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /usr/local/etc/php/conf.d/0-upload_large_dumps.ini
# Fri, 11 Dec 2020 18:43:31 GMT
STOPSIGNAL SIGINT
# Fri, 11 Dec 2020 18:43:33 GMT
RUN addgroup -S adminer &&	adduser -S -G adminer adminer &&	mkdir -p /var/www/html &&	mkdir -p /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 11 Dec 2020 18:43:33 GMT
WORKDIR /var/www/html
# Fri, 11 Dec 2020 18:44:50 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 	postgresql-dev 	sqlite-dev 	unixodbc-dev 	freetds-dev &&	docker-php-ext-configure pdo_odbc --with-pdo-odbc=unixODBC,/usr &&	docker-php-ext-install 	pdo_mysql 	pdo_pgsql 	pdo_sqlite 	pdo_odbc 	pdo_dblib &&	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" &&	apk add --virtual .phpexts-rundeps $runDeps &&	apk del .build-deps
# Fri, 11 Dec 2020 18:44:50 GMT
COPY multi:3020a2cf8da93deb4663b2b608f3156b5f8da81b19c0fa615f495168d48abf9c in /var/www/html/ 
# Fri, 11 Dec 2020 18:44:51 GMT
ENV ADMINER_VERSION=4.7.8
# Fri, 11 Dec 2020 18:44:52 GMT
ENV ADMINER_DOWNLOAD_SHA256=eadca9f2194702a4c0bc74ad02846bf88fdf521128c205ac0ec2c345489b1384
# Fri, 11 Dec 2020 18:44:52 GMT
ENV ADMINER_SRC_DOWNLOAD_SHA256=051544a8d782174218e6c152d777ad50437711b01a010b8c174162f3c066a7c0
# Fri, 11 Dec 2020 18:44:56 GMT
RUN set -x &&	curl -fsSL https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	curl -fsSL https://github.com/vrana/adminer/archive/v$ADMINER_VERSION.tar.gz -o source.tar.gz &&	echo "$ADMINER_SRC_DOWNLOAD_SHA256  source.tar.gz" |sha256sum -c - &&	tar xzf source.tar.gz --strip-components=1 "adminer-$ADMINER_VERSION/designs/" "adminer-$ADMINER_VERSION/plugins/" &&	rm source.tar.gz
# Fri, 11 Dec 2020 18:44:57 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 11 Dec 2020 18:44:57 GMT
ENTRYPOINT ["entrypoint.sh" "docker-php-entrypoint"]
# Fri, 11 Dec 2020 18:44:58 GMT
USER adminer
# Fri, 11 Dec 2020 18:44:59 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Fri, 11 Dec 2020 18:44:59 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:7c2470fe3d16cb70fca0826168095a96838b1322a8cd1502b28284ee8561b491`  
		Last Modified: Fri, 11 Dec 2020 02:10:27 GMT  
		Size: 2.6 MB (2565988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a23c8359d30ae261ad953f292e6681a71ebc7388607b74d901bbc07f71e1311`  
		Last Modified: Fri, 11 Dec 2020 13:48:01 GMT  
		Size: 1.4 MB (1382587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01422c3e898d3241d4134256bf0d911b0752823227af04614187c79c187e2843`  
		Last Modified: Fri, 11 Dec 2020 13:48:03 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a0be2077abd44f96e50bdebb1ed93a6e2b8d504761c23fa0e5e9b87045ca38`  
		Last Modified: Fri, 11 Dec 2020 13:48:01 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267bafe0bb23009994a23ad5cdcc3b4d425f186f0e488b5f7461463ad1b53814`  
		Last Modified: Fri, 11 Dec 2020 13:50:24 GMT  
		Size: 10.3 MB (10338590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36304b0fbddac7ce44edacaedb902676688cfc3bb7082576f6b57eed0ccc133e`  
		Last Modified: Fri, 11 Dec 2020 13:50:25 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fa33489075ff6318ffc5a7cf5c94cb4ce65ccfc82b5970cc91628780c130aae`  
		Last Modified: Fri, 11 Dec 2020 13:50:26 GMT  
		Size: 13.5 MB (13485898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155ae451461e50390ae0db27a78a329e87a86b9f9eb04f6db81fcc27430f2d51`  
		Last Modified: Fri, 11 Dec 2020 13:50:24 GMT  
		Size: 2.3 KB (2257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b379111cc7023c652243c4d9234de47984fa307030d667bf14e5d12889ec8180`  
		Last Modified: Fri, 11 Dec 2020 13:50:24 GMT  
		Size: 16.9 KB (16879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a18e16d8efd7f249149e2d38813d86590cc4a55f23d8c5bbba970725422ea51`  
		Last Modified: Fri, 11 Dec 2020 18:47:13 GMT  
		Size: 310.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ba44137233477a93edb1e0cc94bee3ce4dafaed9ff932d21594190f861ef75`  
		Last Modified: Fri, 11 Dec 2020 18:47:13 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cba732448866bbb0e567b7510578f951e9cf0bc258588c8e898be1606e3a3eb`  
		Last Modified: Fri, 11 Dec 2020 18:47:11 GMT  
		Size: 4.2 MB (4153155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8faf5f39c5d146bc658625977adca6ce417bb45b9683bb1767b99abfea6d3d56`  
		Last Modified: Fri, 11 Dec 2020 18:47:11 GMT  
		Size: 1.5 KB (1473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008d2a285f2f6bcf687be0cb08b167a975a4d7534a16435da10ba2b75b2e2d73`  
		Last Modified: Fri, 11 Dec 2020 18:47:11 GMT  
		Size: 570.9 KB (570918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6852608d1b2324d98a56de31e6fc11ac1fe8e95f605b50c9f72db2bd5cd092`  
		Last Modified: Fri, 11 Dec 2020 18:47:12 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
