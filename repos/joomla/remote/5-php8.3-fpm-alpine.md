## `joomla:5-php8.3-fpm-alpine`

```console
$ docker pull joomla@sha256:de1a8ea2b21a0b164f8f498202ef22665b7ace22527eea9b81919c306f57f6af
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
$ docker pull joomla@sha256:f7425d1d152cc4189ae22c5505b6fb023e4a35e012f5a33f74fd0c32e6cc4594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.7 MB (100719461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40e44d5f409d2988ed796f6e4cc0e8e10a65b19bfff25d9ed2301fdcf00d1694`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:16:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 16 Jun 2026 00:16:18 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 16 Jun 2026 00:16:18 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 16 Jun 2026 00:16:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 16 Jun 2026 00:16:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 16 Jun 2026 00:16:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 16 Jun 2026 00:16:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 16 Jun 2026 00:16:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 16 Jun 2026 00:16:18 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 16 Jun 2026 00:16:18 GMT
ENV PHP_VERSION=8.3.31
# Tue, 16 Jun 2026 00:16:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Tue, 16 Jun 2026 00:16:18 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Tue, 16 Jun 2026 00:16:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Tue, 16 Jun 2026 00:16:21 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:19:04 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 16 Jun 2026 00:19:04 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:19:05 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 16 Jun 2026 00:19:05 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 16 Jun 2026 00:19:05 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 16 Jun 2026 00:19:05 GMT
WORKDIR /var/www/html
# Tue, 16 Jun 2026 00:19:05 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 16 Jun 2026 00:19:05 GMT
STOPSIGNAL SIGQUIT
# Tue, 16 Jun 2026 00:19:05 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 16 Jun 2026 00:19:05 GMT
CMD ["php-fpm"]
# Tue, 16 Jun 2026 01:17:37 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 16 Jun 2026 01:17:37 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 16 Jun 2026 01:17:37 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 		zstd 	; # buildkit
# Tue, 16 Jun 2026 01:19:13 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		icu-dev 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libmemcached-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 		pecl install APCu-5.1.27; 	pecl install memcached-3.4.0; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .joomla-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 16 Jun 2026 01:19:14 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 16 Jun 2026 01:19:14 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 16 Jun 2026 01:19:14 GMT
VOLUME [/var/www/html]
# Tue, 16 Jun 2026 01:19:14 GMT
ENV JOOMLA_VERSION=5.4.6
# Tue, 16 Jun 2026 01:19:14 GMT
ENV JOOMLA_SHA512=d4198b32a37cea890b24ab219b7d267e6a6df3373530d5e76eb7f4563868ef6caebefa7a2b9290065146ef733db2b0becc18d69f291730c767a25aa158cb9c16
# Tue, 16 Jun 2026 01:19:15 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.4.6/Joomla_5.4.6-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Tue, 16 Jun 2026 01:19:15 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 16 Jun 2026 01:19:15 GMT
COPY makedb.php /makedb.php # buildkit
# Tue, 16 Jun 2026 01:19:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Jun 2026 01:19:15 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5dd4732e2b99153a6d793672259fe16511026394361d9a4546a505fc892ec26`  
		Last Modified: Tue, 16 Jun 2026 00:19:12 GMT  
		Size: 3.5 MB (3466800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:564766333e2350c3f785f44564469ebc099dcb0871eb5ff8d9f1174ae9416f39`  
		Last Modified: Tue, 16 Jun 2026 00:19:12 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7470fb2f68ecb33e0cc428289222713040bc6a0fb07a219ec29b9be9f39985bf`  
		Last Modified: Tue, 16 Jun 2026 00:19:12 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c64268d00ab62c4f8906301775f10530956c2d93f9614fc8043f56a19fd3ed`  
		Last Modified: Tue, 16 Jun 2026 00:19:12 GMT  
		Size: 12.6 MB (12626290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8667346ced391e67f639e71ec1fdd3e4f2d5f92304b705cf7502c9aefad6b2aa`  
		Last Modified: Tue, 16 Jun 2026 00:19:13 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9015c0b720110c5cb9b008ee9ca2a43a0522c253d5bb3eaa78678d300b17f1`  
		Last Modified: Tue, 16 Jun 2026 00:19:13 GMT  
		Size: 13.4 MB (13416525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f64f2f99cedc2c8912f0a823a27dcca2cac8ebd8b3fb87bccde22b87b17710c9`  
		Last Modified: Tue, 16 Jun 2026 00:19:14 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:915ffc2502405f650a72b28a68df9f73fe86533e60bb70a5dec1ca9a824d3c12`  
		Last Modified: Tue, 16 Jun 2026 00:19:14 GMT  
		Size: 22.4 KB (22352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ae65494ca8528d38cf4c896b8b4810ea8c9a4a469f902e965bf38edf18ca5e`  
		Last Modified: Tue, 16 Jun 2026 00:19:15 GMT  
		Size: 22.4 KB (22358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ec4a172ae0f050e31e9dcc58b400328245442fd96bba8903ce25ba2e765aa0`  
		Last Modified: Tue, 16 Jun 2026 00:19:15 GMT  
		Size: 9.2 KB (9250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce55c0ab743286fa7bf111559597f12082bcd551bd169ec9f8765aea07146566`  
		Last Modified: Tue, 16 Jun 2026 01:19:23 GMT  
		Size: 32.9 MB (32935930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299867d796905f7cc261631df87cb432a2b69daac02bde0bbb39c30c64431c1f`  
		Last Modified: Tue, 16 Jun 2026 01:19:23 GMT  
		Size: 7.0 MB (6978187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0259704ec71d0b262f844b282cec0ca27b20dc27cb28b9b2b55e6e2f96990f`  
		Last Modified: Tue, 16 Jun 2026 01:19:22 GMT  
		Size: 72.0 KB (72034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1205bbebb67d8e2529b2fcc440518b4b35b617360292c0841ad06d7393e74f89`  
		Last Modified: Tue, 16 Jun 2026 01:19:22 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eda43358a86d08114437146c33784b1b437ea43d302cf154a4b4f1504fc0a3c`  
		Last Modified: Tue, 16 Jun 2026 01:19:24 GMT  
		Size: 27.3 MB (27314116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb19dc824e28ddbb70b0c40b489b090709166306fa5913e5ea04203f15a8996`  
		Last Modified: Tue, 16 Jun 2026 01:19:24 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01cadef8786260c1c57223f3c3f2a630183e3bde389af4f0e9fbdee1aa15da78`  
		Last Modified: Tue, 16 Jun 2026 01:19:24 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:5-php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull joomla@sha256:af3fe821c396d11f01e437f39a13d5acf29f977c69c41ffaa2b27f6d9e1116cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 KB (45715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb810f42388aeec46e2059361b54a6929972751ca24413012d1df2d12e80752`

```dockerfile
```

-	Layers:
	-	`sha256:deee62813e68d9f0412b7bb56ec9b9b82ab1387544b493b960217fd07c57c716`  
		Last Modified: Tue, 16 Jun 2026 01:19:22 GMT  
		Size: 45.7 KB (45715 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:5-php8.3-fpm-alpine` - linux; arm variant v6

```console
$ docker pull joomla@sha256:9a37e98852af5883c825f015c56c738cf7a28c347839ab007a2e714a7a958ce9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.7 MB (95725196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75aed22255e9d02d88af747d4fa3bd10112782f0aba989bba4bae2418c0924f6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:25 GMT
ADD alpine-minirootfs-3.24.1-armhf.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:25 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:16:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 16 Jun 2026 00:16:34 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 16 Jun 2026 00:16:34 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 16 Jun 2026 00:16:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 16 Jun 2026 00:16:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 16 Jun 2026 00:16:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 16 Jun 2026 00:16:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 16 Jun 2026 00:16:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 16 Jun 2026 00:16:34 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 16 Jun 2026 00:16:34 GMT
ENV PHP_VERSION=8.3.31
# Tue, 16 Jun 2026 00:16:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Tue, 16 Jun 2026 00:16:34 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Tue, 16 Jun 2026 00:19:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Tue, 16 Jun 2026 00:19:50 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:22:29 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 16 Jun 2026 00:22:29 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:22:30 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 16 Jun 2026 00:22:31 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 16 Jun 2026 00:22:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 16 Jun 2026 00:22:31 GMT
WORKDIR /var/www/html
# Tue, 16 Jun 2026 00:22:31 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 16 Jun 2026 00:22:31 GMT
STOPSIGNAL SIGQUIT
# Tue, 16 Jun 2026 00:22:31 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 16 Jun 2026 00:22:31 GMT
CMD ["php-fpm"]
# Tue, 16 Jun 2026 01:22:26 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 16 Jun 2026 01:22:26 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 16 Jun 2026 01:22:26 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 		zstd 	; # buildkit
# Tue, 16 Jun 2026 01:24:52 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		icu-dev 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libmemcached-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 		pecl install APCu-5.1.27; 	pecl install memcached-3.4.0; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .joomla-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 16 Jun 2026 01:24:53 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 16 Jun 2026 01:24:53 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 16 Jun 2026 01:24:53 GMT
VOLUME [/var/www/html]
# Tue, 16 Jun 2026 01:24:53 GMT
ENV JOOMLA_VERSION=5.4.6
# Tue, 16 Jun 2026 01:24:53 GMT
ENV JOOMLA_SHA512=d4198b32a37cea890b24ab219b7d267e6a6df3373530d5e76eb7f4563868ef6caebefa7a2b9290065146ef733db2b0becc18d69f291730c767a25aa158cb9c16
# Tue, 16 Jun 2026 01:24:55 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.4.6/Joomla_5.4.6-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Tue, 16 Jun 2026 01:24:55 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 16 Jun 2026 01:24:55 GMT
COPY makedb.php /makedb.php # buildkit
# Tue, 16 Jun 2026 01:24:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Jun 2026 01:24:55 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:3c4836a46d600cfe9a422adf7a80205cb534097e6213325e0176c51f6e5cc02e`  
		Last Modified: Sun, 14 Jun 2026 06:44:57 GMT  
		Size: 3.6 MB (3553450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5230d03921a527b9f279c604c71dc4db15ab131e00ad4ac831317aed9b8592`  
		Last Modified: Tue, 16 Jun 2026 00:19:38 GMT  
		Size: 3.4 MB (3416654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b528158f29bd5ca9983f791571ec7eac252b82c365b58879ae3bd2ff2e48c2f4`  
		Last Modified: Tue, 16 Jun 2026 00:19:38 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8af6fa12a7122bd4001e6224682f17ade9530bc74e05c2722c1ed4a37478318`  
		Last Modified: Tue, 16 Jun 2026 00:19:38 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:668f255cd4d090b89df03b29a76d5c4a5a7acc200f994a634add4c4a079f0851`  
		Last Modified: Tue, 16 Jun 2026 00:22:37 GMT  
		Size: 12.6 MB (12626294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0bd5987c0d80157b12468800d25035c39c7826b125856e5ded0d1094e531d96`  
		Last Modified: Tue, 16 Jun 2026 00:22:36 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b533baab338501d966ffc88ae6c9bf5d223475a1004e418a5b0c11a219245f9`  
		Last Modified: Tue, 16 Jun 2026 00:22:36 GMT  
		Size: 12.2 MB (12159505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe05818d056f3a4c55f207d013300f36d54389bd56430b34a135293b312ace8`  
		Last Modified: Tue, 16 Jun 2026 00:22:36 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cfe9b3ff027b1cb06a1748f0d17f739f6d7c848986665e2050299981e13a21f`  
		Last Modified: Tue, 16 Jun 2026 00:22:37 GMT  
		Size: 22.1 KB (22138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d24d9c21c2e0d79d7af2bb090baf0a2552eca490c70f22c4b6da72d749f9e79`  
		Last Modified: Tue, 16 Jun 2026 00:22:37 GMT  
		Size: 22.2 KB (22155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b967eb9014ecd390e52a6fae91486bdef2eb91ac554af8c4a70b1df24ee1a0`  
		Last Modified: Tue, 16 Jun 2026 00:22:38 GMT  
		Size: 9.3 KB (9251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89efc16d85b33b7e0ad5a53bdfd111ecb6cf1ec3ecb72b5d9ffbde6c13066a06`  
		Last Modified: Tue, 16 Jun 2026 01:25:03 GMT  
		Size: 29.8 MB (29839976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a0473a68656fc9812e24118e3bd8a4c64e657c69573ae46a61b946e38db5b5`  
		Last Modified: Tue, 16 Jun 2026 01:25:02 GMT  
		Size: 6.7 MB (6680350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82aa36542d34a1cc3bdb0637f11464870ab27c8a4c888884684dac9d2b89d863`  
		Last Modified: Tue, 16 Jun 2026 01:25:02 GMT  
		Size: 72.0 KB (72030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b12045ebc059f1abffce935f38e303f707f2f665b6ddf9674fcd684bfcf4baa`  
		Last Modified: Tue, 16 Jun 2026 01:25:02 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a4c222ad12192d24115734e47aa4514fc3e4a6d91670eba812131eba4d22fa`  
		Last Modified: Tue, 16 Jun 2026 01:25:03 GMT  
		Size: 27.3 MB (27314156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd615e8138e5bd4c81ad05119959e06d9cac80233a0e9bc99931b0d34096c10`  
		Last Modified: Tue, 16 Jun 2026 01:25:02 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9f427b95b8d50fe076c7a11cb42b771ef420aa57c5b114d84df8df261b4331f`  
		Last Modified: Tue, 16 Jun 2026 01:25:02 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:5-php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull joomla@sha256:06ba506c952413ddb959cd488d0e1195864d674bece3bd845552a8a1d3215488
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.8 KB (45839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c28da69762d7f80d7d980dde9ed54e17cb6ead59d6627ed8cf6c5a5ed51f4cde`

```dockerfile
```

-	Layers:
	-	`sha256:4d205e3fc8ff121b73ba6d414cb809163197539dc76c78cf40af1da4eba0a084`  
		Last Modified: Tue, 16 Jun 2026 01:25:01 GMT  
		Size: 45.8 KB (45839 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:5-php8.3-fpm-alpine` - linux; arm variant v7

```console
$ docker pull joomla@sha256:a3e8c26f7fc623e82da4aea390116e37fd7cebe3d67615b1ec8e19f9c0440453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 MB (92813600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c87cf5fa3b595850d1fa01f2b45b8de723b896701f3100be10f22b25b59946b7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:26 GMT
ADD alpine-minirootfs-3.24.1-armv7.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:26 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:22:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 16 Jun 2026 00:22:16 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 16 Jun 2026 00:22:16 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 16 Jun 2026 00:22:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 16 Jun 2026 00:22:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 16 Jun 2026 00:22:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 16 Jun 2026 00:22:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 16 Jun 2026 00:22:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 16 Jun 2026 00:22:16 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 16 Jun 2026 00:22:16 GMT
ENV PHP_VERSION=8.3.31
# Tue, 16 Jun 2026 00:22:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Tue, 16 Jun 2026 00:22:16 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Tue, 16 Jun 2026 00:22:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Tue, 16 Jun 2026 00:22:19 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:24:59 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 16 Jun 2026 00:24:59 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:25:00 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 16 Jun 2026 00:25:01 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 16 Jun 2026 00:25:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 16 Jun 2026 00:25:01 GMT
WORKDIR /var/www/html
# Tue, 16 Jun 2026 00:25:01 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 16 Jun 2026 00:25:01 GMT
STOPSIGNAL SIGQUIT
# Tue, 16 Jun 2026 00:25:01 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 16 Jun 2026 00:25:01 GMT
CMD ["php-fpm"]
# Tue, 16 Jun 2026 01:22:25 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 16 Jun 2026 01:22:25 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 16 Jun 2026 01:22:25 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 		zstd 	; # buildkit
# Tue, 16 Jun 2026 01:24:51 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		icu-dev 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libmemcached-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 		pecl install APCu-5.1.27; 	pecl install memcached-3.4.0; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .joomla-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 16 Jun 2026 01:24:52 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 16 Jun 2026 01:24:52 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 16 Jun 2026 01:24:52 GMT
VOLUME [/var/www/html]
# Tue, 16 Jun 2026 01:24:52 GMT
ENV JOOMLA_VERSION=5.4.6
# Tue, 16 Jun 2026 01:24:52 GMT
ENV JOOMLA_SHA512=d4198b32a37cea890b24ab219b7d267e6a6df3373530d5e76eb7f4563868ef6caebefa7a2b9290065146ef733db2b0becc18d69f291730c767a25aa158cb9c16
# Tue, 16 Jun 2026 01:24:53 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.4.6/Joomla_5.4.6-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Tue, 16 Jun 2026 01:24:53 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 16 Jun 2026 01:24:53 GMT
COPY makedb.php /makedb.php # buildkit
# Tue, 16 Jun 2026 01:24:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Jun 2026 01:24:53 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:bc03a9e5b4dd452551f246e199537fe7afc1765f53f510bc81d26df9845e4008`  
		Last Modified: Sun, 14 Jun 2026 06:45:22 GMT  
		Size: 3.3 MB (3260615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642d1d207c87ecb8483478cebba55e69d647f6ecedfc0da267d886cd8a000606`  
		Last Modified: Tue, 16 Jun 2026 00:25:07 GMT  
		Size: 3.2 MB (3233760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1c123bfd6be24a667b3ccaccd14f406e2226ce5ab8c9346189dd55da240b2e`  
		Last Modified: Tue, 16 Jun 2026 00:25:07 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e30dfd0f3a4543dd39f5a397924c79e7a82f96e265c437df4723245e323c12d`  
		Last Modified: Tue, 16 Jun 2026 00:25:07 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4864a0c79d98806c1f9bbe2d7e6a9918ddf041c1d4045e7783b0a7c336b04a1`  
		Last Modified: Tue, 16 Jun 2026 00:25:07 GMT  
		Size: 12.6 MB (12626306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e8df0c609282ee3a8107f5ad60ddd209b59614155ef0d3cc54ea86e17383ba`  
		Last Modified: Tue, 16 Jun 2026 00:25:08 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff4689b77e96c6d5c2efc0bf61e8ead5fc85ceca449788503b307b6af2163680`  
		Last Modified: Tue, 16 Jun 2026 00:25:09 GMT  
		Size: 11.4 MB (11444360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c20a9f88ff092918443f6388d2a059e84be9fe5966c61570ab9fdb0e2d2802`  
		Last Modified: Tue, 16 Jun 2026 00:25:09 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16d4624fa9ed346cf31dd73da2c70202d854ddfb30f63b4c3f464e9677e08de`  
		Last Modified: Tue, 16 Jun 2026 00:25:09 GMT  
		Size: 22.1 KB (22141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f618452ebb0124c504dd117a4b317514bcb0bc9e2ee8b43564ebb76cb45234e3`  
		Last Modified: Tue, 16 Jun 2026 00:25:10 GMT  
		Size: 22.2 KB (22153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c285222c8cb5e18671f79f7007ae11796c2e2832df93a20ff5dde9f04bd54852`  
		Last Modified: Tue, 16 Jun 2026 00:25:10 GMT  
		Size: 9.2 KB (9250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:084580e6db58c9f388a3c10b90ce8f4f0959262cce6255ec831fc4ba538a6a30`  
		Last Modified: Tue, 16 Jun 2026 01:25:01 GMT  
		Size: 28.1 MB (28089140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6980e5f582f236dcc6cd4b04d905689cd301d789bb62bda3997ebf8b73170f`  
		Last Modified: Tue, 16 Jun 2026 01:25:01 GMT  
		Size: 6.7 MB (6710243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f2475952989d9cda4be00a4922df557d49ef0c3ca173607571262d8b1b81e5`  
		Last Modified: Tue, 16 Jun 2026 01:25:00 GMT  
		Size: 72.0 KB (72047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3637c88c24203062e30451ebaef8c1903deba677214b700032d21104e4e2318`  
		Last Modified: Tue, 16 Jun 2026 01:25:00 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a9db7c238600b7bcd86328d8c119b0b82ba8b9d01d0d12c6b3ad0e7369a8ca`  
		Last Modified: Tue, 16 Jun 2026 01:25:02 GMT  
		Size: 27.3 MB (27314349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd615e8138e5bd4c81ad05119959e06d9cac80233a0e9bc99931b0d34096c10`  
		Last Modified: Tue, 16 Jun 2026 01:25:02 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9f427b95b8d50fe076c7a11cb42b771ef420aa57c5b114d84df8df261b4331f`  
		Last Modified: Tue, 16 Jun 2026 01:25:02 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:5-php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull joomla@sha256:8f1a156a34c60254058f27617932536292a8423630a60e070e7ff3c67a343aac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.8 KB (45835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18347d4888d8229a7bd40c72307e03c239c232c7393f84294a0c043a68e394df`

```dockerfile
```

-	Layers:
	-	`sha256:ab9b418406c91de4c530013cc0dc1b955dcfb6002499f435a144b57e524904e0`  
		Last Modified: Tue, 16 Jun 2026 01:25:00 GMT  
		Size: 45.8 KB (45835 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:5-php8.3-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull joomla@sha256:e0470606f8a379891c21df190858642d53f1a5e7fa34eacfd5ef63b48dae14a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.5 MB (100511119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4753cf1605b1a4b8e3317e03e010550edaab0902519908c898a7b308dd455d8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:13:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 16 Jun 2026 00:13:45 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 16 Jun 2026 00:13:45 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 16 Jun 2026 00:13:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 16 Jun 2026 00:13:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 16 Jun 2026 00:13:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 16 Jun 2026 00:13:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 16 Jun 2026 00:13:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 16 Jun 2026 00:13:45 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 16 Jun 2026 00:13:45 GMT
ENV PHP_VERSION=8.3.31
# Tue, 16 Jun 2026 00:13:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Tue, 16 Jun 2026 00:13:45 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Tue, 16 Jun 2026 00:13:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Tue, 16 Jun 2026 00:13:54 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:18:26 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 16 Jun 2026 00:18:26 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:18:26 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 16 Jun 2026 00:18:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 16 Jun 2026 00:18:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 16 Jun 2026 00:18:27 GMT
WORKDIR /var/www/html
# Tue, 16 Jun 2026 00:18:27 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 16 Jun 2026 00:18:27 GMT
STOPSIGNAL SIGQUIT
# Tue, 16 Jun 2026 00:18:27 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 16 Jun 2026 00:18:27 GMT
CMD ["php-fpm"]
# Tue, 16 Jun 2026 01:18:40 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 16 Jun 2026 01:18:40 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 16 Jun 2026 01:18:40 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 		zstd 	; # buildkit
# Tue, 16 Jun 2026 01:20:41 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		icu-dev 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libmemcached-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 		pecl install APCu-5.1.27; 	pecl install memcached-3.4.0; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .joomla-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 16 Jun 2026 01:20:42 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 16 Jun 2026 01:20:42 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 16 Jun 2026 01:20:42 GMT
VOLUME [/var/www/html]
# Tue, 16 Jun 2026 01:20:42 GMT
ENV JOOMLA_VERSION=5.4.6
# Tue, 16 Jun 2026 01:20:42 GMT
ENV JOOMLA_SHA512=d4198b32a37cea890b24ab219b7d267e6a6df3373530d5e76eb7f4563868ef6caebefa7a2b9290065146ef733db2b0becc18d69f291730c767a25aa158cb9c16
# Tue, 16 Jun 2026 01:20:43 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.4.6/Joomla_5.4.6-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Tue, 16 Jun 2026 01:20:43 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 16 Jun 2026 01:20:43 GMT
COPY makedb.php /makedb.php # buildkit
# Tue, 16 Jun 2026 01:20:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Jun 2026 01:20:43 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20927fc874f68b1dfb3247c97d1e06a8d2fd122901377db2698427184e8b3740`  
		Last Modified: Tue, 16 Jun 2026 00:18:34 GMT  
		Size: 3.5 MB (3475810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293370315a62e3dcf82832aa1d28a17337a85a0b63cd5ed39705638e6ad97cab`  
		Last Modified: Tue, 16 Jun 2026 00:18:34 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b508e52c244a07c7e9d094ee31366105e64fc09fd6b131c52c05a7553b3c09`  
		Last Modified: Tue, 16 Jun 2026 00:18:34 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a4c038ac2c897f69ac595a02197e5686e28c2a8d12f85998f1e2b17bbf9a4e`  
		Last Modified: Tue, 16 Jun 2026 00:18:35 GMT  
		Size: 12.6 MB (12626290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0387296813e0cc18bdbc9d044bfc24bdbb69c3336a1efc47c2bca2e2f2fab8`  
		Last Modified: Tue, 16 Jun 2026 00:18:36 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d548ea984a73d437bfb41fed9ed29f55a7a3ef04990d7f1e924dadbf48216efe`  
		Last Modified: Tue, 16 Jun 2026 00:18:36 GMT  
		Size: 13.3 MB (13319719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f72b5cf36b8130c8cef1124ee9f04692ffebc22c09aab85a5cef7179360dc50`  
		Last Modified: Tue, 16 Jun 2026 00:18:36 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6d72804eec9407842761d3de63890c73006e23a639c2bb88f26669e3886537`  
		Last Modified: Tue, 16 Jun 2026 00:18:36 GMT  
		Size: 22.2 KB (22155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8783d73bb465c7c28b5cb490d326631de541ad1b8a5acb17cefc380250af989a`  
		Last Modified: Tue, 16 Jun 2026 00:18:37 GMT  
		Size: 22.2 KB (22178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e723df7026a14767594d3fa1282af584dce55902e0e31ac25c97347545487ad5`  
		Last Modified: Tue, 16 Jun 2026 00:18:37 GMT  
		Size: 9.3 KB (9251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93bb02743f3a0ea8e87710ae02a2f5a41726e87aac733d916a30058a6b9e4ab`  
		Last Modified: Tue, 16 Jun 2026 01:20:51 GMT  
		Size: 32.6 MB (32552231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59a87cf8da44c55ac13bf3ae64c8dea1ef3a5be81126b398be0310d812623fc3`  
		Last Modified: Tue, 16 Jun 2026 01:20:50 GMT  
		Size: 6.9 MB (6904982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce44e846292e25e8a5c6d6c76de342c05c818085832d109ccab25e50f70d33eb`  
		Last Modified: Tue, 16 Jun 2026 01:20:50 GMT  
		Size: 72.0 KB (72028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c658b7f58dfe25f02482bd2599a50aabcd2340c1fdc46575a108e01c1e34c026`  
		Last Modified: Tue, 16 Jun 2026 01:20:50 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92813e0676a4a130012da984a07cbf417d41dd7dfd0672a132ab10f308b85346`  
		Last Modified: Tue, 16 Jun 2026 01:20:52 GMT  
		Size: 27.3 MB (27314212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82e1bdddc9fa304e7a9202c09d404babe731e781c8f07449b24c5afdc75df0e`  
		Last Modified: Tue, 16 Jun 2026 01:20:52 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f85f5ecff79b5e239ccee67b36be8d5b7ffb02d329c0ee3f96a6ae3cdd82cd7`  
		Last Modified: Tue, 16 Jun 2026 01:20:52 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:5-php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull joomla@sha256:8dc332aa3fca666914ac76a9cf5ed0e79057ebb4ec3dbb8d6888ec557fc2202a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 KB (45866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63747b4ed1657b0ea0ce4e2ef8c5b2a36ede4c6aea372812aa81a28c7fae3114`

```dockerfile
```

-	Layers:
	-	`sha256:4f0a83e362fabd8164dc71eabbf065c65b979fc230fd1ec2fee51d40cf1a7f07`  
		Last Modified: Tue, 16 Jun 2026 01:20:50 GMT  
		Size: 45.9 KB (45866 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:5-php8.3-fpm-alpine` - linux; 386

```console
$ docker pull joomla@sha256:07414dd01648a27c544d76e720eaabe01798400526929f8912c64703928e9017
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.4 MB (101381445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5be0c92a32d2fb2731f5bcd30ab7f6f6fff8ca85303a231e1e98dbd21e1e1281`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:19 GMT
ADD alpine-minirootfs-3.24.1-x86.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:19 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:15:19 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 16 Jun 2026 00:15:19 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 16 Jun 2026 00:15:19 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 16 Jun 2026 00:15:19 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 16 Jun 2026 00:15:19 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 16 Jun 2026 00:15:19 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 16 Jun 2026 00:15:19 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 16 Jun 2026 00:15:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 16 Jun 2026 00:15:19 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 16 Jun 2026 00:15:19 GMT
ENV PHP_VERSION=8.3.31
# Tue, 16 Jun 2026 00:15:19 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Tue, 16 Jun 2026 00:15:19 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Tue, 16 Jun 2026 00:15:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Tue, 16 Jun 2026 00:15:22 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 16 Jun 2026 00:18:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:18:23 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 16 Jun 2026 00:18:23 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 16 Jun 2026 00:18:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 16 Jun 2026 00:18:23 GMT
WORKDIR /var/www/html
# Tue, 16 Jun 2026 00:18:23 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 16 Jun 2026 00:18:23 GMT
STOPSIGNAL SIGQUIT
# Tue, 16 Jun 2026 00:18:23 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 16 Jun 2026 00:18:23 GMT
CMD ["php-fpm"]
# Tue, 16 Jun 2026 01:14:29 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 16 Jun 2026 01:14:29 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 16 Jun 2026 01:14:29 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 		zstd 	; # buildkit
# Tue, 16 Jun 2026 01:16:18 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		icu-dev 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libmemcached-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 		pecl install APCu-5.1.27; 	pecl install memcached-3.4.0; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .joomla-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 16 Jun 2026 01:16:19 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 16 Jun 2026 01:16:19 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 16 Jun 2026 01:16:19 GMT
VOLUME [/var/www/html]
# Tue, 16 Jun 2026 01:16:19 GMT
ENV JOOMLA_VERSION=5.4.6
# Tue, 16 Jun 2026 01:16:19 GMT
ENV JOOMLA_SHA512=d4198b32a37cea890b24ab219b7d267e6a6df3373530d5e76eb7f4563868ef6caebefa7a2b9290065146ef733db2b0becc18d69f291730c767a25aa158cb9c16
# Tue, 16 Jun 2026 01:16:21 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.4.6/Joomla_5.4.6-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Tue, 16 Jun 2026 01:16:21 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 16 Jun 2026 01:16:21 GMT
COPY makedb.php /makedb.php # buildkit
# Tue, 16 Jun 2026 01:16:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Jun 2026 01:16:21 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:f86df9d778509895efbf9363d8fcb0cbe0b772de536c7218e4c4c947f0be879f`  
		Last Modified: Sun, 14 Jun 2026 06:45:46 GMT  
		Size: 3.7 MB (3670141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9a1f87309f760a910a5f3b278d7e02cc9e41747bd6c7da50de79c37774b6ce`  
		Last Modified: Tue, 16 Jun 2026 00:18:30 GMT  
		Size: 3.5 MB (3497309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c13d3f542289e7019282f796435ff5feb38ef94d23d9b02eee2f64fbf0ba597`  
		Last Modified: Tue, 16 Jun 2026 00:18:30 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94c86cc39b7afbf4033178653190199e70655723b408046cd102cb5b26e6654e`  
		Last Modified: Tue, 16 Jun 2026 00:18:30 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193d558fad92af7cfba37bbb4d56f2b571ac60036f2046a008dcd58af1429bbb`  
		Last Modified: Tue, 16 Jun 2026 00:18:30 GMT  
		Size: 12.6 MB (12626282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e9deff40ff2ca9d43487cbbee0f4790fb1f54039f2f02b11c40bebdb9bf10a9`  
		Last Modified: Tue, 16 Jun 2026 00:18:31 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b896f0235e2baf509bd727289de262d42e04c3ae687e43d227ad06ed065b4c`  
		Last Modified: Tue, 16 Jun 2026 00:18:32 GMT  
		Size: 13.7 MB (13690201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55251fb34d4af4e5cb217d212ff8bbe79383d88299bbbd9d1fb704123ee2b627`  
		Last Modified: Tue, 16 Jun 2026 00:18:32 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f82ae9a228fc1947483e8ea0561e89fd09612aa6d5430e7c46c6a0ea885e57`  
		Last Modified: Tue, 16 Jun 2026 00:18:32 GMT  
		Size: 22.4 KB (22359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b7adc858c09e3ea06c23f6ffcae3eb1d73b8e22d73e517968a0f13a36dd972`  
		Last Modified: Tue, 16 Jun 2026 00:18:33 GMT  
		Size: 22.4 KB (22369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da74e87d8deff5e4a2df18810d36366b2ad620852aeac3b6e1d98ca55b8d2f97`  
		Last Modified: Tue, 16 Jun 2026 00:18:33 GMT  
		Size: 9.2 KB (9248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84ed6f1938bc1228231d6cea9f79cf267ce3adf10111caa9b37c2fac15ec401`  
		Last Modified: Tue, 16 Jun 2026 01:16:29 GMT  
		Size: 33.4 MB (33362513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4865086025a9d2c5109596b601bc86230e8a9063b8e23afbd4964d2bf2972b1`  
		Last Modified: Tue, 16 Jun 2026 01:16:29 GMT  
		Size: 7.1 MB (7085483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17fe9f2b0b41524d936f84b85af92f0e54f79be9ba31ded420bff7fa10f39fcc`  
		Last Modified: Tue, 16 Jun 2026 01:16:28 GMT  
		Size: 72.0 KB (71999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2b68176d761feb236f3a1521feaacb9d0b259fd569d5baa261be8c2c67b8fc`  
		Last Modified: Tue, 16 Jun 2026 01:16:29 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3902ab13593f93c6538b46388650c5aa73a6df161a960bcf1246ff9c91fdee1`  
		Last Modified: Tue, 16 Jun 2026 01:16:30 GMT  
		Size: 27.3 MB (27314317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b726f5c4d7877983fe9f1b60b46e8afc94330621e6b5705d832e1817ef9d7a`  
		Last Modified: Tue, 16 Jun 2026 01:16:30 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2215e4fb817062c70f50f58811ee4401f9842d69f15c9a7ff313eb055c7e2647`  
		Last Modified: Tue, 16 Jun 2026 01:16:30 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:5-php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull joomla@sha256:514d44f7d6c8338b262d33a44f58c6a1a95a1b3b40f02edf025ba5ff5a9ef264
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 KB (45680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdf4cc9d553998e43d9862b4d09301145186548e1038741af74038debe9e2b19`

```dockerfile
```

-	Layers:
	-	`sha256:8dabcbff37eec71192ce8260e28501a74612342a0f4474ccdf567d9b9239c5cd`  
		Last Modified: Tue, 16 Jun 2026 01:16:28 GMT  
		Size: 45.7 KB (45680 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:5-php8.3-fpm-alpine` - linux; ppc64le

```console
$ docker pull joomla@sha256:156d6970fae7383b5af629484d5e4a67b5da170dc804793dac8854d5b869e3b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.9 MB (102887643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d517742bcf6d8130a2f44e25bd923375a3bf81b16f354676366eb4367a56e97`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:15 GMT
ADD alpine-minirootfs-3.24.1-ppc64le.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:15 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:16:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 16 Jun 2026 00:16:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 16 Jun 2026 00:16:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 16 Jun 2026 00:16:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 16 Jun 2026 00:16:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 16 Jun 2026 00:16:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 16 Jun 2026 00:16:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 16 Jun 2026 00:16:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 16 Jun 2026 00:16:59 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 16 Jun 2026 00:16:59 GMT
ENV PHP_VERSION=8.3.31
# Tue, 16 Jun 2026 00:16:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Tue, 16 Jun 2026 00:16:59 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Tue, 16 Jun 2026 00:30:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Tue, 16 Jun 2026 00:30:57 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:36:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 16 Jun 2026 00:36:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:36:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 16 Jun 2026 00:36:17 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 16 Jun 2026 00:36:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 16 Jun 2026 00:36:17 GMT
WORKDIR /var/www/html
# Tue, 16 Jun 2026 00:36:17 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 16 Jun 2026 00:36:17 GMT
STOPSIGNAL SIGQUIT
# Tue, 16 Jun 2026 00:36:17 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 16 Jun 2026 00:36:17 GMT
CMD ["php-fpm"]
# Tue, 16 Jun 2026 01:34:51 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 16 Jun 2026 01:34:51 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 16 Jun 2026 01:34:51 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 		zstd 	; # buildkit
# Tue, 16 Jun 2026 01:38:33 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		icu-dev 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libmemcached-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 		pecl install APCu-5.1.27; 	pecl install memcached-3.4.0; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .joomla-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 16 Jun 2026 01:38:35 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 16 Jun 2026 01:38:35 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 16 Jun 2026 01:38:35 GMT
VOLUME [/var/www/html]
# Tue, 16 Jun 2026 01:38:35 GMT
ENV JOOMLA_VERSION=5.4.6
# Tue, 16 Jun 2026 01:38:35 GMT
ENV JOOMLA_SHA512=d4198b32a37cea890b24ab219b7d267e6a6df3373530d5e76eb7f4563868ef6caebefa7a2b9290065146ef733db2b0becc18d69f291730c767a25aa158cb9c16
# Tue, 16 Jun 2026 01:42:57 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.4.6/Joomla_5.4.6-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Tue, 16 Jun 2026 01:42:57 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 16 Jun 2026 01:42:57 GMT
COPY makedb.php /makedb.php # buildkit
# Tue, 16 Jun 2026 01:42:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Jun 2026 01:42:57 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:3ebcdcd395ccee658b9200e4b27d7699e5d6ed9f6c1858dea12781aac519ff59`  
		Last Modified: Sun, 14 Jun 2026 06:46:36 GMT  
		Size: 3.8 MB (3813400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:538b9da4fa7a0b9d4db76eaa5e7475a9b26aebc92ecdbad7795d33e8c5862bfa`  
		Last Modified: Tue, 16 Jun 2026 00:21:30 GMT  
		Size: 3.6 MB (3637828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b72717bce2b969f044f4c03b530bca77062f0b0d4dfc1eb2f53b9a1459bcf77c`  
		Last Modified: Tue, 16 Jun 2026 00:21:30 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fecffaea7a9240f30a6d71b76e5cba5e41c27f6ab0409cce52536feeb7b55db`  
		Last Modified: Tue, 16 Jun 2026 00:21:30 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82494c5f949127e6a8557f5449493de7a71bbcce098a218e56de562eb44fef3`  
		Last Modified: Tue, 16 Jun 2026 00:34:57 GMT  
		Size: 12.6 MB (12626311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d8eaaa90bb3f69b2f7b270337e96d5458cc1e911b9caf5f02575e1b9a3857a`  
		Last Modified: Tue, 16 Jun 2026 00:34:56 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626f1a2a1bcf9a7c85feab8a8e31f87e3f9727e526569b5b5459edf4a66236b5`  
		Last Modified: Tue, 16 Jun 2026 00:36:30 GMT  
		Size: 14.0 MB (13984035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6e2a9d220e12aa7b0cf3acf96ea52befedd7eb4fb76b5137fd6d60f0a240013`  
		Last Modified: Tue, 16 Jun 2026 00:36:30 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3618b26084f12d36e6f16cf8d234e77d7dd155a6722c85875d5691d92a4d069f`  
		Last Modified: Tue, 16 Jun 2026 00:36:30 GMT  
		Size: 22.2 KB (22191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fffa0599b7f093ac0f6eadd12b17a300095f127c1c9f101cde156f85eb562fd1`  
		Last Modified: Tue, 16 Jun 2026 00:36:30 GMT  
		Size: 22.2 KB (22201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8cd8d939820864a24757a485595c0ae431e462a8641d34cadb20cc6aa15b050`  
		Last Modified: Tue, 16 Jun 2026 00:36:31 GMT  
		Size: 9.3 KB (9251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:214db3e626a8099927c0d1e5d7adedf9c03065240668f9b66c1e8215b3f8b6fe`  
		Last Modified: Tue, 16 Jun 2026 01:38:52 GMT  
		Size: 34.2 MB (34175962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e00a7238eb3032aac358552c181912c16fb816aafe5ab27ee4b71320899ed71`  
		Last Modified: Tue, 16 Jun 2026 01:38:51 GMT  
		Size: 7.2 MB (7200837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2efba7afb2d9e7914bd5c304de3ab79e1707b2420ead6ac8bac4a46d8323e8`  
		Last Modified: Tue, 16 Jun 2026 01:38:51 GMT  
		Size: 72.1 KB (72078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c4a34c3bd58854f6c8c4bd6f63a9308420a28c39682ee3f088a9e89b4da413`  
		Last Modified: Tue, 16 Jun 2026 01:38:51 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156bfde3736663bc00269a2a0702e16f2b45859ca7961e447a0695462f59fb44`  
		Last Modified: Tue, 16 Jun 2026 01:43:09 GMT  
		Size: 27.3 MB (27314306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ab1959d926d93e31c2c87a0861ff438232a03a05a554dd718c22956595b655`  
		Last Modified: Tue, 16 Jun 2026 01:43:09 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f473c05fa768679337d2cd16e24676551f206f65b78d318236ff4d7fbd3e6a30`  
		Last Modified: Tue, 16 Jun 2026 01:43:09 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:5-php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull joomla@sha256:d1b4b05969dbfc61aa96fb8acec56e64b13418152a63b61329bb1803a80601a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.8 KB (45760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:938c0c8350309d669ba19441ba34b8f896dc16845aed3565a271ca8f92491fdc`

```dockerfile
```

-	Layers:
	-	`sha256:0442b428f69be6c5b3de410cb9a2a4876bc4fe4cc0e985889ba8aff3ef696dc6`  
		Last Modified: Tue, 16 Jun 2026 01:43:08 GMT  
		Size: 45.8 KB (45760 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:5-php8.3-fpm-alpine` - linux; riscv64

```console
$ docker pull joomla@sha256:efcec788049f1e008b8b98b43c5f66f4ba49a159d6b9b22a2890c239941a3888
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.9 MB (99872075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cb6a93d80dbab3b66780d4a111d0183e9797da97ff566c1d6085844d63d8c13`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 16 Jun 2026 05:59:15 GMT
ADD alpine-minirootfs-3.24.1-riscv64.tar.gz / # buildkit
# Tue, 16 Jun 2026 05:59:15 GMT
CMD ["/bin/sh"]
# Wed, 17 Jun 2026 10:08:26 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 17 Jun 2026 10:08:26 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 17 Jun 2026 10:08:27 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 17 Jun 2026 10:08:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 17 Jun 2026 10:08:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 17 Jun 2026 10:08:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Jun 2026 10:08:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Jun 2026 10:08:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 17 Jun 2026 10:08:27 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 17 Jun 2026 10:08:27 GMT
ENV PHP_VERSION=8.3.31
# Wed, 17 Jun 2026 10:08:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Wed, 17 Jun 2026 10:08:27 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Wed, 17 Jun 2026 15:07:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 17 Jun 2026 15:07:12 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 17 Jun 2026 16:55:25 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 17 Jun 2026 16:55:25 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 17 Jun 2026 16:55:30 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 17 Jun 2026 16:55:34 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 17 Jun 2026 16:55:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 17 Jun 2026 16:55:35 GMT
WORKDIR /var/www/html
# Wed, 17 Jun 2026 16:55:35 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 17 Jun 2026 16:55:35 GMT
STOPSIGNAL SIGQUIT
# Wed, 17 Jun 2026 16:55:35 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 17 Jun 2026 16:55:35 GMT
CMD ["php-fpm"]
# Fri, 19 Jun 2026 02:34:56 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Fri, 19 Jun 2026 02:34:56 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Fri, 19 Jun 2026 02:34:56 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 		zstd 	; # buildkit
# Fri, 19 Jun 2026 03:00:08 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		icu-dev 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libmemcached-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 		pecl install APCu-5.1.27; 	pecl install memcached-3.4.0; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .joomla-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Fri, 19 Jun 2026 03:00:13 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 19 Jun 2026 03:00:13 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Fri, 19 Jun 2026 03:00:13 GMT
VOLUME [/var/www/html]
# Fri, 19 Jun 2026 03:00:13 GMT
ENV JOOMLA_VERSION=5.4.6
# Fri, 19 Jun 2026 03:00:13 GMT
ENV JOOMLA_SHA512=d4198b32a37cea890b24ab219b7d267e6a6df3373530d5e76eb7f4563868ef6caebefa7a2b9290065146ef733db2b0becc18d69f291730c767a25aa158cb9c16
# Fri, 19 Jun 2026 04:00:27 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.4.6/Joomla_5.4.6-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Fri, 19 Jun 2026 04:00:28 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 19 Jun 2026 04:00:28 GMT
COPY makedb.php /makedb.php # buildkit
# Fri, 19 Jun 2026 04:00:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 19 Jun 2026 04:00:28 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c34e5222b29b86391cdae95b0473ef789493ff1a0068a3a30b5d66f544bd7cf6`  
		Last Modified: Sun, 14 Jun 2026 06:47:00 GMT  
		Size: 3.6 MB (3574358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc09af4ff1d594ba4ff939387160eac2fe7e3118ca810f61819eb5d92f7b520`  
		Last Modified: Wed, 17 Jun 2026 12:01:56 GMT  
		Size: 3.6 MB (3604699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01600916adca5933ee02bb7a5a25279f28df2779de050e87ee103675d313f666`  
		Last Modified: Wed, 17 Jun 2026 12:01:55 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a891144274182ffd9c264ebaada55f1b357da87b9d652cda214fc6307d6f939`  
		Last Modified: Wed, 17 Jun 2026 12:01:55 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b26c75c574ff3af97cab175a345391d31a62cd3c6b7473fbb8b858d8590af3d0`  
		Last Modified: Wed, 17 Jun 2026 16:01:35 GMT  
		Size: 12.6 MB (12626315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ab09a33775328d19cbae5b76e98794681d5de48dc0d7e72b6ff89f27eebf89`  
		Last Modified: Wed, 17 Jun 2026 16:01:32 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b2abd3b2d639035828ca62d490e7f5b66208283fe8ed08507bb88e28d50f55`  
		Last Modified: Wed, 17 Jun 2026 16:56:25 GMT  
		Size: 12.8 MB (12828570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aac180e1cf49eda4b62545c84d111dc8ffd7a7c418a6cf988f74168a0f94b83`  
		Last Modified: Wed, 17 Jun 2026 16:56:23 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65bf650919738126acd701edf4827af5117aefab4fe2fbf2b2550987cf30ecd`  
		Last Modified: Wed, 17 Jun 2026 16:56:23 GMT  
		Size: 22.2 KB (22179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0da311742467a3c5fabf4aa31db000ffb9e827d29cd644afcc852ab77da339`  
		Last Modified: Wed, 17 Jun 2026 16:56:23 GMT  
		Size: 22.2 KB (22194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e79a33bd91dfb5ef4da8037ca477d35804a7237886aa2ad549c6d1719efa49`  
		Last Modified: Wed, 17 Jun 2026 16:56:24 GMT  
		Size: 9.3 KB (9255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4afa21b2f44c3e770ca43477616ed53fdf9728669a0021643554a240c2c5f229`  
		Last Modified: Fri, 19 Jun 2026 03:01:40 GMT  
		Size: 32.7 MB (32734000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada3fd5df145322300d051cc91233cd821aef6365469be66ac20a60f025eb702`  
		Last Modified: Fri, 19 Jun 2026 03:01:33 GMT  
		Size: 7.1 MB (7054934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9e74155dd6d280fa21b791c69d408fee6ac46822aeaa77ae349951742487a37`  
		Last Modified: Fri, 19 Jun 2026 03:01:31 GMT  
		Size: 72.0 KB (72040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56662cd1585fb8904118513efb3263fc47f719d9e46d2f1f0c1dfc887a9457f9`  
		Last Modified: Fri, 19 Jun 2026 03:01:30 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e349d75e838f4341d8922be74f4c9be93024771148d59de53eaed9ba4b21fa77`  
		Last Modified: Fri, 19 Jun 2026 04:01:34 GMT  
		Size: 27.3 MB (27314287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb79419951ef05f3129fa7fcf4ca22e8d7f75a45d40b081922cb3a5557d3280`  
		Last Modified: Fri, 19 Jun 2026 04:01:30 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004ad8a91d7252a0f234babf14aaad11c06e6feb80da3676b59ec0cc6a390b37`  
		Last Modified: Fri, 19 Jun 2026 04:01:30 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:5-php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull joomla@sha256:687da4d14f0381ee6c89dea02dd0452f0e645052afe458a1f8442feb3b597c70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.8 KB (45761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88dd33267ee5ad49172091f49e1489f2339167cb8d6953519ca4e7612a5036d5`

```dockerfile
```

-	Layers:
	-	`sha256:0ba4655f8fbda985a9dc54dc566dbc164a93f6c90c8cf2c156cb0773f5199672`  
		Last Modified: Fri, 19 Jun 2026 04:01:29 GMT  
		Size: 45.8 KB (45761 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:5-php8.3-fpm-alpine` - linux; s390x

```console
$ docker pull joomla@sha256:b5c6ef1034b185882d8b630bba700acd32f9fd81f802eb0ff3e8210f4b8daf91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.9 MB (101892316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5f83b0bf3994c2a4d589ad44e75cd43984bdf4a8f44f54a2fd7fd06d3078989`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:21 GMT
ADD alpine-minirootfs-3.24.1-s390x.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:21 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:13:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 16 Jun 2026 00:13:52 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 16 Jun 2026 00:13:52 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 16 Jun 2026 00:13:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 16 Jun 2026 00:13:52 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 16 Jun 2026 00:13:52 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 16 Jun 2026 00:13:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 16 Jun 2026 00:13:52 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 16 Jun 2026 00:13:52 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 16 Jun 2026 00:13:52 GMT
ENV PHP_VERSION=8.3.31
# Tue, 16 Jun 2026 00:13:52 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Tue, 16 Jun 2026 00:13:52 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Tue, 16 Jun 2026 00:23:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Tue, 16 Jun 2026 00:23:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:27:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 16 Jun 2026 00:27:56 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 00:27:57 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 16 Jun 2026 00:27:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 16 Jun 2026 00:27:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 16 Jun 2026 00:27:59 GMT
WORKDIR /var/www/html
# Tue, 16 Jun 2026 00:27:59 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 16 Jun 2026 00:27:59 GMT
STOPSIGNAL SIGQUIT
# Tue, 16 Jun 2026 00:27:59 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 16 Jun 2026 00:27:59 GMT
CMD ["php-fpm"]
# Tue, 16 Jun 2026 01:46:09 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 16 Jun 2026 01:46:09 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 16 Jun 2026 01:46:09 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 		zstd 	; # buildkit
# Tue, 16 Jun 2026 01:48:19 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		icu-dev 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libmemcached-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 		pecl install APCu-5.1.27; 	pecl install memcached-3.4.0; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .joomla-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 16 Jun 2026 01:48:20 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 16 Jun 2026 01:48:20 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 16 Jun 2026 01:48:20 GMT
VOLUME [/var/www/html]
# Tue, 16 Jun 2026 01:48:20 GMT
ENV JOOMLA_VERSION=5.4.6
# Tue, 16 Jun 2026 01:48:20 GMT
ENV JOOMLA_SHA512=d4198b32a37cea890b24ab219b7d267e6a6df3373530d5e76eb7f4563868ef6caebefa7a2b9290065146ef733db2b0becc18d69f291730c767a25aa158cb9c16
# Tue, 16 Jun 2026 01:48:22 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.4.6/Joomla_5.4.6-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Tue, 16 Jun 2026 01:48:22 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 16 Jun 2026 01:48:22 GMT
COPY makedb.php /makedb.php # buildkit
# Tue, 16 Jun 2026 01:48:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Jun 2026 01:48:22 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:da43be6afaaa3ec1b607461ce64380942a6d76c3d52cda4337b0770d9a96fa89`  
		Last Modified: Sun, 14 Jun 2026 06:47:25 GMT  
		Size: 3.7 MB (3709320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1478be2c88d13000249832224bb580b87a524c10ccf140e1f65943cb33f59eb`  
		Last Modified: Tue, 16 Jun 2026 00:18:18 GMT  
		Size: 3.7 MB (3651068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4532b14d23ad0cd16945b31df22f9a393cc7b3b64f7aa7fa62ade4877c52fad9`  
		Last Modified: Tue, 16 Jun 2026 00:18:18 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d62373606e3c4c1b6fef638aa78a6674eda0089fb632b2f1eaa05c504adeec8`  
		Last Modified: Tue, 16 Jun 2026 00:17:21 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb960454a3a050789ebff09c3493b411132f19ccb0fad82bdc05f469cc39b14`  
		Last Modified: Tue, 16 Jun 2026 00:28:11 GMT  
		Size: 12.6 MB (12626287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba72edc733fc0cf03ed9d8998ab076026ebaead0f7aa5ae3c4c13d4692c261c`  
		Last Modified: Tue, 16 Jun 2026 00:28:11 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb211e10020f5ebe101b302143029b923096e937408f968683a38637229ebb8c`  
		Last Modified: Tue, 16 Jun 2026 00:28:11 GMT  
		Size: 13.3 MB (13280099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d543d076e4dee58b3803c228720fc1c76d849a906875d8396e78a34caf72871`  
		Last Modified: Tue, 16 Jun 2026 00:28:11 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:843bf5fbcb8266a4d5d7e7668e571950c294d8dd56704d1a14e671fe1f2a8a5f`  
		Last Modified: Tue, 16 Jun 2026 00:28:12 GMT  
		Size: 22.1 KB (22134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f205ffc785403ee30b26f6ec7ee5795b1ef9ed4ee89d67f4871d1b4dd8c4cd`  
		Last Modified: Tue, 16 Jun 2026 00:28:12 GMT  
		Size: 22.2 KB (22158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be9d045787fa842d15e34a5d5736ed9027130ae88c2e6f47c13487fa54adf99`  
		Last Modified: Tue, 16 Jun 2026 00:28:12 GMT  
		Size: 9.3 KB (9251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f149452134c442a6e0a3779c9ff9a54ca3c4abec29c8937c6f6be2a309e12104`  
		Last Modified: Tue, 16 Jun 2026 01:48:35 GMT  
		Size: 34.1 MB (34070306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1582c46736de03167578c6052192cf4ce38e026d832398aa2916582dbdf44b56`  
		Last Modified: Tue, 16 Jun 2026 01:48:34 GMT  
		Size: 7.1 MB (7106196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce9a5122636d9571968b28b18bdbecc832e617d4bdae9c1abcc7cb8de4c72e1`  
		Last Modified: Tue, 16 Jun 2026 01:48:34 GMT  
		Size: 72.0 KB (72048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46521ee3c316226922275e061c2de34fbd4fb4926c90f758a89acd3fefe918cb`  
		Last Modified: Tue, 16 Jun 2026 01:48:33 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd9e537ddb588591b226726829266eb925c6c5e5bd70864785bd679f2cba394e`  
		Last Modified: Tue, 16 Jun 2026 01:48:36 GMT  
		Size: 27.3 MB (27314221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8400021dd8f6ed0be9e8bc67f91ed1d23f8cefb14daf1349c478cbfbfff5365`  
		Last Modified: Tue, 16 Jun 2026 01:48:35 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3710f9c7115c7f78cb2bd8e0e1e3c522790993d392998c283d527a539f7a363d`  
		Last Modified: Tue, 16 Jun 2026 01:48:35 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:5-php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull joomla@sha256:50bca8aab197259882a5e44020bad8281053b3d12c66235f704d0a70543a9a06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 KB (45715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b14aed7f9f36fdd5ef5e0c2a9732d6bbbe7704876106d9ef9e68497d0928f883`

```dockerfile
```

-	Layers:
	-	`sha256:4632c268255ecdbd2f6b70b1731a0653bef0b17654ced92eac5a7c0cce481fc7`  
		Last Modified: Tue, 16 Jun 2026 01:48:34 GMT  
		Size: 45.7 KB (45715 bytes)  
		MIME: application/vnd.in-toto+json
