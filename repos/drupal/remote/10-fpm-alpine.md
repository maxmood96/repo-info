## `drupal:10-fpm-alpine`

```console
$ docker pull drupal@sha256:9f587f7fb604d9d0196a8b9ecdb75bc723ec1994bb9b228a157393ae8feb99c4
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

### `drupal:10-fpm-alpine` - linux; amd64

```console
$ docker pull drupal@sha256:cf9b8ac4901644b7cff7aa2479d14db7f87c15595709f6242ace540ae75218f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56163727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee0bd38bd49958ecb3fcddf1a854013c62695f01a0c987e23eac3c98ab138d32`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 00:32:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 07 Sep 2024 00:32:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Sat, 07 Sep 2024 00:32:04 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 07 Sep 2024 00:32:04 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 07 Sep 2024 00:32:05 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 07 Sep 2024 00:32:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Sep 2024 00:32:05 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Sep 2024 00:32:05 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 07 Sep 2024 01:23:30 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 26 Sep 2024 23:34:37 GMT
ENV PHP_VERSION=8.2.24
# Thu, 26 Sep 2024 23:34:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.24.tar.xz.asc
# Thu, 26 Sep 2024 23:34:38 GMT
ENV PHP_SHA256=80a5225746a9eb484475b312d4c626c63a88a037d8e56d214f30205e1ba1411a
# Thu, 26 Sep 2024 23:34:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 26 Sep 2024 23:34:44 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Sep 2024 23:43:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 26 Sep 2024 23:43:13 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 26 Sep 2024 23:43:14 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Sep 2024 23:43:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Sep 2024 23:43:14 GMT
WORKDIR /var/www/html
# Thu, 26 Sep 2024 23:43:15 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 26 Sep 2024 23:43:15 GMT
STOPSIGNAL SIGQUIT
# Thu, 26 Sep 2024 23:43:15 GMT
EXPOSE 9000
# Thu, 26 Sep 2024 23:43:15 GMT
CMD ["php-fpm"]
# Thu, 03 Oct 2024 15:27:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
ENV DRUPAL_VERSION=10.3.6
# Thu, 03 Oct 2024 15:27:16 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 03 Oct 2024 15:27:16 GMT
WORKDIR /opt/drupal
# Thu, 03 Oct 2024 15:27:16 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
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
	-	`sha256:14b6974b37323387584ee3677fc2200fb09e101404c8487e78f90844edcf3950`  
		Last Modified: Fri, 27 Sep 2024 01:06:41 GMT  
		Size: 12.1 MB (12131299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20aee302f78733f29a1aab06e21f568de268649dce468803fe3893f86778817`  
		Last Modified: Fri, 27 Sep 2024 01:06:40 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9138929e2943f3244dc2833bcabbd35cefa32186bd2c120c7149f716b3796cd`  
		Last Modified: Fri, 27 Sep 2024 01:07:04 GMT  
		Size: 13.3 MB (13335864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c16e8aa640b3d649b29a25fd79fb978f7ee4c3f5d730e57fea207daa2f5d8e`  
		Last Modified: Fri, 27 Sep 2024 01:07:02 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428c6165a2655930c22d5d69643c6c6698b48b70fdb07145feff35dff2d246fc`  
		Last Modified: Fri, 27 Sep 2024 01:07:02 GMT  
		Size: 19.7 KB (19707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41e53bcf0d0aedaf210a6db1bacb20e0e6e874fca729a1ea7db5315d5e420a4`  
		Last Modified: Fri, 27 Sep 2024 01:07:02 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62dce535591b0286c3c872c1eaf0cf0954a7ce1930bec1f68019c7eb6cb6f321`  
		Last Modified: Mon, 07 Oct 2024 20:53:48 GMT  
		Size: 1.9 MB (1898555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037b8605216f2c44f90236238067870524dda27927f77722cdd163e0447f790f`  
		Last Modified: Mon, 07 Oct 2024 20:53:48 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7231b88889b6577eaf0a8fdb89aae3a3029f2c6b3a7f7882c5edd46ce399c488`  
		Last Modified: Mon, 07 Oct 2024 20:53:48 GMT  
		Size: 738.7 KB (738715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c2622e4059892898480198e088405f4d4919d78897844411b84270fcdc381d7`  
		Last Modified: Mon, 07 Oct 2024 20:53:48 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d16071e66dec0e41afccf11412ee7e4c0204c15ca6e66ceb9d662cdeabf826`  
		Last Modified: Mon, 07 Oct 2024 20:53:50 GMT  
		Size: 21.1 MB (21119381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine` - unknown; unknown

```console
$ docker pull drupal@sha256:1ce254d7710854b72c5293d79237f835adbd4d012f11cf6cc39ff5dc0a3490b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.4 KB (385352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4979b3c12a3eeae425de0b6e897a745df1f9b7dc0ad1d536911ae7b724c569d8`

```dockerfile
```

