## `drupal:7-php8.1-fpm-alpine3.20`

```console
$ docker pull drupal@sha256:367ea7a4d25167a1a509f1a1d4a07f6059274c1899319a71d5763e852b45f289
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

### `drupal:7-php8.1-fpm-alpine3.20` - linux; amd64

```console
$ docker pull drupal@sha256:60867bc4bc9eaa62c2466436a5ef6bec11c9add122d40d3b74c43e5d96e2e6a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 MB (36721568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2b57d94385b84ba5659eb7db9af13f69a421da453bb7e972cba7c187afc0d99`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 05 Jun 2024 22:17:43 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Wed, 05 Jun 2024 22:17:43 GMT
CMD ["/bin/sh"]
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 05 Jun 2024 22:17:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 05 Jun 2024 22:17:43 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_VERSION=8.1.29
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 05 Jun 2024 22:17:43 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 05 Jun 2024 22:17:43 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 05 Jun 2024 22:17:43 GMT
RUN docker-php-ext-enable sodium
# Wed, 05 Jun 2024 22:17:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 05 Jun 2024 22:17:43 GMT
WORKDIR /var/www/html
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 05 Jun 2024 22:17:43 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Jun 2024 22:17:43 GMT
EXPOSE 9000
# Wed, 05 Jun 2024 22:17:43 GMT
CMD ["php-fpm"]
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_VERSION=7.101
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.101.tar.gz
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_MD5=ddcd8cb4e885ae865a3d1a8b06707a67
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb15916673af8229814dcc44164d4616a6141bc5b586ae9362e741d64c6e4c91`  
		Last Modified: Sat, 07 Sep 2024 02:15:12 GMT  
		Size: 3.3 MB (3282678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9feb3258c4c6a46b7e182fa372bfe03ff37fd0fdf7f6894ca97b564fc382d7d4`  
		Last Modified: Sat, 07 Sep 2024 02:15:11 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e436918c34ed4c536bdbaeace5213a8aaeb796ec65951fe681a10758ae2677`  
		Last Modified: Sat, 07 Sep 2024 02:15:11 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b6c13c601d9d1574812e6412226c623a020da6c4444c2a3fda0dd707d818575`  
		Last Modified: Sat, 07 Sep 2024 02:20:33 GMT  
		Size: 11.8 MB (11847387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:590632704f8d4427fb629436d2d78f30bf6cc77e7c00be1ac41a1c7b32dcaf48`  
		Last Modified: Sat, 07 Sep 2024 02:20:32 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b902239f3464fe618f72d59c6457a50f10fa83223377ee2ef80efd17b70ef8`  
		Last Modified: Sat, 07 Sep 2024 02:20:56 GMT  
		Size: 12.6 MB (12612149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e084e12857251e1e38672018fef3ce85f9f5ccbaf6593636949166fb93d1bd`  
		Last Modified: Sat, 07 Sep 2024 02:20:54 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f511ff2e668a9eac1787fedfece0f42dc92f11d28fb524146c8f2e98e1edf0b5`  
		Last Modified: Sat, 07 Sep 2024 02:20:54 GMT  
		Size: 19.7 KB (19706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b09eb594cd151c863a7d6838fd5bf8bfd3540985ca4580b60b8abbd620de4b`  
		Last Modified: Sat, 07 Sep 2024 02:20:54 GMT  
		Size: 8.9 KB (8877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0d043f21cb237963f017398172f06f0f68f6ada839466e97bb8f0a08055844`  
		Last Modified: Sat, 07 Sep 2024 02:58:15 GMT  
		Size: 1.9 MB (1894910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3329ce9fab470dd0af74e0a5fc9bf06cfd83d417314427bcf455b23b50d0633`  
		Last Modified: Sat, 07 Sep 2024 02:58:14 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e993ec53e05178e0adeae68e3b9f1f8b9bb70c585e6d169a686695e37105849`  
		Last Modified: Sat, 07 Sep 2024 02:58:15 GMT  
		Size: 3.4 MB (3427632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.1-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:2c319f5545cdee4f864fa605360aaf0a489153bbb2034e9b1d190d1b903efb02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.8 KB (302778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3840cab3e8f7653bc53c5ada59c2057228f2e463a5163358465a105d61b3ed85`

```dockerfile
```

-	Layers:
	-	`sha256:348e17ad5eee4ff69488c104c23c9560be3eaf3d7942de3424d55061b4311375`  
		Last Modified: Sat, 07 Sep 2024 02:58:14 GMT  
		Size: 279.5 KB (279514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:912da7c185a9836bbb05e6ee6c7fa8b9b67fe50d8929e7839c69fa39e837b63e`  
		Last Modified: Sat, 07 Sep 2024 02:58:14 GMT  
		Size: 23.3 KB (23264 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.1-fpm-alpine3.20` - linux; arm variant v6

```console
$ docker pull drupal@sha256:299951c3ae1f9d8ea86ba4ddc091049b52d5b2fd699d2b1908155f0955b42542
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34751852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d21583cd88b02334a54ece8f6c511b5f62fee875277934b3debac01f4cc100b4`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 05 Jun 2024 22:17:43 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Wed, 05 Jun 2024 22:17:43 GMT
CMD ["/bin/sh"]
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 05 Jun 2024 22:17:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 05 Jun 2024 22:17:43 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_VERSION=8.1.29
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 05 Jun 2024 22:17:43 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 05 Jun 2024 22:17:43 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 05 Jun 2024 22:17:43 GMT
RUN docker-php-ext-enable sodium
# Wed, 05 Jun 2024 22:17:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 05 Jun 2024 22:17:43 GMT
WORKDIR /var/www/html
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 05 Jun 2024 22:17:43 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Jun 2024 22:17:43 GMT
EXPOSE 9000
# Wed, 05 Jun 2024 22:17:43 GMT
CMD ["php-fpm"]
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_VERSION=7.101
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.101.tar.gz
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_MD5=ddcd8cb4e885ae865a3d1a8b06707a67
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b78c7a9de9941e89cd785fc3ad14f52410d858d2259f5c9b2a852fd144612520`  
		Last Modified: Sat, 07 Sep 2024 00:48:55 GMT  
		Size: 3.3 MB (3269770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddbf8fddbe2a872480c609959838de42e95d1f5d5d3d8daadf7a1e44e5c381a2`  
		Last Modified: Sat, 07 Sep 2024 00:48:54 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb2d88511b2a3086248129999917d9f1e5928426fda8f08edf40ab5bafa37a9`  
		Last Modified: Sat, 07 Sep 2024 00:48:53 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:180289f3ea8445397c877cd6a868db47de64b24ed61201ee9fb04d3202d2bfcf`  
		Last Modified: Sat, 07 Sep 2024 00:54:28 GMT  
		Size: 11.8 MB (11847381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6168eb3fdb876b28f6120d49dd834976d6fa0eaeb65b3b0526818ccd763499e`  
		Last Modified: Sat, 07 Sep 2024 00:54:27 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc633ed0303bea248597eb4474467a7bac35a0bc9a16bb7556a888119c7748dd`  
		Last Modified: Sat, 07 Sep 2024 00:54:52 GMT  
		Size: 11.4 MB (11437247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cfb5222806126c2aa82eaebc4ef30b5460e6add278f108d8f8d93e253d1111f`  
		Last Modified: Sat, 07 Sep 2024 00:54:50 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75322423e5f1a1d693c6096bc0c6c5c978594f4a902da9fb780f26770cfc6a11`  
		Last Modified: Sat, 07 Sep 2024 00:54:50 GMT  
		Size: 19.5 KB (19490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a272d812cf5727677954d6a866327792aaf82c13043e71f4c0cbc8c6ab6842`  
		Last Modified: Sat, 07 Sep 2024 00:54:50 GMT  
		Size: 8.9 KB (8879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf411a0c55e33b4624ceed6bc95deca20964946ceb5457e22688d1c6a07c124`  
		Last Modified: Sat, 07 Sep 2024 13:00:41 GMT  
		Size: 1.4 MB (1370518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5231b0ff8607dde9c358fe53b87f536b133e43e8ff9ef0aa90b20bdcbd7487`  
		Last Modified: Sat, 07 Sep 2024 13:00:41 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a53ca653e2b0fee508061db1cb5ef6d0fd66322fc8813edb3a941e17c2d91da`  
		Last Modified: Sat, 07 Sep 2024 13:00:41 GMT  
		Size: 3.4 MB (3427639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.1-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:69a1d5fa7b2787c7833762470c352ee7b79e5fe81fdf6c003becef6425bf1bd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 KB (23173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb4de25345913dded19db975e12844b545ea01feadc38207a75c67b1e417f054`

```dockerfile
```

-	Layers:
	-	`sha256:b683a9b1a40f5819d829e45478ec7a8a0f4c8033741727491776537226bd3557`  
		Last Modified: Sat, 07 Sep 2024 13:00:39 GMT  
		Size: 23.2 KB (23173 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.1-fpm-alpine3.20` - linux; arm variant v7

```console
$ docker pull drupal@sha256:91b73b233a07e674cbe1ac85ff307af1bfcd88ee3e6e4ce5cdb900c2d0ea5e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.5 MB (33460528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7dd6991c81e866634600dee918a2670216b091dce6a592cf733c1ce415baf2e`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 05 Jun 2024 22:17:43 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Wed, 05 Jun 2024 22:17:43 GMT
CMD ["/bin/sh"]
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 05 Jun 2024 22:17:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 05 Jun 2024 22:17:43 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_VERSION=8.1.29
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 05 Jun 2024 22:17:43 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 05 Jun 2024 22:17:43 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 05 Jun 2024 22:17:43 GMT
RUN docker-php-ext-enable sodium
# Wed, 05 Jun 2024 22:17:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 05 Jun 2024 22:17:43 GMT
WORKDIR /var/www/html
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 05 Jun 2024 22:17:43 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Jun 2024 22:17:43 GMT
EXPOSE 9000
# Wed, 05 Jun 2024 22:17:43 GMT
CMD ["php-fpm"]
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_VERSION=7.101
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.101.tar.gz
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_MD5=ddcd8cb4e885ae865a3d1a8b06707a67
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57db3d4836535044109c42cf341df21ab1def6a06fecbaf98ffac833b47f15b`  
		Last Modified: Tue, 23 Jul 2024 01:14:20 GMT  
		Size: 3.1 MB (3073093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7991e70be4838afae3979e2bef4b2a7682dffac44793431e072ffbc9fc1686e5`  
		Last Modified: Tue, 23 Jul 2024 01:14:19 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3967a6fef2cedd5f47096963a74875b542f5e4f6667543712aa16505b281dcf7`  
		Last Modified: Tue, 23 Jul 2024 01:14:19 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83bc94e678062643a39f85032f7b45eeb628327b3edd2a8cc3e67bf6b9d81983`  
		Last Modified: Tue, 23 Jul 2024 01:23:06 GMT  
		Size: 11.8 MB (11847384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ad61fca5741fa46b3b017bec08e294b68f4cb0133e446df523de2023f4e9a0`  
		Last Modified: Tue, 23 Jul 2024 01:23:04 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a8dd653f6cafa340afbe207a7a62f90b0a32859edcde3b5e48966157a9b3dc5`  
		Last Modified: Tue, 23 Jul 2024 01:23:29 GMT  
		Size: 10.7 MB (10722762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e932250a661f75645f1924004184bcda0199b7c059834ec675f0cc48caa9055`  
		Last Modified: Tue, 23 Jul 2024 01:23:27 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ac85dd08391a243854814c0157b00cc667e8b280a0c846c487e31164940a29`  
		Last Modified: Tue, 23 Jul 2024 01:23:27 GMT  
		Size: 19.5 KB (19491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92455bebadbed6d1131bd422636d9991d97130ff44f535d13a0666322831c6ee`  
		Last Modified: Tue, 23 Jul 2024 01:23:27 GMT  
		Size: 8.9 KB (8879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad237570c7e37b9e88077d1a766d920a516376d39495bc65d822bdfccc3e2f8`  
		Last Modified: Tue, 23 Jul 2024 12:31:28 GMT  
		Size: 1.3 MB (1261898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13d73ff6e82b25610b31d551b33827e85ed504aaa782b30bd78624557c92488`  
		Last Modified: Tue, 23 Jul 2024 12:31:28 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f172a05e0b26122d221089fff0c6c34a616e973d8a1299cf0fe609ca045a178`  
		Last Modified: Tue, 23 Jul 2024 12:31:28 GMT  
		Size: 3.4 MB (3427635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.1-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:90f35932dce3906256aacd2f12e97fdd9673eeffad1af2000bcdd987aedd0aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.1 KB (300128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee54f64c50b24676ad95b6cdaf5da585953356a4d9bd7473e07484e6dd42eaa9`

```dockerfile
```

-	Layers:
	-	`sha256:365ab5917333081d359d6a9032bc5578e824c15cf6950b9bfdbe978ff3c38e58`  
		Last Modified: Tue, 23 Jul 2024 12:31:26 GMT  
		Size: 276.7 KB (276736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e3d6ef6250f338299919ee072f23c554accdc367030656f926fddf35d8fa715`  
		Last Modified: Tue, 23 Jul 2024 12:31:26 GMT  
		Size: 23.4 KB (23392 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.1-fpm-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:884a7585a1c0f98ca20af39a107f72c65bff1578fb076329e53ce5452749df30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37561581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9858d722a20bc5efbf565be9c6e24b89b238ea025f083e3c11f7ad65feb010b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 05 Jun 2024 22:17:43 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Wed, 05 Jun 2024 22:17:43 GMT
CMD ["/bin/sh"]
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 05 Jun 2024 22:17:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 05 Jun 2024 22:17:43 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_VERSION=8.1.29
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 05 Jun 2024 22:17:43 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 05 Jun 2024 22:17:43 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 05 Jun 2024 22:17:43 GMT
RUN docker-php-ext-enable sodium
# Wed, 05 Jun 2024 22:17:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 05 Jun 2024 22:17:43 GMT
WORKDIR /var/www/html
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 05 Jun 2024 22:17:43 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Jun 2024 22:17:43 GMT
EXPOSE 9000
# Wed, 05 Jun 2024 22:17:43 GMT
CMD ["php-fpm"]
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_VERSION=7.101
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.101.tar.gz
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_MD5=ddcd8cb4e885ae865a3d1a8b06707a67
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ef8ad75958cd7eb0e453d0f85e72134ef3976f8351b5742370df35bc60ed42`  
		Last Modified: Sat, 07 Sep 2024 02:23:50 GMT  
		Size: 3.3 MB (3333388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f80c1299f6c626e7df88761199f03734cced725870be7a04dd95bf11e80104`  
		Last Modified: Sat, 07 Sep 2024 02:23:49 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eb3615e2ca5466e128fbfbd9bfcaa4cc0a7c5935f1d980f13d765c6bfde9144`  
		Last Modified: Sat, 07 Sep 2024 02:23:49 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370bfce2070ad9aca19202e9f320c9ba8b845388870e485302a0842543c2ec16`  
		Last Modified: Sat, 07 Sep 2024 02:28:57 GMT  
		Size: 11.8 MB (11847382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bfb15cc07dd2db0cc8be4bccca8c31d1fa9aca7ecbeb48abdc95bd937ba23c6`  
		Last Modified: Sat, 07 Sep 2024 02:28:56 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f82dc4882e8e0ac256659664e0837e7ebcc48c6d42508a7140284416a5a917`  
		Last Modified: Sat, 07 Sep 2024 02:29:19 GMT  
		Size: 12.7 MB (12662409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c26b62be4fae7342953ef65dc280a97aa75af6282e34544f0b7aaaf9bb5817`  
		Last Modified: Sat, 07 Sep 2024 02:29:17 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1482eb9fdadbf5d5d78fb534cce73ee5686d1a34c573f0b565b0e55e86f1d7c1`  
		Last Modified: Sat, 07 Sep 2024 02:29:17 GMT  
		Size: 19.5 KB (19483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71db967a6ff1911fdd6190b02d12da6c5d711d12df2d1014af47a61a1a521a57`  
		Last Modified: Sat, 07 Sep 2024 02:29:17 GMT  
		Size: 8.9 KB (8880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5731294c4cf954f19bd50c3e5836fe6e83e0d3482afcb8516f6066ffc0e12b8`  
		Last Modified: Sat, 07 Sep 2024 12:33:59 GMT  
		Size: 2.2 MB (2170335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0464745cf00905e6a91cce34642b2e3677364793452a2337cf74d0ee0d45012`  
		Last Modified: Sat, 07 Sep 2024 12:33:59 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2089d941df7f747e613c1b81eced5bbb13340ddecfae8b0aeec9ab05108ed5`  
		Last Modified: Sat, 07 Sep 2024 12:34:00 GMT  
		Size: 3.4 MB (3427639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.1-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:b8c28ab17af2900119b8debfdd29f7adfca39341c48ba3af9f68e94af5f1304f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 KB (300377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ccd5d9fb14809dd484beb752702dc982baed45c98a70c0c62d4124446a692da`

```dockerfile
```

-	Layers:
	-	`sha256:30fd0796d770ddf380e4cf2659efac596803bd344745a139fe3f633e841f47ef`  
		Last Modified: Sat, 07 Sep 2024 12:33:57 GMT  
		Size: 276.8 KB (276754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bd93089d92769fa967366ef004a501fc84fb2289d18d47c4b42c68aaafc1221`  
		Last Modified: Sat, 07 Sep 2024 12:33:57 GMT  
		Size: 23.6 KB (23623 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.1-fpm-alpine3.20` - linux; 386

```console
$ docker pull drupal@sha256:93b1e0993b87ce57df875fdcd184d4ea161d798f17b11ffe44df36302abdc770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 MB (37002556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f986c1098cbb10db239956a0572dab010a3175eab06b0b3e83918d024b89235`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 05 Jun 2024 22:17:43 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Wed, 05 Jun 2024 22:17:43 GMT
CMD ["/bin/sh"]
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 05 Jun 2024 22:17:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 05 Jun 2024 22:17:43 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_VERSION=8.1.29
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 05 Jun 2024 22:17:43 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 05 Jun 2024 22:17:43 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 05 Jun 2024 22:17:43 GMT
RUN docker-php-ext-enable sodium
# Wed, 05 Jun 2024 22:17:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 05 Jun 2024 22:17:43 GMT
WORKDIR /var/www/html
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 05 Jun 2024 22:17:43 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Jun 2024 22:17:43 GMT
EXPOSE 9000
# Wed, 05 Jun 2024 22:17:43 GMT
CMD ["php-fpm"]
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_VERSION=7.101
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.101.tar.gz
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_MD5=ddcd8cb4e885ae865a3d1a8b06707a67
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17866811de1cdb9710f37a522dde62051d068230716118d22b6b987216e037ef`  
		Last Modified: Sat, 07 Sep 2024 01:49:46 GMT  
		Size: 3.3 MB (3331976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9513ca5d3e6e64e8e064f1b178ad39b5d375a65559181a7f4964c9471461ba8f`  
		Last Modified: Sat, 07 Sep 2024 01:49:45 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90338393c7a779c5576927d742c98b6841aa39aa84fe1b137708bd8f4d0ae68e`  
		Last Modified: Sat, 07 Sep 2024 01:49:45 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca65ba13f41089d517e755ef4050b9e90c90f5c89dae0bd0f4573f0f80b3b5c`  
		Last Modified: Sat, 07 Sep 2024 01:55:45 GMT  
		Size: 11.8 MB (11847377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50bf7e5db0defade2048461fc06fe851fdaab6897ebeaf2aeb65ed078915ca01`  
		Last Modified: Sat, 07 Sep 2024 01:55:43 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320f427dfd1a604a58b9547d5731febd09b51f74a556a6ed4e040a98f2957c92`  
		Last Modified: Sat, 07 Sep 2024 01:56:10 GMT  
		Size: 12.9 MB (12939585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9212067c5ecb03d60e07d82fdf5ac550c01a1af3ac9feb2b8de0e23b49657f7f`  
		Last Modified: Sat, 07 Sep 2024 01:56:07 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26234b3a58bcfc1c05996e69d4d5a1014e4a9847e93ecb892653e90d59d064f1`  
		Last Modified: Sat, 07 Sep 2024 01:56:07 GMT  
		Size: 19.7 KB (19697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b54d71ca0ea6bea4f68304422cb5748e63d2fe96d62c13e628329811e7ba0c3`  
		Last Modified: Sat, 07 Sep 2024 01:56:07 GMT  
		Size: 8.9 KB (8882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08875a72af9862f5906f4af4f0028eb36d5be38b12edd3becd021e8cad9344b8`  
		Last Modified: Sat, 07 Sep 2024 02:58:07 GMT  
		Size: 2.0 MB (1953821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a34a88a55b6935eec5377bf589f64706918ab14008a80dbc7bf487b3f5e514a`  
		Last Modified: Sat, 07 Sep 2024 02:58:07 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b60a0e06ad99244b4adea97af3390158ced548d9c574564fe9f81ad19d486b`  
		Last Modified: Sat, 07 Sep 2024 02:58:07 GMT  
		Size: 3.4 MB (3427634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.1-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:d4135d9748f807b37e3c0512ec520da9055fcc0ce494e1c285ebfd2b2a75ed85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.7 KB (302680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0752342bdf821bc712d7c28a4dd0d1cdcf47d3f9b63bb3d817f3b5e833bea69`

```dockerfile
```

-	Layers:
	-	`sha256:f5e510f686fe12eec49fb939dceeed17d09d24857fd92be8c61a9fd65f8f2cb5`  
		Last Modified: Sat, 07 Sep 2024 02:58:06 GMT  
		Size: 279.5 KB (279469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5a43917dd4f1a79647851136c2aaac30e2d8a846f906663428fc5b4a552a506`  
		Last Modified: Sat, 07 Sep 2024 02:58:06 GMT  
		Size: 23.2 KB (23211 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.1-fpm-alpine3.20` - linux; ppc64le

```console
$ docker pull drupal@sha256:a538ee598094b47014c75da7c6c4e4c9b7d68dc72267d0093075365025fe232d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 MB (37014783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f99a8da3f77c30aab38b8c0ce64198f0e3f5cfa93ce563251ed651864bfde91`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 05 Jun 2024 22:17:43 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Wed, 05 Jun 2024 22:17:43 GMT
CMD ["/bin/sh"]
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 05 Jun 2024 22:17:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 05 Jun 2024 22:17:43 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_VERSION=8.1.29
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 05 Jun 2024 22:17:43 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 05 Jun 2024 22:17:43 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 05 Jun 2024 22:17:43 GMT
RUN docker-php-ext-enable sodium
# Wed, 05 Jun 2024 22:17:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 05 Jun 2024 22:17:43 GMT
WORKDIR /var/www/html
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 05 Jun 2024 22:17:43 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Jun 2024 22:17:43 GMT
EXPOSE 9000
# Wed, 05 Jun 2024 22:17:43 GMT
CMD ["php-fpm"]
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_VERSION=7.101
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.101.tar.gz
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_MD5=ddcd8cb4e885ae865a3d1a8b06707a67
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ac727a268c34206d27f9588c3acfc276afdaf0623dfdc19b7d210a7a881ee4`  
		Last Modified: Sat, 07 Sep 2024 01:44:58 GMT  
		Size: 3.4 MB (3408322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b564dcd8f1c226aa29a92bf07685b2a44ccb8ac47267a590bc34a56d25bbbcc4`  
		Last Modified: Sat, 07 Sep 2024 01:44:57 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e3867a87b0703f924c2a7915ce891a49d11c61af6d01613564e485431a9f78`  
		Last Modified: Sat, 07 Sep 2024 01:44:57 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba544878c2622f1d0d768a423c16ad0b5437143c47e143af69f806e84c670a7e`  
		Last Modified: Sat, 07 Sep 2024 01:58:03 GMT  
		Size: 11.8 MB (11847387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b3ab7f471a86acfb2c82a8bffcf8eb5bb111bef09de3fc8eaf0700723f64561`  
		Last Modified: Sat, 07 Sep 2024 01:58:02 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d83b6fda0e924c0aac6b835b1436416153f4a10eadab87ba166f431b8ff29a`  
		Last Modified: Sat, 07 Sep 2024 01:58:26 GMT  
		Size: 13.1 MB (13056134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909cc0f828f4f2c5cd0574599ae24da23d44638c0b0dcdac763d075ae93c5950`  
		Last Modified: Sat, 07 Sep 2024 01:58:24 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79773842285c7ebd51f2fe16c47a17c5a25ac1f76790500101ce1856fbfd33f4`  
		Last Modified: Sat, 07 Sep 2024 01:58:24 GMT  
		Size: 19.5 KB (19486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677580baede78ea803095e691816a93207b9ebb080b0fa43589907f70c91399f`  
		Last Modified: Sat, 07 Sep 2024 01:58:24 GMT  
		Size: 8.9 KB (8877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd46cdd10ff3e6e19f4f2eaaa1062cb64d3eba9804ed0d44d47ba5379cdae7ae`  
		Last Modified: Sat, 07 Sep 2024 12:28:03 GMT  
		Size: 1.7 MB (1670102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e1a769a242b287e3cccbf1a1ee74448dbe1d5bb764de69e3588288cb1fcf87`  
		Last Modified: Sat, 07 Sep 2024 12:28:03 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a1aea36a07fffd331a5de809409617b7110632c7f20336bc8f104ac130af35e`  
		Last Modified: Sat, 07 Sep 2024 12:28:04 GMT  
		Size: 3.4 MB (3427633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.1-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:98a75810b167ed7690ab8ab1b24faec0ed2706c1b5f2d2a1c4b7ddff5e4c719e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.1 KB (298084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4965180ba37aecf2373afc409d0984881a49be951f241125a93bea794c632b9b`

```dockerfile
```

-	Layers:
	-	`sha256:a3277cb619ac7671fa8879c2c50d49e69586333debb70352f950ffb91c487cc8`  
		Last Modified: Sat, 07 Sep 2024 12:28:02 GMT  
		Size: 274.8 KB (274754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a2f06b963b33dd233367c5115548c2d936d725b820d7cdc68ae60b2e3e5455b`  
		Last Modified: Sat, 07 Sep 2024 12:28:01 GMT  
		Size: 23.3 KB (23330 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.1-fpm-alpine3.20` - linux; riscv64

```console
$ docker pull drupal@sha256:cdbac785cc116228b01d32a052037ceb04be2e39dff4e2c8e5463db0aa72ff34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.5 MB (35482023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d3096ea98ac793c3ba96845074bf68b3cd4e9a4d0abf2d17ca3263511213f3c`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 05 Jun 2024 22:17:43 GMT
ADD file:cdf7088bbd70519f0f5d7b4249df34386e40f0194752f45842b3d85f2d331cf5 in / 
# Wed, 05 Jun 2024 22:17:43 GMT
CMD ["/bin/sh"]
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 05 Jun 2024 22:17:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 05 Jun 2024 22:17:43 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_VERSION=8.1.29
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 05 Jun 2024 22:17:43 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 05 Jun 2024 22:17:43 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 05 Jun 2024 22:17:43 GMT
RUN docker-php-ext-enable sodium
# Wed, 05 Jun 2024 22:17:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 05 Jun 2024 22:17:43 GMT
WORKDIR /var/www/html
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 05 Jun 2024 22:17:43 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Jun 2024 22:17:43 GMT
EXPOSE 9000
# Wed, 05 Jun 2024 22:17:43 GMT
CMD ["php-fpm"]
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_VERSION=7.101
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.101.tar.gz
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_MD5=ddcd8cb4e885ae865a3d1a8b06707a67
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:faf447acae27573624c0613a79c4bcf1f9bc46d29f523140352abfd3f7691282`  
		Last Modified: Mon, 22 Jul 2024 22:21:18 GMT  
		Size: 3.4 MB (3370673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2d0e03d7a4d4766a64c04a50abfb02e217be153dd68888273b46568c4cac04`  
		Last Modified: Tue, 23 Jul 2024 12:29:02 GMT  
		Size: 3.4 MB (3397181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56268c2d820d6bf5bbf0e86c5bc55e50edc209a552c0844c6a9f787a880a2c6`  
		Last Modified: Tue, 23 Jul 2024 12:28:58 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05d3b9188b0e4a61167b2493ce280347bad9dfe72e9ecf4c18c5572f2cb6719`  
		Last Modified: Tue, 23 Jul 2024 12:28:58 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:690f906ce1775ad8a14e790070e46a2f7e24fb9e37d65d70e7b42d6117ea584c`  
		Last Modified: Tue, 23 Jul 2024 12:38:23 GMT  
		Size: 11.8 MB (11847380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e1e4c5d214e16641cb479484e95056d429d7ddd8efa054a0ae7d1c3b93b69f`  
		Last Modified: Tue, 23 Jul 2024 12:38:17 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01056fd49a93ae49f6db14eeaefeb08aace29594c579190a77bda7073f8cea3b`  
		Last Modified: Tue, 23 Jul 2024 12:39:09 GMT  
		Size: 11.9 MB (11934219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eec4ade38c5cf79d265303444e0736de397cc97435cb5513d1911cc04c0efdc`  
		Last Modified: Tue, 23 Jul 2024 12:38:58 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b7abbdf46e7e503341a30c728608c755a85c2a62fa99c55e0ac76d56daeb56`  
		Last Modified: Tue, 23 Jul 2024 12:38:58 GMT  
		Size: 19.5 KB (19487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d47df8a61aba967e986102873dee66240dc15407959bfe83ad7ebacbfb5259c`  
		Last Modified: Tue, 23 Jul 2024 12:38:58 GMT  
		Size: 8.9 KB (8880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40353ab14c5bab5c3ebf7299451d3eb2a1544a589b8c815a30a615b15b0d4cd8`  
		Last Modified: Wed, 24 Jul 2024 12:37:42 GMT  
		Size: 1.5 MB (1472135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38322024313f182fe834d290cf511e9ae65595e1854964ffbba3e8ec8837fe8`  
		Last Modified: Wed, 24 Jul 2024 12:37:42 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f3994ad36a53af5effc00b6bf1e2b8e1f26027a67e7da798a4560251e207f6`  
		Last Modified: Wed, 24 Jul 2024 12:37:43 GMT  
		Size: 3.4 MB (3427641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.1-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:af1b8e712a3a24a80499816d21aaa06e6c4d63862acc1bb82b35ab18d7049f9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.1 KB (298098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:716f8be4555e657ba8e765a324f9ce66f02dec4b55b7c4f171b5c912febd8390`

```dockerfile
```

-	Layers:
	-	`sha256:c3088b370c898c8cfe7d670074b67d4f46d1c6fc4a7f6f25e3e504916806737e`  
		Last Modified: Wed, 24 Jul 2024 12:37:40 GMT  
		Size: 274.8 KB (274768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61d726eb3f83a7ca5ba3e13cb0e55b1008d63d7d36603938b7a5beb5aa642868`  
		Last Modified: Wed, 24 Jul 2024 12:37:40 GMT  
		Size: 23.3 KB (23330 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.1-fpm-alpine3.20` - linux; s390x

```console
$ docker pull drupal@sha256:c5d0713647af131e5dde9a76cd632ae689ddd91477bcbd700752e8b8f95c5b00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36375285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9119ca1e25278160922ff23dbd718b8f364fe75f6e3dae11b45455fe7c724e9b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 05 Jun 2024 22:17:43 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Wed, 05 Jun 2024 22:17:43 GMT
CMD ["/bin/sh"]
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 05 Jun 2024 22:17:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 05 Jun 2024 22:17:43 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_VERSION=8.1.29
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 05 Jun 2024 22:17:43 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 05 Jun 2024 22:17:43 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 05 Jun 2024 22:17:43 GMT
RUN docker-php-ext-enable sodium
# Wed, 05 Jun 2024 22:17:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 05 Jun 2024 22:17:43 GMT
WORKDIR /var/www/html
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 05 Jun 2024 22:17:43 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Jun 2024 22:17:43 GMT
EXPOSE 9000
# Wed, 05 Jun 2024 22:17:43 GMT
CMD ["php-fpm"]
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_VERSION=7.101
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.101.tar.gz
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_MD5=ddcd8cb4e885ae865a3d1a8b06707a67
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9208ede8519d248128a660ad6cbef1b3a33b141374be176c946b5b17b2968ab4`  
		Last Modified: Sat, 07 Sep 2024 00:42:38 GMT  
		Size: 3.5 MB (3473993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabbdadb2babb53e22b8c60bffa37b66bacdd1495093eec38748ca15dabc8287`  
		Last Modified: Sat, 07 Sep 2024 00:42:37 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2431f4d7c348124f66281fa6433fdcded6e6a093aedb9cdd6fa9c7d87a1407`  
		Last Modified: Sat, 07 Sep 2024 00:42:37 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0116765f5ce64a8bd0001f907c8e2b29579c2de201b41d6f30bd3e6e7c356b4`  
		Last Modified: Sat, 07 Sep 2024 00:46:26 GMT  
		Size: 11.8 MB (11847379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10734fe6dd93196ccdbae6c99e719100bc7f0c24c64cadf917a99f38aece7f25`  
		Last Modified: Sat, 07 Sep 2024 00:46:26 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c807b8e30b1a2aa589c4ee1cfb03b782d97ed291aa7e645f1cc8f9eae0b84983`  
		Last Modified: Sat, 07 Sep 2024 00:46:42 GMT  
		Size: 12.5 MB (12547441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab9481931a9ea444dff10cc671b9170c4034efbc53c7fdeeeaa1e292e90202c8`  
		Last Modified: Sat, 07 Sep 2024 00:46:39 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3059ecb1a3d1b35c929fdf893a5fabbf5e1533064ca4d1f987819ca393b221`  
		Last Modified: Sat, 07 Sep 2024 00:46:39 GMT  
		Size: 19.5 KB (19488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56951aca4ed2617654fab0812379161933464117b5a396723058ef74c69acdd`  
		Last Modified: Sat, 07 Sep 2024 00:46:39 GMT  
		Size: 8.9 KB (8875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c75eb558e474e16bc5482410314c7e3fcc5e734ccf7ae262db64611408c97c0`  
		Last Modified: Sat, 07 Sep 2024 11:07:47 GMT  
		Size: 1.6 MB (1584455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5d9d494366342e84676658003f52286afd0ccb889be876e3419ead3729754f`  
		Last Modified: Sat, 07 Sep 2024 11:07:47 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a69eb9f79c7ee69fb83df2d5b7a857267f63a68796cdbf404bab6a1f00d65d`  
		Last Modified: Sat, 07 Sep 2024 11:07:48 GMT  
		Size: 3.4 MB (3427638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.1-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:cf72909f225debdcfbf2c876329d163849750857fb83c87634b0f850bfac8ddc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.0 KB (297960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f09e9fc902822236d13bd1ef5ca5f8ee621730ff51f82bf218e93b6d5966a3fc`

```dockerfile
```

-	Layers:
	-	`sha256:8b1952b4bbe61a1e0a9c585e00b714adde5b2a9d23e76ebef23e470d0f67d38a`  
		Last Modified: Sat, 07 Sep 2024 11:07:46 GMT  
		Size: 274.7 KB (274696 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb7d0663085a0fb8accfe6dd0e9beec1dc6c8f9b9a4775a0a2405e4b83ab496f`  
		Last Modified: Sat, 07 Sep 2024 11:07:46 GMT  
		Size: 23.3 KB (23264 bytes)  
		MIME: application/vnd.in-toto+json
