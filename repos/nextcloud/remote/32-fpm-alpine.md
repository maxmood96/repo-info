## `nextcloud:32-fpm-alpine`

```console
$ docker pull nextcloud@sha256:38b5f7e145833b106c0c438e28ef349c268aa28b3fb895f58df061c330543503
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

### `nextcloud:32-fpm-alpine` - linux; amd64

```console
$ docker pull nextcloud@sha256:5685fe0b57ea8139c3d04b3e688b3ff67987f66d904661fc4319b65ec07b0e52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.1 MB (350060503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92d5a0d1f40ccfdb6837f1781234d1eea4f2c58cee615be1aa8aec81657baeb7`
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
# Tue, 16 Jun 2026 01:19:10 GMT
RUN set -ex;         apk add --no-cache         imagemagick         imagemagick-pdf         imagemagick-jpeg         imagemagick-raw         imagemagick-tiff         imagemagick-heic         imagemagick-webp         imagemagick-svg         rsync     ;         rm /var/spool/cron/crontabs/root;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Tue, 16 Jun 2026 01:20:47 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         autoconf         freetype-dev         gmp-dev         icu-dev         imagemagick-dev         libevent-dev         libjpeg-turbo-dev         libmemcached-dev         libpng-dev         libwebp-dev         libxml2-dev         libzip-dev         openldap-dev         pcre-dev         postgresql-dev     ;         docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap;     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.28;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.1;     pecl install --configureoptions 'enable-memcached-igbinary="yes"'         memcached-3.4.0;     pecl install --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"'         redis-6.3.0;         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .nextcloud-phpext-rundeps $runDeps;     apk del --no-network .build-deps # buildkit
# Tue, 16 Jun 2026 01:20:48 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 16 Jun 2026 01:20:48 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 16 Jun 2026 01:20:48 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Tue, 16 Jun 2026 01:20:48 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Tue, 16 Jun 2026 01:20:48 GMT
VOLUME [/var/www/html]
# Tue, 16 Jun 2026 01:20:48 GMT
ENV NEXTCLOUD_VERSION=32.0.11
# Tue, 16 Jun 2026 01:21:18 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         curl -fsSL -o nextcloud.tar.bz2 "https://github.com/nextcloud-releases/server/releases/download/v32.0.11/nextcloud-32.0.11.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://github.com/nextcloud-releases/server/releases/download/v32.0.11/nextcloud-32.0.11.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com  --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;     apk del --no-network .fetch-deps # buildkit
# Tue, 16 Jun 2026 01:21:18 GMT
COPY *.sh upgrade.exclude / # buildkit
# Tue, 16 Jun 2026 01:21:18 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Tue, 16 Jun 2026 01:21:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Jun 2026 01:21:18 GMT
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
	-	`sha256:8eeac477ee518a56458aa4f8f5d94aaeea70ea0aa8dca03a2727da9f55dd1096`  
		Last Modified: Tue, 16 Jun 2026 01:21:46 GMT  
		Size: 43.2 MB (43215177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755734f615291642a705618ca84654c0a90e2f0c8399d85b57bcecc26eeef11a`  
		Last Modified: Tue, 16 Jun 2026 01:21:44 GMT  
		Size: 7.2 MB (7175777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3556a8799799bf042e93687aaafb7cc6e8416ba969bb488d90b07ed7c48f4180`  
		Last Modified: Tue, 16 Jun 2026 01:21:44 GMT  
		Size: 790.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39c6cf3147a0f4031b270313767a418cd28b1e086260699b80ba544ef04c49e0`  
		Last Modified: Tue, 16 Jun 2026 01:21:52 GMT  
		Size: 266.2 MB (266248186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56024866ca4e800a32de12c410b9a32cbdef856cc47d07e55195bf380eccc840`  
		Last Modified: Tue, 16 Jun 2026 01:21:45 GMT  
		Size: 4.1 KB (4135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:742677178aabeb25e70556b8d447bc523407a875b298c586f90d439749224516`  
		Last Modified: Tue, 16 Jun 2026 01:21:46 GMT  
		Size: 2.4 KB (2356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:32-fpm-alpine` - unknown; unknown

```console
$ docker pull nextcloud@sha256:c06ceb253734ebeb56105ee0755927c1c42d5168ff31232ea1b1158fde4c7101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.6 KB (44596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9438679b49e868e9cca5a248bd54e44aa317dde2ab18a93d319762dabd9f8a4`

```dockerfile
```

-	Layers:
	-	`sha256:d64696429e12c3eb56654e40c3fb2a0bfb1c210c261fc65e361aed6c822c6ace`  
		Last Modified: Tue, 16 Jun 2026 01:21:43 GMT  
		Size: 44.6 KB (44596 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:32-fpm-alpine` - linux; arm variant v6

```console
$ docker pull nextcloud@sha256:a266d5f39a3783635c03c3369f69a161ac85f0b9c8916184d288fe831e4646c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.6 MB (344577173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffb1b4849e887153ef059cb720e231de8368053676426e612c550394d2845e08`
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
# Tue, 16 Jun 2026 01:25:37 GMT
RUN set -ex;         apk add --no-cache         imagemagick         imagemagick-pdf         imagemagick-jpeg         imagemagick-raw         imagemagick-tiff         imagemagick-heic         imagemagick-webp         imagemagick-svg         rsync     ;         rm /var/spool/cron/crontabs/root;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Tue, 16 Jun 2026 01:28:07 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         autoconf         freetype-dev         gmp-dev         icu-dev         imagemagick-dev         libevent-dev         libjpeg-turbo-dev         libmemcached-dev         libpng-dev         libwebp-dev         libxml2-dev         libzip-dev         openldap-dev         pcre-dev         postgresql-dev     ;         docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap;     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.28;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.1;     pecl install --configureoptions 'enable-memcached-igbinary="yes"'         memcached-3.4.0;     pecl install --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"'         redis-6.3.0;         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .nextcloud-phpext-rundeps $runDeps;     apk del --no-network .build-deps # buildkit
# Tue, 16 Jun 2026 01:28:08 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 16 Jun 2026 01:28:08 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 16 Jun 2026 01:28:08 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Tue, 16 Jun 2026 01:28:08 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Tue, 16 Jun 2026 01:28:08 GMT
VOLUME [/var/www/html]
# Tue, 16 Jun 2026 01:28:08 GMT
ENV NEXTCLOUD_VERSION=32.0.11
# Tue, 16 Jun 2026 01:28:51 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         curl -fsSL -o nextcloud.tar.bz2 "https://github.com/nextcloud-releases/server/releases/download/v32.0.11/nextcloud-32.0.11.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://github.com/nextcloud-releases/server/releases/download/v32.0.11/nextcloud-32.0.11.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com  --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;     apk del --no-network .fetch-deps # buildkit
# Tue, 16 Jun 2026 01:28:51 GMT
COPY *.sh upgrade.exclude / # buildkit
# Tue, 16 Jun 2026 01:28:51 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Tue, 16 Jun 2026 01:28:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Jun 2026 01:28:51 GMT
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
	-	`sha256:7fb8354e286210816027af8499468cf548b43e66b0989868b19000bc711bff92`  
		Last Modified: Tue, 16 Jun 2026 01:29:20 GMT  
		Size: 39.6 MB (39640214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b70300fec6146217c9f724549e7976ddace67c0c7930d2f45da63fb1b19942`  
		Last Modified: Tue, 16 Jun 2026 01:29:18 GMT  
		Size: 6.9 MB (6867544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473398dd64d9355d2ee96243487184b6f2e183c734cd2ea17ec70f6042aa95a5`  
		Last Modified: Tue, 16 Jun 2026 01:29:18 GMT  
		Size: 789.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:660f7ab844f88417ba43e3e7a92eaad36a50d662ba27a4b15aab36bae47e02e7`  
		Last Modified: Tue, 16 Jun 2026 01:29:24 GMT  
		Size: 266.2 MB (266248564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61d4b215afab4cbe2952b073e942907d0089f7e149c18516c6ff020900171003`  
		Last Modified: Tue, 16 Jun 2026 01:29:19 GMT  
		Size: 4.1 KB (4135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6dd6e16f4d8401b7601e8a8d3892a753f9e864ac7fb91aa0b1bfd9ac1e9cf05`  
		Last Modified: Tue, 16 Jun 2026 01:29:20 GMT  
		Size: 2.4 KB (2356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:32-fpm-alpine` - unknown; unknown

```console
$ docker pull nextcloud@sha256:3826aa87600b5765f30fb0263ebb4c72f235aadff2cb72da02887345e79fc281
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 KB (44707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82fc61ab45d6341a2bbb7a9a3299169f9a1d5dfc7daa18aaf14a563d0d49c647`

```dockerfile
```

-	Layers:
	-	`sha256:7f1d7a54deb5243d029af15e8da9ff8e66f7725fd6b293940c71897ced75a104`  
		Last Modified: Tue, 16 Jun 2026 01:29:18 GMT  
		Size: 44.7 KB (44707 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:32-fpm-alpine` - linux; arm variant v7

```console
$ docker pull nextcloud@sha256:dbb251ec14aee9be1e0f7e9fdcbd11f3a13517ff853b2783d51d27ebdccfe9ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.7 MB (340671582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b091e68db3d917234661889a2f920c5371c570100c6b62e90b698a6d70871b6`
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
# Tue, 16 Jun 2026 01:25:26 GMT
RUN set -ex;         apk add --no-cache         imagemagick         imagemagick-pdf         imagemagick-jpeg         imagemagick-raw         imagemagick-tiff         imagemagick-heic         imagemagick-webp         imagemagick-svg         rsync     ;         rm /var/spool/cron/crontabs/root;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Tue, 16 Jun 2026 01:27:52 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         autoconf         freetype-dev         gmp-dev         icu-dev         imagemagick-dev         libevent-dev         libjpeg-turbo-dev         libmemcached-dev         libpng-dev         libwebp-dev         libxml2-dev         libzip-dev         openldap-dev         pcre-dev         postgresql-dev     ;         docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap;     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.28;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.1;     pecl install --configureoptions 'enable-memcached-igbinary="yes"'         memcached-3.4.0;     pecl install --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"'         redis-6.3.0;         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .nextcloud-phpext-rundeps $runDeps;     apk del --no-network .build-deps # buildkit
# Tue, 16 Jun 2026 01:27:53 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 16 Jun 2026 01:27:53 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 16 Jun 2026 01:27:53 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Tue, 16 Jun 2026 01:27:53 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Tue, 16 Jun 2026 01:27:53 GMT
VOLUME [/var/www/html]
# Tue, 16 Jun 2026 01:27:53 GMT
ENV NEXTCLOUD_VERSION=32.0.11
# Tue, 16 Jun 2026 01:28:29 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         curl -fsSL -o nextcloud.tar.bz2 "https://github.com/nextcloud-releases/server/releases/download/v32.0.11/nextcloud-32.0.11.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://github.com/nextcloud-releases/server/releases/download/v32.0.11/nextcloud-32.0.11.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com  --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;     apk del --no-network .fetch-deps # buildkit
# Tue, 16 Jun 2026 01:28:29 GMT
COPY *.sh upgrade.exclude / # buildkit
# Tue, 16 Jun 2026 01:28:29 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Tue, 16 Jun 2026 01:28:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Jun 2026 01:28:29 GMT
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
	-	`sha256:4a36cc529871e6967d9d14cb014b1f5de48efa5a0c05decfa51a7b5dceb71fe2`  
		Last Modified: Tue, 16 Jun 2026 01:28:58 GMT  
		Size: 36.9 MB (36892004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f280c279e6e866d910ca5c0ee1e35e2cd750949d9668a41466ac44a43870a48d`  
		Last Modified: Tue, 16 Jun 2026 01:28:57 GMT  
		Size: 6.9 MB (6900995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14580631a46d6177d80d9f02061f86941ba89466c5c2129dc125ed8bb3e9e065`  
		Last Modified: Tue, 16 Jun 2026 01:28:56 GMT  
		Size: 787.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa274f76eb515a3c6b23a277ef86f3087db8f205fa1e54ecb24b12a99aaa7ed`  
		Last Modified: Tue, 16 Jun 2026 01:29:03 GMT  
		Size: 266.2 MB (266248604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7ba1758797f2d6a9b4175e32c75df245bc3926f6c5788aee45e965f520c251`  
		Last Modified: Tue, 16 Jun 2026 01:28:58 GMT  
		Size: 4.1 KB (4135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f42bca50935eb5849c8fde222207f1200e67972748b299977782d847be66abb3`  
		Last Modified: Tue, 16 Jun 2026 01:28:59 GMT  
		Size: 2.4 KB (2352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:32-fpm-alpine` - unknown; unknown

```console
$ docker pull nextcloud@sha256:6d2212948b7585583ecd5d12edf759ebd5ffe770e722e4249a2d78b5bc13cdb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 KB (44705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a547d6b362dd14922ff7ea58af4cc0b5602e42c7125b72f31d196c9ad84a78`

```dockerfile
```

-	Layers:
	-	`sha256:a90f614e78ce00e6f5ec2670649beb65f78b9ca886f068331b81114f1a141a7b`  
		Last Modified: Tue, 16 Jun 2026 01:28:56 GMT  
		Size: 44.7 KB (44705 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:32-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull nextcloud@sha256:8a688ffcb85dd6295bd202dccc7bf1ed6f58ddb0dd7f71052ca9e3b7967ce6aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.2 MB (349242171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a2b007056b603e9773a35e9c6a6ac04bb01d1daee7246ff3a33a1466f4802a7`
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
# Tue, 16 Jun 2026 01:21:02 GMT
RUN set -ex;         apk add --no-cache         imagemagick         imagemagick-pdf         imagemagick-jpeg         imagemagick-raw         imagemagick-tiff         imagemagick-heic         imagemagick-webp         imagemagick-svg         rsync     ;         rm /var/spool/cron/crontabs/root;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Tue, 16 Jun 2026 01:23:09 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         autoconf         freetype-dev         gmp-dev         icu-dev         imagemagick-dev         libevent-dev         libjpeg-turbo-dev         libmemcached-dev         libpng-dev         libwebp-dev         libxml2-dev         libzip-dev         openldap-dev         pcre-dev         postgresql-dev     ;         docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap;     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.28;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.1;     pecl install --configureoptions 'enable-memcached-igbinary="yes"'         memcached-3.4.0;     pecl install --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"'         redis-6.3.0;         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .nextcloud-phpext-rundeps $runDeps;     apk del --no-network .build-deps # buildkit
# Tue, 16 Jun 2026 01:23:09 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 16 Jun 2026 01:23:09 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 16 Jun 2026 01:23:09 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Tue, 16 Jun 2026 01:23:09 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Tue, 16 Jun 2026 01:23:09 GMT
VOLUME [/var/www/html]
# Tue, 16 Jun 2026 01:23:09 GMT
ENV NEXTCLOUD_VERSION=32.0.11
# Tue, 16 Jun 2026 01:23:42 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         curl -fsSL -o nextcloud.tar.bz2 "https://github.com/nextcloud-releases/server/releases/download/v32.0.11/nextcloud-32.0.11.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://github.com/nextcloud-releases/server/releases/download/v32.0.11/nextcloud-32.0.11.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com  --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;     apk del --no-network .fetch-deps # buildkit
# Tue, 16 Jun 2026 01:23:42 GMT
COPY *.sh upgrade.exclude / # buildkit
# Tue, 16 Jun 2026 01:23:42 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Tue, 16 Jun 2026 01:23:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Jun 2026 01:23:42 GMT
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
	-	`sha256:d23a21211d50062031fb23912dc55eba6a70f7bd8ec6f5ba2b997776d9579cd0`  
		Last Modified: Tue, 16 Jun 2026 01:24:15 GMT  
		Size: 42.2 MB (42221733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2017755339e4a9c5a4b68cd3682d04cda5f621aeea0028d5ad304992d8d12dc0`  
		Last Modified: Tue, 16 Jun 2026 01:24:13 GMT  
		Size: 7.1 MB (7102480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91cb0ba3419d457c9a99904fcf8cd1e090f1bd054cb092c86ab7d7fe2c82362`  
		Last Modified: Tue, 16 Jun 2026 01:24:12 GMT  
		Size: 786.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72b0c90fc4c7d06151e227a7d0b621af4a3e37e68bbcb4e92e9d695f13720c4`  
		Last Modified: Tue, 16 Jun 2026 01:24:19 GMT  
		Size: 266.2 MB (266248133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f0badcce2523c583ac9f02d6384a9e1fae1456cdd4cd90920cedb0a3fd6b658`  
		Last Modified: Tue, 16 Jun 2026 01:24:14 GMT  
		Size: 4.1 KB (4136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f2722e2ef431671ed08ac4c66e534845b86ffa02a829cbb197fee8f315f470`  
		Last Modified: Tue, 16 Jun 2026 01:24:15 GMT  
		Size: 2.4 KB (2353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:32-fpm-alpine` - unknown; unknown

```console
$ docker pull nextcloud@sha256:861727432b863fcfe6ccdf998923a53630b00ff8db7be3121629f5a17121ae76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 KB (44732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fdf1ddb2cd72b94cfdf06b8de3bcf5fbeca130724d1ce9b04a2a3f4abd524f0`

```dockerfile
```

-	Layers:
	-	`sha256:79ecd84acc6239369e16e8ff5459dd684e800964a0ffdf340f5d55b9256e702a`  
		Last Modified: Tue, 16 Jun 2026 01:24:12 GMT  
		Size: 44.7 KB (44732 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:32-fpm-alpine` - linux; 386

```console
$ docker pull nextcloud@sha256:19db56365c59137e5301249cbbdc6be8b8367880920a7c9628aae047fd485fcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.2 MB (351162999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66bcd5ccf95213297bcf69a72a36c9b825f8aa65922a552bd49d579684d9c8f9`
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
# Tue, 16 Jun 2026 01:16:31 GMT
RUN set -ex;         apk add --no-cache         imagemagick         imagemagick-pdf         imagemagick-jpeg         imagemagick-raw         imagemagick-tiff         imagemagick-heic         imagemagick-webp         imagemagick-svg         rsync     ;         rm /var/spool/cron/crontabs/root;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Tue, 16 Jun 2026 01:18:23 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         autoconf         freetype-dev         gmp-dev         icu-dev         imagemagick-dev         libevent-dev         libjpeg-turbo-dev         libmemcached-dev         libpng-dev         libwebp-dev         libxml2-dev         libzip-dev         openldap-dev         pcre-dev         postgresql-dev     ;         docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap;     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.28;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.1;     pecl install --configureoptions 'enable-memcached-igbinary="yes"'         memcached-3.4.0;     pecl install --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"'         redis-6.3.0;         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .nextcloud-phpext-rundeps $runDeps;     apk del --no-network .build-deps # buildkit
# Tue, 16 Jun 2026 01:18:23 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 16 Jun 2026 01:18:23 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 16 Jun 2026 01:18:23 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Tue, 16 Jun 2026 01:18:23 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Tue, 16 Jun 2026 01:18:23 GMT
VOLUME [/var/www/html]
# Tue, 16 Jun 2026 01:18:23 GMT
ENV NEXTCLOUD_VERSION=32.0.11
# Tue, 16 Jun 2026 01:19:14 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         curl -fsSL -o nextcloud.tar.bz2 "https://github.com/nextcloud-releases/server/releases/download/v32.0.11/nextcloud-32.0.11.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://github.com/nextcloud-releases/server/releases/download/v32.0.11/nextcloud-32.0.11.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com  --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;     apk del --no-network .fetch-deps # buildkit
# Tue, 16 Jun 2026 01:19:15 GMT
COPY *.sh upgrade.exclude / # buildkit
# Tue, 16 Jun 2026 01:19:15 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Tue, 16 Jun 2026 01:19:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Jun 2026 01:19:15 GMT
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
	-	`sha256:32e222ee5752530de4b8649eb6e0b7d5f1ec364abcef0d22b432839f54a23652`  
		Last Modified: Tue, 16 Jun 2026 01:19:43 GMT  
		Size: 44.1 MB (44102191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b2562a4afbd169be0b78b3898f0de832e4bf5e14f26f75bec0e845e5a78b064`  
		Last Modified: Tue, 16 Jun 2026 01:19:41 GMT  
		Size: 7.3 MB (7263205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2692047d0cb45bb97d2d9775e342e43405384789407d29d89d0495e878dc32c7`  
		Last Modified: Tue, 16 Jun 2026 01:19:41 GMT  
		Size: 782.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af30d9a4fd3d482e198d75b4a2afc28416d92d6d9794416d1de95c9ba00dc80a`  
		Last Modified: Tue, 16 Jun 2026 01:19:48 GMT  
		Size: 266.2 MB (266248307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4dffac4af4c39292b2021790165a3a44fe9888bf71670801071e64fab376bcd`  
		Last Modified: Tue, 16 Jun 2026 01:19:36 GMT  
		Size: 4.1 KB (4136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c07da0a9f466c3b80a0b2eb3846c89b5a6a8770e19885a02bd0fd329a19ee38`  
		Last Modified: Tue, 16 Jun 2026 01:19:42 GMT  
		Size: 2.4 KB (2357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:32-fpm-alpine` - unknown; unknown

```console
$ docker pull nextcloud@sha256:56af788b652c447b35a0b2a115473c7515539d527e919fc4da2c199e9efbf9e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.6 KB (44563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25c4f3ec9ab4ba9ab6c08bb458bde79fb2e2738de0b70a9141517ab16239f3b3`

```dockerfile
```

-	Layers:
	-	`sha256:110227579c46377211e883bf5ee2103443afbfb1f6a263040d543bff1ad8ee65`  
		Last Modified: Tue, 16 Jun 2026 01:19:40 GMT  
		Size: 44.6 KB (44563 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:32-fpm-alpine` - linux; ppc64le

```console
$ docker pull nextcloud@sha256:3d1fb3c7bb41ec23ebcbb1f38a2c04c748a0feca9b6d3d927fed42c602e5b51b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.9 MB (354936292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:961b838b05682b64422576317f54ca91ebe63d1034050ba039f6ef41a7c985f2`
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
# Tue, 16 Jun 2026 01:50:41 GMT
RUN set -ex;         apk add --no-cache         imagemagick         imagemagick-pdf         imagemagick-jpeg         imagemagick-raw         imagemagick-tiff         imagemagick-heic         imagemagick-webp         imagemagick-svg         rsync     ;         rm /var/spool/cron/crontabs/root;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Tue, 16 Jun 2026 01:54:30 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         autoconf         freetype-dev         gmp-dev         icu-dev         imagemagick-dev         libevent-dev         libjpeg-turbo-dev         libmemcached-dev         libpng-dev         libwebp-dev         libxml2-dev         libzip-dev         openldap-dev         pcre-dev         postgresql-dev     ;         docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap;     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.28;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.1;     pecl install --configureoptions 'enable-memcached-igbinary="yes"'         memcached-3.4.0;     pecl install --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"'         redis-6.3.0;         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .nextcloud-phpext-rundeps $runDeps;     apk del --no-network .build-deps # buildkit
# Tue, 16 Jun 2026 01:54:30 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 16 Jun 2026 01:54:30 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 16 Jun 2026 01:54:30 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Tue, 16 Jun 2026 01:54:30 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Tue, 16 Jun 2026 01:54:30 GMT
VOLUME [/var/www/html]
# Tue, 16 Jun 2026 01:54:30 GMT
ENV NEXTCLOUD_VERSION=32.0.11
# Tue, 16 Jun 2026 01:55:17 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         curl -fsSL -o nextcloud.tar.bz2 "https://github.com/nextcloud-releases/server/releases/download/v32.0.11/nextcloud-32.0.11.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://github.com/nextcloud-releases/server/releases/download/v32.0.11/nextcloud-32.0.11.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com  --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;     apk del --no-network .fetch-deps # buildkit
# Tue, 16 Jun 2026 01:55:17 GMT
COPY *.sh upgrade.exclude / # buildkit
# Tue, 16 Jun 2026 01:55:18 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Tue, 16 Jun 2026 01:55:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Jun 2026 01:55:18 GMT
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
	-	`sha256:9d3ecfae65fc3b69b61415d1c653eebf6d592d8ce1828fe223c7ec15fcf661d6`  
		Last Modified: Tue, 16 Jun 2026 01:56:12 GMT  
		Size: 47.2 MB (47159486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f8a86517a286df43d6c64f1c77bc4425763218fe5fb7ba66d304aa11e7dd5ab`  
		Last Modified: Tue, 16 Jun 2026 01:56:10 GMT  
		Size: 7.4 MB (7401613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6752641800e12ffdfb0e567ff014bbfa8f21917b1ceb262d4c810eabc32e46`  
		Last Modified: Tue, 16 Jun 2026 01:56:09 GMT  
		Size: 785.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe11aa1b8d7e32ef3f89bf4834b2d535dfa66ba623a4306de48904ad3d0f0757`  
		Last Modified: Tue, 16 Jun 2026 01:56:16 GMT  
		Size: 266.2 MB (266248576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a1334bb88b633b6bcc458657117c8440e00ae9748cf5c9481620a47abfc215`  
		Last Modified: Tue, 16 Jun 2026 01:56:10 GMT  
		Size: 4.1 KB (4136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70de472d6d0359c2a92e853eef2ed863dab57fce42e03dc15c2ff431fda1d8c5`  
		Last Modified: Tue, 16 Jun 2026 01:56:11 GMT  
		Size: 2.4 KB (2353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:32-fpm-alpine` - unknown; unknown

```console
$ docker pull nextcloud@sha256:0e1766ce9cdb45a2ac5234ba8a44912662e7902342cfbb5ea32a261d00a95def
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.6 KB (44639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:349dff4d7e1264b1fdb9a6089c2884c5961a277df0089f85552cef362697fae4`

```dockerfile
```

-	Layers:
	-	`sha256:667ca2dc2b469d6c611d69170453f234452c40f8b324c114d8ff14ea0aa8c354`  
		Last Modified: Tue, 16 Jun 2026 01:56:09 GMT  
		Size: 44.6 KB (44639 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:32-fpm-alpine` - linux; riscv64

```console
$ docker pull nextcloud@sha256:e5f0cc372fdd622d5d7fd40db66f8886cb88f016492e960fddea721f7203ae61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.0 MB (349020461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e77748cf4714dcf42eb82e85f641516e601e47b1d81b89c08fa3d59b044ba08`
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
# Fri, 19 Jun 2026 05:05:01 GMT
RUN set -ex;         apk add --no-cache         imagemagick         imagemagick-pdf         imagemagick-jpeg         imagemagick-raw         imagemagick-tiff         imagemagick-heic         imagemagick-webp         imagemagick-svg         rsync     ;         rm /var/spool/cron/crontabs/root;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Fri, 19 Jun 2026 05:31:23 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         autoconf         freetype-dev         gmp-dev         icu-dev         imagemagick-dev         libevent-dev         libjpeg-turbo-dev         libmemcached-dev         libpng-dev         libwebp-dev         libxml2-dev         libzip-dev         openldap-dev         pcre-dev         postgresql-dev     ;         docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap;     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.28;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.1;     pecl install --configureoptions 'enable-memcached-igbinary="yes"'         memcached-3.4.0;     pecl install --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"'         redis-6.3.0;         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .nextcloud-phpext-rundeps $runDeps;     apk del --no-network .build-deps # buildkit
# Fri, 19 Jun 2026 05:31:23 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 19 Jun 2026 05:31:23 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 19 Jun 2026 05:31:23 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Fri, 19 Jun 2026 05:31:23 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Fri, 19 Jun 2026 05:31:23 GMT
VOLUME [/var/www/html]
# Fri, 19 Jun 2026 05:31:23 GMT
ENV NEXTCLOUD_VERSION=32.0.11
# Fri, 19 Jun 2026 05:35:18 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         curl -fsSL -o nextcloud.tar.bz2 "https://github.com/nextcloud-releases/server/releases/download/v32.0.11/nextcloud-32.0.11.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://github.com/nextcloud-releases/server/releases/download/v32.0.11/nextcloud-32.0.11.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com  --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;     apk del --no-network .fetch-deps # buildkit
# Fri, 19 Jun 2026 05:35:20 GMT
COPY *.sh upgrade.exclude / # buildkit
# Fri, 19 Jun 2026 05:35:20 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Fri, 19 Jun 2026 05:35:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 19 Jun 2026 05:35:20 GMT
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
	-	`sha256:6275c511acac610b3091fb9068ede22f47e402d4758a423930b03d4644148acf`  
		Last Modified: Fri, 19 Jun 2026 05:41:13 GMT  
		Size: 42.8 MB (42785903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd23e4261f3f78dacfc9a8979e7e4b799abee33ab6abe27db2781c6f508b8b1`  
		Last Modified: Fri, 19 Jun 2026 05:41:03 GMT  
		Size: 7.3 MB (7286998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73eb9950b6e257bb66bd0dfca92f9df953daf2307b6798e1defa3754cb236547`  
		Last Modified: Fri, 19 Jun 2026 05:41:00 GMT  
		Size: 787.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:472d3b8a7958fd3d3375d29c8ee748a2b2da370938362f69de4231b5e6bce791`  
		Last Modified: Fri, 19 Jun 2026 05:41:46 GMT  
		Size: 266.2 MB (266248584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e11966a3ea90ab2374dc9756ecde676af1a5d49c3d79db9e0d26696a4e3821e5`  
		Last Modified: Fri, 19 Jun 2026 05:41:02 GMT  
		Size: 4.1 KB (4136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e18748f7f78f1c213be6c12938904a355f03889622885c4ff4cc190162da7ea2`  
		Last Modified: Fri, 19 Jun 2026 05:41:04 GMT  
		Size: 2.4 KB (2354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:32-fpm-alpine` - unknown; unknown

```console
$ docker pull nextcloud@sha256:a84b1ac103440a354260d49c2d00f23f2c392a284a845e0a73aa57900fdb6e79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.6 KB (44640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3d2ed1e4935d40ad8e4b0bd29eab528b8143d44ca6bcf21bbb6ba85f274a0de`

```dockerfile
```

-	Layers:
	-	`sha256:0a650409d1ac2d9c2fa00ef2ff88435a8265773264a81bc26cc718210335f602`  
		Last Modified: Fri, 19 Jun 2026 05:41:00 GMT  
		Size: 44.6 KB (44640 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:32-fpm-alpine` - linux; s390x

```console
$ docker pull nextcloud@sha256:7c264055e642ec3975df318157b9318acd3faba087f4af3b2b8af11a826a2871
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.5 MB (351507684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94c7a398c5d100ceed2f20b7c042ab98cc5863d2c98efc1f7681e1e4394aad8c`
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
# Tue, 16 Jun 2026 01:49:01 GMT
RUN set -ex;         apk add --no-cache         imagemagick         imagemagick-pdf         imagemagick-jpeg         imagemagick-raw         imagemagick-tiff         imagemagick-heic         imagemagick-webp         imagemagick-svg         rsync     ;         rm /var/spool/cron/crontabs/root;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Tue, 16 Jun 2026 01:51:17 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         autoconf         freetype-dev         gmp-dev         icu-dev         imagemagick-dev         libevent-dev         libjpeg-turbo-dev         libmemcached-dev         libpng-dev         libwebp-dev         libxml2-dev         libzip-dev         openldap-dev         pcre-dev         postgresql-dev     ;         docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap;     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.28;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.1;     pecl install --configureoptions 'enable-memcached-igbinary="yes"'         memcached-3.4.0;     pecl install --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"'         redis-6.3.0;         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .nextcloud-phpext-rundeps $runDeps;     apk del --no-network .build-deps # buildkit
# Tue, 16 Jun 2026 01:51:17 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 16 Jun 2026 01:51:17 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 16 Jun 2026 01:51:17 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Tue, 16 Jun 2026 01:51:17 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Tue, 16 Jun 2026 01:51:17 GMT
VOLUME [/var/www/html]
# Tue, 16 Jun 2026 01:51:17 GMT
ENV NEXTCLOUD_VERSION=32.0.11
# Tue, 16 Jun 2026 01:51:47 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         curl -fsSL -o nextcloud.tar.bz2 "https://github.com/nextcloud-releases/server/releases/download/v32.0.11/nextcloud-32.0.11.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://github.com/nextcloud-releases/server/releases/download/v32.0.11/nextcloud-32.0.11.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com  --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;     apk del --no-network .fetch-deps # buildkit
# Tue, 16 Jun 2026 01:51:47 GMT
COPY *.sh upgrade.exclude / # buildkit
# Tue, 16 Jun 2026 01:51:47 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Tue, 16 Jun 2026 01:51:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Jun 2026 01:51:47 GMT
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
	-	`sha256:b6fe2c6dfb6d0588ba01249ff8e1cc1b8e7fabd5199cede7db0853e6dfcc3607`  
		Last Modified: Tue, 16 Jun 2026 01:52:29 GMT  
		Size: 44.6 MB (44627090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518df254cc790757105eb3e5839993590724560ce08a1e78889d327d34eaecb4`  
		Last Modified: Tue, 16 Jun 2026 01:52:27 GMT  
		Size: 7.3 MB (7300300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9c2d768e6b4ba8cb2cd73367fd4aab0a7931884123bdf52b05d215053abdcf7`  
		Last Modified: Tue, 16 Jun 2026 01:52:27 GMT  
		Size: 784.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beec9ccc1f9f1b12b29a3353aa07361138f779dd0dd7215ff0868a2b39bc4869`  
		Last Modified: Tue, 16 Jun 2026 01:52:32 GMT  
		Size: 266.2 MB (266248594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b808a196e7454e5d13154c88f84cb1265c9cb4258ce1e63a7815f93fd409ae`  
		Last Modified: Tue, 16 Jun 2026 01:52:28 GMT  
		Size: 4.1 KB (4135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e137e5757786aaba97b4915a11c4fe510feb0ec95e8033d53e7d3daf58e4ad10`  
		Last Modified: Tue, 16 Jun 2026 01:52:29 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:32-fpm-alpine` - unknown; unknown

```console
$ docker pull nextcloud@sha256:d202275b880b5263c4d308c4e5fc715be15fc5f94229da86ea749f1370e0a1d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.6 KB (44596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f48434b06956368b9e69b3c9b50e98f6e04e59ae8b51910252d6486fb0e75b2b`

```dockerfile
```

-	Layers:
	-	`sha256:35ff9feae0607f7db06c4161b6a359debc24d2957d0ecbb9b57f9f0ab28fdc1a`  
		Last Modified: Tue, 16 Jun 2026 01:52:27 GMT  
		Size: 44.6 KB (44596 bytes)  
		MIME: application/vnd.in-toto+json