-	Layers:
	-	`sha256:b21911bfecfe7f0563704fd2a13d7a9f484169fbdd661d5521e5cd60a8297114`  
		Last Modified: Mon, 07 Oct 2024 20:53:48 GMT  
		Size: 351.1 KB (351135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55da1df960d9ac4a8159b79a5c848470fb1006d2cda84aa126ebec567f9fe468`  
		Last Modified: Mon, 07 Oct 2024 20:53:48 GMT  
		Size: 34.2 KB (34217 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine` - linux; arm variant v6

```console
$ docker pull drupal@sha256:d95fd0182f782dcaf225b63cc4f4401c5db2bf0b065dcb2f51b787f72d85bf1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.2 MB (54222771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cb10dcba04fca1d3837d8c3896c92b1d78f8d327584b5dc874578f7600f3e5a`
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
# Sat, 07 Sep 2024 00:10:58 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 26 Sep 2024 22:21:35 GMT
ENV PHP_VERSION=8.2.24
# Thu, 26 Sep 2024 22:21:35 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.24.tar.xz.asc
# Thu, 26 Sep 2024 22:21:35 GMT
ENV PHP_SHA256=80a5225746a9eb484475b312d4c626c63a88a037d8e56d214f30205e1ba1411a
# Thu, 26 Sep 2024 22:21:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 26 Sep 2024 22:21:41 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Sep 2024 22:30:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 26 Sep 2024 22:30:34 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 26 Sep 2024 22:30:35 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Sep 2024 22:30:36 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Sep 2024 22:30:36 GMT
WORKDIR /var/www/html
# Thu, 26 Sep 2024 22:30:37 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 26 Sep 2024 22:30:37 GMT
STOPSIGNAL SIGQUIT
# Thu, 26 Sep 2024 22:30:38 GMT
EXPOSE 9000
# Thu, 26 Sep 2024 22:30:38 GMT
CMD ["php-fpm"]
# Thu, 03 Oct 2024 15:27:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
ENV DRUPAL_VERSION=10.3.6
# Thu, 03 Oct 2024 15:27:16 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 03 Oct 2024 15:27:16 GMT
WORKDIR /opt/drupal
# Thu, 03 Oct 2024 15:27:16 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
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
	-	`sha256:1626f58189cedc9e9de32f1ecfc64ce30005dc5ba226f4c3195f2610b885b3b5`  
		Last Modified: Thu, 26 Sep 2024 23:23:13 GMT  
		Size: 12.1 MB (12131291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2597795e00baa246783e513d801b1c15969d19a3dcb4e6fb83917ba185d45b45`  
		Last Modified: Thu, 26 Sep 2024 23:23:11 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6731c3567a6020937fd93edbbb9d8d29a9c95514dc3dceede8c666e4db85b5`  
		Last Modified: Thu, 26 Sep 2024 23:23:39 GMT  
		Size: 12.2 MB (12181394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d0d2bfd8b4368d65477c552dba866c7407bddb2e7f477c18a2e267dc0660c2f`  
		Last Modified: Thu, 26 Sep 2024 23:23:36 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f56942133deaba5985ea20304e45c57fb1a65588c1c04c9fc9be3190403a4b`  
		Last Modified: Thu, 26 Sep 2024 23:23:36 GMT  
		Size: 19.5 KB (19495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928d51222fd81cf9d22d2b71ad575921e4d1f84fc734cc2a8552773a3395e766`  
		Last Modified: Thu, 26 Sep 2024 23:23:36 GMT  
		Size: 9.2 KB (9183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b498987c1bb2be5a9feeba3aa1813864db1e31b823b9320ed19ddda28ad8e2`  
		Last Modified: Fri, 27 Sep 2024 00:41:46 GMT  
		Size: 1.4 MB (1382777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a698e23ba80e4700cb6adb71e1d2dfface7d84201cd78d16a3040d9513d4f4e5`  
		Last Modified: Fri, 27 Sep 2024 00:41:46 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42c85016ea18ca5069ee52443b0c975d2aa42a40a16755bee7c1f00e8bbfc47f`  
		Last Modified: Thu, 03 Oct 2024 17:53:33 GMT  
		Size: 738.3 KB (738326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8774d934d16d207ea71a3e442361cea9d0d33ec6b341970e2feb59a4ae34999c`  
		Last Modified: Thu, 03 Oct 2024 17:53:33 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd6d9828e9b29e5a884b90403590fa6aace5f0a11fed2f0c07748b5df55435b`  
		Last Modified: Mon, 07 Oct 2024 18:01:14 GMT  
		Size: 21.1 MB (21119488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine` - unknown; unknown

```console
$ docker pull drupal@sha256:954c4f27b7531f0c297e1ef2b136afdae3dcb18e227cb4fbba36782524149559
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 KB (34211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7b4a3f437c2bdda3fdf74fd99d84b79df38142cf9b82bae85873f9001de05f6`

```dockerfile
```

-	Layers:
	-	`sha256:69dd7175c9e6ccb3eac6907206627c4147ab9ca83cdba8a94276786b7ee570a0`  
		Last Modified: Mon, 07 Oct 2024 18:01:12 GMT  
		Size: 34.2 KB (34211 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine` - linux; arm variant v7

```console
$ docker pull drupal@sha256:81e6abd73a881ee5fb1b4736997c70c054aabcb1c5181464be6e0a8aa1b65bb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52876281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41f1eb22e7ea65b0ac02f678136a347c7693b9ddf1370ec39a6749b8173b5d1e`
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
# Fri, 06 Sep 2024 23:04:26 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 26 Sep 2024 23:56:21 GMT
ENV PHP_VERSION=8.2.24
# Thu, 26 Sep 2024 23:56:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.24.tar.xz.asc
# Thu, 26 Sep 2024 23:56:21 GMT
ENV PHP_SHA256=80a5225746a9eb484475b312d4c626c63a88a037d8e56d214f30205e1ba1411a
# Thu, 26 Sep 2024 23:56:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 26 Sep 2024 23:56:26 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 27 Sep 2024 00:03:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 27 Sep 2024 00:03:29 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 27 Sep 2024 00:03:30 GMT
RUN docker-php-ext-enable sodium
# Fri, 27 Sep 2024 00:03:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 27 Sep 2024 00:03:30 GMT
WORKDIR /var/www/html
# Fri, 27 Sep 2024 00:03:31 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 27 Sep 2024 00:03:31 GMT
STOPSIGNAL SIGQUIT
# Fri, 27 Sep 2024 00:03:31 GMT
EXPOSE 9000
# Fri, 27 Sep 2024 00:03:31 GMT
CMD ["php-fpm"]
# Thu, 03 Oct 2024 15:27:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
ENV DRUPAL_VERSION=10.3.6
# Thu, 03 Oct 2024 15:27:16 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 03 Oct 2024 15:27:16 GMT
WORKDIR /opt/drupal
# Thu, 03 Oct 2024 15:27:16 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
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
	-	`sha256:d085fc144b4d853d3a9442d055237a5d4983c102e36ec8422273743958905824`  
		Last Modified: Fri, 27 Sep 2024 01:15:01 GMT  
		Size: 12.1 MB (12131294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4967615c959c08d53e989faf2904df9afe8c025bac2f3d0c7c69e8184f025ef1`  
		Last Modified: Fri, 27 Sep 2024 01:15:00 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5860c1c8fdeec92eb4d8477f742a03cdb1a7c125c01b43afd25cabbc45501a`  
		Last Modified: Fri, 27 Sep 2024 01:15:25 GMT  
		Size: 11.4 MB (11405518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ff016129be9645dded92dc7389711130765673b5132f56c74c2dc8d5db0fcd`  
		Last Modified: Fri, 27 Sep 2024 01:15:23 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bd2bb8fda50ee32d87e4a78d14a513cd91074bc43e7bfc87b0d00417d09f8da`  
		Last Modified: Fri, 27 Sep 2024 01:15:23 GMT  
		Size: 19.5 KB (19507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c167560330cfa8672740886289362feb566b534f460c1ed26eefe51a363a1e3`  
		Last Modified: Fri, 27 Sep 2024 01:15:23 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a588e223ba3d321c3abcb54cf067ffc0e791419fa8832a25eb8a231455435497`  
		Last Modified: Fri, 27 Sep 2024 10:26:03 GMT  
		Size: 1.3 MB (1273612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae14e22898c2edb657b8e409e954a799812c4bbbb9452e6200d147080d804d1e`  
		Last Modified: Fri, 27 Sep 2024 10:26:03 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:826a5a97b2046bc268b50f9fc937c176f0c82d8c8cba00de0ce9273dbe422c98`  
		Last Modified: Thu, 03 Oct 2024 18:06:15 GMT  
		Size: 738.3 KB (738327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb75db19db7d4e21d35ee690c8be7ed01d2b748c5e6ebc788dbe88378cd13c1`  
		Last Modified: Thu, 03 Oct 2024 18:06:16 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2519276abb57f93d8b74587f8da21ef5af16ed51c940768cb2a963d5ba285de`  
		Last Modified: Mon, 07 Oct 2024 18:14:08 GMT  
		Size: 21.1 MB (21119233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine` - unknown; unknown

```console
$ docker pull drupal@sha256:4502759a60d93fda3dc1a7109f4400579e67fc831bc2b721e67a11f333f18fb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.8 KB (382801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12c82a2fabc3926fde70c98f07f34a6e01f9f52398d1c23e22a62241d05eab4d`

```dockerfile
```

-	Layers:
	-	`sha256:2b5211321988ac72d0f718db4295a67f965bd510ac7ea8f4d730b99cfd9a3d0f`  
		Last Modified: Mon, 07 Oct 2024 18:14:06 GMT  
		Size: 348.4 KB (348371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c91aca081dd0e08de81cd42d8269a88adc75a3d83f85bbf8c65ecc5364e8854a`  
		Last Modified: Mon, 07 Oct 2024 18:14:06 GMT  
		Size: 34.4 KB (34430 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:9750407cee149a26ceeda5c5a6c463d824700ad6e2fe12052e7a75825e4be4a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.0 MB (57033107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cf54c15a97377f5e5f78b53fd9c2bb3a55a80641065cb6c44e91858ae5b9e57`
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
# Sat, 07 Sep 2024 01:32:33 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 26 Sep 2024 23:20:51 GMT
ENV PHP_VERSION=8.2.24
# Thu, 26 Sep 2024 23:20:51 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.24.tar.xz.asc
# Thu, 26 Sep 2024 23:20:51 GMT
ENV PHP_SHA256=80a5225746a9eb484475b312d4c626c63a88a037d8e56d214f30205e1ba1411a
# Thu, 26 Sep 2024 23:20:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 26 Sep 2024 23:20:56 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Sep 2024 23:28:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 26 Sep 2024 23:28:54 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 26 Sep 2024 23:28:55 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Sep 2024 23:28:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Sep 2024 23:28:55 GMT
WORKDIR /var/www/html
# Thu, 26 Sep 2024 23:28:55 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 26 Sep 2024 23:28:55 GMT
STOPSIGNAL SIGQUIT
# Thu, 26 Sep 2024 23:28:56 GMT
EXPOSE 9000
# Thu, 26 Sep 2024 23:28:56 GMT
CMD ["php-fpm"]
# Thu, 03 Oct 2024 15:27:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
ENV DRUPAL_VERSION=10.3.6
# Thu, 03 Oct 2024 15:27:16 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 03 Oct 2024 15:27:16 GMT
WORKDIR /opt/drupal
# Thu, 03 Oct 2024 15:27:16 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
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
	-	`sha256:144a45efbef71a0ddbfc477b25417715f317afb9c9ae5253f9cddb0c51503aa4`  
		Last Modified: Fri, 27 Sep 2024 00:49:32 GMT  
		Size: 12.1 MB (12131289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4435815a8ad1b5e78e94667521b4fa69fe25360915e854dea7f5471f4cf993c`  
		Last Modified: Fri, 27 Sep 2024 00:49:32 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:732a7a60895dba63f76b829342ac0f3fb90ae242f72efd9c036dd622cd385db6`  
		Last Modified: Fri, 27 Sep 2024 00:49:56 GMT  
		Size: 13.4 MB (13414626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9458245f4dc4ba4a46190f6b89e37e9129b1b3119be609a803cb393db2649106`  
		Last Modified: Fri, 27 Sep 2024 00:49:54 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38029843aae9f10bffc16627304f5827756475e59d197468133a4025a7a83803`  
		Last Modified: Fri, 27 Sep 2024 00:49:54 GMT  
		Size: 19.5 KB (19483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a0cf9036c22c09fe1530c50ed6f2d865c44c625e287d90f10ea88c2cc79f2b`  
		Last Modified: Fri, 27 Sep 2024 00:49:54 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a1a3fb7a11432bb698303f2cb6a7483c427a0c92265c7f26bc8f324896b1fb`  
		Last Modified: Thu, 03 Oct 2024 18:18:05 GMT  
		Size: 2.2 MB (2174836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5563e5e5ea7a23905bbe67a5f4b71983c0837aa73a379b68a1dacff8d4cecb`  
		Last Modified: Thu, 03 Oct 2024 18:18:04 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b525980f20e8617ca9aab0cee162a8384410e5345824a4eb6647bad2a2e7886e`  
		Last Modified: Mon, 07 Oct 2024 21:04:09 GMT  
		Size: 738.7 KB (738724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7963ae9d790a2f511e869df9c66e09b10c8d0542c6de09db69520cd91ccfe8f`  
		Last Modified: Mon, 07 Oct 2024 21:04:08 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d09deb8f0e53ecf5488760e0a28af2cdf215712e4e1d28b9a9d4617571a01d2f`  
		Last Modified: Mon, 07 Oct 2024 21:04:10 GMT  
		Size: 21.1 MB (21119396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine` - unknown; unknown

```console
$ docker pull drupal@sha256:7cfaefcb72da575a8c5185269ab150ecb73ae942442a7b64424be9255e67711c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.9 KB (382922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:817ddabb062178a44a834150578db4cb3da2fc0a5e202c853a1f1a906c4f2770`

```dockerfile
```

-	Layers:
	-	`sha256:bd9f8bcaf0af71a9e65b2f82fac3227eca05c44b3c15df181fb0aa204d6b9156`  
		Last Modified: Mon, 07 Oct 2024 21:04:08 GMT  
		Size: 348.4 KB (348423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92c1728ba3ec3c4eb4899a4415030f9c8f163f09ce0df459cd1ce474e4d377a3`  
		Last Modified: Mon, 07 Oct 2024 21:04:08 GMT  
		Size: 34.5 KB (34499 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine` - linux; 386

```console
$ docker pull drupal@sha256:89ee44f12f730ee92d79a98560f1241ce75138cbd6f8108e2ba724f2a4e56983
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56486318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49fcf3b64ce006112d622513c058916100299e0dadb375c19e1389ea336ababe`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 06 Sep 2024 22:41:21 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Fri, 06 Sep 2024 22:41:21 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 22:57:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 06 Sep 2024 22:57:51 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 06 Sep 2024 22:57:52 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 06 Sep 2024 22:57:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 06 Sep 2024 22:57:52 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 06 Sep 2024 22:57:52 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 22:57:53 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 22:57:53 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 07 Sep 2024 00:24:55 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 27 Sep 2024 01:08:34 GMT
ENV PHP_VERSION=8.2.24
# Fri, 27 Sep 2024 01:08:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.24.tar.xz.asc
# Fri, 27 Sep 2024 01:08:34 GMT
ENV PHP_SHA256=80a5225746a9eb484475b312d4c626c63a88a037d8e56d214f30205e1ba1411a
# Fri, 27 Sep 2024 01:08:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 27 Sep 2024 01:08:39 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 27 Sep 2024 01:22:02 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 27 Sep 2024 01:22:02 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 27 Sep 2024 01:22:04 GMT
RUN docker-php-ext-enable sodium
# Fri, 27 Sep 2024 01:22:04 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 27 Sep 2024 01:22:04 GMT
WORKDIR /var/www/html
# Fri, 27 Sep 2024 01:22:04 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 27 Sep 2024 01:22:05 GMT
STOPSIGNAL SIGQUIT
# Fri, 27 Sep 2024 01:22:05 GMT
EXPOSE 9000
# Fri, 27 Sep 2024 01:22:05 GMT
CMD ["php-fpm"]
# Thu, 03 Oct 2024 15:27:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
ENV DRUPAL_VERSION=10.3.6
# Thu, 03 Oct 2024 15:27:16 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 03 Oct 2024 15:27:16 GMT
WORKDIR /opt/drupal
# Thu, 03 Oct 2024 15:27:16 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
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
	-	`sha256:a95bbce46d856900c2d09cc8e6936792aa2c16a0168152eec91c75cda5546b5e`  
		Last Modified: Fri, 27 Sep 2024 03:31:40 GMT  
		Size: 12.1 MB (12131291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3864122d099e9cb75bc64aead88b2e2d5afbf9a8c073d0fb24ecf32d8c08e410`  
		Last Modified: Fri, 27 Sep 2024 03:31:38 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7da61f4d3b4a6947f992ff1f0d90185183849e3282b30cee8af6952abbb7a1`  
		Last Modified: Fri, 27 Sep 2024 03:32:06 GMT  
		Size: 13.7 MB (13704148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ac95cef2fe8eacc55f50353da0820404b4823ea27a9f35be8de937688a3b25`  
		Last Modified: Fri, 27 Sep 2024 03:32:03 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086d4bdfffdbe33c51f5380ca6049ea34d552cacc542123f8e202ac7f12f7c80`  
		Last Modified: Fri, 27 Sep 2024 03:32:03 GMT  
		Size: 19.7 KB (19700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124e14b8183cae7591f1457a38c5f3ac6b5f9b6e9134c86a2f27990068ad3856`  
		Last Modified: Fri, 27 Sep 2024 03:32:03 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c68f46e7e2badf7a5a93e432864b816021c37c061a3b42254b3bcbbaeae0b86`  
		Last Modified: Mon, 07 Oct 2024 20:53:39 GMT  
		Size: 2.0 MB (1958197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40dd48e606b845017c6bc52b30d2f90bfd015563f2a4987975ee32512fda5e0a`  
		Last Modified: Mon, 07 Oct 2024 20:53:39 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5bd14d5da9ef600312d44f1e93786ff409627d1f1b88f41178db161f58c9056`  
		Last Modified: Mon, 07 Oct 2024 20:53:39 GMT  
		Size: 738.7 KB (738715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:267ca11eceefcd0ec9d7f37d1684609edb2dc1cda2aef5f0be6ae6ab9b31d676`  
		Last Modified: Mon, 07 Oct 2024 20:53:39 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:876f8c84f4f09d03009d8a83ddf7e9ec37db64b92f7d74f303eb5156b7083cd6`  
		Last Modified: Mon, 07 Oct 2024 20:53:40 GMT  
		Size: 21.1 MB (21119412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine` - unknown; unknown

```console
$ docker pull drupal@sha256:84cfce9dc31e7467bb8a2d7f776c9348873c37bf1f80b935e7c5fd1268818906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.1 KB (385124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94a2211f27c453569bf7c2e47c2b4db63b151c70bd777b828c591fde73d4acc7`

```dockerfile
```

-	Layers:
	-	`sha256:d5552d888cf4be87c47b3c7db80c4a3dd73b77e7997586349f7b94a45f01b91a`  
		Last Modified: Mon, 07 Oct 2024 20:53:39 GMT  
		Size: 351.1 KB (351070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c74f5ceb261515b16f002999650cd0ccdb9eb930d4e170c997d72f7ec5c50b53`  
		Last Modified: Mon, 07 Oct 2024 20:53:39 GMT  
		Size: 34.1 KB (34054 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine` - linux; ppc64le

```console
$ docker pull drupal@sha256:899f524ab75e78fd5c8aad999606c2735f0a7773f7879a03cc834601bfb61f26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56534969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eae71b0eaa059867012f35a76cbe189f8ca1a348e4516b2de0f331ce7de422b`
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
# Sat, 07 Sep 2024 00:41:34 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 26 Sep 2024 23:51:57 GMT
ENV PHP_VERSION=8.2.24
# Thu, 26 Sep 2024 23:51:57 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.24.tar.xz.asc
# Thu, 26 Sep 2024 23:51:57 GMT
ENV PHP_SHA256=80a5225746a9eb484475b312d4c626c63a88a037d8e56d214f30205e1ba1411a
# Thu, 26 Sep 2024 23:52:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 26 Sep 2024 23:52:04 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Sep 2024 23:57:02 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 26 Sep 2024 23:57:03 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 26 Sep 2024 23:57:05 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Sep 2024 23:57:05 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Sep 2024 23:57:05 GMT
WORKDIR /var/www/html
# Thu, 26 Sep 2024 23:57:06 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 26 Sep 2024 23:57:06 GMT
STOPSIGNAL SIGQUIT
# Thu, 26 Sep 2024 23:57:07 GMT
EXPOSE 9000
# Thu, 26 Sep 2024 23:57:07 GMT
CMD ["php-fpm"]
# Thu, 03 Oct 2024 15:27:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
ENV DRUPAL_VERSION=10.3.6
# Thu, 03 Oct 2024 15:27:16 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 03 Oct 2024 15:27:16 GMT
WORKDIR /opt/drupal
# Thu, 03 Oct 2024 15:27:16 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
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
	-	`sha256:8af4b850980f655963574ee5f2a3e704622f226d19e3352db0cf31b5c3294be1`  
		Last Modified: Fri, 27 Sep 2024 01:01:45 GMT  
		Size: 12.1 MB (12131297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2abca31f38d435d83b9607fd56a44b436f3eafd8f675cc1e2d44e68b5edc44df`  
		Last Modified: Fri, 27 Sep 2024 01:01:44 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73edead7e6d33325fabf6a7aa38140987f7cc5d433f8b5d8232352c9f9238f65`  
		Last Modified: Fri, 27 Sep 2024 01:02:11 GMT  
		Size: 13.9 MB (13852428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1e78e87ab109129adc9e64167a6359db698b683fd1774d9f08e72a63a6da46`  
		Last Modified: Fri, 27 Sep 2024 01:02:08 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e703f0c0e01f3c3e8e01c286913026d219f8c9eacca75e143d5aa8eca81fa092`  
		Last Modified: Fri, 27 Sep 2024 01:02:08 GMT  
		Size: 19.5 KB (19488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed344d586e53a1ccba6e76654e822f1199888ba710f1d08bc88744b1b3c2793f`  
		Last Modified: Fri, 27 Sep 2024 01:02:08 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:779c760eda1b538f5170268574346b66df7ea4c71aa0396ee4e6aa1350cfde46`  
		Last Modified: Thu, 03 Oct 2024 18:07:30 GMT  
		Size: 1.7 MB (1679293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1de7ba078e6cf713c3514b122c09685bad766d055bf06da326ad195f6a32ee1`  
		Last Modified: Thu, 03 Oct 2024 18:07:30 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e345afa891146fe01c39fc30ea42398a7218cedec24c56c160ba01ef8f410e4`  
		Last Modified: Mon, 07 Oct 2024 21:04:15 GMT  
		Size: 738.7 KB (738722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfeda96eaed3acf9976d02a19be3aefe04440c9ee5b9108f4b288e85be95bc7`  
		Last Modified: Mon, 07 Oct 2024 21:04:15 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0652618bd4450b25b3604f193919a1f45a40b4204060038155f6db01ae5a12`  
		Last Modified: Mon, 07 Oct 2024 21:04:16 GMT  
		Size: 21.1 MB (21119289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine` - unknown; unknown

```console
$ docker pull drupal@sha256:a2d4a8ad679567ea44a3f85d9b8c39a4359400327de6dc766a162d3307de7d5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.7 KB (380747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01646e8012054dd0720fbbd3ad4508776a034053578f342459c2bbbde941298c`

```dockerfile
```

-	Layers:
	-	`sha256:7764341c32259e959b1fed6da4504983f40b6a7a358ab002e56f0c5820387566`  
		Last Modified: Mon, 07 Oct 2024 21:04:15 GMT  
		Size: 346.4 KB (346399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78a4b37062ce9b4a8aafb370120110cbc1bc13d5f4330f62f44ab2fbcf5b8856`  
		Last Modified: Mon, 07 Oct 2024 21:04:14 GMT  
		Size: 34.3 KB (34348 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine` - linux; riscv64

```console
$ docker pull drupal@sha256:867ad3cefa1d252fffa3d9ce02f8c2b0d6ea60d9fba7c98b2f1dd2d451591b73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.0 MB (54983911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50159d1613a45272325662a9b46fe559c73c06c9fdebacb2f2d7c8313bf5b43f`
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
# Sat, 07 Sep 2024 04:48:01 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 27 Sep 2024 02:44:52 GMT
ENV PHP_VERSION=8.2.24
# Fri, 27 Sep 2024 02:44:52 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.24.tar.xz.asc
# Fri, 27 Sep 2024 02:44:53 GMT
ENV PHP_SHA256=80a5225746a9eb484475b312d4c626c63a88a037d8e56d214f30205e1ba1411a
# Fri, 27 Sep 2024 02:45:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 27 Sep 2024 02:45:26 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 27 Sep 2024 04:18:37 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 27 Sep 2024 04:18:39 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 27 Sep 2024 04:18:47 GMT
RUN docker-php-ext-enable sodium
# Fri, 27 Sep 2024 04:18:47 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 27 Sep 2024 04:18:48 GMT
WORKDIR /var/www/html
# Fri, 27 Sep 2024 04:18:50 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 27 Sep 2024 04:18:51 GMT
STOPSIGNAL SIGQUIT
# Fri, 27 Sep 2024 04:18:51 GMT
EXPOSE 9000
# Fri, 27 Sep 2024 04:18:52 GMT
CMD ["php-fpm"]
# Thu, 03 Oct 2024 15:27:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
ENV DRUPAL_VERSION=10.3.6
# Thu, 03 Oct 2024 15:27:16 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 03 Oct 2024 15:27:16 GMT
WORKDIR /opt/drupal
# Thu, 03 Oct 2024 15:27:16 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
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
	-	`sha256:dddeec9876ec898927bc3afdb800ee78fef13e9e2b6cc82c4305fbafc9417cdf`  
		Last Modified: Fri, 27 Sep 2024 07:27:03 GMT  
		Size: 12.1 MB (12131300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8c5dfda73c315519017670d748c1b87f5e2c02a4c243e9981225a6c78d80cd`  
		Last Modified: Fri, 27 Sep 2024 07:26:57 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deea25e51a274843175a36c2cc2c00256c840fd17b1d82f8a54fd70f989e45a9`  
		Last Modified: Fri, 27 Sep 2024 07:27:51 GMT  
		Size: 12.7 MB (12703558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14bfaa03a30655a8149c1142c3c6b7bce5d104b340fc98c1592edb20b149d8f2`  
		Last Modified: Fri, 27 Sep 2024 07:27:40 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6a3ed3379bcd4edca48edc947ab395ddbf2bafb6e95df16f421790f1c12d73`  
		Last Modified: Fri, 27 Sep 2024 07:27:40 GMT  
		Size: 19.5 KB (19503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c49a62fc31791ca5d0df6e5bca80f3d1eeff981f8b0f04c66d6457fd523094d`  
		Last Modified: Fri, 27 Sep 2024 07:27:40 GMT  
		Size: 9.2 KB (9184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c02f9807b48c11bcc6a08f499610733924c09f403d5d8b121e1e3baa66135d5`  
		Last Modified: Fri, 27 Sep 2024 15:42:44 GMT  
		Size: 1.5 MB (1480698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9b77a880adc654e096138c21f17567be32f5f2c270b4c5b4b23573aa4be0d8`  
		Last Modified: Fri, 27 Sep 2024 15:42:43 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2857cd0db76399cbd67dc7823a6bb5ee81b13103284730452b00e0a887a536`  
		Last Modified: Mon, 07 Oct 2024 21:02:41 GMT  
		Size: 738.7 KB (738722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3c44dd3704d28b2a6782febeb8bf95646f7de644bf65983261159eadf281e8`  
		Last Modified: Mon, 07 Oct 2024 21:02:41 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e9a88543e8a7c1b8278ee8fac6a81f6d72ade218faf0533004200bf6d702a0f`  
		Last Modified: Mon, 07 Oct 2024 21:02:44 GMT  
		Size: 21.1 MB (21119737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine` - unknown; unknown

```console
$ docker pull drupal@sha256:c899ef42c7648c2f07901d54bbf01bbd4626e5963b13c1c3a7db8626a5ca5861
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.7 KB (380744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e50f8cbf175bdfeaa48f598186aa6b545230dd0bc3a1181d54a4de23043dbf4`

```dockerfile
```

-	Layers:
	-	`sha256:ce962971e0300439c808cb83468887dea818f23f62ed9408288b3e8f5a326643`  
		Last Modified: Mon, 07 Oct 2024 21:02:41 GMT  
		Size: 346.4 KB (346395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1176c28692be0d40b200e4e8decf96d232e31333fe910e9e92c2e4f4b4d17add`  
		Last Modified: Mon, 07 Oct 2024 21:02:41 GMT  
		Size: 34.3 KB (34349 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine` - linux; s390x

```console
$ docker pull drupal@sha256:e3fd041bf7f098deca7d7495f3f1016d2abeb46da0a3dc40a98aaefdac86f328
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.9 MB (55881634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d68078965a6f8c091ea34bfc90285dad9c2bea0c84cde5d9366f7654b46689d`
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
# Sat, 07 Sep 2024 00:02:19 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 26 Sep 2024 23:09:21 GMT
ENV PHP_VERSION=8.2.24
# Thu, 26 Sep 2024 23:09:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.24.tar.xz.asc
# Thu, 26 Sep 2024 23:09:21 GMT
ENV PHP_SHA256=80a5225746a9eb484475b312d4c626c63a88a037d8e56d214f30205e1ba1411a
# Thu, 26 Sep 2024 23:09:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 26 Sep 2024 23:09:25 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Sep 2024 23:15:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 26 Sep 2024 23:15:54 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 26 Sep 2024 23:15:55 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Sep 2024 23:15:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Sep 2024 23:15:55 GMT
WORKDIR /var/www/html
# Thu, 26 Sep 2024 23:15:55 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 26 Sep 2024 23:15:56 GMT
STOPSIGNAL SIGQUIT
# Thu, 26 Sep 2024 23:15:56 GMT
EXPOSE 9000
# Thu, 26 Sep 2024 23:15:56 GMT
CMD ["php-fpm"]
# Thu, 03 Oct 2024 15:27:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
ENV DRUPAL_VERSION=10.3.6
# Thu, 03 Oct 2024 15:27:16 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 03 Oct 2024 15:27:16 GMT
WORKDIR /opt/drupal
# Thu, 03 Oct 2024 15:27:16 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 03 Oct 2024 15:27:16 GMT
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
	-	`sha256:ed8cbb98fb1f132e7bb5c2d54a8cd266982ddacccf359d9365ed5f51af3b21e3`  
		Last Modified: Fri, 27 Sep 2024 00:24:33 GMT  
		Size: 12.1 MB (12131293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edeb013b74cc0b8a441bb8ca7877ddccd4772dc8117fe778180ecd9431f7b4c1`  
		Last Modified: Fri, 27 Sep 2024 00:24:32 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9d871b9beb0c44ec8df1eb5457e423af34829531e1cfde3201fc8d0679fef8`  
		Last Modified: Fri, 27 Sep 2024 00:24:49 GMT  
		Size: 13.3 MB (13328617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:384d4bdcefd4778942e9925ee1c46c44f10afa9e0d98ea306b67a7c93a5aafe5`  
		Last Modified: Fri, 27 Sep 2024 00:24:47 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4418202cab72c12e2f2f299fc6be846fda32b266c4d114d075bee55c4fc150`  
		Last Modified: Fri, 27 Sep 2024 00:24:47 GMT  
		Size: 19.5 KB (19489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a09eaca06a00a4eeec3001ebd5a3d3ebf1b89a4a9a30a5ec588f0edf695d3996`  
		Last Modified: Fri, 27 Sep 2024 00:24:47 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a656b24cead8c1f78e40a3fd08b8b44212dac48af7211428ad161302dff4f1b`  
		Last Modified: Thu, 03 Oct 2024 18:03:22 GMT  
		Size: 1.6 MB (1595415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f6293140a8ac187f5fec0e996a377bad4c1112f5449962439a4cd13a6778ea`  
		Last Modified: Thu, 03 Oct 2024 18:03:22 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9bcb9a014f835c0bd2b22ed852cc7d7f8639a82a304706974bbb065b915480`  
		Last Modified: Thu, 03 Oct 2024 18:03:23 GMT  
		Size: 738.3 KB (738324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc1604280c89bf79fdb096e27aca3958cf7fd54a051b3f59871c35baf62de50`  
		Last Modified: Thu, 03 Oct 2024 18:03:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dae2237baff594d2c422864be9f30544f100719b1bd08b3436c2d7fd6d75612`  
		Last Modified: Mon, 07 Oct 2024 18:18:41 GMT  
		Size: 21.1 MB (21119193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine` - unknown; unknown

```console
$ docker pull drupal@sha256:239c59ad46748e90bbe002a3844295be2e11b500ffb7de099c38a30d4db3ca39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.6 KB (380565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeae187bc015167652a067848c3a0906f7c0b0ba0a7d4c40aeb81e99f482e334`

```dockerfile
```

-	Layers:
	-	`sha256:4ff848d93cc5292ae1c9c35215bf6b54eb7caeb34bffca2e7f68163139087ec5`  
		Last Modified: Mon, 07 Oct 2024 18:18:40 GMT  
		Size: 346.3 KB (346317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2610b73c5c309e451c4487e012d3dd8fa04d5b2ac319897519b682f34b163540`  
		Last Modified: Mon, 07 Oct 2024 18:18:40 GMT  
		Size: 34.2 KB (34248 bytes)  
		MIME: application/vnd.in-toto+json
