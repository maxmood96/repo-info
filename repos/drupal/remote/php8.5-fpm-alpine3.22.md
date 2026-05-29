## `drupal:php8.5-fpm-alpine3.22`

```console
$ docker pull drupal@sha256:d3d3ca3053a5097f0cc636e3d62343a20ffc6836378cd7173ba3b4ea8b4be89b
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

### `drupal:php8.5-fpm-alpine3.22` - linux; amd64

```console
$ docker pull drupal@sha256:d4b5b8cbe5118aed2e07c18b09ce652f18df492733a1884553472ed7bc5bdb71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (62024377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a55250ce61bdceba6f2d1013ebc042002289ce4091acf0bffce6b9c5ea39326f`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 16:45:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 08 May 2026 16:45:24 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 08 May 2026 16:45:25 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 08 May 2026 16:45:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 16:45:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 16:45:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:45:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:45:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 16:45:25 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 08 May 2026 16:45:25 GMT
ENV PHP_VERSION=8.5.6
# Fri, 08 May 2026 16:45:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Fri, 08 May 2026 16:45:25 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Fri, 08 May 2026 16:45:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 08 May 2026 16:45:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:48:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 16:48:34 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:48:34 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 16:48:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 16:48:34 GMT
WORKDIR /var/www/html
# Fri, 08 May 2026 16:48:35 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 08 May 2026 16:48:35 GMT
STOPSIGNAL SIGQUIT
# Fri, 08 May 2026 16:48:35 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 08 May 2026 16:48:35 GMT
CMD ["php-fpm"]
# Thu, 28 May 2026 22:11:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 28 May 2026 22:11:55 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 28 May 2026 22:11:55 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 28 May 2026 22:11:55 GMT
ENV DRUPAL_VERSION=11.3.10
# Thu, 28 May 2026 22:11:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 28 May 2026 22:11:55 GMT
WORKDIR /opt/drupal
# Thu, 28 May 2026 22:12:06 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 28 May 2026 22:12:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6dde758cf171e78102f1b65ad5d77868798aabf9b8b9edb0e4090eb722a9ee3`  
		Last Modified: Fri, 08 May 2026 16:48:43 GMT  
		Size: 3.5 MB (3464931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54514c155beedb9028b799978ebebe6a8264fbdacc3cc68050d95e0e3a3f708f`  
		Last Modified: Fri, 08 May 2026 16:48:42 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7812da1ee4bb9cdfa9301e0d724cc1c49e491864ff61d60107a668bf7d8b0333`  
		Last Modified: Fri, 08 May 2026 16:48:43 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c9bbb4eda04854b786561a3de59488e7ff2cff28304620f7e53bcaa3d6cc1c`  
		Last Modified: Fri, 08 May 2026 16:48:43 GMT  
		Size: 14.4 MB (14414763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786adc4d571ecf89d9ff1f161b7c1ed1509f68edcab485603cc2b27f073f4a17`  
		Last Modified: Fri, 08 May 2026 16:48:44 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e481efb5e367aaa1aa8c28e650c43cc25470a52e7ca7c11ee80dfad505774e4`  
		Last Modified: Fri, 08 May 2026 16:48:46 GMT  
		Size: 16.6 MB (16625056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:352fc0cfb1d0ccf27f86f0d6bfc7bcdb1bc3d72fa3ad885cf4e0bf2253549fa2`  
		Last Modified: Fri, 08 May 2026 16:48:44 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f86add09f08ae52ad6050b06beeeeba57a2595306365bde48817a5fb2a812e`  
		Last Modified: Fri, 08 May 2026 16:48:44 GMT  
		Size: 20.0 KB (20023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dff7a5ba3b640d227a3f7f08a0023e5ca76552e16acd409414ed0c348c4285b`  
		Last Modified: Fri, 08 May 2026 16:48:45 GMT  
		Size: 9.3 KB (9263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f31b897e67b6d9a971cd32d0f64ca6fe2ff7af20f2c341a6eacfb889c8bd43`  
		Last Modified: Thu, 28 May 2026 22:12:17 GMT  
		Size: 1.5 MB (1494081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b1be7b06eafde3ab8b8b2b18439ade4cd433f748b81d040d6c7783c099474e`  
		Last Modified: Thu, 28 May 2026 22:12:17 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4014623d92b8fc7c6e0b0ba8474d80aa7f1b73f91ae45f23caa6fc21e7ece1cd`  
		Last Modified: Thu, 28 May 2026 22:12:17 GMT  
		Size: 822.5 KB (822516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21976425d219d5b878f1b76a9fc6423490a591d46ea2fad508400f91c95f05f`  
		Last Modified: Thu, 28 May 2026 22:12:17 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87bb343ca0468624c768a38b39a33cf86968c1030fc2e26f2910349793ed5c09`  
		Last Modified: Thu, 28 May 2026 22:12:19 GMT  
		Size: 21.4 MB (21361001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:9bf6a3739bdbb4a1983531a771761f20ed2bedb9b9800cddcd4cb07168390023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.4 KB (406400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86b3ba646be10021d96068cb4ab871701e103b1dbd64ae11be44a29c95c20bd9`

```dockerfile
```

-	Layers:
	-	`sha256:89b1b1b65885a09c57e5a04664585a8308e694a200502369ff8b4d8e24604633`  
		Last Modified: Thu, 28 May 2026 22:12:17 GMT  
		Size: 374.1 KB (374128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1eefc1c2ba9f1ebdf893467c960def9ca2b4c22dc37bb608b2e27ff4801efc36`  
		Last Modified: Thu, 28 May 2026 22:12:17 GMT  
		Size: 32.3 KB (32272 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.5-fpm-alpine3.22` - linux; arm variant v6

```console
$ docker pull drupal@sha256:2454cc10ae1ff837ae7d32e517634a42ee2868d4083ec6fa52c1de6f5d901ad0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59444773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0f127edc43972c51a6126bed7f8f698d111f621bf46105a710b40d4eeb2d9d3`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 16:41:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 08 May 2026 16:41:02 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 08 May 2026 16:41:02 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 08 May 2026 16:41:02 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 16:41:02 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 16:41:02 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:41:02 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:41:02 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 16:41:02 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 08 May 2026 16:41:02 GMT
ENV PHP_VERSION=8.5.6
# Fri, 08 May 2026 16:41:02 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Fri, 08 May 2026 16:41:02 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Fri, 08 May 2026 16:41:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 08 May 2026 16:41:06 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:44:16 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 16:44:16 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:44:17 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 16:44:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 16:44:17 GMT
WORKDIR /var/www/html
# Fri, 08 May 2026 16:44:17 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 08 May 2026 16:44:17 GMT
STOPSIGNAL SIGQUIT
# Fri, 08 May 2026 16:44:17 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 08 May 2026 16:44:17 GMT
CMD ["php-fpm"]
# Thu, 28 May 2026 22:14:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 28 May 2026 22:14:30 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 28 May 2026 22:14:30 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 28 May 2026 22:14:30 GMT
ENV DRUPAL_VERSION=11.3.10
# Thu, 28 May 2026 22:14:30 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 28 May 2026 22:14:30 GMT
WORKDIR /opt/drupal
# Thu, 28 May 2026 22:14:39 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 28 May 2026 22:14:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880d47c9a450a8e5dc89174fe9431aad7ac79118bc25d537236f93fbc549a44e`  
		Last Modified: Fri, 08 May 2026 16:44:22 GMT  
		Size: 3.4 MB (3428187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff79f7e826aec26ecc4d20bc2a4ba11068e828fb7c3dcd8c176d660829b0a78b`  
		Last Modified: Fri, 08 May 2026 16:44:22 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f45e6df65fd39f9f947f90cb7942043bd1526fc4645c44221c802a4e377235c`  
		Last Modified: Fri, 08 May 2026 16:44:22 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6d5b171787c6bd80203412de77af871cddb7ca0d480468146bf98720c42885`  
		Last Modified: Fri, 08 May 2026 16:44:23 GMT  
		Size: 14.4 MB (14414813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9407ece582487b3ef80487220791f776f3115d2842def97bb655ede817fc23`  
		Last Modified: Fri, 08 May 2026 16:44:23 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ccb796a45a825a7889c4cb2d98597b07bd74c63025305ec2858ee0024b232f`  
		Last Modified: Fri, 08 May 2026 16:44:24 GMT  
		Size: 14.5 MB (14540591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:020c25600ff7511ab853540454f424ce943c0fd0c070085fe173ea76dcbd71b7`  
		Last Modified: Fri, 08 May 2026 16:44:24 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f8c62cf6374a4b41b7b3be86a9bbf8eeb5f82e0d273540c2985d6b45ddce08`  
		Last Modified: Fri, 08 May 2026 16:44:24 GMT  
		Size: 19.8 KB (19836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da5538ea4da18760518daa4d410d3b2eb65487a22f4da0e723a3b1c89e50dc33`  
		Last Modified: Fri, 08 May 2026 16:44:25 GMT  
		Size: 9.3 KB (9262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df8f90c5763872981183923950756f163068e6a418b790c610cd9fda234040df`  
		Last Modified: Thu, 28 May 2026 22:14:47 GMT  
		Size: 1.3 MB (1336574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa10821b5a64d7efd6381f87e10ba74cd80e7835a5c65693edd2bb2e619112db`  
		Last Modified: Thu, 28 May 2026 22:14:47 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29dec4ee495abc642fbac3dd613ed0f06e3d3c2887b297f8ae70a5f731e4946f`  
		Last Modified: Thu, 28 May 2026 22:14:47 GMT  
		Size: 822.5 KB (822513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:449aa976eb9bbc458d3d23d7535b4d52dd7191c24d38d66c3474838565ce6bd0`  
		Last Modified: Thu, 28 May 2026 22:14:47 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8869b805ba180be88ffb6af16b09657f9ca61b63962da8462e685e00cc946de2`  
		Last Modified: Thu, 28 May 2026 22:14:49 GMT  
		Size: 21.4 MB (21361065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:7ed891689c945ae1f42a2271acb4251bcb62b556217e21243c5964d4b588b7ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 KB (32185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:935cc626c88f3421b4c25de78530f25222474a2555d15f9981c524440acb7394`

```dockerfile
```

-	Layers:
	-	`sha256:d42f36eca87a49f9b97ccc663113639ed9c11356d9ad933f76d2d7c02b4e6d76`  
		Last Modified: Thu, 28 May 2026 22:14:47 GMT  
		Size: 32.2 KB (32185 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.5-fpm-alpine3.22` - linux; arm variant v7

```console
$ docker pull drupal@sha256:2b2c4bd5eff0c757c9b591776fd6b542c1e5d516074e485f589566866d884666
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.1 MB (58090598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ad909ea2255f10a9ba0f4be28c30ef5728ce877a4423209f0ca614de7ec3bcd`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 16:45:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 08 May 2026 16:45:22 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 08 May 2026 16:45:22 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 08 May 2026 16:45:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 16:45:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 16:45:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:45:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:45:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 16:45:22 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 08 May 2026 16:45:22 GMT
ENV PHP_VERSION=8.5.6
# Fri, 08 May 2026 16:45:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Fri, 08 May 2026 16:45:22 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Fri, 08 May 2026 16:45:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 08 May 2026 16:45:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:48:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 16:48:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:48:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 16:48:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 16:48:40 GMT
WORKDIR /var/www/html
# Fri, 08 May 2026 16:48:41 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 08 May 2026 16:48:41 GMT
STOPSIGNAL SIGQUIT
# Fri, 08 May 2026 16:48:41 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 08 May 2026 16:48:41 GMT
CMD ["php-fpm"]
# Thu, 28 May 2026 22:14:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 28 May 2026 22:14:33 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 28 May 2026 22:14:33 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 28 May 2026 22:14:33 GMT
ENV DRUPAL_VERSION=11.3.10
# Thu, 28 May 2026 22:14:33 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 28 May 2026 22:14:33 GMT
WORKDIR /opt/drupal
# Thu, 28 May 2026 22:14:45 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 28 May 2026 22:14:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b70a811d4ab57277566cd3cfeac5dffdf8047b4376cf0f5e6cce86eaf940a3`  
		Last Modified: Fri, 08 May 2026 16:48:47 GMT  
		Size: 3.2 MB (3244440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa95f79bc8a009a3c088872d6ecad04c212aacf2705d0454687b3a4b13cf270`  
		Last Modified: Fri, 08 May 2026 16:48:47 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:613725503fd0120c628f8a8cf97075bc7e5a6e12aacc234de2a42603517d36d5`  
		Last Modified: Fri, 08 May 2026 16:48:47 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b33a279c8bf31f388cf8a37c4599a0d6d67784ce4a71154aeb455079d59824a`  
		Last Modified: Fri, 08 May 2026 16:48:47 GMT  
		Size: 14.4 MB (14414759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2154160d8ce09da9620560e93d6cf4d0dc6a73cdb26a27727118df97239d591`  
		Last Modified: Fri, 08 May 2026 16:48:48 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e20c79097d5f97e18df76eb698cd5ed4004d49adecc151587bb0c5b637745d1c`  
		Last Modified: Fri, 08 May 2026 16:48:49 GMT  
		Size: 13.8 MB (13753565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ef76fdb433d7c92a2cd9af06827e84cb0bd2256e1481cddd1af24c5459a983`  
		Last Modified: Fri, 08 May 2026 16:48:49 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5a4d7e509f9542a9905fcfd79367148428be843734e31694a18e40ce42a1e5`  
		Last Modified: Fri, 08 May 2026 16:48:49 GMT  
		Size: 19.8 KB (19816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1bbf638768c60f4a3c6765937c08f50ce7cc5f8fc8f37511611b9a8183fe371`  
		Last Modified: Fri, 08 May 2026 16:48:49 GMT  
		Size: 9.3 KB (9262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ac057982820cde5e917ee29489305b888bd9ff2c789017fc27c4b7475c7f98`  
		Last Modified: Thu, 28 May 2026 22:14:59 GMT  
		Size: 1.2 MB (1234873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:035fbcac768589620e9e7ff369ea01321abd9b24bb3206a9d185d34917a0dce5`  
		Last Modified: Thu, 28 May 2026 22:14:59 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94ddc83449946fb0d4f7eeb9d34da4f4b664647b88e89a134222ca3e1846002`  
		Last Modified: Thu, 28 May 2026 22:14:59 GMT  
		Size: 822.5 KB (822516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1e28725d96acfefbb900fc5cbe839cbf01cbc2e871b8166229c3766edd3981`  
		Last Modified: Thu, 28 May 2026 22:14:59 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ea4d7b2e2669436f929fb2112181eb42609d47df6003b9482b1a54c2026102`  
		Last Modified: Thu, 28 May 2026 22:15:00 GMT  
		Size: 21.4 MB (21360992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:e0bff51795b74f1c8a919269ea893faf5329b1d6d72d3b3ad82e1e639a653711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.6 KB (403574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f80e891f1fd2d0fc02a87b0e39704b99b5c261a06fabb56b6089a1e0e99bb828`

```dockerfile
```

-	Layers:
	-	`sha256:7f077398f8f8cdd3a9795126224c380b4854667a6de34f0106495fef65e89534`  
		Last Modified: Thu, 28 May 2026 22:14:59 GMT  
		Size: 371.2 KB (371174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1586698a7c9ac178210725a98d895dbf520bb7118752bdf97a366c398559d9a9`  
		Last Modified: Thu, 28 May 2026 22:14:59 GMT  
		Size: 32.4 KB (32400 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.5-fpm-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:ee0a033eb0cb924ac406504f10ecfa6666a15a34b590c78ec4c38db13d086ef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61879524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:383cf2e778a3e2ae297c249af99a7525950e066f10d74324abee85657af684d8`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 16:43:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 08 May 2026 16:43:25 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 08 May 2026 16:43:25 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 08 May 2026 16:43:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 16:43:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 16:43:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:43:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:43:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 16:43:25 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 08 May 2026 16:43:25 GMT
ENV PHP_VERSION=8.5.6
# Fri, 08 May 2026 16:43:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Fri, 08 May 2026 16:43:25 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Fri, 08 May 2026 16:43:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 08 May 2026 16:43:30 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:47:16 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 16:47:16 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:47:17 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 16:47:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 16:47:17 GMT
WORKDIR /var/www/html
# Fri, 08 May 2026 16:47:17 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 08 May 2026 16:47:17 GMT
STOPSIGNAL SIGQUIT
# Fri, 08 May 2026 16:47:17 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 08 May 2026 16:47:17 GMT
CMD ["php-fpm"]
# Thu, 28 May 2026 22:11:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 28 May 2026 22:11:51 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 28 May 2026 22:11:51 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 28 May 2026 22:11:51 GMT
ENV DRUPAL_VERSION=11.3.10
# Thu, 28 May 2026 22:11:51 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 28 May 2026 22:11:51 GMT
WORKDIR /opt/drupal
# Thu, 28 May 2026 22:12:02 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 28 May 2026 22:12:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d7c2a95ab18725272d3d5eec9590f11ca4361150591d870a6f60614387be59`  
		Last Modified: Fri, 08 May 2026 16:47:25 GMT  
		Size: 3.5 MB (3467735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d57d50f2e370031623ae8734376af6bccd1116bb96221932d46e243ab45a9b`  
		Last Modified: Fri, 08 May 2026 16:47:20 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e1df7cb8893d52a7dea68e4bffdec0530bfd83631f8e38b69f07ed7670c3f2`  
		Last Modified: Fri, 08 May 2026 16:47:25 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8079e81084b57cf7ffcc4f5bbb62dacae9f64b8200adf8a2ad9a2ffd08ca01c7`  
		Last Modified: Fri, 08 May 2026 16:47:25 GMT  
		Size: 14.4 MB (14414756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d91d001fdd21f3dd04eac04d5785159f7e35b726373f601bf95df742a004920`  
		Last Modified: Fri, 08 May 2026 16:47:25 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a0c2335f8b91bd1fe71e8352de2aa55155ec12ed05c298fc6842e85cbf261ad`  
		Last Modified: Fri, 08 May 2026 16:47:27 GMT  
		Size: 16.2 MB (16156295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8100de785e55f4449bddb86b6e8242980faf39ff4b76c947690455fc81ac0c9b`  
		Last Modified: Fri, 08 May 2026 16:47:26 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c009acbf243eddfd07e8442d1f45dfedd1e5a29226ea22438c3879a595ed6eb`  
		Last Modified: Fri, 08 May 2026 16:47:27 GMT  
		Size: 19.8 KB (19827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de240841421e53a0898cbd2f911037f9e564b1d5ca8492e8a9b411a9ea9597b1`  
		Last Modified: Fri, 08 May 2026 16:47:27 GMT  
		Size: 9.3 KB (9260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d197743842fb97e9b6eb0fa463aac10f66a62181ca4071cb95063c1fae7e7662`  
		Last Modified: Thu, 28 May 2026 22:12:15 GMT  
		Size: 1.5 MB (1481658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf3f8f61cae2b4766f91c2eb8d3a9933bba5c195beeb492e1bc1712daa0a72c`  
		Last Modified: Thu, 28 May 2026 22:12:15 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ebd98feafb5ceddc3d84ab8797400204e30c48070466763535cea371d0a62dc`  
		Last Modified: Thu, 28 May 2026 22:12:15 GMT  
		Size: 822.5 KB (822520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd77f0862a000f6110aefac1b31773b6a5738e751e3cef8f1d465d883589c4b2`  
		Last Modified: Thu, 28 May 2026 22:12:15 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf64bf988caa90717aed9b6d5a088d472f6c3e645fac787c1cee42c0a6b9c579`  
		Last Modified: Thu, 28 May 2026 22:12:17 GMT  
		Size: 21.4 MB (21361034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:af7ccc3a272c87d593bbeefed9b2edfb4ec2399c431c3ccb83de0a52ff51fbad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.6 KB (403626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14f3b7c7db1b63b2f3c36be2b03853ebbfbdb319470ee1e6d57dfdcc3dfc9de4`

```dockerfile
```

-	Layers:
	-	`sha256:7f7a2cf265c61b33f2d921573be0a050f1a3b7406e0b358fd932977c87feee5d`  
		Last Modified: Thu, 28 May 2026 22:12:15 GMT  
		Size: 371.2 KB (371194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82a19f1d089c4ad40fc061f311a75ed196ed6e49e49299b6b81b8fb01f064bb7`  
		Last Modified: Thu, 28 May 2026 22:12:15 GMT  
		Size: 32.4 KB (32432 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.5-fpm-alpine3.22` - linux; 386

```console
$ docker pull drupal@sha256:c2a6e718b9cb1d34125cd507218a8495c2efb3ad780668801d5ee5f744601bb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62422286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5724ec5325d16557e9f63564e3e3f760cffb2771ca139312658085ad050efdb9`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 17 Apr 2026 02:42:29 GMT
ADD alpine-minirootfs-3.22.4-x86.tar.gz / # buildkit
# Fri, 17 Apr 2026 02:42:29 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 16:45:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 08 May 2026 16:45:56 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 08 May 2026 16:45:56 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 08 May 2026 16:45:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 16:45:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 16:45:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:45:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:45:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 16:45:56 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 08 May 2026 16:45:56 GMT
ENV PHP_VERSION=8.5.6
# Fri, 08 May 2026 16:45:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Fri, 08 May 2026 16:45:56 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Fri, 08 May 2026 16:46:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 08 May 2026 16:46:01 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:49:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 16:49:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:49:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 16:49:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 16:49:15 GMT
WORKDIR /var/www/html
# Fri, 08 May 2026 16:49:15 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 08 May 2026 16:49:15 GMT
STOPSIGNAL SIGQUIT
# Fri, 08 May 2026 16:49:15 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 08 May 2026 16:49:15 GMT
CMD ["php-fpm"]
# Thu, 28 May 2026 22:12:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 28 May 2026 22:12:01 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 28 May 2026 22:12:02 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 28 May 2026 22:12:02 GMT
ENV DRUPAL_VERSION=11.3.10
# Thu, 28 May 2026 22:12:02 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 28 May 2026 22:12:02 GMT
WORKDIR /opt/drupal
# Thu, 28 May 2026 22:12:12 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 28 May 2026 22:12:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:481dba1f7704181ddc1e2b499675e9651a93f972d4cd141a4933d44622cdc88a`  
		Last Modified: Fri, 17 Apr 2026 02:42:34 GMT  
		Size: 3.6 MB (3624721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1c7def46431a4467d12063fe87f32092bb905e4e2dc3ea4d834b8632f051d12`  
		Last Modified: Fri, 08 May 2026 16:49:22 GMT  
		Size: 3.5 MB (3522642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa2bd98b29faea8c13f8b049fec3bbc5b5ddb54a5c84e713111da25e47571847`  
		Last Modified: Fri, 08 May 2026 16:49:22 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:719c2a173da077d36e4e1ffbe8b0a60cd3e7b896965c50b025095aad753cf562`  
		Last Modified: Fri, 08 May 2026 16:49:22 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32175b397b3f2b31ac1b2f9f77cd751b949e5164a945a21312344a30c38706ad`  
		Last Modified: Fri, 08 May 2026 16:49:22 GMT  
		Size: 14.4 MB (14414765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e43c794bd53cae8874d04a6b8b110c7b22a698bb3af0baac43167b92307724c`  
		Last Modified: Fri, 08 May 2026 16:49:23 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f4288d7d3e4a8e02330e2dfb9e3a08a316a87501cdf8da279e41cac430da05`  
		Last Modified: Fri, 08 May 2026 16:49:24 GMT  
		Size: 17.1 MB (17062449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d19029bb143319e1aa72079504e0c593c476fe70698107c31d3d2331cec96109`  
		Last Modified: Fri, 08 May 2026 16:49:23 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:199efefb82e8e760c0b544bde099b347424621baa1587d01185ed48560f5febe`  
		Last Modified: Fri, 08 May 2026 16:49:24 GMT  
		Size: 20.0 KB (20019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f23657efdddc811a26da91d9f0d3d16e7966ca075221cd4fc4d918f69e8f690`  
		Last Modified: Fri, 08 May 2026 16:49:24 GMT  
		Size: 9.3 KB (9259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f60b50f9aec273c7d7c2375b83b9efd44873a1721e74f7f17f440fd8c622a5ab`  
		Last Modified: Thu, 28 May 2026 22:12:25 GMT  
		Size: 1.6 MB (1580254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ff79f1521268117af73189eff921d71284f009678c96272d7fc9876f01f8fc`  
		Last Modified: Thu, 28 May 2026 22:12:25 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad9b992b1096936389ef736549a70bf5f561be964e410898496eb7283c8d745`  
		Last Modified: Thu, 28 May 2026 22:12:25 GMT  
		Size: 822.5 KB (822514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1796353b0a5858ae6f57d205e4190b640ce59589baa3fb37e4bb07ca77a301f2`  
		Last Modified: Thu, 28 May 2026 22:12:25 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f455b08586aab74929bc0b93471257818c2e19bdc5e48c5a7f215e99de048e2`  
		Last Modified: Thu, 28 May 2026 22:12:27 GMT  
		Size: 21.4 MB (21361120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:3cebab784fe44338f56a646cbf800bc4637c33a893a5c85f8b2df25e172b9376
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.3 KB (406332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ac6bc66d86897e7cd955aa8443fae9b8b1c293a7f4f82e30d4e8f28431ee2d5`

```dockerfile
```

-	Layers:
	-	`sha256:d93e25e3395340c280baa79b33a1c41ef6d12fb442af282b99d4d340e0761032`  
		Last Modified: Thu, 28 May 2026 22:12:25 GMT  
		Size: 374.1 KB (374103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f37904556ca0b40862bac97576eb265cee09216e44391e02e59c084d8ea42bcd`  
		Last Modified: Thu, 28 May 2026 22:12:24 GMT  
		Size: 32.2 KB (32229 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.5-fpm-alpine3.22` - linux; ppc64le

```console
$ docker pull drupal@sha256:d9397441d6b9ac98a6ccc2dcded1f68c7b0f5b07948190c7eb34af1094912872
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62564609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4e4370d1dafe3dab4b3fc0f333d50327b528b007ddc35562de634cee782b4d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:19:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 17 Apr 2026 00:19:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 17 Apr 2026 00:19:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 17 Apr 2026 00:19:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 17 Apr 2026 00:19:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 17 Apr 2026 00:19:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Apr 2026 00:19:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Apr 2026 00:19:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 17 Apr 2026 00:19:29 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 17 Apr 2026 00:19:29 GMT
ENV PHP_VERSION=8.5.6
# Fri, 17 Apr 2026 00:19:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Fri, 17 Apr 2026 00:19:29 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Fri, 08 May 2026 19:54:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 08 May 2026 19:54:25 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 20:02:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 20:02:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 20:02:29 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 20:02:29 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 20:02:30 GMT
WORKDIR /var/www/html
# Fri, 08 May 2026 20:02:30 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 08 May 2026 20:02:30 GMT
STOPSIGNAL SIGQUIT
# Fri, 08 May 2026 20:02:30 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 08 May 2026 20:02:30 GMT
CMD ["php-fpm"]
# Thu, 28 May 2026 22:15:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 28 May 2026 22:15:39 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 28 May 2026 22:15:39 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 28 May 2026 22:15:41 GMT
ENV DRUPAL_VERSION=11.3.10
# Thu, 28 May 2026 22:15:41 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 28 May 2026 22:15:41 GMT
WORKDIR /opt/drupal
# Thu, 28 May 2026 22:15:56 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 28 May 2026 22:15:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b158ada90b6cc8f44737ff5d95bedaf7f63979acc7eb3452859f5d0ace79a5`  
		Last Modified: Fri, 17 Apr 2026 00:25:56 GMT  
		Size: 3.6 MB (3615071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b99d415a1788bb58d298132317074efb0a3a7801f8a3fed0809ed39f6869175`  
		Last Modified: Fri, 17 Apr 2026 00:25:55 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9eb866ab296180559ca8a3add579c6854d381da1068c287f30bf1ddcaa1eaf8`  
		Last Modified: Fri, 17 Apr 2026 00:25:55 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303002683dcb0c061010153ec450a53b518aecadd44b3da584d766c0f3313ba5`  
		Last Modified: Fri, 08 May 2026 19:59:07 GMT  
		Size: 14.4 MB (14414825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1c0e59a80090ec48aad0e2c6ffed2c41e2f690ef00daf1060e9db5f5d26bcd8`  
		Last Modified: Fri, 08 May 2026 19:59:07 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50959a53f625392ab119bdea42e360edc72f18904867abc512460103d2aedf38`  
		Last Modified: Fri, 08 May 2026 20:02:43 GMT  
		Size: 17.0 MB (16965283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a38ed1852e4a2e02ece7faaade46d661621e9eb4002b021fb61b5dee93c63a`  
		Last Modified: Fri, 08 May 2026 20:02:42 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646811af180b70959daf6fbe6a38fec644cf0b26a76048083b1337f295526d6e`  
		Last Modified: Fri, 08 May 2026 20:02:42 GMT  
		Size: 19.8 KB (19841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a1ca8ce9c69793f2b31f8a7f47382e774615a19e49e8adb1103f7effd17743`  
		Last Modified: Fri, 08 May 2026 20:02:43 GMT  
		Size: 9.3 KB (9263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202ed7773d8a2c16546bf519036f83f1802d3b45b6c65b596d68e050bf172579`  
		Last Modified: Thu, 28 May 2026 22:16:34 GMT  
		Size: 1.6 MB (1615494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7d914681e656dc7b089cc039eab1ba1c3aa8285c1ba72f3f705b32b6f836c1`  
		Last Modified: Thu, 28 May 2026 22:16:34 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3c680e39b71eed69ac3f9c4777e416fbb282580e2cb89ea5e28e2228a13906`  
		Last Modified: Thu, 28 May 2026 22:16:34 GMT  
		Size: 822.5 KB (822513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5ab07514ea87bf104b0352c4bff49cc8a3ad6cb762557c56cca0ff38cbe247`  
		Last Modified: Thu, 28 May 2026 22:16:34 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011f6a7273c4d60fc68e43110b134ff95940a727532d70386a4d297a8f89e1b1`  
		Last Modified: Thu, 28 May 2026 22:16:36 GMT  
		Size: 21.4 MB (21361111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:e4c3919949d8afd63b63451357e3616a747eb19ad6b487099c78585a32fd4c00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.6 KB (401550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddb2d173188ae4628829adb410f15265e18b96919a5c2c0a011ed78cd0694298`

```dockerfile
```

-	Layers:
	-	`sha256:cda60a552d28e67521adda47119c3334fb5dd50c0133b169cf2df713f1d6bc83`  
		Last Modified: Thu, 28 May 2026 22:16:34 GMT  
		Size: 369.2 KB (369221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2aabc3a56260abae942f6de2b4cf5f804c0cf7b6a28f28e6616cc01698471f2e`  
		Last Modified: Thu, 28 May 2026 22:16:33 GMT  
		Size: 32.3 KB (32329 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.5-fpm-alpine3.22` - linux; riscv64

```console
$ docker pull drupal@sha256:3e552e6de4ca1c179695b7fa19632789527b5b781496c47596dd16e599d69060
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60930573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a50b2ac50fa2e2132bdd41602061f8194bf5ef2e99815cb8e355ec57547ea2a0`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 17 Apr 2026 07:18:45 GMT
ADD alpine-minirootfs-3.22.4-riscv64.tar.gz / # buildkit
# Fri, 17 Apr 2026 07:18:45 GMT
CMD ["/bin/sh"]
# Sat, 18 Apr 2026 11:02:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 18 Apr 2026 11:02:25 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Sat, 18 Apr 2026 11:02:26 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Sat, 18 Apr 2026 11:02:26 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 18 Apr 2026 11:02:26 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 18 Apr 2026 11:02:26 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Apr 2026 11:02:26 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Apr 2026 11:02:26 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 18 Apr 2026 11:02:26 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Sat, 18 Apr 2026 11:02:26 GMT
ENV PHP_VERSION=8.5.6
# Sat, 18 Apr 2026 11:02:26 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Sat, 18 Apr 2026 11:02:26 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Sat, 09 May 2026 00:12:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Sat, 09 May 2026 00:12:12 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 09 May 2026 02:14:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 09 May 2026 02:14:43 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 09 May 2026 02:14:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 09 May 2026 02:14:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 09 May 2026 02:14:49 GMT
WORKDIR /var/www/html
# Sat, 09 May 2026 02:14:49 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 09 May 2026 02:14:49 GMT
STOPSIGNAL SIGQUIT
# Sat, 09 May 2026 02:14:49 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 09 May 2026 02:14:49 GMT
CMD ["php-fpm"]
# Tue, 12 May 2026 01:28:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 12 May 2026 01:28:55 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 28 May 2026 22:48:51 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 28 May 2026 22:48:51 GMT
ENV DRUPAL_VERSION=11.3.10
# Thu, 28 May 2026 22:48:51 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 28 May 2026 22:48:51 GMT
WORKDIR /opt/drupal
# Thu, 28 May 2026 22:49:35 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 28 May 2026 22:49:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:fbc07c8b85a3c60e503ffd0cbe3e1b3947fd65764784e1bd9d943ac21097cce7`  
		Last Modified: Fri, 17 Apr 2026 07:19:08 GMT  
		Size: 3.5 MB (3520880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aba8e387b0f52a066bd16fc16548380bb5c1ba358c87f632f41bf0e1538804c`  
		Last Modified: Sat, 18 Apr 2026 12:03:48 GMT  
		Size: 3.6 MB (3600194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e0aef12c28ba880017fb96a48e3e22f4b4e363ee1be8f9a85075a131d12b72`  
		Last Modified: Sat, 18 Apr 2026 12:03:47 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6a7d02aa931427745ea3ec5ed71cd22b97056886e6224d2e88e3226411519f`  
		Last Modified: Sat, 18 Apr 2026 12:03:47 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dc3a63321ea6b26e03e2ec4fe3b8673c2fdd91fda1cb02144de9e7a5f4d8199`  
		Last Modified: Sat, 09 May 2026 01:12:55 GMT  
		Size: 14.4 MB (14414810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9ce3a0f71dd1a6fed72d290b7abc8f1131fcd2ee155be871bcc68c2ea5b563`  
		Last Modified: Sat, 09 May 2026 01:12:51 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca047b2cb2ce03525d6279144c87b34ca3dbc02ee3b5127c8a66d88d616aaae`  
		Last Modified: Sat, 09 May 2026 02:15:47 GMT  
		Size: 15.8 MB (15761183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f60fa876c53b886e99a10375cc8ce12fcc831852882931aab1bddf850fd94d`  
		Last Modified: Sat, 09 May 2026 02:15:45 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42d6d77d5062cb6060a82401f45cd9a1caf245720ff487dbc3c4359f4768347`  
		Last Modified: Sat, 09 May 2026 02:15:45 GMT  
		Size: 19.8 KB (19832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b858c3d94c3f02de279d0ca43cd3afe8832e1b3a79db1e87b9fcce55322c57`  
		Last Modified: Sat, 09 May 2026 02:15:45 GMT  
		Size: 9.3 KB (9259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34ed1890b6585367d934419535b96da5b0c5ac45130bcde3b4294e72ad0e03e`  
		Last Modified: Tue, 12 May 2026 01:32:06 GMT  
		Size: 1.4 MB (1416260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b48fd2895673d74f52079fc12eb17a8e363b2a3f455dd3e66297b27470537f`  
		Last Modified: Tue, 12 May 2026 01:32:06 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af7d647bec8d2d5e28d43ec7fc10ce8c32e57582b94f990defb844e82a60b1b`  
		Last Modified: Thu, 28 May 2026 22:52:08 GMT  
		Size: 822.5 KB (822528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70974b7142cf0651bbce63e042cb0d6fc674f4e32769926c8ebf2d7e4c495fd5`  
		Last Modified: Thu, 28 May 2026 22:52:08 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08d7fdd6b102c58ba08ddec9ed49a92a750f6cbe286f282627f2ceb6236b65d7`  
		Last Modified: Thu, 28 May 2026 22:52:11 GMT  
		Size: 21.4 MB (21361063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:3ab96b331cf63de418bb6fdb8dab09efc7d4f74811ec275487d3cc1a01456438
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.5 KB (401543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5a814760538f824337c46d68348461331467e52f0bc2a29fe59d3472a18ab40`

```dockerfile
```

-	Layers:
	-	`sha256:08620af1c28f12fb28a569d738c92a61861f860db96677ab6e63e2f4e145ead0`  
		Last Modified: Thu, 28 May 2026 22:52:08 GMT  
		Size: 369.2 KB (369213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61d777dc53558b323f209865ff09ea4b218a49b4bbc1dbed4653145e965a6a37`  
		Last Modified: Thu, 28 May 2026 22:52:07 GMT  
		Size: 32.3 KB (32330 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.5-fpm-alpine3.22` - linux; s390x

```console
$ docker pull drupal@sha256:ead71f979d74fc731a281e686b84f0d4832991f7d80bd0ec8f8f546b54034f6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61529295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84a4c5ca3b434a1bbe96c5dba310bd61107a91321dcd7c66dafc6863538ae65b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Tue, 05 May 2026 23:44:35 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 05 May 2026 23:44:35 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 05 May 2026 23:44:38 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 05 May 2026 23:44:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 05 May 2026 23:44:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 05 May 2026 23:44:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 05 May 2026 23:44:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 05 May 2026 23:44:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 05 May 2026 23:44:41 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 05 May 2026 23:44:41 GMT
ENV PHP_VERSION=8.5.6
# Tue, 05 May 2026 23:44:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Tue, 05 May 2026 23:44:41 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Fri, 08 May 2026 16:52:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 08 May 2026 16:52:02 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 17:02:18 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 17:02:18 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 17:02:19 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 17:02:19 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 17:02:19 GMT
WORKDIR /var/www/html
# Fri, 08 May 2026 17:02:19 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 08 May 2026 17:02:19 GMT
STOPSIGNAL SIGQUIT
# Fri, 08 May 2026 17:02:19 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 08 May 2026 17:02:19 GMT
CMD ["php-fpm"]
# Thu, 28 May 2026 22:11:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 28 May 2026 22:11:55 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 28 May 2026 22:11:55 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 28 May 2026 22:11:55 GMT
ENV DRUPAL_VERSION=11.3.10
# Thu, 28 May 2026 22:11:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 28 May 2026 22:11:55 GMT
WORKDIR /opt/drupal
# Thu, 28 May 2026 22:12:02 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 28 May 2026 22:12:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b6dcb26ae98e73b45a978805e015d44350999a048c41cd7da8044a82ee23859`  
		Last Modified: Tue, 05 May 2026 23:51:33 GMT  
		Size: 3.7 MB (3691328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075db37433ba472b3c2e4660b5096d82017458a133539a149873f17278d3354d`  
		Last Modified: Tue, 05 May 2026 23:51:32 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4752cdd80fe1d3ba27da8dcdcede15c3ea0c6a5a99e47c62ec5e46014d9c331`  
		Last Modified: Tue, 05 May 2026 23:51:32 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d2fa14d53ae0c3fba4968c952a8f670b13f1e301d41f463e269b5e013beba0`  
		Last Modified: Fri, 08 May 2026 16:58:46 GMT  
		Size: 14.4 MB (14414812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11fd9ac8a4f386c32b516df2afac48aa4d40df503090dacb2e035e54066494b2`  
		Last Modified: Fri, 08 May 2026 16:58:43 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ededd3d453f32fec93ef5aa2a00af384a1eced827daf687fb83fc43fb07f1f`  
		Last Modified: Fri, 08 May 2026 17:02:31 GMT  
		Size: 16.0 MB (16011961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8c15f0994cef5e377700c28b04cce17c037b7b7965b6577a9610cc453d6dd2c`  
		Last Modified: Fri, 08 May 2026 17:02:31 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea426bb39cb592352ad2551a84367adf96647ab744266c5830947a5c9052031`  
		Last Modified: Fri, 08 May 2026 17:02:31 GMT  
		Size: 19.8 KB (19829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85222461fbf26fdfb6033b1da2c73c31a93fb800610510ea868db7bb9041dac1`  
		Last Modified: Fri, 08 May 2026 17:02:31 GMT  
		Size: 9.3 KB (9261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01dde177105fe4a3a241cb1fe55c1cb13412c78cd0959035c1abc96125a2487f`  
		Last Modified: Thu, 28 May 2026 22:12:22 GMT  
		Size: 1.5 MB (1540125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093d527687b6e29e9b3d5227ea75f05c654a9c98ee458e225c6b0665ad9dfc21`  
		Last Modified: Thu, 28 May 2026 22:12:22 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:898b68e173b8ebf8efb7fe8916b88fd26f400928668d719700d1d0d4d9490c85`  
		Last Modified: Thu, 28 May 2026 22:12:22 GMT  
		Size: 822.5 KB (822517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21976425d219d5b878f1b76a9fc6423490a591d46ea2fad508400f91c95f05f`  
		Last Modified: Thu, 28 May 2026 22:12:17 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f08ab10d3db340a78473de8c8448d3a796e09348ed6e02f0e3964bb1c188011`  
		Last Modified: Thu, 28 May 2026 22:12:24 GMT  
		Size: 21.4 MB (21361031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:fadb4f3186b17f1251da267daada5d8835fbde858dcad585d548a68c2f128ea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.5 KB (401459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27bb154962113c763a17cc14779f0f873a269a34270c8a5006b4c564a13f55de`

```dockerfile
```

-	Layers:
	-	`sha256:789f4057f410252b19fa0e58a664f17fa86f59aa29cbc770bc7e750370d127d2`  
		Last Modified: Thu, 28 May 2026 22:12:22 GMT  
		Size: 369.2 KB (369187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:670a71b310c6b7e4699dcf4f11b950e4dbf0fe5005f05a97395653bc57596abf`  
		Last Modified: Thu, 28 May 2026 22:12:22 GMT  
		Size: 32.3 KB (32272 bytes)  
		MIME: application/vnd.in-toto+json
