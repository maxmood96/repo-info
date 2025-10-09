## `nextcloud:production-fpm-alpine`

```console
$ docker pull nextcloud@sha256:f4f454c4ed59a4dc379e09c6f202c5c0c41cb37e4dec07e8308be2e641d06283
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

### `nextcloud:production-fpm-alpine` - linux; amd64

```console
$ docker pull nextcloud@sha256:4eff6e45fa0452e407050b40c66188dbc37b8e51cd1f4afb3afe8b378c92c41d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.9 MB (336930853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ebd9d593efa6cf768914bb25e148785544eedb56755c2e0728eac127ae3c9d8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 25 Sep 2025 23:53:24 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 25 Sep 2025 23:53:24 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_VERSION=8.3.26
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 25 Sep 2025 23:53:24 GMT
WORKDIR /var/www/html
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
STOPSIGNAL SIGQUIT
# Thu, 25 Sep 2025 23:53:24 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 25 Sep 2025 23:53:24 GMT
CMD ["php-fpm"]
# Fri, 26 Sep 2025 01:22:24 GMT
RUN set -ex;         apk add --no-cache         imagemagick         imagemagick-pdf         imagemagick-jpeg         imagemagick-raw         imagemagick-tiff         imagemagick-heic         imagemagick-webp         imagemagick-svg         rsync     ;         rm /var/spool/cron/crontabs/root;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Fri, 26 Sep 2025 01:22:24 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         autoconf         freetype-dev         gmp-dev         icu-dev         imagemagick-dev         libevent-dev         libjpeg-turbo-dev         libmemcached-dev         libpng-dev         libwebp-dev         libxml2-dev         libzip-dev         openldap-dev         pcre-dev         postgresql-dev     ;         docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap;     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.27;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.0;     pecl install memcached-3.3.0         --configureoptions 'enable-memcached-igbinary="yes"';     pecl install redis-6.2.0         --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"';         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .nextcloud-phpext-rundeps $runDeps;     apk del --no-network .build-deps # buildkit
# Fri, 26 Sep 2025 01:22:24 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 26 Sep 2025 01:22:24 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 26 Sep 2025 01:22:24 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Fri, 26 Sep 2025 01:22:24 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Fri, 26 Sep 2025 01:22:24 GMT
VOLUME [/var/www/html]
# Fri, 26 Sep 2025 01:22:24 GMT
ENV NEXTCLOUD_VERSION=31.0.9
# Fri, 26 Sep 2025 01:22:24 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-31.0.9.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-31.0.9.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com  --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;     apk del --no-network .fetch-deps # buildkit
# Fri, 26 Sep 2025 01:22:24 GMT
COPY *.sh upgrade.exclude / # buildkit
# Fri, 26 Sep 2025 01:22:24 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Fri, 26 Sep 2025 01:22:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 01:22:24 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a9e9f1584554daa5c541ea366aad608354f0127715dd54018728e65c805318`  
		Last Modified: Fri, 26 Sep 2025 21:49:56 GMT  
		Size: 5.9 MB (5928428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364c3e15727b227a313b0cf9a7594c60c0c787bdc4b2a46c7b9b12eccce1b52c`  
		Last Modified: Fri, 26 Sep 2025 21:49:56 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c174eff561d097b7c68cf1ee3db486e96a4ce6d4fa093a8e16f12dc3a9d4dfd3`  
		Last Modified: Fri, 26 Sep 2025 21:49:56 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8d0864a7668e879cbe839a77a1598ec7d22462e59b944e137827732dd75b93`  
		Last Modified: Fri, 26 Sep 2025 21:49:57 GMT  
		Size: 12.6 MB (12601921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1050b3c5bacb55fc1cf9b4c63bf18e6e575dce2fa50f7f71a1201063ce2a110`  
		Last Modified: Fri, 26 Sep 2025 21:49:56 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e7158ee9caabe6fa9b9612be5593c3a661358b1fd55a1f1f3bf75b053809b22`  
		Last Modified: Fri, 26 Sep 2025 21:49:57 GMT  
		Size: 13.3 MB (13268285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abfcd651048c1e01cb72ec229d8fa3b3d6e60f4db58548b232be53e1f0141bea`  
		Last Modified: Fri, 26 Sep 2025 21:49:57 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61659f47e179108746d5845c44a56830802448b74f660f6587046f3f2542a823`  
		Last Modified: Fri, 26 Sep 2025 21:49:57 GMT  
		Size: 20.0 KB (19953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10028bd4c3fd3a01dd6cd261bb98ff9cad3225f2726454d56491336781cda4c5`  
		Last Modified: Fri, 26 Sep 2025 21:49:57 GMT  
		Size: 20.0 KB (19954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7f3d3ae7710ab18d1e40b373a021df2bad8bb989b7382fa6550d2c3f73a72f7`  
		Last Modified: Fri, 26 Sep 2025 21:49:57 GMT  
		Size: 9.2 KB (9176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d385429fe46446b0dc9bbac2567ad7c459fbe3389af4a3f4dd26d3041b39295`  
		Last Modified: Fri, 26 Sep 2025 22:17:02 GMT  
		Size: 44.5 MB (44527449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd787ad639bbdeceec82f3b3ab3a5156f3e1518dd09b17d621396dbfa9ad3c2`  
		Last Modified: Fri, 26 Sep 2025 22:16:59 GMT  
		Size: 7.3 MB (7287918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c25d764c70c5bf78512f7a033398042760c94022b6f4d2654835285c871b46`  
		Last Modified: Fri, 26 Sep 2025 22:16:58 GMT  
		Size: 785.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e9b43c54b9a8ec1881432f0525d0684a763d5373b334f696aaad77de1f6b0da`  
		Last Modified: Fri, 26 Sep 2025 22:50:42 GMT  
		Size: 249.5 MB (249456769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb72070515a262610d29fa3b4582cba54090696c7660557ad7763bb523b1bf1`  
		Last Modified: Fri, 26 Sep 2025 22:16:59 GMT  
		Size: 4.0 KB (4047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a261823adb300db7515b0c3b4395748b08de1d3471fc1468bfa8c1236d215904`  
		Last Modified: Fri, 26 Sep 2025 22:16:59 GMT  
		Size: 2.4 KB (2358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:production-fpm-alpine` - unknown; unknown

```console
$ docker pull nextcloud@sha256:d3b0586aba4472a1fd5048e448bed972c8c2a84a077412893310ea55fc984d8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 KB (45483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4709e33f82fc1f614a29feeb771e7ddd4e9e6d0cb75bafc114ab13c82c873819`

```dockerfile
```

-	Layers:
	-	`sha256:e631fd991ab6e5e705f669b092e68aa262bb0294575e633ba51d18f3b2415108`  
		Last Modified: Fri, 26 Sep 2025 23:52:21 GMT  
		Size: 45.5 KB (45483 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:production-fpm-alpine` - linux; arm variant v6

```console
$ docker pull nextcloud@sha256:4e2637847d1aeb62fe04b6c7b7df44bd1251302df2a126f07d3ae6055cf1aa29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.0 MB (325983221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af8e6907fbb4ad76e6f734019516d388f20f110d717043ff33d945801c01cc2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 25 Sep 2025 23:53:24 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
CMD ["/bin/sh"]
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 25 Sep 2025 23:53:24 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 25 Sep 2025 23:53:24 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_VERSION=8.3.26
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 25 Sep 2025 23:53:24 GMT
WORKDIR /var/www/html
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
STOPSIGNAL SIGQUIT
# Thu, 25 Sep 2025 23:53:24 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 25 Sep 2025 23:53:24 GMT
CMD ["php-fpm"]
# Fri, 26 Sep 2025 01:22:24 GMT
RUN set -ex;         apk add --no-cache         imagemagick         imagemagick-pdf         imagemagick-jpeg         imagemagick-raw         imagemagick-tiff         imagemagick-heic         imagemagick-webp         imagemagick-svg         rsync     ;         rm /var/spool/cron/crontabs/root;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Fri, 26 Sep 2025 01:22:24 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         autoconf         freetype-dev         gmp-dev         icu-dev         imagemagick-dev         libevent-dev         libjpeg-turbo-dev         libmemcached-dev         libpng-dev         libwebp-dev         libxml2-dev         libzip-dev         openldap-dev         pcre-dev         postgresql-dev     ;         docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap;     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.27;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.0;     pecl install memcached-3.3.0         --configureoptions 'enable-memcached-igbinary="yes"';     pecl install redis-6.2.0         --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"';         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .nextcloud-phpext-rundeps $runDeps;     apk del --no-network .build-deps # buildkit
# Fri, 26 Sep 2025 01:22:24 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 26 Sep 2025 01:22:24 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 26 Sep 2025 01:22:24 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Fri, 26 Sep 2025 01:22:24 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Fri, 26 Sep 2025 01:22:24 GMT
VOLUME [/var/www/html]
# Fri, 26 Sep 2025 01:22:24 GMT
ENV NEXTCLOUD_VERSION=31.0.9
# Fri, 26 Sep 2025 01:22:24 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-31.0.9.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-31.0.9.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com  --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;     apk del --no-network .fetch-deps # buildkit
# Fri, 26 Sep 2025 01:22:24 GMT
COPY *.sh upgrade.exclude / # buildkit
# Fri, 26 Sep 2025 01:22:24 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Fri, 26 Sep 2025 01:22:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 01:22:24 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3cdcb39afd821d13b22ca21c865ff19e58569c683f9e18b9a0ceb95c92b680`  
		Last Modified: Wed, 08 Oct 2025 21:46:05 GMT  
		Size: 3.4 MB (3428334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b8740db6975c9b8c5220191ade53612421b7da5301d9f3f7da94286205eb5ec`  
		Last Modified: Wed, 08 Oct 2025 21:46:04 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc4035a2fd0c27d5270cc96e2d8cfb3e6e50f6a5677241510df3134795ece31`  
		Last Modified: Wed, 08 Oct 2025 21:46:04 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9643c46440d442a3ea77f7680b646ca563c09924e3893a139f0fae39b0fe17b2`  
		Last Modified: Wed, 08 Oct 2025 21:52:36 GMT  
		Size: 12.6 MB (12602017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343fd232e2ed6ec2be8585a876afb24be002ab0ca52eaaffe0602b53ec99008a`  
		Last Modified: Wed, 08 Oct 2025 21:52:34 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7ebc2b7684c32e73e8386b551f89d6b67b81d3ea7bba27fdefd855628b0525`  
		Last Modified: Wed, 08 Oct 2025 21:52:35 GMT  
		Size: 12.0 MB (11983688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f744d5bcb115c5143f8a956a038bd848a40c6c1cba3a35da7cc19e2df4f1e9`  
		Last Modified: Wed, 08 Oct 2025 21:52:34 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b77520ca9455202004fbf3faf0048cd387a9893e8ec1d93699b3b2c83c6b93f`  
		Last Modified: Wed, 08 Oct 2025 21:52:34 GMT  
		Size: 19.9 KB (19866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf4961f2b4ef141575ff94a1fe99d95871bd0975125a7075a4e23109130d18e`  
		Last Modified: Wed, 08 Oct 2025 21:52:34 GMT  
		Size: 19.9 KB (19863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5c84b4f3a4d7577bc1b755f1ebdbecf63cf09fc3dc54d97d3e2803e4a736af`  
		Last Modified: Wed, 08 Oct 2025 21:52:34 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccafabf8448ffb96e53a06785d53915e86e626728d50270c28a4ff8119386500`  
		Last Modified: Wed, 08 Oct 2025 23:11:15 GMT  
		Size: 38.0 MB (37979373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a91c7b1a043d5e3a6a5b7805db5ffba0788fd5241127b7565bd985e9379c93`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 7.0 MB (6968435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3378e76c17b3d72426277f2e503e9d0260482992dbbddb18170545966f2f4eec`  
		Last Modified: Wed, 08 Oct 2025 23:11:06 GMT  
		Size: 785.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6102e7673f60e1cbfd6f1e1d2148f073a4dd774bc287309b20f18321105cbe47`  
		Last Modified: Wed, 08 Oct 2025 23:52:39 GMT  
		Size: 249.5 MB (249457076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70fa790629a3e2455967de091708fb8323f1ec915ba37fadc497cbda64d4172b`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 4.0 KB (4047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02fd419abe5a2842e3a86e1b0eda312bd38b959f93cc6603d473a09b5e3e443f`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 2.4 KB (2353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:production-fpm-alpine` - unknown; unknown

```console
$ docker pull nextcloud@sha256:13e966143c0958e3dae5b30254679362c699039d9ee720e7db7ba1df7f6077f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 KB (45299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f485b87e70131f73519c3ec3fc102a9be9f96d074b0ed76832d3dd5caa2e42cf`

```dockerfile
```

-	Layers:
	-	`sha256:7ef41eb9f77c1e66eb510e4a987f283fed37a7df2c4ca299f9722689ad0df13d`  
		Last Modified: Wed, 08 Oct 2025 23:50:21 GMT  
		Size: 45.3 KB (45299 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:production-fpm-alpine` - linux; arm variant v7

```console
$ docker pull nextcloud@sha256:df3346995668c9bf7de1231ef922e7392ab73131745018ee88b347c0bdbf274c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.2 MB (324184380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f817bca68717685fe14e07b06fe935c4269e90b60daccb8444875b2da86c17e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 25 Sep 2025 23:53:24 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
CMD ["/bin/sh"]
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 25 Sep 2025 23:53:24 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 25 Sep 2025 23:53:24 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_VERSION=8.3.26
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 25 Sep 2025 23:53:24 GMT
WORKDIR /var/www/html
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
STOPSIGNAL SIGQUIT
# Thu, 25 Sep 2025 23:53:24 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 25 Sep 2025 23:53:24 GMT
CMD ["php-fpm"]
# Fri, 26 Sep 2025 01:22:24 GMT
RUN set -ex;         apk add --no-cache         imagemagick         imagemagick-pdf         imagemagick-jpeg         imagemagick-raw         imagemagick-tiff         imagemagick-heic         imagemagick-webp         imagemagick-svg         rsync     ;         rm /var/spool/cron/crontabs/root;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Fri, 26 Sep 2025 01:22:24 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         autoconf         freetype-dev         gmp-dev         icu-dev         imagemagick-dev         libevent-dev         libjpeg-turbo-dev         libmemcached-dev         libpng-dev         libwebp-dev         libxml2-dev         libzip-dev         openldap-dev         pcre-dev         postgresql-dev     ;         docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap;     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.27;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.0;     pecl install memcached-3.3.0         --configureoptions 'enable-memcached-igbinary="yes"';     pecl install redis-6.2.0         --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"';         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .nextcloud-phpext-rundeps $runDeps;     apk del --no-network .build-deps # buildkit
# Fri, 26 Sep 2025 01:22:24 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 26 Sep 2025 01:22:24 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 26 Sep 2025 01:22:24 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Fri, 26 Sep 2025 01:22:24 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Fri, 26 Sep 2025 01:22:24 GMT
VOLUME [/var/www/html]
# Fri, 26 Sep 2025 01:22:24 GMT
ENV NEXTCLOUD_VERSION=31.0.9
# Fri, 26 Sep 2025 01:22:24 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-31.0.9.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-31.0.9.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com  --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;     apk del --no-network .fetch-deps # buildkit
# Fri, 26 Sep 2025 01:22:24 GMT
COPY *.sh upgrade.exclude / # buildkit
# Fri, 26 Sep 2025 01:22:24 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Fri, 26 Sep 2025 01:22:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 01:22:24 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3cd31953efba831f10d0cb18b5b3ad75edf03f314e7bbe38c1aca633e797fb`  
		Last Modified: Wed, 08 Oct 2025 21:53:31 GMT  
		Size: 3.2 MB (3244402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076b71c74c2ecafb3a798b10fd0c6397ad7786a6849c4856db6dd514a2c975c4`  
		Last Modified: Wed, 08 Oct 2025 21:53:31 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c7f53a180a3a248d39673c498c7ab85a1a6d5183694c33d3038f736b071339`  
		Last Modified: Wed, 08 Oct 2025 21:53:31 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3ae452ce63af9658d481ffccc2ad1c744f0e444c5aba07d691b2bdbb9dce03`  
		Last Modified: Wed, 08 Oct 2025 21:53:32 GMT  
		Size: 12.6 MB (12602014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaafbcc1dbfaa222ffc2a08f1c645d03c40816a9ad7154fe580dc4f88638f2d3`  
		Last Modified: Wed, 08 Oct 2025 21:53:31 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:469404dd41d3961db5905a469aba22f0ca5a2b50cc4ef6f27a787fd8969b7299`  
		Last Modified: Wed, 08 Oct 2025 21:53:31 GMT  
		Size: 11.3 MB (11290087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a611eba00f6c7e0ca133eac77c4d2469a32de3c937f62d6604ff7616b2fd03b8`  
		Last Modified: Wed, 08 Oct 2025 21:53:31 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4946eff1c882514c3fb48260ba445a5ea3166606dd48c64255490e71b4da599`  
		Last Modified: Wed, 08 Oct 2025 21:53:30 GMT  
		Size: 19.9 KB (19854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800d7396291b673444e3f1ca3abee6e42f50100bbafedb89359d1bbe624fe1ef`  
		Last Modified: Wed, 08 Oct 2025 21:53:31 GMT  
		Size: 19.8 KB (19847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b9da2b8b4bf4b148499be92fb2365fb19dd97a47810a0c299a0d23f148cf37b`  
		Last Modified: Wed, 08 Oct 2025 21:53:31 GMT  
		Size: 9.2 KB (9185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:048e0262f4a0c642c2f86da7b085cdf56b61cb98a87444350e446819c50d3c8d`  
		Last Modified: Wed, 08 Oct 2025 23:26:11 GMT  
		Size: 36.9 MB (36905958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30391454e87a31112b40431f7991566c6c57fc60c0ff2958df9d61dfa5647b8d`  
		Last Modified: Wed, 08 Oct 2025 23:26:10 GMT  
		Size: 7.4 MB (7403312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41fb7a712e40878eb4868cc5b69eca71f4a5f4e7d2c39c19beba704dad64b2c5`  
		Last Modified: Wed, 08 Oct 2025 23:26:08 GMT  
		Size: 788.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b0d5f09ae5244bd2b6b44fd5093589d9ea9f9667603879bea016ecfd96b0b4`  
		Last Modified: Wed, 08 Oct 2025 23:50:55 GMT  
		Size: 249.5 MB (249456859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de9b4b7377f71c73dc3be3c683032f40185a5fb60ee567031b7fa014222d742c`  
		Last Modified: Wed, 08 Oct 2025 23:26:08 GMT  
		Size: 4.0 KB (4047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5deb48955c20483b55dc123ca690de90bdb229a0833035bcc85a26dc474a0cd4`  
		Last Modified: Wed, 08 Oct 2025 23:26:08 GMT  
		Size: 2.4 KB (2355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:production-fpm-alpine` - unknown; unknown

```console
$ docker pull nextcloud@sha256:c81358119fbadfca152d3579983a43a04ed01b305fd9375495c89530a35b804f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 KB (45296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc7837d1879ca126ac9a4ea1674f5058960b075672eb10e79c6ded45768945a`

```dockerfile
```

-	Layers:
	-	`sha256:799d7fff30766961f5686770d88e73313592bfa4d2814a48622d265e516107f9`  
		Last Modified: Wed, 08 Oct 2025 23:50:23 GMT  
		Size: 45.3 KB (45296 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:production-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull nextcloud@sha256:6f03ccd53635e881767db0d1c259fdebb305b6038f06901e9d4bed3e15f22019
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.8 MB (334761382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4b82f818ed2a33ccaae859cd34c42b26b2fd89894abd29ae3c08b338b0ba7e9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 25 Sep 2025 23:53:24 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
CMD ["/bin/sh"]
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 25 Sep 2025 23:53:24 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 25 Sep 2025 23:53:24 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_VERSION=8.3.26
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 25 Sep 2025 23:53:24 GMT
WORKDIR /var/www/html
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
STOPSIGNAL SIGQUIT
# Thu, 25 Sep 2025 23:53:24 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 25 Sep 2025 23:53:24 GMT
CMD ["php-fpm"]
# Fri, 26 Sep 2025 01:22:24 GMT
RUN set -ex;         apk add --no-cache         imagemagick         imagemagick-pdf         imagemagick-jpeg         imagemagick-raw         imagemagick-tiff         imagemagick-heic         imagemagick-webp         imagemagick-svg         rsync     ;         rm /var/spool/cron/crontabs/root;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Fri, 26 Sep 2025 01:22:24 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         autoconf         freetype-dev         gmp-dev         icu-dev         imagemagick-dev         libevent-dev         libjpeg-turbo-dev         libmemcached-dev         libpng-dev         libwebp-dev         libxml2-dev         libzip-dev         openldap-dev         pcre-dev         postgresql-dev     ;         docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap;     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.27;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.0;     pecl install memcached-3.3.0         --configureoptions 'enable-memcached-igbinary="yes"';     pecl install redis-6.2.0         --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"';         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .nextcloud-phpext-rundeps $runDeps;     apk del --no-network .build-deps # buildkit
# Fri, 26 Sep 2025 01:22:24 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 26 Sep 2025 01:22:24 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 26 Sep 2025 01:22:24 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Fri, 26 Sep 2025 01:22:24 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Fri, 26 Sep 2025 01:22:24 GMT
VOLUME [/var/www/html]
# Fri, 26 Sep 2025 01:22:24 GMT
ENV NEXTCLOUD_VERSION=31.0.9
# Fri, 26 Sep 2025 01:22:24 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-31.0.9.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-31.0.9.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com  --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;     apk del --no-network .fetch-deps # buildkit
# Fri, 26 Sep 2025 01:22:24 GMT
COPY *.sh upgrade.exclude / # buildkit
# Fri, 26 Sep 2025 01:22:24 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Fri, 26 Sep 2025 01:22:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 01:22:24 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa3e41c2bec91c6a90481f49cd9f7a03a7d1dbd5d60ce7c5743431e60b7d710`  
		Last Modified: Wed, 08 Oct 2025 21:38:06 GMT  
		Size: 3.5 MB (3466806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b621ccd53774b77e761ded3f6cfa38a6c70de2968d763a229a32620219f1de9`  
		Last Modified: Wed, 08 Oct 2025 21:38:05 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9695a5b19f8045abdfdfdba80a7cb2d67c597ce00657b1b8914af7122d3ff6f`  
		Last Modified: Wed, 08 Oct 2025 21:38:06 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ebb674d348d7bbc3a447314380a4eb2158b7cd2e4f9bbed10e0b9ce37af4e83`  
		Last Modified: Wed, 08 Oct 2025 21:38:08 GMT  
		Size: 12.6 MB (12602011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:736ac14f3ae9d84197d99b5d9ded705973d83185f0d582651f07ae3bd6dbe5ff`  
		Last Modified: Wed, 08 Oct 2025 21:38:06 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf54de2111690e343d01da97a959c419582524f4f27a6284397fc4a5f59dcb59`  
		Last Modified: Wed, 08 Oct 2025 21:38:07 GMT  
		Size: 13.3 MB (13252360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a18f9f6d12709e6de4dd76cdb1d4becef27de271aa590b300b3bbff216238a`  
		Last Modified: Wed, 08 Oct 2025 21:38:06 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7ed75515c438605782fbe38189fc3ae4dc33c1571cc0e21a0037a8d15eb5661`  
		Last Modified: Wed, 08 Oct 2025 21:38:06 GMT  
		Size: 19.9 KB (19864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd0980473342d6525da82928bbf700163f81885d0f9f1cf04017cc39fffc376`  
		Last Modified: Wed, 08 Oct 2025 21:38:06 GMT  
		Size: 19.9 KB (19852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50cbe33dd0bd206a9b0e87239de20bf7735c0fe353b7765455c3a606f2323ed1`  
		Last Modified: Wed, 08 Oct 2025 21:38:06 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c8f4a99a48f96e21406048cb7b7c9198442e2ae99a929d3a0db3d48d3d99b3`  
		Last Modified: Wed, 08 Oct 2025 23:24:47 GMT  
		Size: 44.6 MB (44582265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:861ce5e0092a174fd8f1d37dea6a59a1e23cd25108f11a1bf28c4b6edbab2960`  
		Last Modified: Wed, 08 Oct 2025 23:24:40 GMT  
		Size: 7.2 MB (7202733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86f7abb6ca4e5bf8b8b9a5ebe47ba9bd358fca3ab345c479a4df631777027ec`  
		Last Modified: Wed, 08 Oct 2025 23:24:41 GMT  
		Size: 785.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955de37e6f8423dabdfb825a509c14c33b6608c6a3f53bed4d6bb5700bbde312`  
		Last Modified: Wed, 08 Oct 2025 23:25:21 GMT  
		Size: 249.5 MB (249456935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8febfc12fdeba4c2015e4ddba8547e881a76e4a5cb4be51928cf5cb5c8fe80f`  
		Last Modified: Wed, 08 Oct 2025 23:24:39 GMT  
		Size: 4.0 KB (4047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c49b86c66b2b56b900679a5c72de4c57c3a14dfb1addb259a4fe2dc5be3fc27d`  
		Last Modified: Wed, 08 Oct 2025 23:24:45 GMT  
		Size: 2.4 KB (2355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:production-fpm-alpine` - unknown; unknown

```console
$ docker pull nextcloud@sha256:ff9cd612db7b71ad1d6fca4b237e43cff921f933cf59978e3b09fb18ead95d24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 KB (45333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc6715c1caf645146ef834befd340fdc593f3211e5714aae116f895617a7400e`

```dockerfile
```

-	Layers:
	-	`sha256:63bd05069da603fd391bb04856649866cf72f023bc0c2178f3df9d2a21d5e32d`  
		Last Modified: Wed, 08 Oct 2025 23:50:27 GMT  
		Size: 45.3 KB (45333 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:production-fpm-alpine` - linux; 386

```console
$ docker pull nextcloud@sha256:349483a90a05fd34727d43fd7aa2130e102e5736cf65ce442ae8f19b2427feeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.6 MB (332579677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a28a89dbfea034064daf34d58f2c4c1fb1b79a6235d159860c6367a7d57a9131`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 25 Sep 2025 23:53:24 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
CMD ["/bin/sh"]
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 25 Sep 2025 23:53:24 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 25 Sep 2025 23:53:24 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_VERSION=8.3.26
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 25 Sep 2025 23:53:24 GMT
WORKDIR /var/www/html
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
STOPSIGNAL SIGQUIT
# Thu, 25 Sep 2025 23:53:24 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 25 Sep 2025 23:53:24 GMT
CMD ["php-fpm"]
# Fri, 26 Sep 2025 01:22:24 GMT
RUN set -ex;         apk add --no-cache         imagemagick         imagemagick-pdf         imagemagick-jpeg         imagemagick-raw         imagemagick-tiff         imagemagick-heic         imagemagick-webp         imagemagick-svg         rsync     ;         rm /var/spool/cron/crontabs/root;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Fri, 26 Sep 2025 01:22:24 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         autoconf         freetype-dev         gmp-dev         icu-dev         imagemagick-dev         libevent-dev         libjpeg-turbo-dev         libmemcached-dev         libpng-dev         libwebp-dev         libxml2-dev         libzip-dev         openldap-dev         pcre-dev         postgresql-dev     ;         docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap;     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.27;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.0;     pecl install memcached-3.3.0         --configureoptions 'enable-memcached-igbinary="yes"';     pecl install redis-6.2.0         --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"';         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .nextcloud-phpext-rundeps $runDeps;     apk del --no-network .build-deps # buildkit
# Fri, 26 Sep 2025 01:22:24 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 26 Sep 2025 01:22:24 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 26 Sep 2025 01:22:24 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Fri, 26 Sep 2025 01:22:24 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Fri, 26 Sep 2025 01:22:24 GMT
VOLUME [/var/www/html]
# Fri, 26 Sep 2025 01:22:24 GMT
ENV NEXTCLOUD_VERSION=31.0.9
# Fri, 26 Sep 2025 01:22:24 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-31.0.9.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-31.0.9.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com  --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;     apk del --no-network .fetch-deps # buildkit
# Fri, 26 Sep 2025 01:22:24 GMT
COPY *.sh upgrade.exclude / # buildkit
# Fri, 26 Sep 2025 01:22:24 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Fri, 26 Sep 2025 01:22:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 01:22:24 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc44e12fbc69b1f156d8436eec520233e385936119e6e0a134082ff123e16b8`  
		Last Modified: Wed, 08 Oct 2025 21:29:27 GMT  
		Size: 3.5 MB (3522953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d58ed34924355103745542522524dcc6e0fbe84c3aeb4514d964f5f13593de`  
		Last Modified: Wed, 08 Oct 2025 21:29:28 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834a1d273fe98862d2876a4b50f8329c53bc213ac93598ead0a75cdeb2e0141f`  
		Last Modified: Wed, 08 Oct 2025 21:29:27 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2c0e8a295ce017176da8f2dd0b22b2e9ad62dbade4a4899661a219fc0fb8f7`  
		Last Modified: Wed, 08 Oct 2025 22:18:01 GMT  
		Size: 12.6 MB (12601992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ebff2d2e144484dbc07c92fda4ab6b679d071f3bb77c3d0efd1b8064c5bb24`  
		Last Modified: Wed, 08 Oct 2025 22:17:59 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d028b32894ac2aab87c098c7e23a0f05f3e95aec43114ccf54a21aa366535d8a`  
		Last Modified: Wed, 08 Oct 2025 22:18:01 GMT  
		Size: 13.6 MB (13577998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10aec0f569c9e4902cbf9d66e166dcbbbfe6b61419999b211d219048a93e2c4`  
		Last Modified: Wed, 08 Oct 2025 22:17:57 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5db0495d5a7730774dcb84ad77c626fb2287541938cc40337778b70420e1aef`  
		Last Modified: Wed, 08 Oct 2025 22:17:57 GMT  
		Size: 20.1 KB (20053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aedb159c872f256a2a413e338389f972e446f639c2f297b2ae2d6b0fa13c630`  
		Last Modified: Wed, 08 Oct 2025 22:17:58 GMT  
		Size: 20.0 KB (20047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e55aa185dcebdee08ebd308c270df822db903158cf3dfedb10187179fd12f7f`  
		Last Modified: Wed, 08 Oct 2025 22:17:57 GMT  
		Size: 9.2 KB (9176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b143464bc657d0835317c36b914fca0f8e9798a8bb7390e9c8b666c2d72371b`  
		Last Modified: Wed, 08 Oct 2025 22:27:34 GMT  
		Size: 42.4 MB (42361743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e931b69a6810c93a386b9d6eb5a3bbb0fb28a449ae0b19568c84e9d0e179ee9`  
		Last Modified: Wed, 08 Oct 2025 22:27:32 GMT  
		Size: 7.4 MB (7378809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b00fd8e8d4f68ce0d918af68f2ac66aca8b0eef093d9d4cd97e192ceb39958a4`  
		Last Modified: Wed, 08 Oct 2025 22:27:31 GMT  
		Size: 789.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff39f18174b306c17c4b95e00b61c5a8f6b231b598b18d7c023f129e6e00134`  
		Last Modified: Wed, 08 Oct 2025 23:50:53 GMT  
		Size: 249.5 MB (249456670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caec4de15b57682593330836c83cd0f544726ea85e3ce42070920a78a66393e7`  
		Last Modified: Wed, 08 Oct 2025 22:27:32 GMT  
		Size: 4.0 KB (4047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd545f4643aeb292f163126b982596fc1ca0c3ba81e603147cb1fa1cfa18612f`  
		Last Modified: Wed, 08 Oct 2025 22:27:32 GMT  
		Size: 2.3 KB (2349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:production-fpm-alpine` - unknown; unknown

```console
$ docker pull nextcloud@sha256:c8a92b9293138df5cc8a8daef163d768f51587e43c30c0599e16a65598147b7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 KB (45128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d826da06dd7ef2275fe1b889ff7154b2814e82444221b0a3775617e381aba82`

```dockerfile
```

-	Layers:
	-	`sha256:9716ea6ced5e458263ebfe81ea77eb51efcb1c14adb9ddc12a00b29830acad49`  
		Last Modified: Wed, 08 Oct 2025 23:50:30 GMT  
		Size: 45.1 KB (45128 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:production-fpm-alpine` - linux; ppc64le

```console
$ docker pull nextcloud@sha256:da8d893d5e779bee34036284529e1eee90c81bf417c6663452e853f393531fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.5 MB (342543209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14d7a27bc8caf6e35eb2107daa383e4d6a2bd7da3f7eed98a3b6fe013e0fbf17`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 25 Sep 2025 23:53:24 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 25 Sep 2025 23:53:24 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_VERSION=8.3.26
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 25 Sep 2025 23:53:24 GMT
WORKDIR /var/www/html
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
STOPSIGNAL SIGQUIT
# Thu, 25 Sep 2025 23:53:24 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 25 Sep 2025 23:53:24 GMT
CMD ["php-fpm"]
# Fri, 26 Sep 2025 01:22:24 GMT
RUN set -ex;         apk add --no-cache         imagemagick         imagemagick-pdf         imagemagick-jpeg         imagemagick-raw         imagemagick-tiff         imagemagick-heic         imagemagick-webp         imagemagick-svg         rsync     ;         rm /var/spool/cron/crontabs/root;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Fri, 26 Sep 2025 01:22:24 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         autoconf         freetype-dev         gmp-dev         icu-dev         imagemagick-dev         libevent-dev         libjpeg-turbo-dev         libmemcached-dev         libpng-dev         libwebp-dev         libxml2-dev         libzip-dev         openldap-dev         pcre-dev         postgresql-dev     ;         docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap;     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.27;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.0;     pecl install memcached-3.3.0         --configureoptions 'enable-memcached-igbinary="yes"';     pecl install redis-6.2.0         --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"';         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .nextcloud-phpext-rundeps $runDeps;     apk del --no-network .build-deps # buildkit
# Fri, 26 Sep 2025 01:22:24 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 26 Sep 2025 01:22:24 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 26 Sep 2025 01:22:24 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Fri, 26 Sep 2025 01:22:24 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Fri, 26 Sep 2025 01:22:24 GMT
VOLUME [/var/www/html]
# Fri, 26 Sep 2025 01:22:24 GMT
ENV NEXTCLOUD_VERSION=31.0.9
# Fri, 26 Sep 2025 01:22:24 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-31.0.9.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-31.0.9.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com  --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;     apk del --no-network .fetch-deps # buildkit
# Fri, 26 Sep 2025 01:22:24 GMT
COPY *.sh upgrade.exclude / # buildkit
# Fri, 26 Sep 2025 01:22:24 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Fri, 26 Sep 2025 01:22:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 01:22:24 GMT
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
	-	`sha256:c21cfadffc066033bb3b2fb968e591ebbf95e2cc63d5efec774453f70aac4f9a`  
		Last Modified: Fri, 26 Sep 2025 23:11:15 GMT  
		Size: 12.6 MB (12601928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af1c9397d85dd5a6f1894ceb18b3f66da3683fde1099e158db3048f1c9f2c9b0`  
		Last Modified: Fri, 26 Sep 2025 23:11:13 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c528ca01c68b519264ffb9422fc05cc4cf69ecc76be75d9de3d0861328f7d03`  
		Last Modified: Fri, 26 Sep 2025 23:15:02 GMT  
		Size: 16.5 MB (16540679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c098ae3cc2c7e481c630a62b06a8cf24caa820873fa7698d6479982b514a3a`  
		Last Modified: Fri, 26 Sep 2025 23:15:01 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0636b77a8576201d370138b273dee1f7283d1aca90edcad0bf5bc16d592d7209`  
		Last Modified: Fri, 26 Sep 2025 23:15:01 GMT  
		Size: 19.8 KB (19751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b89f1f1582843d46bdf75334d4b96403fcca4bdccf60cecc8885da71b606ec1`  
		Last Modified: Fri, 26 Sep 2025 23:15:01 GMT  
		Size: 19.7 KB (19748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e80a103b867f5587ce107c56b44928f623693e6852631bba8921e7bbd67ca3`  
		Last Modified: Fri, 26 Sep 2025 23:15:01 GMT  
		Size: 9.2 KB (9183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac6b05e1c052d0f10c1a8942def11503ad6404a2e1616cc0db0cb783c428643c`  
		Last Modified: Sat, 27 Sep 2025 02:28:00 GMT  
		Size: 49.1 MB (49104828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e5facc65b1ba14691453c9d7faf7e598e42e1f5f3fccfe89c52bdd3e051c62`  
		Last Modified: Sat, 27 Sep 2025 02:27:57 GMT  
		Size: 7.4 MB (7441093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8103fdc7a2a63a2285359427b6bba4acbe4212bf79c5c65dd71a58d862bc4c90`  
		Last Modified: Sat, 27 Sep 2025 02:27:56 GMT  
		Size: 791.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:063ef212a60a8452c3557e2dc98cdab4fc62c95d3ef946d5760161d4732ceca7`  
		Last Modified: Sat, 27 Sep 2025 03:10:10 GMT  
		Size: 249.5 MB (249456400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cebdf3c28f714fc76b1a8c4800f0e0c54f2e0f62d8fe0777de6c43bd5e9a6fe`  
		Last Modified: Sat, 27 Sep 2025 02:27:56 GMT  
		Size: 4.0 KB (4047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db7172928958f3694ba969c30083a46abd10e389a5f7798bf165eae8e60a4d7c`  
		Last Modified: Sat, 27 Sep 2025 02:27:56 GMT  
		Size: 2.4 KB (2354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:production-fpm-alpine` - unknown; unknown

```console
$ docker pull nextcloud@sha256:fdca3dea86b022090332669dfc1b0bdee5fe6fb998615d08ad39ae6dde23de61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 KB (45546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d2161d1965b7fb51acacb7a863a520ea48300ec2113e4162ab0db454f1b057d`

```dockerfile
```

-	Layers:
	-	`sha256:ee16b3d3ce5e818be97d4b2df791d90f07be64f7b5b27d445655596121ed4b3d`  
		Last Modified: Sat, 27 Sep 2025 05:50:46 GMT  
		Size: 45.5 KB (45546 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:production-fpm-alpine` - linux; riscv64

```console
$ docker pull nextcloud@sha256:4dde59a52d45e6b8871768a2eeb9e77b60bd40fa30ca04eec36e6be8fb2e1d74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.0 MB (332967865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69cc8daaa561606e70d6eb00988188a9afe455bb50463156a53c7366dd32fb1a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 25 Sep 2025 23:53:24 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 25 Sep 2025 23:53:24 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_VERSION=8.3.26
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 25 Sep 2025 23:53:24 GMT
WORKDIR /var/www/html
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
STOPSIGNAL SIGQUIT
# Thu, 25 Sep 2025 23:53:24 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 25 Sep 2025 23:53:24 GMT
CMD ["php-fpm"]
# Fri, 26 Sep 2025 01:22:24 GMT
RUN set -ex;         apk add --no-cache         imagemagick         imagemagick-pdf         imagemagick-jpeg         imagemagick-raw         imagemagick-tiff         imagemagick-heic         imagemagick-webp         imagemagick-svg         rsync     ;         rm /var/spool/cron/crontabs/root;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Fri, 26 Sep 2025 01:22:24 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         autoconf         freetype-dev         gmp-dev         icu-dev         imagemagick-dev         libevent-dev         libjpeg-turbo-dev         libmemcached-dev         libpng-dev         libwebp-dev         libxml2-dev         libzip-dev         openldap-dev         pcre-dev         postgresql-dev     ;         docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap;     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.27;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.0;     pecl install memcached-3.3.0         --configureoptions 'enable-memcached-igbinary="yes"';     pecl install redis-6.2.0         --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"';         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .nextcloud-phpext-rundeps $runDeps;     apk del --no-network .build-deps # buildkit
# Fri, 26 Sep 2025 01:22:24 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 26 Sep 2025 01:22:24 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 26 Sep 2025 01:22:24 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Fri, 26 Sep 2025 01:22:24 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Fri, 26 Sep 2025 01:22:24 GMT
VOLUME [/var/www/html]
# Fri, 26 Sep 2025 01:22:24 GMT
ENV NEXTCLOUD_VERSION=31.0.9
# Fri, 26 Sep 2025 01:22:24 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-31.0.9.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-31.0.9.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com  --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;     apk del --no-network .fetch-deps # buildkit
# Fri, 26 Sep 2025 01:22:24 GMT
COPY *.sh upgrade.exclude / # buildkit
# Fri, 26 Sep 2025 01:22:24 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Fri, 26 Sep 2025 01:22:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 01:22:24 GMT
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
	-	`sha256:9f40758817c562000fa033f5597679b300b136bc52ac8009f321d4bba962d9b3`  
		Last Modified: Sat, 27 Sep 2025 20:34:02 GMT  
		Size: 12.6 MB (12601912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f2ef97e09374d14c7b37786bcdeeb71666fecc48c4b9067ecced783b2bf1c4d`  
		Last Modified: Sat, 27 Sep 2025 20:34:01 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bedc0a7e2cf95442e95fa793591cc5f31aaff286dbde4d8079962859a701b5c`  
		Last Modified: Sat, 27 Sep 2025 21:29:22 GMT  
		Size: 15.4 MB (15373339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56d6e53eafaf2c23a067208c3b95f7a88dca91bd132b454c95d27d12b6944991`  
		Last Modified: Sat, 27 Sep 2025 21:29:21 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f285d32a741198cec1b6611f9887f5322ef17e9ce5f2906dd925a25cb103434`  
		Last Modified: Sat, 27 Sep 2025 21:29:21 GMT  
		Size: 19.7 KB (19741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d66d9d4cb4a9ad433444fae2098bdc6cf5037aeb7c22f8cdbd6f065471e853`  
		Last Modified: Sat, 27 Sep 2025 21:29:21 GMT  
		Size: 19.7 KB (19735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d15695a95e791f746bdfd0d72e163b51f08ed4ad7ba6d07528e8c2b55dbd1fc`  
		Last Modified: Sat, 27 Sep 2025 21:29:21 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78e369d1eb75def3b4ef2b1b8e5769a6a67de469622b1b5bc5eddeac5fb1439`  
		Last Modified: Sun, 28 Sep 2025 17:58:19 GMT  
		Size: 41.3 MB (41268913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b97353d84aa35dc63c3387bdf0e94bdbd8b9e824668f9a561741b4c2fcd774`  
		Last Modified: Sun, 28 Sep 2025 17:58:16 GMT  
		Size: 7.1 MB (7099964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f99a75929077a32d81bba7bfdc669aed5b8da9d7a63c05592f2ddad016b7373`  
		Last Modified: Sun, 28 Sep 2025 17:58:15 GMT  
		Size: 788.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04825f94327f63a5ffccd57f73e1b9b42b775a5bbed39f4d6647aa92025c8130`  
		Last Modified: Sun, 28 Sep 2025 20:53:42 GMT  
		Size: 249.5 MB (249456787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e2e1ea392dabb71141ee2333a8ffe94f16f687c68b45e445e6c1274d86334cd`  
		Last Modified: Sun, 28 Sep 2025 18:33:23 GMT  
		Size: 4.0 KB (4046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20edbc7c382585971682400915a34bd80edd4c799456c7f18cf2783cfd9cd575`  
		Last Modified: Sun, 28 Sep 2025 18:33:23 GMT  
		Size: 2.4 KB (2353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:production-fpm-alpine` - unknown; unknown

```console
$ docker pull nextcloud@sha256:b1f9650cb4a285c0c18849278bb1db71ab8040be9a38bd15f87ae05927eab8a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 KB (45543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893f87c7b6dc19c7aabb0b58cd85dc376c27993d75e07f1754883cec2dc9b020`

```dockerfile
```

-	Layers:
	-	`sha256:3b344d359c1d86491c7bce599b758ec835dde01d75119e66c7ca39a9356568ec`  
		Last Modified: Sun, 28 Sep 2025 20:50:22 GMT  
		Size: 45.5 KB (45543 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:production-fpm-alpine` - linux; s390x

```console
$ docker pull nextcloud@sha256:7900ac49ce7be8983d94f1050e01e34bf6d38b36f9dbe0b3e0198a9c50defd72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.0 MB (339957846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c214183525ecf622f172e8939fde9ee849809bb48e7f1d66f86b05348a1f6e3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 25 Sep 2025 23:53:24 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 25 Sep 2025 23:53:24 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_VERSION=8.3.26
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 25 Sep 2025 23:53:24 GMT
WORKDIR /var/www/html
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
STOPSIGNAL SIGQUIT
# Thu, 25 Sep 2025 23:53:24 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 25 Sep 2025 23:53:24 GMT
CMD ["php-fpm"]
# Fri, 26 Sep 2025 01:22:24 GMT
RUN set -ex;         apk add --no-cache         imagemagick         imagemagick-pdf         imagemagick-jpeg         imagemagick-raw         imagemagick-tiff         imagemagick-heic         imagemagick-webp         imagemagick-svg         rsync     ;         rm /var/spool/cron/crontabs/root;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Fri, 26 Sep 2025 01:22:24 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         $PHPIZE_DEPS         autoconf         freetype-dev         gmp-dev         icu-dev         imagemagick-dev         libevent-dev         libjpeg-turbo-dev         libmemcached-dev         libpng-dev         libwebp-dev         libxml2-dev         libzip-dev         openldap-dev         pcre-dev         postgresql-dev     ;         docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap;     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.27;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.0;     pecl install memcached-3.3.0         --configureoptions 'enable-memcached-igbinary="yes"';     pecl install redis-6.2.0         --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"';         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .nextcloud-phpext-rundeps $runDeps;     apk del --no-network .build-deps # buildkit
# Fri, 26 Sep 2025 01:22:24 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 26 Sep 2025 01:22:24 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 26 Sep 2025 01:22:24 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Fri, 26 Sep 2025 01:22:24 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Fri, 26 Sep 2025 01:22:24 GMT
VOLUME [/var/www/html]
# Fri, 26 Sep 2025 01:22:24 GMT
ENV NEXTCLOUD_VERSION=31.0.9
# Fri, 26 Sep 2025 01:22:24 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps         bzip2         gnupg     ;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-31.0.9.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-31.0.9.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com  --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;     apk del --no-network .fetch-deps # buildkit
# Fri, 26 Sep 2025 01:22:24 GMT
COPY *.sh upgrade.exclude / # buildkit
# Fri, 26 Sep 2025 01:22:24 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Fri, 26 Sep 2025 01:22:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 01:22:24 GMT
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
	-	`sha256:2149689de406e21c39f1da3fa3d9788fda15f8300744f3cedaa8a558d9745e4c`  
		Last Modified: Sat, 27 Sep 2025 00:40:20 GMT  
		Size: 12.6 MB (12601914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17097d343a1adb55100bc03bbbdbeb0a0806e36ecbd3a26baaf26d1377d0d746`  
		Last Modified: Sat, 27 Sep 2025 00:40:18 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4835cd8742df784ee5ad33421fa12f372a4f78d63cea47cc03fb18f0157437`  
		Last Modified: Sat, 27 Sep 2025 00:44:14 GMT  
		Size: 16.0 MB (15978565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af85153c2334bfe9fcf93b974341e5b20ca36531d01db990e1b9a7629b889bfc`  
		Last Modified: Sat, 27 Sep 2025 00:44:13 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e45f0aab43e7731dc8bf87bfe21e2e61bb18edc653b39d1339d2c890c30a29`  
		Last Modified: Sat, 27 Sep 2025 00:44:13 GMT  
		Size: 19.8 KB (19751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ad6307ff0214e8fb7c417270b4ea1ff5f0678778b7518229226579eb45b736`  
		Last Modified: Sat, 27 Sep 2025 00:44:13 GMT  
		Size: 19.7 KB (19744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edabd5783f9862cf298dcd5ee3d46771273d3b06c4bb92af0c2059271805dd34`  
		Last Modified: Sat, 27 Sep 2025 00:44:13 GMT  
		Size: 9.2 KB (9176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673b935de225f124ac6ca75c9238892847e1849ee5c85ea7300b10872fbfa361`  
		Last Modified: Sat, 27 Sep 2025 03:41:22 GMT  
		Size: 47.1 MB (47143814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea90ffa33e30e71d4feb02c4a0b00bf63935b7da18e6ef02adb47cbcd315b7c`  
		Last Modified: Sat, 27 Sep 2025 03:41:18 GMT  
		Size: 7.4 MB (7392162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3957fd0683eb4f7e8f85a318de638123546dab6d1e6c31bd57f2e53f224ef8d1`  
		Last Modified: Sat, 27 Sep 2025 03:41:18 GMT  
		Size: 790.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d1559ba6513b19608371d2d6407da96a55e0901ecc26718bd4f5a591cfdc79a`  
		Last Modified: Sat, 27 Sep 2025 05:56:53 GMT  
		Size: 249.5 MB (249456579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e9fd9ddcc29e77efb3444cd30e225560a30f43c78916f3efc3f82f9301baad`  
		Last Modified: Sat, 27 Sep 2025 03:41:18 GMT  
		Size: 4.0 KB (4047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9809349d089ea3deefb9f096686d0e3b7b57bda7dcc4d532fa8d53186cdbb419`  
		Last Modified: Sat, 27 Sep 2025 03:41:18 GMT  
		Size: 2.4 KB (2354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:production-fpm-alpine` - unknown; unknown

```console
$ docker pull nextcloud@sha256:8f3beab6c8e79cce10c50d7187bacc085ca646f897afc76a5082556dcec8c30f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 KB (45484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20ac9f8ed5318f6d4c8740823cef47c9fc58516444e007c4d297aea2a8c245d8`

```dockerfile
```

-	Layers:
	-	`sha256:d4242fcb1bdc9bf77211360341217f347776e20e0bcae66b6801e4462394b32f`  
		Last Modified: Sat, 27 Sep 2025 05:50:51 GMT  
		Size: 45.5 KB (45484 bytes)  
		MIME: application/vnd.in-toto+json
