## `nextcloud:production-fpm-alpine`

```console
$ docker pull nextcloud@sha256:46a1e7611c6f1f15ca264157477d25ebc536a133cce067121241584dae6eb601
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

### `nextcloud:production-fpm-alpine` - linux; amd64

```console
$ docker pull nextcloud@sha256:a1cc3ba78756b6760e67b1615fbed2877d65d1cf15bfcf3b3c852469ed39d9fb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.8 MB (208780687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:913ed080f77b91050a7936f159f2552c8c97679b1a66ac8da4284df563ce5d3b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 00:59:37 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 05 Apr 2022 00:59:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 05 Apr 2022 00:59:39 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 05 Apr 2022 00:59:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 05 Apr 2022 00:59:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 05 Apr 2022 00:59:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 05 Apr 2022 00:59:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 05 Apr 2022 00:59:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 05 Apr 2022 01:48:21 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 10 Jun 2022 01:25:20 GMT
ENV PHP_VERSION=8.0.20
# Fri, 10 Jun 2022 01:25:20 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.20.tar.xz.asc
# Fri, 10 Jun 2022 01:25:20 GMT
ENV PHP_SHA256=973fec765336ee01f47536a5db1c2eee98df9d34a41522b7b6c760159bf0a77b
# Fri, 10 Jun 2022 01:25:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 10 Jun 2022 01:25:27 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 10 Jun 2022 01:32:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 10 Jun 2022 01:32:58 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 10 Jun 2022 01:32:59 GMT
RUN docker-php-ext-enable sodium
# Fri, 10 Jun 2022 01:32:59 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 10 Jun 2022 01:32:59 GMT
WORKDIR /var/www/html
# Fri, 10 Jun 2022 01:33:00 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 10 Jun 2022 01:33:00 GMT
STOPSIGNAL SIGQUIT
# Fri, 10 Jun 2022 01:33:00 GMT
EXPOSE 9000
# Fri, 10 Jun 2022 01:33:00 GMT
CMD ["php-fpm"]
# Fri, 10 Jun 2022 03:32:48 GMT
RUN set -ex;         apk add --no-cache         rsync     ;         rm /var/spool/cron/crontabs/root;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Fri, 10 Jun 2022 03:35:20 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         autoconf         freetype-dev         icu-dev         libevent-dev         libjpeg-turbo-dev         libmcrypt-dev         libpng-dev         libmemcached-dev         libxml2-dev         libzip-dev         openldap-dev         pcre-dev         postgresql-dev         imagemagick-dev         libwebp-dev         gmp-dev     ;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap;     docker-php-ext-install -j "$(nproc)"         bcmath         exif         gd         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         zip         gmp     ;         pecl install APCu-5.1.21;     pecl install memcached-3.2.0;     pecl install redis-5.3.7;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --virtual .nextcloud-phpext-rundeps $runDeps;     apk del .build-deps
# Fri, 10 Jun 2022 03:35:20 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 10 Jun 2022 03:35:20 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 10 Jun 2022 03:35:21 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=16';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/nextcloud.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 10 Jun 2022 03:35:21 GMT
VOLUME [/var/www/html]
# Fri, 10 Jun 2022 03:37:26 GMT
ENV NEXTCLOUD_VERSION=23.0.5
# Fri, 10 Jun 2022 03:38:13 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         curl -fsSL -o nextcloud.tar.bz2         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com  --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;     apk del .fetch-deps
# Fri, 10 Jun 2022 03:38:15 GMT
COPY multi:497b8d243f90fa6abd88194ba134de5703abecf47c13a92d2f2fb8210d2cfa77 in / 
# Fri, 10 Jun 2022 03:38:15 GMT
COPY multi:7281097c8fd959eff64684726d7707d598f15dc22353d1f6f843624f642bdcd2 in /usr/src/nextcloud/config/ 
# Fri, 10 Jun 2022 03:38:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 10 Jun 2022 03:38:15 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a60f85627e3d0df735c885c9502afee6c4a98aec08c02a0b31ffd6ee36d1d3ed`  
		Last Modified: Tue, 05 Apr 2022 02:49:01 GMT  
		Size: 1.7 MB (1701412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89395091f2959844751d9669bf4ffa0d72cae1e7710bd34d692c4a724abcfe20`  
		Last Modified: Tue, 05 Apr 2022 02:49:00 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2342a00f1dee7a210bf0e6327fce29393f5b0b67b1dbd297a5d39b322c2c61df`  
		Last Modified: Tue, 05 Apr 2022 02:49:00 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9a2fc7c70326d12259a895bb7fffd7597a55e7c44617e44673f8d7a46060de9`  
		Last Modified: Fri, 10 Jun 2022 01:45:51 GMT  
		Size: 10.9 MB (10899013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa914bd91b9b2734e3becab9f16c36d5a861bccabd00595fca84052be201ed4`  
		Last Modified: Fri, 10 Jun 2022 01:45:50 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0fa650472fcd72710ca93119273783c593977a4229b0994cba3553ab411d5c3`  
		Last Modified: Fri, 10 Jun 2022 01:46:11 GMT  
		Size: 13.9 MB (13900879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e4584ac93bca40639d9797879e99f5296ad024a87c76973730b1361055cdb7e`  
		Last Modified: Fri, 10 Jun 2022 01:46:08 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f1325c302b7a46f134b8be09f50e4c0da136cf2748f04e1051d1c907bbfa15`  
		Last Modified: Fri, 10 Jun 2022 01:46:08 GMT  
		Size: 18.6 KB (18555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d829363ca59866666bdffe9385d210ef2ae0078643b4189a46385932809c8d9`  
		Last Modified: Fri, 10 Jun 2022 01:46:08 GMT  
		Size: 8.6 KB (8569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7583ff35470eb057853d8f7932fc1201ab317993f8a31d8954c305dcad506e2`  
		Last Modified: Fri, 10 Jun 2022 03:42:33 GMT  
		Size: 830.0 KB (829988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f9d071c3565a5f79e61c3ee73d6e4136dc6855d8670a077fe7a934f8e89e2d9`  
		Last Modified: Fri, 10 Jun 2022 03:42:34 GMT  
		Size: 25.2 MB (25205940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa1ee877e8e9f338085531fe974d57b687ffa50a6a57f22f15669d0b90d82e88`  
		Last Modified: Fri, 10 Jun 2022 03:42:31 GMT  
		Size: 595.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80b51d29ae2e3293ba4d4c19deafda13e04916ebb3348b1a7928e1af6ec8ff97`  
		Last Modified: Fri, 10 Jun 2022 03:44:23 GMT  
		Size: 153.4 MB (153391606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07e8f714a0155e7ab0b15bee425213683cea621ecc966f44f8941ff0b92efe5`  
		Last Modified: Fri, 10 Jun 2022 03:44:03 GMT  
		Size: 3.0 KB (2964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ddec5f079ec597fbc6f55dcdf0e41b7eba498996d6350f9302ddcb630db103`  
		Last Modified: Fri, 10 Jun 2022 03:44:03 GMT  
		Size: 2.1 KB (2135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:production-fpm-alpine` - linux; arm variant v6

```console
$ docker pull nextcloud@sha256:4a7102a55ec96b0b3fc1b2fe23c8bcab474225b20d376b68b9fb5399e86658bf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.9 MB (205879102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f0e50f8396b9593d4ef62be3fab20e9d4758bc89f8febaa9153c5af3726181c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Mon, 04 Apr 2022 23:53:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 04 Apr 2022 23:53:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Mon, 04 Apr 2022 23:53:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Mon, 04 Apr 2022 23:53:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 04 Apr 2022 23:53:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Mon, 04 Apr 2022 23:53:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 04 Apr 2022 23:53:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 04 Apr 2022 23:53:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 05 Apr 2022 00:35:51 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 10 Jun 2022 00:12:29 GMT
ENV PHP_VERSION=8.0.20
# Fri, 10 Jun 2022 00:12:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.20.tar.xz.asc
# Fri, 10 Jun 2022 00:12:29 GMT
ENV PHP_SHA256=973fec765336ee01f47536a5db1c2eee98df9d34a41522b7b6c760159bf0a77b
# Fri, 10 Jun 2022 00:12:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 10 Jun 2022 00:12:40 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 10 Jun 2022 00:22:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 10 Jun 2022 00:22:14 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 10 Jun 2022 00:22:17 GMT
RUN docker-php-ext-enable sodium
# Fri, 10 Jun 2022 00:22:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 10 Jun 2022 00:22:17 GMT
WORKDIR /var/www/html
# Fri, 10 Jun 2022 00:22:19 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 10 Jun 2022 00:22:19 GMT
STOPSIGNAL SIGQUIT
# Fri, 10 Jun 2022 00:22:20 GMT
EXPOSE 9000
# Fri, 10 Jun 2022 00:22:20 GMT
CMD ["php-fpm"]
# Fri, 10 Jun 2022 02:21:25 GMT
RUN set -ex;         apk add --no-cache         rsync     ;         rm /var/spool/cron/crontabs/root;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Fri, 10 Jun 2022 02:26:58 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         autoconf         freetype-dev         icu-dev         libevent-dev         libjpeg-turbo-dev         libmcrypt-dev         libpng-dev         libmemcached-dev         libxml2-dev         libzip-dev         openldap-dev         pcre-dev         postgresql-dev         imagemagick-dev         libwebp-dev         gmp-dev     ;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap;     docker-php-ext-install -j "$(nproc)"         bcmath         exif         gd         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         zip         gmp     ;         pecl install APCu-5.1.21;     pecl install memcached-3.2.0;     pecl install redis-5.3.7;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --virtual .nextcloud-phpext-rundeps $runDeps;     apk del .build-deps
# Fri, 10 Jun 2022 02:26:58 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 10 Jun 2022 02:26:59 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 10 Jun 2022 02:27:00 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=16';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/nextcloud.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 10 Jun 2022 02:27:01 GMT
VOLUME [/var/www/html]
# Fri, 10 Jun 2022 02:29:02 GMT
ENV NEXTCLOUD_VERSION=23.0.5
# Fri, 10 Jun 2022 02:30:44 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         curl -fsSL -o nextcloud.tar.bz2         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com  --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;     apk del .fetch-deps
# Fri, 10 Jun 2022 02:30:47 GMT
COPY multi:497b8d243f90fa6abd88194ba134de5703abecf47c13a92d2f2fb8210d2cfa77 in / 
# Fri, 10 Jun 2022 02:30:49 GMT
COPY multi:7281097c8fd959eff64684726d7707d598f15dc22353d1f6f843624f642bdcd2 in /usr/src/nextcloud/config/ 
# Fri, 10 Jun 2022 02:30:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 10 Jun 2022 02:30:50 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f4857007e05a14c6f648dc95eb29cd4faae7806674bb49c86a9c22bf5c828e`  
		Last Modified: Tue, 05 Apr 2022 01:33:30 GMT  
		Size: 1.7 MB (1688742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb0f12cd34ba09b6e733247467586fb1354d26dfc93308155099ca243578518`  
		Last Modified: Tue, 05 Apr 2022 01:33:29 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ebc724c09cd88ae23080a3eb4cc057c4cbe9cbd5c83048ea54c647cbcc8f040`  
		Last Modified: Tue, 05 Apr 2022 01:33:29 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a761e838868ef7af1b098872521e86a3af7b9f52cbb667dc26c24e2a575047`  
		Last Modified: Fri, 10 Jun 2022 00:40:39 GMT  
		Size: 10.9 MB (10898999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e6d66d219f242d9e4c34b40cb649bdd3c7599548503c59c3b8bd32a6e25008`  
		Last Modified: Fri, 10 Jun 2022 00:40:37 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e40681d9b4791ed6672c1c7a96210d2d39f6137a61400aa7bd8c0cc083c73f`  
		Last Modified: Fri, 10 Jun 2022 00:41:17 GMT  
		Size: 12.6 MB (12566665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0caae61b26c7bf4e9d96814a7c009016e23a6c757faedad9850a16503b48e2cf`  
		Last Modified: Fri, 10 Jun 2022 00:41:08 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9aea91e38385da1c70de6518db1d5f687c12df23ad1fb2a5335545a244be1f7`  
		Last Modified: Fri, 10 Jun 2022 00:41:08 GMT  
		Size: 18.5 KB (18541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:966891c30b60b824461c3f8ae9861261197788bea6dfb78e958e5bc40a4ca4fd`  
		Last Modified: Fri, 10 Jun 2022 00:41:08 GMT  
		Size: 8.6 KB (8569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa32041c386804c63efb07baca77e20c984c2f57745c4eb36af4ea9c44a8929e`  
		Last Modified: Fri, 10 Jun 2022 02:33:50 GMT  
		Size: 778.8 KB (778761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a11bcc639e387e14a2c06e1126ed92770420aacf8bc746b9d7e78adfcdd478`  
		Last Modified: Fri, 10 Jun 2022 02:34:01 GMT  
		Size: 23.9 MB (23894876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45b6ee978ee3ca30a054f3fe19c640b31a710070eaf98e9f9ab8650ff87c7b08`  
		Last Modified: Fri, 10 Jun 2022 02:33:47 GMT  
		Size: 593.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53524d7b68da56bd7df6c3bfc498f42a0d8b4598dadb481af140ac42f2e94913`  
		Last Modified: Fri, 10 Jun 2022 02:37:24 GMT  
		Size: 153.4 MB (153391807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44c2039fceb703378e70176d44a1ade84d982f7f6594444b07093995756d0b2`  
		Last Modified: Fri, 10 Jun 2022 02:35:40 GMT  
		Size: 3.0 KB (2964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8b2fe183bbdac3349c184cf442f915948e4b22185793f766e7b403bb67bcb7`  
		Last Modified: Fri, 10 Jun 2022 02:35:40 GMT  
		Size: 2.1 KB (2139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:production-fpm-alpine` - linux; arm variant v7

```console
$ docker pull nextcloud@sha256:fef3e2cb27b83840f649163f82e2b7ad7426fc1ae0177728aaed302497bf623d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.2 MB (204228519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5c296f1fddbea3306e190259c85497718c5278ab91013e8b281f9330cb2f392`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:34 GMT
ADD file:20f8cdddc53a4a8bd78945fc32fe08e9f80ab3b16dc20a9aa4ba73b79f2bc71c in / 
# Mon, 04 Apr 2022 23:57:35 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 00:44:26 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 05 Apr 2022 00:44:29 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 05 Apr 2022 00:44:31 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 05 Apr 2022 00:44:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 05 Apr 2022 00:44:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 05 Apr 2022 00:44:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 05 Apr 2022 00:44:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 05 Apr 2022 00:44:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 05 Apr 2022 01:28:17 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 13 May 2022 06:54:40 GMT
ENV PHP_VERSION=8.0.19
# Fri, 13 May 2022 06:54:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.19.tar.xz.asc
# Fri, 13 May 2022 06:54:40 GMT
ENV PHP_SHA256=ba62219c4b0486cbb2a04f0796749a46b0ee1f5a142ed454212b4e2460cb0fab
# Fri, 13 May 2022 06:54:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 13 May 2022 06:54:48 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 13 May 2022 07:03:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 13 May 2022 07:03:35 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 13 May 2022 07:03:37 GMT
RUN docker-php-ext-enable sodium
# Fri, 13 May 2022 07:03:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 13 May 2022 07:03:38 GMT
WORKDIR /var/www/html
# Fri, 13 May 2022 07:03:40 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 13 May 2022 07:03:40 GMT
STOPSIGNAL SIGQUIT
# Fri, 13 May 2022 07:03:41 GMT
EXPOSE 9000
# Fri, 13 May 2022 07:03:41 GMT
CMD ["php-fpm"]
# Fri, 13 May 2022 11:31:45 GMT
RUN set -ex;         apk add --no-cache         rsync     ;         rm /var/spool/cron/crontabs/root;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Fri, 13 May 2022 11:36:58 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         autoconf         freetype-dev         icu-dev         libevent-dev         libjpeg-turbo-dev         libmcrypt-dev         libpng-dev         libmemcached-dev         libxml2-dev         libzip-dev         openldap-dev         pcre-dev         postgresql-dev         imagemagick-dev         libwebp-dev         gmp-dev     ;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap;     docker-php-ext-install -j "$(nproc)"         bcmath         exif         gd         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         zip         gmp     ;         pecl install APCu-5.1.21;     pecl install memcached-3.2.0;     pecl install redis-5.3.7;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --virtual .nextcloud-phpext-rundeps $runDeps;     apk del .build-deps
# Fri, 13 May 2022 11:36:59 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 13 May 2022 11:36:59 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 13 May 2022 11:37:01 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=16';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/nextcloud.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 13 May 2022 11:37:01 GMT
VOLUME [/var/www/html]
# Fri, 20 May 2022 21:30:06 GMT
ENV NEXTCLOUD_VERSION=23.0.5
# Fri, 20 May 2022 21:31:44 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         curl -fsSL -o nextcloud.tar.bz2         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com  --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;     apk del .fetch-deps
# Fri, 20 May 2022 21:31:47 GMT
COPY multi:497b8d243f90fa6abd88194ba134de5703abecf47c13a92d2f2fb8210d2cfa77 in / 
# Fri, 20 May 2022 21:31:49 GMT
COPY multi:7281097c8fd959eff64684726d7707d598f15dc22353d1f6f843624f642bdcd2 in /usr/src/nextcloud/config/ 
# Fri, 20 May 2022 21:31:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 20 May 2022 21:31:50 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:57fb4b5f1a47c953ca5703f0f81ce14e5d01cf23aa79558b5adb961cc526e320`  
		Last Modified: Mon, 04 Apr 2022 19:09:36 GMT  
		Size: 2.4 MB (2424323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31e79621416caf77f775491eca7e32b6744cb98a7f314d25662db9d47388f78c`  
		Last Modified: Tue, 05 Apr 2022 02:39:26 GMT  
		Size: 1.6 MB (1556468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8e6096135db80ad99d3893e56fed755390988cde114bfa2eadb0344135aa68`  
		Last Modified: Tue, 05 Apr 2022 02:39:26 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e579551e9fe0160cdaf60f2b80ab01b627b8bfea2c89907509913896a5f1b118`  
		Last Modified: Tue, 05 Apr 2022 02:39:25 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dff108c1db1aeee78e063212233558b0fcdad9e3695be3969492a760967aa54d`  
		Last Modified: Fri, 13 May 2022 07:53:14 GMT  
		Size: 10.8 MB (10798938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4c3d3da048037a3b11ce590e5cd38c38037ede518387994a32066f8813efbf0`  
		Last Modified: Fri, 13 May 2022 07:53:11 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6eeb121e5fa64efed6fbe29e6ec1930da515592ababcf9ba0e2e0cdb52296a`  
		Last Modified: Fri, 13 May 2022 07:54:04 GMT  
		Size: 11.8 MB (11799230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd9346a84631b72530e8ce5461a513be2af0e1eccb7bfef62fd77af9ef2e8fbe`  
		Last Modified: Fri, 13 May 2022 07:53:56 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce9e7c9f528ec9df83269b05c4168b312f832291db1d82a8319d4dc62724958`  
		Last Modified: Fri, 13 May 2022 07:53:57 GMT  
		Size: 18.5 KB (18511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c373d779eac3e5caba73d4f938cb4db2aea2231e19dddc037110c76b4f20c5d7`  
		Last Modified: Fri, 13 May 2022 07:53:57 GMT  
		Size: 8.6 KB (8572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9331a516f73d13e93a34e171c43f6e8df5feabb79ee00a9bee67a6cbae5be5f7`  
		Last Modified: Fri, 13 May 2022 11:58:07 GMT  
		Size: 713.5 KB (713463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:630a0c5ff553b0252c8ff6d6de812e8c36996e4daae88ff2f47daaf274752c75`  
		Last Modified: Fri, 13 May 2022 11:58:17 GMT  
		Size: 23.5 MB (23506843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:794cd5be764660c6c86cc8f6aad6b835b84d637f3900957e43dc0dc86dd26922`  
		Last Modified: Fri, 13 May 2022 11:58:05 GMT  
		Size: 594.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:673c1fa6762eb67b3cecfa59b69113b3c5cdacd36b63e1e9bc34e72ac96adfb9`  
		Last Modified: Fri, 20 May 2022 21:53:22 GMT  
		Size: 153.4 MB (153391992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19ed2f7cc2a76b6064d7a97280c686891bce7269d1a2dd62233d08ca1f255c2`  
		Last Modified: Fri, 20 May 2022 21:51:37 GMT  
		Size: 3.0 KB (2963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79343ce0ed928e3f7cbe3541adb3c873dc6d87a4445018bdbed4c600d3e28081`  
		Last Modified: Fri, 20 May 2022 21:51:37 GMT  
		Size: 2.1 KB (2146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:production-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull nextcloud@sha256:0ce25fb8d09059d6f32dd85d1a6b9da36b4d8fbf20a2fc6b8245516c8d3b221e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.4 MB (207362032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b937d85c165404a89162d747c8dc771117231ef20cc220ff26f062ee9bcdf27`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 00:14:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 05 Apr 2022 00:14:50 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 05 Apr 2022 00:14:51 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 05 Apr 2022 00:14:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 05 Apr 2022 00:14:53 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 05 Apr 2022 00:14:54 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 05 Apr 2022 00:14:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 05 Apr 2022 00:14:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 05 Apr 2022 01:02:45 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Thu, 12 May 2022 21:03:22 GMT
ENV PHP_VERSION=8.0.19
# Thu, 12 May 2022 21:03:23 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.19.tar.xz.asc
# Thu, 12 May 2022 21:03:24 GMT
ENV PHP_SHA256=ba62219c4b0486cbb2a04f0796749a46b0ee1f5a142ed454212b4e2460cb0fab
# Thu, 12 May 2022 21:03:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 12 May 2022 21:03:40 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 12 May 2022 21:17:18 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 12 May 2022 21:17:20 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 12 May 2022 21:17:21 GMT
RUN docker-php-ext-enable sodium
# Thu, 12 May 2022 21:17:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 May 2022 21:17:23 GMT
WORKDIR /var/www/html
# Thu, 12 May 2022 21:17:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 12 May 2022 21:17:25 GMT
STOPSIGNAL SIGQUIT
# Thu, 12 May 2022 21:17:26 GMT
EXPOSE 9000
# Thu, 12 May 2022 21:17:27 GMT
CMD ["php-fpm"]
# Thu, 12 May 2022 23:44:36 GMT
RUN set -ex;         apk add --no-cache         rsync     ;         rm /var/spool/cron/crontabs/root;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Thu, 12 May 2022 23:46:57 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         autoconf         freetype-dev         icu-dev         libevent-dev         libjpeg-turbo-dev         libmcrypt-dev         libpng-dev         libmemcached-dev         libxml2-dev         libzip-dev         openldap-dev         pcre-dev         postgresql-dev         imagemagick-dev         libwebp-dev         gmp-dev     ;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap;     docker-php-ext-install -j "$(nproc)"         bcmath         exif         gd         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         zip         gmp     ;         pecl install APCu-5.1.21;     pecl install memcached-3.2.0;     pecl install redis-5.3.7;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --virtual .nextcloud-phpext-rundeps $runDeps;     apk del .build-deps
# Thu, 12 May 2022 23:46:57 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 12 May 2022 23:46:58 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 12 May 2022 23:46:59 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=16';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/nextcloud.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Thu, 12 May 2022 23:47:00 GMT
VOLUME [/var/www/html]
# Fri, 20 May 2022 20:50:54 GMT
ENV NEXTCLOUD_VERSION=23.0.5
# Fri, 20 May 2022 20:51:33 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         curl -fsSL -o nextcloud.tar.bz2         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com  --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;     apk del .fetch-deps
# Fri, 20 May 2022 20:51:35 GMT
COPY multi:497b8d243f90fa6abd88194ba134de5703abecf47c13a92d2f2fb8210d2cfa77 in / 
# Fri, 20 May 2022 20:51:36 GMT
COPY multi:7281097c8fd959eff64684726d7707d598f15dc22353d1f6f843624f642bdcd2 in /usr/src/nextcloud/config/ 
# Fri, 20 May 2022 20:51:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 20 May 2022 20:51:38 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f69c83c314e8e18362c8a6739f6f7857ed89cc606ea05f0a95d6eb922fbc3f5`  
		Last Modified: Tue, 05 Apr 2022 01:52:13 GMT  
		Size: 1.7 MB (1696240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c8f271730dc83953a1ddf4c1d17b33fcb696501a3331a55c9ed5ccfec44542c`  
		Last Modified: Tue, 05 Apr 2022 01:52:13 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d1df3f0f228d28d8f270e64056adb7297fcca517c48468be36d482e2f383dd`  
		Last Modified: Tue, 05 Apr 2022 01:52:12 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6683ecf45d1d79c4356c3225f70828f89be7b0c3d2c2b72c30a26354bb44bec9`  
		Last Modified: Thu, 12 May 2022 21:59:50 GMT  
		Size: 10.8 MB (10798718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bac6eef4bc297b0d644ce4f463866a6a39add85423457b955fe321b7269be0a`  
		Last Modified: Thu, 12 May 2022 21:59:49 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff937945b8cf09f37d556a2bb472b6f7201e7885654982334a26efaa9a9d12b4`  
		Last Modified: Thu, 12 May 2022 22:00:25 GMT  
		Size: 13.3 MB (13261855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f24cf5a31c71d3da593aaf9087672d4a17afeb1982c93278312946d0a4d23e62`  
		Last Modified: Thu, 12 May 2022 22:00:23 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:356592aa934c74b39b9dd957eca533d4221544b2fa10ab385be2d410318210ac`  
		Last Modified: Thu, 12 May 2022 22:00:23 GMT  
		Size: 18.4 KB (18441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb066903a2219a2b018b5767b716e8f8372ebd13177233521556014bd875682`  
		Last Modified: Thu, 12 May 2022 22:00:23 GMT  
		Size: 8.6 KB (8570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d4103ed36b588f8acd4946a1cbf149bceedee1fe5a43fd62aadf43fcc14fc18`  
		Last Modified: Thu, 12 May 2022 23:54:08 GMT  
		Size: 840.8 KB (840822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd2636ca06b47aac865f13f96649de0934c19bff95d03306f71dea4adbfd1230`  
		Last Modified: Thu, 12 May 2022 23:54:08 GMT  
		Size: 24.6 MB (24616217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7ec9ff7c77a9f5920e73add630f07f55fdd57cb972402e11acaf25ee5fffd8`  
		Last Modified: Thu, 12 May 2022 23:54:05 GMT  
		Size: 566.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550f91098419ca8d96bde5ddf9869abc13e0ab016e85f57cfbdac2958d21ea70`  
		Last Modified: Fri, 20 May 2022 21:00:16 GMT  
		Size: 153.4 MB (153394625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31e5d8154a0f093defe68fc278d8160a2b816941ebfe43ad490a3e7677e61daf`  
		Last Modified: Fri, 20 May 2022 20:59:54 GMT  
		Size: 3.0 KB (2964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:882c3ef208daf0b110e59584b9b3a62e05973923606b4ceec5b573d068857b2b`  
		Last Modified: Fri, 20 May 2022 20:59:54 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:production-fpm-alpine` - linux; 386

```console
$ docker pull nextcloud@sha256:b46f799d5dc1e5138e4802bb8bb3ad58c561ae4a0b312aa2a166c7dae1358c31
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.5 MB (209496325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad0559ea8ab39b099decaa4295a0d23cbccb32aade1498079f731834d208fff3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 04 Apr 2022 23:38:25 GMT
ADD file:7d51a0f8691eb78c9062fd31984423a93d276a67b4ed5d1a706e1c2cd9fea23a in / 
# Mon, 04 Apr 2022 23:38:25 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 00:05:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 05 Apr 2022 00:05:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 05 Apr 2022 00:05:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 05 Apr 2022 00:05:50 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 05 Apr 2022 00:05:51 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 05 Apr 2022 00:05:52 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 05 Apr 2022 00:05:53 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 05 Apr 2022 00:05:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 05 Apr 2022 00:37:45 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 10 Jun 2022 01:10:59 GMT
ENV PHP_VERSION=8.0.20
# Fri, 10 Jun 2022 01:11:00 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.20.tar.xz.asc
# Fri, 10 Jun 2022 01:11:01 GMT
ENV PHP_SHA256=973fec765336ee01f47536a5db1c2eee98df9d34a41522b7b6c760159bf0a77b
# Fri, 10 Jun 2022 01:11:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 10 Jun 2022 01:11:09 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 10 Jun 2022 01:18:00 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 10 Jun 2022 01:18:01 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 10 Jun 2022 01:18:01 GMT
RUN docker-php-ext-enable sodium
# Fri, 10 Jun 2022 01:18:02 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 10 Jun 2022 01:18:03 GMT
WORKDIR /var/www/html
# Fri, 10 Jun 2022 01:18:04 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 10 Jun 2022 01:18:05 GMT
STOPSIGNAL SIGQUIT
# Fri, 10 Jun 2022 01:18:06 GMT
EXPOSE 9000
# Fri, 10 Jun 2022 01:18:07 GMT
CMD ["php-fpm"]
# Fri, 10 Jun 2022 03:08:30 GMT
RUN set -ex;         apk add --no-cache         rsync     ;         rm /var/spool/cron/crontabs/root;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Fri, 10 Jun 2022 03:10:58 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         autoconf         freetype-dev         icu-dev         libevent-dev         libjpeg-turbo-dev         libmcrypt-dev         libpng-dev         libmemcached-dev         libxml2-dev         libzip-dev         openldap-dev         pcre-dev         postgresql-dev         imagemagick-dev         libwebp-dev         gmp-dev     ;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap;     docker-php-ext-install -j "$(nproc)"         bcmath         exif         gd         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         zip         gmp     ;         pecl install APCu-5.1.21;     pecl install memcached-3.2.0;     pecl install redis-5.3.7;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --virtual .nextcloud-phpext-rundeps $runDeps;     apk del .build-deps
# Fri, 10 Jun 2022 03:10:58 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 10 Jun 2022 03:10:59 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 10 Jun 2022 03:11:00 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=16';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/nextcloud.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 10 Jun 2022 03:11:01 GMT
VOLUME [/var/www/html]
# Fri, 10 Jun 2022 03:14:17 GMT
ENV NEXTCLOUD_VERSION=23.0.5
# Fri, 10 Jun 2022 03:15:09 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         curl -fsSL -o nextcloud.tar.bz2         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com  --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;     apk del .fetch-deps
# Fri, 10 Jun 2022 03:15:11 GMT
COPY multi:497b8d243f90fa6abd88194ba134de5703abecf47c13a92d2f2fb8210d2cfa77 in / 
# Fri, 10 Jun 2022 03:15:12 GMT
COPY multi:7281097c8fd959eff64684726d7707d598f15dc22353d1f6f843624f642bdcd2 in /usr/src/nextcloud/config/ 
# Fri, 10 Jun 2022 03:15:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 10 Jun 2022 03:15:13 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:73b28a5955ec7fb46f2cf0434e4901a889f7dda3f8c9ec496300feb256c7eda8`  
		Last Modified: Mon, 04 Apr 2022 19:10:03 GMT  
		Size: 2.8 MB (2818974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c45a8803aeb5badfcbafc3a64d45ef0d99401331488cc5495a9bf7e66c3c475`  
		Last Modified: Tue, 05 Apr 2022 01:23:59 GMT  
		Size: 1.8 MB (1800021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8efaa6aa5ded5cf73ecb3fc3a3fb655e5cadfea53b9ab939d90bf4ddb8653d0`  
		Last Modified: Tue, 05 Apr 2022 01:23:59 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f0f938930408ae4fa469fe3ce2586fc2b3be3450492deeabddfac3f9533860`  
		Last Modified: Tue, 05 Apr 2022 01:23:59 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e0b62b5d18cc4ec0666588307755c4d90ce4a267adee632592743f539445937`  
		Last Modified: Fri, 10 Jun 2022 01:37:58 GMT  
		Size: 10.9 MB (10898750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b87de64668bc1af479ba48b2ff4a67ac4da999858880cf1b11b4cd14f9329260`  
		Last Modified: Fri, 10 Jun 2022 01:37:56 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995f465484ac9e076d3999cd5d92cb2fe0725d8d7ef51455d0b32b575fdcba0f`  
		Last Modified: Fri, 10 Jun 2022 01:38:19 GMT  
		Size: 14.2 MB (14189817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e307567fa10841d9819fa683f52dfd882d5db4601bff2fd4751386fa2108255c`  
		Last Modified: Fri, 10 Jun 2022 01:38:17 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9499770462aac25ec05f59aa009e31694f6f0fe6389d2c7aa2468300026a289c`  
		Last Modified: Fri, 10 Jun 2022 01:38:17 GMT  
		Size: 18.4 KB (18426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a10008ce36ccb67750e7459be007fe50a0cbc83c43f60304806d1a257e95413`  
		Last Modified: Fri, 10 Jun 2022 01:38:17 GMT  
		Size: 8.6 KB (8566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b5e32e7c915a1f3d99daf8d7d18656f0c08a3ed2693fdfcf9bc291d9599377d`  
		Last Modified: Fri, 10 Jun 2022 03:21:42 GMT  
		Size: 798.6 KB (798584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c9cc0a4603501403e923ec814d8e506881bea1561f9ead95aad99e72584b280`  
		Last Modified: Fri, 10 Jun 2022 03:21:57 GMT  
		Size: 25.6 MB (25558147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbdc5b0d58ca37a9107fff63c28365b9db79443aac2a8ffd8097a94bbce409d5`  
		Last Modified: Fri, 10 Jun 2022 03:21:39 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d6f04ad74fa5bdc3ce4a787acb177f123bbee5ccd1c41aeaab2ff7f1ad7c7fd`  
		Last Modified: Fri, 10 Jun 2022 03:24:52 GMT  
		Size: 153.4 MB (153394983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14155bd56b518d02936bc4b937b4547d1448d077ebaf2eb5dac5f8d4e013fa8b`  
		Last Modified: Fri, 10 Jun 2022 03:24:32 GMT  
		Size: 3.0 KB (2964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:427333c647f6fe8c5e1c63abb23b9bea1523b33ec370861b01f6b78ebb4009df`  
		Last Modified: Fri, 10 Jun 2022 03:24:53 GMT  
		Size: 2.1 KB (2138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:production-fpm-alpine` - linux; ppc64le

```console
$ docker pull nextcloud@sha256:9c14cf19dcd2e3d59ebca49afd3258c67a9d6a9c44a3e5cdd0753444e3b366c3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.1 MB (209116392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11db881b53a5ea099616ac05882d333f0bb1f9cbd1df73d278c4f70b6d9eafe4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 05 Apr 2022 00:23:30 GMT
ADD file:960cf6f9d3d1cfcb36c2d67dd4c3eaba7db1d0c7afe97968512248d7f234ad47 in / 
# Tue, 05 Apr 2022 00:23:32 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 01:16:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 05 Apr 2022 01:16:42 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 05 Apr 2022 01:16:56 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 05 Apr 2022 01:16:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 05 Apr 2022 01:17:05 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 05 Apr 2022 01:17:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 05 Apr 2022 01:17:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 05 Apr 2022 01:17:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 05 Apr 2022 02:09:29 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 13 May 2022 02:24:02 GMT
ENV PHP_VERSION=8.0.19
# Fri, 13 May 2022 02:24:11 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.19.tar.xz.asc
# Fri, 13 May 2022 02:24:19 GMT
ENV PHP_SHA256=ba62219c4b0486cbb2a04f0796749a46b0ee1f5a142ed454212b4e2460cb0fab
# Fri, 13 May 2022 02:24:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 13 May 2022 02:25:01 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 13 May 2022 02:36:51 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 13 May 2022 02:37:02 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 13 May 2022 02:37:16 GMT
RUN docker-php-ext-enable sodium
# Fri, 13 May 2022 02:37:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 13 May 2022 02:37:30 GMT
WORKDIR /var/www/html
# Fri, 13 May 2022 02:37:39 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 13 May 2022 02:37:45 GMT
STOPSIGNAL SIGQUIT
# Fri, 13 May 2022 02:37:52 GMT
EXPOSE 9000
# Fri, 13 May 2022 02:37:56 GMT
CMD ["php-fpm"]
# Fri, 13 May 2022 07:33:32 GMT
RUN set -ex;         apk add --no-cache         rsync     ;         rm /var/spool/cron/crontabs/root;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Fri, 13 May 2022 07:37:56 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         autoconf         freetype-dev         icu-dev         libevent-dev         libjpeg-turbo-dev         libmcrypt-dev         libpng-dev         libmemcached-dev         libxml2-dev         libzip-dev         openldap-dev         pcre-dev         postgresql-dev         imagemagick-dev         libwebp-dev         gmp-dev     ;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap;     docker-php-ext-install -j "$(nproc)"         bcmath         exif         gd         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         zip         gmp     ;         pecl install APCu-5.1.21;     pecl install memcached-3.2.0;     pecl install redis-5.3.7;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --virtual .nextcloud-phpext-rundeps $runDeps;     apk del .build-deps
# Fri, 13 May 2022 07:38:05 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 13 May 2022 07:38:12 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 13 May 2022 07:38:40 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=16';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/nextcloud.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 13 May 2022 07:38:58 GMT
VOLUME [/var/www/html]
# Fri, 20 May 2022 22:04:17 GMT
ENV NEXTCLOUD_VERSION=23.0.5
# Fri, 20 May 2022 22:05:53 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         curl -fsSL -o nextcloud.tar.bz2         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com  --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;     apk del .fetch-deps
# Fri, 20 May 2022 22:05:58 GMT
COPY multi:497b8d243f90fa6abd88194ba134de5703abecf47c13a92d2f2fb8210d2cfa77 in / 
# Fri, 20 May 2022 22:05:59 GMT
COPY multi:7281097c8fd959eff64684726d7707d598f15dc22353d1f6f843624f642bdcd2 in /usr/src/nextcloud/config/ 
# Fri, 20 May 2022 22:06:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 20 May 2022 22:06:06 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:1877acf2d48ed8bcb5bd9756a95aca0c077457be7cf4fcef25807f4e9be88db1`  
		Last Modified: Mon, 04 Apr 2022 19:09:49 GMT  
		Size: 2.8 MB (2811186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb67fc22738d58442db1bd40a3c6f60cb5038ef87b356fda058eae811b9e66a1`  
		Last Modified: Tue, 05 Apr 2022 03:22:51 GMT  
		Size: 1.7 MB (1744650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7c452ba09cd632ffe58aa658dc18133d1783bb3b475ac3001e7cb6492a41dcb`  
		Last Modified: Tue, 05 Apr 2022 03:22:51 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03960c8a570255096ca4926f8aac09cdf62550255cb84376f5dab02635482972`  
		Last Modified: Tue, 05 Apr 2022 03:22:51 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4887ccb7fd455fab8ae38f2cbe978a3b6ac34dc15e5a9b51e3ef4b3123259b15`  
		Last Modified: Fri, 13 May 2022 03:23:50 GMT  
		Size: 10.8 MB (10798964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47019057302b25261fd48f6e8dbd4a566d0dc9991af10d1a2fdc0f9edd18d60f`  
		Last Modified: Fri, 13 May 2022 03:23:49 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:017cce984823a0205768157cf8f972c19507ae824bc52fc553f948af8d1d1169`  
		Last Modified: Fri, 13 May 2022 03:24:33 GMT  
		Size: 14.3 MB (14258763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d278da191c051a29044ead0944b0187cf4d86a155bc9b2e29e33ac01f439d8e5`  
		Last Modified: Fri, 13 May 2022 03:24:30 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25b47cca46f5cd1e7ae0817feaed4af76213bf8cf54a33bb8e58695c31586115`  
		Last Modified: Fri, 13 May 2022 03:24:30 GMT  
		Size: 18.5 KB (18523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94b09d2b1997f5ad300d36bb3b81b08ca368fc6b75b43268dc89c6ae10919c12`  
		Last Modified: Fri, 13 May 2022 03:24:30 GMT  
		Size: 8.6 KB (8572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7564f4bf79bb5309365ea23431594256b80a4c03ee539ebc74607cc09a60b686`  
		Last Modified: Fri, 13 May 2022 08:18:04 GMT  
		Size: 973.9 KB (973935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87831e911102a14cfcab08a4be7634ba8be8440f94fca1c865d494c8d9fd3225`  
		Last Modified: Fri, 13 May 2022 08:18:19 GMT  
		Size: 25.1 MB (25099751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b50da46c59c722795c279d5e661763f3adc47c5c3b2e18c05703ffa68d0c46fc`  
		Last Modified: Fri, 13 May 2022 08:17:59 GMT  
		Size: 597.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e40d9485b99d217cd89e15aa05d150bc3d670c9f7e27aaa3f4f4aa1f039c8af`  
		Last Modified: Fri, 20 May 2022 22:31:58 GMT  
		Size: 153.4 MB (153391865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2a4bbd2af7ad098e2f97cf013b2398889dac4c097484ecd245175c9b2b50fa6`  
		Last Modified: Fri, 20 May 2022 22:30:06 GMT  
		Size: 3.0 KB (2963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aaf47c0ebf2c10eff900aa346db1b58cf33681736ed13a67c6bab581f4d32c3`  
		Last Modified: Fri, 20 May 2022 22:30:07 GMT  
		Size: 2.1 KB (2143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:production-fpm-alpine` - linux; s390x

```console
$ docker pull nextcloud@sha256:f9921430821968d9fca3c0d838df87bdf9768b47cead6e496c36fb155f0b02fb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.8 MB (206847027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:521fe7e02230140d75373f99c11b1e2878c042efe701d5a50b3303e17e263433`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 04 Apr 2022 23:41:39 GMT
ADD file:f22e4b2be87d3c59c8c609acf79015938dc1fba0b26d7c1b59bd0fc36d63a906 in / 
# Mon, 04 Apr 2022 23:41:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 00:02:57 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 05 Apr 2022 00:02:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 05 Apr 2022 00:02:59 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 05 Apr 2022 00:02:59 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 05 Apr 2022 00:03:00 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 05 Apr 2022 00:03:00 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 05 Apr 2022 00:03:00 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 05 Apr 2022 00:03:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 05 Apr 2022 00:29:06 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Thu, 12 May 2022 20:42:51 GMT
ENV PHP_VERSION=8.0.19
# Thu, 12 May 2022 20:42:51 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.19.tar.xz.asc
# Thu, 12 May 2022 20:42:51 GMT
ENV PHP_SHA256=ba62219c4b0486cbb2a04f0796749a46b0ee1f5a142ed454212b4e2460cb0fab
# Thu, 12 May 2022 20:42:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 12 May 2022 20:42:55 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 12 May 2022 20:48:45 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 12 May 2022 20:48:46 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 12 May 2022 20:48:47 GMT
RUN docker-php-ext-enable sodium
# Thu, 12 May 2022 20:48:47 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 May 2022 20:48:48 GMT
WORKDIR /var/www/html
# Thu, 12 May 2022 20:48:48 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 12 May 2022 20:48:48 GMT
STOPSIGNAL SIGQUIT
# Thu, 12 May 2022 20:48:48 GMT
EXPOSE 9000
# Thu, 12 May 2022 20:48:48 GMT
CMD ["php-fpm"]
# Thu, 12 May 2022 23:19:24 GMT
RUN set -ex;         apk add --no-cache         rsync     ;         rm /var/spool/cron/crontabs/root;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Thu, 12 May 2022 23:21:08 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         autoconf         freetype-dev         icu-dev         libevent-dev         libjpeg-turbo-dev         libmcrypt-dev         libpng-dev         libmemcached-dev         libxml2-dev         libzip-dev         openldap-dev         pcre-dev         postgresql-dev         imagemagick-dev         libwebp-dev         gmp-dev     ;         docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap;     docker-php-ext-install -j "$(nproc)"         bcmath         exif         gd         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         zip         gmp     ;         pecl install APCu-5.1.21;     pecl install memcached-3.2.0;     pecl install redis-5.3.7;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;     rm -r /tmp/pear;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --virtual .nextcloud-phpext-rundeps $runDeps;     apk del .build-deps
# Thu, 12 May 2022 23:21:09 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 12 May 2022 23:21:09 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 12 May 2022 23:21:09 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=16';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/nextcloud.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Thu, 12 May 2022 23:21:10 GMT
VOLUME [/var/www/html]
# Fri, 20 May 2022 21:08:35 GMT
ENV NEXTCLOUD_VERSION=23.0.5
# Fri, 20 May 2022 21:09:28 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         curl -fsSL -o nextcloud.tar.bz2         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com  --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;     apk del .fetch-deps
# Fri, 20 May 2022 21:09:39 GMT
COPY multi:497b8d243f90fa6abd88194ba134de5703abecf47c13a92d2f2fb8210d2cfa77 in / 
# Fri, 20 May 2022 21:09:40 GMT
COPY multi:7281097c8fd959eff64684726d7707d598f15dc22353d1f6f843624f642bdcd2 in /usr/src/nextcloud/config/ 
# Fri, 20 May 2022 21:09:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 20 May 2022 21:09:41 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:a27b630f446c3da376a30cf610e4bfa6847f8b87c83702c29e72b986f4e52d28`  
		Last Modified: Mon, 04 Apr 2022 23:42:37 GMT  
		Size: 2.6 MB (2600375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df780ceebfdd113d5a6f5772c1d4abeb603e14b99c871ea2281632b11cf6f759`  
		Last Modified: Tue, 05 Apr 2022 01:09:34 GMT  
		Size: 1.8 MB (1760653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca5640ab2fd0b3501350a8a837b003d809c84b6169e11a74c71e7a193175a3e3`  
		Last Modified: Tue, 05 Apr 2022 01:09:35 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4910c970dadd8c90e6942fd635f2d508e9f2a2ecd4c5281578cf6470fa8bc432`  
		Last Modified: Tue, 05 Apr 2022 01:09:34 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc0cdcd558f5d71b3ee3b56c7051a8d6e989384743f4953c47dc2fd6a7787d7`  
		Last Modified: Thu, 12 May 2022 21:17:07 GMT  
		Size: 10.8 MB (10798962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716e006f544710cd81721408b9f2149292cda8d853b4f8218e299a4744c3039e`  
		Last Modified: Thu, 12 May 2022 21:17:07 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3208a75c8604202aa909dccf15db15fe13b499a4dfd9571e0f2e5e5012a2d9d`  
		Last Modified: Thu, 12 May 2022 21:17:28 GMT  
		Size: 12.9 MB (12899552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a840b469235faa25ca16f9379fd42a4c560db3d07b11955d7517dff64791b86f`  
		Last Modified: Thu, 12 May 2022 21:17:27 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7de3a8c24739443edb182add0ef47847a10b0284512b84e9d202cb148f2913f`  
		Last Modified: Thu, 12 May 2022 21:17:27 GMT  
		Size: 18.6 KB (18571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bc237519d4e0c33369a4ecb9332ad7416675c330365934039a2cc56bb90be90`  
		Last Modified: Thu, 12 May 2022 21:17:27 GMT  
		Size: 8.6 KB (8570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ae3dbd424be69ada48d78db68937cfebb687714cb9ba46905bf6c5822ade63`  
		Last Modified: Thu, 12 May 2022 23:31:09 GMT  
		Size: 846.7 KB (846720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a138106e1bb738e4c46e6737705558de41e1be10cef6aacb57bad110e389608f`  
		Last Modified: Thu, 12 May 2022 23:31:11 GMT  
		Size: 24.5 MB (24511678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94b25a3ad864b6b3a9acee7ada5bc639a5bdb8d89ff3e19b3cfbf20305a44efb`  
		Last Modified: Thu, 12 May 2022 23:31:08 GMT  
		Size: 593.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fab988caff3c2467dc26941d7ae4e0f8e2daae90f3dd5810efd00af011e5b77`  
		Last Modified: Fri, 20 May 2022 21:18:37 GMT  
		Size: 153.4 MB (153391778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0beede44cc2ca30b2c8e4a4fc12faf8893c11731048c14e927b5db65d9f0daa`  
		Last Modified: Fri, 20 May 2022 21:18:20 GMT  
		Size: 3.0 KB (2963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c35e9a421b717b1ad8854db02bf8c3a6b7c34a13b65a02872aed9df6765384ce`  
		Last Modified: Fri, 20 May 2022 21:18:20 GMT  
		Size: 2.1 KB (2140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
