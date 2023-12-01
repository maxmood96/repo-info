## `drupal:7-php8.1-fpm-alpine3.18`

```console
$ docker pull drupal@sha256:d882108bdf593f28d4cba07790a022df4c0cc81c68d6fdccfe507fe9915dbb9d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `drupal:7-php8.1-fpm-alpine3.18` - linux; amd64

```console
$ docker pull drupal@sha256:d4851dd66228a795b97c3af361c08a755588d8f9fb4f58669f5b367f370006c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36218550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e48ada36c352e3e7426d3fac324ec9e28046eb752de2f9f0ce4b2e81dda9b01d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 14 Jun 2023 17:25:34 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Wed, 14 Jun 2023 17:25:34 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 14 Jun 2023 17:25:34 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 14 Jun 2023 17:25:34 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_VERSION=8.1.26
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.26.tar.xz.asc
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_SHA256=17f87133596449327451ad4b8d9911bfaea59ff5109f3a6f2bb679f967a8ea0f
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 14 Jun 2023 17:25:34 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 14 Jun 2023 17:25:34 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 14 Jun 2023 17:25:34 GMT
RUN docker-php-ext-enable sodium
# Wed, 14 Jun 2023 17:25:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 14 Jun 2023 17:25:34 GMT
WORKDIR /var/www/html
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 14 Jun 2023 17:25:34 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Jun 2023 17:25:34 GMT
EXPOSE 9000
# Wed, 14 Jun 2023 17:25:34 GMT
CMD ["php-fpm"]
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 14 Jun 2023 17:25:34 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 14 Jun 2023 17:25:34 GMT
ENV DRUPAL_VERSION=7.98
# Wed, 14 Jun 2023 17:25:34 GMT
ENV DRUPAL_MD5=4139f0feecb44a53645242194809b73a
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e26b626c27026d1938a0b6bd77e36b4113da4b7a1134df8d1aa9f49658b25f`  
		Last Modified: Fri, 01 Dec 2023 00:42:07 GMT  
		Size: 2.7 MB (2679359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23427f6f19cc27aa3496173559d7fc30c2501d1d179a15b52ac1758cc1667d37`  
		Last Modified: Fri, 01 Dec 2023 00:42:07 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:938ee652f0dd66c081c31e773163d4c3d8ec979f9ced384ed270cdc5fbcbe657`  
		Last Modified: Fri, 01 Dec 2023 00:42:07 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06356221483a64a90213adafb9d379350b7aef844a42c6a42631628f70139da`  
		Last Modified: Fri, 01 Dec 2023 00:46:16 GMT  
		Size: 11.8 MB (11830201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b8c1e9f0655a900964521f2a4e485874ffc4c977cdb93344b0762d3a31bd670`  
		Last Modified: Fri, 01 Dec 2023 00:46:15 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4422d5e1975f96077f1540f5c8966c9c0661b4bfd8c342013d27a8431693d0b1`  
		Last Modified: Fri, 01 Dec 2023 00:46:42 GMT  
		Size: 12.4 MB (12426586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4d4e9e86d27a38f33c6dda2999c5287f9dddf7bae80a402c2c0dc7bb0a617b`  
		Last Modified: Fri, 01 Dec 2023 00:46:40 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83565756f3020d836bfeb2b911076d77645535466b8972bce1839818654d3b55`  
		Last Modified: Fri, 01 Dec 2023 00:46:40 GMT  
		Size: 19.0 KB (18953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa1b4e2bbc13222cb25dd869265c81e0c601010fa110778546b771ce057c7d96`  
		Last Modified: Fri, 01 Dec 2023 00:46:40 GMT  
		Size: 8.9 KB (8878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bbe85d36cca5882f1a3ee9f0462023b4440eef155ad7e00eec40b1096208792`  
		Last Modified: Fri, 01 Dec 2023 02:12:07 GMT  
		Size: 2.4 MB (2437072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19eab4d7afdcb96db473e7d413f46a66f551e19a0c626011af36586174cb0184`  
		Last Modified: Fri, 01 Dec 2023 02:12:07 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df728971162208e19df9a3c2bd6288baf96fdfba3578395d9d28d5af42780ce`  
		Last Modified: Fri, 01 Dec 2023 02:12:08 GMT  
		Size: 3.4 MB (3410292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.1-fpm-alpine3.18` - unknown; unknown

```console
$ docker pull drupal@sha256:dc4a7d8b05521261fd39dc022809b0b9a876f619de5ef4839061ab1f87255fd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.2 KB (258219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88d38e0914c64f4140344a42e5271cd347e34e8328dc6a8c74cd33678ae1a78a`

```dockerfile
```

-	Layers:
	-	`sha256:95b5bc5795ad57fa384a2dc1d903052559488f3999679ab73b841fd1afab0f52`  
		Last Modified: Fri, 01 Dec 2023 02:12:06 GMT  
		Size: 234.7 KB (234719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fddab6219c69335920e010afed76845245aa157ac135f90898cca350fc4ca9b`  
		Last Modified: Fri, 01 Dec 2023 02:12:06 GMT  
		Size: 23.5 KB (23500 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.1-fpm-alpine3.18` - linux; arm variant v6

```console
$ docker pull drupal@sha256:fcf03c41af64455d05cfa54f093b55a957783d07ffbc682c0c87156026f350ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34278118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2eb2889e3342d40a1c660f64e0303acad0aac2071827d84f48c61a5bba865a`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 14 Jun 2023 17:25:34 GMT
ADD file:dbf65487d049081dc2d39b3d99d2c64b6c89754e7e2996a46169d3512e59f32a in / 
# Wed, 14 Jun 2023 17:25:34 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 14 Jun 2023 17:25:34 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 14 Jun 2023 17:25:34 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_VERSION=8.1.26
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.26.tar.xz.asc
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_SHA256=17f87133596449327451ad4b8d9911bfaea59ff5109f3a6f2bb679f967a8ea0f
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 14 Jun 2023 17:25:34 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 14 Jun 2023 17:25:34 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 14 Jun 2023 17:25:34 GMT
RUN docker-php-ext-enable sodium
# Wed, 14 Jun 2023 17:25:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 14 Jun 2023 17:25:34 GMT
WORKDIR /var/www/html
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 14 Jun 2023 17:25:34 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Jun 2023 17:25:34 GMT
EXPOSE 9000
# Wed, 14 Jun 2023 17:25:34 GMT
CMD ["php-fpm"]
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 14 Jun 2023 17:25:34 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 14 Jun 2023 17:25:34 GMT
ENV DRUPAL_VERSION=7.98
# Wed, 14 Jun 2023 17:25:34 GMT
ENV DRUPAL_MD5=4139f0feecb44a53645242194809b73a
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:85ae953f9e6740471d4e1440b27721679dc7a511e112eb73df467a4cde26e421`  
		Last Modified: Thu, 30 Nov 2023 22:49:40 GMT  
		Size: 3.1 MB (3146870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ad3f4bb45cafc3a0c4349f9564390ff0fe5c2a3dc4287f0ddf3de8a86dcbb66`  
		Last Modified: Fri, 01 Dec 2023 00:15:00 GMT  
		Size: 2.7 MB (2685809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a06cb8c5272936441cf9c53173eed2af740b588b3a9d8bbbb0b6565f38005e36`  
		Last Modified: Fri, 01 Dec 2023 00:14:59 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6156dbc484960b6656a156d5d82d973371555039e45046b37e9af1cbfec8569`  
		Last Modified: Fri, 01 Dec 2023 00:14:59 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd1e20ee3475c24c7baf10d302c0e2d9e649ae5bc97ddb3df77764d9ecfc2ccb`  
		Last Modified: Fri, 01 Dec 2023 00:19:06 GMT  
		Size: 11.8 MB (11830194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a5f5fc8fd3476c61779c76dff5c6d3d80b0c4b67e62679e23cbc730f997537`  
		Last Modified: Fri, 01 Dec 2023 00:19:05 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11e3acc37cb6490d080a20ab6c5f9c8bc3eff1eaad544ee18363b9290c77faca`  
		Last Modified: Fri, 01 Dec 2023 00:19:32 GMT  
		Size: 11.3 MB (11327869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061a4fde7eb6aa7965f40f5704152c3bd61cd0f531e864376e484262e695fdc8`  
		Last Modified: Fri, 01 Dec 2023 00:19:30 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f542a432088cfa212883e4ef26bec0e5dba25c69a68beddf6bab4d0afc232ddb`  
		Last Modified: Fri, 01 Dec 2023 00:19:30 GMT  
		Size: 18.8 KB (18768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49bf4531d1874c42e5bfb8ec35709e450d2b4348fbd1cbf808b48ec208c06846`  
		Last Modified: Fri, 01 Dec 2023 00:19:30 GMT  
		Size: 8.9 KB (8877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bde6fe74a65263f81a7de4e316c06b47f66e952e995fc0f0d310618267693e4`  
		Last Modified: Fri, 01 Dec 2023 13:29:40 GMT  
		Size: 1.8 MB (1844662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa3c43d728d526570f90445e696061d141364470788cd9a671793c9180b6f59`  
		Last Modified: Fri, 01 Dec 2023 13:29:40 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e3012e4e3b81d09598e40d330a99234fdf00637f6744a2a2a734b7a07180971`  
		Last Modified: Fri, 01 Dec 2023 13:38:42 GMT  
		Size: 3.4 MB (3410283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:7-php8.1-fpm-alpine3.18` - linux; arm variant v7

```console
$ docker pull drupal@sha256:97ed78bac1888cecc5991e6d2ef6b55cc874a512bb98b08a7ad84bee994117ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33000469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0777ef01a086a48938c2a2a7bac6686982a710759d9900ff76602c16f2d51752`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 14 Jun 2023 17:25:34 GMT
ADD file:dcb85d43d1fb96861612c42288878b13debfa9d0b956adea1f2472d0c50f0144 in / 
# Wed, 14 Jun 2023 17:25:34 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 14 Jun 2023 17:25:34 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 14 Jun 2023 17:25:34 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_VERSION=8.1.26
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.26.tar.xz.asc
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_SHA256=17f87133596449327451ad4b8d9911bfaea59ff5109f3a6f2bb679f967a8ea0f
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 14 Jun 2023 17:25:34 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 14 Jun 2023 17:25:34 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 14 Jun 2023 17:25:34 GMT
RUN docker-php-ext-enable sodium
# Wed, 14 Jun 2023 17:25:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 14 Jun 2023 17:25:34 GMT
WORKDIR /var/www/html
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 14 Jun 2023 17:25:34 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Jun 2023 17:25:34 GMT
EXPOSE 9000
# Wed, 14 Jun 2023 17:25:34 GMT
CMD ["php-fpm"]
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 14 Jun 2023 17:25:34 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 14 Jun 2023 17:25:34 GMT
ENV DRUPAL_VERSION=7.98
# Wed, 14 Jun 2023 17:25:34 GMT
ENV DRUPAL_MD5=4139f0feecb44a53645242194809b73a
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:2387a44129d2147bd4e806bf369f3db92eb3ad3b6b8825c739db364b8baa4e26`  
		Last Modified: Thu, 30 Nov 2023 22:49:56 GMT  
		Size: 2.9 MB (2901006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:463dfc43b4287670c76354cf1d002e077c0a4b8f41207fdbd96316d0f649fdd5`  
		Last Modified: Thu, 30 Nov 2023 23:58:02 GMT  
		Size: 2.5 MB (2524902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab8445d08981ee2b82e7069c3bf290f41039993039dd9740da05b6c962c368ea`  
		Last Modified: Thu, 30 Nov 2023 23:58:01 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8472c3889e6c64cf9e26fe36cc30bf9e211560aea77f82e97443348cb5956b88`  
		Last Modified: Thu, 30 Nov 2023 23:58:00 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddd7bd20e4cda68a166659026b82c9c9f4a68e09efa30c335aa2e6a196e106b`  
		Last Modified: Fri, 01 Dec 2023 00:02:30 GMT  
		Size: 11.8 MB (11830205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50679e5dffc6e3fb50eb9d451d86580bbc128f6d24dd96688f778313a074a6e`  
		Last Modified: Fri, 01 Dec 2023 00:02:29 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30cecddb35339da764ebd2381301a7e7afa649a67ea9233b8ace46894992ec4e`  
		Last Modified: Fri, 01 Dec 2023 00:02:54 GMT  
		Size: 10.6 MB (10591241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc98d6e89f3fed1eb53eaf46b410f22fbcc475cae6f387d1030fce6ea5bcd155`  
		Last Modified: Fri, 01 Dec 2023 00:02:51 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2aab90b1b6760c363cab1699d12b02eeca800c49364bcde9062df80af4ccf45`  
		Last Modified: Fri, 01 Dec 2023 00:02:52 GMT  
		Size: 18.8 KB (18779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff84c7cbf7992beda4123b7047869d9a762e3d547dd2e45b7568584235cccfd`  
		Last Modified: Fri, 01 Dec 2023 00:02:51 GMT  
		Size: 8.9 KB (8880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0372021e5b0bf9736319954bae6bfa9395eba261d032e55510a8d55e593513fd`  
		Last Modified: Fri, 01 Dec 2023 10:42:11 GMT  
		Size: 1.7 MB (1710384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa85a249d7ef2bd627641c200ca92e7ee869653b1b63b96165e7a8901710e7dc`  
		Last Modified: Fri, 01 Dec 2023 10:42:11 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e1055bd6d412b37986599e59d9e3883e5ae4e222fb9e53a8692a59b41c6f6c`  
		Last Modified: Fri, 01 Dec 2023 10:53:22 GMT  
		Size: 3.4 MB (3410292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.1-fpm-alpine3.18` - unknown; unknown

```console
$ docker pull drupal@sha256:8cd302da5d62e02cba8e5b5cf99ea80d55a2da7d510cd9746b5bff772dfb0af8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.3 KB (254252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65c96e814a4a6f2bddbda06932712be43ae9ddd5e4293869c8cbf3b82ffda355`

```dockerfile
```

-	Layers:
	-	`sha256:2f87118377df18e78e06673895a86701c37d0ccb9040f846f6b2a8bba2003660`  
		Last Modified: Fri, 01 Dec 2023 10:53:22 GMT  
		Size: 232.3 KB (232279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79b808529ecfee940ff7a9807bc7f6583f36d0cb428488ccecd7be35aecf64e7`  
		Last Modified: Fri, 01 Dec 2023 10:53:21 GMT  
		Size: 22.0 KB (21973 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.1-fpm-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:d5e092d54f9f60de409cc8f6b10852d3dc299113d1dc9f1569b72b7903c535a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.5 MB (36522244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fda258698314bd589e094c665c0d92da33527935bbcbfbd234a5d7d002696e5`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 14 Jun 2023 17:25:34 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Wed, 14 Jun 2023 17:25:34 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 14 Jun 2023 17:25:34 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 14 Jun 2023 17:25:34 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_VERSION=8.1.26
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.26.tar.xz.asc
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_SHA256=17f87133596449327451ad4b8d9911bfaea59ff5109f3a6f2bb679f967a8ea0f
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 14 Jun 2023 17:25:34 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 14 Jun 2023 17:25:34 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 14 Jun 2023 17:25:34 GMT
RUN docker-php-ext-enable sodium
# Wed, 14 Jun 2023 17:25:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 14 Jun 2023 17:25:34 GMT
WORKDIR /var/www/html
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 14 Jun 2023 17:25:34 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Jun 2023 17:25:34 GMT
EXPOSE 9000
# Wed, 14 Jun 2023 17:25:34 GMT
CMD ["php-fpm"]
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 14 Jun 2023 17:25:34 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 14 Jun 2023 17:25:34 GMT
ENV DRUPAL_VERSION=7.98
# Wed, 14 Jun 2023 17:25:34 GMT
ENV DRUPAL_MD5=4139f0feecb44a53645242194809b73a
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec91cb5b5977bc2c77c932761c9cd04eda4b0df9636a46228a4c0af65ad1b4f3`  
		Last Modified: Fri, 01 Dec 2023 00:40:05 GMT  
		Size: 2.7 MB (2717190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1563f945b2330cf35b9fc87a3f6456664dde2d6c4b6739047a9dd457f4a3d681`  
		Last Modified: Fri, 01 Dec 2023 00:40:04 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2549a9ef4a38d3afd713cc21e4de8fdf9a61d4d4f5b2897c0de403ec047f69a`  
		Last Modified: Fri, 01 Dec 2023 00:40:03 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d10bc79efbc5193023feec864e880c28f904ef87376840e2d8ed6d89efe4162e`  
		Last Modified: Fri, 01 Dec 2023 00:44:08 GMT  
		Size: 11.8 MB (11830183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ccb8941de88b7ed8ed240c5393b81de98fef63fbcd45df98af7ba24055e022`  
		Last Modified: Fri, 01 Dec 2023 00:44:07 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e640b2719a9c451f6f08efc43e2ed9b33a84abc7e0748be9b541b2c89263d0e6`  
		Last Modified: Fri, 01 Dec 2023 00:44:32 GMT  
		Size: 12.5 MB (12494894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9894968b3f1dfe1bffaa150c532c8d89dfdfc967a4b5c599e79c52a359e40980`  
		Last Modified: Fri, 01 Dec 2023 00:44:30 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7dba04dbc3daba98d3bbff275e9fafdb9d4e08b44c556984f015c319ea39e91`  
		Last Modified: Fri, 01 Dec 2023 00:44:30 GMT  
		Size: 18.7 KB (18728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f055bc5f70dbf3faec2833f899629a5ed6ee261b932181f0a09189267af7c8a`  
		Last Modified: Fri, 01 Dec 2023 00:44:30 GMT  
		Size: 8.9 KB (8875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c3c751a1c397380a35573f5b35d0eba79b57689a38dcd2ae50d659d486596e`  
		Last Modified: Fri, 01 Dec 2023 13:05:14 GMT  
		Size: 2.7 MB (2704259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c871f4f2f84db9513a78d8a6e35ce62ef31c042430b72e2eb8013554d1741a`  
		Last Modified: Fri, 01 Dec 2023 13:05:14 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a7994573b9f8d865e5757358eb34fafc8f5fc5a822569d8f14870af6b855c1d`  
		Last Modified: Fri, 01 Dec 2023 13:05:14 GMT  
		Size: 3.4 MB (3410296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.1-fpm-alpine3.18` - unknown; unknown

```console
$ docker pull drupal@sha256:7c411fa159b6a0d53d9061b3f5444e8dd6b5ffecb349b966224ec51067ee2876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.8 KB (255766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93bd1f9a2ae8b6fea65046c86dadc35d92f06128c76de2c98bb9bec611d04f77`

```dockerfile
```

-	Layers:
	-	`sha256:c89cf078ad8959b0292d1004c3044afe94a5a584f3c7b04047007c486379cdde`  
		Last Modified: Fri, 01 Dec 2023 13:05:12 GMT  
		Size: 232.3 KB (232254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:826551b9b34e9ff6916c92283b1f6390b1a1de3f20b1434de945922bb2007b2a`  
		Last Modified: Fri, 01 Dec 2023 13:05:12 GMT  
		Size: 23.5 KB (23512 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.1-fpm-alpine3.18` - linux; 386

```console
$ docker pull drupal@sha256:d5fb4b86ba2ceadeca49ad078a83c989ab800da9fe3ad2d9eed014efde5f560a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.3 MB (36276017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d29c106cd90be40e2670ddb04ecebf231f93d5b481fa8d68a61c9811fca4848`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 14 Jun 2023 17:25:34 GMT
ADD file:92902088cd15ed8f5dca2f7fc6570fb4e4824fac8b09e091c88e96bbd0ca814b in / 
# Wed, 14 Jun 2023 17:25:34 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 14 Jun 2023 17:25:34 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 14 Jun 2023 17:25:34 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_VERSION=8.1.26
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.26.tar.xz.asc
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_SHA256=17f87133596449327451ad4b8d9911bfaea59ff5109f3a6f2bb679f967a8ea0f
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 14 Jun 2023 17:25:34 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 14 Jun 2023 17:25:34 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 14 Jun 2023 17:25:34 GMT
RUN docker-php-ext-enable sodium
# Wed, 14 Jun 2023 17:25:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 14 Jun 2023 17:25:34 GMT
WORKDIR /var/www/html
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 14 Jun 2023 17:25:34 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Jun 2023 17:25:34 GMT
EXPOSE 9000
# Wed, 14 Jun 2023 17:25:34 GMT
CMD ["php-fpm"]
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 14 Jun 2023 17:25:34 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 14 Jun 2023 17:25:34 GMT
ENV DRUPAL_VERSION=7.98
# Wed, 14 Jun 2023 17:25:34 GMT
ENV DRUPAL_MD5=4139f0feecb44a53645242194809b73a
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:4966a8bd129b0a6adf93dc295a8fbe8f665d3194a684a5ce199c1c3596dbf3d9`  
		Last Modified: Fri, 01 Dec 2023 02:04:18 GMT  
		Size: 3.2 MB (3238831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786b6949c7da1fc85a439f51aa05ace6592ed6759802ad370ed74bc4f479828b`  
		Last Modified: Fri, 01 Dec 2023 04:07:07 GMT  
		Size: 2.7 MB (2723376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27aec508afba473c67b8d2ad4216ba2489f0e9f08768454183b11877384d8139`  
		Last Modified: Fri, 01 Dec 2023 04:07:05 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55ae0822cb02fa8febaedc0ea40b1c5b2823b47b9e9f3dc9436f506df98f121`  
		Last Modified: Fri, 01 Dec 2023 04:07:05 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86efd93984488fda4c07febefb3bf48e07f9e58a815646fd296eb038add0b17e`  
		Last Modified: Fri, 01 Dec 2023 04:11:52 GMT  
		Size: 11.8 MB (11830194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711d726f1ebe168f9fb46556121c9050406a3fa9a6c1f8d1af7193097dd03f97`  
		Last Modified: Fri, 01 Dec 2023 04:11:50 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca8a1d668e9e93d2e901aa80dc6f26e20bba17eb32db327e7bdd4dd627a2d95`  
		Last Modified: Fri, 01 Dec 2023 04:12:23 GMT  
		Size: 12.6 MB (12613637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f1f393bd9679c3b547769b141b18106d472b6fafcbcb8cea636166eb6421a02`  
		Last Modified: Fri, 01 Dec 2023 04:12:19 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ece81ff10dd056bb223eca44a3904e5b27e12d089c8088c2c3477f501359b7d`  
		Last Modified: Fri, 01 Dec 2023 04:12:19 GMT  
		Size: 18.9 KB (18931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6594cb7353d194aafab0f56a2ea8bf440252cd1dc7a441c8657e72959f91bbf`  
		Last Modified: Fri, 01 Dec 2023 04:12:19 GMT  
		Size: 8.9 KB (8879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e166c1c50be37b99748474288159daa040100369ccab5f3b68bd18831886ed`  
		Last Modified: Fri, 01 Dec 2023 05:11:47 GMT  
		Size: 2.4 MB (2427105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af794e2e36aa9c32c2e77ea40d34d2a18ef0e9237d3835f97498ccfca1b01cac`  
		Last Modified: Fri, 01 Dec 2023 05:11:47 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20ee51884678f3ec970fbfdf3f197efd22be12674a873bd99cc0d88f850d6b1`  
		Last Modified: Fri, 01 Dec 2023 05:11:48 GMT  
		Size: 3.4 MB (3410283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.1-fpm-alpine3.18` - unknown; unknown

```console
$ docker pull drupal@sha256:1a70fcaaf2351861ecaa278d1b37c8f5eab83c6ce38f80c2de61083e1995f325
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 KB (23254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a06ad19ad70788f03c840e7f5813db38d2536237016c8c7dd829fb5c562e310`

```dockerfile
```

-	Layers:
	-	`sha256:18844ff83753900d127f9563e5ff56db986530d4bdfe7a2f8a5349bafc6297db`  
		Last Modified: Fri, 01 Dec 2023 05:11:46 GMT  
		Size: 23.3 KB (23254 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.1-fpm-alpine3.18` - linux; ppc64le

```console
$ docker pull drupal@sha256:ecbe8fc1abacdbe2c5a0f9c5549a6f9d826638ddb283f3e92d54c6852b50cb4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36430009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8faaf6e45487269f4fbb6b15fb8d8d0a9839701325004b32fbd77f722a964773`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 14 Jun 2023 17:25:34 GMT
ADD file:3450a1687b552498a987f87cb844b7f597c7181d7c3d31943d7b3036d5300d5e in / 
# Wed, 14 Jun 2023 17:25:34 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 14 Jun 2023 17:25:34 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 14 Jun 2023 17:25:34 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_VERSION=8.1.26
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.26.tar.xz.asc
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_SHA256=17f87133596449327451ad4b8d9911bfaea59ff5109f3a6f2bb679f967a8ea0f
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 14 Jun 2023 17:25:34 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 14 Jun 2023 17:25:34 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 14 Jun 2023 17:25:34 GMT
RUN docker-php-ext-enable sodium
# Wed, 14 Jun 2023 17:25:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 14 Jun 2023 17:25:34 GMT
WORKDIR /var/www/html
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 14 Jun 2023 17:25:34 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Jun 2023 17:25:34 GMT
EXPOSE 9000
# Wed, 14 Jun 2023 17:25:34 GMT
CMD ["php-fpm"]
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 14 Jun 2023 17:25:34 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 14 Jun 2023 17:25:34 GMT
ENV DRUPAL_VERSION=7.98
# Wed, 14 Jun 2023 17:25:34 GMT
ENV DRUPAL_MD5=4139f0feecb44a53645242194809b73a
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:4e13780adf2776477b14ef9c0f4f563f820a2fde166d472218037b979e84d31a`  
		Last Modified: Thu, 30 Nov 2023 23:20:01 GMT  
		Size: 3.3 MB (3348322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f8cb9b4da64e0956e297ed583f04085128cdc4a68dcffa3a41c639319245c27`  
		Last Modified: Fri, 01 Dec 2023 00:53:04 GMT  
		Size: 2.8 MB (2766423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e2afe36ae984e44fa290115e1355ddb9ba0833dc70a7e3e1f1ed384492c3ec`  
		Last Modified: Fri, 01 Dec 2023 00:53:04 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:233860698dd8a6e8c7a48373c7cb0a908fc5e1ad61c7ba6c0606e54226ed4c5d`  
		Last Modified: Fri, 01 Dec 2023 00:53:03 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f79fe1b5369f8a1c8e0bd6ae80a92f18975ee0b2991ae73905059b564b61bdaf`  
		Last Modified: Fri, 01 Dec 2023 00:57:55 GMT  
		Size: 11.8 MB (11830192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b78e7c03a2acc53160c3f22f7724459ead0679cda281dad1932d64f8a99f429a`  
		Last Modified: Fri, 01 Dec 2023 00:57:53 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e624731329026e7b41a3508796561bfdb534b5c8d5feb5c6e42f7628625afbec`  
		Last Modified: Fri, 01 Dec 2023 00:58:23 GMT  
		Size: 12.8 MB (12792838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87acd1be6016ae5308a23ac234b60a56c17ebdcc4fd9be0ac3c8db463e18ea7`  
		Last Modified: Fri, 01 Dec 2023 00:58:20 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c4112f8eab64e35b89bc8bfb9efabaa24c55b9af8cb2e6141553b1ebcb9e1a`  
		Last Modified: Fri, 01 Dec 2023 00:58:20 GMT  
		Size: 18.7 KB (18733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5a59dd4aa787793799cfc625c141dfc0f30824555b025f0aeeb1262d70770e`  
		Last Modified: Fri, 01 Dec 2023 00:58:20 GMT  
		Size: 8.9 KB (8876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a89ece867b3b119564432e0974e5091aa4bb855a2af6d98b42ced8dbd11331c7`  
		Last Modified: Fri, 01 Dec 2023 11:56:03 GMT  
		Size: 2.2 MB (2249541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f7eec2969c2ccca6c1a878136fb16afade0729e04bb29b087572a94ef080633`  
		Last Modified: Fri, 01 Dec 2023 11:56:03 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87f6e7787c0d2d4383aa8884bac3fe9d4352973260a5cdf4a2d94f26847ed83`  
		Last Modified: Fri, 01 Dec 2023 11:56:04 GMT  
		Size: 3.4 MB (3410296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.1-fpm-alpine3.18` - unknown; unknown

```console
$ docker pull drupal@sha256:e754c06e4acffd5e2a1d07d512b7ddb7f8c5c2abffe3fa230f610a515f9ec47e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.2 KB (254184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32800969c177bc8b3bbc89cf10637963383eeff7d1cce979fb4f490b2933bcee`

```dockerfile
```

-	Layers:
	-	`sha256:2cff75ce219206c95467839d5a813833714ea5ab49243f2da8749ae777374bd2`  
		Last Modified: Fri, 01 Dec 2023 11:56:01 GMT  
		Size: 230.6 KB (230641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3430cc92d29837549bd5368bc33bb122c158f4b4ccfef066598a546383e14715`  
		Last Modified: Fri, 01 Dec 2023 11:56:01 GMT  
		Size: 23.5 KB (23543 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.1-fpm-alpine3.18` - linux; s390x

```console
$ docker pull drupal@sha256:9cbcaa0b18f639e6ed79fae1c04d76f2578b29ed757cfa4c5f54abc093f332ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.9 MB (34866660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c40d9269bfb40ce8f3b12822641a7e689c76f343d778e9e916b1d6f918153eb7`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 14 Jun 2023 17:25:34 GMT
ADD file:50d6643abf7df167a927decd69d193b980557ff73cca48dce86d57e2ff25ad45 in / 
# Wed, 14 Jun 2023 17:25:34 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 14 Jun 2023 17:25:34 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 14 Jun 2023 17:25:34 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_VERSION=8.1.26
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.26.tar.xz.asc
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_SHA256=17f87133596449327451ad4b8d9911bfaea59ff5109f3a6f2bb679f967a8ea0f
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 14 Jun 2023 17:25:34 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 14 Jun 2023 17:25:34 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 14 Jun 2023 17:25:34 GMT
RUN docker-php-ext-enable sodium
# Wed, 14 Jun 2023 17:25:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 14 Jun 2023 17:25:34 GMT
WORKDIR /var/www/html
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 14 Jun 2023 17:25:34 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Jun 2023 17:25:34 GMT
EXPOSE 9000
# Wed, 14 Jun 2023 17:25:34 GMT
CMD ["php-fpm"]
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 14 Jun 2023 17:25:34 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 14 Jun 2023 17:25:34 GMT
ENV DRUPAL_VERSION=7.98
# Wed, 14 Jun 2023 17:25:34 GMT
ENV DRUPAL_MD5=4139f0feecb44a53645242194809b73a
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:2ea477e1c0c3db3337ee1d7c659f8c465021a65c036998ed3fa3b667d4b30153`  
		Last Modified: Thu, 30 Nov 2023 22:42:52 GMT  
		Size: 3.2 MB (3217454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa5313d02d4fcc59703ea6bd09df7b0df122fc73121b0954b541c214229202e`  
		Last Modified: Thu, 30 Nov 2023 23:47:29 GMT  
		Size: 2.8 MB (2789878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f082f983656d312447043a024c0fa5528e4055dbd73f4101ac38d1d2d3158ea`  
		Last Modified: Thu, 30 Nov 2023 23:47:28 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35feaf89a3d400114f4864637453e2e21cd9e7cb6a859699bd6272483f3a56ee`  
		Last Modified: Thu, 30 Nov 2023 23:47:28 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e991a7a2f1b73cfa48ea8640a15d8a2ee57997605a8a69dbab9de4c1e64998a`  
		Last Modified: Thu, 30 Nov 2023 23:50:33 GMT  
		Size: 11.8 MB (11830192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6de224836744daaf46f3bf87cd6ccdfb3a1ee63e227390613557aa1f16e138a`  
		Last Modified: Thu, 30 Nov 2023 23:50:33 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba5ca5bad84896e6318daccffe917ff6d48d699278554f62b269b36a2a00294`  
		Last Modified: Thu, 30 Nov 2023 23:50:52 GMT  
		Size: 11.6 MB (11595880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90088749be79e1ddde95d1f645f8083e16ce4847ffd12107b8e28e8cae659ae5`  
		Last Modified: Thu, 30 Nov 2023 23:50:49 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db25968b4d7061fbcd01317fb29b3b4710b03e0c1a08fe0d671a1ef8acd3e002`  
		Last Modified: Thu, 30 Nov 2023 23:50:49 GMT  
		Size: 18.8 KB (18765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3305b13de196bfb2b69ebd578f66ef1aef033110c9fd852a425353bb285d0a42`  
		Last Modified: Thu, 30 Nov 2023 23:50:49 GMT  
		Size: 8.9 KB (8875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dedf7ba8257c72aa3ff119229cc076c191785d06feb645b27172cf5253e8d5e2`  
		Last Modified: Fri, 01 Dec 2023 10:41:19 GMT  
		Size: 2.0 MB (1990543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e7bcd58890ef529a0a5fa53762c297a1a5ed3dfd8ea07392d4b3b2ef8f9572`  
		Last Modified: Fri, 01 Dec 2023 10:41:19 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533dcbbf711386d52a18cd127ab578decc2f3ad190518466e42eaef1c53b7b9e`  
		Last Modified: Fri, 01 Dec 2023 10:59:59 GMT  
		Size: 3.4 MB (3410292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.1-fpm-alpine3.18` - unknown; unknown

```console
$ docker pull drupal@sha256:f3246cc94922db352914d27a7df8f0c69792d379d2a882f7f2308d82dffcb06d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.5 KB (252484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fbc56dbfab8e52f40fba7a1a39afcb4855e3c1fe2e7890ec8de90a56c503f6d`

```dockerfile
```

-	Layers:
	-	`sha256:06b1e6390ae4429e2208fea19df69a8d1781184f1c28cf2d645bf92aeaf2cae9`  
		Last Modified: Fri, 01 Dec 2023 10:59:59 GMT  
		Size: 230.6 KB (230607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c37aa24bd7a1798c8df46f14f337d9805afacb20a6b06e9dc1eead400a9c4d07`  
		Last Modified: Fri, 01 Dec 2023 10:59:58 GMT  
		Size: 21.9 KB (21877 bytes)  
		MIME: application/vnd.in-toto+json
