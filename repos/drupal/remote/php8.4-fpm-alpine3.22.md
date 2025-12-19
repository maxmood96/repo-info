## `drupal:php8.4-fpm-alpine3.22`

```console
$ docker pull drupal@sha256:3e6dbfde5814433b28d053b7c0b590369becbde481c5fb995f5d2c120de4c6ec
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
$ docker pull drupal@sha256:e3fcc5e1f7ed1922af17b7c690a4429f523ca8ffcc7ba254210b66d6132915d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59606887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f32400f52900d80092b86c8f17f276a8b1b42b7a02e0e32903ae29f576d4b2`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 19 Dec 2025 01:26:23 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Dec 2025 01:26:23 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Dec 2025 01:26:23 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Dec 2025 01:26:23 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Dec 2025 01:26:23 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Dec 2025 01:26:23 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Dec 2025 01:26:23 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Dec 2025 01:26:23 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Dec 2025 01:26:23 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Dec 2025 01:26:23 GMT
ENV PHP_VERSION=8.4.16
# Fri, 19 Dec 2025 01:26:23 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.16.tar.xz.asc
# Fri, 19 Dec 2025 01:26:23 GMT
ENV PHP_SHA256=f66f8f48db34e9e29f7bfd6901178e9cf4a1b163e6e497716dfcb8f88bcfae30
# Fri, 19 Dec 2025 01:26:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Dec 2025 01:26:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 01:29:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Dec 2025 01:29:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 01:29:23 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Dec 2025 01:29:23 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Dec 2025 01:29:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Dec 2025 01:29:23 GMT
WORKDIR /var/www/html
# Fri, 19 Dec 2025 01:29:23 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 19 Dec 2025 01:29:23 GMT
STOPSIGNAL SIGQUIT
# Fri, 19 Dec 2025 01:29:23 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 19 Dec 2025 01:29:23 GMT
CMD ["php-fpm"]
# Fri, 19 Dec 2025 02:13:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 19 Dec 2025 02:13:41 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 19 Dec 2025 02:13:41 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 02:13:41 GMT
ENV DRUPAL_VERSION=11.3.1
# Fri, 19 Dec 2025 02:13:41 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Dec 2025 02:13:41 GMT
WORKDIR /opt/drupal
# Fri, 19 Dec 2025 02:13:51 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 19 Dec 2025 02:13:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6c849c0691d30261ca7a1393e3e429ff27eb6ba878bf35adaac3888a82bdf47`  
		Last Modified: Fri, 19 Dec 2025 01:29:40 GMT  
		Size: 3.5 MB (3464375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89009065f7c63e900011d47f67be55bf87c3d842f7b6f0344c855c52952b380`  
		Last Modified: Fri, 19 Dec 2025 01:29:39 GMT  
		Size: 937.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95ed98ca36f62b9daf9d3a5ffba8923d3a79755a1ed584beb007cae50a12eb7`  
		Last Modified: Fri, 19 Dec 2025 01:29:39 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f2d3c58e7b52ae176e4b663d524e52b4b8008aab5ffc6c30945e7b3ad312c6`  
		Last Modified: Fri, 19 Dec 2025 01:29:40 GMT  
		Size: 13.7 MB (13682604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cfda37699dbae635bc8ffb85cd698285e1fa7cff548440bfd26415490de1368`  
		Last Modified: Fri, 19 Dec 2025 01:29:39 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ea56647fb3e6fdc08611aff1c228536728598bab4b4b10aeadb72823cb2c73`  
		Last Modified: Fri, 19 Dec 2025 01:29:42 GMT  
		Size: 15.0 MB (15039028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecae164da9af8cb7d9ee14f7d73bb2e46a392176bb57e6c12c4669e31fbcccc6`  
		Last Modified: Fri, 19 Dec 2025 01:29:39 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46be64edc6d8719406b69eca6432b3d4169e0d38e255fcd3b141605e6d4f81af`  
		Last Modified: Fri, 19 Dec 2025 01:29:39 GMT  
		Size: 20.1 KB (20079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435c510b1a3cd30ab0c5024a4a7557cab2fe9d114f90ff713553c337b62d1155`  
		Last Modified: Fri, 19 Dec 2025 01:29:39 GMT  
		Size: 20.1 KB (20071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f159f85f7733b8e4118b4890ac8b98f587dd84e274a8404c54b12741d218eddf`  
		Last Modified: Fri, 19 Dec 2025 01:29:39 GMT  
		Size: 9.2 KB (9190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3bd20c9579e6f465cf1edd2ebf0b4483442d3c672e85abb45f97a87a6efcfd`  
		Last Modified: Fri, 19 Dec 2025 02:14:10 GMT  
		Size: 1.5 MB (1493516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f130a111ce1454f6789e7c959e5f3821b9d35b206725074680d5fbd658b2a7`  
		Last Modified: Fri, 19 Dec 2025 02:14:11 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f49c9b911459f920ba424485cd596ba012a785618f84b5a827e566ec476726`  
		Last Modified: Fri, 19 Dec 2025 02:14:12 GMT  
		Size: 778.0 KB (777990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eb35141238cfcccd40a7c4c27b019d786fae1a621910e804b0fbae21bf7c58c`  
		Last Modified: Fri, 19 Dec 2025 02:14:11 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f281bf3e679fdcae59c1a7c1ffba9b543d54d14e1d6a5953f339ffbe977bd14`  
		Last Modified: Fri, 19 Dec 2025 02:14:13 GMT  
		Size: 21.3 MB (21293034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:c263030141c6555eb9bf7b6e58ae24af69be6d9d0ac756234b539cab723f2b6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.8 KB (411818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11760db1651ffd0811bcba4991237dad960b67ad5cc53c302458c579d1457647`

```dockerfile
```

-	Layers:
	-	`sha256:9b3ad1ed4b8dc520def97272065b131f445311facfa887d878e5102c2a1d1634`  
		Last Modified: Fri, 19 Dec 2025 06:07:10 GMT  
		Size: 377.3 KB (377318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cab5e382bf27474f7f5da7211b7b5a6bad97fa41dc0faf7bff2a0b12135d7a76`  
		Last Modified: Fri, 19 Dec 2025 06:07:10 GMT  
		Size: 34.5 KB (34500 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-fpm-alpine3.22` - linux; arm variant v6

```console
$ docker pull drupal@sha256:87d472addf1744abad890521e81a1236d499f8cf3657da431dd39c82a17fc5b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.6 MB (57618347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e238274652f77d52a382a2377c987bff50d90e03a914f029bd96dd8717bee3`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 19 Dec 2025 01:29:57 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Dec 2025 01:29:57 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Dec 2025 01:29:57 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Dec 2025 01:29:57 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Dec 2025 01:29:57 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Dec 2025 01:29:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Dec 2025 01:29:57 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Dec 2025 01:29:57 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Dec 2025 01:29:57 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Dec 2025 01:29:57 GMT
ENV PHP_VERSION=8.4.16
# Fri, 19 Dec 2025 01:29:57 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.16.tar.xz.asc
# Fri, 19 Dec 2025 01:29:57 GMT
ENV PHP_SHA256=f66f8f48db34e9e29f7bfd6901178e9cf4a1b163e6e497716dfcb8f88bcfae30
# Fri, 19 Dec 2025 01:30:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Dec 2025 01:30:01 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 01:33:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Dec 2025 01:33:03 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 01:33:04 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Dec 2025 01:33:05 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Dec 2025 01:33:05 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Dec 2025 01:33:05 GMT
WORKDIR /var/www/html
# Fri, 19 Dec 2025 01:33:05 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 19 Dec 2025 01:33:05 GMT
STOPSIGNAL SIGQUIT
# Fri, 19 Dec 2025 01:33:05 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 19 Dec 2025 01:33:05 GMT
CMD ["php-fpm"]
# Fri, 19 Dec 2025 02:18:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 19 Dec 2025 02:18:01 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 19 Dec 2025 02:18:01 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 02:18:01 GMT
ENV DRUPAL_VERSION=11.3.1
# Fri, 19 Dec 2025 02:18:01 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Dec 2025 02:18:01 GMT
WORKDIR /opt/drupal
# Fri, 19 Dec 2025 02:18:12 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 19 Dec 2025 02:18:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Sun, 07 Dec 2025 22:05:32 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f3c1005c8f7f5d638b208f42d96c40b1e45b2121e319bcdd86bd40861d8567`  
		Last Modified: Fri, 19 Dec 2025 01:33:20 GMT  
		Size: 3.4 MB (3428658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:919f9af37fa8d2d8d747590f269c48304b26265720761196e4a072a5ef2a6194`  
		Last Modified: Fri, 19 Dec 2025 01:33:20 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec12349e3c415f6dbf7f73427eb7aeaa70b8f5aa2cf646a44322aa05736a47c`  
		Last Modified: Fri, 19 Dec 2025 01:33:19 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6dc009bd68148253314c5ed9b689b31699fbbc2ec2612a15b8c0ba0dcfb9367`  
		Last Modified: Fri, 19 Dec 2025 01:33:21 GMT  
		Size: 13.7 MB (13682617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103f61abbc3e817832650728f6e9939174e38a3371f6462f51fc4eca519aafd4`  
		Last Modified: Fri, 19 Dec 2025 01:33:19 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f36d4e0e52eeaa57c8cfc35eccef62e663d76d049f5ebc6ba9bdd4eb469a360`  
		Last Modified: Fri, 19 Dec 2025 01:33:21 GMT  
		Size: 13.5 MB (13542548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a47300f24ba3d1cfe87ed91f70907e26c38177f3e046e1b092036206cfbf28b`  
		Last Modified: Fri, 19 Dec 2025 01:33:19 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d3403528e35d4c201239ab3c5417a31d2cf9ef920aafcdba2e867b1ba8debb7`  
		Last Modified: Fri, 19 Dec 2025 01:33:19 GMT  
		Size: 19.9 KB (19874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc1f890bc1d302bc2bb68534321fa32e3169c8a54be5f66c55ffbbfea6d676d`  
		Last Modified: Fri, 19 Dec 2025 01:33:20 GMT  
		Size: 19.9 KB (19870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47288f0d73edff059f00ee77ded60e43c7f147090a6c4b5e95698e25de2f7ece`  
		Last Modified: Fri, 19 Dec 2025 01:33:20 GMT  
		Size: 9.2 KB (9191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d0a96e9140d0f0adafac1f5ef2cdd562aa5b324189542f5211269417d0bbacb`  
		Last Modified: Fri, 19 Dec 2025 02:18:27 GMT  
		Size: 1.3 MB (1335850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b9d26c752212ae04883a4065914dbc4a18cef8103db3e3899d119bca3df059`  
		Last Modified: Fri, 19 Dec 2025 02:18:27 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9294dac3d93a0e1f583abbf69763188e5917a6534b22b5ffee08cd959a8d9fd`  
		Last Modified: Fri, 19 Dec 2025 02:18:27 GMT  
		Size: 778.0 KB (777997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c0172cf6d6ed6ea2857bae1c3d829c520b37ddc4246399d139178ff83dbc4b`  
		Last Modified: Fri, 19 Dec 2025 02:18:27 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5c007b9a19fce48c53ea1f1f39de1c3d9134aff6d5c71e6cd7f084b02d3816a`  
		Last Modified: Fri, 19 Dec 2025 02:18:29 GMT  
		Size: 21.3 MB (21293120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:8df1c3a72103fd85ef8c3ecf40379511fcb51445c28943520c65c279afbb1014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.4 KB (34445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:832a0403bca80a8ca6dab357158b153f97db9681763c6746f157d58e6a1a2e55`

```dockerfile
```

-	Layers:
	-	`sha256:f8e2e17dcb1785e72ff0d2c3ed7662f558f86f4e84987cb76117c526932edce7`  
		Last Modified: Fri, 19 Dec 2025 03:12:14 GMT  
		Size: 34.4 KB (34445 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-fpm-alpine3.22` - linux; arm variant v7

```console
$ docker pull drupal@sha256:0f7c329db8a770e2519e37f964dfce8802c6d449fe2cfb8e1f867d751518d7fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.3 MB (56293379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c6948a1e58e23ded1b2a9c23379b92c3f3e0342d008781b580c6ad403f877c0`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 19 Dec 2025 01:33:50 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Dec 2025 01:33:50 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Dec 2025 01:33:50 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Dec 2025 01:33:50 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Dec 2025 01:33:51 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Dec 2025 01:33:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Dec 2025 01:33:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Dec 2025 01:33:51 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Dec 2025 01:33:51 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Dec 2025 01:33:51 GMT
ENV PHP_VERSION=8.4.16
# Fri, 19 Dec 2025 01:33:51 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.16.tar.xz.asc
# Fri, 19 Dec 2025 01:33:51 GMT
ENV PHP_SHA256=f66f8f48db34e9e29f7bfd6901178e9cf4a1b163e6e497716dfcb8f88bcfae30
# Fri, 19 Dec 2025 01:33:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Dec 2025 01:33:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 01:36:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Dec 2025 01:36:53 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 01:36:53 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Dec 2025 01:36:54 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Dec 2025 01:36:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Dec 2025 01:36:54 GMT
WORKDIR /var/www/html
# Fri, 19 Dec 2025 01:36:54 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 19 Dec 2025 01:36:54 GMT
STOPSIGNAL SIGQUIT
# Fri, 19 Dec 2025 01:36:54 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 19 Dec 2025 01:36:54 GMT
CMD ["php-fpm"]
# Fri, 19 Dec 2025 02:20:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 19 Dec 2025 02:20:11 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 19 Dec 2025 02:20:11 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 02:20:11 GMT
ENV DRUPAL_VERSION=11.3.1
# Fri, 19 Dec 2025 02:20:11 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Dec 2025 02:20:11 GMT
WORKDIR /opt/drupal
# Fri, 19 Dec 2025 02:20:20 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 19 Dec 2025 02:20:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Sun, 07 Dec 2025 13:57:17 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccef110fd6415d4c03ae7ce085c24d1028c93480d2004144ed8b1ccd5a5ed7ad`  
		Last Modified: Fri, 19 Dec 2025 01:37:10 GMT  
		Size: 3.2 MB (3244488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45baf9091e68283e0adcd947e84ad4f391315d692872afa17b57ba43d5208208`  
		Last Modified: Fri, 19 Dec 2025 01:37:10 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10fc278c464cfe80f715b0d90f5c58533d35b9618261bf3a5e1d29b46f8aa3ca`  
		Last Modified: Fri, 19 Dec 2025 01:37:10 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f8e9d40d2d15959f55f9ae6fa8bb7ff401aa1c7f25e571ed8746d58a225568`  
		Last Modified: Fri, 19 Dec 2025 01:37:11 GMT  
		Size: 13.7 MB (13682604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a822319d23bf2954a279302ef65e3f82ddcb09907c072625a5ca1289b96a77`  
		Last Modified: Fri, 19 Dec 2025 01:37:09 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ac64c21d881d8e59824da6ebfe362c338d455c66f9636645ac82915b720ed1`  
		Last Modified: Fri, 19 Dec 2025 01:37:11 GMT  
		Size: 12.8 MB (12786166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620fcef3c257fef5d76a416786533eb114103f6643db504723a24bdb6aa4146c`  
		Last Modified: Fri, 19 Dec 2025 01:37:09 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5d3809920afaad8f6eca50ac14b12c3a7d080ff3a816f36f05b2bd67c66ba6e`  
		Last Modified: Fri, 19 Dec 2025 01:37:10 GMT  
		Size: 19.9 KB (19859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd9368b3a43f166dd8f979c99a41be6cfd8e29b38e41267d455093553e006c3`  
		Last Modified: Fri, 19 Dec 2025 01:37:10 GMT  
		Size: 19.9 KB (19858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c35af0fbf55302fe241c1d81e940c8cc3264fa35db7251046448c7046bb090d`  
		Last Modified: Fri, 19 Dec 2025 01:37:10 GMT  
		Size: 9.2 KB (9190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fed9825e50bb562e7ab003138804165665e33085609353b4db27a3a38d51e76`  
		Last Modified: Fri, 19 Dec 2025 02:20:41 GMT  
		Size: 1.2 MB (1234012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931d4bab07a9eac3be616ef2780461e1f3f5827b546e1278a0a176e508d09354`  
		Last Modified: Fri, 19 Dec 2025 02:20:40 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02627a09487cd5b0aae7e5c0e333ef8399bf340d7e0858be210905bc69f5bdb0`  
		Last Modified: Fri, 19 Dec 2025 02:20:40 GMT  
		Size: 778.0 KB (777996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6fff998bbe71eb2d8bf661e9fd7967c408200238851090d5f658cce250660f`  
		Last Modified: Fri, 19 Dec 2025 02:20:40 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7403aecb87471fe0eed0e5a46431db94dc0ca6e7799bf307f5d4650e58cf1f97`  
		Last Modified: Fri, 19 Dec 2025 02:20:47 GMT  
		Size: 21.3 MB (21293100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:acea3091545b28e38d08c8ea5119fd8cb5c07130c2406d231f3fc4b3b38c294e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **409.1 KB (409055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:262422ada3ab0593ee3b587fa17a577fc98daa0acb58f1e587ad2e25d014585b`

```dockerfile
```

-	Layers:
	-	`sha256:1d003645a5abe2c84b25dc830a42785f69f08e4fc3b7cb1dfa3b99e83a95f456`  
		Last Modified: Fri, 19 Dec 2025 03:12:16 GMT  
		Size: 374.4 KB (374396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f82357abef9e28e492fa5900d99767c6bb35eaa44e528fc5896c3c4418714a35`  
		Last Modified: Fri, 19 Dec 2025 03:12:17 GMT  
		Size: 34.7 KB (34659 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-fpm-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:4893ff80a89d8b5a7d31abb448b34c78ea9b1ac866fb138b961184e9e7dfdcc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59565558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1d332ca53806f08db6283e617845e28e311142e3c91a1a136cad4a9da9b2a4b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 19 Dec 2025 01:30:07 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Dec 2025 01:30:07 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Dec 2025 01:30:07 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Dec 2025 01:30:07 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Dec 2025 01:30:07 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Dec 2025 01:30:07 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Dec 2025 01:30:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Dec 2025 01:30:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Dec 2025 01:30:07 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Dec 2025 01:30:07 GMT
ENV PHP_VERSION=8.4.16
# Fri, 19 Dec 2025 01:30:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.16.tar.xz.asc
# Fri, 19 Dec 2025 01:30:07 GMT
ENV PHP_SHA256=f66f8f48db34e9e29f7bfd6901178e9cf4a1b163e6e497716dfcb8f88bcfae30
# Fri, 19 Dec 2025 01:30:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Dec 2025 01:30:11 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 01:33:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Dec 2025 01:33:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 01:33:49 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Dec 2025 01:33:50 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Dec 2025 01:33:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Dec 2025 01:33:50 GMT
WORKDIR /var/www/html
# Fri, 19 Dec 2025 01:33:50 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 19 Dec 2025 01:33:50 GMT
STOPSIGNAL SIGQUIT
# Fri, 19 Dec 2025 01:33:50 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 19 Dec 2025 01:33:50 GMT
CMD ["php-fpm"]
# Fri, 19 Dec 2025 02:14:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 19 Dec 2025 02:14:41 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 19 Dec 2025 02:14:41 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 02:14:41 GMT
ENV DRUPAL_VERSION=11.3.1
# Fri, 19 Dec 2025 02:14:41 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Dec 2025 02:14:41 GMT
WORKDIR /opt/drupal
# Fri, 19 Dec 2025 02:14:49 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 19 Dec 2025 02:14:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef0ff7fca305b10c295ecf7da43487d7d552920ac0d01b76fef65b5d4e69a44d`  
		Last Modified: Fri, 19 Dec 2025 01:34:05 GMT  
		Size: 3.5 MB (3467155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:decfd6404fb702ffe56238a2a34e0fec9220e5f9c810833a9ffe0d24510c21a5`  
		Last Modified: Fri, 19 Dec 2025 01:34:04 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4685af4ef1a36898f1f8dfb6dcc2a282d79e4dd6d400d25b6861a69065ec276b`  
		Last Modified: Fri, 19 Dec 2025 01:34:04 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021a642f9e999711e637fc6ebbe9cc1712d7b58a915684c7dc804ac0b9efbe7f`  
		Last Modified: Fri, 19 Dec 2025 01:34:05 GMT  
		Size: 13.7 MB (13682601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee427caa35fec149c452965222a1dfcdaa7727e6e348147fdadbd50ec57c3d4e`  
		Last Modified: Fri, 19 Dec 2025 01:34:04 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8089e6d7f4f81e39d3a118ac6a134c001fb672606162374c1aa074a3cbe9c8a9`  
		Last Modified: Fri, 19 Dec 2025 01:34:05 GMT  
		Size: 14.7 MB (14672122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58c0352a8b11cfedbfe3b7f8d022062a7c49f2e4c424cbebfcf2ec05cec3da9`  
		Last Modified: Fri, 19 Dec 2025 01:34:04 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4856f91d48e57b5c49d9e322ed07e1068dc2404e94e40fc905745917cb71c1f1`  
		Last Modified: Fri, 19 Dec 2025 01:34:04 GMT  
		Size: 19.9 KB (19857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c1db605823f0584888db4e73575458c5af110da38e8de51333ff2334dac4a53`  
		Last Modified: Fri, 19 Dec 2025 01:34:18 GMT  
		Size: 19.9 KB (19856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12de3b84a5696e9a4db17d082abac8adf8f4704a89d217c1f54625e527930d72`  
		Last Modified: Fri, 19 Dec 2025 01:34:04 GMT  
		Size: 9.2 KB (9190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:167c91be8c2870a58102fd9857cb0403b4b16c0e51f08fac8145155a981e00ee`  
		Last Modified: Fri, 19 Dec 2025 02:15:10 GMT  
		Size: 1.5 MB (1480887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc32794112345fd03a68d481d7898ae5223df07e0655c2e4ced68a3cb360665`  
		Last Modified: Fri, 19 Dec 2025 02:15:10 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e1f58d1455e1e0dfca91291dab42c013361f14321783f331cd8da8b22fae271`  
		Last Modified: Fri, 19 Dec 2025 02:15:10 GMT  
		Size: 778.0 KB (777996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e440374bbcbef195e1aa49ec4963d923c9f25bf1a7fecbcc38d24cf1824f0f7f`  
		Last Modified: Fri, 19 Dec 2025 02:15:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56357b99e73f512522010f5992427fa3f41f059a25932a12336086ada657af33`  
		Last Modified: Fri, 19 Dec 2025 02:15:11 GMT  
		Size: 21.3 MB (21293283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:ec0a189bacaa5b2cccc1ee52c0b1fd468a2f1ebba8d8bede58bd57c7e5376d86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **409.1 KB (409140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1289437acba3aeb2fc543f432449f832ef1335e4a95e60d897f3c638dd67c1bb`

```dockerfile
```

-	Layers:
	-	`sha256:904f6a036f6a3853e38e5e24f311f70cf13e3faf1a8e5df5943c5df8d6c2e004`  
		Last Modified: Fri, 19 Dec 2025 03:13:15 GMT  
		Size: 374.4 KB (374432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3a6061a290f478ea8507633260b2585d0038faad1c41988c18bc8f88bc1eafc`  
		Last Modified: Fri, 19 Dec 2025 03:13:15 GMT  
		Size: 34.7 KB (34708 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-fpm-alpine3.22` - linux; 386

```console
$ docker pull drupal@sha256:820386baeedf5a80cdeaa42cd01eb6eb88feccd7cf6b1ce0e8d2d01a0eeaa1de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (59962253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:868ba0c305709ffe2a7a0a8a9f3a4ae5540c925833ee4feb67a5516f746c6403`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 19 Dec 2025 01:30:30 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Dec 2025 01:30:30 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Dec 2025 01:30:30 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Dec 2025 01:30:30 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Dec 2025 01:30:30 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Dec 2025 01:30:30 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Dec 2025 01:30:30 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Dec 2025 01:30:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Dec 2025 01:30:30 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Dec 2025 01:30:30 GMT
ENV PHP_VERSION=8.4.16
# Fri, 19 Dec 2025 01:30:30 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.16.tar.xz.asc
# Fri, 19 Dec 2025 01:30:30 GMT
ENV PHP_SHA256=f66f8f48db34e9e29f7bfd6901178e9cf4a1b163e6e497716dfcb8f88bcfae30
# Fri, 19 Dec 2025 01:30:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Dec 2025 01:30:34 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 01:33:39 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Dec 2025 01:33:39 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 01:33:40 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Dec 2025 01:33:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Dec 2025 01:33:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Dec 2025 01:33:41 GMT
WORKDIR /var/www/html
# Fri, 19 Dec 2025 01:33:41 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 19 Dec 2025 01:33:41 GMT
STOPSIGNAL SIGQUIT
# Fri, 19 Dec 2025 01:33:41 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 19 Dec 2025 01:33:41 GMT
CMD ["php-fpm"]
# Fri, 19 Dec 2025 02:27:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 19 Dec 2025 02:27:09 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 19 Dec 2025 02:27:09 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 02:27:09 GMT
ENV DRUPAL_VERSION=11.3.1
# Fri, 19 Dec 2025 02:27:09 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Dec 2025 02:27:09 GMT
WORKDIR /opt/drupal
# Fri, 19 Dec 2025 02:27:19 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 19 Dec 2025 02:27:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Sun, 07 Dec 2025 14:06:47 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd1c0062a99d555f17139f7fb56fdc3a0d99fbd0cdbacdf2c594d7f74c0505f`  
		Last Modified: Fri, 19 Dec 2025 01:33:56 GMT  
		Size: 3.5 MB (3523240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c351abb41195e73da8c208aa3abf7ac586ffea6d099466a5bec6286de2f11f`  
		Last Modified: Fri, 19 Dec 2025 01:33:55 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:576359e4ebc598df6d65d569872e666752c5e5453f994946a6c821bcc01b4aba`  
		Last Modified: Fri, 19 Dec 2025 01:33:55 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f95e49bcfe1b080687dfd3cacf54547107dbefa6bb04f6cd6db1c9273289869d`  
		Last Modified: Fri, 19 Dec 2025 01:34:00 GMT  
		Size: 13.7 MB (13682580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc7a3421d6bd665dfa3200b051d1387a318b8fe3fa6e1453bce87cc8c0016d4`  
		Last Modified: Fri, 19 Dec 2025 01:33:56 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c59e36d4e689b9bbe23c92554a154611118a695d1a607003bffd61e190b8b7`  
		Last Modified: Fri, 19 Dec 2025 01:33:57 GMT  
		Size: 15.4 MB (15433506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e627e33a59ad3f7b4a8e12d2e1f9ea9d4fc4482925b61596eafc7dc1ca5e932`  
		Last Modified: Fri, 19 Dec 2025 01:33:56 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620b76c4da512e2f8b0579c28d813b5ec0c31e36507936bd1a496023d1a8641f`  
		Last Modified: Fri, 19 Dec 2025 01:33:56 GMT  
		Size: 20.1 KB (20059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe402a92aabd40958a3b1a50042f49523ee3e5641764403dd2e5aa12732a52ea`  
		Last Modified: Fri, 19 Dec 2025 01:33:56 GMT  
		Size: 20.1 KB (20054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c69d8d7504111ec17b56a4a34e798b57a61307aac23a62e63efdf26f0806eba`  
		Last Modified: Fri, 19 Dec 2025 01:33:56 GMT  
		Size: 9.2 KB (9195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9ca3cf4a782fccfcc2bfe65fb780766fd74124f976ada696a64a72ffd04feb7`  
		Last Modified: Fri, 19 Dec 2025 02:27:38 GMT  
		Size: 1.6 MB (1579018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c962ced1e8d3003a098f052b701e72646663378902fd7e410eb80ea68c478378`  
		Last Modified: Fri, 19 Dec 2025 02:27:37 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d50b6f7f2a130f9cd11c9f425a2fd22eb45cef813c92c6b77cf8244f539bc747`  
		Last Modified: Fri, 19 Dec 2025 02:27:38 GMT  
		Size: 778.0 KB (777999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91ccca28e74d48742243670bedebad97c91aa7018f87d217bd4a0fc7766d460`  
		Last Modified: Fri, 19 Dec 2025 02:27:38 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b605222a7a134d798ac9691b9532f18d31139e174214c78e33c1af6781193965`  
		Last Modified: Fri, 19 Dec 2025 02:27:40 GMT  
		Size: 21.3 MB (21293127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:16a521a71519fa745130ac8b07a35eccca459f5d95a4ae1c1d073b548f4fc454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.7 KB (411710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:400b46cf39f1f1f0245ebf837705fb3319315e8193aceacdddbd08ad37fa804d`

```dockerfile
```

-	Layers:
	-	`sha256:6922abd02ae9dbd1bf692a42a1b7135de6d66e475747ad5f16c25838adf70875`  
		Last Modified: Fri, 19 Dec 2025 06:07:19 GMT  
		Size: 377.3 KB (377273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8237dddd683c1fe9cc9262bfb57eccb58d576d126d2c3f4458ddf00b0bcf974`  
		Last Modified: Fri, 19 Dec 2025 06:07:20 GMT  
		Size: 34.4 KB (34437 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-fpm-alpine3.22` - linux; ppc64le

```console
$ docker pull drupal@sha256:f99c60a6701cce316be67c438f3f79f234200ad3d694e77ecdf78320315f70ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60417745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6c52322b005055e9f63c0fdeb6e2d344b008867ac02c4fce4d339b39280fabc`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 09 Oct 2025 00:51:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 09 Oct 2025 00:51:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 09 Oct 2025 00:51:44 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 09 Oct 2025 00:51:44 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 09 Oct 2025 00:51:44 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 09 Oct 2025 00:51:44 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Oct 2025 00:51:44 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Oct 2025 00:51:44 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 09 Oct 2025 00:51:44 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 09 Oct 2025 00:51:44 GMT
ENV PHP_VERSION=8.4.16
# Thu, 09 Oct 2025 00:51:44 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.16.tar.xz.asc
# Thu, 09 Oct 2025 00:51:44 GMT
ENV PHP_SHA256=f66f8f48db34e9e29f7bfd6901178e9cf4a1b163e6e497716dfcb8f88bcfae30
# Fri, 19 Dec 2025 02:13:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Dec 2025 02:13:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 02:20:08 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Dec 2025 02:20:08 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 02:20:09 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Dec 2025 02:20:11 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Dec 2025 02:20:11 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Dec 2025 02:20:12 GMT
WORKDIR /var/www/html
# Fri, 19 Dec 2025 02:20:12 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 19 Dec 2025 02:20:12 GMT
STOPSIGNAL SIGQUIT
# Fri, 19 Dec 2025 02:20:12 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 19 Dec 2025 02:20:12 GMT
CMD ["php-fpm"]
# Fri, 19 Dec 2025 03:18:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 19 Dec 2025 03:18:31 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 19 Dec 2025 03:18:32 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 03:18:32 GMT
ENV DRUPAL_VERSION=11.3.1
# Fri, 19 Dec 2025 03:18:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Dec 2025 03:18:32 GMT
WORKDIR /opt/drupal
# Fri, 19 Dec 2025 03:18:51 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 19 Dec 2025 03:18:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Sun, 07 Dec 2025 14:06:45 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95a0b03903475651b081c7c705a4ab0f68ab5f5bba328735e8dae6e168526c7`  
		Last Modified: Mon, 08 Dec 2025 02:09:34 GMT  
		Size: 3.6 MB (3614664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436cae3ea479232d2bcf67ca55e6705ab3775fa412e53331855937a2a7340b65`  
		Last Modified: Mon, 08 Dec 2025 02:09:34 GMT  
		Size: 937.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1164e359044b0e56f99538c30031735fcef9128820673f06e10663118d04d0e3`  
		Last Modified: Mon, 08 Dec 2025 02:09:34 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a390b71c0b7395c8d70610b4ec9ce49e6a91f10379ac052134add24a9921e50`  
		Last Modified: Fri, 19 Dec 2025 02:17:51 GMT  
		Size: 13.7 MB (13682596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d0e0d3a2cb3f75bcf4714ae877c91708c7b11c7f8f8868aaea4ce90ed4fda9a`  
		Last Modified: Fri, 19 Dec 2025 02:17:54 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ab3c4864eec22be07dc22d938206c5f2e6ba912f983e2efc143eb09ebc80be`  
		Last Modified: Fri, 19 Dec 2025 02:20:35 GMT  
		Size: 15.6 MB (15647793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6516b25197b1ab5bb165812963c4b78605f4d2901a05d47bc8e24a9134d03086`  
		Last Modified: Fri, 19 Dec 2025 02:20:33 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629151646c7f90ce95541b250da6608327b8420103d89680dc5ab1cefc46bae0`  
		Last Modified: Fri, 19 Dec 2025 02:20:33 GMT  
		Size: 19.9 KB (19882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb73a3b65041f5a073ec9b7415511cc165e9ced1a8660d8429a2d86671a92b5`  
		Last Modified: Fri, 19 Dec 2025 02:20:33 GMT  
		Size: 19.9 KB (19879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37b7a29fbb08af075e930bfe45cfd019baf88b3c25a72d9610997e4a965f7ae`  
		Last Modified: Fri, 19 Dec 2025 02:20:33 GMT  
		Size: 9.2 KB (9196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e24d8ba1f0534106c2197dcd84003c7be6b01e9e8c58842c9a644f6f379a8c6`  
		Last Modified: Fri, 19 Dec 2025 03:19:39 GMT  
		Size: 1.6 MB (1615668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b2aa42c8527b917797ec8fb616b5f29611573ebf259d2fa098f28510194b5c`  
		Last Modified: Fri, 19 Dec 2025 03:19:39 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e27ca50a9f9ecf92105e77099429c2047b81af72f548b7f3254ef8a6a1b4f7e`  
		Last Modified: Fri, 19 Dec 2025 03:19:39 GMT  
		Size: 778.0 KB (777995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c666afdd36c8421cbe5d3aa47fb025dd75f4ec0f6a155aa55a6ea0d6bf4c815`  
		Last Modified: Fri, 19 Dec 2025 03:19:39 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdb7a02e91b013058537d41368a2b8b7c233f4a616d81d06eb51f8ec717c422`  
		Last Modified: Fri, 19 Dec 2025 03:19:41 GMT  
		Size: 21.3 MB (21293272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:715e5f140beda4ea2b858c17e95f3a06320b5a827efade299581ac67da00b78c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.0 KB (407017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d9d5fcc2442b0f6eb7cacb28d332d70bf51e43f5bf26c07bbd12d2a785777b7`

```dockerfile
```

-	Layers:
	-	`sha256:f5ad6c2375ee223966c1c4cf6b553f1d05f520831e442ec76ea4853c97cf0ba8`  
		Last Modified: Fri, 19 Dec 2025 06:07:24 GMT  
		Size: 372.4 KB (372435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:317746747a514bbd83f33ed4f2b88c46d7fc26aabd7f7f09947372be2a6d8671`  
		Last Modified: Fri, 19 Dec 2025 06:07:25 GMT  
		Size: 34.6 KB (34582 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-fpm-alpine3.22` - linux; riscv64

```console
$ docker pull drupal@sha256:bb390cb0480fad11df4f682d23fea2261b534f95591abf17baaacceee7045606
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.1 MB (58120269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2edfeac72a564f6832f7380d91922a152cf5ac634bdbff2c2a41f6296e76fdd4`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 09 Oct 2025 05:22:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 09 Oct 2025 05:22:42 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 09 Oct 2025 05:22:42 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 09 Oct 2025 05:22:42 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 09 Oct 2025 05:22:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 09 Oct 2025 05:22:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Oct 2025 05:22:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Oct 2025 05:22:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 09 Oct 2025 05:22:43 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 09 Oct 2025 05:22:43 GMT
ENV PHP_VERSION=8.4.15
# Thu, 09 Oct 2025 05:22:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.15.tar.xz.asc
# Thu, 09 Oct 2025 05:22:43 GMT
ENV PHP_SHA256=a060684f614b8344f9b34c334b6ba8db1177555997edb5b1aceab0a4b807da7e
# Sat, 22 Nov 2025 06:10:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Sat, 22 Nov 2025 06:10:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 22 Nov 2025 08:05:51 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 22 Nov 2025 08:05:51 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 22 Nov 2025 08:05:57 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 22 Nov 2025 08:06:02 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 22 Nov 2025 08:06:02 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 22 Nov 2025 08:06:02 GMT
WORKDIR /var/www/html
# Sat, 22 Nov 2025 08:06:03 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 22 Nov 2025 08:06:03 GMT
STOPSIGNAL SIGQUIT
# Sat, 22 Nov 2025 08:06:03 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 22 Nov 2025 08:06:03 GMT
CMD ["php-fpm"]
# Mon, 24 Nov 2025 18:36:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 24 Nov 2025 18:36:57 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Mon, 24 Nov 2025 18:36:57 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Mon, 24 Nov 2025 18:36:57 GMT
ENV DRUPAL_VERSION=11.2.10
# Mon, 24 Nov 2025 18:36:57 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 24 Nov 2025 18:36:57 GMT
WORKDIR /opt/drupal
# Sun, 14 Dec 2025 09:07:26 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Sun, 14 Dec 2025 09:07:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Sun, 07 Dec 2025 22:49:04 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58e9f10e445dbf7ba866462dd44d0f912a09342dc97a4685769a2d057bcc7a9`  
		Last Modified: Tue, 09 Dec 2025 02:08:24 GMT  
		Size: 3.6 MB (3600269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2579c35b4a5055268b9ccb82f8c3307c0a781af77168952679399ed4bde3b60a`  
		Last Modified: Tue, 09 Dec 2025 02:08:23 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b6a920874b5f6759a41702af348a1eefb32a0674eeae4cd9d750418594caed`  
		Last Modified: Tue, 09 Dec 2025 02:08:23 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331170c4328036a3269b793e5fd9ac752d80feb44103a984ea324988b0db1df4`  
		Last Modified: Sat, 22 Nov 2025 07:08:45 GMT  
		Size: 13.7 MB (13673887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c2a8a76b8fe94dfb64b674f64bb4173189f79d3b177f92ff910f6a2cd067311`  
		Last Modified: Sat, 22 Nov 2025 07:08:42 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ebb538a608d81d53634b820fe51785d32273bb08a3dfc12249c664908ee311`  
		Last Modified: Sat, 22 Nov 2025 08:07:05 GMT  
		Size: 14.4 MB (14437528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3886d8190f13d76eddc2ac15e637d39ae230fec2df1617ffe46eaf390b5d2ff2`  
		Last Modified: Sat, 22 Nov 2025 08:07:03 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0bf09194f621a0baca60fb48d1d2a411ce019ead0db362a4c1172a8d32910b5`  
		Last Modified: Sat, 22 Nov 2025 08:07:03 GMT  
		Size: 19.9 KB (19868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f794309f515a91b31a599675d6a1981dc1be4f16e25297ea0e76d501d0af7d68`  
		Last Modified: Sat, 22 Nov 2025 08:07:03 GMT  
		Size: 19.9 KB (19857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb73575e1657db4aba3f2abd6e0279e849be1df4f00867c4fac50b9c2aa73796`  
		Last Modified: Sat, 22 Nov 2025 08:07:03 GMT  
		Size: 9.2 KB (9194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c2af42431a9827bdf18bf636f27b5009dcfbf16c5380715b99f5a356467e39`  
		Last Modified: Mon, 24 Nov 2025 18:40:24 GMT  
		Size: 1.4 MB (1414748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c65fd8289e0bd42ddfe2270f04e3eaf4901e1d9b457f9baaccbac558f60e77`  
		Last Modified: Mon, 24 Nov 2025 18:40:24 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119fc818753b260525f3638a1a8846bcfdb0c7cb8d61680ad028902181050ede`  
		Last Modified: Mon, 24 Nov 2025 18:40:24 GMT  
		Size: 778.0 KB (777997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b81559b10c9181b0f691f5727b63bd3b948bfb27720214b1deef5256bd4528a`  
		Last Modified: Mon, 24 Nov 2025 18:40:24 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b25d0f03ef60d6434106a524c3bae158f581d6c98257c6b7fa15d37c7fb447cc`  
		Last Modified: Sun, 14 Dec 2025 09:10:07 GMT  
		Size: 20.6 MB (20647125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:0b9a3f89b17ee0acb69ac1417dd52b8d843b2f7c983fb06f629db916b44da589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **409.1 KB (409132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27727527e8579d148bd6cc23012e555d25348436bdbfbab602781a3b03686eeb`

```dockerfile
```

-	Layers:
	-	`sha256:5a0279520f03b77f38048fbefff1c8fcd1055b005cd61cd272f2af991e10df40`  
		Last Modified: Sun, 14 Dec 2025 11:58:01 GMT  
		Size: 374.5 KB (374545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0c26e991a402604470f7d03a584d1af0112ddecf9f4b5197e92ab41a8460ff5`  
		Last Modified: Sun, 14 Dec 2025 11:58:02 GMT  
		Size: 34.6 KB (34587 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-fpm-alpine3.22` - linux; s390x

```console
$ docker pull drupal@sha256:c8815073b5c119735fbff1a50dcaeca8518868df0a4020c4022e7ccfa105a753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59713423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58166ed1cbf24d387852dab8d94c4888409198e769de1c98f3b2b0d6f21aa2a9`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 20 Nov 2025 20:07:46 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Nov 2025 20:07:46 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 18 Dec 2025 21:25:45 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 18 Dec 2025 21:25:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Dec 2025 21:25:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Dec 2025 21:25:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Dec 2025 21:25:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Dec 2025 21:25:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Dec 2025 21:25:45 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 18 Dec 2025 21:25:45 GMT
ENV PHP_VERSION=8.4.16
# Thu, 18 Dec 2025 21:25:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.16.tar.xz.asc
# Thu, 18 Dec 2025 21:25:45 GMT
ENV PHP_SHA256=f66f8f48db34e9e29f7bfd6901178e9cf4a1b163e6e497716dfcb8f88bcfae30
# Fri, 19 Dec 2025 01:39:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Dec 2025 01:39:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 01:44:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Dec 2025 01:44:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 01:44:39 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Dec 2025 01:44:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Dec 2025 01:44:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Dec 2025 01:44:40 GMT
WORKDIR /var/www/html
# Fri, 19 Dec 2025 01:44:40 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 19 Dec 2025 01:44:40 GMT
STOPSIGNAL SIGQUIT
# Fri, 19 Dec 2025 01:44:40 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 19 Dec 2025 01:44:40 GMT
CMD ["php-fpm"]
# Fri, 19 Dec 2025 02:15:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 19 Dec 2025 02:15:30 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 19 Dec 2025 02:15:30 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 02:15:30 GMT
ENV DRUPAL_VERSION=11.3.1
# Fri, 19 Dec 2025 02:15:30 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Dec 2025 02:15:30 GMT
WORKDIR /opt/drupal
# Fri, 19 Dec 2025 02:15:37 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 19 Dec 2025 02:15:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Sun, 07 Dec 2025 14:06:46 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd4b2ff0842c178e1087be78ce7fd9398e218ab3073b14df552c39751910aff3`  
		Last Modified: Thu, 20 Nov 2025 20:25:24 GMT  
		Size: 3.7 MB (3692751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98970dae6ec226fa5b2211ea3ccd1469feab0f7fe3b6e39ee7636d46eda3ec13`  
		Last Modified: Thu, 18 Dec 2025 21:31:04 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ce81fd762306676d63e4ae5519fafe546496c1de85dfad336d2b374a174305`  
		Last Modified: Thu, 18 Dec 2025 21:31:02 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:483c6f76270e27dfa7045e1775bfca014ec7271e5ccefccaf9ce7a65e6eaf5ab`  
		Last Modified: Fri, 19 Dec 2025 01:44:32 GMT  
		Size: 13.7 MB (13682624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb300000245d045822755ff4052ee8ea42107e1f0a123cd71843935be736139`  
		Last Modified: Fri, 19 Dec 2025 01:44:31 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816da2185bcf57be479333ce81be01e800f027163dfca37d0e465bd4b0abc2aa`  
		Last Modified: Fri, 19 Dec 2025 01:44:58 GMT  
		Size: 15.0 MB (15024404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e0a36bbca8bc72dffde19812c8839de9205584ae58500bed978a0ae88dd495`  
		Last Modified: Fri, 19 Dec 2025 01:44:56 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39620d36588939ff9c7c9a64e8a5e61241365d4dc27634e5f67e6c2119505159`  
		Last Modified: Fri, 19 Dec 2025 01:45:05 GMT  
		Size: 19.9 KB (19885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326ff9f50ccba8710a912fe3953b5a442a6dc2ace2f93bf04cc3a7f255cf13e1`  
		Last Modified: Fri, 19 Dec 2025 01:44:56 GMT  
		Size: 19.9 KB (19883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb58bf997fcb78af28728c82a370c51cc906141db98d152736f74668c27df777`  
		Last Modified: Fri, 19 Dec 2025 01:44:57 GMT  
		Size: 9.2 KB (9192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15fe5994a5354942d8abe5326551dc4ac6730fdcc33ea7ad3d57d92e3c68ed4f`  
		Last Modified: Fri, 19 Dec 2025 02:16:04 GMT  
		Size: 1.5 MB (1539777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94cac6d759d0e2f9f23f002fe17f879a5ade186e22cf33c349f3d95645109ca`  
		Last Modified: Fri, 19 Dec 2025 02:16:04 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ac98d7a24c94f3fa24e236442200c4c351e8a65a10eeee7bceab031289e0c6`  
		Last Modified: Fri, 19 Dec 2025 02:16:12 GMT  
		Size: 778.0 KB (777996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2b347f6fe83fdb12c9697f8226a5b9d4cd2fc22798d27ee485b94bfca0c390`  
		Last Modified: Fri, 19 Dec 2025 02:15:56 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b79a63aea2c5cfc98d1641945c844174e8eb875c220d3c5c1372f4ac613eee`  
		Last Modified: Fri, 19 Dec 2025 02:16:07 GMT  
		Size: 21.3 MB (21293105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:245e72b85aaaca06b5cfa97e7beba462112553ec94cdcea19ec02c92bb4574ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.9 KB (406877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ea0cbe75c7b1b4d7bd84bb65ee657c42da6bcf0f6759ae8997ed2fbdbca5c38`

```dockerfile
```

-	Layers:
	-	`sha256:a32910e1bee5123d94b52250159a58febe58a531f18ed52139e97682b54c92e0`  
		Last Modified: Fri, 19 Dec 2025 06:07:29 GMT  
		Size: 372.4 KB (372377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1ee6bc6d6241ebb12f8d8a0286dd47668a665b219c781802f62e0ab35e8a891`  
		Last Modified: Fri, 19 Dec 2025 06:07:30 GMT  
		Size: 34.5 KB (34500 bytes)  
		MIME: application/vnd.in-toto+json
