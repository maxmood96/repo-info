## `nextcloud:26-fpm-alpine`

```console
$ docker pull nextcloud@sha256:f415313925f4d29c0b3f89fd902e5511c82a63f53c97f4784479c06008351c3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `nextcloud:26-fpm-alpine` - linux; amd64

```console
$ docker pull nextcloud@sha256:4242b63c99703621ce873caae728fc6a9ac52e3e5fbaf0b3a63a836154102733
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.3 MB (251268684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:061e2245fec7c7477ca886c160213af4d87cbc8fbd5ecc711e826a3d1e7d7b22`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 00:31:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 Jun 2023 00:31:26 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 15 Jun 2023 00:31:26 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 15 Jun 2023 00:31:26 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 Jun 2023 00:31:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 15 Jun 2023 00:31:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jun 2023 00:31:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jun 2023 00:31:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 Jun 2023 00:54:34 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 15 Jun 2023 00:54:34 GMT
ENV PHP_VERSION=8.2.7
# Thu, 15 Jun 2023 00:54:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.7.tar.xz.asc
# Thu, 15 Jun 2023 00:54:34 GMT
ENV PHP_SHA256=4b9fb3dcd7184fe7582d7e44544ec7c5153852a2528de3b6754791258ffbdfa0
# Thu, 15 Jun 2023 00:54:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 15 Jun 2023 00:54:41 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 15 Jun 2023 01:01:57 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 15 Jun 2023 01:01:57 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 15 Jun 2023 01:01:58 GMT
RUN docker-php-ext-enable sodium
# Thu, 15 Jun 2023 01:01:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 Jun 2023 01:01:58 GMT
WORKDIR /var/www/html
# Thu, 15 Jun 2023 01:01:59 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 15 Jun 2023 01:01:59 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jun 2023 01:01:59 GMT
EXPOSE 9000
# Thu, 15 Jun 2023 01:01:59 GMT
CMD ["php-fpm"]
# Thu, 15 Jun 2023 08:05:13 GMT
RUN set -ex;         apk add --no-cache         imagemagick         rsync     ;         rm /var/spool/cron/crontabs/root;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Thu, 15 Jun 2023 08:07:39 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         autoconf         freetype-dev         gmp-dev         icu-dev         imagemagick-dev         libevent-dev         libjpeg-turbo-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libwebp-dev         libxml2-dev         libzip-dev         openldap-dev         pcre-dev         postgresql-dev     ;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap;     docker-php-ext-install -j "$(nproc)"         bcmath         exif         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.22;     pecl install imagick-3.7.0;     pecl install memcached-3.2.0;     pecl install redis-5.3.7;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .nextcloud-phpext-rundeps $runDeps;     apk del --no-network .build-deps
# Thu, 15 Jun 2023 08:07:39 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 15 Jun 2023 08:07:39 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 23 Jun 2023 18:24:45 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 23 Jun 2023 18:24:45 GMT
VOLUME [/var/www/html]
# Fri, 23 Jun 2023 18:24:45 GMT
ENV NEXTCLOUD_VERSION=26.0.3
# Fri, 23 Jun 2023 18:25:33 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-26.0.3.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-26.0.3.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com  --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;     apk del --no-network .fetch-deps
# Fri, 23 Jun 2023 18:25:35 GMT
COPY multi:f14917ef3f8441cf73a9faa81b54c7e51061a07185e365974d47ddb315426c8f in / 
# Fri, 23 Jun 2023 18:25:35 GMT
COPY multi:1aa0c68034f207c7e2fb6f047fda45b55878afe2781ef10723107e35ee22547e in /usr/src/nextcloud/config/ 
# Fri, 23 Jun 2023 18:25:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 23 Jun 2023 18:25:35 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f034080c2b5d3afb2ec354e2b425f48df6326f28bcf3d2cee4ed50b9721ba482`  
		Last Modified: Thu, 15 Jun 2023 02:07:05 GMT  
		Size: 2.7 MB (2659635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b8701d6f7d5844dd4fa64c17ce3e1999f152f0dbfa3ea704bf38e8617e6b4d5`  
		Last Modified: Thu, 15 Jun 2023 02:07:05 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:259e9197ff8b826653ac60962d424d223ae725c1368f3fbd6efe6853200e945c`  
		Last Modified: Thu, 15 Jun 2023 02:07:04 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a16e442da9b3fb4490b11e4664c414090d1113b974cc31af75dbfb1d5d8c4046`  
		Last Modified: Thu, 15 Jun 2023 02:08:53 GMT  
		Size: 12.0 MB (12037914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82868e6e9750585aa5ba0a2a2583fcf1d82fc3bd489f13340731940955d56483`  
		Last Modified: Thu, 15 Jun 2023 02:08:52 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f1f0c77ff7f88374c8b8d10c73f3b112f9156ce9d6cd73c4e9562fdb747146b`  
		Last Modified: Thu, 15 Jun 2023 02:09:35 GMT  
		Size: 12.7 MB (12693419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21a98cab6dcc360269527e2e4332f204d0d006dfaae8e0f19a649b1a69bf242`  
		Last Modified: Thu, 15 Jun 2023 02:09:33 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756e46c6b2a96d3f31a23077ef6a7a40f6f1d14659fd3be219f0f5540915a7a4`  
		Last Modified: Thu, 15 Jun 2023 02:09:33 GMT  
		Size: 18.9 KB (18937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e1316337e692b14e56fc94be1a648d6c27d37140f6f0a85f8b1b32d9f6564b`  
		Last Modified: Thu, 15 Jun 2023 02:09:33 GMT  
		Size: 9.2 KB (9176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c9439d8c438a66e54b1d732964dae7866b0da0c402c90d8c2ff9aa7ddf4848c`  
		Last Modified: Thu, 15 Jun 2023 08:10:59 GMT  
		Size: 44.9 MB (44905924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8081bb03a24baca78874f863c5e3269b11e541fb189166ce753c2db0e559a737`  
		Last Modified: Thu, 15 Jun 2023 08:10:51 GMT  
		Size: 7.0 MB (6951687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a4b3854f94f5b97e560a658bd5e05b64d3f503edb33ce5c10191ab4c2aed25a`  
		Last Modified: Fri, 23 Jun 2023 18:32:42 GMT  
		Size: 762.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed3a056665f9df8c8e5e93a85950a975bf2e39b0c1e7d66cc596a06fff495e86`  
		Last Modified: Fri, 23 Jun 2023 18:33:01 GMT  
		Size: 168.6 MB (168583180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f26d20947a907ee38140771dd973d7b282613fa16d27f8247a9cffd1c77899d`  
		Last Modified: Fri, 23 Jun 2023 18:32:42 GMT  
		Size: 3.5 KB (3470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d362221ebe2d36366ba9407816ca44401cebd86e30b326b1858f7337a6380ef`  
		Last Modified: Fri, 23 Jun 2023 18:32:42 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:26-fpm-alpine` - linux; arm variant v6

```console
$ docker pull nextcloud@sha256:69f272ba072280178582f3218002c028e34d3e36bdee1af14bb094bceb5f1a0f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.1 MB (245117699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4011eef9e25cbad29662d746d01aba5ed9a6e1284bd7ed215bc1c731f5143d8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 14 Jun 2023 18:49:20 GMT
ADD file:4213782693bf27a9a6de23bc924ef0c4fb6b2d56010fc07b25f81edeba83b0d4 in / 
# Wed, 14 Jun 2023 18:49:20 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 00:03:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 Jun 2023 00:03:56 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 15 Jun 2023 00:03:56 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 15 Jun 2023 00:03:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 Jun 2023 00:03:57 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 15 Jun 2023 00:03:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jun 2023 00:03:57 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jun 2023 00:03:57 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 Jun 2023 00:21:56 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Mon, 10 Jul 2023 20:37:38 GMT
ENV PHP_VERSION=8.2.8
# Mon, 10 Jul 2023 20:37:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.8.tar.xz.asc
# Mon, 10 Jul 2023 20:37:38 GMT
ENV PHP_SHA256=cfe1055fbcd486de7d3312da6146949aae577365808790af6018205567609801
# Mon, 10 Jul 2023 20:37:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Mon, 10 Jul 2023 20:37:47 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Mon, 10 Jul 2023 20:49:41 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Mon, 10 Jul 2023 20:49:42 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Mon, 10 Jul 2023 20:49:43 GMT
RUN docker-php-ext-enable sodium
# Mon, 10 Jul 2023 20:49:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 10 Jul 2023 20:49:43 GMT
WORKDIR /var/www/html
# Mon, 10 Jul 2023 20:49:44 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Mon, 10 Jul 2023 20:49:44 GMT
STOPSIGNAL SIGQUIT
# Mon, 10 Jul 2023 20:49:44 GMT
EXPOSE 9000
# Mon, 10 Jul 2023 20:49:44 GMT
CMD ["php-fpm"]
# Mon, 10 Jul 2023 23:45:17 GMT
RUN set -ex;         apk add --no-cache         imagemagick         rsync     ;         rm /var/spool/cron/crontabs/root;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Mon, 10 Jul 2023 23:47:24 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         autoconf         freetype-dev         gmp-dev         icu-dev         imagemagick-dev         libevent-dev         libjpeg-turbo-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libwebp-dev         libxml2-dev         libzip-dev         openldap-dev         pcre-dev         postgresql-dev     ;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap;     docker-php-ext-install -j "$(nproc)"         bcmath         exif         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.22;     pecl install imagick-3.7.0;     pecl install memcached-3.2.0;     pecl install redis-5.3.7;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .nextcloud-phpext-rundeps $runDeps;     apk del --no-network .build-deps
# Mon, 10 Jul 2023 23:47:24 GMT
ENV PHP_MEMORY_LIMIT=512M
# Mon, 10 Jul 2023 23:47:24 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Mon, 10 Jul 2023 23:47:25 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Mon, 10 Jul 2023 23:47:25 GMT
VOLUME [/var/www/html]
# Mon, 10 Jul 2023 23:47:25 GMT
ENV NEXTCLOUD_VERSION=26.0.3
# Mon, 10 Jul 2023 23:48:19 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-26.0.3.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-26.0.3.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com  --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;     apk del --no-network .fetch-deps
# Mon, 10 Jul 2023 23:48:22 GMT
COPY multi:f14917ef3f8441cf73a9faa81b54c7e51061a07185e365974d47ddb315426c8f in / 
# Mon, 10 Jul 2023 23:48:23 GMT
COPY multi:1aa0c68034f207c7e2fb6f047fda45b55878afe2781ef10723107e35ee22547e in /usr/src/nextcloud/config/ 
# Mon, 10 Jul 2023 23:48:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 10 Jul 2023 23:48:23 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:7836be94d3024e2042069c1095caba0b391f70c4b3d34a0475a503239d73dfba`  
		Last Modified: Wed, 14 Jun 2023 18:49:46 GMT  
		Size: 3.1 MB (3143353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c974e2f4fb5afd0ccf2987ea9cdb17437ec18fae29ffb9fc867ac3086eb74400`  
		Last Modified: Thu, 15 Jun 2023 01:17:09 GMT  
		Size: 2.7 MB (2664702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f64a2d84af76d29961595fccdcdf8d0e78b788f70e833458794d041be66462b5`  
		Last Modified: Thu, 15 Jun 2023 01:17:09 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e225c1eaef0162b3af2e6f6a0e68d0597a6d17226f086e1a5ee69dcd2e5248d`  
		Last Modified: Thu, 15 Jun 2023 01:17:09 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b012f48fc648d11a7873cecf19367f5cf79a397d73b90c41e8cebf0037835964`  
		Last Modified: Mon, 10 Jul 2023 21:54:16 GMT  
		Size: 12.1 MB (12055813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db91b0c8f729c39bf7ca8b77c2eed1813f40567c6e8764af97c83824c518a94`  
		Last Modified: Mon, 10 Jul 2023 21:54:15 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:939f607cb402addbbf5e1c5cfb4a54ab2e65f3429c366f0266fc1d8c122cdcbb`  
		Last Modified: Mon, 10 Jul 2023 21:54:59 GMT  
		Size: 11.6 MB (11609887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:359fa737cb29b8c0561698a57563b545950b6212a27e15133bc228d85729345a`  
		Last Modified: Mon, 10 Jul 2023 21:54:57 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:785bf6bc1325bf0021ab3df2547154d0145549ed90260e518f332a419324ac65`  
		Last Modified: Mon, 10 Jul 2023 21:54:57 GMT  
		Size: 18.8 KB (18754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1caab8dad014d79d3d00b24b10ce1d40ae8e19bd9d0976681e835e65071b9737`  
		Last Modified: Mon, 10 Jul 2023 21:54:57 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13d71419e2494e756c01230b7dade63007524760f405e941befd6d6435bfbd5`  
		Last Modified: Mon, 10 Jul 2023 23:50:51 GMT  
		Size: 40.7 MB (40705590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a46f67a04a416954fb73cfdce58a8e7e0cd99cb9897ab5ac01a36d8bce07017d`  
		Last Modified: Mon, 10 Jul 2023 23:50:41 GMT  
		Size: 6.3 MB (6315981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77991dec2397bfd87def04679b7c015323c87195e3396f4b21265b8a65f31658`  
		Last Modified: Mon, 10 Jul 2023 23:50:39 GMT  
		Size: 760.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f0595dbf4f4d1e72f0f4c62d96048a2c3cc5a3744b6f3839afaf4953d6d7edf`  
		Last Modified: Mon, 10 Jul 2023 23:51:09 GMT  
		Size: 168.6 MB (168583507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24128f28ff9951682ec45a49c7fceffc185819f3e79e8f6eb02c1eb0e806c247`  
		Last Modified: Mon, 10 Jul 2023 23:50:39 GMT  
		Size: 3.5 KB (3468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76db0fd765b33eb91d469779e033f3e0f08a4247a38ac644479d3686fc4901bc`  
		Last Modified: Mon, 10 Jul 2023 23:50:40 GMT  
		Size: 2.2 KB (2222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:26-fpm-alpine` - linux; arm variant v7

```console
$ docker pull nextcloud@sha256:e1228f5b16a1c111d149056a38a202ea2fa8911ab7b57767bf6967a4b7ac4b99
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.7 MB (241736200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a569505de936b092718b0c5207713c270de9abea5fd974bdc9e8c2b80da92c5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 14 Jun 2023 22:36:15 GMT
ADD file:082f034323c559f3cb9feb6422c88b1ec8017f436d6109e238a5c5384a32a90a in / 
# Wed, 14 Jun 2023 22:36:15 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 05:41:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 Jun 2023 05:41:15 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 15 Jun 2023 05:41:16 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 15 Jun 2023 05:41:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 Jun 2023 05:41:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 15 Jun 2023 05:41:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jun 2023 05:41:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jun 2023 05:41:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 Jun 2023 05:57:26 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 15 Jun 2023 05:57:26 GMT
ENV PHP_VERSION=8.2.7
# Thu, 15 Jun 2023 05:57:26 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.7.tar.xz.asc
# Thu, 15 Jun 2023 05:57:26 GMT
ENV PHP_SHA256=4b9fb3dcd7184fe7582d7e44544ec7c5153852a2528de3b6754791258ffbdfa0
# Thu, 15 Jun 2023 05:57:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 15 Jun 2023 05:57:34 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 15 Jun 2023 06:02:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 15 Jun 2023 06:02:25 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 15 Jun 2023 06:02:26 GMT
RUN docker-php-ext-enable sodium
# Thu, 15 Jun 2023 06:02:26 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 Jun 2023 06:02:26 GMT
WORKDIR /var/www/html
# Thu, 15 Jun 2023 06:02:26 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 15 Jun 2023 06:02:26 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jun 2023 06:02:26 GMT
EXPOSE 9000
# Thu, 15 Jun 2023 06:02:26 GMT
CMD ["php-fpm"]
# Thu, 15 Jun 2023 09:41:25 GMT
RUN set -ex;         apk add --no-cache         imagemagick         rsync     ;         rm /var/spool/cron/crontabs/root;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Thu, 15 Jun 2023 09:43:26 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         autoconf         freetype-dev         gmp-dev         icu-dev         imagemagick-dev         libevent-dev         libjpeg-turbo-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libwebp-dev         libxml2-dev         libzip-dev         openldap-dev         pcre-dev         postgresql-dev     ;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap;     docker-php-ext-install -j "$(nproc)"         bcmath         exif         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.22;     pecl install imagick-3.7.0;     pecl install memcached-3.2.0;     pecl install redis-5.3.7;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .nextcloud-phpext-rundeps $runDeps;     apk del --no-network .build-deps
# Thu, 15 Jun 2023 09:43:26 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 15 Jun 2023 09:43:26 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 23 Jun 2023 18:03:14 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 23 Jun 2023 18:03:14 GMT
VOLUME [/var/www/html]
# Fri, 23 Jun 2023 18:03:14 GMT
ENV NEXTCLOUD_VERSION=26.0.3
# Fri, 23 Jun 2023 18:04:08 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-26.0.3.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-26.0.3.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com  --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;     apk del --no-network .fetch-deps
# Fri, 23 Jun 2023 18:04:12 GMT
COPY multi:f14917ef3f8441cf73a9faa81b54c7e51061a07185e365974d47ddb315426c8f in / 
# Fri, 23 Jun 2023 18:04:12 GMT
COPY multi:1aa0c68034f207c7e2fb6f047fda45b55878afe2781ef10723107e35ee22547e in /usr/src/nextcloud/config/ 
# Fri, 23 Jun 2023 18:04:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 23 Jun 2023 18:04:13 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:633ba29fd335042456b6e2c073636f6fa30de56f1331c442914739b92a479974`  
		Last Modified: Wed, 14 Jun 2023 22:36:49 GMT  
		Size: 2.9 MB (2898508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36fcad4bb8996a5b45e9295adfb95c371938b842eb57e046b2913e94204a7f33`  
		Last Modified: Thu, 15 Jun 2023 06:52:24 GMT  
		Size: 2.5 MB (2502362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2cccda84c43168533736f637359fef9f6288fd02a44c5e793caaaa24105477`  
		Last Modified: Thu, 15 Jun 2023 06:52:23 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19901d84d4d52625e92590e32d9e2621e75c0beb01f75489bce2608d20f1c7ba`  
		Last Modified: Thu, 15 Jun 2023 06:52:23 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad4ee4411084b57f61076fbd40a42217fbbbc54afd490573c4a6d7850a44a74e`  
		Last Modified: Thu, 15 Jun 2023 06:54:05 GMT  
		Size: 12.0 MB (12037921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9d5f9155c1ca45d7c577c010490c88cbf92ff3bcc295e37a0e9db8b8b61fb1`  
		Last Modified: Thu, 15 Jun 2023 06:54:04 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a0028c65135e73adc24464b626d6961e2c83017ccbe7f3d4e8166807c8805e`  
		Last Modified: Thu, 15 Jun 2023 06:54:45 GMT  
		Size: 10.8 MB (10845942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894721e2305afcef2a81121af96a9c63df5892eb1c2fcf58f68a2b22a7a18f7c`  
		Last Modified: Thu, 15 Jun 2023 06:54:43 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8357b9bde1222a1fe0d1834dc3d4c65b45220715c47401ac606f1272c21a99`  
		Last Modified: Thu, 15 Jun 2023 06:54:43 GMT  
		Size: 18.8 KB (18762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f4ea6ce5db74f8fec3d3053dec7fe664d71b5711dba6251e738f6beed903616`  
		Last Modified: Thu, 15 Jun 2023 06:54:43 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8788e947279de9cd391fb2674bc8b5509e3cf0750030ae400eaec19ea1bc27c`  
		Last Modified: Thu, 15 Jun 2023 09:46:56 GMT  
		Size: 38.5 MB (38541226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c617d3c15be411fcd046203e45eea8a57f52d6d2ce7b4d1fc9fec4305a452d61`  
		Last Modified: Thu, 15 Jun 2023 09:46:50 GMT  
		Size: 6.3 MB (6287906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17bddb96961aa7da2886951aef37990b1801d68d1ffa8c5be6f06aed267deb88`  
		Last Modified: Fri, 23 Jun 2023 18:12:12 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:433b9378ac697939b7cad3c4f5b470a72b54e462e59403f44d2d2ef9b28a9ff4`  
		Last Modified: Fri, 23 Jun 2023 18:12:37 GMT  
		Size: 168.6 MB (168583469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2639baa84cd9656ff738fc82bcbd4efa8112f942ae63dea7a6bbfe0141b7da8a`  
		Last Modified: Fri, 23 Jun 2023 18:12:12 GMT  
		Size: 3.5 KB (3469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05839476a0beebffd73b70bd841c8594e63ce64491416bdc99809efa1905e758`  
		Last Modified: Fri, 23 Jun 2023 18:12:12 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:26-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull nextcloud@sha256:55d2af4fc8673b3e4ca09ad20e884c29f9c06538629d4ad25851ee6701119c78
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.7 MB (250737769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ee77284a8a709f6d1b2b0343f7af6c9fb1dcb12e237ce09209088d48dcdc952`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 03:05:37 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 Jun 2023 03:05:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 15 Jun 2023 03:05:39 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 15 Jun 2023 03:05:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 Jun 2023 03:05:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 15 Jun 2023 03:05:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jun 2023 03:05:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jun 2023 03:05:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 Jun 2023 03:30:20 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 15 Jun 2023 03:30:20 GMT
ENV PHP_VERSION=8.2.7
# Thu, 15 Jun 2023 03:30:20 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.7.tar.xz.asc
# Thu, 15 Jun 2023 03:30:20 GMT
ENV PHP_SHA256=4b9fb3dcd7184fe7582d7e44544ec7c5153852a2528de3b6754791258ffbdfa0
# Thu, 15 Jun 2023 03:30:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 15 Jun 2023 03:30:27 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 15 Jun 2023 03:37:46 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 15 Jun 2023 03:37:47 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 15 Jun 2023 03:37:48 GMT
RUN docker-php-ext-enable sodium
# Thu, 15 Jun 2023 03:37:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 Jun 2023 03:37:48 GMT
WORKDIR /var/www/html
# Thu, 15 Jun 2023 03:37:48 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 15 Jun 2023 03:37:48 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jun 2023 03:37:48 GMT
EXPOSE 9000
# Thu, 15 Jun 2023 03:37:48 GMT
CMD ["php-fpm"]
# Thu, 15 Jun 2023 08:51:06 GMT
RUN set -ex;         apk add --no-cache         imagemagick         rsync     ;         rm /var/spool/cron/crontabs/root;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Thu, 15 Jun 2023 08:53:49 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         autoconf         freetype-dev         gmp-dev         icu-dev         imagemagick-dev         libevent-dev         libjpeg-turbo-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libwebp-dev         libxml2-dev         libzip-dev         openldap-dev         pcre-dev         postgresql-dev     ;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap;     docker-php-ext-install -j "$(nproc)"         bcmath         exif         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.22;     pecl install imagick-3.7.0;     pecl install memcached-3.2.0;     pecl install redis-5.3.7;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .nextcloud-phpext-rundeps $runDeps;     apk del --no-network .build-deps
# Thu, 15 Jun 2023 08:53:49 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 15 Jun 2023 08:53:49 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 23 Jun 2023 18:44:32 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 23 Jun 2023 18:44:32 GMT
VOLUME [/var/www/html]
# Fri, 23 Jun 2023 18:44:32 GMT
ENV NEXTCLOUD_VERSION=26.0.3
# Fri, 23 Jun 2023 18:45:17 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-26.0.3.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-26.0.3.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com  --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;     apk del --no-network .fetch-deps
# Fri, 23 Jun 2023 18:45:22 GMT
COPY multi:f14917ef3f8441cf73a9faa81b54c7e51061a07185e365974d47ddb315426c8f in / 
# Fri, 23 Jun 2023 18:45:22 GMT
COPY multi:1aa0c68034f207c7e2fb6f047fda45b55878afe2781ef10723107e35ee22547e in /usr/src/nextcloud/config/ 
# Fri, 23 Jun 2023 18:45:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 23 Jun 2023 18:45:22 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68cbf4f33af4ff20fa90638cea5f48dda44f171afe80c0ca68a40b5c67ee1102`  
		Last Modified: Thu, 15 Jun 2023 04:39:12 GMT  
		Size: 2.7 MB (2696456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0262450c79d37bc5398bf1154c4bb2681100ef9caf7e008c5d0bd06c3d840a7`  
		Last Modified: Thu, 15 Jun 2023 04:39:11 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ca0f0b2514d4e2b8323c60eece66557c89959c380362deb6862fe5ffe3ad14`  
		Last Modified: Thu, 15 Jun 2023 04:39:11 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b58a31969c464d209f6338c19ffcc3ffa5cd1b719cc1d51d8d17bb436368424f`  
		Last Modified: Thu, 15 Jun 2023 04:40:50 GMT  
		Size: 12.0 MB (12037901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c22ecd80207b141e59fa3a40ad129bbced191c30b0cf8f2be2d324301f30587f`  
		Last Modified: Thu, 15 Jun 2023 04:40:48 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8e4497f71db74dd78d5ae574d84bccdc90f47b8a876098885243eb70ac8b2f`  
		Last Modified: Thu, 15 Jun 2023 04:41:29 GMT  
		Size: 12.8 MB (12770377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1151d5ab28fcb76884fe12db8006d68e2682a6dfa99030911f77b6fa31021ae1`  
		Last Modified: Thu, 15 Jun 2023 04:41:27 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:571fb0d265dfe7969fbbe3e1dea15866dd50c6bda97511518badca9e1a8c6ef0`  
		Last Modified: Thu, 15 Jun 2023 04:41:27 GMT  
		Size: 18.7 KB (18702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c69f93ae2f10ad6e6868c046ea56fec3dc600318ffc1b1bd07d969213b3bbfe1`  
		Last Modified: Thu, 15 Jun 2023 04:41:28 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db64072542f2887055587e455cfe595fbb015fa3393eabeeeea2c5633868d49f`  
		Last Modified: Thu, 15 Jun 2023 08:56:52 GMT  
		Size: 44.0 MB (44049887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2912ebb818bca6f19189745dcb125cab045e6557b1bb1a3bececc1b7649798f9`  
		Last Modified: Thu, 15 Jun 2023 08:56:47 GMT  
		Size: 7.2 MB (7231893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14cccd13d9aceb1bb64c90201855fe66ee324bbefb767a09275642cb1e790050`  
		Last Modified: Fri, 23 Jun 2023 18:51:55 GMT  
		Size: 761.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2c693047fdc83e4c0a7619feb962adefb1a9499cbe30aa7e5ddb066991b5032`  
		Last Modified: Fri, 23 Jun 2023 18:52:11 GMT  
		Size: 168.6 MB (168583199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3912edcac8e7ddc0e0379c84c67bb97eef653a400309894ed652680ee512f04`  
		Last Modified: Fri, 23 Jun 2023 18:51:55 GMT  
		Size: 3.5 KB (3469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197ed70ebc59ed2604ab9a63b5a6f87068509388ebc33e62369b463f93bc31ab`  
		Last Modified: Fri, 23 Jun 2023 18:51:55 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:26-fpm-alpine` - linux; 386

```console
$ docker pull nextcloud@sha256:66ce674e4d47c8c30a98fa20f59115c449c471f27f27f1868b7d78c34c79fa05
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.2 MB (248188073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b76d9abb1fd8a38fe692c754ace314ba9cea65a3715462e9166f7088a884bbf7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 14 Jun 2023 22:33:22 GMT
ADD file:94bec00e2c0c7f47c81ec4355a29ca23a81b439797d037b1a5a455f36a25dab4 in / 
# Wed, 14 Jun 2023 22:33:22 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 06:26:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 Jun 2023 06:26:16 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 15 Jun 2023 06:26:16 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 15 Jun 2023 06:26:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 Jun 2023 06:26:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 15 Jun 2023 06:26:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jun 2023 06:26:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jun 2023 06:26:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 Jun 2023 07:05:14 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Mon, 10 Jul 2023 21:56:51 GMT
ENV PHP_VERSION=8.2.8
# Mon, 10 Jul 2023 21:56:51 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.8.tar.xz.asc
# Mon, 10 Jul 2023 21:56:51 GMT
ENV PHP_SHA256=cfe1055fbcd486de7d3312da6146949aae577365808790af6018205567609801
# Mon, 10 Jul 2023 21:56:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Mon, 10 Jul 2023 21:56:58 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Mon, 10 Jul 2023 22:09:20 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Mon, 10 Jul 2023 22:09:21 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Mon, 10 Jul 2023 22:09:22 GMT
RUN docker-php-ext-enable sodium
# Mon, 10 Jul 2023 22:09:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 10 Jul 2023 22:09:22 GMT
WORKDIR /var/www/html
# Mon, 10 Jul 2023 22:09:22 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Mon, 10 Jul 2023 22:09:23 GMT
STOPSIGNAL SIGQUIT
# Mon, 10 Jul 2023 22:09:23 GMT
EXPOSE 9000
# Mon, 10 Jul 2023 22:09:23 GMT
CMD ["php-fpm"]
# Tue, 11 Jul 2023 01:20:08 GMT
RUN set -ex;         apk add --no-cache         imagemagick         rsync     ;         rm /var/spool/cron/crontabs/root;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Tue, 11 Jul 2023 01:23:02 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         autoconf         freetype-dev         gmp-dev         icu-dev         imagemagick-dev         libevent-dev         libjpeg-turbo-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libwebp-dev         libxml2-dev         libzip-dev         openldap-dev         pcre-dev         postgresql-dev     ;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap;     docker-php-ext-install -j "$(nproc)"         bcmath         exif         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.22;     pecl install imagick-3.7.0;     pecl install memcached-3.2.0;     pecl install redis-5.3.7;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .nextcloud-phpext-rundeps $runDeps;     apk del --no-network .build-deps
# Tue, 11 Jul 2023 01:23:02 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 11 Jul 2023 01:23:03 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 11 Jul 2023 01:23:03 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Tue, 11 Jul 2023 01:23:03 GMT
VOLUME [/var/www/html]
# Tue, 11 Jul 2023 01:23:03 GMT
ENV NEXTCLOUD_VERSION=26.0.3
# Tue, 11 Jul 2023 01:24:03 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-26.0.3.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-26.0.3.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com  --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;     apk del --no-network .fetch-deps
# Tue, 11 Jul 2023 01:24:06 GMT
COPY multi:f14917ef3f8441cf73a9faa81b54c7e51061a07185e365974d47ddb315426c8f in / 
# Tue, 11 Jul 2023 01:24:07 GMT
COPY multi:1aa0c68034f207c7e2fb6f047fda45b55878afe2781ef10723107e35ee22547e in /usr/src/nextcloud/config/ 
# Tue, 11 Jul 2023 01:24:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 11 Jul 2023 01:24:07 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:b3f50075abd13aad1cb7d8c1427aa59d7fcac88f3690d3f9c3efdbec80fd0856`  
		Last Modified: Wed, 14 Jun 2023 22:33:48 GMT  
		Size: 3.2 MB (3233951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:686addfe363578d7327e190b5b07780e2e046ab88a2d36c1d45bf9433e6dcd5a`  
		Last Modified: Thu, 15 Jun 2023 09:10:03 GMT  
		Size: 2.7 MB (2699507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fcfa11cca4a6fe8bb794ac07926f350ef4be9309437a2e4665ef8a89b425b54`  
		Last Modified: Thu, 15 Jun 2023 09:10:03 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1a40c4c1022edb58f063eb71a5482c5b66ab16c804b7b215db18d809affb5b`  
		Last Modified: Thu, 15 Jun 2023 09:10:03 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e956a5e55f4075a93a2e84549c69cc9e42e867ac12ba4faff5006ecc1a481c68`  
		Last Modified: Tue, 11 Jul 2023 00:31:39 GMT  
		Size: 12.1 MB (12055818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3110d0a429ca4e8e6d3a238b9e239c76352399f003b200c3258071eefffa9a83`  
		Last Modified: Tue, 11 Jul 2023 00:31:38 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:713767c19830afd14b3f9e6646f2053ea1d49e8039e3b8a3df62f3388e7d2ee6`  
		Last Modified: Tue, 11 Jul 2023 00:32:25 GMT  
		Size: 12.9 MB (12898188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23744e74b514875367e6f0dfc748727d4d6fdc2e29b671b40560e0c6cd847126`  
		Last Modified: Tue, 11 Jul 2023 00:32:22 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce4f14bd5f9e6719e42ecea4421e12bfe47fc5a7e0d75f31e88c54b73111882b`  
		Last Modified: Tue, 11 Jul 2023 00:32:22 GMT  
		Size: 18.9 KB (18924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:333c64195752425d45fc1fa7f313807a6500e70a9462476aa64bca90878aba20`  
		Last Modified: Tue, 11 Jul 2023 00:32:22 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b8f5c0ffe2e65470206b6b4054a8daba6daa24786583e08814156eb712956b`  
		Last Modified: Tue, 11 Jul 2023 01:33:11 GMT  
		Size: 41.7 MB (41657417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baa48c17114ad0ad8574b9bceb633132d76ec5538e4356b49db685cc7e9b1f63`  
		Last Modified: Tue, 11 Jul 2023 01:33:01 GMT  
		Size: 7.0 MB (7020758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46950e8eab9370b88a08dd357bd1d73f3de6565de6342a4750e69866af79b97d`  
		Last Modified: Tue, 11 Jul 2023 01:32:59 GMT  
		Size: 758.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adf4556005eac98ebe98015b83d0d1788b946770d29367d51cd4c240fd406ae8`  
		Last Modified: Tue, 11 Jul 2023 01:33:31 GMT  
		Size: 168.6 MB (168583408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c43c14516996bd807b8093c120b83191b12a2920357f1934b4f4560a761ec62`  
		Last Modified: Tue, 11 Jul 2023 01:32:59 GMT  
		Size: 3.5 KB (3469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0c4564b4296f7d88c61a8d1061d433792c64737c0baf9c9c4b8826778267913`  
		Last Modified: Tue, 11 Jul 2023 01:32:59 GMT  
		Size: 2.2 KB (2222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:26-fpm-alpine` - linux; ppc64le

```console
$ docker pull nextcloud@sha256:786df073d78d076adcefbe2d21f1f3787db9b347e3288874dee206e77b400693
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.5 MB (256466615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:070e99b56b8dac0d1e53d8cc262fa1a0e04b49cfa8ab214e5520bae1d6c019c5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 15 Jun 2023 00:39:49 GMT
ADD file:694c636c0dd19fd01accbc189e4c1dc4d063952692c6e7eb26dce02a7adba833 in / 
# Thu, 15 Jun 2023 00:39:49 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 02:20:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 Jun 2023 02:20:19 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 15 Jun 2023 02:20:20 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 15 Jun 2023 02:20:20 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 Jun 2023 02:20:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 15 Jun 2023 02:20:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jun 2023 02:20:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jun 2023 02:20:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 Jun 2023 02:46:03 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 15 Jun 2023 02:46:03 GMT
ENV PHP_VERSION=8.2.7
# Thu, 15 Jun 2023 02:46:04 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.7.tar.xz.asc
# Thu, 15 Jun 2023 02:46:04 GMT
ENV PHP_SHA256=4b9fb3dcd7184fe7582d7e44544ec7c5153852a2528de3b6754791258ffbdfa0
# Thu, 15 Jun 2023 02:46:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 15 Jun 2023 02:46:13 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 15 Jun 2023 02:54:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 15 Jun 2023 02:54:04 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 15 Jun 2023 02:54:06 GMT
RUN docker-php-ext-enable sodium
# Thu, 15 Jun 2023 02:54:06 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 Jun 2023 02:54:07 GMT
WORKDIR /var/www/html
# Thu, 15 Jun 2023 02:54:08 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 15 Jun 2023 02:54:08 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jun 2023 02:54:08 GMT
EXPOSE 9000
# Thu, 15 Jun 2023 02:54:08 GMT
CMD ["php-fpm"]
# Thu, 15 Jun 2023 13:58:09 GMT
RUN set -ex;         apk add --no-cache         imagemagick         rsync     ;         rm /var/spool/cron/crontabs/root;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Thu, 15 Jun 2023 14:02:29 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         autoconf         freetype-dev         gmp-dev         icu-dev         imagemagick-dev         libevent-dev         libjpeg-turbo-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libwebp-dev         libxml2-dev         libzip-dev         openldap-dev         pcre-dev         postgresql-dev     ;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap;     docker-php-ext-install -j "$(nproc)"         bcmath         exif         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.22;     pecl install imagick-3.7.0;     pecl install memcached-3.2.0;     pecl install redis-5.3.7;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .nextcloud-phpext-rundeps $runDeps;     apk del --no-network .build-deps
# Thu, 15 Jun 2023 14:02:30 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 15 Jun 2023 14:02:32 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 23 Jun 2023 18:26:03 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 23 Jun 2023 18:26:04 GMT
VOLUME [/var/www/html]
# Fri, 23 Jun 2023 18:26:04 GMT
ENV NEXTCLOUD_VERSION=26.0.3
# Fri, 23 Jun 2023 18:27:14 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-26.0.3.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-26.0.3.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com  --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;     apk del --no-network .fetch-deps
# Fri, 23 Jun 2023 18:27:17 GMT
COPY multi:f14917ef3f8441cf73a9faa81b54c7e51061a07185e365974d47ddb315426c8f in / 
# Fri, 23 Jun 2023 18:27:17 GMT
COPY multi:1aa0c68034f207c7e2fb6f047fda45b55878afe2781ef10723107e35ee22547e in /usr/src/nextcloud/config/ 
# Fri, 23 Jun 2023 18:27:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 23 Jun 2023 18:27:19 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:ffa4a466dbb8eebd7e7f25590a9df12390de9016abf82279c29c9a64aa76491a`  
		Last Modified: Thu, 15 Jun 2023 00:40:26 GMT  
		Size: 3.3 MB (3344781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a82af153dde64aaecebbaa654ef25fe458cadc53b82b53ef2709b36ee12472`  
		Last Modified: Thu, 15 Jun 2023 04:11:27 GMT  
		Size: 2.7 MB (2743785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:513a439724cb0dce6489fcef92ec4c613854488cc971907f16b38f06ff6e8a14`  
		Last Modified: Thu, 15 Jun 2023 04:11:26 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60c5f3fdb07b83b724766e77b9ffeaaa86c0112dc077280c28d8ab36d1b52955`  
		Last Modified: Thu, 15 Jun 2023 04:11:26 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7760ce68e38ca476fdc456b26599cd13038502047cc7313a5c2d5af54555b82`  
		Last Modified: Thu, 15 Jun 2023 04:13:27 GMT  
		Size: 12.0 MB (12037908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:480b5a949ff724a8b28f13e61adc9b7df52667085b75f01b9a4fd6d27cfcddc6`  
		Last Modified: Thu, 15 Jun 2023 04:13:25 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb716923151fa7f620063ad5c3fc8b5ff536eebac49eaa8a03ae311816a83cbe`  
		Last Modified: Thu, 15 Jun 2023 04:14:13 GMT  
		Size: 13.1 MB (13106627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1592c057e1c90903081c8d7b37441b701d8439ab0237b2b56bd8a40789fc91e4`  
		Last Modified: Thu, 15 Jun 2023 04:14:10 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d1f737dfbd851e51ce59fb6a65a50c7afd7f538c3d648c6c320a15d1cab79d3`  
		Last Modified: Thu, 15 Jun 2023 04:14:10 GMT  
		Size: 18.7 KB (18727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3d0a89475bfdb517a44a3d29787d957fbb706e337949e0bc254942a036e6a8`  
		Last Modified: Thu, 15 Jun 2023 04:14:10 GMT  
		Size: 9.2 KB (9184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1afb573a80604109a97e8fd3b5002f6433c54d1d2f1d8cfaebaeeaf4336b0c20`  
		Last Modified: Thu, 15 Jun 2023 14:07:46 GMT  
		Size: 49.7 MB (49731159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455da7939c6978210dfe2e1e7cf156e22268b828c6436caab457354a62b969c9`  
		Last Modified: Thu, 15 Jun 2023 14:07:35 GMT  
		Size: 6.9 MB (6880337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdeee6a909f2605282b103e1749b41ab2a064a57d64e478ed5ac3a1ac915ec85`  
		Last Modified: Fri, 23 Jun 2023 18:37:47 GMT  
		Size: 758.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f42dfb88c76186d7a01d6df0016633ccb7da33bd8779fe26f38be92e12fabcfb`  
		Last Modified: Fri, 23 Jun 2023 18:38:22 GMT  
		Size: 168.6 MB (168583179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b756a7735011cffe1898df0d41e7e8705caaddac1e09b97c3d42560143238859`  
		Last Modified: Fri, 23 Jun 2023 18:37:47 GMT  
		Size: 3.5 KB (3469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07972aa04eb294f57e020d48e209a3c10658c5d75b7168deecc0d8f9a8a3db31`  
		Last Modified: Fri, 23 Jun 2023 18:37:47 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:26-fpm-alpine` - linux; s390x

```console
$ docker pull nextcloud@sha256:b8af722840e8336029ddfb426438d9284b7f88ed6c8c332eaa69bc33d04235c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.8 MB (249773445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4513cd7ca8fb08d614abb8e2fa571beeb5bf541f3980406ba799763a783faa9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 15 Jun 2023 05:18:38 GMT
ADD file:a59beca78118ebf4f86cc1685237dc3a29a519401a70668da520beaa3d29eb7a in / 
# Thu, 15 Jun 2023 05:18:38 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 18:32:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 Jun 2023 18:32:18 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 15 Jun 2023 18:32:20 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 15 Jun 2023 18:32:20 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 Jun 2023 18:32:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 15 Jun 2023 18:32:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jun 2023 18:32:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jun 2023 18:32:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 Jun 2023 19:09:45 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 15 Jun 2023 19:09:45 GMT
ENV PHP_VERSION=8.2.7
# Thu, 15 Jun 2023 19:09:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.7.tar.xz.asc
# Thu, 15 Jun 2023 19:09:46 GMT
ENV PHP_SHA256=4b9fb3dcd7184fe7582d7e44544ec7c5153852a2528de3b6754791258ffbdfa0
# Thu, 15 Jun 2023 19:09:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 15 Jun 2023 19:09:55 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 15 Jun 2023 19:17:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 15 Jun 2023 19:17:59 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 15 Jun 2023 19:18:00 GMT
RUN docker-php-ext-enable sodium
# Thu, 15 Jun 2023 19:18:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 Jun 2023 19:18:01 GMT
WORKDIR /var/www/html
# Thu, 15 Jun 2023 19:18:01 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 15 Jun 2023 19:18:01 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jun 2023 19:18:02 GMT
EXPOSE 9000
# Thu, 15 Jun 2023 19:18:02 GMT
CMD ["php-fpm"]
# Fri, 16 Jun 2023 01:04:02 GMT
RUN set -ex;         apk add --no-cache         imagemagick         rsync     ;         rm /var/spool/cron/crontabs/root;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Fri, 16 Jun 2023 01:05:42 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         autoconf         freetype-dev         gmp-dev         icu-dev         imagemagick-dev         libevent-dev         libjpeg-turbo-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libwebp-dev         libxml2-dev         libzip-dev         openldap-dev         pcre-dev         postgresql-dev     ;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap;     docker-php-ext-install -j "$(nproc)"         bcmath         exif         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.22;     pecl install imagick-3.7.0;     pecl install memcached-3.2.0;     pecl install redis-5.3.7;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .nextcloud-phpext-rundeps $runDeps;     apk del --no-network .build-deps
# Fri, 16 Jun 2023 01:05:43 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 16 Jun 2023 01:05:43 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 23 Jun 2023 18:50:14 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 23 Jun 2023 18:50:14 GMT
VOLUME [/var/www/html]
# Fri, 23 Jun 2023 18:50:14 GMT
ENV NEXTCLOUD_VERSION=26.0.3
# Fri, 23 Jun 2023 18:50:49 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-26.0.3.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-26.0.3.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com  --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;     apk del --no-network .fetch-deps
# Fri, 23 Jun 2023 18:50:58 GMT
COPY multi:f14917ef3f8441cf73a9faa81b54c7e51061a07185e365974d47ddb315426c8f in / 
# Fri, 23 Jun 2023 18:50:58 GMT
COPY multi:1aa0c68034f207c7e2fb6f047fda45b55878afe2781ef10723107e35ee22547e in /usr/src/nextcloud/config/ 
# Fri, 23 Jun 2023 18:50:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 23 Jun 2023 18:50:58 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:998cc98447b44e5f0fe799dce691412796ba586ab22eb7c99aebf9d45f34833b`  
		Last Modified: Thu, 15 Jun 2023 05:29:38 GMT  
		Size: 3.2 MB (3213497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9863b5dcc3e5885fe5ff8335b86d4287dfd59b451fe22e94b79f83b396c3776d`  
		Last Modified: Thu, 15 Jun 2023 21:54:07 GMT  
		Size: 2.8 MB (2766871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f159305449b6c309659dadfedb968259be79e6f5b9f552d97134f0a94490ae8`  
		Last Modified: Thu, 15 Jun 2023 21:54:07 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0e5f78cdbb2bcfe6b24c6cc002d51d1551a0fbabd06fa3baaee2be566d6d55f`  
		Last Modified: Thu, 15 Jun 2023 21:54:07 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0585437a9672289117fb5f7c79c593b6cec67984e39bef0804e544a22cee6137`  
		Last Modified: Thu, 15 Jun 2023 22:09:53 GMT  
		Size: 12.0 MB (12037903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:591832229400208438aeaf1c3ac7c35df6510c5f4136ffad415dcfac84950420`  
		Last Modified: Thu, 15 Jun 2023 22:09:52 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba42294af74b0eeddf476c7e4630d527fd8aabb87fda05b1f976525c616e49d`  
		Last Modified: Thu, 15 Jun 2023 22:11:32 GMT  
		Size: 11.9 MB (11855436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3de2a4b2383156f540ecab01b74b2f7313a0450aba1dcc4cd65237e160de027`  
		Last Modified: Thu, 15 Jun 2023 22:11:30 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:060a4ba7a2c44a0a502702c080f56f3f4ef6a572e23db2683063d22902fa0218`  
		Last Modified: Thu, 15 Jun 2023 22:11:30 GMT  
		Size: 18.8 KB (18757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92308fc2c074e13591364d60b642f27b167d8719ddb7f7229c42f260b7d6658`  
		Last Modified: Thu, 15 Jun 2023 22:11:30 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0326a790ffe52ab893f60a275fc4ac6c5a9415b308e37d247e8c7513505f1786`  
		Last Modified: Fri, 16 Jun 2023 01:31:22 GMT  
		Size: 44.6 MB (44598413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de4158b995eb5e0f9473390b208d2d4dd9234a3913370aa757c04e63f190032b`  
		Last Modified: Fri, 16 Jun 2023 01:31:16 GMT  
		Size: 6.7 MB (6680163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c246a678e5861707092c381fc068fe6e475874f1247d0bde2fead411e452d4c2`  
		Last Modified: Fri, 23 Jun 2023 18:59:21 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7751dd327b938a3b255f4460e80a78d2140f537df7ef486b3b431e7c73aa2a60`  
		Last Modified: Fri, 23 Jun 2023 18:59:40 GMT  
		Size: 168.6 MB (168582298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b0ef7fef412d739e2ec4edf67d22e32c1209d5c6f0f5f191871eba203e3c4d0`  
		Last Modified: Fri, 23 Jun 2023 18:59:20 GMT  
		Size: 3.5 KB (3470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f76b9254caa0b0b8db1882fab1af74bc4c3f360557cc1502176c8370c1c25d3`  
		Last Modified: Fri, 23 Jun 2023 18:59:20 GMT  
		Size: 2.2 KB (2221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
