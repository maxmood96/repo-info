## `drupal:7-fpm-alpine3.20`

```console
$ docker pull drupal@sha256:0e917771d64b683042b87a1d01f1808e86803190ba5afe628c58c5f169e6f79d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `drupal:7-fpm-alpine3.20` - linux; amd64

```console
$ docker pull drupal@sha256:10a748bcd868beaac68978853969667a81490af36f6f4694137f8770d91e997f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36843993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:921524b4f4fc17d545f7255f3aa56c65e76efc0d32c7788a75e03f73e1ecf430`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 04 Dec 2024 16:27:27 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
CMD ["/bin/sh"]
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 04 Dec 2024 16:27:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 04 Dec 2024 16:27:27 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_VERSION=8.1.31
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.31.tar.xz.asc
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_SHA256=c4f244d46ba51c72f7d13d4f66ce6a9e9a8d6b669c51be35e01765ba58e7afca
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		patch 		patchutils 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	curl -fL 'https://github.com/php/php-src/commit/577b8ae4226368e66fee7a9b5c58f9e2428372fc.patch?full_index=1' -o 11678.patch; 	echo '6edc20c3bb3e7cc13515abce7f2fffa8ebea6cf7469abfbc78fcdc120350b239 *11678.patch' | sha256sum -c -; 	patch -p1 < 11678.patch; 	rm 11678.patch; 	curl -fL 'https://github.com/php/php-src/commit/67259e451d5d58b4842776c5696a66d74e157609.patch?full_index=1' -o 14834.patch; 	echo 'ed10a1b254091ad676ed204e55628ecbd6c8962004d6185a1821cedecd526c0f *14834.patch' | sha256sum -c -; 	filterdiff -x '*/NEWS' 14834.patch | patch -p1; 	rm 14834.patch; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 04 Dec 2024 16:27:27 GMT
WORKDIR /var/www/html
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
STOPSIGNAL SIGQUIT
# Wed, 04 Dec 2024 16:27:27 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 04 Dec 2024 16:27:27 GMT
CMD ["php-fpm"]
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
ENV DRUPAL_VERSION=7.103
# Wed, 04 Dec 2024 16:27:27 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.103.tar.gz
# Wed, 04 Dec 2024 16:27:27 GMT
ENV DRUPAL_MD5=9330ed0dd9926e82b06afb9cf236d5f6
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08358ca15debb36d353f504343fc9cf9f903bb95bd9e7a896c5aeb67232c6e37`  
		Last Modified: Wed, 08 Jan 2025 18:11:42 GMT  
		Size: 3.3 MB (3308799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba70851ade3e8327c1e218e6e1ece1e94396f843ac115037cd6552dd9a134f2`  
		Last Modified: Wed, 08 Jan 2025 18:11:42 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:486339850221ed0d9a334e406a75eb7aff66ba4d9ea77e133f03c870a48962ba`  
		Last Modified: Wed, 08 Jan 2025 18:11:43 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e79a1556fd4d7c107ef366163a145446bc2ea85e48aff84d6efbffa428eb80`  
		Last Modified: Wed, 08 Jan 2025 18:11:42 GMT  
		Size: 11.9 MB (11937874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61387e69ee66777349e5234145acb12f447d5aa59d24d5e8b3c9db840d764545`  
		Last Modified: Wed, 08 Jan 2025 18:11:42 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:828fbe8408adefc58e756d567db70ff53128284fc95b4395543b97c5279bb97b`  
		Last Modified: Wed, 08 Jan 2025 18:11:43 GMT  
		Size: 12.6 MB (12614173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b85eecf86aaa1fd594ec4cceb0ebd5312b902bdf465e5be4e2c141b8bf40a5`  
		Last Modified: Wed, 08 Jan 2025 18:11:43 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38aed69cfe4a3feb514661ab97f6e6de9ddff66f649b83488a7fbc01fe384bd`  
		Last Modified: Wed, 08 Jan 2025 18:11:43 GMT  
		Size: 19.7 KB (19704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa13b0a704d540c27cc48877b6bd4a8821d3bbbca2e92e2b8e83b528af687e60`  
		Last Modified: Wed, 08 Jan 2025 18:11:44 GMT  
		Size: 8.9 KB (8876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5462d8e2f14a51289a3489990f16327ea6f65404ae85845de6b5a70b4ea1314`  
		Last Modified: Wed, 08 Jan 2025 18:23:53 GMT  
		Size: 1.9 MB (1894866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9feb6a88831424652d2913f4caf28faeeb89c6ef5bff066a974f56e11b134006`  
		Last Modified: Wed, 08 Jan 2025 18:23:53 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2edd13e6eb604564c70f4e4b6279951f78c156c58441678cd369272c700d907`  
		Last Modified: Wed, 08 Jan 2025 18:23:53 GMT  
		Size: 3.4 MB (3429012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:221969381b6d069fe196f4415042726e20eec0686601c0f91ddd94f6a7f388f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.0 KB (302003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e62d0d2b7b8c670d56fff7a4011f8c5628a09efe9806654d83b71425674282`

```dockerfile
```

-	Layers:
	-	`sha256:a3f2fb64b0b8d8ec5ca953141a3de337a6b958164b2689f7c09762c03aefa25c`  
		Last Modified: Wed, 08 Jan 2025 18:23:53 GMT  
		Size: 279.4 KB (279427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c37bce04a55cdfb95ea8172862e8e19608020b912d329ddf3b4a204cd7a04431`  
		Last Modified: Wed, 08 Jan 2025 18:23:52 GMT  
		Size: 22.6 KB (22576 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-fpm-alpine3.20` - linux; arm variant v6

```console
$ docker pull drupal@sha256:0d37dcac08627dfa4349cb64d6dc0db01b5ac671e84795f72db9c2cec554acdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.9 MB (34871962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3226eb870db010f968c1e0c992b15d7d91225d21cf4b15a42853a8008ff20b76`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 04 Dec 2024 16:27:27 GMT
ADD alpine-minirootfs-3.20.5-armhf.tar.gz / # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
CMD ["/bin/sh"]
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 04 Dec 2024 16:27:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 04 Dec 2024 16:27:27 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_VERSION=8.1.31
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.31.tar.xz.asc
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_SHA256=c4f244d46ba51c72f7d13d4f66ce6a9e9a8d6b669c51be35e01765ba58e7afca
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		patch 		patchutils 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	curl -fL 'https://github.com/php/php-src/commit/577b8ae4226368e66fee7a9b5c58f9e2428372fc.patch?full_index=1' -o 11678.patch; 	echo '6edc20c3bb3e7cc13515abce7f2fffa8ebea6cf7469abfbc78fcdc120350b239 *11678.patch' | sha256sum -c -; 	patch -p1 < 11678.patch; 	rm 11678.patch; 	curl -fL 'https://github.com/php/php-src/commit/67259e451d5d58b4842776c5696a66d74e157609.patch?full_index=1' -o 14834.patch; 	echo 'ed10a1b254091ad676ed204e55628ecbd6c8962004d6185a1821cedecd526c0f *14834.patch' | sha256sum -c -; 	filterdiff -x '*/NEWS' 14834.patch | patch -p1; 	rm 14834.patch; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 04 Dec 2024 16:27:27 GMT
WORKDIR /var/www/html
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
STOPSIGNAL SIGQUIT
# Wed, 04 Dec 2024 16:27:27 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 04 Dec 2024 16:27:27 GMT
CMD ["php-fpm"]
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
ENV DRUPAL_VERSION=7.103
# Wed, 04 Dec 2024 16:27:27 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.103.tar.gz
# Wed, 04 Dec 2024 16:27:27 GMT
ENV DRUPAL_MD5=9330ed0dd9926e82b06afb9cf236d5f6
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:27a1f2308f194d2c8cfe617a324e0078d055d65032c6c342eae11afb7a8d38c0`  
		Last Modified: Wed, 08 Jan 2025 17:23:56 GMT  
		Size: 3.4 MB (3371473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db6ffe3ef654cff5545ca59dc5f06633dd6a45d737ad50c60dbdf1cfaa7c1cd`  
		Last Modified: Wed, 08 Jan 2025 19:01:55 GMT  
		Size: 3.3 MB (3291511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb0b3742a8730e352c2d2f9b2b074af69eca367f405a0f860eb4588c6dc8e881`  
		Last Modified: Wed, 08 Jan 2025 19:01:55 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536a818f8e79c0c89eeb3c2062540dc8de02edfa1d91832c4872509e9271ef3c`  
		Last Modified: Wed, 08 Jan 2025 19:01:55 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf3dee05825bace399bd47382253b68249424d0f4b78a377531136d55882ce0`  
		Last Modified: Wed, 08 Jan 2025 20:49:45 GMT  
		Size: 11.9 MB (11937870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948d78e8853a9a5bbc8290dad64d2990df8e6f8569c6acc826b1a3ae5b220220`  
		Last Modified: Wed, 08 Jan 2025 20:49:44 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b1b79f09ea285d175a7709a9c447b53d87aa9a736b44a8c4a54d8c1a172deb2`  
		Last Modified: Wed, 08 Jan 2025 20:53:15 GMT  
		Size: 11.4 MB (11438778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1e7f079f180bff1a729464848883aec6b362142cb9f3e51faa1272ebee279e`  
		Last Modified: Wed, 08 Jan 2025 20:53:15 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d55f1460b70e1b9c82724fd08d0485ab0b478c40e81ffad445f164ec20bd5315`  
		Last Modified: Wed, 08 Jan 2025 20:53:15 GMT  
		Size: 19.5 KB (19497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3dd2f89644c3a7f4280039f9360f1eea4b9a20e5e35fee776138f01a8212a5`  
		Last Modified: Wed, 08 Jan 2025 20:53:15 GMT  
		Size: 8.9 KB (8877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b1b7ecdf6e34ac707826a85ecc27fe5286aac7fa9adc7e1a6f685e3c7214f3`  
		Last Modified: Thu, 09 Jan 2025 09:21:17 GMT  
		Size: 1.4 MB (1370500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11d3d68ecd1643fbbb658355050745200431c2bbc60e85d9da801e5176c2aef0`  
		Last Modified: Thu, 09 Jan 2025 09:21:16 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0ed1b63c4ce52fca608338f8647cce6573bcf90d1b12b7834bbf7bd7346e72`  
		Last Modified: Thu, 09 Jan 2025 09:21:17 GMT  
		Size: 3.4 MB (3429012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:136d279db4a7d4caaee076e2efdc6242016cff594c12fcac3cb75687d2dbaf8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.5 KB (22463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38362636964f6150d8e30b9ef13c9fd2557878df5adfe60f3692dfbbd4f2aebc`

```dockerfile
```

-	Layers:
	-	`sha256:eb47375ee0e269b29ebfef4b2b12da3d1f2931a80dd5f659142eb2bf603d72ad`  
		Last Modified: Thu, 09 Jan 2025 09:21:16 GMT  
		Size: 22.5 KB (22463 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-fpm-alpine3.20` - linux; arm variant v7

```console
$ docker pull drupal@sha256:fef152f715a732af87917c17ae8387e2dd434db779c321b22b2718b8791091ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.6 MB (33580118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d51c060d490d19c0a2349d9d7bbf9b559be007b08933e938f277441dc7e137`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 04 Dec 2024 16:27:27 GMT
ADD alpine-minirootfs-3.20.5-armv7.tar.gz / # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
CMD ["/bin/sh"]
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 04 Dec 2024 16:27:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 04 Dec 2024 16:27:27 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_VERSION=8.1.31
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.31.tar.xz.asc
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_SHA256=c4f244d46ba51c72f7d13d4f66ce6a9e9a8d6b669c51be35e01765ba58e7afca
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		patch 		patchutils 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	curl -fL 'https://github.com/php/php-src/commit/577b8ae4226368e66fee7a9b5c58f9e2428372fc.patch?full_index=1' -o 11678.patch; 	echo '6edc20c3bb3e7cc13515abce7f2fffa8ebea6cf7469abfbc78fcdc120350b239 *11678.patch' | sha256sum -c -; 	patch -p1 < 11678.patch; 	rm 11678.patch; 	curl -fL 'https://github.com/php/php-src/commit/67259e451d5d58b4842776c5696a66d74e157609.patch?full_index=1' -o 14834.patch; 	echo 'ed10a1b254091ad676ed204e55628ecbd6c8962004d6185a1821cedecd526c0f *14834.patch' | sha256sum -c -; 	filterdiff -x '*/NEWS' 14834.patch | patch -p1; 	rm 14834.patch; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 04 Dec 2024 16:27:27 GMT
WORKDIR /var/www/html
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
STOPSIGNAL SIGQUIT
# Wed, 04 Dec 2024 16:27:27 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 04 Dec 2024 16:27:27 GMT
CMD ["php-fpm"]
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
ENV DRUPAL_VERSION=7.103
# Wed, 04 Dec 2024 16:27:27 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.103.tar.gz
# Wed, 04 Dec 2024 16:27:27 GMT
ENV DRUPAL_MD5=9330ed0dd9926e82b06afb9cf236d5f6
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:c8a32ed454e751770c0976636b8d0d0fccc4f778a2dd26c428067d613be1a299`  
		Last Modified: Wed, 08 Jan 2025 17:34:15 GMT  
		Size: 3.1 MB (3095514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59598ed4d46933f984783e283ed636ac43c785dd3207a5432bcc816f12d3e64`  
		Last Modified: Wed, 08 Jan 2025 19:04:10 GMT  
		Size: 3.1 MB (3098287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395c20ee4940a4e59421ae1219a3af584a15664ef7e2cac6f928fe961a0dbe08`  
		Last Modified: Wed, 08 Jan 2025 19:04:10 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee856b900e721e0ee0e69e264eac4529da212f3087333fa1155fcba6c61c4c7e`  
		Last Modified: Wed, 08 Jan 2025 19:04:10 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d555b78078ca4545f4f62b122f86cee51280043410cb393d2eed219378921415`  
		Last Modified: Wed, 08 Jan 2025 20:55:18 GMT  
		Size: 11.9 MB (11937873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39dbb78b392c9f03c5844605504ffcae38ddee07ee76120344b6aff1aeb6e8af`  
		Last Modified: Wed, 08 Jan 2025 20:55:18 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0936e589e7ff944d98dbf563208295402de292ca524940aa160e0db312a5e74`  
		Last Modified: Wed, 08 Jan 2025 20:58:44 GMT  
		Size: 10.7 MB (10724726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35fafcf3edbb5831ceb5c666d4546d70fad8280905a6006872448ecd621c1378`  
		Last Modified: Wed, 08 Jan 2025 20:58:43 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6dbbe76daa4d7bf1a95135fad3ee103dce31b34a61dbcc3a7bfeea523de24ca`  
		Last Modified: Wed, 08 Jan 2025 20:58:44 GMT  
		Size: 19.5 KB (19512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296a8048134d7a49ceb18bce4fae0501a5264ee56c277f5cc58d98e1aaa37760`  
		Last Modified: Wed, 08 Jan 2025 20:58:44 GMT  
		Size: 8.9 KB (8875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773b9b8af1ae60f7c3c77953bdea45ab19444f28e8cde2f77650687228b2942a`  
		Last Modified: Thu, 09 Jan 2025 10:16:36 GMT  
		Size: 1.3 MB (1261885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d6a3da4e69b1780595db05e3b6c6505dea5b1ac4d874a699dfd79b537cbb26`  
		Last Modified: Thu, 09 Jan 2025 10:16:36 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d842cfb7996a3f743012284ebc59fe6b5d7215a4ca36fda11392741542f57254`  
		Last Modified: Thu, 09 Jan 2025 10:16:36 GMT  
		Size: 3.4 MB (3429009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:9586992b8e8fc94541fd88608e1b84550cff55e2233115fa94ab0f229ba84f8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.3 KB (299280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff64d75f0d850b5d913ffdbb6e5adb872941577a26048b6ce6c5b79d982b38ba`

```dockerfile
```

-	Layers:
	-	`sha256:522aecf42a771b83da184acaa98835c936cea4377160424c79787b5cf5d6dad1`  
		Last Modified: Thu, 09 Jan 2025 10:16:35 GMT  
		Size: 276.6 KB (276602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97b9984d00d820e22df4aa3f0f5fdecf0349ecb79f26c63ddc96285d488a38fc`  
		Last Modified: Thu, 09 Jan 2025 10:16:35 GMT  
		Size: 22.7 KB (22678 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-fpm-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:cd56faa7f89a1af2085a22ed9ca0b20ef234da37cb26fb2ce8aa2e37c9e6385a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37686553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbb678b782b044b4a8d701187928c87110e3c39f5073db8583852e9b062b2256`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 04 Dec 2024 16:27:27 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
CMD ["/bin/sh"]
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 04 Dec 2024 16:27:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 04 Dec 2024 16:27:27 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_VERSION=8.1.31
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.31.tar.xz.asc
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_SHA256=c4f244d46ba51c72f7d13d4f66ce6a9e9a8d6b669c51be35e01765ba58e7afca
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		patch 		patchutils 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	curl -fL 'https://github.com/php/php-src/commit/577b8ae4226368e66fee7a9b5c58f9e2428372fc.patch?full_index=1' -o 11678.patch; 	echo '6edc20c3bb3e7cc13515abce7f2fffa8ebea6cf7469abfbc78fcdc120350b239 *11678.patch' | sha256sum -c -; 	patch -p1 < 11678.patch; 	rm 11678.patch; 	curl -fL 'https://github.com/php/php-src/commit/67259e451d5d58b4842776c5696a66d74e157609.patch?full_index=1' -o 14834.patch; 	echo 'ed10a1b254091ad676ed204e55628ecbd6c8962004d6185a1821cedecd526c0f *14834.patch' | sha256sum -c -; 	filterdiff -x '*/NEWS' 14834.patch | patch -p1; 	rm 14834.patch; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 04 Dec 2024 16:27:27 GMT
WORKDIR /var/www/html
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
STOPSIGNAL SIGQUIT
# Wed, 04 Dec 2024 16:27:27 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 04 Dec 2024 16:27:27 GMT
CMD ["php-fpm"]
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
ENV DRUPAL_VERSION=7.103
# Wed, 04 Dec 2024 16:27:27 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.103.tar.gz
# Wed, 04 Dec 2024 16:27:27 GMT
ENV DRUPAL_MD5=9330ed0dd9926e82b06afb9cf236d5f6
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Wed, 08 Jan 2025 17:24:05 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dbfea75779fb9f51b30df44aa75d799257f21786a16d817ec263eb6cb4d24df`  
		Last Modified: Wed, 08 Jan 2025 18:59:13 GMT  
		Size: 3.4 MB (3360616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47781173f5085c5bf81fea23c55143896e3f61e88db6ca44fe803f5cff0e87b7`  
		Last Modified: Wed, 08 Jan 2025 18:59:13 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c52892499eb092197769cb95ccbc932a1373115445d0425ff828aa7d428bb5`  
		Last Modified: Wed, 08 Jan 2025 18:59:13 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba32531a0a870cf3cebdbd844bce6f07a46f9d034cbca2e18cb44cacc1c32ab`  
		Last Modified: Wed, 08 Jan 2025 21:08:42 GMT  
		Size: 11.9 MB (11937874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e240a93377926ffb348c84a1a7115d119b7e5026d1289a276824dd6e58fe6875`  
		Last Modified: Wed, 08 Jan 2025 21:08:41 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:876fb6ee0313c00eeb4bf7a1ec0dbbea7587885c1676293b10c4c6b6cf36177c`  
		Last Modified: Wed, 08 Jan 2025 21:13:00 GMT  
		Size: 12.7 MB (12665115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f641a1c84b11cbba1d12336d661ce1d9f4f27e076a6441c55cb50170eb48e45`  
		Last Modified: Wed, 08 Jan 2025 21:12:59 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea285d9cfc7edcb0b3456bc2d25532d0e6c27c8e6759724ad5c5b4e9499b0d49`  
		Last Modified: Wed, 08 Jan 2025 21:12:59 GMT  
		Size: 19.5 KB (19479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa365fccb7868b1aa40c5791e385ae1fde552a5cb4307b1f2de7349f64c6726`  
		Last Modified: Wed, 08 Jan 2025 21:12:59 GMT  
		Size: 8.9 KB (8879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3ba7813a4f22a2e14ec565cbe5b17db65e0f3c8e4ce32bcd64c07ea53a1972`  
		Last Modified: Thu, 09 Jan 2025 06:59:44 GMT  
		Size: 2.2 MB (2170373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8ea7f567d02997bd3062a71db5501f565a17151abee394a68888ac32f75c67`  
		Last Modified: Thu, 09 Jan 2025 06:59:43 GMT  
		Size: 308.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b6308681abd9343ffa0e2dfd0c96478335a2c941ef80fafc77800f7c74fabf`  
		Last Modified: Thu, 09 Jan 2025 06:59:44 GMT  
		Size: 3.4 MB (3429010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:4b1f56153fabaee0b95191bf5ce6a92065b3fd57b1b352dffee0d8662cbbc24c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.3 KB (299332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ff72ba2a996db050fabe0ede516b09e8413fe34db39b260daf603aeb0cefe61`

```dockerfile
```

-	Layers:
	-	`sha256:8b269add19f9caf8b3e6d16758973707891aadb3172e46f4c7f36e1f0fdd0ec8`  
		Last Modified: Thu, 09 Jan 2025 06:59:43 GMT  
		Size: 276.6 KB (276622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15ee815b7934d85a24268626cb4a3bede03a33b0339d35e04c487eaf66a86eac`  
		Last Modified: Thu, 09 Jan 2025 06:59:43 GMT  
		Size: 22.7 KB (22710 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-fpm-alpine3.20` - linux; 386

```console
$ docker pull drupal@sha256:a77377c4c6a39913b24bcd5ba179566bc40371af9dc8f1b77a143351905c0446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37131450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e66fdb368fc0f51ab8b38592b6a6581301953cd9dd69999709303a542ede6ec5`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 04 Dec 2024 16:27:27 GMT
ADD alpine-minirootfs-3.20.5-x86.tar.gz / # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
CMD ["/bin/sh"]
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 04 Dec 2024 16:27:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 04 Dec 2024 16:27:27 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_VERSION=8.1.31
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.31.tar.xz.asc
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_SHA256=c4f244d46ba51c72f7d13d4f66ce6a9e9a8d6b669c51be35e01765ba58e7afca
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		patch 		patchutils 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	curl -fL 'https://github.com/php/php-src/commit/577b8ae4226368e66fee7a9b5c58f9e2428372fc.patch?full_index=1' -o 11678.patch; 	echo '6edc20c3bb3e7cc13515abce7f2fffa8ebea6cf7469abfbc78fcdc120350b239 *11678.patch' | sha256sum -c -; 	patch -p1 < 11678.patch; 	rm 11678.patch; 	curl -fL 'https://github.com/php/php-src/commit/67259e451d5d58b4842776c5696a66d74e157609.patch?full_index=1' -o 14834.patch; 	echo 'ed10a1b254091ad676ed204e55628ecbd6c8962004d6185a1821cedecd526c0f *14834.patch' | sha256sum -c -; 	filterdiff -x '*/NEWS' 14834.patch | patch -p1; 	rm 14834.patch; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 04 Dec 2024 16:27:27 GMT
WORKDIR /var/www/html
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
STOPSIGNAL SIGQUIT
# Wed, 04 Dec 2024 16:27:27 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 04 Dec 2024 16:27:27 GMT
CMD ["php-fpm"]
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
ENV DRUPAL_VERSION=7.103
# Wed, 04 Dec 2024 16:27:27 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.103.tar.gz
# Wed, 04 Dec 2024 16:27:27 GMT
ENV DRUPAL_MD5=9330ed0dd9926e82b06afb9cf236d5f6
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:6d632fc6244662e41ee3b3f29090684a520e615dc5c282638a7587366dcd4fb9`  
		Last Modified: Wed, 08 Jan 2025 17:23:34 GMT  
		Size: 3.5 MB (3470969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110b9cc2cc78f6b5adaf3c95d1b8c7ccf41c0dc9764a126e33502b5a2ac31a68`  
		Last Modified: Wed, 08 Jan 2025 18:09:06 GMT  
		Size: 3.4 MB (3359986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f919c3a6051e84e7f322b16e35e66523aa2b5bffe1f389d3ed5071023055d3c3`  
		Last Modified: Wed, 08 Jan 2025 18:09:06 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ada4b5daec9e7e93780dd48e0c717247b7692fc87be10a7f4c9acab60843d8b`  
		Last Modified: Wed, 08 Jan 2025 18:09:06 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e57009596615908b0e4ebc3d8de086c5181f2cdf59c2d13467543350de72df1`  
		Last Modified: Wed, 08 Jan 2025 18:09:07 GMT  
		Size: 11.9 MB (11937874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4fe0ea2de9eb59bf391d71ef0196eed640617355d6ac2eb91864ab08e1e320e`  
		Last Modified: Wed, 08 Jan 2025 18:09:07 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad0028afb2e44125a475ecd7dfadac6bbf94552b59316908fb9c4d568fe56939`  
		Last Modified: Wed, 08 Jan 2025 18:09:07 GMT  
		Size: 12.9 MB (12946650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b0e1373c5e1836fba97899c58c95693bfebb9f3bda1942e40487107c252199`  
		Last Modified: Wed, 08 Jan 2025 18:09:07 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb902f81bc57b79a6d54dd344ee5ebd7b8be028505a8981db7d6d01dcc75846`  
		Last Modified: Wed, 08 Jan 2025 18:09:08 GMT  
		Size: 19.7 KB (19708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ca107a4b28080c22f6f9a096c2e6c46025dee25a696838fa52b0b894d2e616`  
		Last Modified: Wed, 08 Jan 2025 18:09:08 GMT  
		Size: 8.9 KB (8875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e36c2b95b25364745026151f7b6b233191fbb67c368f84a2caeb5986acce7a5`  
		Last Modified: Wed, 08 Jan 2025 18:23:48 GMT  
		Size: 2.0 MB (1953943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acd799bf97d75e17eb78302821b105a5a87736c6b232ec8044bd7ea205c60c3`  
		Last Modified: Wed, 08 Jan 2025 18:23:48 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dedbad2b93cbf4ce6e93c3c14595c16965872ae90a43427c1ab2dbd36cff973`  
		Last Modified: Wed, 08 Jan 2025 18:23:49 GMT  
		Size: 3.4 MB (3429012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:d52a97364e481346cbad5989efde362134945e89bd273554fc3e5b50d392c78d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.9 KB (301941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cdb387a8d8e44fc50361985bfb7478052355ec311b536f6a5a243ae4034e3a8`

```dockerfile
```

-	Layers:
	-	`sha256:5c632f64a7c8971801e2e0d9dc7ceb39d48792bf31aab46b60919651e472b79b`  
		Last Modified: Wed, 08 Jan 2025 18:23:48 GMT  
		Size: 279.4 KB (279402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bc0c631bd1c9eb9ab557f288b52838abb1f1e557c1fec2242c9547b2db2a90a`  
		Last Modified: Wed, 08 Jan 2025 18:23:48 GMT  
		Size: 22.5 KB (22539 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-fpm-alpine3.20` - linux; ppc64le

```console
$ docker pull drupal@sha256:fadc8df838b2e0a71a16162cae755e24fe777235d4ade421d53359e172a066df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37138586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88ad15bd3c6c0927b339b30009ce43a37232a3abc48c19eca83a5b5663f268c8`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 04 Dec 2024 16:27:27 GMT
ADD alpine-minirootfs-3.20.5-ppc64le.tar.gz / # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
CMD ["/bin/sh"]
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 04 Dec 2024 16:27:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 04 Dec 2024 16:27:27 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_VERSION=8.1.31
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.31.tar.xz.asc
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_SHA256=c4f244d46ba51c72f7d13d4f66ce6a9e9a8d6b669c51be35e01765ba58e7afca
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		patch 		patchutils 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	curl -fL 'https://github.com/php/php-src/commit/577b8ae4226368e66fee7a9b5c58f9e2428372fc.patch?full_index=1' -o 11678.patch; 	echo '6edc20c3bb3e7cc13515abce7f2fffa8ebea6cf7469abfbc78fcdc120350b239 *11678.patch' | sha256sum -c -; 	patch -p1 < 11678.patch; 	rm 11678.patch; 	curl -fL 'https://github.com/php/php-src/commit/67259e451d5d58b4842776c5696a66d74e157609.patch?full_index=1' -o 14834.patch; 	echo 'ed10a1b254091ad676ed204e55628ecbd6c8962004d6185a1821cedecd526c0f *14834.patch' | sha256sum -c -; 	filterdiff -x '*/NEWS' 14834.patch | patch -p1; 	rm 14834.patch; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 04 Dec 2024 16:27:27 GMT
WORKDIR /var/www/html
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
STOPSIGNAL SIGQUIT
# Wed, 04 Dec 2024 16:27:27 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 04 Dec 2024 16:27:27 GMT
CMD ["php-fpm"]
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
ENV DRUPAL_VERSION=7.103
# Wed, 04 Dec 2024 16:27:27 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.103.tar.gz
# Wed, 04 Dec 2024 16:27:27 GMT
ENV DRUPAL_MD5=9330ed0dd9926e82b06afb9cf236d5f6
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:3383dff810cd4af0350465f92c0a5f925af062ceac665a36e91384093216a7db`  
		Last Modified: Wed, 08 Jan 2025 17:24:56 GMT  
		Size: 3.6 MB (3574406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac389e1bad8c901cdd7df01f96be5f8508854f3411c6da9e6e8ef6668f4b16c`  
		Last Modified: Wed, 08 Jan 2025 18:46:53 GMT  
		Size: 3.4 MB (3435551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b7f9d7dcac76616498febca2aa6101a5ff06711026417e0332b7700a8e89f8`  
		Last Modified: Wed, 08 Jan 2025 18:46:52 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3bef84277af6646e9da0330c1f81457cb9ace93a33c43f40275eb914946791c`  
		Last Modified: Wed, 08 Jan 2025 18:46:53 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0abf98a27824f897bc0af3e91c436dc9bf80f80bf5070a4da180b7773c5fa4f4`  
		Last Modified: Wed, 08 Jan 2025 20:32:41 GMT  
		Size: 11.9 MB (11937879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc96bdc5f12f132320d960a259f1460f97d4c50bcc5656cc3fa987e0856375c`  
		Last Modified: Wed, 08 Jan 2025 20:32:41 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f89089c4893af0a0a51a579a7cf428024eeaca538021511d10cdc7783aa2b2`  
		Last Modified: Wed, 08 Jan 2025 20:36:04 GMT  
		Size: 13.1 MB (13058714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac80a2d9a9cf78e4fb9c3ff9738e837b09222d5975c06a5a97b0e31664197b12`  
		Last Modified: Wed, 08 Jan 2025 20:36:03 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:780a86044a8f8f0ddaa0cd7322d83b8f75102d68abb2dcaf9f93bfb07451c771`  
		Last Modified: Wed, 08 Jan 2025 20:36:03 GMT  
		Size: 19.5 KB (19487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa1c16b0ce86a7c586dc201451045fac5e7e3e8778bd05e8330dd0ccb42222b3`  
		Last Modified: Wed, 08 Jan 2025 20:36:03 GMT  
		Size: 8.9 KB (8880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbbff037f6a372a5a469367a53aaba12e7e0c666832249eab525e352dd749dc`  
		Last Modified: Thu, 09 Jan 2025 01:35:28 GMT  
		Size: 1.7 MB (1670215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfdf2e6991bf940fee15e3e280614945de85e24d934ed07361977951e3339127`  
		Last Modified: Thu, 09 Jan 2025 01:35:28 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0482d367af77377b6ec616fbe71b6c3ba324d61e8267254724efb42fd9875ff`  
		Last Modified: Thu, 09 Jan 2025 01:35:28 GMT  
		Size: 3.4 MB (3429008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:b0be10ce2116a0d859fda9a80779be7d6f5212d2e2fd47f7119b1cfe53845c4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 KB (297273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12e8bd11c37211fc6179706ddc90296460a9dcedcee927666c4fb26dc42756d3`

```dockerfile
```

-	Layers:
	-	`sha256:631c0a83071cc51cc627ca3777e2d54e6a98d2ecc7329ec9537d59e5312b9a82`  
		Last Modified: Thu, 09 Jan 2025 01:35:27 GMT  
		Size: 274.6 KB (274649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b81c3a5c9b638e9f60ec64307464290506534c851cda1a491c3a2d6800b43ee`  
		Last Modified: Thu, 09 Jan 2025 01:35:27 GMT  
		Size: 22.6 KB (22624 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-fpm-alpine3.20` - linux; riscv64

```console
$ docker pull drupal@sha256:ddcbd5e31836a65fbb811cbc9ed79f2e331943d0b9a2f647f34e78147820407f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 MB (38047960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:365d2bab2dff2075ffcd4090a998c891c67185a74a9bef75c0196fca95deeee0`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-riscv64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 04 Dec 2024 16:27:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 04 Dec 2024 16:27:27 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_VERSION=8.1.31
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.31.tar.xz.asc
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_SHA256=c4f244d46ba51c72f7d13d4f66ce6a9e9a8d6b669c51be35e01765ba58e7afca
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		patch 		patchutils 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	curl -fL 'https://github.com/php/php-src/commit/577b8ae4226368e66fee7a9b5c58f9e2428372fc.patch?full_index=1' -o 11678.patch; 	echo '6edc20c3bb3e7cc13515abce7f2fffa8ebea6cf7469abfbc78fcdc120350b239 *11678.patch' | sha256sum -c -; 	patch -p1 < 11678.patch; 	rm 11678.patch; 	curl -fL 'https://github.com/php/php-src/commit/67259e451d5d58b4842776c5696a66d74e157609.patch?full_index=1' -o 14834.patch; 	echo 'ed10a1b254091ad676ed204e55628ecbd6c8962004d6185a1821cedecd526c0f *14834.patch' | sha256sum -c -; 	filterdiff -x '*/NEWS' 14834.patch | patch -p1; 	rm 14834.patch; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 04 Dec 2024 16:27:27 GMT
WORKDIR /var/www/html
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
STOPSIGNAL SIGQUIT
# Wed, 04 Dec 2024 16:27:27 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 04 Dec 2024 16:27:27 GMT
CMD ["php-fpm"]
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
ENV DRUPAL_VERSION=7.103
# Wed, 04 Dec 2024 16:27:27 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.103.tar.gz
# Wed, 04 Dec 2024 16:27:27 GMT
ENV DRUPAL_MD5=9330ed0dd9926e82b06afb9cf236d5f6
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:ea37667e50ca807fa8abc1caf0d21091cbbe1d66b2c217158fb3e91c2787afaf`  
		Last Modified: Tue, 12 Nov 2024 00:55:56 GMT  
		Size: 3.4 MB (3371482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8ca85c9d20c6f76d0a8087ac3a4ddd6a1e40652d189dc8dad7ca6b0737c4b0`  
		Last Modified: Tue, 12 Nov 2024 06:14:49 GMT  
		Size: 5.4 MB (5382174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d2dfe107b4bddcc389bedcee9ca3fc81f02dc0799e313c21f307ddb454b4dc`  
		Last Modified: Tue, 12 Nov 2024 06:14:47 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df7310166e795cb48e721a885b92af688db981613ad6597943011293aca738c`  
		Last Modified: Tue, 12 Nov 2024 06:14:47 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb9ea701a0e6dade687d4558cd4a6ca78c5358d1bc6fde5ba327f2283f6a7bde`  
		Last Modified: Fri, 22 Nov 2024 02:05:35 GMT  
		Size: 11.9 MB (11937856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e1dd72cb8a9fa8bbf8d3831c89ce08fcfe654cef81dac92990d05bea51238f`  
		Last Modified: Fri, 22 Nov 2024 02:05:33 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a22e99e46edf2c3ad43d1f79041c2ecd34a96a4d5630d32fb39614d355f02115`  
		Last Modified: Thu, 12 Dec 2024 21:47:11 GMT  
		Size: 12.4 MB (12422539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c4e5e6e0fc2eb4324ba5d1d814f5e2a8f1d0ccc7af73f954c0d6926f91929ad`  
		Last Modified: Thu, 12 Dec 2024 21:47:10 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aaabf3d829b071c35ff313cd8f14d01b018f0deb372640e71ef6301a65c5a5e`  
		Last Modified: Thu, 12 Dec 2024 21:47:10 GMT  
		Size: 19.4 KB (19445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4556a672046f7836b3940d45d956325efb94a75dedf649ba619a57f6f75cd4b`  
		Last Modified: Thu, 12 Dec 2024 21:47:10 GMT  
		Size: 8.9 KB (8877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e717c5ffb98354fcffab60ce6cd2957cf23ffca322f119e672afaa7dfafa1904`  
		Last Modified: Fri, 13 Dec 2024 01:05:53 GMT  
		Size: 1.5 MB (1472126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36de196a9ef0b848cdcf1e0184c46629f0d8fd883e196e64a47ade891c73efe6`  
		Last Modified: Fri, 13 Dec 2024 01:05:52 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c37d1f12f8ee610393becf2f7ce8b93a6ede9b227b936ca71e176400b1eead`  
		Last Modified: Fri, 13 Dec 2024 01:05:57 GMT  
		Size: 3.4 MB (3429009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:4d94721be3b0e77899db43f76903e7ec46dcc9eb2d10a2ec6a4d3d6fa7c701eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.0 KB (299004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea29305cd4c4dedba2a0970e72edd77084554faa86bd25e45392c8fbd2b16c25`

```dockerfile
```

-	Layers:
	-	`sha256:b729add4b874bfc9fa3a65b541d14f91477485bca34f4ea2aecc88e0ec016e27`  
		Last Modified: Fri, 13 Dec 2024 01:05:52 GMT  
		Size: 275.1 KB (275072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:444c8f8a766766571bc9c9e329bc13c47d44d3ad0a76dec2f121732852f87d09`  
		Last Modified: Fri, 13 Dec 2024 01:05:52 GMT  
		Size: 23.9 KB (23932 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-fpm-alpine3.20` - linux; s390x

```console
$ docker pull drupal@sha256:7591cd48b38e3fbabc1585ebd5196da41361c73f6720cf96496112a4d52c08a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.5 MB (36499511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8674de03351bc316aab033d36ef31aa6ea7e98e509cf2fb2d9493b16ec5329e6`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 04 Dec 2024 16:27:27 GMT
ADD alpine-minirootfs-3.20.5-s390x.tar.gz / # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
CMD ["/bin/sh"]
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 04 Dec 2024 16:27:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 04 Dec 2024 16:27:27 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_VERSION=8.1.31
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.31.tar.xz.asc
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_SHA256=c4f244d46ba51c72f7d13d4f66ce6a9e9a8d6b669c51be35e01765ba58e7afca
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		patch 		patchutils 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	curl -fL 'https://github.com/php/php-src/commit/577b8ae4226368e66fee7a9b5c58f9e2428372fc.patch?full_index=1' -o 11678.patch; 	echo '6edc20c3bb3e7cc13515abce7f2fffa8ebea6cf7469abfbc78fcdc120350b239 *11678.patch' | sha256sum -c -; 	patch -p1 < 11678.patch; 	rm 11678.patch; 	curl -fL 'https://github.com/php/php-src/commit/67259e451d5d58b4842776c5696a66d74e157609.patch?full_index=1' -o 14834.patch; 	echo 'ed10a1b254091ad676ed204e55628ecbd6c8962004d6185a1821cedecd526c0f *14834.patch' | sha256sum -c -; 	filterdiff -x '*/NEWS' 14834.patch | patch -p1; 	rm 14834.patch; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 04 Dec 2024 16:27:27 GMT
WORKDIR /var/www/html
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
STOPSIGNAL SIGQUIT
# Wed, 04 Dec 2024 16:27:27 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 04 Dec 2024 16:27:27 GMT
CMD ["php-fpm"]
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
ENV DRUPAL_VERSION=7.103
# Wed, 04 Dec 2024 16:27:27 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.103.tar.gz
# Wed, 04 Dec 2024 16:27:27 GMT
ENV DRUPAL_MD5=9330ed0dd9926e82b06afb9cf236d5f6
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:3e71c43ed556c3ed564b517d9141db651f4134655f96c8731767c14c6dedc4d0`  
		Last Modified: Wed, 08 Jan 2025 17:25:57 GMT  
		Size: 3.5 MB (3463322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f228edf04a39559d957ef5581b08c9a7d393dc64a098575e63c061140ae78557`  
		Last Modified: Wed, 08 Jan 2025 18:50:04 GMT  
		Size: 3.5 MB (3501854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3a938ef64c5dda4d67df22456ef7b998d8d733e6b109f8565eae8077a42767`  
		Last Modified: Wed, 08 Jan 2025 18:50:04 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8665be221001567b6093cf5d6fd1080ca3c33832bf4656568c06b3f7959c83`  
		Last Modified: Wed, 08 Jan 2025 18:50:04 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc41b820b1b50fc2a3bfda067326541fad07dbdaf653ab637be18c281598c747`  
		Last Modified: Wed, 08 Jan 2025 21:07:25 GMT  
		Size: 11.9 MB (11937865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6abf2c160e3efbc9970263bd079554d333636b3ddb6ecb2065d0ffa4a2a578`  
		Last Modified: Wed, 08 Jan 2025 21:07:24 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc146e1f997a2e6f73de0504938b442e83296fa2fbcff23b338d8cedd22fb210`  
		Last Modified: Wed, 08 Jan 2025 21:10:54 GMT  
		Size: 12.6 MB (12550172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8694d2f213eba31f2f9732885cc89566b1971283c0d54b1e29145ecbe5afb6c`  
		Last Modified: Wed, 08 Jan 2025 21:10:53 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e65b6c3116ce6b7e326e6fd6b9ced5b0004cc07edff6b49c08a8bf32df394e`  
		Last Modified: Wed, 08 Jan 2025 21:10:53 GMT  
		Size: 19.5 KB (19497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5139d2ab25bc65b5456b82ee6d94c6c3c6d0ab3361c09b6aa9009e96aa367013`  
		Last Modified: Wed, 08 Jan 2025 21:10:53 GMT  
		Size: 8.9 KB (8877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88710e0697cdd67429ae36d7c99bf0132869e33a9b68cbd8a6b975e9f8d41968`  
		Last Modified: Thu, 09 Jan 2025 07:44:34 GMT  
		Size: 1.6 MB (1584459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:120f6f5bbd15365c68fd71060384200ebec005c137134183a8e7e71b6f9164af`  
		Last Modified: Thu, 09 Jan 2025 07:44:34 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b6a67dd1a346bb9d73b72ee0043b62a3629768ee20eae1df8afff3a9a6a16b5`  
		Last Modified: Thu, 09 Jan 2025 07:44:35 GMT  
		Size: 3.4 MB (3429018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:eee99ea146dfa8377f13f29212d4ea25aa89448a3950214911d3779d827e04df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.2 KB (297191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fe775fe67bc0cec280392513697aec3f411e8c8532515c19e5da0a4629598dc`

```dockerfile
```

-	Layers:
	-	`sha256:7cb01746800153a1b1d6cfe4bf38ee6cf69249ad7ecc92d990d5822e5fc0cad9`  
		Last Modified: Thu, 09 Jan 2025 07:44:34 GMT  
		Size: 274.6 KB (274615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f868ead63720ea1d618f85e5682afe0cc2ffb34436b98b9672a042df83cd7ad`  
		Last Modified: Thu, 09 Jan 2025 07:44:34 GMT  
		Size: 22.6 KB (22576 bytes)  
		MIME: application/vnd.in-toto+json
