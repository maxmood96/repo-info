## `drupal:fpm-alpine`

```console
$ docker pull drupal@sha256:a967531e11944864c5f60e37c15436d393ddbbd7176832f28ec23c4522460c9d
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

### `drupal:fpm-alpine` - linux; amd64

```console
$ docker pull drupal@sha256:0bafc031fbad01d3b88506d9ca2e2cf5e8a8030221d6903bf0bc372977d798ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56732871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deeee1f6e08bd06a61862a5c0415410e7c30f5b6b3e8a5d2f20ec7282291234b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 03 Oct 2024 09:27:25 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 03 Oct 2024 09:27:25 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHP_VERSION=8.3.13
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 03 Oct 2024 09:27:25 GMT
WORKDIR /var/www/html
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
STOPSIGNAL SIGQUIT
# Thu, 03 Oct 2024 09:27:25 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 03 Oct 2024 09:27:25 GMT
CMD ["php-fpm"]
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
ENV DRUPAL_VERSION=11.0.5
# Thu, 03 Oct 2024 09:27:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 03 Oct 2024 09:27:25 GMT
WORKDIR /opt/drupal
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:974d6dc539b97171c225398207a086e6255618c2e6224626a53d677f8c1d86f4`  
		Last Modified: Mon, 28 Oct 2024 22:12:21 GMT  
		Size: 5.6 MB (5581755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4919596a5ac2b751eb748eea5bf956b187a320d695acf150688e39e0243dab3d`  
		Last Modified: Mon, 28 Oct 2024 22:12:21 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3e4aacc92d63badd05283255c5c738f39b5816d21c0be85477445b63e2cc7b`  
		Last Modified: Mon, 28 Oct 2024 22:12:20 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b281f39e9998881c524e2a60bfce640d0954562cd58bab3aa143866178b055`  
		Last Modified: Mon, 28 Oct 2024 22:12:21 GMT  
		Size: 12.5 MB (12504598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa521d28c238b882be42e7a8661ffeb992fa2dd31c8979ae793ad09c6ce5b09`  
		Last Modified: Mon, 28 Oct 2024 22:12:21 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb11d4a736daf3576e4f10806679d8b97222376548a0bc789755eaedc2c2c5a`  
		Last Modified: Mon, 28 Oct 2024 22:12:22 GMT  
		Size: 13.1 MB (13101988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed160c3394627cbe0154d202029ee2d0cbb4f9f04639f2260c0254b36ecd61e`  
		Last Modified: Mon, 28 Oct 2024 22:12:22 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89617376b50668ec39a950347d68785192a230097a77237f785ed4bef8556d19`  
		Last Modified: Mon, 28 Oct 2024 22:12:22 GMT  
		Size: 19.7 KB (19658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72edb4e6fec4f966334ad2c4e895fbda55a4539bf4efe38e140601dd432d9dfe`  
		Last Modified: Mon, 28 Oct 2024 22:12:22 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3f389292126677a2d5b5a98629893b42ed21dcfdb7d0e98329a4eb509a7e28`  
		Last Modified: Mon, 28 Oct 2024 23:23:58 GMT  
		Size: 1.9 MB (1901798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d8dbe60e5f9331c6e0e5fd00459171548e7539efa3a4fc1c4831aa396ca9ddc`  
		Last Modified: Mon, 28 Oct 2024 23:23:58 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0239fbe9e60686c5ee2a1a08562439d14f5bd35815c1a948306ca345e5b2dba4`  
		Last Modified: Mon, 28 Oct 2024 23:23:58 GMT  
		Size: 738.7 KB (738713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f834889ef7c92080117036fa73e460feb176b9735a06566be77123c33d1b9a`  
		Last Modified: Mon, 28 Oct 2024 23:23:58 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73bf06e5a1581851e0fc46721ecbc0b11e652bfa5d7b322589f5e9b08d0e9ee3`  
		Last Modified: Mon, 28 Oct 2024 23:23:59 GMT  
		Size: 19.2 MB (19246827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-alpine` - unknown; unknown

```console
$ docker pull drupal@sha256:d325bf688263d8e12b7ade8577c9199db6abb710ad356eb628b52869e7fa1990
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.6 KB (389633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5db304f09324c1133a7445265571e9859b1720e63d9963b57e87f7e28cba14d9`

```dockerfile
```

-	Layers:
	-	`sha256:1ba97f3643080822cbe1865f56ee763564288a683d0714fbb80147b8ec725ba9`  
		Last Modified: Mon, 28 Oct 2024 23:23:58 GMT  
		Size: 353.4 KB (353394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:941a019bbea3968742b3b50a90ae11319fc217b16a7f770b65daaf4176e54ac2`  
		Last Modified: Mon, 28 Oct 2024 23:23:58 GMT  
		Size: 36.2 KB (36239 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm-alpine` - linux; arm variant v6

```console
$ docker pull drupal@sha256:f3f86f88fcab65600c0a087c0605978f052cc2dddfad689237789ada08aa270e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 MB (55457641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bad7052a09002963778a687f65bbec0a6476d635ebe8495bccfd800a8ae9b619`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 23:30:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 06 Sep 2024 23:30:23 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 06 Sep 2024 23:30:24 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 06 Sep 2024 23:30:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 06 Sep 2024 23:30:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 06 Sep 2024 23:30:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 23:30:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 23:30:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 06 Sep 2024 23:51:09 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHP_VERSION=8.3.13
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 03 Oct 2024 09:27:25 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 03 Oct 2024 09:27:25 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 03 Oct 2024 09:27:25 GMT
RUN docker-php-ext-enable sodium
# Thu, 03 Oct 2024 09:27:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 03 Oct 2024 09:27:25 GMT
WORKDIR /var/www/html
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 03 Oct 2024 09:27:25 GMT
STOPSIGNAL SIGQUIT
# Thu, 03 Oct 2024 09:27:25 GMT
EXPOSE 9000
# Thu, 03 Oct 2024 09:27:25 GMT
CMD ["php-fpm"]
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
ENV DRUPAL_VERSION=11.0.5
# Thu, 03 Oct 2024 09:27:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 03 Oct 2024 09:27:25 GMT
WORKDIR /opt/drupal
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
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
	-	`sha256:2913caf4eeb0b47e0a269d5500be80ad644b55b830987923b9b25d7c47b779b6`  
		Last Modified: Fri, 25 Oct 2024 01:12:37 GMT  
		Size: 12.5 MB (12504684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd40e2319cfc199b8ddae2c1022299e653810d5c8fcff021ecf9e71bc732119`  
		Last Modified: Fri, 25 Oct 2024 01:12:36 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a22bd48d8cd970d4d3abf524222b5af1cc44f622ea91cb6c04457b6fccaf6ab`  
		Last Modified: Fri, 25 Oct 2024 01:13:20 GMT  
		Size: 14.9 MB (14911759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2820c6b94ddaf1cfe93b1233a605eed5247758d2c2480b675cf4d245c7c924`  
		Last Modified: Fri, 25 Oct 2024 01:13:16 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91f5ddf0231e9286b2035969b2e8d7ce898d929a8b6ea78c5bced453eeeadcb`  
		Last Modified: Fri, 25 Oct 2024 01:13:16 GMT  
		Size: 19.5 KB (19509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c698ffba2fada2b58d2c3104bc9da45a5204ed1c5683458ba97e51a1e5101c2`  
		Last Modified: Fri, 25 Oct 2024 01:13:16 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f8990f236cacebce54802c2539db0b08ef34837b7231ddb8349d4d4a9ff68e`  
		Last Modified: Fri, 25 Oct 2024 02:49:26 GMT  
		Size: 1.4 MB (1385695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b2c75871492b5acc8ec9de25af2a127ee13eae8d60d7cfe6fe1ecfed465be4`  
		Last Modified: Fri, 25 Oct 2024 02:49:26 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56651eae4190dde84ed73945bc1875a6041ea9fa15e95aab4c87f068f594910a`  
		Last Modified: Fri, 25 Oct 2024 02:49:26 GMT  
		Size: 738.7 KB (738720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0640587ba83af93b6eb3f0e1fdef8e4a1b1999981d706b6c553e8802c88282c9`  
		Last Modified: Fri, 25 Oct 2024 02:49:26 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ce08dcb8ecb3a073be012355d18b97517eaf22a2267c69a6827f4ca3c9cac7`  
		Last Modified: Fri, 25 Oct 2024 02:49:28 GMT  
		Size: 19.2 MB (19247282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-alpine` - unknown; unknown

```console
$ docker pull drupal@sha256:ab07ea47c4632d1a74a7bc41219dbfaf1616811bb768875c66629970ef697049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.5 KB (35544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ba4c840d6f029be8850856f87f7527f172ec0fcee40437d6eaaa29a655b9a7`

```dockerfile
```

-	Layers:
	-	`sha256:7d2907b5a6d4800b3bce7d90ed5c5d4d4838a0d8bb3eea1065196cdb26fd4bc3`  
		Last Modified: Fri, 25 Oct 2024 02:49:25 GMT  
		Size: 35.5 KB (35544 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm-alpine` - linux; arm variant v7

```console
$ docker pull drupal@sha256:4825643ea15f90c3ac2cda4e8e1c236a02b1ba08dee414a82defb54d31d41b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53922085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0973820060196e2268d927b359acdaaed9fc460864dac181adabb70ce4b04f07`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 22:29:07 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 06 Sep 2024 22:29:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 06 Sep 2024 22:29:10 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 06 Sep 2024 22:29:10 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 06 Sep 2024 22:29:10 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 06 Sep 2024 22:29:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 22:29:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 22:29:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 06 Sep 2024 22:47:09 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHP_VERSION=8.3.13
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 03 Oct 2024 09:27:25 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 03 Oct 2024 09:27:25 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 03 Oct 2024 09:27:25 GMT
RUN docker-php-ext-enable sodium
# Thu, 03 Oct 2024 09:27:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 03 Oct 2024 09:27:25 GMT
WORKDIR /var/www/html
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 03 Oct 2024 09:27:25 GMT
STOPSIGNAL SIGQUIT
# Thu, 03 Oct 2024 09:27:25 GMT
EXPOSE 9000
# Thu, 03 Oct 2024 09:27:25 GMT
CMD ["php-fpm"]
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
ENV DRUPAL_VERSION=11.0.5
# Thu, 03 Oct 2024 09:27:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 03 Oct 2024 09:27:25 GMT
WORKDIR /opt/drupal
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f12c01d5f758f7fce28807153dec7a85ae2e307cf0d73f644d575cd875cb994a`  
		Last Modified: Fri, 06 Sep 2024 23:45:25 GMT  
		Size: 3.1 MB (3079568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c3e48f803b4ca0c1ec0b16f85f80f0a17b054845918112eb73b80eb9bd7297`  
		Last Modified: Fri, 06 Sep 2024 23:45:23 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7c21bdd57d9b7548f08c79a56f0a75d4e14a705967ae55d0450a10f0c6c43e`  
		Last Modified: Fri, 06 Sep 2024 23:45:21 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93efe62db4f1f9f85f795e6cc1e7f8d835b0a8657d2a60143ba15d82d5863841`  
		Last Modified: Fri, 25 Oct 2024 02:37:26 GMT  
		Size: 12.5 MB (12504680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1204359c9c9eb5cb76578981a5c068e3fac227ce0e7df1a86096569dc1230c85`  
		Last Modified: Fri, 25 Oct 2024 02:37:25 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8988b5bf0a07fc37e38cc4d562bb42efb707d2b8386eb6eef3d7000622e4d43`  
		Last Modified: Fri, 25 Oct 2024 02:38:07 GMT  
		Size: 13.9 MB (13947713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b049572e0d13219dcd42d20089bd59d6860af37f2c9c0fe7c8a1e79774aa3375`  
		Last Modified: Fri, 25 Oct 2024 02:38:04 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de8112cd845766274a465b7aba29e08f38d21fa62445a41530e0794502690bc`  
		Last Modified: Fri, 25 Oct 2024 02:38:04 GMT  
		Size: 19.5 KB (19521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6bb294d616611f994756d0922816947e2fe904b62ed2fd97f4dfe87c61118ea`  
		Last Modified: Fri, 25 Oct 2024 02:38:04 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d362ebc82db7c50ac7c7d9ba7a0e4a0797b9b84f921f08473dede4f7368d95b`  
		Last Modified: Fri, 25 Oct 2024 05:02:03 GMT  
		Size: 1.3 MB (1275753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757b7f8700d97c8ee7a7dcd00644c7efdfca57e283fc7f258aac4d2297935a91`  
		Last Modified: Fri, 25 Oct 2024 05:02:03 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e136755d94353c69d7c72163c1204bfec00275ec0be0a8cb09094565be9c9ee6`  
		Last Modified: Fri, 25 Oct 2024 05:02:04 GMT  
		Size: 738.7 KB (738707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4496ea9e2417d36da9f4e8887d161b82bbc842798b132c8e5afe8e75acf4399`  
		Last Modified: Fri, 25 Oct 2024 05:02:04 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e9462a7de68c04e88cf4613f03e760bc9762b6fecff2caa59c0e90e5023f4c`  
		Last Modified: Fri, 25 Oct 2024 05:02:05 GMT  
		Size: 19.2 MB (19246926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-alpine` - unknown; unknown

```console
$ docker pull drupal@sha256:d19b098a0e62e54d2447c2215b12ec40fe1ff9c3d9d262e3126e7509ba2e102e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.4 KB (386421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b83594e2efd7320a90081abad3952cc3008ffab5bb2cb127899ffebb82aecb`

```dockerfile
```

-	Layers:
	-	`sha256:0e643150646397333bdf721093039ec173ed4b53e4bd85baac78d76dd31f5aee`  
		Last Modified: Fri, 25 Oct 2024 05:02:02 GMT  
		Size: 350.7 KB (350662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19f626cc1c1f132a09a8be313551535c3d6fb540fd8d68344f617f1fa065df32`  
		Last Modified: Fri, 25 Oct 2024 05:02:02 GMT  
		Size: 35.8 KB (35759 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:a17e34c02d184f5d61fbbab31443f713f8145f2b4365133b615c916deae2cfec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (59024956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32ee8e2d547350c2924516118eda6168abae9ece8df08defc3105ac98c4aff90`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 00:43:30 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 07 Sep 2024 00:43:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Sat, 07 Sep 2024 00:43:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 07 Sep 2024 00:43:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 07 Sep 2024 00:43:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 07 Sep 2024 00:43:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Sep 2024 00:43:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Sep 2024 00:43:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 07 Sep 2024 01:04:32 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHP_VERSION=8.3.13
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 03 Oct 2024 09:27:25 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 03 Oct 2024 09:27:25 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 03 Oct 2024 09:27:25 GMT
RUN docker-php-ext-enable sodium
# Thu, 03 Oct 2024 09:27:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 03 Oct 2024 09:27:25 GMT
WORKDIR /var/www/html
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 03 Oct 2024 09:27:25 GMT
STOPSIGNAL SIGQUIT
# Thu, 03 Oct 2024 09:27:25 GMT
EXPOSE 9000
# Thu, 03 Oct 2024 09:27:25 GMT
CMD ["php-fpm"]
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
ENV DRUPAL_VERSION=11.0.5
# Thu, 03 Oct 2024 09:27:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 03 Oct 2024 09:27:25 GMT
WORKDIR /opt/drupal
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
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
	-	`sha256:5b324dba8535eea2357b994da9864afef849388a4c8e80235090810383253f31`  
		Last Modified: Fri, 25 Oct 2024 02:19:36 GMT  
		Size: 12.5 MB (12504686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e479347c3f32eee03df523edd0f1a869f7a7636702922f9d5db1ac9024ea211`  
		Last Modified: Fri, 25 Oct 2024 02:19:35 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23b04a5644c6d20e08059cccd97d6934147bebb18605c1dde72dd77c2a76455`  
		Last Modified: Fri, 25 Oct 2024 02:20:15 GMT  
		Size: 16.9 MB (16902093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7df40e793bac6573c663125ccfbeba7981561c44124f6fb6587c5a7b8254174`  
		Last Modified: Fri, 25 Oct 2024 02:20:12 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0990d1cc9efa7a886064d609af6f66ec31e70549b0a76e6e69d5a9901efc35ba`  
		Last Modified: Fri, 25 Oct 2024 02:20:12 GMT  
		Size: 19.5 KB (19500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:997895c9b9ff476cc722581727f34c89230d1e2154be9e19517a382813e484af`  
		Last Modified: Fri, 25 Oct 2024 02:20:13 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c576aeac28c5d3d066cb184aaff8ce1ab2472e7a773b2445b847f5bbb565ec0`  
		Last Modified: Fri, 25 Oct 2024 05:09:04 GMT  
		Size: 2.2 MB (2178144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c217914f60f2e82c25487c2bb5b650c2ce6f3ff24e1f074839520f48f81af828`  
		Last Modified: Fri, 25 Oct 2024 05:09:04 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb7ab062fcd856a699880ab181922e2592ec146eb9b2e07dc67511e3f76d88f`  
		Last Modified: Fri, 25 Oct 2024 05:09:04 GMT  
		Size: 738.7 KB (738717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b453c91a6088a26c897efe0d6597eeca43be82a2bec6b1967557894733865e02`  
		Last Modified: Fri, 25 Oct 2024 05:09:04 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e0c7ae86705bd84b44f37dbbf5a40eb8c84e62685a3474f1d59a0a2b433473`  
		Last Modified: Fri, 25 Oct 2024 05:09:06 GMT  
		Size: 19.2 MB (19247059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-alpine` - unknown; unknown

```console
$ docker pull drupal@sha256:bcf5c6b5c17ceb6e1c81be4f1f175315f09f20d08e01f3263ae12c375e2cc1b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.6 KB (386573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3410907629f2e6d2f70e84026a8e5fcebc4ab4054465ef5ef6e5e70d499bd480`

```dockerfile
```

-	Layers:
	-	`sha256:b6c2a809400e42f6b6a93c965177665cc8574ddd1d69cd21cdc4b170a252c5f9`  
		Last Modified: Fri, 25 Oct 2024 05:09:03 GMT  
		Size: 350.7 KB (350730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12e04d9bb6f3041c2e808bfd0f83215553d973d40acb2c1bbb867fd209d3d370`  
		Last Modified: Fri, 25 Oct 2024 05:09:02 GMT  
		Size: 35.8 KB (35843 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm-alpine` - linux; 386

```console
$ docker pull drupal@sha256:cc1da3ca5ac5c041eeafa379e59a2e152a385a04a435786fcd1b1eabb6df199d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.9 MB (56852240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2143ac202128c34e0eef082c44a40218af86f6dc3c56528ff752b7950fa34ba7`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 06 Sep 2024 22:41:21 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Fri, 06 Sep 2024 22:41:21 GMT
CMD ["/bin/sh"]
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 03 Oct 2024 09:27:25 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 03 Oct 2024 09:27:25 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHP_VERSION=8.3.13
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 03 Oct 2024 09:27:25 GMT
WORKDIR /var/www/html
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
STOPSIGNAL SIGQUIT
# Thu, 03 Oct 2024 09:27:25 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 03 Oct 2024 09:27:25 GMT
CMD ["php-fpm"]
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
ENV DRUPAL_VERSION=11.0.5
# Thu, 03 Oct 2024 09:27:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 03 Oct 2024 09:27:25 GMT
WORKDIR /opt/drupal
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a81be091ca83867d07836d773e08352f7066724252e72bf248e75ba26a2de58`  
		Last Modified: Mon, 28 Oct 2024 22:12:22 GMT  
		Size: 5.5 MB (5465510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b7410a797f9a9267320b4c9b37018f9adf100a763ad90de1cc556011d45bef`  
		Last Modified: Mon, 28 Oct 2024 22:12:21 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dddd90587e3aa0e8acbcc458a95f1453da5f81dcfe7de9e3c3dd7869a4fafef`  
		Last Modified: Mon, 28 Oct 2024 22:12:21 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c401274a26b5f21036d26f1317104d72a255f40bc7baada38851edb4c658dab`  
		Last Modified: Mon, 28 Oct 2024 22:12:22 GMT  
		Size: 12.5 MB (12504589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61589d01d52d491ea1350c957cfa71d82506329f92a7db9023fb85ff6c9a603`  
		Last Modified: Mon, 28 Oct 2024 22:12:22 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41a2a20655521f7c76e995af030259cfbcc8670c92d54bfc83cd2eacd7e278cf`  
		Last Modified: Mon, 28 Oct 2024 22:12:22 GMT  
		Size: 13.4 MB (13431766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a85075df7e740a0f57adcafc19ed29d22ad07e89368548b39f51c912c985f40`  
		Last Modified: Mon, 28 Oct 2024 22:12:23 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62ceee31d792da299ab85ab70a53d76aef0179b54bfe0afa8a0cc1f081f69ee`  
		Last Modified: Mon, 28 Oct 2024 22:12:23 GMT  
		Size: 19.6 KB (19646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49269426edb037a8b25510d3ea055076adeca23e4292d8bc54655f3bb1a9a2e7`  
		Last Modified: Mon, 28 Oct 2024 22:12:23 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2122a8e669e15c2e0d1b3e613560ae8ff7d2b03cc13597dc064ffe5427fa65ca`  
		Last Modified: Mon, 28 Oct 2024 23:23:57 GMT  
		Size: 2.0 MB (1962186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97fcd9283045ff9084d868c2ea99a9f09245180229a7f2fe27715fefef423796`  
		Last Modified: Mon, 28 Oct 2024 23:23:57 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe60b4fb7729f266daa8e637d8fa3ec8a68e346759c3339a45320f6b5a4f0af`  
		Last Modified: Mon, 28 Oct 2024 23:23:57 GMT  
		Size: 738.7 KB (738707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28d24b4e2d8cef76eb4b1b82669207fc8963da912a80b627aeb47ca166218ad`  
		Last Modified: Mon, 28 Oct 2024 23:23:57 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e09ae091ab168504175b1f7fa114683548d581180cba4646d063e093c97b190`  
		Last Modified: Mon, 28 Oct 2024 23:23:58 GMT  
		Size: 19.2 MB (19246939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-alpine` - unknown; unknown

```console
$ docker pull drupal@sha256:a80663439b7a7622eedd999d902d11676cc40fdae1660bea106c1dfcfc8d6e1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.4 KB (389444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29541934601f00bf24d037d7e3c28262caa5dcf64a72e3671edcdef9aba109e5`

```dockerfile
```

-	Layers:
	-	`sha256:877516fa811a0185dd5ef9829bfc38e2ebd3f21afac54d099b35aaa5a7f8c18f`  
		Last Modified: Mon, 28 Oct 2024 23:23:57 GMT  
		Size: 353.3 KB (353309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:077c3d60e88a574b63b115d2c8147664c51eda4d5cd786dab669982bb996506c`  
		Last Modified: Mon, 28 Oct 2024 23:23:57 GMT  
		Size: 36.1 KB (36135 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm-alpine` - linux; ppc64le

```console
$ docker pull drupal@sha256:3e8de1f1ff960c0d7de16d00806ff89ae51086fbbb2925b44281b6b41c5d8090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.0 MB (57977719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c994847044bddc2e51831d419e43ea8c243ec03ed9461a5b1178aa5d37a84770`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 23:15:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 06 Sep 2024 23:15:54 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 06 Sep 2024 23:15:56 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 06 Sep 2024 23:15:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 06 Sep 2024 23:15:57 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 06 Sep 2024 23:15:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 23:15:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 23:15:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 06 Sep 2024 23:59:12 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHP_VERSION=8.3.13
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 03 Oct 2024 09:27:25 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 03 Oct 2024 09:27:25 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 03 Oct 2024 09:27:25 GMT
RUN docker-php-ext-enable sodium
# Thu, 03 Oct 2024 09:27:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 03 Oct 2024 09:27:25 GMT
WORKDIR /var/www/html
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 03 Oct 2024 09:27:25 GMT
STOPSIGNAL SIGQUIT
# Thu, 03 Oct 2024 09:27:25 GMT
EXPOSE 9000
# Thu, 03 Oct 2024 09:27:25 GMT
CMD ["php-fpm"]
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
ENV DRUPAL_VERSION=11.0.5
# Thu, 03 Oct 2024 09:27:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 03 Oct 2024 09:27:25 GMT
WORKDIR /opt/drupal
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
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
	-	`sha256:d8622608d41f825e14aa5bd26799c3251549bceef128cf2eae2f52f1ab78913e`  
		Last Modified: Fri, 25 Oct 2024 00:57:34 GMT  
		Size: 12.5 MB (12504690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b9b2cc7fa22223c46604afd8fd56f225e535ca1e7d006d545233f411a4a3c0`  
		Last Modified: Fri, 25 Oct 2024 00:57:33 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef8924f82b2625f8ef5e7542cf8df90a7ea23be0b16c0aba4eb7c33c1e1db88`  
		Last Modified: Fri, 25 Oct 2024 00:58:17 GMT  
		Size: 16.8 MB (16793437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:647cbae8e31365e26a7ccf044621ddbc54465f9788a82ff7a606cdcd2f3d2fd0`  
		Last Modified: Fri, 25 Oct 2024 00:58:14 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64837aa45d7b316149d05d385f9cf0d1242cc5f508dc01d54707975495ba636a`  
		Last Modified: Fri, 25 Oct 2024 00:58:14 GMT  
		Size: 19.5 KB (19493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c122d2282416fd41b44d88133833d1a36b36278e61186c0d6ee962ce2ef7c45c`  
		Last Modified: Fri, 25 Oct 2024 00:58:14 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17939a7213501ca0e57ac6b8931663244027c7fc53578fe9d9b2e9089bfd2fe`  
		Last Modified: Fri, 25 Oct 2024 04:01:33 GMT  
		Size: 1.7 MB (1680216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4221cf02724933049ecbcd06e737aea908e3333c402b8cd4d2f46c58bed066e7`  
		Last Modified: Fri, 25 Oct 2024 04:01:33 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89631441ff1f6c5b47da85df50c89660d57400b37be429d4ffdaa52bd139d75b`  
		Last Modified: Fri, 25 Oct 2024 04:01:33 GMT  
		Size: 738.7 KB (738716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6edee801a2ee4e6a6bdb8aa66e9cb47982475b79fd86c4685d84bfe20c24d18b`  
		Last Modified: Fri, 25 Oct 2024 04:01:33 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad7cea7e65c0cb71fbb1310d2856528473268ecc63b53bf623986f503354ba1`  
		Last Modified: Fri, 25 Oct 2024 04:01:35 GMT  
		Size: 19.2 MB (19246709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-alpine` - unknown; unknown

```console
$ docker pull drupal@sha256:249c5adba4fc492ccccd3fc0f80385a50d95da754cbb97c759377e71645e8bb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.4 KB (384351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b11e49a17616bc617972207a4650655760ecda7ff87ae2e18f3bc12ae861d1f9`

```dockerfile
```

-	Layers:
	-	`sha256:14df78a7be02ae4e4c8a2f327e5ab17df4b0c2a4d58584e599084de33cfb98be`  
		Last Modified: Fri, 25 Oct 2024 04:01:32 GMT  
		Size: 348.7 KB (348682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e87dcbce32ed0025300e7e4d7edc11451dbe32a36540a3f42328c7202aa05b5`  
		Last Modified: Fri, 25 Oct 2024 04:01:32 GMT  
		Size: 35.7 KB (35669 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm-alpine` - linux; riscv64

```console
$ docker pull drupal@sha256:e20b8e6c33cab4241302b738f1ff255d3bb3ac510b7568ef736eab273a2625a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.4 MB (56441718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdbf2ca7c86409860afc8a5447975925eddef256e1df2a52a36be0f2c931c35f`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:03 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Fri, 06 Sep 2024 22:26:04 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 23:47:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 06 Sep 2024 23:48:04 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 06 Sep 2024 23:48:06 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 06 Sep 2024 23:48:07 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 06 Sep 2024 23:48:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 06 Sep 2024 23:48:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 23:48:10 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 23:48:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 07 Sep 2024 02:23:25 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHP_VERSION=8.3.13
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 03 Oct 2024 09:27:25 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 03 Oct 2024 09:27:25 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 03 Oct 2024 09:27:25 GMT
RUN docker-php-ext-enable sodium
# Thu, 03 Oct 2024 09:27:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 03 Oct 2024 09:27:25 GMT
WORKDIR /var/www/html
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 03 Oct 2024 09:27:25 GMT
STOPSIGNAL SIGQUIT
# Thu, 03 Oct 2024 09:27:25 GMT
EXPOSE 9000
# Thu, 03 Oct 2024 09:27:25 GMT
CMD ["php-fpm"]
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
ENV DRUPAL_VERSION=11.0.5
# Thu, 03 Oct 2024 09:27:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 03 Oct 2024 09:27:25 GMT
WORKDIR /opt/drupal
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160a71fe2c21fa0be03f4ecb3856d46307a8cab34f0749e89c452111c128a28e`  
		Last Modified: Sat, 07 Sep 2024 09:00:45 GMT  
		Size: 3.4 MB (3405216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99de0cdf41fffa764363801fb8a9efbd008b3689317846613f74f55be82ad4ec`  
		Last Modified: Sat, 07 Sep 2024 09:00:41 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f4878284381f1e57d12b980a3d3f2476a10fab26827866948f61cc0a2214a8`  
		Last Modified: Sat, 07 Sep 2024 09:00:41 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d60d72a55a97ca66240c87e7bc1886bc5aa87d97579097a6d9bab88a75ae1d`  
		Last Modified: Fri, 25 Oct 2024 06:19:30 GMT  
		Size: 12.5 MB (12504693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55404ef143ec5be664bfb8b7d19253fad3452d91340eac96ad5cb7f88c34e9e`  
		Last Modified: Fri, 25 Oct 2024 06:19:24 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6565572e238b55b785f604e9609955c4a6d60ee460553a3269f935df74a98e14`  
		Last Modified: Fri, 25 Oct 2024 06:20:50 GMT  
		Size: 15.7 MB (15657790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cbd38af9e162b89a00f8a77e1f0e5abb8ec1f1775d8b00c2ff88c1e57ab8e3d`  
		Last Modified: Fri, 25 Oct 2024 06:20:35 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f197b49ef6cb7bc30e04a4d33b718c5e5225879f2c7f0cdbb6e48ddc73d3f29`  
		Last Modified: Fri, 25 Oct 2024 06:20:35 GMT  
		Size: 19.5 KB (19517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6e120d29123e8cb3c5bc524f3ad28afd9b72da67182498b2aecdb57848a6e3`  
		Last Modified: Fri, 25 Oct 2024 06:20:35 GMT  
		Size: 9.2 KB (9184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb0097caa89b70000f52c0ce9fc9f153d9479217ad08a943d6db8868e92dc8b`  
		Last Modified: Fri, 25 Oct 2024 11:49:17 GMT  
		Size: 1.5 MB (1483034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:887c4e79455887db81b755b908f677c0b407d6782bacdace463008923d30b1c8`  
		Last Modified: Fri, 25 Oct 2024 11:49:16 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4061bb156693fdd4ac8000dae8721424ebab2f71ff7101711054f6db6ac3f7f`  
		Last Modified: Fri, 25 Oct 2024 11:49:17 GMT  
		Size: 738.7 KB (738717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a2acaddaa71928c7f17f6c5efb7a39118b31a2ab0796e39cd290ce83fc1750`  
		Last Modified: Fri, 25 Oct 2024 11:49:17 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:171b4f52196c205a3f7f2ad4acb07050f64ef214369ce7166cfcdeb13d4d276c`  
		Last Modified: Fri, 25 Oct 2024 11:49:20 GMT  
		Size: 19.2 MB (19247573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-alpine` - unknown; unknown

```console
$ docker pull drupal@sha256:00b83046f353a95beb294b4655af42dd17a8f518d4cd08977de4d80a3fab6731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.3 KB (384347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82b6bb6ab9dd052dbf4127fb6f938545a32d928915cc035fa22488134ff14a77`

```dockerfile
```

-	Layers:
	-	`sha256:8eb50d5b70ec64ca7ca6a03b2711a2bda0bff498d69276628ea143fc106e1820`  
		Last Modified: Fri, 25 Oct 2024 11:49:16 GMT  
		Size: 348.7 KB (348678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f22abd81e9a62f16f51f19021263a8bd8601ecc01c979b24aab4d45d59a818f2`  
		Last Modified: Fri, 25 Oct 2024 11:49:16 GMT  
		Size: 35.7 KB (35669 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm-alpine` - linux; s390x

```console
$ docker pull drupal@sha256:a79a6d765fe55d2e93f55fc7e0bf0f2793a9b9e5c1184146c08e06bf6af6957d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57245180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f770ad56aec87ecde133c0d10c1c3cd97212b79532a9ddf4b1e45deda18c0950`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 22:48:17 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 23:21:07 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 06 Sep 2024 23:21:08 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 06 Sep 2024 23:21:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 06 Sep 2024 23:21:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 06 Sep 2024 23:21:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 06 Sep 2024 23:21:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 23:21:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 23:21:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 06 Sep 2024 23:42:29 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHP_VERSION=8.3.13
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 03 Oct 2024 09:27:25 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 03 Oct 2024 09:27:25 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 03 Oct 2024 09:27:25 GMT
RUN docker-php-ext-enable sodium
# Thu, 03 Oct 2024 09:27:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 03 Oct 2024 09:27:25 GMT
WORKDIR /var/www/html
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 03 Oct 2024 09:27:25 GMT
STOPSIGNAL SIGQUIT
# Thu, 03 Oct 2024 09:27:25 GMT
EXPOSE 9000
# Thu, 03 Oct 2024 09:27:25 GMT
CMD ["php-fpm"]
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
ENV DRUPAL_VERSION=11.0.5
# Thu, 03 Oct 2024 09:27:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 03 Oct 2024 09:27:25 GMT
WORKDIR /opt/drupal
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
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
	-	`sha256:4a8632e206b7bc36b0bfe226c5ec5e94154bc411b3677a2903f0f33e8b4d06d3`  
		Last Modified: Fri, 25 Oct 2024 02:46:23 GMT  
		Size: 12.5 MB (12504693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5950b6d1374ddd91229978b32c87237f1a304df6908d46a3e6c6617379120ecb`  
		Last Modified: Fri, 25 Oct 2024 02:46:22 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3cc61644360b59d50134ed38d2defec3ad2ecee51dbdd310c912797074475da`  
		Last Modified: Fri, 25 Oct 2024 02:47:01 GMT  
		Size: 16.2 MB (16188632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d25a374b64e7ce3c35d3398fdc3af9f3b6e1195f7c5b8c682b1142ec2a38f9`  
		Last Modified: Fri, 25 Oct 2024 02:46:59 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68b4f86d9bbe144f80a9d0fdf2b7f54f4c4f0a6e29fb33787b0178664240f18`  
		Last Modified: Fri, 25 Oct 2024 02:46:59 GMT  
		Size: 19.5 KB (19511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5275ccecb6382815ec7bf599f86ac95cf0d82514c4fe1f3815fe804979820ba`  
		Last Modified: Fri, 25 Oct 2024 02:46:59 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f9012e8b42c93d34083a8b8be25e6add00f8f5fa3af1ea519d3eb2b455d6df`  
		Last Modified: Fri, 25 Oct 2024 08:10:35 GMT  
		Size: 1.6 MB (1597081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ddf5fd3cd726e107510d0a4195a2a06a917d283f06ce051f6ad6c73b179b87c`  
		Last Modified: Fri, 25 Oct 2024 08:10:35 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f02e962e211a0c3b0cb3abddc4515db17fb00109a35619dbd42a74901d443b6`  
		Last Modified: Fri, 25 Oct 2024 08:10:35 GMT  
		Size: 738.7 KB (738717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aea1bb7ab5eaef17667bf03f27f2c3697e855d4b9a7546837c76b3178584aa3`  
		Last Modified: Fri, 25 Oct 2024 08:10:35 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4655c800053586d0017c966f1b6e336655ba66ae6a01103a5a985d28e1a3bd69`  
		Last Modified: Fri, 25 Oct 2024 08:10:36 GMT  
		Size: 19.2 MB (19247243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-alpine` - unknown; unknown

```console
$ docker pull drupal@sha256:e3dae868535d6020c00e07b7558ab6e050bbea9aef12850538d64119e5e8f0a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.1 KB (384121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9d8e243c5187007c95ee0d061ce969f0f9cb006d978e7c4de7599500a5eb130`

```dockerfile
```

-	Layers:
	-	`sha256:a86ffeb6f90adfcad20c39b845a74d06355a8cc722cbc9026ed05e058154e3e3`  
		Last Modified: Fri, 25 Oct 2024 08:10:34 GMT  
		Size: 348.6 KB (348576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aeb452d0488b01deec213f40b90af9ac9100c933d34bc23dee886d45623356b6`  
		Last Modified: Fri, 25 Oct 2024 08:10:34 GMT  
		Size: 35.5 KB (35545 bytes)  
		MIME: application/vnd.in-toto+json
