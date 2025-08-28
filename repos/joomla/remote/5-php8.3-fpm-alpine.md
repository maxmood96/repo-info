## `joomla:5-php8.3-fpm-alpine`

```console
$ docker pull joomla@sha256:14b9ad79597d0373f75979efb9e8fc5acdab4434b6443e7a16605a14c5f5591f
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

### `joomla:5-php8.3-fpm-alpine` - linux; amd64

```console
$ docker pull joomla@sha256:5e3523ea4b484199523a906ba505be1aee1fc653c1a3fd3d02bfad09105f0fc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 MB (96443007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:052cb4dbdcb75b40307bc074fa29bb1d28387753e09708739bd649367371e9b8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 19 Aug 2025 22:37:33 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 Aug 2025 22:37:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_VERSION=8.3.25
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.25.tar.xz.asc
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_SHA256=187b61bb795015adacf53f8c55b44414a63777ec19a776b75fb88614506c0d37
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 Aug 2025 22:37:33 GMT
WORKDIR /var/www/html
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 Aug 2025 22:37:33 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 19 Aug 2025 22:37:33 GMT
CMD ["php-fpm"]
# Tue, 19 Aug 2025 22:37:33 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 		zstd 	; # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		icu-dev 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libmemcached-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 		pecl install APCu-5.1.24; 	pecl install memcached-3.3.0; 	pecl install redis-6.1.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .joomla-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
VOLUME [/var/www/html]
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_VERSION=5.3.3
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_SHA512=efc0c5249758f1f7d9915992e01aa44203e86126c59c4c3adec8a7342aec132da2f5e10910fd7e2485ab8f58faa981de6be99cfe3c3b3f3c1e79e7d2d0321388
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.3.3/Joomla_5.3.3-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY makedb.php /makedb.php # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 22:37:33 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e10ac87811a7151f2d455ecd66e1f24914759aa556bf865115e9b5451c34c6`  
		Last Modified: Thu, 28 Aug 2025 18:19:54 GMT  
		Size: 5.9 MB (5927523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8fc0402d547809980039811ae9b42dfcded62490cdfd22f86eeae02a5401c4f`  
		Last Modified: Thu, 28 Aug 2025 18:19:54 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5118a89a65a7879c4cdee30e47c63bad49e3b3db33a51de3fe326c3d569fc205`  
		Last Modified: Thu, 28 Aug 2025 18:19:54 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd1735270d6e1518aaee894fef4efe6676e548396eb6350a2823bd039d45d65`  
		Last Modified: Thu, 28 Aug 2025 18:19:55 GMT  
		Size: 12.6 MB (12604759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b287e8c3fc7e356d999ffd59f3ff23eaeafabb55d3e982709ea8418d30caa7`  
		Last Modified: Thu, 28 Aug 2025 18:19:54 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1b8c7c6fddb40b2fb483e7c0cdb28a715ad094759babae305cc3ee8b3324cad`  
		Last Modified: Thu, 28 Aug 2025 18:19:55 GMT  
		Size: 13.3 MB (13265060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca0b473638630b0d5752cba198cb4c45e865cc6f571d15a657778b8c9573f7c`  
		Last Modified: Thu, 28 Aug 2025 18:19:54 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fadbc3591c836d34e9c40cf1dbc676c2da1c2c323afd6e29624fe20bf6143a7f`  
		Last Modified: Thu, 28 Aug 2025 18:19:54 GMT  
		Size: 20.0 KB (19959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fff2d0bf89e370e10b4bdf5193157afcda7091db8c80f48573111444634e51a`  
		Last Modified: Thu, 28 Aug 2025 18:19:54 GMT  
		Size: 19.9 KB (19950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a961078f85baeb62fad90d7f53e5a386185ce08cde9f06f1cbaa0c3d91b7e81`  
		Last Modified: Thu, 28 Aug 2025 18:54:14 GMT  
		Size: 9.2 KB (9176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0a3c81efc3160d1d0a912eed52f99530721bec13c4674fccfe10325c4e162d`  
		Last Modified: Thu, 28 Aug 2025 18:59:04 GMT  
		Size: 28.4 MB (28406536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a7020fc00a74953652e940faf37e374c4dcb431f5c2c9adb69fb9ae7a8f514`  
		Last Modified: Thu, 28 Aug 2025 18:59:01 GMT  
		Size: 7.2 MB (7199698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d209909025d5469b9203b239307a003b39614b8545e9b613895af97fb7b8a54`  
		Last Modified: Thu, 28 Aug 2025 18:59:01 GMT  
		Size: 63.4 KB (63363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4daf4a73f3a4ff40c699a5e7f816c184f5f22b152b7ab8369b2f2813c1233f`  
		Last Modified: Thu, 28 Aug 2025 18:59:01 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c6517e9f97505295cec2a91ac46f8f65c42506a49c7f383247063f5417d9eb`  
		Last Modified: Thu, 28 Aug 2025 18:59:10 GMT  
		Size: 25.1 MB (25118063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73312afbf720257fe50c03751858a2a6b626bf6176dfc8f25d0e0a4d86462e43`  
		Last Modified: Thu, 28 Aug 2025 18:59:02 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377d0c57f2fcb77c2f191820f0c7cbea3061dd90ad578407ccf334c1b12749c0`  
		Last Modified: Thu, 28 Aug 2025 18:59:02 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:5-php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull joomla@sha256:a94ddff9f896b2988b216aa6e860b8f747f2a391c9450b978a9f4a06dc0d3528
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 KB (46082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0ebba683d4dc9fa13dc48766293a108f423c0b40fa412638ccde0f3202a0adf`

```dockerfile
```

-	Layers:
	-	`sha256:d79bca1fc0ee29603fb119e2aab49efaddb54237ad2a17d6131e358673942681`  
		Last Modified: Thu, 28 Aug 2025 19:44:11 GMT  
		Size: 46.1 KB (46082 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:5-php8.3-fpm-alpine` - linux; arm variant v6

```console
$ docker pull joomla@sha256:ae5e8ac589c263bc2a7b5999433c0bced6e62e16e4efd6248296f17fb94c2710
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.7 MB (91654453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ec16ec2cfc2b1ce3fa35f9a1f333b3a52c52abb397f9636c9107b02398d4cda`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 31 Jul 2025 20:44:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 31 Jul 2025 20:44:18 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 31 Jul 2025 20:44:18 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 31 Jul 2025 20:44:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 31 Jul 2025 20:44:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 31 Jul 2025 20:44:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 31 Jul 2025 20:44:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 31 Jul 2025 20:44:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 31 Jul 2025 20:44:18 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 31 Jul 2025 20:44:18 GMT
ENV PHP_VERSION=8.3.24
# Thu, 31 Jul 2025 20:44:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.24.tar.xz.asc
# Thu, 31 Jul 2025 20:44:18 GMT
ENV PHP_SHA256=388ee5fd111097e97bae439bff46aec4ea27f816d3f0c2cb5490a41410d44251
# Thu, 31 Jul 2025 20:44:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 31 Jul 2025 20:44:18 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 31 Jul 2025 20:44:18 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 31 Jul 2025 20:44:18 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 31 Jul 2025 20:44:18 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 31 Jul 2025 20:44:18 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 31 Jul 2025 20:44:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 31 Jul 2025 20:44:18 GMT
WORKDIR /var/www/html
# Thu, 31 Jul 2025 20:44:18 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 31 Jul 2025 20:44:18 GMT
STOPSIGNAL SIGQUIT
# Thu, 31 Jul 2025 20:44:18 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 31 Jul 2025 20:44:18 GMT
CMD ["php-fpm"]
# Tue, 19 Aug 2025 22:37:33 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 		zstd 	; # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		icu-dev 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libmemcached-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 		pecl install APCu-5.1.24; 	pecl install memcached-3.3.0; 	pecl install redis-6.1.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .joomla-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
VOLUME [/var/www/html]
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_VERSION=5.3.3
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_SHA512=efc0c5249758f1f7d9915992e01aa44203e86126c59c4c3adec8a7342aec132da2f5e10910fd7e2485ab8f58faa981de6be99cfe3c3b3f3c1e79e7d2d0321388
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.3.3/Joomla_5.3.3-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY makedb.php /makedb.php # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 22:37:33 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d22834b475ece2203538fb14057fd70a6b00476b61f6902242434b53353f4d0`  
		Last Modified: Tue, 15 Jul 2025 20:02:10 GMT  
		Size: 3.4 MB (3422001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f63604d1779bd23de30ef4abf3b540a7b132c0448407347f39a4861ebe61b1`  
		Last Modified: Tue, 15 Jul 2025 20:02:10 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0566a827016b139c8586e6ca71c129f5fbbe4fc6e3cae54b699905df197b2a33`  
		Last Modified: Tue, 15 Jul 2025 20:02:10 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:412aab248b23001939c46b31a1bd44af1cabed7294fb2e28a2d617a380aeb622`  
		Last Modified: Mon, 04 Aug 2025 22:06:29 GMT  
		Size: 12.6 MB (12599867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f46a8da570857cb3459270b7874c27c4bf86e6484af5228a4b6934143323e722`  
		Last Modified: Mon, 04 Aug 2025 22:06:26 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:295337c6456a1d764b61b396d4080ade0d041de6dec37b3ec695ee41fae57584`  
		Last Modified: Mon, 04 Aug 2025 22:12:15 GMT  
		Size: 12.0 MB (11982091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc01084443a99185615578eccfc5961886914790eb58f136137ee4e1352e9419`  
		Last Modified: Mon, 04 Aug 2025 22:12:12 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed776ca2836f12a914deea1513754c7bcb674d6f9a3477ddd91a62a93c99edbf`  
		Last Modified: Mon, 04 Aug 2025 22:12:12 GMT  
		Size: 19.7 KB (19731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc4003e2485f49b6410dc2e8cf1b7b76f508398546b836ecd30175ccff4cd672`  
		Last Modified: Mon, 04 Aug 2025 22:12:12 GMT  
		Size: 19.7 KB (19731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53fcaa21c9f581fe9397d5dd0dd156cb60831d6373f148ecf611d73254f56a9f`  
		Last Modified: Mon, 04 Aug 2025 22:12:13 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f95658ef7e8a6f8663b491d1333d0e923f59f89d9a68b108f45c17c62c329ed`  
		Last Modified: Tue, 19 Aug 2025 23:05:46 GMT  
		Size: 25.4 MB (25410977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3762e0c3c980f965a648c005e835396738036efdbd00a0b346721c960b578719`  
		Last Modified: Tue, 19 Aug 2025 23:05:44 GMT  
		Size: 9.5 MB (9499322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a9bc00dc23be7a8ebb946cad1b1bf4cd3e8870b866ae387fbc552bde1c6e2a5`  
		Last Modified: Tue, 19 Aug 2025 23:05:44 GMT  
		Size: 63.3 KB (63336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b30054e99a28432127e10be2d85633a9f11eb02d9bb1e03d7a180b88aefe07c`  
		Last Modified: Tue, 19 Aug 2025 23:05:44 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1253cbd1b00e5bd6a7a1497a57b90bdbd16b18df8ee49d449de2d6f009eb674`  
		Last Modified: Tue, 19 Aug 2025 23:13:49 GMT  
		Size: 25.1 MB (25118064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6746d0129da780346b11fc491e1fba3a400041a328407f9930e01e2a622e1d`  
		Last Modified: Tue, 19 Aug 2025 23:13:41 GMT  
		Size: 3.7 KB (3653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03064082af152f09adef4b8c8607afc521664e8cde52edca3a7a96b9defb3e79`  
		Last Modified: Tue, 19 Aug 2025 23:13:41 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:5-php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull joomla@sha256:b6807bb42c36ffadcf498663554dfb5a927e71cd3057dbcd5aec06fab8294f82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 KB (46210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e726cd8b572abfdc4d7f02d48f15fa7141d0059e57a742f8fc40e8c3bc82cf61`

```dockerfile
```

-	Layers:
	-	`sha256:0ba94d507dc761e86d5e4b7ad2eb669a9d209ddc89a7963f99771ba8909738e7`  
		Last Modified: Wed, 20 Aug 2025 01:48:23 GMT  
		Size: 46.2 KB (46210 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:5-php8.3-fpm-alpine` - linux; arm variant v7

```console
$ docker pull joomla@sha256:fde2643e4313d0f33fe93d2b4f64cefa3b7c5466150f42ca042b0fda6d3488eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.0 MB (89004848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c538cedfd17843a4147d017d9c4adb82fba46e3777526266613036398ec24ef3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 31 Jul 2025 20:44:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 31 Jul 2025 20:44:18 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 31 Jul 2025 20:44:18 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 31 Jul 2025 20:44:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 31 Jul 2025 20:44:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 31 Jul 2025 20:44:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 31 Jul 2025 20:44:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 31 Jul 2025 20:44:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 31 Jul 2025 20:44:18 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 31 Jul 2025 20:44:18 GMT
ENV PHP_VERSION=8.3.24
# Thu, 31 Jul 2025 20:44:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.24.tar.xz.asc
# Thu, 31 Jul 2025 20:44:18 GMT
ENV PHP_SHA256=388ee5fd111097e97bae439bff46aec4ea27f816d3f0c2cb5490a41410d44251
# Thu, 31 Jul 2025 20:44:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 31 Jul 2025 20:44:18 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 31 Jul 2025 20:44:18 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 31 Jul 2025 20:44:18 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 31 Jul 2025 20:44:18 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 31 Jul 2025 20:44:18 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 31 Jul 2025 20:44:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 31 Jul 2025 20:44:18 GMT
WORKDIR /var/www/html
# Thu, 31 Jul 2025 20:44:18 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 31 Jul 2025 20:44:18 GMT
STOPSIGNAL SIGQUIT
# Thu, 31 Jul 2025 20:44:18 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 31 Jul 2025 20:44:18 GMT
CMD ["php-fpm"]
# Tue, 19 Aug 2025 22:37:33 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 		zstd 	; # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		icu-dev 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libmemcached-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 		pecl install APCu-5.1.24; 	pecl install memcached-3.3.0; 	pecl install redis-6.1.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .joomla-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
VOLUME [/var/www/html]
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_VERSION=5.3.3
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_SHA512=efc0c5249758f1f7d9915992e01aa44203e86126c59c4c3adec8a7342aec132da2f5e10910fd7e2485ab8f58faa981de6be99cfe3c3b3f3c1e79e7d2d0321388
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.3.3/Joomla_5.3.3-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY makedb.php /makedb.php # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 22:37:33 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdac87f9414bf366e318e5481a7ff1ed73cd811cd08fe0b8520657cf9b1a85f5`  
		Last Modified: Tue, 15 Jul 2025 19:40:41 GMT  
		Size: 3.2 MB (3240894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9762a4da160644bcaa3d665d94969930997f9214ad191083373940ee5240dc1`  
		Last Modified: Tue, 15 Jul 2025 19:40:40 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ebef0b263131dc81229136e7114545e060fdf60de8166dced2089dd8f8c4fd`  
		Last Modified: Tue, 15 Jul 2025 19:40:40 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba00dd2d5d8f6a44bf0a20885871d1853fc7167d84fb6ec957e7ac660ed1f49`  
		Last Modified: Tue, 05 Aug 2025 00:07:34 GMT  
		Size: 12.6 MB (12599855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01db466338552dbc3e51fab25cfb4c0a29f8cba308945ce14c23b2f3cc32a569`  
		Last Modified: Tue, 05 Aug 2025 00:07:32 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5e1050777a14bb79aae042037d3142cdf0379a6fa13e1bbd464536acaab1c4`  
		Last Modified: Tue, 05 Aug 2025 00:11:30 GMT  
		Size: 11.3 MB (11287235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3533ff91d2cbf4b64276ed59a40895b09a8dcd8196b65d19578e2c5fb49878e1`  
		Last Modified: Tue, 05 Aug 2025 00:11:29 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b0618cc8e7a0c9625469ed1f03151d3a30be85350383e190f2611267e11ce7`  
		Last Modified: Tue, 05 Aug 2025 00:11:29 GMT  
		Size: 19.7 KB (19725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c93fa35098206749c593cfd31020dd3187b539cb278056d4b68f8a7abd3312`  
		Last Modified: Tue, 05 Aug 2025 00:11:29 GMT  
		Size: 19.7 KB (19717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c160173b8f73a178b3ac82cfd72acbd558dba08c5a7ed38426a8a9e6eb839f`  
		Last Modified: Tue, 05 Aug 2025 00:11:30 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9276c7f96a273047a310c22e6a98dee12932c05916640194d76679daaa796662`  
		Last Modified: Tue, 19 Aug 2025 23:10:03 GMT  
		Size: 24.1 MB (24121381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac9f56a8c82953c98430156f8a5a20ccd464af232b210b93d0cda68c2199a0e`  
		Last Modified: Tue, 19 Aug 2025 23:10:03 GMT  
		Size: 9.3 MB (9297219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506070f9e14ff672133b75db0dde37ced587af1a18391fc733a91edcb78a68b5`  
		Last Modified: Tue, 19 Aug 2025 23:10:02 GMT  
		Size: 63.3 KB (63296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac31711e6fb5220a11bf4f4441247ae8ee8357cb8af2108b31e3afbfc42a65a`  
		Last Modified: Tue, 19 Aug 2025 23:10:02 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64371ecc02f1b335a82e03d49d2027758d813b3881de0d3bf83e946aef6d1fec`  
		Last Modified: Tue, 19 Aug 2025 23:37:43 GMT  
		Size: 25.1 MB (25118065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5932d5b0a0021de1e7313b5199a0a804f10f36b8c3e0aa73c9d7ed478edd42fe`  
		Last Modified: Tue, 19 Aug 2025 23:37:41 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07cc1ed74b501d1a9677978b2691234e3b370a0dec6c530b3ca9ae75c7c88581`  
		Last Modified: Tue, 19 Aug 2025 23:37:41 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:5-php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull joomla@sha256:113278e9f8ddd38d93658cb8b4f2c6a743ce8ff1cdd7a8d4aae885d14dbaa523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 KB (46210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed9d2bf4a57e264a532a9a34264663a93afd1f0421c29f39f29d68b2e6f4a4e2`

```dockerfile
```

-	Layers:
	-	`sha256:94e30e8c1913c3dc9c8fa0bcc1146281e86707c51f447bae1ac753d0e4820aed`  
		Last Modified: Wed, 20 Aug 2025 01:48:26 GMT  
		Size: 46.2 KB (46210 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:5-php8.3-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull joomla@sha256:0f3866acb3a0b06e139d77e4b4b67d335cf510da9d11694757cb20742a55cea2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.3 MB (97267364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8f800c3ca51a731e187c1e2f3241ec76904fe08fcd104e2dd7594e8181469f0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 31 Jul 2025 20:44:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 31 Jul 2025 20:44:18 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 31 Jul 2025 20:44:18 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 31 Jul 2025 20:44:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 31 Jul 2025 20:44:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 31 Jul 2025 20:44:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 31 Jul 2025 20:44:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 31 Jul 2025 20:44:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 31 Jul 2025 20:44:18 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 31 Jul 2025 20:44:18 GMT
ENV PHP_VERSION=8.3.24
# Thu, 31 Jul 2025 20:44:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.24.tar.xz.asc
# Thu, 31 Jul 2025 20:44:18 GMT
ENV PHP_SHA256=388ee5fd111097e97bae439bff46aec4ea27f816d3f0c2cb5490a41410d44251
# Thu, 31 Jul 2025 20:44:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 31 Jul 2025 20:44:18 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 31 Jul 2025 20:44:18 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 31 Jul 2025 20:44:18 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 31 Jul 2025 20:44:18 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 31 Jul 2025 20:44:18 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 31 Jul 2025 20:44:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 31 Jul 2025 20:44:18 GMT
WORKDIR /var/www/html
# Thu, 31 Jul 2025 20:44:18 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 31 Jul 2025 20:44:18 GMT
STOPSIGNAL SIGQUIT
# Thu, 31 Jul 2025 20:44:18 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 31 Jul 2025 20:44:18 GMT
CMD ["php-fpm"]
# Tue, 19 Aug 2025 22:37:33 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 		zstd 	; # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		icu-dev 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libmemcached-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 		pecl install APCu-5.1.24; 	pecl install memcached-3.3.0; 	pecl install redis-6.1.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .joomla-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
VOLUME [/var/www/html]
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_VERSION=5.3.3
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_SHA512=efc0c5249758f1f7d9915992e01aa44203e86126c59c4c3adec8a7342aec132da2f5e10910fd7e2485ab8f58faa981de6be99cfe3c3b3f3c1e79e7d2d0321388
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.3.3/Joomla_5.3.3-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY makedb.php /makedb.php # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 22:37:33 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb504dccc917de6b6b8bbc11ff4b9599d71f3ad971f142f67cc631aea843760`  
		Last Modified: Tue, 05 Aug 2025 00:49:21 GMT  
		Size: 3.5 MB (3454743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7532649a0813cdb3165d225287dc7cbef8b4e47991127457849e1947e5549636`  
		Last Modified: Tue, 05 Aug 2025 00:49:21 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e253b9848099c2406835511872822d9dab1ea36834b393e1588c17a784e3bcb1`  
		Last Modified: Tue, 05 Aug 2025 00:49:21 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a54c312f75964337f4db7770ce494c065e1775810a79a6ad25cc8846d1924eb8`  
		Last Modified: Tue, 05 Aug 2025 02:40:12 GMT  
		Size: 12.6 MB (12599871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3179efae18545d01b9663211a16a1cae37ca72749953364336d472c4e81e2f`  
		Last Modified: Tue, 05 Aug 2025 02:40:09 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2e3af117145aa9db60dbdb547182b06888346793df58c20cf6ed3d58f79499`  
		Last Modified: Tue, 05 Aug 2025 02:45:31 GMT  
		Size: 13.2 MB (13249851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71127f1e5a0d78107b15f785398d341b771fdb0179d1132baacf28602dbaafd6`  
		Last Modified: Tue, 05 Aug 2025 02:45:29 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024bb4e36e07326dda259a05227cadf8e5e26b6fc8e6ff2c756423e75f55a5f2`  
		Last Modified: Tue, 05 Aug 2025 02:45:30 GMT  
		Size: 19.8 KB (19752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8110b4929c8b1443c6afd235ecbc59b4a2d6797414a06ba0cc2a541b0e7be8ba`  
		Last Modified: Tue, 05 Aug 2025 02:45:39 GMT  
		Size: 19.7 KB (19749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaddacb01d48656b98dbc057e2387016c89d834cabaf74099ed0fdaa5ef89dc7`  
		Last Modified: Tue, 05 Aug 2025 02:45:29 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30149229ea24a4abf90ede02dce2d303350264ab0949e54ee8977e5498c0271d`  
		Last Modified: Tue, 19 Aug 2025 23:09:05 GMT  
		Size: 28.2 MB (28221824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00dc80efa21634f9e8ed5cc481a7bb65a817f7bec91067cde0733b558fc60bdd`  
		Last Modified: Tue, 19 Aug 2025 23:09:00 GMT  
		Size: 10.4 MB (10371012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2135e24a6aca76ef1f23a18655e7bdf2eb9278c19f094ed76572b84b93295e23`  
		Last Modified: Tue, 19 Aug 2025 23:08:59 GMT  
		Size: 63.3 KB (63327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0a1ebd10496b3bea6a6b85da71c1b76ddb419ee1592db46b26e54975c37e02`  
		Last Modified: Tue, 19 Aug 2025 23:08:59 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:718e792aae871647d7b8502ee1764e1d811489c4bb6aab7d5b8d4cae77f93e5b`  
		Last Modified: Tue, 19 Aug 2025 23:32:44 GMT  
		Size: 25.1 MB (25118065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891345a2397510916012c9aa9d6d56446e5e3b760a9dcaa90a8a2a0916d12ab6`  
		Last Modified: Tue, 19 Aug 2025 23:32:39 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf81a1a1efd3409672af6f17628dabc903fb01c7add4201f690afeced877cf2`  
		Last Modified: Tue, 19 Aug 2025 23:32:40 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:5-php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull joomla@sha256:a6f6df4c049be95175dc094ac49a78bfa748033bbaf01bc0e3c4f2991d7d3138
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 KB (46252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de3777eda29994cd4468f4cc26b6c8da77bcd943d8c8a1c8484d3e88dcd06e59`

```dockerfile
```

-	Layers:
	-	`sha256:d1929b679cf8dc8b0597160fd3445fe8924933a8014b1c3921bf90d7e2841df6`  
		Last Modified: Wed, 20 Aug 2025 01:48:30 GMT  
		Size: 46.3 KB (46252 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:5-php8.3-fpm-alpine` - linux; 386

```console
$ docker pull joomla@sha256:da462916ef177d05e4918606d0318dae5c2f5308e5da0f9070505dc925e5b251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.8 MB (96758262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:160f1eb80795d73cc04589584be3fb87cdcc01a89cd4ca1b29227a1900cdbceb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 19 Aug 2025 22:37:33 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 Aug 2025 22:37:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_VERSION=8.3.25
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.25.tar.xz.asc
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_SHA256=187b61bb795015adacf53f8c55b44414a63777ec19a776b75fb88614506c0d37
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 Aug 2025 22:37:33 GMT
WORKDIR /var/www/html
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 Aug 2025 22:37:33 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 19 Aug 2025 22:37:33 GMT
CMD ["php-fpm"]
# Tue, 19 Aug 2025 22:37:33 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 		zstd 	; # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		icu-dev 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libmemcached-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 		pecl install APCu-5.1.24; 	pecl install memcached-3.3.0; 	pecl install redis-6.1.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .joomla-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
VOLUME [/var/www/html]
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_VERSION=5.3.3
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_SHA512=efc0c5249758f1f7d9915992e01aa44203e86126c59c4c3adec8a7342aec132da2f5e10910fd7e2485ab8f58faa981de6be99cfe3c3b3f3c1e79e7d2d0321388
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.3.3/Joomla_5.3.3-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY makedb.php /makedb.php # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 22:37:33 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c9a59919ff7785468d660110ee9507b13705f5565f639b7d7bca52a140856b5`  
		Last Modified: Thu, 28 Aug 2025 18:21:34 GMT  
		Size: 5.8 MB (5794083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33e8e8baf1e334700853edab49903aab1f8ea7b65bc8ea9036cad309a3b7118`  
		Last Modified: Thu, 28 Aug 2025 18:21:33 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76198f21a38b8e65970b7af97c8146cceaaec7b8de4cf4fce2e437c8d7c1ded2`  
		Last Modified: Thu, 28 Aug 2025 18:21:33 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0592096578de3942e0d1a4c0f06e422ce9b189222d19d93f037d9a2a7cd776dd`  
		Last Modified: Thu, 28 Aug 2025 18:21:35 GMT  
		Size: 12.6 MB (12604751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96ff3610c46e30d8afb952ca77229101670ff07b031f0081af9be71a61f790d9`  
		Last Modified: Thu, 28 Aug 2025 18:21:33 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654f9edc9ac84dc15c4aeb3c15f82244bce0018deaef4c21466f4176f60271d3`  
		Last Modified: Thu, 28 Aug 2025 18:21:35 GMT  
		Size: 13.6 MB (13576202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a6a5ffb0b2a909ed36d16b6d5edb06ad2441db4e65f12a3e54b31a4257f002`  
		Last Modified: Thu, 28 Aug 2025 18:21:33 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88c4b3d6bd1e1a984ffcff35fb9de7fde05ffe9612a5162b6623b81891a7738f`  
		Last Modified: Thu, 28 Aug 2025 18:21:33 GMT  
		Size: 19.9 KB (19939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7860d1b0c44da61c8fcd2da1c6fc38bb05b9af25db92a95654b50e27c114639d`  
		Last Modified: Thu, 28 Aug 2025 18:21:34 GMT  
		Size: 19.9 KB (19931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264286dd6fb0223c2ba34bbb87fdf4e5aa440f4c3d17067731cb9bca46215247`  
		Last Modified: Thu, 28 Aug 2025 18:21:33 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69640d6684af4c4db4643a4afcfcbda8c9194efd00008759171928ad817e48c`  
		Last Modified: Thu, 28 Aug 2025 19:44:48 GMT  
		Size: 28.6 MB (28622590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:509efa728e93fc0295fdd43cd8a29adf548ca4fa3c797a8218290218e41d347a`  
		Last Modified: Thu, 28 Aug 2025 19:44:43 GMT  
		Size: 7.3 MB (7305997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3b3ac8aac526bdbfc8bb515017f10c183c543105ff75ef931e695e5a356baf`  
		Last Modified: Thu, 28 Aug 2025 19:44:43 GMT  
		Size: 63.3 KB (63285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b75e27c8e788502bba7d4e8f50807531e3838a8a2708f9d7e101b016ee59ec`  
		Last Modified: Thu, 28 Aug 2025 19:44:43 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b709f69e9d257840964c40c06764029e9bd26861af208980263d58918e886688`  
		Last Modified: Thu, 28 Aug 2025 19:44:47 GMT  
		Size: 25.1 MB (25118066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aeb42eef14c5fd65901744ccf4330ead5943589eab44c6461958201c047be64`  
		Last Modified: Thu, 28 Aug 2025 19:44:43 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83196571831205812dda61945d6a1d8487d0a15c79caa300d67f777d4440fe6d`  
		Last Modified: Thu, 28 Aug 2025 19:44:44 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:5-php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull joomla@sha256:814f10e254529596dbb0be8db06dc0bd53c4983d06f5ae848c23991dab49a565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 KB (46042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0a49ef366fb2cb04ba9af41564751d49e48c41356789a915725c1c9a09638cc`

```dockerfile
```

-	Layers:
	-	`sha256:432d81fa4b84f0de02f72283052b322024f7bffe9640982c50e53c80e3c24bf4`  
		Last Modified: Thu, 28 Aug 2025 19:44:22 GMT  
		Size: 46.0 KB (46042 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:5-php8.3-fpm-alpine` - linux; ppc64le

```console
$ docker pull joomla@sha256:6a0ff2b4ef1ef212923caec4e6503e2e37376715cab603b63823db2d67b86187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 MB (98063613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d602ae27105630fe57a0c6425811d9f432087174b4ecb116c23d5d2e85696a8c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 31 Jul 2025 20:44:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 31 Jul 2025 20:44:18 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 31 Jul 2025 20:44:18 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 31 Jul 2025 20:44:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 31 Jul 2025 20:44:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 31 Jul 2025 20:44:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 31 Jul 2025 20:44:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 31 Jul 2025 20:44:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 31 Jul 2025 20:44:18 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 31 Jul 2025 20:44:18 GMT
ENV PHP_VERSION=8.3.24
# Thu, 31 Jul 2025 20:44:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.24.tar.xz.asc
# Thu, 31 Jul 2025 20:44:18 GMT
ENV PHP_SHA256=388ee5fd111097e97bae439bff46aec4ea27f816d3f0c2cb5490a41410d44251
# Thu, 31 Jul 2025 20:44:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 31 Jul 2025 20:44:18 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 31 Jul 2025 20:44:18 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 31 Jul 2025 20:44:18 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 31 Jul 2025 20:44:18 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 31 Jul 2025 20:44:18 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 31 Jul 2025 20:44:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 31 Jul 2025 20:44:18 GMT
WORKDIR /var/www/html
# Thu, 31 Jul 2025 20:44:18 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 31 Jul 2025 20:44:18 GMT
STOPSIGNAL SIGQUIT
# Thu, 31 Jul 2025 20:44:18 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 31 Jul 2025 20:44:18 GMT
CMD ["php-fpm"]
# Tue, 19 Aug 2025 22:37:33 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 		zstd 	; # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		icu-dev 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libmemcached-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 		pecl install APCu-5.1.24; 	pecl install memcached-3.3.0; 	pecl install redis-6.1.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .joomla-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
VOLUME [/var/www/html]
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_VERSION=5.3.3
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_SHA512=efc0c5249758f1f7d9915992e01aa44203e86126c59c4c3adec8a7342aec132da2f5e10910fd7e2485ab8f58faa981de6be99cfe3c3b3f3c1e79e7d2d0321388
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.3.3/Joomla_5.3.3-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY makedb.php /makedb.php # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 22:37:33 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c06a09b74ec526da3ee14df3d2b5a91f72a4fa277f482bbf918bb4cccb1652b`  
		Last Modified: Tue, 05 Aug 2025 00:06:20 GMT  
		Size: 3.6 MB (3611165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed9e57a166c2abcf7305f3cb2afd6de830c6af45dd6c91b2a8218f7a4912f6c`  
		Last Modified: Tue, 05 Aug 2025 00:06:19 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e0e72d666cf9be46385f732d53bc45342fa962757abf4c31f4b45015775159`  
		Last Modified: Tue, 05 Aug 2025 00:06:19 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7afea3ff1a55cd1792a8e64481f14518dfcb576dfa3d19bf97e598dc725a314`  
		Last Modified: Tue, 05 Aug 2025 01:24:26 GMT  
		Size: 12.6 MB (12599881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ce8edbb87bbd2dae7350f982fef8786dab63c95b1cdcaa6447b211ea5dd6d6`  
		Last Modified: Tue, 05 Aug 2025 01:24:25 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345e094929378315708a186dd96aec526fcce0b74800d7da428c1fc526a69f7c`  
		Last Modified: Tue, 05 Aug 2025 01:27:58 GMT  
		Size: 13.7 MB (13733436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c67a689b009152557ab3f5e3109a568cd2181e27a9a8880e5f8424106b5647af`  
		Last Modified: Tue, 05 Aug 2025 01:27:54 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e438da494fff08dd7155b6f3c5929f50cfe9230d3084485a2d94bfbb89b11ec2`  
		Last Modified: Tue, 05 Aug 2025 01:27:54 GMT  
		Size: 19.7 KB (19738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:965b1a291960272c429bc9fd3e8ad7ffeda0dbceea98e9de56c1679d92ab972f`  
		Last Modified: Tue, 05 Aug 2025 01:27:54 GMT  
		Size: 19.7 KB (19728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecad038c628b170712953ffd695fd9e7205f2b61a0cd789750a5a06c2f96ba4e`  
		Last Modified: Tue, 05 Aug 2025 01:27:54 GMT  
		Size: 9.2 KB (9176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce8d337469a7bc2ee8762517ce138561fc589292354d78d1d528bf4c46bae93`  
		Last Modified: Tue, 19 Aug 2025 23:12:01 GMT  
		Size: 29.1 MB (29053447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395c59f7ae0e31839d7d1e24eab0364e83fda5386c392784fc26c56d13265945`  
		Last Modified: Tue, 19 Aug 2025 23:11:58 GMT  
		Size: 10.1 MB (10099259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca46daf433f203a076eb26f702604d1fd2f978b9f4a8a098ed1603b1e60d2ee`  
		Last Modified: Tue, 19 Aug 2025 23:11:57 GMT  
		Size: 63.3 KB (63328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb8cb6b63a00b0540e238c73fcf0f729686fdb268446d573874432061d2f0f5`  
		Last Modified: Tue, 19 Aug 2025 23:11:57 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91fa4a3b7c1d6cf0d521787aca5d7dabdd7b5ed52698bc8667f70cc988dcf32`  
		Last Modified: Tue, 19 Aug 2025 23:51:39 GMT  
		Size: 25.1 MB (25118099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6961e116f602275a8e850c1461761f12ec61beae2a04ac62b21fc245bbdbb0d7`  
		Last Modified: Tue, 19 Aug 2025 23:51:34 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522e88f26b5053e336a58963f0ebc0a8b4b20e7c03ec482b3d86979ba25ef1fb`  
		Last Modified: Tue, 19 Aug 2025 23:51:34 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:5-php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull joomla@sha256:1e5f6159eebef5fa4e7ab4db9de677816d99dc86ea06d202b0c55d378cc4a395
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 KB (46140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a44b9dd996d79810e2dd2cf822c7bed225dae83460ca91b1caa6c8b00d114abc`

```dockerfile
```

-	Layers:
	-	`sha256:f4766fca15995aa371125cfd3319151edf7fd7ec1288d3b90235e9b616b65bed`  
		Last Modified: Wed, 20 Aug 2025 01:48:36 GMT  
		Size: 46.1 KB (46140 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:5-php8.3-fpm-alpine` - linux; riscv64

```console
$ docker pull joomla@sha256:7e848c4805d5f0ea131942858afdd68d3ba854c6cd508fd9e37a7a46ba9f4365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.5 MB (95527612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cae4c139f1b086b292694bd30161e30ed856df49e4f3a2e743432f991d741bcb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 31 Jul 2025 20:44:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 31 Jul 2025 20:44:18 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 31 Jul 2025 20:44:18 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 31 Jul 2025 20:44:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 31 Jul 2025 20:44:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 31 Jul 2025 20:44:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 31 Jul 2025 20:44:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 31 Jul 2025 20:44:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 31 Jul 2025 20:44:18 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 31 Jul 2025 20:44:18 GMT
ENV PHP_VERSION=8.3.24
# Thu, 31 Jul 2025 20:44:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.24.tar.xz.asc
# Thu, 31 Jul 2025 20:44:18 GMT
ENV PHP_SHA256=388ee5fd111097e97bae439bff46aec4ea27f816d3f0c2cb5490a41410d44251
# Thu, 31 Jul 2025 20:44:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 31 Jul 2025 20:44:18 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 31 Jul 2025 20:44:18 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 31 Jul 2025 20:44:18 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 31 Jul 2025 20:44:18 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 31 Jul 2025 20:44:18 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 31 Jul 2025 20:44:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 31 Jul 2025 20:44:18 GMT
WORKDIR /var/www/html
# Thu, 31 Jul 2025 20:44:18 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 31 Jul 2025 20:44:18 GMT
STOPSIGNAL SIGQUIT
# Thu, 31 Jul 2025 20:44:18 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 31 Jul 2025 20:44:18 GMT
CMD ["php-fpm"]
# Tue, 19 Aug 2025 22:37:33 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 		zstd 	; # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		icu-dev 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libmemcached-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 		pecl install APCu-5.1.24; 	pecl install memcached-3.3.0; 	pecl install redis-6.1.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .joomla-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
VOLUME [/var/www/html]
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_VERSION=5.3.3
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_SHA512=efc0c5249758f1f7d9915992e01aa44203e86126c59c4c3adec8a7342aec132da2f5e10910fd7e2485ab8f58faa981de6be99cfe3c3b3f3c1e79e7d2d0321388
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.3.3/Joomla_5.3.3-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY makedb.php /makedb.php # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 22:37:33 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c293b040c7a67eeac13c53a522990f19f36e1b39939bdc55cbe7dbeefa2c82`  
		Last Modified: Wed, 16 Jul 2025 04:08:41 GMT  
		Size: 3.6 MB (3594168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4153c5fef55d21621d3f69b9fd9a25c43bda1995413d8f4dcacf545b0d8d2a0b`  
		Last Modified: Wed, 16 Jul 2025 04:08:41 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc109449c55003e3c992ac8133ad0a1b0794f6911cb2e1cc81ff0acc6e85daa1`  
		Last Modified: Wed, 16 Jul 2025 04:08:41 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a201b0a16aadc2a7c27ca0b373c85630463930fde99bd3c73f103ab676945d2`  
		Last Modified: Tue, 05 Aug 2025 12:57:01 GMT  
		Size: 12.6 MB (12599871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24220ce5963ab886efe9c3b3f66ba547029509a02a6800ed1f96dd054b509f70`  
		Last Modified: Tue, 05 Aug 2025 12:57:00 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f524b7a4013d49f1672e3def14da703786da1c7f1e3bfd8287705fa4b7f7d9`  
		Last Modified: Tue, 05 Aug 2025 13:51:36 GMT  
		Size: 12.8 MB (12760936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b19de0d3435de422114fee898a6b066f70ee28ecfd5f589638e2dd921f1b9e2`  
		Last Modified: Tue, 05 Aug 2025 13:51:38 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c7e96cf40ae551ebddd54c87ea502aef0be1094aafd9756757f0938d43bc2d6`  
		Last Modified: Tue, 05 Aug 2025 13:51:35 GMT  
		Size: 19.7 KB (19737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2fe0ec7d18971f49b97f267bc624a19192d37ac9a1a0211e5465c4fad6d585d`  
		Last Modified: Tue, 05 Aug 2025 13:51:35 GMT  
		Size: 19.7 KB (19736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f97d9049337329d8dd279f3212dfcc82651729e891bcffe27adcdcbebd199c`  
		Last Modified: Tue, 05 Aug 2025 13:51:37 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410683f45255c55b47dde54748d6970272fc7bbd096e11df02ffaceb906abe06`  
		Last Modified: Fri, 22 Aug 2025 04:29:09 GMT  
		Size: 28.2 MB (28207521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bd2c6007d90cb0c9be5491017e06e44fd8b1a09064f9000166b19d355d0204`  
		Last Modified: Fri, 22 Aug 2025 04:29:08 GMT  
		Size: 9.6 MB (9612974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5323bcea68f359a85a2cc9832abe3789f61e3abf8492139faf1bddf9d204de6f`  
		Last Modified: Fri, 22 Aug 2025 04:29:07 GMT  
		Size: 63.3 KB (63318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0f35ec94b9ab87d0ca336ceb306c7d52062aeaa8721b88cbdde0c9a0171615`  
		Last Modified: Fri, 22 Aug 2025 04:29:07 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e15096fc6c34d3d8821dc39fcb61b9f13ed2140709507e2f91581bbf65a34b`  
		Last Modified: Fri, 22 Aug 2025 10:44:47 GMT  
		Size: 25.1 MB (25118117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1518900b5ecb096efb28d8fd1ad18bd068196f82ab784c077c038278271bd22`  
		Last Modified: Fri, 22 Aug 2025 09:37:27 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c45251ca3daf8a7809976217276bd016a7fe11bef8ef0a1e3416fad65cb7d86`  
		Last Modified: Fri, 22 Aug 2025 09:39:28 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:5-php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull joomla@sha256:c3e56d609aa7a5b262db2abe6e8b3cce4e928aefbbd1043aa1d5f33b540c2f48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 KB (46134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bbebc73bb9f937d2deafe2935481350e59a1936934dd20b898e8a9a8d52f92e`

```dockerfile
```

-	Layers:
	-	`sha256:8d9370bc93e7fbfd42daa9d7d9f039024ab19f7e691d7f2693739ec8e3b5c7bc`  
		Last Modified: Fri, 22 Aug 2025 10:44:32 GMT  
		Size: 46.1 KB (46134 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:5-php8.3-fpm-alpine` - linux; s390x

```console
$ docker pull joomla@sha256:72732efc8de7ff89c00b2a4eb43bd20e6f8e126fe6730ed800bf211d664396e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.8 MB (97831886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96ce1ce7bec99cf7cec634c86de975de260830e223488f51bb54abf6327d146d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 31 Jul 2025 20:44:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 31 Jul 2025 20:44:18 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 31 Jul 2025 20:44:18 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 31 Jul 2025 20:44:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 31 Jul 2025 20:44:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 31 Jul 2025 20:44:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 31 Jul 2025 20:44:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 31 Jul 2025 20:44:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 31 Jul 2025 20:44:18 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 31 Jul 2025 20:44:18 GMT
ENV PHP_VERSION=8.3.24
# Thu, 31 Jul 2025 20:44:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.24.tar.xz.asc
# Thu, 31 Jul 2025 20:44:18 GMT
ENV PHP_SHA256=388ee5fd111097e97bae439bff46aec4ea27f816d3f0c2cb5490a41410d44251
# Thu, 31 Jul 2025 20:44:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 31 Jul 2025 20:44:18 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 31 Jul 2025 20:44:18 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 31 Jul 2025 20:44:18 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 31 Jul 2025 20:44:18 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 31 Jul 2025 20:44:18 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 31 Jul 2025 20:44:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 31 Jul 2025 20:44:18 GMT
WORKDIR /var/www/html
# Thu, 31 Jul 2025 20:44:18 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 31 Jul 2025 20:44:18 GMT
STOPSIGNAL SIGQUIT
# Thu, 31 Jul 2025 20:44:18 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 31 Jul 2025 20:44:18 GMT
CMD ["php-fpm"]
# Tue, 19 Aug 2025 22:37:33 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 		zstd 	; # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		icu-dev 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libmemcached-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 		pecl install APCu-5.1.24; 	pecl install memcached-3.3.0; 	pecl install redis-6.1.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .joomla-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
VOLUME [/var/www/html]
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_VERSION=5.3.3
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_SHA512=efc0c5249758f1f7d9915992e01aa44203e86126c59c4c3adec8a7342aec132da2f5e10910fd7e2485ab8f58faa981de6be99cfe3c3b3f3c1e79e7d2d0321388
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.3.3/Joomla_5.3.3-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY makedb.php /makedb.php # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 22:37:33 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d15b60ab2e403d45cb5d55d6ca4fec6dd4b321b0b3cbc9546510731b3196b34`  
		Last Modified: Mon, 04 Aug 2025 22:19:48 GMT  
		Size: 3.7 MB (3679854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f3a40b40361a6800f5592be421b6f972babf00ef4514af5b3cbbbecca685cb4`  
		Last Modified: Mon, 04 Aug 2025 22:19:47 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef30c8663103c30e07298c1dfa1db3aff21896305d5331f168c38f508379cdd6`  
		Last Modified: Mon, 04 Aug 2025 22:19:46 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2523afe7bac87b158b525d19c04b257f3c07e08691519ce8330dd437653643c2`  
		Last Modified: Mon, 04 Aug 2025 23:37:17 GMT  
		Size: 12.6 MB (12599878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78df3cd97ddbf126a4a6dfd5bf63960fc6ccf9adfdb9aa202edcc51b19c13c2`  
		Last Modified: Mon, 04 Aug 2025 23:37:15 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851854bea31942fe2c53199a441ecdcdab06a3e076fe408512317e67f5b4a771`  
		Last Modified: Mon, 04 Aug 2025 23:41:14 GMT  
		Size: 13.2 MB (13210677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b8257fc0b983043ce66078653ca13abb7f9a5fc1ab5a2c0c153f5a15001dd3`  
		Last Modified: Mon, 04 Aug 2025 23:41:12 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3938a4241c29aafc2b6a7e97e8b4850970dd6104375af53a1e3ed200d5eec5a`  
		Last Modified: Mon, 04 Aug 2025 23:41:13 GMT  
		Size: 19.7 KB (19745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78755911dfc20b138109d2303255ac2c16fb7ded0a53fe627fc8a508dbe07e8e`  
		Last Modified: Mon, 04 Aug 2025 23:41:13 GMT  
		Size: 19.7 KB (19742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f0c15c5819db3959fbf66a1cba899ae66e9869e1113c660149c00934a42fbe`  
		Last Modified: Mon, 04 Aug 2025 23:41:13 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ede16e579d4c3942bcc9ee532e4c26161bd4df12145c7b8eb8c3fa83969ce6f`  
		Last Modified: Tue, 19 Aug 2025 23:08:51 GMT  
		Size: 29.4 MB (29382921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057e2fb2c01f0f79a117a4d9bedb7f5d50797e0990e5afe6ff84931e6b36a9c4`  
		Last Modified: Tue, 19 Aug 2025 23:08:51 GMT  
		Size: 10.1 MB (10074318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3237dcf78a45744bfc510f3bf8ce9e0f11d86ea18976cabdba33f26e269a4506`  
		Last Modified: Tue, 19 Aug 2025 23:08:53 GMT  
		Size: 63.3 KB (63324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a274ee227cd1a0fe99312370a9df5d50cf1a920981ab7d74758724756a8baab`  
		Last Modified: Tue, 19 Aug 2025 23:08:53 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e22748a4d7191cb0618888e063182ff729aac76960c836553245a23cbe008ae`  
		Last Modified: Tue, 19 Aug 2025 23:39:37 GMT  
		Size: 25.1 MB (25118044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29a4eb3cad5d035faf62c8493c149ac52af820cacd2707d702c176a907f4b8e3`  
		Last Modified: Tue, 19 Aug 2025 23:39:34 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5530c4ad94b21ffc4899cc61fb669eaf50344f1592b1341940f01719d3e9c9cb`  
		Last Modified: Tue, 19 Aug 2025 23:39:34 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:5-php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull joomla@sha256:d2bf62f76529843031abd08f3f46ae88534badf8104f927216bf35b0664592bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 KB (46088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3daa597eac1948a40082c86cb55023e764b953fcfb384c72c3835bc005ab828`

```dockerfile
```

-	Layers:
	-	`sha256:25f5410e9afec47795ae4ce2f64dbe6e9bc287d9b80c196eb3d40be05d4ac660`  
		Last Modified: Wed, 20 Aug 2025 01:48:42 GMT  
		Size: 46.1 KB (46088 bytes)  
		MIME: application/vnd.in-toto+json
