## `drupal:php8.4-fpm-alpine3.22`

```console
$ docker pull drupal@sha256:2fae0011ecc5ad0ec99561e676ba017c7f6d04b7f42ed4d5079a7ff36ed74fec
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

### `drupal:php8.4-fpm-alpine3.22` - linux; amd64

```console
$ docker pull drupal@sha256:a3618314cf6395f64f83f426850ef8a9b37f308c4faf1bd64f451d3a32a24b54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.6 MB (63554781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37deb0d0af89536de911b2f794364576af192e45bd90b7fad0b34e623327e7d4`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Thu, 09 Apr 2026 22:19:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 09 Apr 2026 22:19:18 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 09 Apr 2026 22:19:18 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 09 Apr 2026 22:19:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 09 Apr 2026 22:19:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 09 Apr 2026 22:19:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Apr 2026 22:19:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Apr 2026 22:19:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 09 Apr 2026 22:19:18 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 09 Apr 2026 22:19:18 GMT
ENV PHP_VERSION=8.4.20
# Thu, 09 Apr 2026 22:19:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Thu, 09 Apr 2026 22:19:18 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Thu, 09 Apr 2026 22:19:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 09 Apr 2026 22:19:22 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:22:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 09 Apr 2026 22:22:17 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:22:18 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 09 Apr 2026 22:22:19 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 09 Apr 2026 22:22:19 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 09 Apr 2026 22:22:19 GMT
WORKDIR /var/www/html
# Thu, 09 Apr 2026 22:22:19 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 09 Apr 2026 22:22:19 GMT
STOPSIGNAL SIGQUIT
# Thu, 09 Apr 2026 22:22:19 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 09 Apr 2026 22:22:19 GMT
CMD ["php-fpm"]
# Tue, 14 Apr 2026 18:58:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 14 Apr 2026 18:58:39 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 14 Apr 2026 18:58:39 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 18:58:39 GMT
ENV DRUPAL_VERSION=11.3.6
# Tue, 14 Apr 2026 18:58:39 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Apr 2026 18:58:39 GMT
WORKDIR /opt/drupal
# Tue, 14 Apr 2026 18:58:45 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 14 Apr 2026 18:58:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:472cf5ca97ee75f355bb48975cac34f9c112fd723cf2fce103f0d85ce3d4e4ed`  
		Last Modified: Thu, 09 Apr 2026 22:22:26 GMT  
		Size: 3.5 MB (3464762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66472dcc68b6c5e38411af2ebc0d581e0712101370b5bed4e2cc60368fa445a7`  
		Last Modified: Thu, 09 Apr 2026 22:22:26 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb6e598f73a05a792dbeb96a27f79c0816c25f92e119c61e9ab71d3ffc9fbd9`  
		Last Modified: Thu, 09 Apr 2026 22:22:25 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f222ac1b9326d2085602e5e4a06dd5d8b5a191d116d45011fb08d67db517f3ff`  
		Last Modified: Thu, 09 Apr 2026 22:22:26 GMT  
		Size: 13.7 MB (13707505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13cf6b91079307a1a130859e340f2963f3f46aa91da46aa2548f9c2f63db17a0`  
		Last Modified: Thu, 09 Apr 2026 22:22:27 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d68ea8f1ffe860241985412e54f7a49030b813249c86e707b9fe917588f2bd6`  
		Last Modified: Thu, 09 Apr 2026 22:22:27 GMT  
		Size: 15.5 MB (15475783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45e73735640e37b00331bf03a6988296ba3c12ffd16eac0ef8799f198c45656a`  
		Last Modified: Thu, 09 Apr 2026 22:22:27 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75079574e7c2655f69ae5e912dc86a4cd860fc818b60a5630f8f7c317fa20434`  
		Last Modified: Thu, 09 Apr 2026 22:22:27 GMT  
		Size: 20.1 KB (20112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbab7ab1888f74d6c541b85975192b914dc64d5df680b8bd0ca7177cd7280b7b`  
		Last Modified: Thu, 09 Apr 2026 22:22:28 GMT  
		Size: 20.1 KB (20112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f8705a04a1e7293d01250c1d54704a3bbe270e8b5d04e4db5e785aa6c6ff14`  
		Last Modified: Thu, 09 Apr 2026 22:22:28 GMT  
		Size: 9.3 KB (9263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dbea2decc9fae7841d0997c106aba1b2a3a03f32c02d21364719d0de596045e`  
		Last Modified: Tue, 14 Apr 2026 18:58:57 GMT  
		Size: 4.9 MB (4922876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ac083f66aad3813727faab52a19015ddb8de0d3f90c29afda319ffb32f4946e`  
		Last Modified: Tue, 14 Apr 2026 18:58:57 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a659c833447a298d96c5ac345e4ab66ac40f4dd60f12cdf587457de869d12e35`  
		Last Modified: Tue, 14 Apr 2026 18:58:57 GMT  
		Size: 790.8 KB (790768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6fb5ab7e11dff56fd0ddc910ed36c46e9d5e28a68e2f24723cbb6e46244ef9f`  
		Last Modified: Tue, 14 Apr 2026 18:58:57 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf083aa42c0221410dc6a8919ed2f84dfc0dea1d8d766281349558565ac58550`  
		Last Modified: Tue, 14 Apr 2026 18:58:58 GMT  
		Size: 21.3 MB (21334177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:eba376499757bce308d4d04fca7d2f064af72604e2c57748eca7117049fd3cf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **412.8 KB (412841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a904e7436c6a8271ff7a9d94394dbccb31ea32720f1d809e7ea78fdeac97631`

```dockerfile
```

-	Layers:
	-	`sha256:44340ec300894c938136ff49e2f6c4726c27c795a58ae21faecf1ce535f24a3d`  
		Last Modified: Tue, 14 Apr 2026 18:58:56 GMT  
		Size: 378.3 KB (378341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a52b8b138ad78fee18e1840cef200c75f5b98405476c4d35f1778bbc6379031`  
		Last Modified: Tue, 14 Apr 2026 18:58:56 GMT  
		Size: 34.5 KB (34500 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-fpm-alpine3.22` - linux; arm variant v6

```console
$ docker pull drupal@sha256:e5d1b3ebfaf58a845514aa070bd8a0ba2907c7b3673e8c2ca91851f2a9e47b0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61208767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c181e4c4b3195c043b2267e177a0a509ec6def209e1674e0106b038a89e48a`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Thu, 09 Apr 2026 22:12:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 09 Apr 2026 22:12:16 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 09 Apr 2026 22:12:16 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 09 Apr 2026 22:12:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 09 Apr 2026 22:12:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 09 Apr 2026 22:12:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Apr 2026 22:12:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Apr 2026 22:12:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 09 Apr 2026 22:12:16 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 09 Apr 2026 22:12:16 GMT
ENV PHP_VERSION=8.4.20
# Thu, 09 Apr 2026 22:12:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Thu, 09 Apr 2026 22:12:16 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Thu, 09 Apr 2026 22:19:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 09 Apr 2026 22:19:39 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:22:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 09 Apr 2026 22:22:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:22:39 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 09 Apr 2026 22:22:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 09 Apr 2026 22:22:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 09 Apr 2026 22:22:40 GMT
WORKDIR /var/www/html
# Thu, 09 Apr 2026 22:22:40 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 09 Apr 2026 22:22:40 GMT
STOPSIGNAL SIGQUIT
# Thu, 09 Apr 2026 22:22:40 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 09 Apr 2026 22:22:40 GMT
CMD ["php-fpm"]
# Tue, 14 Apr 2026 18:55:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 14 Apr 2026 18:55:51 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 14 Apr 2026 18:55:51 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 18:55:51 GMT
ENV DRUPAL_VERSION=11.3.6
# Tue, 14 Apr 2026 18:55:51 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Apr 2026 18:55:51 GMT
WORKDIR /opt/drupal
# Tue, 14 Apr 2026 18:56:00 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 14 Apr 2026 18:56:00 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4ea279ecd0622aada20637a59ba54b46230d0656d6e893aeb1ee5cfcac3990`  
		Last Modified: Thu, 09 Apr 2026 22:15:40 GMT  
		Size: 3.4 MB (3428886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d73f80330efb23e6103a6dc569942b96ab7c5d6cd3f68512bdcc759b9bbb7c`  
		Last Modified: Thu, 09 Apr 2026 22:15:39 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c889f4c4f1ceeb5b6f1cee6f8e7b3f641d8f57fdc317672846df9c2c0e9b0810`  
		Last Modified: Thu, 09 Apr 2026 22:15:40 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afbd2d3f4e6173e3a4d2ab781f0e37b28bb08f6a4f4642be6cc84936407f2e39`  
		Last Modified: Thu, 09 Apr 2026 22:22:46 GMT  
		Size: 13.7 MB (13707517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:275f6321704a0313b8adfcbaab11d41ab195235bf83b6b0c9e74b7661bc14cf2`  
		Last Modified: Thu, 09 Apr 2026 22:22:45 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5238e26dd79a7ffd9efd2bf6c25ac976c7f47900a02b5205e455581f7d7c90e2`  
		Last Modified: Thu, 09 Apr 2026 22:22:46 GMT  
		Size: 14.0 MB (13969191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5955db58b33ea2d2f53c009ecd73d087e9cf0d76dd39525abca34c499f63c6`  
		Last Modified: Thu, 09 Apr 2026 22:22:45 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d7dacb23644a241e4cd79881d82fafcd62ddd9f7f03f98b96f3b3e709a0125`  
		Last Modified: Thu, 09 Apr 2026 22:22:46 GMT  
		Size: 19.9 KB (19911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5262baac4c03f905d14a7d2d10a28d6f97ee8cac34e755b18b421c0ec57d0fd`  
		Last Modified: Thu, 09 Apr 2026 22:22:46 GMT  
		Size: 19.9 KB (19906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffafc1a4c8a7be17cc74815283783ef899f5d520d6ce8339e64db9392a0c2761`  
		Last Modified: Thu, 09 Apr 2026 22:22:47 GMT  
		Size: 9.3 KB (9259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a1577301dcdf3cc03d03d5cf48cbaf28e5a064ab5872cf3b20353160ec0d8a`  
		Last Modified: Tue, 14 Apr 2026 18:56:09 GMT  
		Size: 4.4 MB (4419470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e311adb953448de5b7d817fc1820f70c1a7eb710362cd706f4af7ea02fc71c4`  
		Last Modified: Tue, 14 Apr 2026 18:56:08 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baebd63c8ea190f1837ccfe32e86575a8dc971f30f81b95bd1ab44cb5d583b0f`  
		Last Modified: Tue, 14 Apr 2026 18:56:08 GMT  
		Size: 790.8 KB (790766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8947bbddedc6564f075a4337fc1210c8537e37b636b02dcff58e0b906bfa18`  
		Last Modified: Tue, 14 Apr 2026 18:56:08 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17574eafb187e4addacc92f90a2fbedec835a7f3b43ab86a36fdff2f84ec6551`  
		Last Modified: Tue, 14 Apr 2026 18:56:10 GMT  
		Size: 21.3 MB (21334268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:fe1152e0ebd78cd7467796d3caa7adba744cf9d59a6d109cc90fdedfd311ddba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.4 KB (34444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35390dc11a46f1d33a011f78c5ade49152f3f6dcec36d9f29dfc7f9fd2169e9b`

```dockerfile
```

-	Layers:
	-	`sha256:70613f5b491153ad6bd008da065fd2e50dd42326046f894784ffc580a9ef44bd`  
		Last Modified: Tue, 14 Apr 2026 18:56:08 GMT  
		Size: 34.4 KB (34444 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-fpm-alpine3.22` - linux; arm variant v7

```console
$ docker pull drupal@sha256:ac66cdc0e63a62f18d4c6aea5980a57d87804298a600af0d242e0f118cc1e994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59159677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf19c523daeaed71732867db76380d543839530c9d5cfa1caa7eddf620d7963c`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Thu, 09 Apr 2026 22:31:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 09 Apr 2026 22:31:29 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 09 Apr 2026 22:31:29 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 09 Apr 2026 22:31:29 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 09 Apr 2026 22:31:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 09 Apr 2026 22:31:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Apr 2026 22:31:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Apr 2026 22:31:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 09 Apr 2026 22:31:29 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 09 Apr 2026 22:31:29 GMT
ENV PHP_VERSION=8.4.20
# Thu, 09 Apr 2026 22:31:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Thu, 09 Apr 2026 22:31:29 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Thu, 09 Apr 2026 22:31:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 09 Apr 2026 22:31:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:34:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 09 Apr 2026 22:34:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:34:29 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 09 Apr 2026 22:34:30 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 09 Apr 2026 22:34:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 09 Apr 2026 22:34:30 GMT
WORKDIR /var/www/html
# Thu, 09 Apr 2026 22:34:30 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 09 Apr 2026 22:34:30 GMT
STOPSIGNAL SIGQUIT
# Thu, 09 Apr 2026 22:34:30 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 09 Apr 2026 22:34:30 GMT
CMD ["php-fpm"]
# Tue, 14 Apr 2026 18:57:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 14 Apr 2026 18:57:59 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 14 Apr 2026 18:57:59 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 18:57:59 GMT
ENV DRUPAL_VERSION=11.3.6
# Tue, 14 Apr 2026 18:57:59 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Apr 2026 18:57:59 GMT
WORKDIR /opt/drupal
# Tue, 14 Apr 2026 18:58:06 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 14 Apr 2026 18:58:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f393bd3f8ba72e7ef04c7bbada2126b9b88c9aa4cd6eda8c8fc626eaccee9ad`  
		Last Modified: Thu, 09 Apr 2026 22:34:36 GMT  
		Size: 5.2 MB (5197085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b166c64db4cf73ba9760ad6400b7c7fc9ef90c22e5bf102f51fbdcd153a051`  
		Last Modified: Thu, 09 Apr 2026 22:34:36 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8bcc1767f0850613cefbbec51d4556c74d5cdecce63f172611c1224c24bd16a`  
		Last Modified: Thu, 09 Apr 2026 22:34:36 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1d43f0bd3d5a3c43e9f563fe7b95705cac8961cc8c7f8206140b1a98795c10`  
		Last Modified: Thu, 09 Apr 2026 22:34:37 GMT  
		Size: 13.7 MB (13707518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca8a68406f1d1924893a8734e4b426896e5470678533c5784aafe811fbaf8ce2`  
		Last Modified: Thu, 09 Apr 2026 22:34:37 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:116635c68f803ab773bc1c597fcfe040a05cf9855da5d28886a106f4c77dab87`  
		Last Modified: Thu, 09 Apr 2026 22:34:37 GMT  
		Size: 13.2 MB (13181748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4012db9ffd627bbd06bc978a4b7072544255591e190b541dd1bc8131520b37c`  
		Last Modified: Thu, 09 Apr 2026 22:34:38 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ee4156373b72957ea0b4ad9d7c1e0c90c38ee68262cc4474ab672a0947b43c`  
		Last Modified: Thu, 09 Apr 2026 22:34:38 GMT  
		Size: 19.9 KB (19910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5638bedb82ed088173f2c41c369ecd620c2e4302e7072ca77f55d609fb91b7e6`  
		Last Modified: Thu, 09 Apr 2026 22:34:38 GMT  
		Size: 19.9 KB (19905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0812c0fae1879a21b43052cb0c43b68bb71b36fce3dc32fb7e8d1c9728a3f21b`  
		Last Modified: Thu, 09 Apr 2026 22:34:39 GMT  
		Size: 9.3 KB (9264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203cf6cf4b529f545f032840caf6cbe7d448be530b853b7f25890184208c7c76`  
		Last Modified: Tue, 14 Apr 2026 18:58:19 GMT  
		Size: 1.7 MB (1670868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:997cedddb01c1a50592b4824d8913a41e48ea9090725095713a5f560751caa60`  
		Last Modified: Tue, 14 Apr 2026 18:58:19 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8db07ded8d1a06505ccbd93b01514b81e71849703d66448e51dd638b04329f3`  
		Last Modified: Tue, 14 Apr 2026 18:58:19 GMT  
		Size: 790.8 KB (790766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf08c3bb500d808ceb09d12ba098d6f41ed713aec11d644195617989879a195f`  
		Last Modified: Tue, 14 Apr 2026 18:58:19 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:022fcce347a745b915c65c9d1377bfebb2772d4d6f403b5b60d0eb8af7bc2f75`  
		Last Modified: Tue, 14 Apr 2026 18:58:21 GMT  
		Size: 21.3 MB (21334439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:c4fd21741e115daacae4da1d6e20a6af45e0f1a24fb6a036607c1e6471da9617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.1 KB (410079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff021208938d4b6c277c38c722097c0ab4507aeb0f094a9ff8a1cad6ccebb140`

```dockerfile
```

-	Layers:
	-	`sha256:159efa0356c1ffeb2182a48ea55613619b77bd4df2ee438d7fb36c3c40e6caa3`  
		Last Modified: Tue, 14 Apr 2026 18:58:19 GMT  
		Size: 375.4 KB (375419 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5405531f9408b0a57c075e203e9f7662f0455b6c4ee881d41df03e90b496af3`  
		Last Modified: Tue, 14 Apr 2026 18:58:19 GMT  
		Size: 34.7 KB (34660 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-fpm-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:faf17360e89a9c7c45fb6ffd5b72a08047cc2f98a7b325df9dcd2cd75dc72727
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63810791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00d0ac1f01736c84218e11761c11669715cd95e6d192a95932665870202df830`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Thu, 09 Apr 2026 22:20:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 09 Apr 2026 22:20:22 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 09 Apr 2026 22:20:22 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 09 Apr 2026 22:20:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 09 Apr 2026 22:20:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 09 Apr 2026 22:20:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Apr 2026 22:20:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Apr 2026 22:20:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 09 Apr 2026 22:20:22 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 09 Apr 2026 22:20:22 GMT
ENV PHP_VERSION=8.4.20
# Thu, 09 Apr 2026 22:20:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Thu, 09 Apr 2026 22:20:22 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Thu, 09 Apr 2026 22:20:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 09 Apr 2026 22:20:26 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:24:04 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 09 Apr 2026 22:24:04 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:24:04 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 09 Apr 2026 22:24:05 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 09 Apr 2026 22:24:05 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 09 Apr 2026 22:24:05 GMT
WORKDIR /var/www/html
# Thu, 09 Apr 2026 22:24:05 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 09 Apr 2026 22:24:05 GMT
STOPSIGNAL SIGQUIT
# Thu, 09 Apr 2026 22:24:05 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 09 Apr 2026 22:24:05 GMT
CMD ["php-fpm"]
# Tue, 14 Apr 2026 18:59:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 14 Apr 2026 18:59:33 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 14 Apr 2026 18:59:33 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 18:59:33 GMT
ENV DRUPAL_VERSION=11.3.6
# Tue, 14 Apr 2026 18:59:33 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Apr 2026 18:59:33 GMT
WORKDIR /opt/drupal
# Tue, 14 Apr 2026 18:59:40 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 14 Apr 2026 18:59:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931f4d004d98db2d60485268d8f3b6f1bbf8e441baa85017d93c02665b43f856`  
		Last Modified: Thu, 09 Apr 2026 22:24:12 GMT  
		Size: 3.5 MB (3467251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a81c4fb00665092d3a67bbe671cf87e57ab28cb4eefb0ed510ea03b731c8a4`  
		Last Modified: Thu, 09 Apr 2026 22:24:12 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a490e5ec3be83d25c50a5e11c2c6cf22f63350f389e68a4a105f543152a33b`  
		Last Modified: Thu, 09 Apr 2026 22:24:12 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e2af3fa61ecfc4064a5d9e059553a888249887298dc4b969c6ca47acca32780`  
		Last Modified: Thu, 09 Apr 2026 22:24:12 GMT  
		Size: 13.7 MB (13707502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b5161a03e8c57c8011203f5948cd2e0d30408a1458dd565e5f6250d12a8dda7`  
		Last Modified: Thu, 09 Apr 2026 22:24:13 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a6c58d93450c6dd14042be325cee2a4962a323a89d45ba4fd49f5cd6b41651`  
		Last Modified: Thu, 09 Apr 2026 22:24:13 GMT  
		Size: 15.1 MB (15111342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6267f34658668bb4c0036e454c464e68a37126cc511d630a9ec9871c0ccf432`  
		Last Modified: Thu, 09 Apr 2026 22:24:13 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966c90e342da9f395de59eb381dc6d0b13892f2036ab84bc9bfff4f0e76e0948`  
		Last Modified: Thu, 09 Apr 2026 22:24:14 GMT  
		Size: 19.9 KB (19907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d77f6e6ce59f998b2d9791113d82b49d47a3b7f4cf450ac69325bd6f74f0499`  
		Last Modified: Thu, 09 Apr 2026 22:24:14 GMT  
		Size: 19.9 KB (19907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af38b394290683a6acd5072254af2fdd10bb0e33e4d992738ce6e18554df1ce`  
		Last Modified: Thu, 09 Apr 2026 22:24:15 GMT  
		Size: 9.3 KB (9264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4590fc655e2691430f6f3c957b404b1b0ec0a5afb108b859df47083da5731999`  
		Last Modified: Tue, 14 Apr 2026 18:59:53 GMT  
		Size: 5.2 MB (5206220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dab6a96f86dea4344ac231c073a27e4917527ec9b0cf15fa095d8c823b4fef6`  
		Last Modified: Tue, 14 Apr 2026 18:59:53 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a477971cc9023124025495919b1c73cb99027ab8efd2cfc67af1c29e138b21a6`  
		Last Modified: Tue, 14 Apr 2026 18:59:53 GMT  
		Size: 790.8 KB (790764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bab4e327702385c48b176941a4e1fcae174f3b686dd9e220c4df33024de333b`  
		Last Modified: Tue, 14 Apr 2026 18:59:53 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:107c8a642f8a7991e21c31864360e71405c9105e75937d2d1f8654a8016df5cb`  
		Last Modified: Tue, 14 Apr 2026 18:59:55 GMT  
		Size: 21.3 MB (21334571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:eff1e9025ad4a52875de1d600a385292b4657d49770b8fb7e49f9eb97c6f0c65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.2 KB (410163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:419a737097d6bca7ce8510a1cd262f87fb6ce19503715cab78c632ac485b716b`

```dockerfile
```

-	Layers:
	-	`sha256:e37a30dd31d60bd3686cf60f09ebf5cf8967a472197fe4d720877d964650eee5`  
		Last Modified: Tue, 14 Apr 2026 18:59:53 GMT  
		Size: 375.5 KB (375455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65b25bf5e296121b7e3e0f981f0063a3029048322328a57860292d0fa5b4f9a8`  
		Last Modified: Tue, 14 Apr 2026 18:59:53 GMT  
		Size: 34.7 KB (34708 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-fpm-alpine3.22` - linux; 386

```console
$ docker pull drupal@sha256:1f3b29c1c7a92c2d83d5041bb4c58cfaa9e8bbffe68997211c2c228a2c5d5e3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63244575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0531d99bf74368035307ee461a649bfbe7fd7f5e8ae23ba0393abb8c3c4e49c`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:53 GMT
ADD alpine-minirootfs-3.22.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:53 GMT
CMD ["/bin/sh"]
# Fri, 10 Apr 2026 00:20:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 10 Apr 2026 00:20:56 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 10 Apr 2026 00:20:56 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 10 Apr 2026 00:20:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 10 Apr 2026 00:20:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 10 Apr 2026 00:20:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 10 Apr 2026 00:20:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 10 Apr 2026 00:20:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 10 Apr 2026 00:20:56 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 10 Apr 2026 00:20:56 GMT
ENV PHP_VERSION=8.4.20
# Fri, 10 Apr 2026 00:20:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Fri, 10 Apr 2026 00:20:56 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Fri, 10 Apr 2026 00:21:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 10 Apr 2026 00:21:01 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 00:24:16 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 10 Apr 2026 00:24:16 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 00:24:17 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 10 Apr 2026 00:24:18 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 10 Apr 2026 00:24:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 10 Apr 2026 00:24:18 GMT
WORKDIR /var/www/html
# Fri, 10 Apr 2026 00:24:18 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 10 Apr 2026 00:24:18 GMT
STOPSIGNAL SIGQUIT
# Fri, 10 Apr 2026 00:24:18 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 10 Apr 2026 00:24:18 GMT
CMD ["php-fpm"]
# Tue, 14 Apr 2026 18:57:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 14 Apr 2026 18:57:07 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 14 Apr 2026 18:57:07 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 18:57:07 GMT
ENV DRUPAL_VERSION=11.3.6
# Tue, 14 Apr 2026 18:57:07 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Apr 2026 18:57:07 GMT
WORKDIR /opt/drupal
# Tue, 14 Apr 2026 18:57:13 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 14 Apr 2026 18:57:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:757a99eda61f22434071cfbc7a70f9526b63aeb5479a64272982017ee7cd9cfd`  
		Last Modified: Wed, 28 Jan 2026 01:18:59 GMT  
		Size: 3.6 MB (3620732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954b0df7f78d81c0899e129e67a55b792ae63a3ed950331098028b7dd9ef481f`  
		Last Modified: Fri, 10 Apr 2026 00:24:26 GMT  
		Size: 5.8 MB (5807148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f767e40180f52a8e1cca5fcb1d20fd867a24e722a09b4cca10a5b7fe2d2cc86`  
		Last Modified: Fri, 10 Apr 2026 00:24:25 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c4703ed0c9c8a3c51706e8b4a28803202daa2e8357851263f8f45bf7567979`  
		Last Modified: Fri, 10 Apr 2026 00:24:25 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1bf6f2c2e26bbf7b348ebdd36c833f4c6145bd7d8eacc0ab27e88bffc8bb0e4`  
		Last Modified: Fri, 10 Apr 2026 00:24:26 GMT  
		Size: 13.7 MB (13707495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14228cf001547dfb68739a1844f414a7bcdb83531aab5d089c5068d1db4f917a`  
		Last Modified: Fri, 10 Apr 2026 00:24:26 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7276392de2bdb3957871a41094185b88575f4b77a68c2d25ce40e854d6dc0313`  
		Last Modified: Fri, 10 Apr 2026 00:24:27 GMT  
		Size: 15.9 MB (15876397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b09f7293aab1bf6afe65b2af7f5b85a0ad30f6d3db2d4cd7c4ff038ba72a4749`  
		Last Modified: Fri, 10 Apr 2026 00:24:27 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52bd735542fe2233c2bbd6698acaf7b45df842418b6e57ae9f365993b4ab288f`  
		Last Modified: Fri, 10 Apr 2026 00:24:27 GMT  
		Size: 20.1 KB (20094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a2476df8038bef366250ce90f6b7b58311b9b3dcdf1d032f4a574ee3fa10a9`  
		Last Modified: Fri, 10 Apr 2026 00:24:28 GMT  
		Size: 20.1 KB (20096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb98ac7534f9de8fd7a9a8f2458f8ffda4a0509930561f15132a351b3a973c1c`  
		Last Modified: Fri, 10 Apr 2026 00:24:28 GMT  
		Size: 9.3 KB (9266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0eec2e269f3e61967be9a8a8e51d5e2651f06c382d6e5b3284c0155b3129213`  
		Last Modified: Tue, 14 Apr 2026 18:57:25 GMT  
		Size: 2.1 MB (2053509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f412699aed61a3ba41a4779915d8151787e1d20596e28e6b4405e61292a3c925`  
		Last Modified: Tue, 14 Apr 2026 18:57:25 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa0701d8bc49fadbe604e69aa5ad3d0a3ae6d6ca2f88670ac2c3772c77e88f9`  
		Last Modified: Tue, 14 Apr 2026 18:57:25 GMT  
		Size: 790.8 KB (790764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:879aeaac97b840bc46d85afc4f9aa8a1494c52c2a583bc4436d18081d45aeecd`  
		Last Modified: Tue, 14 Apr 2026 18:57:25 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0da615aabec0432caf4d10454f5b573e1a1a6b6f230cd19dce97e49e8a30069`  
		Last Modified: Tue, 14 Apr 2026 18:57:27 GMT  
		Size: 21.3 MB (21334527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:68440e6081c55eb409107e543732e8c2c4a550eabb2872167d551694b6663482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **412.7 KB (412733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2db02f10d51ab05a88b2fe3243feb1b569e047c51c0b71982ac639d21b86b6e`

```dockerfile
```

-	Layers:
	-	`sha256:ca9c73e24dc65eb300ee4102bfb3b2a0be699dc12f7dcb315ef8f5cba52cdf69`  
		Last Modified: Tue, 14 Apr 2026 18:57:25 GMT  
		Size: 378.3 KB (378296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7246e87cdddd394fb13035a76eabdcfdde791c166f2e0993e1915f0b10fd582b`  
		Last Modified: Tue, 14 Apr 2026 18:57:25 GMT  
		Size: 34.4 KB (34437 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-fpm-alpine3.22` - linux; ppc64le

```console
$ docker pull drupal@sha256:07164f2bb260e084af0520529c894640d1cc07f7e7b39c28f4d6eaef76477323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.1 MB (63136203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccca8522a634c8d789d245b740eb47b5b1725e93432cf329dac66bbc0fe1a64e`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Thu, 09 Apr 2026 22:40:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 09 Apr 2026 22:40:00 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 09 Apr 2026 22:40:01 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 09 Apr 2026 22:40:01 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 09 Apr 2026 22:40:01 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 09 Apr 2026 22:40:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Apr 2026 22:40:01 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Apr 2026 22:40:01 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 09 Apr 2026 22:40:01 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 09 Apr 2026 22:40:01 GMT
ENV PHP_VERSION=8.4.20
# Thu, 09 Apr 2026 22:40:01 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Thu, 09 Apr 2026 22:40:01 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Thu, 09 Apr 2026 23:16:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 09 Apr 2026 23:16:46 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 23:22:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 09 Apr 2026 23:22:56 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 23:22:58 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 09 Apr 2026 23:22:59 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 09 Apr 2026 23:22:59 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 09 Apr 2026 23:23:00 GMT
WORKDIR /var/www/html
# Thu, 09 Apr 2026 23:23:01 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 09 Apr 2026 23:23:01 GMT
STOPSIGNAL SIGQUIT
# Thu, 09 Apr 2026 23:23:01 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 09 Apr 2026 23:23:01 GMT
CMD ["php-fpm"]
# Fri, 10 Apr 2026 01:23:42 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 10 Apr 2026 01:23:42 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 14 Apr 2026 19:00:48 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:00:48 GMT
ENV DRUPAL_VERSION=11.3.6
# Tue, 14 Apr 2026 19:00:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Apr 2026 19:00:48 GMT
WORKDIR /opt/drupal
# Tue, 14 Apr 2026 19:01:07 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 14 Apr 2026 19:01:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f75f0d68fec15e86a66bb1163cc325a06b9f5675b56ea20c405cce5e7adb7a`  
		Last Modified: Thu, 09 Apr 2026 22:45:10 GMT  
		Size: 5.9 MB (5945783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f7eb72ca6c1423ccd1a389d0bbdcacbefca48fa8957dce2abc28e75dd020a9c`  
		Last Modified: Thu, 09 Apr 2026 22:45:10 GMT  
		Size: 937.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2109b462465754c71efb3d3c36c4659284495e4e79c59797b775c9caa59c469c`  
		Last Modified: Thu, 09 Apr 2026 22:45:10 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2f9ea0b96017fbf9d5d23b0cf032e0d919b67b4d66bfcb054735a5d8b5e212`  
		Last Modified: Thu, 09 Apr 2026 23:21:21 GMT  
		Size: 13.7 MB (13707526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0122075701f2a404afe78d3ec55d777b227a3e5a17f5148b6c45ee5e1022cbf8`  
		Last Modified: Thu, 09 Apr 2026 23:21:21 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7b1e2a1c4b70bde70b0b2ee3ce62b782756bd51f8a5e4c08e8d03285c3e1a1`  
		Last Modified: Thu, 09 Apr 2026 23:23:16 GMT  
		Size: 16.0 MB (15954421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a85b3ec124297c5a95d57fdc0fc81393bc8404df2a3ceab658b57c065650bb3`  
		Last Modified: Thu, 09 Apr 2026 23:23:16 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d68f94a7f9b0b157a6939739a435ced1bbdded6d814516cee5bd199cd22f4e9`  
		Last Modified: Thu, 09 Apr 2026 23:23:16 GMT  
		Size: 19.9 KB (19921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b6540918c2725f209e1b325532aab5ec7fa43c491487a7c1a6f1063e15ad02`  
		Last Modified: Thu, 09 Apr 2026 23:23:16 GMT  
		Size: 19.9 KB (19915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970b06da75760fc654a69beab7b514c416e048737a6890c073baff33d12c33dc`  
		Last Modified: Thu, 09 Apr 2026 23:23:17 GMT  
		Size: 9.3 KB (9265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31bc5543ef97358188dde26419ac4b1ada33aefe26ce19dac22060141769fa30`  
		Last Modified: Fri, 10 Apr 2026 01:24:27 GMT  
		Size: 1.6 MB (1615857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1edd257c1cc441da9c5f926de81c325ef0b3384fad8b3ff3c6bfc2ad4d8dd81`  
		Last Modified: Fri, 10 Apr 2026 01:24:27 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1991c733eb4bc2b1ff6aaad4d6a496e49fcb35668b32c68e5e6baaa3c27b56f`  
		Last Modified: Tue, 14 Apr 2026 19:01:39 GMT  
		Size: 790.8 KB (790772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd377cc0b9edb9d505613c4c6362031481888ce28114c2ca8bfbb89a24741657`  
		Last Modified: Tue, 14 Apr 2026 19:01:05 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dfea02b4dbfe985fb3ee650686c0008fb2679424358992cd667f3a44b285204`  
		Last Modified: Tue, 14 Apr 2026 19:01:40 GMT  
		Size: 21.3 MB (21333882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:d30fc32069aa7a508bd09b1663b5644a7dd27d24450a4a3288c4804905a36daa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **408.0 KB (408039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26759f357bc58437f2b01034f403f712e1065e266f91685a81ee1d67b454dcb5`

```dockerfile
```

-	Layers:
	-	`sha256:de0d07851259447d80a7e6b2b3df4a3eaef060e80b8fbdf6a11c98e864f93ae9`  
		Last Modified: Tue, 14 Apr 2026 19:01:39 GMT  
		Size: 373.5 KB (373458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:241fdcbe0cef6ae6575ada56da819af037aa073d53a6fb31fb0625fca9d0c203`  
		Last Modified: Tue, 14 Apr 2026 19:01:39 GMT  
		Size: 34.6 KB (34581 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-fpm-alpine3.22` - linux; riscv64

```console
$ docker pull drupal@sha256:3b2dbf0746a2654262ba3ecca37743bb14ae0b5e8f99d87a7fdb1930e6c19a37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58868924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b22bded78a8d16acd46cbf7025ab9e4d6a2a30091c77f035a19fe8d2bf5d684f`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 28 Jan 2026 03:49:43 GMT
ADD alpine-minirootfs-3.22.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:49:43 GMT
CMD ["/bin/sh"]
# Fri, 27 Mar 2026 02:06:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 27 Mar 2026 02:06:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 27 Mar 2026 02:06:33 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 27 Mar 2026 02:06:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 27 Mar 2026 02:06:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 27 Mar 2026 02:06:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Mar 2026 02:06:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Mar 2026 02:06:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 27 Mar 2026 02:06:33 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 27 Mar 2026 02:06:33 GMT
ENV PHP_VERSION=8.4.20
# Fri, 27 Mar 2026 02:06:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Fri, 27 Mar 2026 02:06:33 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Fri, 10 Apr 2026 22:00:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 10 Apr 2026 22:00:07 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 23:56:18 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 10 Apr 2026 23:56:19 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 23:56:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 10 Apr 2026 23:56:30 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 10 Apr 2026 23:56:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 10 Apr 2026 23:56:30 GMT
WORKDIR /var/www/html
# Fri, 10 Apr 2026 23:56:30 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 10 Apr 2026 23:56:30 GMT
STOPSIGNAL SIGQUIT
# Fri, 10 Apr 2026 23:56:30 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 10 Apr 2026 23:56:30 GMT
CMD ["php-fpm"]
# Mon, 13 Apr 2026 00:29:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 13 Apr 2026 00:29:46 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 14 Apr 2026 19:35:54 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:35:54 GMT
ENV DRUPAL_VERSION=11.3.6
# Tue, 14 Apr 2026 19:35:54 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Apr 2026 19:35:54 GMT
WORKDIR /opt/drupal
# Tue, 14 Apr 2026 19:36:37 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 14 Apr 2026 19:36:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:15ea87d2370d91334d14e1cb46366adb6a57bbae717f07f8c9f55735cf137f62`  
		Last Modified: Wed, 28 Jan 2026 03:50:15 GMT  
		Size: 3.5 MB (3517422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdfcec5e28255dc0e86ab83e16a74b5c1c525134a3732aee9e431f8cc84bce27`  
		Last Modified: Fri, 27 Mar 2026 14:21:20 GMT  
		Size: 3.6 MB (3600619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0570e48bf7a46da44ec0d6ff793a75c8aba195204deaed906886b9c3172e561d`  
		Last Modified: Fri, 27 Mar 2026 14:21:19 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:453a134d0a16baab5e83185028e3a86fe467859436a2b79af399201c18fdf43c`  
		Last Modified: Fri, 27 Mar 2026 14:21:19 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6b7cf352b97fb84db7ca5b713f985cfd204e4becc1bc8f9c165c6e5ac0e274`  
		Last Modified: Fri, 10 Apr 2026 22:58:42 GMT  
		Size: 13.7 MB (13707498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649a9e468e04f5fcf932aab246f649344b6f1258e1f018a781b7bbe18b3ff15b`  
		Last Modified: Fri, 10 Apr 2026 22:58:23 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:498f339d707f1b77608ac3121500ceed7a8a3c3f8e4891019a7b2d04b3f0156a`  
		Last Modified: Fri, 10 Apr 2026 23:57:23 GMT  
		Size: 14.4 MB (14448743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ebe7b2f076ba147038c760de026260b28ec58247dfb163a3ffba1d1e0e00cd`  
		Last Modified: Fri, 10 Apr 2026 23:57:21 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19626d1f771abf697116b3212ef52278a2003ca85f12aa7a24c1a0f2a16daf58`  
		Last Modified: Fri, 10 Apr 2026 23:57:21 GMT  
		Size: 19.9 KB (19864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cacf30b1b24da54f22f01f173911a88f11cd9d200a4cd199e71a76b27749d1e`  
		Last Modified: Fri, 10 Apr 2026 23:57:21 GMT  
		Size: 19.9 KB (19867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2821816d5ea7af43623eb476a5432ec69ca462670a7a34b4a7baeff50552230b`  
		Last Modified: Fri, 10 Apr 2026 23:57:23 GMT  
		Size: 9.3 KB (9264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fbbb12a0a1ce8a31b425cc0283e66c39fa5f24d60cbba716bf18eb03f15e01`  
		Last Modified: Mon, 13 Apr 2026 00:32:58 GMT  
		Size: 1.4 MB (1414894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8423c4a7404d3e386b9896b0d498523eacb1dedbfb64289dca0575b1dbc19a2`  
		Last Modified: Mon, 13 Apr 2026 00:32:57 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288a7978375ad816f2e6e1f79b52fa941f67a5645bdca63e6662d2e39f4746fc`  
		Last Modified: Tue, 14 Apr 2026 19:39:15 GMT  
		Size: 790.8 KB (790777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f12978d47b000dc9fb5487f1ab7248f5cf0ab0a236bf05d53fc66c06b5c75daf`  
		Last Modified: Tue, 14 Apr 2026 19:39:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cafb76adbee32b53d10445c03ead54bdd3c627c5f5e7d616eebd5d5a448681e`  
		Last Modified: Tue, 14 Apr 2026 19:39:19 GMT  
		Size: 21.3 MB (21335411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:5c38fcb1155e45726612994c3b5badd84dec4dbb40e3119a42712c5282805585
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.0 KB (407013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e80501544f86849b20a7d12f6222cfd2e19f8666c73ec2ad6a9742d7e78829a`

```dockerfile
```

-	Layers:
	-	`sha256:5b7852991da0f0753551ef83e9cddd06778822561c508480d4a4b4ff0f4e65e4`  
		Last Modified: Tue, 14 Apr 2026 19:39:15 GMT  
		Size: 372.4 KB (372431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a31154bbb8047188556fe4b5dc5b0f2e19d21982d88b65c85e57d90901819dc4`  
		Last Modified: Tue, 14 Apr 2026 19:39:14 GMT  
		Size: 34.6 KB (34582 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-fpm-alpine3.22` - linux; s390x

```console
$ docker pull drupal@sha256:aa3117511193b6350172bc9c94ca5dc66f128d27e6f2d71a2bed41518b62fe41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.9 MB (62904984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01d9a95b8468349ae62941d8b1cb7d90dc540d98956786174445706f8e87d956`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Thu, 09 Apr 2026 22:27:35 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 09 Apr 2026 22:27:35 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 09 Apr 2026 22:27:35 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 09 Apr 2026 22:27:35 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 09 Apr 2026 22:27:35 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 09 Apr 2026 22:27:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Apr 2026 22:27:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Apr 2026 22:27:35 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 09 Apr 2026 22:27:35 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 09 Apr 2026 22:27:35 GMT
ENV PHP_VERSION=8.4.20
# Thu, 09 Apr 2026 22:27:35 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Thu, 09 Apr 2026 22:27:35 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Thu, 09 Apr 2026 22:44:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 09 Apr 2026 22:44:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:50:10 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 09 Apr 2026 22:50:10 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:50:11 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 09 Apr 2026 22:50:11 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 09 Apr 2026 22:50:11 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 09 Apr 2026 22:50:12 GMT
WORKDIR /var/www/html
# Thu, 09 Apr 2026 22:50:12 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 09 Apr 2026 22:50:12 GMT
STOPSIGNAL SIGQUIT
# Thu, 09 Apr 2026 22:50:12 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 09 Apr 2026 22:50:12 GMT
CMD ["php-fpm"]
# Thu, 09 Apr 2026 23:36:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 09 Apr 2026 23:36:33 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 14 Apr 2026 18:57:28 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 18:57:28 GMT
ENV DRUPAL_VERSION=11.3.6
# Tue, 14 Apr 2026 18:57:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Apr 2026 18:57:28 GMT
WORKDIR /opt/drupal
# Tue, 14 Apr 2026 18:57:37 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 14 Apr 2026 18:57:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b03f78560b492a6a896fc1de4f8b2a22350e0783e19d18796a0368ece29fe5a9`  
		Last Modified: Thu, 09 Apr 2026 22:33:22 GMT  
		Size: 3.7 MB (3693214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c5c3db78af4ad975f687ea0000215b60b8309556794377c339f416f692db1c`  
		Last Modified: Thu, 09 Apr 2026 22:33:22 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba7da6b53b99bf8fc44dba62cc974863447aca25c57f7278ab7db5bc687338c`  
		Last Modified: Thu, 09 Apr 2026 22:33:22 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd1d6f3817a39bdf24342ef4691ed9edf101729ccfeb470e0d5d3a7a8f22a0b`  
		Last Modified: Thu, 09 Apr 2026 22:50:26 GMT  
		Size: 13.7 MB (13707522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abeadba0343feee1d6c8dc41fe1d2d0d3264dfba74e6874e2f48ce68020507c6`  
		Last Modified: Thu, 09 Apr 2026 22:50:25 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb93606c83ff648acc6e79eed8e67c186c008b3ecf34f3e9cc4ce5f2fb9997c`  
		Last Modified: Thu, 09 Apr 2026 22:50:26 GMT  
		Size: 18.1 MB (18135130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab039dbdc4efef04b9808d2eb64b7a27e00d01db687abc46883500d32679a40`  
		Last Modified: Thu, 09 Apr 2026 22:50:26 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a128d7bd3f2c71dd2bf22e257f707017af9e4ae574e280069350097fa7ead30`  
		Last Modified: Thu, 09 Apr 2026 22:50:27 GMT  
		Size: 19.9 KB (19928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e98957e8d20442e3860f99801382966a3a724db2d0aa76fa649f44ef3b35fdb`  
		Last Modified: Thu, 09 Apr 2026 22:50:26 GMT  
		Size: 19.9 KB (19910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da43f3fc6ba36c43f35ffd4efe4d7254d7eabe6b6da147169adefa9c875bb07`  
		Last Modified: Thu, 09 Apr 2026 22:50:27 GMT  
		Size: 9.3 KB (9265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb862d19366952dc7ffd9654a45c943d3890919b8ffb4995da96815ede8fd9eb`  
		Last Modified: Thu, 09 Apr 2026 23:37:00 GMT  
		Size: 1.5 MB (1540031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8442fb1fa22fcb46e2889cc0e0342f865a248af82ef297bc3f42132db4417a4`  
		Last Modified: Thu, 09 Apr 2026 23:36:59 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4100b822bff361899553eae54e907273db3ca8983ca4cfd4d55c2db01bea2175`  
		Last Modified: Tue, 14 Apr 2026 18:58:00 GMT  
		Size: 790.8 KB (790771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84b9a9ce1c98443c29546be613f9d477a97e6f2a88a0a24e3fd7f61223da558a`  
		Last Modified: Tue, 14 Apr 2026 18:58:00 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86cc33dd65d3025415e61f436a1ad617df88482ba868f132797d20f59107b89`  
		Last Modified: Tue, 14 Apr 2026 18:58:01 GMT  
		Size: 21.3 MB (21334229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:87af6a14fc30be2de9e598a53125c83fe76299a7269cea5cf066bb86829a8719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.9 KB (407901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d7881ea2dfb5d4658b0a29d8e18c2547699a4a847fc4d7eaa3e77403d4a64db`

```dockerfile
```

-	Layers:
	-	`sha256:1a76f5bc90385346becc6e334b1152a3ed9134d69bb301e978d136e20a3553a2`  
		Last Modified: Tue, 14 Apr 2026 18:58:00 GMT  
		Size: 373.4 KB (373400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2df63641cc3c1f7908e1c3e12d606074def1cc5be7ed96b8819edf7ffdefb10`  
		Last Modified: Tue, 14 Apr 2026 18:58:00 GMT  
		Size: 34.5 KB (34501 bytes)  
		MIME: application/vnd.in-toto+json
