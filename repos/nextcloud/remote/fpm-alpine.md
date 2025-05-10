## `nextcloud:fpm-alpine`

```console
$ docker pull nextcloud@sha256:255a3734978e664f7dbc6d46987344f14f4c5f23bcaea6dbaad91a14ccd1bdce
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

### `nextcloud:fpm-alpine` - linux; amd64

```console
$ docker pull nextcloud@sha256:2df305eb9753d54d4dcb7eef09c452ce4acdbdf9fde3b2dbf65c25c0c4bd8fad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.9 MB (330928682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7bee936cd1f5a1383cf8941de699bfcff0885248f258ea03b8097857c426bc4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 18 Apr 2025 15:01:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 18 Apr 2025 15:01:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 18 Apr 2025 15:01:40 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_VERSION=8.3.21
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.21.tar.xz.asc
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_SHA256=4dfb329f209a552c3716394fc123bb62e80a468b55ce27fc8cb0fd5f30b9dcd6
# Fri, 18 Apr 2025 15:01:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 18 Apr 2025 15:01:40 GMT
WORKDIR /var/www/html
# Fri, 18 Apr 2025 15:01:40 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
STOPSIGNAL SIGQUIT
# Fri, 18 Apr 2025 15:01:40 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 18 Apr 2025 15:01:40 GMT
CMD ["php-fpm"]
# Fri, 18 Apr 2025 15:01:40 GMT
RUN set -ex;         apk add --no-cache         imagemagick         imagemagick-pdf         imagemagick-jpeg         imagemagick-raw         imagemagick-tiff         imagemagick-heic         imagemagick-webp         imagemagick-svg         rsync     ;         rm /var/spool/cron/crontabs/root;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         autoconf         freetype-dev         gmp-dev         icu-dev         imagemagick-dev         libevent-dev         libjpeg-turbo-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libwebp-dev         libxml2-dev         libzip-dev         openldap-dev         pcre-dev         postgresql-dev     ;         docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap;     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.24;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.0;     pecl install memcached-3.3.0         --configureoptions 'enable-memcached-igbinary="yes"';     pecl install redis-6.2.0         --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"';         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .nextcloud-phpext-rundeps $runDeps;     apk del --no-network .build-deps # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Fri, 18 Apr 2025 15:01:40 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
VOLUME [/var/www/html]
# Fri, 18 Apr 2025 15:01:40 GMT
ENV NEXTCLOUD_VERSION=31.0.4
# Fri, 18 Apr 2025 15:01:40 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-31.0.4.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-31.0.4.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com  --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;     apk del --no-network .fetch-deps # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
COPY *.sh upgrade.exclude / # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Apr 2025 15:01:40 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ae2d63846e3f3a8cf511e8363f773065c9679634a4dac56180cb0e5fea1f44`  
		Last Modified: Fri, 09 May 2025 17:26:35 GMT  
		Size: 3.3 MB (3339418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:984ac2fbab4c55f3bbfdc01c84d2c00d79bf5355f93d0b394b4f50d273c9f670`  
		Last Modified: Fri, 09 May 2025 17:26:35 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6febbfc1f8036274382dede71894e339025396c6dcd78a8f53a05fafa72fd56`  
		Last Modified: Fri, 09 May 2025 17:26:35 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae8c0b3df265b0d230eabca804c1231dc541fba5b34f53d92db7fe0d983a5789`  
		Last Modified: Fri, 09 May 2025 17:26:35 GMT  
		Size: 12.6 MB (12587272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4868d39426399139dab64cded94dc40f374ca6f1ce2a31a21ebf5600ab158e41`  
		Last Modified: Fri, 09 May 2025 17:26:36 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6eea1622b6bf20d6ab643ae71ed8ada86934a51e4596d0cf89db202398c781`  
		Last Modified: Fri, 09 May 2025 17:26:36 GMT  
		Size: 13.2 MB (13248958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea81cfecdcb310b341b15591100a2380c8d903570e8a6ce231fc3a07b39527d5`  
		Last Modified: Fri, 09 May 2025 17:26:36 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8687c16c73207afe63a956f2cf47459783a40885608b0306cbcf6dfc13962f6e`  
		Last Modified: Fri, 09 May 2025 17:26:36 GMT  
		Size: 20.0 KB (20046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50bf699f3caacba609039ce8e92e5cba34011f995fd31dfb73d2f652d77d9e3f`  
		Last Modified: Fri, 09 May 2025 17:26:37 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84341fa68c14d882edda210cbf9f8668208967df9d6c922c703b2a5d25eaa752`  
		Last Modified: Fri, 09 May 2025 17:38:12 GMT  
		Size: 44.2 MB (44186537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:926fe769936be9624ecc3c16842f54ab9a7af44bd5977439bc1f519087176a4f`  
		Last Modified: Fri, 09 May 2025 17:38:11 GMT  
		Size: 7.6 MB (7578174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c5ab0f2ab53e34b90808a5528b67f30edf3e04e17dd88bd267720bea418919e`  
		Last Modified: Fri, 09 May 2025 17:38:10 GMT  
		Size: 786.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:653e0bb37822d9534d28bbebfa4b70e62d97eafe0d6e8f141b60e82991392265`  
		Last Modified: Fri, 09 May 2025 17:38:16 GMT  
		Size: 246.3 MB (246305557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2092da96c5effb8c693edbf11f1f9f2b3d593c155d0a6e4b4ec3ee52aa59c73`  
		Last Modified: Fri, 09 May 2025 17:38:11 GMT  
		Size: 4.0 KB (4047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a525ddf3a139924267aaeba2be38d025911574d4d615e65f9bc03b42d2579a`  
		Last Modified: Fri, 09 May 2025 17:38:12 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:fpm-alpine` - unknown; unknown

```console
$ docker pull nextcloud@sha256:63ff14fd6a42d27aec7708d94090be40e244203926428299f908c81f59cf5a77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.6 KB (44570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95b7c6c67489dee4d6644694985cc022064b6b8ebc057fac62aa4863cd4a4296`

```dockerfile
```

-	Layers:
	-	`sha256:0267e115f227b357a34515f52816732218a053dfb91749903a898f7fb96691e0`  
		Last Modified: Fri, 09 May 2025 17:38:09 GMT  
		Size: 44.6 KB (44570 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:fpm-alpine` - linux; arm variant v6

```console
$ docker pull nextcloud@sha256:209bd9584349656e5af85c1dd070893c9b2d051ac25be9ba835d97ea074f191e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.9 MB (322877906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:079af9bfe2c01d77637be1b32addeb61ce6cbd41c73e495b20bd05a1a3b70890`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 18 Apr 2025 15:01:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 18 Apr 2025 15:01:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 18 Apr 2025 15:01:40 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_VERSION=8.3.21
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.21.tar.xz.asc
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_SHA256=4dfb329f209a552c3716394fc123bb62e80a468b55ce27fc8cb0fd5f30b9dcd6
# Fri, 18 Apr 2025 15:01:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 18 Apr 2025 15:01:40 GMT
WORKDIR /var/www/html
# Fri, 18 Apr 2025 15:01:40 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
STOPSIGNAL SIGQUIT
# Fri, 18 Apr 2025 15:01:40 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 18 Apr 2025 15:01:40 GMT
CMD ["php-fpm"]
# Fri, 18 Apr 2025 15:01:40 GMT
RUN set -ex;         apk add --no-cache         imagemagick         imagemagick-pdf         imagemagick-jpeg         imagemagick-raw         imagemagick-tiff         imagemagick-heic         imagemagick-webp         imagemagick-svg         rsync     ;         rm /var/spool/cron/crontabs/root;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         autoconf         freetype-dev         gmp-dev         icu-dev         imagemagick-dev         libevent-dev         libjpeg-turbo-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libwebp-dev         libxml2-dev         libzip-dev         openldap-dev         pcre-dev         postgresql-dev     ;         docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap;     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.24;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.0;     pecl install memcached-3.3.0         --configureoptions 'enable-memcached-igbinary="yes"';     pecl install redis-6.2.0         --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"';         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .nextcloud-phpext-rundeps $runDeps;     apk del --no-network .build-deps # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Fri, 18 Apr 2025 15:01:40 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
VOLUME [/var/www/html]
# Fri, 18 Apr 2025 15:01:40 GMT
ENV NEXTCLOUD_VERSION=31.0.4
# Fri, 18 Apr 2025 15:01:40 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-31.0.4.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-31.0.4.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com  --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;     apk del --no-network .fetch-deps # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
COPY *.sh upgrade.exclude / # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Apr 2025 15:01:40 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee7560caccbd432ecca159038f0b286f2c0b02efec5546bf18a775ad0e99486`  
		Last Modified: Fri, 14 Feb 2025 20:02:54 GMT  
		Size: 3.3 MB (3309064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9633ce950391c85eec86506afa8a80635896647c5785246258ef925ff53571b2`  
		Last Modified: Fri, 14 Feb 2025 20:02:54 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25cec00a4490a77b96f81fdbda726d926b9b6c604919f947a6b1af7adfd131e9`  
		Last Modified: Fri, 14 Feb 2025 20:02:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e464dc24629b41a36e4014199e2ebcdd14caea91d97b307cbf44176e5bdd84`  
		Last Modified: Fri, 09 May 2025 17:26:26 GMT  
		Size: 12.6 MB (12587275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28f79ad8227d0aa6fc5cac080093c8af20a219dd62a32ec16c6b09040521dae`  
		Last Modified: Fri, 09 May 2025 17:26:25 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee75c6e547f77fcf1771c6a94975f2aa428a70e5f6081f1a68ca63726b2a40b7`  
		Last Modified: Fri, 09 May 2025 17:33:26 GMT  
		Size: 12.7 MB (12725039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed8008d688a9e9faa34b3a4b2d121f9f0bcb38aa151e83a5631d92441732731`  
		Last Modified: Fri, 09 May 2025 17:33:25 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a73756cfe9bc675de7bb64aceafe803c0246f3dba80753fd695d5b2450ee70`  
		Last Modified: Fri, 09 May 2025 17:33:25 GMT  
		Size: 19.9 KB (19861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e09d689f863b868ffa5d84c00264a30abe55804d9df1cd75471fb8cc468278`  
		Last Modified: Fri, 09 May 2025 17:33:26 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f28625f54d6012c7379503c0530e9e48f64b08bf57abc0ef10b0cc8215a460`  
		Last Modified: Fri, 09 May 2025 18:35:37 GMT  
		Size: 37.7 MB (37653147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4976ca8e05bf80f812314c3fd31f392290451a1f6b9d2e81de24cb77740970`  
		Last Modified: Fri, 09 May 2025 18:35:36 GMT  
		Size: 6.9 MB (6891938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0983df5f1f35654a18091d095e300b10876343213aeb4738a497d86bf95bad`  
		Last Modified: Fri, 09 May 2025 18:35:36 GMT  
		Size: 794.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb092fec13e4290b4f7627f37b22dff5e4fdc072ee1c3ad419564e23895a1757`  
		Last Modified: Fri, 09 May 2025 18:37:41 GMT  
		Size: 246.3 MB (246306357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28a634cfb822f87a02408ff20dedaf4d7ddaea5d51575c55d17a95e0d002db0`  
		Last Modified: Fri, 09 May 2025 18:37:34 GMT  
		Size: 4.0 KB (4046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef17c7de3fdc8115267d1d89a615b9235f734e5f499023d2b7b864e9aca62114`  
		Last Modified: Fri, 09 May 2025 18:37:34 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:fpm-alpine` - unknown; unknown

```console
$ docker pull nextcloud@sha256:2126ccdcd81448db5351088fb9f994fd79d17095912743461ccdca280d3dacbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 KB (44701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5081d1ed1db476fb8799c73e171d4dc7e33bbaa7f6ce07771600416821de3cbe`

```dockerfile
```

-	Layers:
	-	`sha256:ed51c750e448d76bcd8ccf6ec1562386d372ce28a1c25a3123c7c9176f667619`  
		Last Modified: Fri, 09 May 2025 18:37:34 GMT  
		Size: 44.7 KB (44701 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:fpm-alpine` - linux; arm variant v7

```console
$ docker pull nextcloud@sha256:dce4d1eea89054c927f4a95875c45cffdd850db9caded4ce042dda23b6c4cd25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.7 MB (320705278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa55754b6b83a76b778da0d64685f6afda042ee41e54ca69cfba3297df236424`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 18 Apr 2025 15:01:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 18 Apr 2025 15:01:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 18 Apr 2025 15:01:40 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_VERSION=8.3.21
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.21.tar.xz.asc
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_SHA256=4dfb329f209a552c3716394fc123bb62e80a468b55ce27fc8cb0fd5f30b9dcd6
# Fri, 18 Apr 2025 15:01:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 18 Apr 2025 15:01:40 GMT
WORKDIR /var/www/html
# Fri, 18 Apr 2025 15:01:40 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
STOPSIGNAL SIGQUIT
# Fri, 18 Apr 2025 15:01:40 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 18 Apr 2025 15:01:40 GMT
CMD ["php-fpm"]
# Fri, 18 Apr 2025 15:01:40 GMT
RUN set -ex;         apk add --no-cache         imagemagick         imagemagick-pdf         imagemagick-jpeg         imagemagick-raw         imagemagick-tiff         imagemagick-heic         imagemagick-webp         imagemagick-svg         rsync     ;         rm /var/spool/cron/crontabs/root;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         autoconf         freetype-dev         gmp-dev         icu-dev         imagemagick-dev         libevent-dev         libjpeg-turbo-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libwebp-dev         libxml2-dev         libzip-dev         openldap-dev         pcre-dev         postgresql-dev     ;         docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap;     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.24;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.0;     pecl install memcached-3.3.0         --configureoptions 'enable-memcached-igbinary="yes"';     pecl install redis-6.2.0         --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"';         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .nextcloud-phpext-rundeps $runDeps;     apk del --no-network .build-deps # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Fri, 18 Apr 2025 15:01:40 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
VOLUME [/var/www/html]
# Fri, 18 Apr 2025 15:01:40 GMT
ENV NEXTCLOUD_VERSION=31.0.4
# Fri, 18 Apr 2025 15:01:40 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-31.0.4.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-31.0.4.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com  --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;     apk del --no-network .fetch-deps # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
COPY *.sh upgrade.exclude / # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Apr 2025 15:01:40 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f58037841180f7071b0cb17f16a917752d43e658ee1f1d1590b910d941697a3`  
		Last Modified: Fri, 14 Feb 2025 19:44:47 GMT  
		Size: 3.1 MB (3120400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03b42d7db9fed02f8be351555a7c1cb492e5de9aeba350f89727c645ea19994`  
		Last Modified: Fri, 14 Feb 2025 19:44:47 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9997ea5283ca84c2230478f14c34317ce0e2df8d2463a0535910174e4ed66809`  
		Last Modified: Fri, 14 Feb 2025 19:44:47 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15d4327302ecb15e267cc401b84aed3031a22b8216c6c70ead677fa06747b8c7`  
		Last Modified: Fri, 09 May 2025 18:19:23 GMT  
		Size: 12.6 MB (12587281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd0fd851e14e93ed6f968c5a1663f252d67fa2fa036f18b718999327e0f8ec3`  
		Last Modified: Fri, 09 May 2025 18:19:22 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bdf192f61a6602326166cd07b04b518c8f84fcf61037ff21a87fb06ea92f9d`  
		Last Modified: Fri, 09 May 2025 18:22:53 GMT  
		Size: 12.0 MB (11971239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb35feb904fa9467e8c6c63b494b7ede417256fde3ee581395d7234c84ef4aec`  
		Last Modified: Fri, 09 May 2025 18:22:52 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77d15f815185427013b34399653d48a897468ad8aa1b0e577e03137e9790faf6`  
		Last Modified: Fri, 09 May 2025 18:22:53 GMT  
		Size: 19.9 KB (19869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858a70af72159deb93843f9740b64a71d0a3ac364b69478fedf0f9fb1dcec311`  
		Last Modified: Fri, 09 May 2025 18:22:53 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d97a72cfefcceaddcb9eec9a061dab47d56f574e88d5da28b5552e3d419814`  
		Last Modified: Fri, 09 May 2025 20:36:50 GMT  
		Size: 36.7 MB (36718601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48c100084e7355fe40da4caabd9f0a7eba6ab7159655eb5b7a6a242467c5d58`  
		Last Modified: Fri, 09 May 2025 20:36:49 GMT  
		Size: 6.9 MB (6862994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:392bc65d02ac85a85dae6bcbd0fec5e3d11b1bdea6610928f29c36ee6b7cd7b2`  
		Last Modified: Fri, 09 May 2025 20:36:48 GMT  
		Size: 789.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2b472cfbccfb13e9e77c9a3995b019975b58ae87ceea2ecdb069641c1b3611`  
		Last Modified: Fri, 09 May 2025 20:43:01 GMT  
		Size: 246.3 MB (246306280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:338948913809b59b1a55b0442778d0401937e11393485aa97337330bbefdffe1`  
		Last Modified: Fri, 09 May 2025 20:42:55 GMT  
		Size: 4.0 KB (4046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b3707ebcf992ff188f6db6c978bafd94fd1eb7dd3025e72b9ab8eebf2f929fa`  
		Last Modified: Fri, 09 May 2025 20:42:55 GMT  
		Size: 2.4 KB (2352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:fpm-alpine` - unknown; unknown

```console
$ docker pull nextcloud@sha256:114cb7ce8d4394d414cb46f245f1b540773b23da1fff6264a7b901fbb5962684
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 KB (44701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c80744f25d94fc86839aff97ca9d64778d6efd97bde4c8c33fd74fd829da659`

```dockerfile
```

-	Layers:
	-	`sha256:7e432807507bf7697e20ec8fee432d0a90bac898b1850e7ad8cf36d31483a5da`  
		Last Modified: Fri, 09 May 2025 20:42:54 GMT  
		Size: 44.7 KB (44701 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull nextcloud@sha256:17273796c053de0cb50ca226ac2e5931bf73bd16a6d61bffa88f57ae3246daab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.6 MB (331570566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e63a9c55c88547393851d6170e9f3acc1e7ccee538ba6cc53a30640148a3a1a8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 18 Apr 2025 15:01:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 18 Apr 2025 15:01:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 18 Apr 2025 15:01:40 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_VERSION=8.3.21
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.21.tar.xz.asc
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_SHA256=4dfb329f209a552c3716394fc123bb62e80a468b55ce27fc8cb0fd5f30b9dcd6
# Fri, 18 Apr 2025 15:01:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 18 Apr 2025 15:01:40 GMT
WORKDIR /var/www/html
# Fri, 18 Apr 2025 15:01:40 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
STOPSIGNAL SIGQUIT
# Fri, 18 Apr 2025 15:01:40 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 18 Apr 2025 15:01:40 GMT
CMD ["php-fpm"]
# Fri, 18 Apr 2025 15:01:40 GMT
RUN set -ex;         apk add --no-cache         imagemagick         imagemagick-pdf         imagemagick-jpeg         imagemagick-raw         imagemagick-tiff         imagemagick-heic         imagemagick-webp         imagemagick-svg         rsync     ;         rm /var/spool/cron/crontabs/root;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         autoconf         freetype-dev         gmp-dev         icu-dev         imagemagick-dev         libevent-dev         libjpeg-turbo-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libwebp-dev         libxml2-dev         libzip-dev         openldap-dev         pcre-dev         postgresql-dev     ;         docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap;     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.24;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.0;     pecl install memcached-3.3.0         --configureoptions 'enable-memcached-igbinary="yes"';     pecl install redis-6.2.0         --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"';         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .nextcloud-phpext-rundeps $runDeps;     apk del --no-network .build-deps # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Fri, 18 Apr 2025 15:01:40 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
VOLUME [/var/www/html]
# Fri, 18 Apr 2025 15:01:40 GMT
ENV NEXTCLOUD_VERSION=31.0.4
# Fri, 18 Apr 2025 15:01:40 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-31.0.4.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-31.0.4.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com  --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;     apk del --no-network .fetch-deps # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
COPY *.sh upgrade.exclude / # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Apr 2025 15:01:40 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5752b27585c21531ef183f9331718681f7d5a399ad1721fe17bf65ec91aa026d`  
		Last Modified: Thu, 08 May 2025 22:34:00 GMT  
		Size: 3.3 MB (3332291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c504757a74563c6c69cb5f5ab95d450088933adf663323509ef07a437fda44`  
		Last Modified: Thu, 08 May 2025 22:34:00 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64969c8e6dd0ea68ca6e1a455172bdc1ce583b5d543fc3120d33f200e06302a1`  
		Last Modified: Thu, 08 May 2025 22:34:00 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3db65a67aecb67d45a8d2a0a98aeee16d655b6e43c478f269185aa9040efa8`  
		Last Modified: Fri, 09 May 2025 18:20:15 GMT  
		Size: 12.6 MB (12587295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:828a623ccf0e2df458dfd0a527615245460c2cae04ada176c33d75aca519ad85`  
		Last Modified: Fri, 09 May 2025 18:20:14 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:511dace11188dd3aa6fee198101d942f8919c611dcf8f1493e2b4971a6c56e85`  
		Last Modified: Fri, 09 May 2025 18:25:22 GMT  
		Size: 13.2 MB (13241986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc62bfcd88a322d2853d744d09b443df7ba4eab19619eb2ff0192ca38eed33c7`  
		Last Modified: Fri, 09 May 2025 18:25:21 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5cd24690fef5e37e75077913c400c931a210df574ac144af1e8a3bf1c6da8c`  
		Last Modified: Fri, 09 May 2025 18:25:21 GMT  
		Size: 19.9 KB (19854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:233788e5753d83cfd06da6b6fcf5b6d1f9e543b40d032d274616d76264681840`  
		Last Modified: Fri, 09 May 2025 18:25:21 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f400814c23c396acb9a65d7775a64270429f6277af3db5bb87578f78e98a4b4`  
		Last Modified: Fri, 09 May 2025 21:29:39 GMT  
		Size: 44.3 MB (44296256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3bc05d1f7851bf137d3a45134c0caf78f59cd89128fa967b336207d236a8a1`  
		Last Modified: Fri, 09 May 2025 21:29:38 GMT  
		Size: 7.8 MB (7772898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b4cfe9c8adcbc3b9efe5b918b70de3d9c4c4eb9639171b6c84cb6ca51f62d7`  
		Last Modified: Fri, 09 May 2025 21:29:38 GMT  
		Size: 786.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913c25e69dc086f2d4c705bf36943ffcf1e152f1db66d8cac4c8189fa9f850ce`  
		Last Modified: Fri, 09 May 2025 21:29:43 GMT  
		Size: 246.3 MB (246306463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f4605b314e996d091a764dcdef50f59bc60497371864599a704de9fe9e161c6`  
		Last Modified: Fri, 09 May 2025 21:29:39 GMT  
		Size: 4.0 KB (4046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d104c20ec5415ffd5e88b06cd481a8ff22295bc808dc70b0ac1e5d9b86da30`  
		Last Modified: Fri, 09 May 2025 21:29:39 GMT  
		Size: 2.4 KB (2353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:fpm-alpine` - unknown; unknown

```console
$ docker pull nextcloud@sha256:d7eea0b48c23557280b24683442050280d7763d6fe725b8de04b0aa043140654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 KB (44743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:446030c1328c8180f3c5644b81706404f949d89efc0518fed433d7e3e25b7d38`

```dockerfile
```

-	Layers:
	-	`sha256:dabde34efe6438b8671f970d8dbc6b86ed71e54d2ba137cb2ca3a1799634e29a`  
		Last Modified: Fri, 09 May 2025 21:29:37 GMT  
		Size: 44.7 KB (44743 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:fpm-alpine` - linux; 386

```console
$ docker pull nextcloud@sha256:7085faaf635fc83c18d8a7ed4236b224af054cde49ab3f692ddfc3c0e5e70367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.0 MB (329002423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d5067ca21da2f9564e6755b8980d4c21a02c40d799e72e8e1eb51c9a332a17`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 18 Apr 2025 15:01:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 18 Apr 2025 15:01:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 18 Apr 2025 15:01:40 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_VERSION=8.3.21
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.21.tar.xz.asc
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_SHA256=4dfb329f209a552c3716394fc123bb62e80a468b55ce27fc8cb0fd5f30b9dcd6
# Fri, 18 Apr 2025 15:01:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 18 Apr 2025 15:01:40 GMT
WORKDIR /var/www/html
# Fri, 18 Apr 2025 15:01:40 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
STOPSIGNAL SIGQUIT
# Fri, 18 Apr 2025 15:01:40 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 18 Apr 2025 15:01:40 GMT
CMD ["php-fpm"]
# Fri, 18 Apr 2025 15:01:40 GMT
RUN set -ex;         apk add --no-cache         imagemagick         imagemagick-pdf         imagemagick-jpeg         imagemagick-raw         imagemagick-tiff         imagemagick-heic         imagemagick-webp         imagemagick-svg         rsync     ;         rm /var/spool/cron/crontabs/root;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         autoconf         freetype-dev         gmp-dev         icu-dev         imagemagick-dev         libevent-dev         libjpeg-turbo-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libwebp-dev         libxml2-dev         libzip-dev         openldap-dev         pcre-dev         postgresql-dev     ;         docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap;     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.24;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.0;     pecl install memcached-3.3.0         --configureoptions 'enable-memcached-igbinary="yes"';     pecl install redis-6.2.0         --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"';         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .nextcloud-phpext-rundeps $runDeps;     apk del --no-network .build-deps # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Fri, 18 Apr 2025 15:01:40 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
VOLUME [/var/www/html]
# Fri, 18 Apr 2025 15:01:40 GMT
ENV NEXTCLOUD_VERSION=31.0.4
# Fri, 18 Apr 2025 15:01:40 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-31.0.4.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-31.0.4.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com  --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;     apk del --no-network .fetch-deps # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
COPY *.sh upgrade.exclude / # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Apr 2025 15:01:40 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de926c45de6fd2061cb3f5cf9061a214b74c9aa42e93900833c5142b58874723`  
		Last Modified: Fri, 09 May 2025 17:26:40 GMT  
		Size: 3.4 MB (3379891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4fa5c4391c4caaf54388c15e110b96f1a9e108d4275abdc5773073ddb8d6e2`  
		Last Modified: Fri, 09 May 2025 17:26:40 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8735041113b5b7fedd75e4ba8c6e39c35baf6b70078e3fc7b4d5a998b97dcf3`  
		Last Modified: Fri, 09 May 2025 17:26:40 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cb8997ea5e14185126819258d78cc550f8338edbc1c8f7f607d01bd206f7725`  
		Last Modified: Fri, 09 May 2025 17:26:41 GMT  
		Size: 12.6 MB (12587274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6909a6be219011bcd23d0bb7ee9a9e15437e416f3546d46ca56ced88b6d17294`  
		Last Modified: Fri, 09 May 2025 17:26:41 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb26b81a339e58ceb89298afc50bf8bb13195ea73f447368a7e0742893d73d5`  
		Last Modified: Fri, 09 May 2025 17:26:42 GMT  
		Size: 13.6 MB (13561418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403188f37afc393757245ab12a3efd507cb79e18f5b190ecaac99df31f2032ae`  
		Last Modified: Fri, 09 May 2025 17:26:41 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3181be72267116dfc4b67197761257d5ac9639a60dcb217f8a11373dcadb4e98`  
		Last Modified: Fri, 09 May 2025 17:26:42 GMT  
		Size: 20.0 KB (20044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303ca17e2b05cc24f3e6774221e56503062b9451625ac27489e32cf12f25652f`  
		Last Modified: Fri, 09 May 2025 17:26:42 GMT  
		Size: 9.2 KB (9176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4fb209ed7392be7430b1b9abe19a5a913c89141038e7068a88bfd7df441f5dd`  
		Last Modified: Fri, 09 May 2025 17:38:12 GMT  
		Size: 42.0 MB (42015313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d06c17d43cb395c153d3b359c0bc355f13449f08c59b6a2636bfd217dc0f05d`  
		Last Modified: Fri, 09 May 2025 17:38:11 GMT  
		Size: 7.6 MB (7648395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81be4d7b1ee913842e42231c1bb56ad5ca226a8ab4b063c1729bb25ed72f01af`  
		Last Modified: Fri, 09 May 2025 17:38:11 GMT  
		Size: 783.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ddcbbebc2fe274cafb243861ec38094b63c3decb25f8f59381f6cd92652eae`  
		Last Modified: Fri, 09 May 2025 17:38:16 GMT  
		Size: 246.3 MB (246305994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a837832b43071f1a04e08bec3e0497cfdd722613091cb0e0ed8e9bab5e2b5e`  
		Last Modified: Fri, 09 May 2025 17:38:12 GMT  
		Size: 4.0 KB (4047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b5511c6129a48d67915bb70fc2de152d32de85b1d65de6238a1bf6b87901a69`  
		Last Modified: Fri, 09 May 2025 17:38:12 GMT  
		Size: 2.4 KB (2354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:fpm-alpine` - unknown; unknown

```console
$ docker pull nextcloud@sha256:dbe379b2f86a796c4c2b2d5a311fd614e1fa19e699a318d60b5d40a589aea5e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.5 KB (44522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd10b7a1244a9b29bf39c0c0523618273ccaf80f30d43ba5d4f24af83a27dfc`

```dockerfile
```

-	Layers:
	-	`sha256:bcb0c7472b9da09c84bb14e214f6fe3306c494842583af381f7674880b67d4fe`  
		Last Modified: Fri, 09 May 2025 17:38:10 GMT  
		Size: 44.5 KB (44522 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:fpm-alpine` - linux; ppc64le

```console
$ docker pull nextcloud@sha256:ed4e3e9e9c15381fd2cda8355d8dc6a8822176222bdf604cf415b15a45198957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.7 MB (336651611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf19b77db471578da9af0492476816fd993106cc39945133d61ffb3e23d73cc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 18 Apr 2025 15:01:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 18 Apr 2025 15:01:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 18 Apr 2025 15:01:40 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_VERSION=8.3.21
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.21.tar.xz.asc
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_SHA256=4dfb329f209a552c3716394fc123bb62e80a468b55ce27fc8cb0fd5f30b9dcd6
# Fri, 18 Apr 2025 15:01:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 18 Apr 2025 15:01:40 GMT
WORKDIR /var/www/html
# Fri, 18 Apr 2025 15:01:40 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
STOPSIGNAL SIGQUIT
# Fri, 18 Apr 2025 15:01:40 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 18 Apr 2025 15:01:40 GMT
CMD ["php-fpm"]
# Fri, 18 Apr 2025 15:01:40 GMT
RUN set -ex;         apk add --no-cache         imagemagick         imagemagick-pdf         imagemagick-jpeg         imagemagick-raw         imagemagick-tiff         imagemagick-heic         imagemagick-webp         imagemagick-svg         rsync     ;         rm /var/spool/cron/crontabs/root;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         autoconf         freetype-dev         gmp-dev         icu-dev         imagemagick-dev         libevent-dev         libjpeg-turbo-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libwebp-dev         libxml2-dev         libzip-dev         openldap-dev         pcre-dev         postgresql-dev     ;         docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap;     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.24;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.0;     pecl install memcached-3.3.0         --configureoptions 'enable-memcached-igbinary="yes"';     pecl install redis-6.2.0         --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"';         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .nextcloud-phpext-rundeps $runDeps;     apk del --no-network .build-deps # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Fri, 18 Apr 2025 15:01:40 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
VOLUME [/var/www/html]
# Fri, 18 Apr 2025 15:01:40 GMT
ENV NEXTCLOUD_VERSION=31.0.4
# Fri, 18 Apr 2025 15:01:40 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-31.0.4.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-31.0.4.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com  --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;     apk del --no-network .fetch-deps # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
COPY *.sh upgrade.exclude / # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Apr 2025 15:01:40 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b0c526beb901f3bef02cf410e0d947ea692436a5dbc5258b999b61fcd3f138`  
		Last Modified: Fri, 14 Feb 2025 19:49:03 GMT  
		Size: 3.5 MB (3481114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0f40451f4984088d9122ed91962de6fe91c34c09944da85f4c5c0b7bebf552`  
		Last Modified: Fri, 14 Feb 2025 19:49:02 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08e0c24d8ed4f70ce3641f51d7fb3e73e1e18d70e33576240bae71133a633b9`  
		Last Modified: Fri, 14 Feb 2025 19:49:02 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c81bf0bc0310a039db773ba58497f114a3bc66b577bd85eddf0a8e483a2cd8`  
		Last Modified: Fri, 09 May 2025 17:46:41 GMT  
		Size: 12.6 MB (12587282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aed60dbe6fbf6a6397cfeb008e8cefdf60b1b42606dfcd7b2cef71bbf9115486`  
		Last Modified: Fri, 09 May 2025 17:46:40 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3404f4f5649f9b6fe5caacbf582c1772b446412ce40b249a3dd1a0ee494efc3e`  
		Last Modified: Fri, 09 May 2025 17:50:13 GMT  
		Size: 14.6 MB (14557299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:843ec98711dbe17425573f526b250e1dc586bb198723d10998ecef3606701527`  
		Last Modified: Fri, 09 May 2025 17:50:12 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1b8e516277bde2af9ad6bd54806a7b73f11fadc39a718d828514a40157a247`  
		Last Modified: Fri, 09 May 2025 17:50:12 GMT  
		Size: 19.8 KB (19849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0aa29030d9e890fc0f6ed1477324a57a76cbe2edf69681bc382b01a021d2853`  
		Last Modified: Fri, 09 May 2025 17:50:12 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c6d25e9e821d5efe1232689bed195b56d0382788e14e7b750d164e500dc4e75`  
		Last Modified: Fri, 09 May 2025 21:08:53 GMT  
		Size: 48.7 MB (48725231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c446ac26807aa6dd457a5c439e3c83dc2f21b5b1904fdb6a379f9b8245a690a6`  
		Last Modified: Fri, 09 May 2025 21:08:52 GMT  
		Size: 7.4 MB (7379611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a21e32ad57fc30138dacc31c6b56a2f41339f51ab1b790715f1656fe882433`  
		Last Modified: Fri, 09 May 2025 21:08:51 GMT  
		Size: 789.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2295a97f256b76f7f87b329ec5578d242513382dc79e8e91f6c0bcd7226d9e3f`  
		Last Modified: Fri, 09 May 2025 21:09:01 GMT  
		Size: 246.3 MB (246306379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6e84af918e0880eda1eeb5d44cffaba92d06c8bba4c342f85002c2dd49cde0`  
		Last Modified: Fri, 09 May 2025 21:08:52 GMT  
		Size: 4.0 KB (4047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28894fedcc63943149d554acdca2c886716f864f01704de80179812259237e99`  
		Last Modified: Fri, 09 May 2025 21:08:53 GMT  
		Size: 2.4 KB (2355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:fpm-alpine` - unknown; unknown

```console
$ docker pull nextcloud@sha256:d057cb02e6269b2a81e0ca1b690171bb5d17cd71157c0bf4edf724ef35d8d187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.6 KB (44632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbd5bb7400ced6516cad7c03f1dfdf33b2c82bce98a9a7e614486bdde95f1bd4`

```dockerfile
```

-	Layers:
	-	`sha256:470944ac10a78b025d990f7f23bf142772ca63e71bf2b5011a5c9be4731df2aa`  
		Last Modified: Fri, 09 May 2025 21:08:51 GMT  
		Size: 44.6 KB (44632 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:fpm-alpine` - linux; riscv64

```console
$ docker pull nextcloud@sha256:f4981847ea849ddead8e2be522f0384ec8edf928b9e390e99b89c44f96af6584
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.0 MB (327952863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24ec8bce99f4f46664de3f8206130e6b237d152fdb9aa7887b8e3889f89469bf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 10 Apr 2025 18:46:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 10 Apr 2025 18:46:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 10 Apr 2025 18:46:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 10 Apr 2025 18:46:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 10 Apr 2025 18:46:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 10 Apr 2025 18:46:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 10 Apr 2025 18:46:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 10 Apr 2025 18:46:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 10 Apr 2025 18:46:32 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 10 Apr 2025 18:46:32 GMT
ENV PHP_VERSION=8.3.20
# Thu, 10 Apr 2025 18:46:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.20.tar.xz.asc
# Thu, 10 Apr 2025 18:46:32 GMT
ENV PHP_SHA256=f15914e071b5bddaf1475b5f2ba68107e8b8846655f9e89690fb7cd410b0db6c
# Thu, 10 Apr 2025 18:46:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 10 Apr 2025 18:46:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 18:46:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 10 Apr 2025 18:46:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 10 Apr 2025 18:46:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 10 Apr 2025 18:46:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 10 Apr 2025 18:46:32 GMT
WORKDIR /var/www/html
# Thu, 10 Apr 2025 18:46:32 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 10 Apr 2025 18:46:32 GMT
STOPSIGNAL SIGQUIT
# Thu, 10 Apr 2025 18:46:32 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 10 Apr 2025 18:46:32 GMT
CMD ["php-fpm"]
# Fri, 18 Apr 2025 15:01:40 GMT
RUN set -ex;         apk add --no-cache         imagemagick         imagemagick-pdf         imagemagick-jpeg         imagemagick-raw         imagemagick-tiff         imagemagick-heic         imagemagick-webp         imagemagick-svg         rsync     ;         rm /var/spool/cron/crontabs/root;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         autoconf         freetype-dev         gmp-dev         icu-dev         imagemagick-dev         libevent-dev         libjpeg-turbo-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libwebp-dev         libxml2-dev         libzip-dev         openldap-dev         pcre-dev         postgresql-dev     ;         docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap;     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.24;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.0;     pecl install memcached-3.3.0         --configureoptions 'enable-memcached-igbinary="yes"';     pecl install redis-6.2.0         --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"';         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .nextcloud-phpext-rundeps $runDeps;     apk del --no-network .build-deps # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Fri, 18 Apr 2025 15:01:40 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
VOLUME [/var/www/html]
# Fri, 18 Apr 2025 15:01:40 GMT
ENV NEXTCLOUD_VERSION=31.0.4
# Fri, 18 Apr 2025 15:01:40 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-31.0.4.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-31.0.4.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com  --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;     apk del --no-network .fetch-deps # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
COPY *.sh upgrade.exclude / # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Apr 2025 15:01:40 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75a14eca9423f582254c3b4d8d658ea4f006113a3355a1688bdbc6bac3eb770`  
		Last Modified: Sat, 15 Feb 2025 00:30:36 GMT  
		Size: 3.5 MB (3462944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8a148fbb1301ad573d1000e2ec04300c75cbfc42b27312197cb623017dae4d`  
		Last Modified: Sat, 15 Feb 2025 00:30:35 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5298f8d578c92ab374fdbb481a72f1557c4e7a726be21e513d65f51dd957cf`  
		Last Modified: Sat, 15 Feb 2025 00:30:35 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80820c17f015ea81e511c1df3373b1f59aa53f9bec86fdd662d1907469b8a101`  
		Last Modified: Sat, 12 Apr 2025 00:03:00 GMT  
		Size: 12.6 MB (12569999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6332bbe81ac07672f371c0d47a75e79e67ca211f7bde76e8a3c184828d4ea34d`  
		Last Modified: Sat, 12 Apr 2025 00:02:58 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13da7d7084851fa2fbba41d077393f99a088e0d06303761347f49b1b1ce370c`  
		Last Modified: Sat, 12 Apr 2025 01:01:47 GMT  
		Size: 13.5 MB (13533090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b9e5fb39849ce8d312fe3cdcba2bbdf36a90f01711c61035e5acffd076c55e`  
		Last Modified: Sat, 12 Apr 2025 01:01:44 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be9515f8021d2d316be61d32d1a3c6062f68b3d3a3113971ecacce24119dd060`  
		Last Modified: Sat, 12 Apr 2025 01:01:45 GMT  
		Size: 19.8 KB (19842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b96ba08731b78ce642a24ccc66d0c782cef1819d58cb84646282a29a9964f15`  
		Last Modified: Sat, 12 Apr 2025 01:01:45 GMT  
		Size: 9.2 KB (9185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc59bc57cb51cdd408013a07a49c9117ee3838c8d6b27a8aaf2cbb7f7afcca3a`  
		Last Modified: Mon, 21 Apr 2025 23:20:08 GMT  
		Size: 40.8 MB (40826508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe388db4dcf8826f8a90014caa021ef263d39333b977e14c73c0e67347a21b7`  
		Last Modified: Mon, 21 Apr 2025 23:20:04 GMT  
		Size: 7.9 MB (7862609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c00a3334123ea641a84b8bb2c725ee5b3e84987d5d7db611bea0e091a94b14f`  
		Last Modified: Mon, 21 Apr 2025 23:20:02 GMT  
		Size: 794.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8ed4942269f5a4b1a4ba00a4ff10537bebb834544079530eb85cefc98d91a8`  
		Last Modified: Mon, 21 Apr 2025 23:31:19 GMT  
		Size: 246.3 MB (246305918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d014ce094254dda220e118e2264ed7496aea95c2ff3fc69cc705582a356965`  
		Last Modified: Mon, 21 Apr 2025 23:30:45 GMT  
		Size: 4.0 KB (4047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02b3e479df8b5e01ec9ff22e16ee631723d094f3bb5f323e1c164ff50494403`  
		Last Modified: Mon, 21 Apr 2025 23:30:45 GMT  
		Size: 2.4 KB (2357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:fpm-alpine` - unknown; unknown

```console
$ docker pull nextcloud@sha256:7a7a5d68ea3859dcc90b3c6bee0dcbdee431d4e0abd32c5b6515bca151acef45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.6 KB (44632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea365b9b4e764a5956d56b63ad0b2682e6ee6b10a4c8e33d37c3fcf87e6b245e`

```dockerfile
```

-	Layers:
	-	`sha256:fef9311692303e36759649fcd3386c4bf338da9d5710149d145e2c047e9ba0d6`  
		Last Modified: Mon, 21 Apr 2025 23:30:45 GMT  
		Size: 44.6 KB (44632 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:fpm-alpine` - linux; s390x

```console
$ docker pull nextcloud@sha256:c86631ee26e54712d6b8522234ca302335efbe808b3d0fdc2d0c3682423297b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.3 MB (334260190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:810b68c752f3d0ff6af428ec287189c3937565e76fe8067448e34afe83fed55c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 18 Apr 2025 15:01:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 18 Apr 2025 15:01:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 18 Apr 2025 15:01:40 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_VERSION=8.3.21
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.21.tar.xz.asc
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_SHA256=4dfb329f209a552c3716394fc123bb62e80a468b55ce27fc8cb0fd5f30b9dcd6
# Fri, 18 Apr 2025 15:01:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 18 Apr 2025 15:01:40 GMT
WORKDIR /var/www/html
# Fri, 18 Apr 2025 15:01:40 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
STOPSIGNAL SIGQUIT
# Fri, 18 Apr 2025 15:01:40 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 18 Apr 2025 15:01:40 GMT
CMD ["php-fpm"]
# Fri, 18 Apr 2025 15:01:40 GMT
RUN set -ex;         apk add --no-cache         imagemagick         imagemagick-pdf         imagemagick-jpeg         imagemagick-raw         imagemagick-tiff         imagemagick-heic         imagemagick-webp         imagemagick-svg         rsync     ;         rm /var/spool/cron/crontabs/root;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         autoconf         freetype-dev         gmp-dev         icu-dev         imagemagick-dev         libevent-dev         libjpeg-turbo-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libwebp-dev         libxml2-dev         libzip-dev         openldap-dev         pcre-dev         postgresql-dev     ;         docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap;     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.24;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.0;     pecl install memcached-3.3.0         --configureoptions 'enable-memcached-igbinary="yes"';     pecl install redis-6.2.0         --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"';         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .nextcloud-phpext-rundeps $runDeps;     apk del --no-network .build-deps # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 18 Apr 2025 15:01:40 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Fri, 18 Apr 2025 15:01:40 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
VOLUME [/var/www/html]
# Fri, 18 Apr 2025 15:01:40 GMT
ENV NEXTCLOUD_VERSION=31.0.4
# Fri, 18 Apr 2025 15:01:40 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-31.0.4.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-31.0.4.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com  --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;     apk del --no-network .fetch-deps # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
COPY *.sh upgrade.exclude / # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Fri, 18 Apr 2025 15:01:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Apr 2025 15:01:40 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa956d396b0345789b0b8754caea46d8279eb9aaef195e5c0751997771bc98b`  
		Last Modified: Fri, 14 Feb 2025 19:52:31 GMT  
		Size: 3.6 MB (3566207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa28a25dd21eb15acefc90a9671a91830929d27b461de939eaa00e611391d4d`  
		Last Modified: Fri, 14 Feb 2025 19:52:31 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd758f782beaedae4bd78b431d2d8eec0ec738f9e5330203a2fb129e7a6b5dda`  
		Last Modified: Fri, 14 Feb 2025 19:52:31 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70fccf6e5e3e9757b126412a5b5818adb3c50fab5919d6cf8ab493ee52c84d8b`  
		Last Modified: Fri, 09 May 2025 17:55:06 GMT  
		Size: 12.6 MB (12587288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e30d07e848c2bc6492508cbfaf94b9556d55aea7e8520ad7c4c33b450486f22d`  
		Last Modified: Fri, 09 May 2025 17:55:05 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87bd1078ee4aff7e802e509d21cf06a62e43b58971291ec91922dd2170cee6d`  
		Last Modified: Fri, 09 May 2025 18:00:40 GMT  
		Size: 14.0 MB (14019960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:861f225cf6fbf6a1183d24589980eac1bcbefb61bff4cc1f035cf2eefdc63786`  
		Last Modified: Fri, 09 May 2025 18:00:39 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e253d78a8bdae47fffb0a7706e2c7e2e58c049b23d3df0c75b9d9151041a010`  
		Last Modified: Fri, 09 May 2025 18:00:39 GMT  
		Size: 19.9 KB (19856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05dcaa31a53399d022fa1cb0a9d9803672ec73d61c7423196e6fcf293499a540`  
		Last Modified: Fri, 09 May 2025 18:00:39 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:789ad12f24d6c36222deb2bb8a26c0ad5806b3b1ec98da69529fa16237b8c72c`  
		Last Modified: Fri, 09 May 2025 20:12:10 GMT  
		Size: 46.9 MB (46946582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4289d9700b159f2e453e4776c33e8377ff8b1c2f645647b2927d35bd6bae724`  
		Last Modified: Fri, 09 May 2025 20:12:08 GMT  
		Size: 7.3 MB (7326436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2d7a8c9d1607c810356e669619f2f4310e319d246e779806ddc70d2ec45aabd`  
		Last Modified: Fri, 09 May 2025 20:12:08 GMT  
		Size: 789.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7008b810ece0f7de3baba96aec92079e89beff8cdc74a9aacdad7db95d345a53`  
		Last Modified: Fri, 09 May 2025 20:12:13 GMT  
		Size: 246.3 MB (246305804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e084e378f5a90f50b4c231028bb6b3decc448918750b815d03015bd57ae3cc35`  
		Last Modified: Fri, 09 May 2025 20:12:09 GMT  
		Size: 4.0 KB (4047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b9e7624857ee0a5bfce6381edf8feabc53a9205cfc19cfd88acc90e21232e7`  
		Last Modified: Fri, 09 May 2025 20:12:10 GMT  
		Size: 2.4 KB (2355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:fpm-alpine` - unknown; unknown

```console
$ docker pull nextcloud@sha256:7a06d2e13469aedadd4d4de17714bb9eba09deebeebff5025f4eff4d3536d914
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.6 KB (44569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92caa427e615f6d111d48949ed2d7f825a5bb8a16b1011a498a997ac2c2ee398`

```dockerfile
```

-	Layers:
	-	`sha256:6407d224d0a2ce3cabeef2047624f76af6adfb0abb8f39ec705cd680bf554674`  
		Last Modified: Fri, 09 May 2025 20:12:08 GMT  
		Size: 44.6 KB (44569 bytes)  
		MIME: application/vnd.in-toto+json
