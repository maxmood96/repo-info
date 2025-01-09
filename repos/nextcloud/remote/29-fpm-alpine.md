## `nextcloud:29-fpm-alpine`

```console
$ docker pull nextcloud@sha256:cd7d69fa3817001b7cc483e60ba3609f59ae6dbd011923255eb1f4f2039c4666
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

### `nextcloud:29-fpm-alpine` - linux; amd64

```console
$ docker pull nextcloud@sha256:a26593e852cc560b281469f08ed248fa6290909ddde467e83851148cb9b2c496
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.7 MB (307749416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd12e81778ddcb597c9071225a7c64e0ca53444e5f7d55ce510a20473ff257e1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 05 Dec 2024 20:29:40 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 05 Dec 2024 20:29:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 05 Dec 2024 20:29:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 05 Dec 2024 20:29:40 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_VERSION=8.2.27
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.27.tar.xz.asc
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_SHA256=3eec91294d8c09b3df80b39ec36d574ed9b05de4c8afcb25fa215d48f9ecbc6b
# Thu, 05 Dec 2024 20:29:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 05 Dec 2024 20:29:40 GMT
WORKDIR /var/www/html
# Thu, 05 Dec 2024 20:29:40 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
STOPSIGNAL SIGQUIT
# Thu, 05 Dec 2024 20:29:40 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 05 Dec 2024 20:29:40 GMT
CMD ["php-fpm"]
# Thu, 05 Dec 2024 20:29:40 GMT
RUN set -ex;         apk add --no-cache         imagemagick         imagemagick-pdf         imagemagick-jpeg         imagemagick-raw         imagemagick-tiff         imagemagick-heic         imagemagick-webp         imagemagick-svg         rsync     ;         rm /var/spool/cron/crontabs/root;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         autoconf         freetype-dev         gmp-dev         icu-dev         imagemagick-dev         libevent-dev         libjpeg-turbo-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libwebp-dev         libxml2-dev         libzip-dev         openldap-dev         pcre-dev         postgresql-dev     ;         docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap;     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.24;     pecl install imagick-3.7.0;     pecl install memcached-3.3.0;     pecl install redis-6.1.0;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .nextcloud-phpext-rundeps $runDeps;     apk del --no-network .build-deps # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 05 Dec 2024 20:29:40 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
VOLUME [/var/www/html]
# Thu, 05 Dec 2024 20:29:40 GMT
ENV NEXTCLOUD_VERSION=29.0.10
# Thu, 05 Dec 2024 20:29:40 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-29.0.10.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-29.0.10.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com  --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;     apk del --no-network .fetch-deps # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Dec 2024 20:29:40 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:098416b50b349d4cc7c38e06ae1277d78ee9c7dd22755ae18aa755bb3b93cc72`  
		Last Modified: Wed, 08 Jan 2025 18:11:12 GMT  
		Size: 3.3 MB (3308790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:febeecff39cd3f20c090cf63f3b6c572dc1c7fbe02bc94b129d1418ab41f818d`  
		Last Modified: Wed, 08 Jan 2025 18:11:12 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b1816711da8fcd731ae8681986b40c631ba1b4af2981134d97b2e55cb1fb4d`  
		Last Modified: Wed, 08 Jan 2025 18:11:12 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2266b936f7140a13eeb816d5d9b1c63ff2e2cefcffa11fed94ad37e0d0782122`  
		Last Modified: Wed, 08 Jan 2025 18:11:12 GMT  
		Size: 12.2 MB (12172236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3301b9993d58851ecbb799d421f9dd9e66518465904685a951fad6f061fe512`  
		Last Modified: Wed, 08 Jan 2025 18:11:13 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c0f845a9e21b1f50becaf8ea56bcae2ce923c39b99c1dc0594fc98d4ac22fc`  
		Last Modified: Wed, 08 Jan 2025 18:11:13 GMT  
		Size: 12.9 MB (12876980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0369601958c4663d5fe0305da32eff0b0eae3743ecd959a19bed00641cc263`  
		Last Modified: Wed, 08 Jan 2025 18:11:13 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:268a2c07cda3b8e6c9e2208fe43716ffa54551ab8af84c930d907ce0385f9b9d`  
		Last Modified: Wed, 08 Jan 2025 18:11:14 GMT  
		Size: 19.7 KB (19711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad0109653f56fdae24cbc264a5282cda4738d9b9179089830f12e86798ea061`  
		Last Modified: Wed, 08 Jan 2025 18:11:14 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce9b7b12ae4e88f152b4982d579a160c635ca62833c9083f1409001bf0be1870`  
		Last Modified: Wed, 08 Jan 2025 18:27:45 GMT  
		Size: 43.1 MB (43119499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1e7a94c80a2ad3b90cb55340eb1c6f6a88fd3dd0286efea1e2e40c91db1cf8`  
		Last Modified: Wed, 08 Jan 2025 18:27:45 GMT  
		Size: 7.4 MB (7372334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62060f2be9e40616995362d230855747c8c5c7c20767eb4f3010d1747fcbc1d`  
		Last Modified: Wed, 08 Jan 2025 18:27:45 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37eed7334e191df01ef6fb463b86b03667ebc5508ed2ddc08fd4584a85123d69`  
		Last Modified: Wed, 08 Jan 2025 18:27:48 GMT  
		Size: 225.2 MB (225233376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8a24efcbc917c43d13bc8bf0082a3b4ad45c4fe7baa223916b8a872ce0055e4`  
		Last Modified: Wed, 08 Jan 2025 18:27:45 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d4e95e11d893b7dbb674ee563158123f8c248c561927bbcd03052d67952e868`  
		Last Modified: Wed, 08 Jan 2025 18:27:46 GMT  
		Size: 2.3 KB (2336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:29-fpm-alpine` - unknown; unknown

```console
$ docker pull nextcloud@sha256:9d1935d5f08722918ac536cbfeafa7ea16116fc4f2ef66852290d7dfe4eec335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 KB (42106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbc87697c84cab64c160093bb43450f75be8a81f4f11355e56410c7be11ae507`

```dockerfile
```

-	Layers:
	-	`sha256:24756fd079e2851735959bd2403e1b8d2365c519c6fdb327f4d08ba2f039aa72`  
		Last Modified: Wed, 08 Jan 2025 18:27:45 GMT  
		Size: 42.1 KB (42106 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:29-fpm-alpine` - linux; arm variant v6

```console
$ docker pull nextcloud@sha256:23c2f3dbcd0ce41527ab1bd30cd48b96beef70f90030e234b21f5a78f16fa900
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.6 MB (299586612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbb80180a15f48262e847361835c0bd8c78ddc848376ffd5c2188829717bee5d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 05 Dec 2024 20:29:40 GMT
ADD alpine-minirootfs-3.20.4-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 05 Dec 2024 20:29:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 05 Dec 2024 20:29:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 05 Dec 2024 20:29:40 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_VERSION=8.2.27
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.27.tar.xz.asc
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_SHA256=3eec91294d8c09b3df80b39ec36d574ed9b05de4c8afcb25fa215d48f9ecbc6b
# Thu, 05 Dec 2024 20:29:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 05 Dec 2024 20:29:40 GMT
WORKDIR /var/www/html
# Thu, 05 Dec 2024 20:29:40 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
STOPSIGNAL SIGQUIT
# Thu, 05 Dec 2024 20:29:40 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 05 Dec 2024 20:29:40 GMT
CMD ["php-fpm"]
# Thu, 05 Dec 2024 20:29:40 GMT
RUN set -ex;         apk add --no-cache         imagemagick         imagemagick-pdf         imagemagick-jpeg         imagemagick-raw         imagemagick-tiff         imagemagick-heic         imagemagick-webp         imagemagick-svg         rsync     ;         rm /var/spool/cron/crontabs/root;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         autoconf         freetype-dev         gmp-dev         icu-dev         imagemagick-dev         libevent-dev         libjpeg-turbo-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libwebp-dev         libxml2-dev         libzip-dev         openldap-dev         pcre-dev         postgresql-dev     ;         docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap;     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.24;     pecl install imagick-3.7.0;     pecl install memcached-3.3.0;     pecl install redis-6.1.0;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .nextcloud-phpext-rundeps $runDeps;     apk del --no-network .build-deps # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 05 Dec 2024 20:29:40 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
VOLUME [/var/www/html]
# Thu, 05 Dec 2024 20:29:40 GMT
ENV NEXTCLOUD_VERSION=29.0.10
# Thu, 05 Dec 2024 20:29:40 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-29.0.10.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-29.0.10.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com  --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;     apk del --no-network .fetch-deps # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Dec 2024 20:29:40 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:9327c400cc7c63bc8696a8da86f21db1ffdb7ce43885aa521a67ab8105dd2af9`  
		Last Modified: Tue, 07 Jan 2025 02:29:49 GMT  
		Size: 3.4 MB (3363944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aeb6e5e4c2e68718d1f73ada486908f719d13b227a11f78fc8876bdae65936e`  
		Last Modified: Tue, 07 Jan 2025 04:16:48 GMT  
		Size: 3.3 MB (3277802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da5effe2170797797df1994313aee89dcd1884282164d0f8a7b2b6624090726`  
		Last Modified: Tue, 07 Jan 2025 04:16:48 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8e18edcb50238487ec3d15c28791318639104f7da84baac7d0aee6de4f24e5`  
		Last Modified: Tue, 07 Jan 2025 04:16:48 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd8f82a038e05a38d256bf25ebd6bc4e3d90e687fc337ebcc44a4a9c2d2b7c72`  
		Last Modified: Tue, 07 Jan 2025 05:52:44 GMT  
		Size: 12.2 MB (12172084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d239563fd4deb3eb150eafdd816921ecf973023856ff837d38878b9761214c04`  
		Last Modified: Tue, 07 Jan 2025 05:52:44 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68853dff18482e28b7578e834e4204e8ae15404f9477ade0cb02594ac991fb63`  
		Last Modified: Tue, 07 Jan 2025 05:56:32 GMT  
		Size: 11.7 MB (11721397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e5f42753fb6a5d5fe660b382f8cdfc7b50cd5b6fbd9640959cafb14b6381404`  
		Last Modified: Tue, 07 Jan 2025 05:56:31 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1c9848e8f9fbf4c8583c01320e070779ca8e966c1594e23274ae1915b8b965`  
		Last Modified: Tue, 07 Jan 2025 05:56:31 GMT  
		Size: 19.2 KB (19220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b59dacde45a6d418bc41b0332c4702090a2c9c29eea6fea5de4d0965f0dc3a`  
		Last Modified: Tue, 07 Jan 2025 05:56:32 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7a93180751d27f859605bb33900b69b701342d445763fc4a005e0ecddc7651`  
		Last Modified: Tue, 07 Jan 2025 19:12:32 GMT  
		Size: 37.0 MB (37045570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82fe1027a6dd1ea3cf7d6935d5dcae6c9ea602ce95c200fdfa279fae97647c4a`  
		Last Modified: Tue, 07 Jan 2025 19:12:32 GMT  
		Size: 6.7 MB (6732169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6239f1b22a913cc4b2a65ad47e09118871a08cf1eda05e82bb38333388cd47a9`  
		Last Modified: Tue, 07 Jan 2025 19:12:31 GMT  
		Size: 708.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93fc09bf2b2a539ada8709bcac53c106de6817e936efce1a8e664c9f5e86abfb`  
		Last Modified: Tue, 07 Jan 2025 19:14:28 GMT  
		Size: 225.2 MB (225234175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f8e2b21ee9fe94287aae4bbfdc62741ad6cdfffe35a0bc3dd711d509f2d807`  
		Last Modified: Fri, 20 Dec 2024 23:45:37 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3946d5f900eebf0a4034ebeb3bab199329535bce22227e6f3225de13ccf9c02`  
		Last Modified: Tue, 07 Jan 2025 19:14:23 GMT  
		Size: 2.3 KB (2337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:29-fpm-alpine` - unknown; unknown

```console
$ docker pull nextcloud@sha256:97f787d1cd715b65ef9c8b81098f238da201ee33e5a50405caa06d8c8c4c2f2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 KB (42213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9873f8226a2a43f35a1e9513a63be4bc8a09984e42b3f46f242bb168c8fbf2bd`

```dockerfile
```

-	Layers:
	-	`sha256:26e5465d0163fe2d3032dadfcaf7509185375494ce3d79e5f7962e2e10914fe9`  
		Last Modified: Tue, 07 Jan 2025 19:14:22 GMT  
		Size: 42.2 KB (42213 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:29-fpm-alpine` - linux; arm variant v7

```console
$ docker pull nextcloud@sha256:6d2df779348f90036d942c08abaa6a5b60a7e7e43a66b99d4cd0f2a107429e9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.4 MB (297370914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98e66c4e4e94d6fb61b918ee97c93d153ae31b57b944e7b6b86b0c7efb2f29a0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 05 Dec 2024 20:29:40 GMT
ADD alpine-minirootfs-3.20.4-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 05 Dec 2024 20:29:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 05 Dec 2024 20:29:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 05 Dec 2024 20:29:40 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_VERSION=8.2.27
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.27.tar.xz.asc
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_SHA256=3eec91294d8c09b3df80b39ec36d574ed9b05de4c8afcb25fa215d48f9ecbc6b
# Thu, 05 Dec 2024 20:29:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 05 Dec 2024 20:29:40 GMT
WORKDIR /var/www/html
# Thu, 05 Dec 2024 20:29:40 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
STOPSIGNAL SIGQUIT
# Thu, 05 Dec 2024 20:29:40 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 05 Dec 2024 20:29:40 GMT
CMD ["php-fpm"]
# Thu, 05 Dec 2024 20:29:40 GMT
RUN set -ex;         apk add --no-cache         imagemagick         imagemagick-pdf         imagemagick-jpeg         imagemagick-raw         imagemagick-tiff         imagemagick-heic         imagemagick-webp         imagemagick-svg         rsync     ;         rm /var/spool/cron/crontabs/root;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         autoconf         freetype-dev         gmp-dev         icu-dev         imagemagick-dev         libevent-dev         libjpeg-turbo-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libwebp-dev         libxml2-dev         libzip-dev         openldap-dev         pcre-dev         postgresql-dev     ;         docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap;     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.24;     pecl install imagick-3.7.0;     pecl install memcached-3.3.0;     pecl install redis-6.1.0;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .nextcloud-phpext-rundeps $runDeps;     apk del --no-network .build-deps # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 05 Dec 2024 20:29:40 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
VOLUME [/var/www/html]
# Thu, 05 Dec 2024 20:29:40 GMT
ENV NEXTCLOUD_VERSION=29.0.10
# Thu, 05 Dec 2024 20:29:40 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-29.0.10.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-29.0.10.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com  --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;     apk del --no-network .fetch-deps # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Dec 2024 20:29:40 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:0695ed689d581197c59573cee0b2f2ef2c3a332e0d52bbb8f0e7e0865c2d5b23`  
		Last Modified: Tue, 07 Jan 2025 02:55:40 GMT  
		Size: 3.1 MB (3091288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666fe9f2778fc13085387269ec8e5a9a92fe5a5cd43a1c04d0550044cef029e5`  
		Last Modified: Tue, 07 Jan 2025 04:03:10 GMT  
		Size: 3.1 MB (3086378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad33e8f07354fb119b701cf115f1a2dc9d9e81c9a1d4e577cc25369377d26496`  
		Last Modified: Tue, 07 Jan 2025 04:03:09 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7628e2f49a6657703e1bf3b16f926b733c3fcfdc62265ce69d5a5b75d985504d`  
		Last Modified: Tue, 07 Jan 2025 04:03:09 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9f039be4f7d666405429bcb67d4b7210330cac059e2481adfb1ddf38ee8ec7b`  
		Last Modified: Tue, 07 Jan 2025 05:36:06 GMT  
		Size: 12.2 MB (12172083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0ec1a1ea3118bc910350ec3b15f7cd08583213ddb4cda7dd74c517266492c6`  
		Last Modified: Tue, 07 Jan 2025 05:36:05 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c4484b2955a17c8565aaae1c21657b6c2adc2d35bbd6d9bb36b9e38ef50bf6`  
		Last Modified: Tue, 07 Jan 2025 05:39:55 GMT  
		Size: 11.0 MB (10984237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc81d9cb2f739347320ad4243da2378eb9385e0d28c3d2a2a2f6a0ecb050d1b`  
		Last Modified: Tue, 07 Jan 2025 05:39:55 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c16e361ca5a140469d6ae9c9d18cb04e47d6f14f4899b6afe57da7298334c16`  
		Last Modified: Tue, 07 Jan 2025 05:39:55 GMT  
		Size: 19.2 KB (19226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6380f32e52417ce841a1b973b048bdaf6d257521d38a75865873be480c4862`  
		Last Modified: Tue, 07 Jan 2025 05:39:55 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf021a31fb80004565cfa4316b58fd7976cb5db577bee5fb6ad15ee68abfa74`  
		Last Modified: Tue, 07 Jan 2025 19:32:42 GMT  
		Size: 36.1 MB (36065534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4366437a366eb50498b2e6f0b34889a2df095d0922ec898976eb056c9560f5e9`  
		Last Modified: Tue, 07 Jan 2025 19:32:41 GMT  
		Size: 6.7 MB (6697659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:973f5cec7263f8a5769710f4a5b2c7a4a580b4d74624549116562501d816fd6e`  
		Last Modified: Tue, 07 Jan 2025 19:32:41 GMT  
		Size: 709.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8922bf1a303fc06a0bb0ff9af67e6950d7260fcdf2332bfa924f3e1fbb6d77f5`  
		Last Modified: Tue, 07 Jan 2025 19:32:47 GMT  
		Size: 225.2 MB (225234270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b13f1cff1f8e193b9bb987a7b0aba82af127bbfc5813de2ffd264b7cd0c927d`  
		Last Modified: Tue, 07 Jan 2025 19:32:42 GMT  
		Size: 3.9 KB (3882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fda11fc3f62825f58e50e3076961cbb18f4d2fa3ee9bd169a4454800aa732ac`  
		Last Modified: Tue, 07 Jan 2025 19:32:42 GMT  
		Size: 2.3 KB (2335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:29-fpm-alpine` - unknown; unknown

```console
$ docker pull nextcloud@sha256:65b489a93cccd1c526ab174575adafc9f413982f8d3fef546ac247754476a3c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 KB (42212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c9f425fecfd6e4fe4fac260b50c32f2275ea7b2759ce09409cd360111e3f77d`

```dockerfile
```

-	Layers:
	-	`sha256:446107d9a8c50e2e0f3bdb8416f54a91222364cfecf520030d145ae1905047dd`  
		Last Modified: Tue, 07 Jan 2025 19:32:41 GMT  
		Size: 42.2 KB (42212 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:29-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull nextcloud@sha256:9e78988417e2e9fb1da8150ea728c10d514c5778469f45b7266dda2c8aa17c3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.3 MB (309285330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa7a646ceea572295c9dfc705897cb1a8787bf503ab7517bc494ac88ae86471e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 05 Dec 2024 20:29:40 GMT
ADD alpine-minirootfs-3.20.4-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 05 Dec 2024 20:29:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 05 Dec 2024 20:29:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 05 Dec 2024 20:29:40 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_VERSION=8.2.27
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.27.tar.xz.asc
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_SHA256=3eec91294d8c09b3df80b39ec36d574ed9b05de4c8afcb25fa215d48f9ecbc6b
# Thu, 05 Dec 2024 20:29:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 05 Dec 2024 20:29:40 GMT
WORKDIR /var/www/html
# Thu, 05 Dec 2024 20:29:40 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
STOPSIGNAL SIGQUIT
# Thu, 05 Dec 2024 20:29:40 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 05 Dec 2024 20:29:40 GMT
CMD ["php-fpm"]
# Thu, 05 Dec 2024 20:29:40 GMT
RUN set -ex;         apk add --no-cache         imagemagick         imagemagick-pdf         imagemagick-jpeg         imagemagick-raw         imagemagick-tiff         imagemagick-heic         imagemagick-webp         imagemagick-svg         rsync     ;         rm /var/spool/cron/crontabs/root;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         autoconf         freetype-dev         gmp-dev         icu-dev         imagemagick-dev         libevent-dev         libjpeg-turbo-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libwebp-dev         libxml2-dev         libzip-dev         openldap-dev         pcre-dev         postgresql-dev     ;         docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap;     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.24;     pecl install imagick-3.7.0;     pecl install memcached-3.3.0;     pecl install redis-6.1.0;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .nextcloud-phpext-rundeps $runDeps;     apk del --no-network .build-deps # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 05 Dec 2024 20:29:40 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
VOLUME [/var/www/html]
# Thu, 05 Dec 2024 20:29:40 GMT
ENV NEXTCLOUD_VERSION=29.0.10
# Thu, 05 Dec 2024 20:29:40 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-29.0.10.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-29.0.10.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com  --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;     apk del --no-network .fetch-deps # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Dec 2024 20:29:40 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:ef22e11fe7735044a1b56fc644666588aa863fb6abe827f676cb9d11ba34d993`  
		Last Modified: Tue, 07 Jan 2025 03:03:03 GMT  
		Size: 4.1 MB (4086686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be12651a1164be1c0ff5ff6b5888077c5a5ce96f08fe1a1eea4c3c70cec19c59`  
		Last Modified: Tue, 07 Jan 2025 04:36:53 GMT  
		Size: 3.3 MB (3341946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a29137c219172cc292e8d59680364cf3eee1a1e71b5507c0237d302305c00ec3`  
		Last Modified: Tue, 07 Jan 2025 04:36:53 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c134198c2af672fa5dd2e3639c0be7847f521d9b05277485eaa64a00c4c20fb`  
		Last Modified: Tue, 07 Jan 2025 04:36:53 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68180f62e12b951a2599954d187137957e78c570ee51f9a25d8fd5d6e1489fa`  
		Last Modified: Tue, 07 Jan 2025 06:21:47 GMT  
		Size: 12.2 MB (12172075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21e514ab4ea37cf35c78027bda3b039f7af592646641336dd27cf3f833ffbd2b`  
		Last Modified: Tue, 07 Jan 2025 06:21:46 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78861658c52ee67e18905783c7b49166c4c81edbf0ba173a134453900c6ac14f`  
		Last Modified: Tue, 07 Jan 2025 06:26:10 GMT  
		Size: 12.9 MB (12945232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9bea323f9c42539041fe0f49045eca5b089fe192517bfbbcfcee6d3dd03d1a8`  
		Last Modified: Tue, 07 Jan 2025 06:26:09 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e990f9687d57f5d72334b62fe804ae26485580df0079007b5e833dcbd54c522`  
		Last Modified: Tue, 07 Jan 2025 06:26:10 GMT  
		Size: 19.2 KB (19199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467a56e07d096500834258908ed92d01f6ac6fa2bd20ff4d5f04796c56bad551`  
		Last Modified: Tue, 07 Jan 2025 06:26:10 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b9c0ef4223c60aaa646477045caad59a069de4e6c334d8e6dbcbaced6c0307`  
		Last Modified: Tue, 07 Jan 2025 17:17:27 GMT  
		Size: 43.8 MB (43808843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fbcacb5c57512d3b72185cf4da7c970a90f0105f1ec825aca5666a34f8b7af5`  
		Last Modified: Tue, 07 Jan 2025 17:17:26 GMT  
		Size: 7.7 MB (7656997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948817a66fd62b2d5c9a4e513761bb1a2ed599456dea2e0928434a87fbaa1ed8`  
		Last Modified: Tue, 07 Jan 2025 17:17:26 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f58e2be5eca047b68a0f19fa821c86a228f92f9ce2524ebad6da52ab3d7a87`  
		Last Modified: Tue, 07 Jan 2025 17:17:32 GMT  
		Size: 225.2 MB (225234120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf8d6e59b8aa7811b820cebaee74cf245d6a832cee7ea9a00014536f7ba63f6`  
		Last Modified: Tue, 07 Jan 2025 17:17:27 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d554f42a3553d7723a86f654e5a87491f26853a30fe97cd7f73070d66141921`  
		Last Modified: Tue, 07 Jan 2025 17:17:28 GMT  
		Size: 2.3 KB (2334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:29-fpm-alpine` - unknown; unknown

```console
$ docker pull nextcloud@sha256:1869c46426a669a409ed6c4a755694f00fec839fbe44b30746b7cdc1f224f2a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 KB (42243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1facfe19ac17a3cf08b121b966e2aabbc0f812022d6d020ef3e54ee525117f63`

```dockerfile
```

-	Layers:
	-	`sha256:2ffc5ce13fbf2782befec686512c3564faa422a840b0499084834c4e9ffbb360`  
		Last Modified: Tue, 07 Jan 2025 17:17:25 GMT  
		Size: 42.2 KB (42243 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:29-fpm-alpine` - linux; 386

```console
$ docker pull nextcloud@sha256:e19a8d0e837e057babc32f969e9c4217d76cd5b26e9cfbac9e80c05b18188adc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.3 MB (306271643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a70a8d1956e796b193a03d674cdab585c3a040871122859a0c133f351e5b2ab`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 05 Dec 2024 20:29:40 GMT
ADD alpine-minirootfs-3.20.5-x86.tar.gz / # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 05 Dec 2024 20:29:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 05 Dec 2024 20:29:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 05 Dec 2024 20:29:40 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_VERSION=8.2.27
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.27.tar.xz.asc
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_SHA256=3eec91294d8c09b3df80b39ec36d574ed9b05de4c8afcb25fa215d48f9ecbc6b
# Thu, 05 Dec 2024 20:29:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 05 Dec 2024 20:29:40 GMT
WORKDIR /var/www/html
# Thu, 05 Dec 2024 20:29:40 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
STOPSIGNAL SIGQUIT
# Thu, 05 Dec 2024 20:29:40 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 05 Dec 2024 20:29:40 GMT
CMD ["php-fpm"]
# Thu, 05 Dec 2024 20:29:40 GMT
RUN set -ex;         apk add --no-cache         imagemagick         imagemagick-pdf         imagemagick-jpeg         imagemagick-raw         imagemagick-tiff         imagemagick-heic         imagemagick-webp         imagemagick-svg         rsync     ;         rm /var/spool/cron/crontabs/root;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         autoconf         freetype-dev         gmp-dev         icu-dev         imagemagick-dev         libevent-dev         libjpeg-turbo-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libwebp-dev         libxml2-dev         libzip-dev         openldap-dev         pcre-dev         postgresql-dev     ;         docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap;     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.24;     pecl install imagick-3.7.0;     pecl install memcached-3.3.0;     pecl install redis-6.1.0;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .nextcloud-phpext-rundeps $runDeps;     apk del --no-network .build-deps # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 05 Dec 2024 20:29:40 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
VOLUME [/var/www/html]
# Thu, 05 Dec 2024 20:29:40 GMT
ENV NEXTCLOUD_VERSION=29.0.10
# Thu, 05 Dec 2024 20:29:40 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-29.0.10.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-29.0.10.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com  --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;     apk del --no-network .fetch-deps # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Dec 2024 20:29:40 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:6d632fc6244662e41ee3b3f29090684a520e615dc5c282638a7587366dcd4fb9`  
		Last Modified: Wed, 08 Jan 2025 17:23:34 GMT  
		Size: 3.5 MB (3470969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786d36b52928954da7808f6c1df4a7e5aa7f96b6f67a08beead55a7811bdd036`  
		Last Modified: Wed, 08 Jan 2025 18:08:10 GMT  
		Size: 3.4 MB (3359955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e6aa805c6c559c646e440b71420701c1049c4d8abb52811e8aeadd089b3958`  
		Last Modified: Wed, 08 Jan 2025 18:08:09 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb7e0385df6fd74baad58982dfd5322a1bc9325e673806e744af54ab86677f2`  
		Last Modified: Wed, 08 Jan 2025 18:08:09 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7315a390c99219bee8ea917ba7be87d8a852c9abbb67bb9afc82bcd0a734b59a`  
		Last Modified: Wed, 08 Jan 2025 18:08:11 GMT  
		Size: 12.2 MB (12172239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0d7ba1b6ce85b34df702db42564d121f30532edc6b0adc4d257ab7f34da0e8`  
		Last Modified: Wed, 08 Jan 2025 18:08:10 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:854203f2539afbe9b2097a8d8620b0e66d8863e4a199ed091b591313b74562d6`  
		Last Modified: Wed, 08 Jan 2025 18:08:11 GMT  
		Size: 13.2 MB (13225699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deef689698359b9ba08519c5108232e399eee8145999bf6c5bf446ad4b81a116`  
		Last Modified: Wed, 08 Jan 2025 18:08:11 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb42b6286081c49d8c92062f2e6ce9248da5fd55ca2f5fabb05a5875ba1dd454`  
		Last Modified: Wed, 08 Jan 2025 18:08:11 GMT  
		Size: 19.7 KB (19714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69745f9319eeffd8f7ca406a8d81a56a8acbee8a2829af5c177d6e17b3e8b009`  
		Last Modified: Wed, 08 Jan 2025 18:08:11 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad0fcdb378ee5de7719bc42c63c55e72f1c1bacf9fd12c31fe4c9c76b22f47c`  
		Last Modified: Wed, 08 Jan 2025 18:29:10 GMT  
		Size: 41.3 MB (41311209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0681fffaa4d7220257578799e1485faf541ddf69fa97a42b47945e698f073ca6`  
		Last Modified: Wed, 08 Jan 2025 18:29:08 GMT  
		Size: 7.5 MB (7457864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff6650ba29528ecfb6250db0b927706a7bd8c15458b11596fca96632334958e`  
		Last Modified: Wed, 08 Jan 2025 18:29:05 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5b88e4a57b70ae61e709ae560aec0155171bbe1147bddad45647f44ea8675d`  
		Last Modified: Wed, 08 Jan 2025 18:29:13 GMT  
		Size: 225.2 MB (225233768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4039bce0cbbcbfbe7c555bcd9ade0f79d1f2a1b7ef5072111549b525b2577d95`  
		Last Modified: Wed, 08 Jan 2025 18:29:08 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1114d6187450f8d3f066d95e2a7c69b901eacb6cd7849d5e59636b88297e021e`  
		Last Modified: Wed, 08 Jan 2025 18:29:09 GMT  
		Size: 2.3 KB (2336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:29-fpm-alpine` - unknown; unknown

```console
$ docker pull nextcloud@sha256:c6a29e63b8eb4cc25be8637160d8137fb03ae21a5b57a9468d2ecb542b66c1de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 KB (42073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66fcee27464bccd213f34e78fd8c52a5a0dfafa851a88eb00152d3c84093bfcf`

```dockerfile
```

-	Layers:
	-	`sha256:a3a9bdd49366f1491fc0359637db29f21085e646d7d6aac068731e58bb5addeb`  
		Last Modified: Wed, 08 Jan 2025 18:29:07 GMT  
		Size: 42.1 KB (42073 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:29-fpm-alpine` - linux; ppc64le

```console
$ docker pull nextcloud@sha256:734d3cc5e21c2cceb9b1da0dc81ce4733cde33cbd1daa930c4efe88d6ce0d61b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.6 MB (313567817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e45aa54b205717c5f24275a7703a1e181e76c0fce128fc27284c1f323cd594bb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 05 Dec 2024 20:29:40 GMT
ADD alpine-minirootfs-3.20.5-ppc64le.tar.gz / # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 05 Dec 2024 20:29:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 05 Dec 2024 20:29:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 05 Dec 2024 20:29:40 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_VERSION=8.2.27
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.27.tar.xz.asc
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_SHA256=3eec91294d8c09b3df80b39ec36d574ed9b05de4c8afcb25fa215d48f9ecbc6b
# Thu, 05 Dec 2024 20:29:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 05 Dec 2024 20:29:40 GMT
WORKDIR /var/www/html
# Thu, 05 Dec 2024 20:29:40 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
STOPSIGNAL SIGQUIT
# Thu, 05 Dec 2024 20:29:40 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 05 Dec 2024 20:29:40 GMT
CMD ["php-fpm"]
# Thu, 05 Dec 2024 20:29:40 GMT
RUN set -ex;         apk add --no-cache         imagemagick         imagemagick-pdf         imagemagick-jpeg         imagemagick-raw         imagemagick-tiff         imagemagick-heic         imagemagick-webp         imagemagick-svg         rsync     ;         rm /var/spool/cron/crontabs/root;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         autoconf         freetype-dev         gmp-dev         icu-dev         imagemagick-dev         libevent-dev         libjpeg-turbo-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libwebp-dev         libxml2-dev         libzip-dev         openldap-dev         pcre-dev         postgresql-dev     ;         docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap;     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.24;     pecl install imagick-3.7.0;     pecl install memcached-3.3.0;     pecl install redis-6.1.0;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .nextcloud-phpext-rundeps $runDeps;     apk del --no-network .build-deps # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 05 Dec 2024 20:29:40 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
VOLUME [/var/www/html]
# Thu, 05 Dec 2024 20:29:40 GMT
ENV NEXTCLOUD_VERSION=29.0.10
# Thu, 05 Dec 2024 20:29:40 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-29.0.10.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-29.0.10.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com  --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;     apk del --no-network .fetch-deps # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Dec 2024 20:29:40 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:3383dff810cd4af0350465f92c0a5f925af062ceac665a36e91384093216a7db`  
		Last Modified: Wed, 08 Jan 2025 17:24:56 GMT  
		Size: 3.6 MB (3574406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac389e1bad8c901cdd7df01f96be5f8508854f3411c6da9e6e8ef6668f4b16c`  
		Last Modified: Wed, 08 Jan 2025 18:46:53 GMT  
		Size: 3.4 MB (3435551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b7f9d7dcac76616498febca2aa6101a5ff06711026417e0332b7700a8e89f8`  
		Last Modified: Wed, 08 Jan 2025 18:46:52 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3bef84277af6646e9da0330c1f81457cb9ace93a33c43f40275eb914946791c`  
		Last Modified: Wed, 08 Jan 2025 18:46:53 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3b521c4e3173f894d141280cea6e8ff6550211f30c9ce60410769fbd3120c3`  
		Last Modified: Wed, 08 Jan 2025 20:15:21 GMT  
		Size: 12.2 MB (12172240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d78a853cbfdfafa9dc261817f00e59a3a65e66cf74349dd2b2b3aa6ac1c547`  
		Last Modified: Wed, 08 Jan 2025 20:15:20 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41efbf34bf082cc78b6dbee80c8220b865406c981d643691b18f6c6cac6713a3`  
		Last Modified: Wed, 08 Jan 2025 20:18:47 GMT  
		Size: 13.4 MB (13375041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf22658ff7b9a512c95372be3497886fa8f81be5f53746b1d391b711e26d571`  
		Last Modified: Wed, 08 Jan 2025 20:18:46 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c13cccd2abb8a8e9b24a391c3c66a0997bc7bc1a65f05da2b7b26641d75c5b3`  
		Last Modified: Wed, 08 Jan 2025 20:18:46 GMT  
		Size: 19.5 KB (19487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ad0acf4d319dbb4502825d9654538a094b02413c1b3a7d034d2ce5a89cb677`  
		Last Modified: Wed, 08 Jan 2025 20:18:46 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd39c7582ac33b78ed80e90909cfe6c95473f4f9d49a9995b7934d89a05db37`  
		Last Modified: Thu, 09 Jan 2025 03:24:10 GMT  
		Size: 48.6 MB (48599521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff87b9a249f37cd817ee969cbe34e076f323b04fe9ae99f897e60f89352d747`  
		Last Modified: Thu, 09 Jan 2025 03:24:09 GMT  
		Size: 7.1 MB (7137865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9268e5df3f2a86fa03b57c1680dda04f14c3da52e1527a976f83bedfdc32c4`  
		Last Modified: Thu, 09 Jan 2025 03:24:08 GMT  
		Size: 709.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862c4c077320e2f953350ef66119d02fc84996303b84e36e7fd073a5597185ff`  
		Last Modified: Thu, 09 Jan 2025 03:24:14 GMT  
		Size: 225.2 MB (225233465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a1834930dc706aeee0f8e6f06da9fd90b35491500976d79676ad35a1acc071`  
		Last Modified: Thu, 09 Jan 2025 03:24:09 GMT  
		Size: 3.9 KB (3882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f88fb5e9258cb487e1f750f0b29d7b4f01ed208f0c6735c944798d70fc702eb`  
		Last Modified: Thu, 09 Jan 2025 03:24:10 GMT  
		Size: 2.3 KB (2335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:29-fpm-alpine` - unknown; unknown

```console
$ docker pull nextcloud@sha256:6ad7858c5fdf3b5f928a771712edba56ca45a3930308ba9a670cee9723a44db7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 KB (42149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b42f1e20414f9c387e966474396312b984730fdd934886213ad73777f50db9fb`

```dockerfile
```

-	Layers:
	-	`sha256:99959e2aae656343ffd281eed467102927abf5f7489e4679bd2e9c6069b72d73`  
		Last Modified: Thu, 09 Jan 2025 03:24:08 GMT  
		Size: 42.1 KB (42149 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:29-fpm-alpine` - linux; riscv64

```console
$ docker pull nextcloud@sha256:89285cb039b2fcea51b1061efb5242eda7f36028c6407deea24beecb907f6836
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.4 MB (306441295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:316bf621b41e33cf77cc3a5c19272de029b31d363fdb522e317d3b262d231ce2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-riscv64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 05 Dec 2024 20:29:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 05 Dec 2024 20:29:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 05 Dec 2024 20:29:40 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_VERSION=8.2.27
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.27.tar.xz.asc
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_SHA256=3eec91294d8c09b3df80b39ec36d574ed9b05de4c8afcb25fa215d48f9ecbc6b
# Thu, 05 Dec 2024 20:29:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 05 Dec 2024 20:29:40 GMT
WORKDIR /var/www/html
# Thu, 05 Dec 2024 20:29:40 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
STOPSIGNAL SIGQUIT
# Thu, 05 Dec 2024 20:29:40 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 05 Dec 2024 20:29:40 GMT
CMD ["php-fpm"]
# Thu, 05 Dec 2024 20:29:40 GMT
RUN set -ex;         apk add --no-cache         imagemagick         imagemagick-pdf         imagemagick-jpeg         imagemagick-raw         imagemagick-tiff         imagemagick-heic         imagemagick-webp         imagemagick-svg         rsync     ;         rm /var/spool/cron/crontabs/root;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         autoconf         freetype-dev         gmp-dev         icu-dev         imagemagick-dev         libevent-dev         libjpeg-turbo-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libwebp-dev         libxml2-dev         libzip-dev         openldap-dev         pcre-dev         postgresql-dev     ;         docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap;     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.24;     pecl install imagick-3.7.0;     pecl install memcached-3.3.0;     pecl install redis-6.1.0;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .nextcloud-phpext-rundeps $runDeps;     apk del --no-network .build-deps # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 05 Dec 2024 20:29:40 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
VOLUME [/var/www/html]
# Thu, 05 Dec 2024 20:29:40 GMT
ENV NEXTCLOUD_VERSION=29.0.10
# Thu, 05 Dec 2024 20:29:40 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-29.0.10.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-29.0.10.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com  --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;     apk del --no-network .fetch-deps # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Dec 2024 20:29:40 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:ea37667e50ca807fa8abc1caf0d21091cbbe1d66b2c217158fb3e91c2787afaf`  
		Last Modified: Tue, 12 Nov 2024 00:55:56 GMT  
		Size: 3.4 MB (3371482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8ca85c9d20c6f76d0a8087ac3a4ddd6a1e40652d189dc8dad7ca6b0737c4b0`  
		Last Modified: Tue, 12 Nov 2024 06:14:49 GMT  
		Size: 5.4 MB (5382174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d2dfe107b4bddcc389bedcee9ca3fc81f02dc0799e313c21f307ddb454b4dc`  
		Last Modified: Tue, 12 Nov 2024 06:14:47 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df7310166e795cb48e721a885b92af688db981613ad6597943011293aca738c`  
		Last Modified: Tue, 12 Nov 2024 06:14:47 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e9326f4fb36b4448d4aaa9ae41be92cc84e67f7f3e396a5cdad1aa2d2290fd`  
		Last Modified: Sat, 21 Dec 2024 11:44:07 GMT  
		Size: 12.2 MB (12172224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1f963fedcf04b4071c3f584a54de4225b9a0dbc62c3f9cf7a68dce2d360a71`  
		Last Modified: Sat, 21 Dec 2024 11:44:04 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834658859dfb145eb334d4dde2df425a0f85545e5246e53f43c4d49c519b4e45`  
		Last Modified: Sat, 21 Dec 2024 12:28:39 GMT  
		Size: 12.7 MB (12723348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f19cbb304f2638d194385df4e0f59293d7ff88074a3b4fb562a3084e8f37718c`  
		Last Modified: Sat, 21 Dec 2024 12:28:37 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6c77521af9cf906f0173285ac5b5c68b336b7a941be548086c69a9865d8993`  
		Last Modified: Sat, 21 Dec 2024 12:28:37 GMT  
		Size: 19.4 KB (19441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be8611b0c3062a1f0c9c39ac99e2330d44a6cafb24fbfbc1bbdaf44321ab7e7`  
		Last Modified: Sat, 21 Dec 2024 12:28:38 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8241c61da8b55c3b740fe8bfdbfe85c729188eb3618ce7101462ffc54b6f6dcf`  
		Last Modified: Sat, 21 Dec 2024 17:48:00 GMT  
		Size: 40.7 MB (40674247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f9ef97b4a51ae244e31176efb9e449de9ae662cd91f8d98a19a2ac1fe6c438`  
		Last Modified: Sat, 21 Dec 2024 17:47:55 GMT  
		Size: 6.8 MB (6844571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c72ce167d26ea47966d9f46793f52cadf10631ecde8632b4990785dee973af`  
		Last Modified: Sat, 21 Dec 2024 17:47:54 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b6c973aadb1cea5cc7073c478d366d9dfcf0c544d5ca9b044574af9cfd3cd0`  
		Last Modified: Sat, 21 Dec 2024 17:57:36 GMT  
		Size: 225.2 MB (225233552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3dd6e97a0110061d44d539e0afce93e21f088d0b6042c2401334bd5c848e1e`  
		Last Modified: Sat, 21 Dec 2024 17:57:05 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1719743f3042d9ad9a41e3f958908655ee8787f7085142b73f338cf66264ab74`  
		Last Modified: Sat, 21 Dec 2024 17:57:05 GMT  
		Size: 2.3 KB (2337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:29-fpm-alpine` - unknown; unknown

```console
$ docker pull nextcloud@sha256:edca14098c0eb5a3fc80088f36082e984cb0655b7132702a2ff91f92d814acae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 KB (42149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:568663fba25d298f9997579b5ad79c0af87eb0226f3a854983e27ce7f14d543e`

```dockerfile
```

-	Layers:
	-	`sha256:fd4eae61e1b398b903d361feabb11f7c829fa21b83215d45c4f073e36013b11d`  
		Last Modified: Sat, 21 Dec 2024 17:57:05 GMT  
		Size: 42.1 KB (42149 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:29-fpm-alpine` - linux; s390x

```console
$ docker pull nextcloud@sha256:b696b9071f75b29c01c37efe8c20cf02f732d157d3c52f9440ed774c3bd69abd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.5 MB (310521122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c06689a784d44b595f3e7ebf8456305df2ea0a452756462a0888e903d5f51fa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 05 Dec 2024 20:29:40 GMT
ADD alpine-minirootfs-3.20.4-s390x.tar.gz / # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 05 Dec 2024 20:29:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 05 Dec 2024 20:29:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 05 Dec 2024 20:29:40 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_VERSION=8.2.27
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.27.tar.xz.asc
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_SHA256=3eec91294d8c09b3df80b39ec36d574ed9b05de4c8afcb25fa215d48f9ecbc6b
# Thu, 05 Dec 2024 20:29:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 05 Dec 2024 20:29:40 GMT
WORKDIR /var/www/html
# Thu, 05 Dec 2024 20:29:40 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
STOPSIGNAL SIGQUIT
# Thu, 05 Dec 2024 20:29:40 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 05 Dec 2024 20:29:40 GMT
CMD ["php-fpm"]
# Thu, 05 Dec 2024 20:29:40 GMT
RUN set -ex;         apk add --no-cache         imagemagick         imagemagick-pdf         imagemagick-jpeg         imagemagick-raw         imagemagick-tiff         imagemagick-heic         imagemagick-webp         imagemagick-svg         rsync     ;         rm /var/spool/cron/crontabs/root;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         autoconf         freetype-dev         gmp-dev         icu-dev         imagemagick-dev         libevent-dev         libjpeg-turbo-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libwebp-dev         libxml2-dev         libzip-dev         openldap-dev         pcre-dev         postgresql-dev     ;         docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap;     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.24;     pecl install imagick-3.7.0;     pecl install memcached-3.3.0;     pecl install redis-6.1.0;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .nextcloud-phpext-rundeps $runDeps;     apk del --no-network .build-deps # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 05 Dec 2024 20:29:40 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 05 Dec 2024 20:29:40 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
VOLUME [/var/www/html]
# Thu, 05 Dec 2024 20:29:40 GMT
ENV NEXTCLOUD_VERSION=29.0.10
# Thu, 05 Dec 2024 20:29:40 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-29.0.10.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-29.0.10.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com  --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;     apk del --no-network .fetch-deps # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Thu, 05 Dec 2024 20:29:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Dec 2024 20:29:40 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:2ed16bdf68dac880df118dfa3d21d44652bc18382729359f97297fa5998086cd`  
		Last Modified: Tue, 07 Jan 2025 02:32:49 GMT  
		Size: 3.5 MB (3459179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcacb882a5db1e743c34cc92815e2f3aab3e188ee2522e3208a1ed1657316319`  
		Last Modified: Tue, 07 Jan 2025 04:04:30 GMT  
		Size: 3.5 MB (3485610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:271c95db3928cf5b057875d0344bcbb766164738b63d3ec9f076fd1b10abd46e`  
		Last Modified: Tue, 07 Jan 2025 04:04:30 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17161d12eebb02d227b9e5af0a2feca4cb2817d393db01e188518657f245ce3`  
		Last Modified: Tue, 07 Jan 2025 04:04:30 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5838456b31fdb3e01a5b5d2ed57af0629a238779cce167887e1e59c9d563f43a`  
		Last Modified: Tue, 07 Jan 2025 05:32:56 GMT  
		Size: 12.2 MB (12172068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54fb97bdeee2a69d42254a35facf30a79ca7a580b86de44d0a46c10b845ad6c7`  
		Last Modified: Tue, 07 Jan 2025 05:32:56 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04f49a22f791afaa3ea1ee73f9b50836a2bf3a71b54ff5e8d33b52d75515671`  
		Last Modified: Tue, 07 Jan 2025 05:36:29 GMT  
		Size: 12.8 MB (12847735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68664a74b1a558d1b8fb7a674597c47a5d4615a7ee5b5d61b479dc919e0d384d`  
		Last Modified: Tue, 07 Jan 2025 05:36:28 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c1dfb1d076594397b2e077f03007c1bbbf574bf295ce1009bd2bdddb120ae0`  
		Last Modified: Tue, 07 Jan 2025 05:36:28 GMT  
		Size: 19.2 KB (19214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69a62d00513e6ff435b45e75de6c3d207ad34ad9ef9b8778a8b6291d74cae62a`  
		Last Modified: Tue, 07 Jan 2025 05:36:28 GMT  
		Size: 9.2 KB (9183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21eb9557139b46081aa218e2c788b9c46b168f0df4cdae37d61cdcc5c79a9b65`  
		Last Modified: Tue, 07 Jan 2025 16:45:01 GMT  
		Size: 46.1 MB (46128676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69314498fda68b3719a403dc0af98fe802b467de7a381b75e4feb5b5442ec715`  
		Last Modified: Tue, 07 Jan 2025 16:45:02 GMT  
		Size: 7.2 MB (7154278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd37d29a265902acb7017fa8c64f1a609233355ed211997ce4e17fc201cb2dc`  
		Last Modified: Tue, 07 Jan 2025 16:45:01 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a45ed8d8fec13f6f9b3c6025f04cff064411ba32963d47a4c992c570250738ee`  
		Last Modified: Tue, 07 Jan 2025 16:48:28 GMT  
		Size: 225.2 MB (225234115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d35feef88d837023238c736895d6c6b786c72b4c1cdde8d02dbae9762d1c3d`  
		Last Modified: Tue, 07 Jan 2025 16:48:19 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43014d576d37fff836011644a5216bcc65641a9177436f13ea5782627eca9f25`  
		Last Modified: Tue, 07 Jan 2025 16:48:19 GMT  
		Size: 2.3 KB (2339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:29-fpm-alpine` - unknown; unknown

```console
$ docker pull nextcloud@sha256:c3706e351369e90dc4f27aac56c5f601c584ab61fd7f2c5fe8d4be3ea3e80fc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 KB (42106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ac36c2a084f649e03d2229d80ce3ea98e69eb2998e9433a9e0b59f7317bd761`

```dockerfile
```

-	Layers:
	-	`sha256:642d60ad4eb0299daa1adb8a439eee4a32e1ef2e0eb1441f283dd82546f80995`  
		Last Modified: Tue, 07 Jan 2025 16:48:19 GMT  
		Size: 42.1 KB (42106 bytes)  
		MIME: application/vnd.in-toto+json
