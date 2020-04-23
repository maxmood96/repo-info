## `nextcloud:17-fpm`

```console
$ docker pull nextcloud@sha256:94414da1a04451c4b39c66e6d5a4a5613536a400f85cd08357181e3c6bb7d461
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `nextcloud:17-fpm` - linux; amd64

```console
$ docker pull nextcloud@sha256:94e644f14c9923f2438a48dd72b8c655ed99e7ebfbaffd52456114b806bfe8a3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.0 MB (235974034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42c725d9118d21837911be280515b8830cb7e922dd92320fe1494ff8b275744d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 16 Apr 2020 03:22:36 GMT
ADD file:865f9041e12eb341f0a394764ddc11db49cbc8b91d4fb57c6fb1960b68b1bb41 in / 
# Thu, 16 Apr 2020 03:22:36 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 15:16:13 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 16 Apr 2020 15:16:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 16 Apr 2020 15:16:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 15:16:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 16 Apr 2020 15:16:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 16 Apr 2020 15:29:24 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Thu, 16 Apr 2020 15:29:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Apr 2020 15:29:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Apr 2020 11:37:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 17 Apr 2020 12:39:53 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Fri, 17 Apr 2020 12:39:54 GMT
ENV PHP_VERSION=7.3.17
# Fri, 17 Apr 2020 12:39:54 GMT
ENV PHP_URL=https://www.php.net/get/php-7.3.17.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.3.17.tar.xz.asc/from/this/mirror
# Fri, 17 Apr 2020 12:39:54 GMT
ENV PHP_SHA256=6a30304c27f7e7a94538f5ffec599f600ee93aedbbecad8aa4f8bec539b10ad8 PHP_MD5=
# Fri, 17 Apr 2020 12:40:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 17 Apr 2020 12:40:06 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 17 Apr 2020 12:46:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 17 Apr 2020 12:46:26 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Fri, 17 Apr 2020 12:46:27 GMT
RUN docker-php-ext-enable sodium
# Fri, 17 Apr 2020 12:46:28 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Fri, 17 Apr 2020 12:46:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 17 Apr 2020 12:46:28 GMT
WORKDIR /var/www/html
# Fri, 17 Apr 2020 12:46:29 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 17 Apr 2020 12:46:29 GMT
STOPSIGNAL SIGQUIT
# Fri, 17 Apr 2020 12:46:29 GMT
EXPOSE 9000
# Fri, 17 Apr 2020 12:46:29 GMT
CMD ["php-fpm"]
# Fri, 17 Apr 2020 16:09:00 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         busybox-static     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Fri, 17 Apr 2020 16:11:33 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libxml2-dev         libmagickwand-dev         libzip-dev         libwebp-dev         libgmp-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     if [ ! -e /usr/include/gmp.h ]; then ln -s /usr/include/$debMultiarch/gmp.h /usr/include/gmp.h; fi;    docker-php-ext-configure gd --with-freetype-dir=/usr --with-png-dir=/usr --with-jpeg-dir=/usr --with-webp-dir=/usr;     docker-php-ext-configure gmp --with-gmp="/usr/include/$debMultiarch";     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         exif         gd         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         zip         gmp     ;         pecl install APCu-5.1.18;     pecl install memcached-3.1.5;     pecl install redis-4.3.0;     pecl install imagick-3.4.4;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 17 Apr 2020 16:11:34 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 17 Apr 2020 16:11:34 GMT
VOLUME [/var/www/html]
# Fri, 17 Apr 2020 16:11:35 GMT
ENV NEXTCLOUD_VERSION=17.0.5
# Fri, 17 Apr 2020 16:12:00 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm -r "$GNUPGHOME" nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Fri, 17 Apr 2020 16:12:01 GMT
COPY multi:57de70033920dd582f0dbb812d28f0cfdcf6a102d5b4374faf9435d87a0a7585 in / 
# Mon, 20 Apr 2020 18:10:15 GMT
COPY multi:965c5cb843579fcde0cf3c9edb975639cbd2d55de5f645b1061d46855979394d in /usr/src/nextcloud/config/ 
# Mon, 20 Apr 2020 18:10:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Apr 2020 18:10:16 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:123275d6e508d282237a22fefa5aef822b719a06496444ea89efa65da523fc4b`  
		Last Modified: Thu, 16 Apr 2020 03:31:44 GMT  
		Size: 27.1 MB (27098147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7092974b7b31e1df4eea2a0dc16c923935c66865089738215d9d47c711045598`  
		Last Modified: Thu, 16 Apr 2020 17:30:22 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9112462bf4d40d5e33366d3124145a039c0f557d0a0269e614af8c1edec0b0f`  
		Last Modified: Thu, 16 Apr 2020 17:30:37 GMT  
		Size: 76.7 MB (76652064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9079bbeda63926320822bad70d04785361bd7d7246c0bcd9d8cce726f613aa59`  
		Last Modified: Thu, 16 Apr 2020 17:30:21 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328d349a2f1854b56500c6233b6c86c5b97f211663b1a33bb99c93cc3a4f4ec5`  
		Last Modified: Fri, 17 Apr 2020 15:25:38 GMT  
		Size: 12.4 MB (12437850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d99a3ca34b2652e0b998c549e4af44037946aaf9a04dcc9603437dfdac3ece`  
		Last Modified: Fri, 17 Apr 2020 15:25:37 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abc6d530b3d742ac98006a521f77b1200f0395eda330a8d688b40f9e8f1aa1ec`  
		Last Modified: Fri, 17 Apr 2020 15:25:41 GMT  
		Size: 28.8 MB (28765671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ca338b2545215e2881737e3b10495443391f345f57d7237b06915ffbeac424`  
		Last Modified: Fri, 17 Apr 2020 15:25:36 GMT  
		Size: 2.2 KB (2223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76fad38bd4587b0ebedd08110be3b2f5982bd0d91320e04aeb7eac7cea5fdf59`  
		Last Modified: Fri, 17 Apr 2020 15:25:36 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37b48a5b1cfdd824709bb75ed0b286f4746e5a6b7841f194d6568915044f5e5e`  
		Last Modified: Fri, 17 Apr 2020 15:25:36 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3918f38079bbb94357f092819d22a38d22f6cd0dc9280589cf99a9cb2e3dd6`  
		Last Modified: Fri, 17 Apr 2020 15:25:36 GMT  
		Size: 8.4 KB (8415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d21dfbde25c06e472c47ab0a1efd3c850ae8d042565bf3b484fab15fbc518127`  
		Last Modified: Fri, 17 Apr 2020 16:18:06 GMT  
		Size: 1.6 MB (1635231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ea2f03543cd234e6dac65ba9f4a7c6b8004dfee6ba7f498e0f290522ad4f0b9`  
		Last Modified: Fri, 17 Apr 2020 16:18:09 GMT  
		Size: 16.3 MB (16344051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f707cde900e8e30353cd2d1caeb573f0abd1988525bab46f054caafe1af7e78d`  
		Last Modified: Fri, 17 Apr 2020 16:18:04 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08556a7c6042f00d6b9880ca6f4affb5fc190fbcb7a6d5d2fe2deb01ef32abdc`  
		Last Modified: Fri, 17 Apr 2020 16:18:22 GMT  
		Size: 73.0 MB (73024563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c64a4eaded68847f3924c7cccb5e71cfb5125d2cb3108c159e45a52847b4341`  
		Last Modified: Fri, 17 Apr 2020 16:18:05 GMT  
		Size: 2.6 KB (2554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b01c641c847bc03eaf4d2eebd8fd47e6b94b9e2db3ad7d1b59b6fbc1510a588`  
		Last Modified: Mon, 20 Apr 2020 18:20:20 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:17-fpm` - linux; arm variant v5

```console
$ docker pull nextcloud@sha256:a5611d0f975133c492f0bc4ec836113273062dac3bdd6778b5671be4d8abbe48
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.1 MB (213051668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f960bde5e64948e2718ed49ef008ae4c50efedc5a51d16babb6925933e3200c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 23 Apr 2020 00:52:22 GMT
ADD file:62a9732be4e3237ccc896f724a34606e01f351c4877e52c9a9cd85029c06b956 in / 
# Thu, 23 Apr 2020 00:52:23 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 05:05:35 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 23 Apr 2020 05:05:36 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 23 Apr 2020 05:06:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 05:06:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 23 Apr 2020 05:06:26 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 23 Apr 2020 05:14:48 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Thu, 23 Apr 2020 05:14:50 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Apr 2020 05:14:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Apr 2020 05:14:53 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 23 Apr 2020 05:31:28 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Thu, 23 Apr 2020 05:31:29 GMT
ENV PHP_VERSION=7.3.17
# Thu, 23 Apr 2020 05:31:29 GMT
ENV PHP_URL=https://www.php.net/get/php-7.3.17.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.3.17.tar.xz.asc/from/this/mirror
# Thu, 23 Apr 2020 05:31:30 GMT
ENV PHP_SHA256=6a30304c27f7e7a94538f5ffec599f600ee93aedbbecad8aa4f8bec539b10ad8 PHP_MD5=
# Thu, 23 Apr 2020 05:31:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Apr 2020 05:31:53 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Apr 2020 05:35:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 23 Apr 2020 05:35:30 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Thu, 23 Apr 2020 05:35:32 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Apr 2020 05:35:35 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Thu, 23 Apr 2020 05:35:35 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Apr 2020 05:35:36 GMT
WORKDIR /var/www/html
# Thu, 23 Apr 2020 05:35:38 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 23 Apr 2020 05:35:39 GMT
STOPSIGNAL SIGQUIT
# Thu, 23 Apr 2020 05:35:39 GMT
EXPOSE 9000
# Thu, 23 Apr 2020 05:35:40 GMT
CMD ["php-fpm"]
# Thu, 23 Apr 2020 11:35:04 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         busybox-static     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Thu, 23 Apr 2020 11:40:28 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libxml2-dev         libmagickwand-dev         libzip-dev         libwebp-dev         libgmp-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     if [ ! -e /usr/include/gmp.h ]; then ln -s /usr/include/$debMultiarch/gmp.h /usr/include/gmp.h; fi;    docker-php-ext-configure gd --with-freetype-dir=/usr --with-png-dir=/usr --with-jpeg-dir=/usr --with-webp-dir=/usr;     docker-php-ext-configure gmp --with-gmp="/usr/include/$debMultiarch";     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         exif         gd         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         zip         gmp     ;         pecl install APCu-5.1.18;     pecl install memcached-3.1.5;     pecl install redis-4.3.0;     pecl install imagick-3.4.4;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 11:40:32 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Thu, 23 Apr 2020 11:40:33 GMT
VOLUME [/var/www/html]
# Thu, 23 Apr 2020 19:53:39 GMT
ENV NEXTCLOUD_VERSION=17.0.6
# Thu, 23 Apr 2020 19:54:51 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm -r "$GNUPGHOME" nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 19:54:54 GMT
COPY multi:57de70033920dd582f0dbb812d28f0cfdcf6a102d5b4374faf9435d87a0a7585 in / 
# Thu, 23 Apr 2020 19:54:56 GMT
COPY multi:965c5cb843579fcde0cf3c9edb975639cbd2d55de5f645b1061d46855979394d in /usr/src/nextcloud/config/ 
# Thu, 23 Apr 2020 19:54:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Apr 2020 19:54:59 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:a8c46e5952878f9f324df86c5a2b45b2e0020f6721e820981e74461d77a100dd`  
		Last Modified: Thu, 23 Apr 2020 00:59:50 GMT  
		Size: 24.8 MB (24836319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a265de7879713459cf6e6045e802665b84c49dcb7194d42e80f713168a926d4`  
		Last Modified: Thu, 23 Apr 2020 06:32:43 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:710cdb8f85f5abf4fda742431a0310421e7bd540337a4d831a04c9da4f000b2e`  
		Last Modified: Thu, 23 Apr 2020 06:33:06 GMT  
		Size: 58.8 MB (58799213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a36a8c43726552051e04d6641b87a0c8dd7104c18f21f0b0a2f06ed6d5e03377`  
		Last Modified: Thu, 23 Apr 2020 06:32:43 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e23870922b7bb1bf0ae29b7200761fe8a9d54c9fa99b2b64fcf3c9f7e97ea9`  
		Last Modified: Thu, 23 Apr 2020 06:36:42 GMT  
		Size: 12.4 MB (12436171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:795acda6cd6944b93231cd93e9a44308e48b95b10b7b04e0507dee69a34a4ce9`  
		Last Modified: Thu, 23 Apr 2020 06:36:40 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9177a890e02a5c21ff89226c3f82d7ad6be0f9ee47a6951de92924fe60be577f`  
		Last Modified: Thu, 23 Apr 2020 06:36:47 GMT  
		Size: 27.3 MB (27317086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8376063be0ea19dc13b15128f628dbeacb01ae8b210e099a387b64a284bf0525`  
		Last Modified: Thu, 23 Apr 2020 06:36:36 GMT  
		Size: 2.2 KB (2222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a95cebe111a4a35c0deaf78c8de850f45bfb171ed7526367c7681fae679ff44`  
		Last Modified: Thu, 23 Apr 2020 06:36:36 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055e74fc20fb4548028dbce874ec1ded25e10045b9e2fd587cb226d13c50ed1a`  
		Last Modified: Thu, 23 Apr 2020 06:36:36 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4706d8de96978fa1ca27aa5de308cb0cbacedb95bb05e3aaf6c7289371cf1a0b`  
		Last Modified: Thu, 23 Apr 2020 06:36:37 GMT  
		Size: 8.4 KB (8417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86cbd89d0bdf32ff3bdd2ad1c49b7a48bac1907d8f04844c6e80c849def4bf36`  
		Last Modified: Thu, 23 Apr 2020 11:58:10 GMT  
		Size: 1.6 MB (1573088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ceb0862df5717e96d6274faed94ef705186d3285a9a01ec54f6ecb4fc3944a4`  
		Last Modified: Thu, 23 Apr 2020 11:58:10 GMT  
		Size: 14.9 MB (14898531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:591969bc0da90efb1b101054ebb84712319bcf28a12fc2126807a25f2cd4d8a8`  
		Last Modified: Thu, 23 Apr 2020 11:58:07 GMT  
		Size: 535.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ad5cdff2b030751ac81320219c9226aa848e424dc4d17fe48f5c629b9e785b`  
		Last Modified: Thu, 23 Apr 2020 20:06:07 GMT  
		Size: 73.2 MB (73174715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:311b5d403bd8761e93037a29b731d0f0d36e87e21984fc6d792e8d319aabfc3c`  
		Last Modified: Thu, 23 Apr 2020 20:05:39 GMT  
		Size: 2.6 KB (2553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e497c573f50106e7476ba7fc9091a15b76008112abe92ece949f48202e835f7`  
		Last Modified: Thu, 23 Apr 2020 20:05:39 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:17-fpm` - linux; arm variant v7

```console
$ docker pull nextcloud@sha256:464a470c05f531d3fe028425063e77c71924866cc77de2c3e0ad1ef1a40f5fb4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.3 MB (209273952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c84c90504f4e66f33c8a9d6824011fee68ed90d1ac5d2f6dfc6d5e6fb8d31c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 16 Apr 2020 00:59:45 GMT
ADD file:e346a36a456d66d8019344b5f7d60df8b5b24aea1461c19838982135ad1f4d7d in / 
# Thu, 16 Apr 2020 00:59:47 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 09:52:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 16 Apr 2020 09:52:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 16 Apr 2020 09:53:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 09:53:11 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 16 Apr 2020 09:53:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 16 Apr 2020 10:01:10 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Thu, 16 Apr 2020 10:01:11 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Apr 2020 10:01:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Apr 2020 12:23:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 17 Apr 2020 12:57:26 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Fri, 17 Apr 2020 12:57:26 GMT
ENV PHP_VERSION=7.3.17
# Fri, 17 Apr 2020 12:57:27 GMT
ENV PHP_URL=https://www.php.net/get/php-7.3.17.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.3.17.tar.xz.asc/from/this/mirror
# Fri, 17 Apr 2020 12:57:28 GMT
ENV PHP_SHA256=6a30304c27f7e7a94538f5ffec599f600ee93aedbbecad8aa4f8bec539b10ad8 PHP_MD5=
# Fri, 17 Apr 2020 12:57:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 17 Apr 2020 12:57:44 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 17 Apr 2020 13:00:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 17 Apr 2020 13:00:53 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Fri, 17 Apr 2020 13:00:56 GMT
RUN docker-php-ext-enable sodium
# Fri, 17 Apr 2020 13:00:58 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Fri, 17 Apr 2020 13:00:59 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 17 Apr 2020 13:00:59 GMT
WORKDIR /var/www/html
# Fri, 17 Apr 2020 13:01:04 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 17 Apr 2020 13:01:05 GMT
STOPSIGNAL SIGQUIT
# Fri, 17 Apr 2020 13:01:07 GMT
EXPOSE 9000
# Fri, 17 Apr 2020 13:01:08 GMT
CMD ["php-fpm"]
# Fri, 17 Apr 2020 15:58:22 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         busybox-static     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Fri, 17 Apr 2020 16:02:58 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libxml2-dev         libmagickwand-dev         libzip-dev         libwebp-dev         libgmp-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     if [ ! -e /usr/include/gmp.h ]; then ln -s /usr/include/$debMultiarch/gmp.h /usr/include/gmp.h; fi;    docker-php-ext-configure gd --with-freetype-dir=/usr --with-png-dir=/usr --with-jpeg-dir=/usr --with-webp-dir=/usr;     docker-php-ext-configure gmp --with-gmp="/usr/include/$debMultiarch";     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         exif         gd         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         zip         gmp     ;         pecl install APCu-5.1.18;     pecl install memcached-3.1.5;     pecl install redis-4.3.0;     pecl install imagick-3.4.4;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 17 Apr 2020 16:03:01 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 17 Apr 2020 16:03:01 GMT
VOLUME [/var/www/html]
# Fri, 17 Apr 2020 16:03:02 GMT
ENV NEXTCLOUD_VERSION=17.0.5
# Fri, 17 Apr 2020 16:03:49 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm -r "$GNUPGHOME" nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Fri, 17 Apr 2020 16:03:58 GMT
COPY multi:57de70033920dd582f0dbb812d28f0cfdcf6a102d5b4374faf9435d87a0a7585 in / 
# Mon, 20 Apr 2020 17:15:18 GMT
COPY multi:965c5cb843579fcde0cf3c9edb975639cbd2d55de5f645b1061d46855979394d in /usr/src/nextcloud/config/ 
# Mon, 20 Apr 2020 17:15:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Apr 2020 17:15:19 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:838dc71644c10eab485c4bdfa3879e0fb9e72426de1239cfac1d4c05c23db7be`  
		Last Modified: Thu, 16 Apr 2020 01:08:59 GMT  
		Size: 22.7 MB (22705228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51f8fdbff988ba585ce37f923bf4b49474ca9c838dfe877ca1cb91db76b4750d`  
		Last Modified: Thu, 16 Apr 2020 11:20:53 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8674d4305249be09893f40da34923200030cb3141bef3a0007a7269611c7e1c`  
		Last Modified: Thu, 16 Apr 2020 11:21:11 GMT  
		Size: 59.5 MB (59501464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d380b1b0920e653046b83a9ac2f4faf28f2aca78e9723d0a7d849bb2bb71916`  
		Last Modified: Thu, 16 Apr 2020 11:20:53 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55814bfdce5e4cdce009576d2d6e37e3d2da7132ca01237dcf60c0963d1a92e3`  
		Last Modified: Fri, 17 Apr 2020 14:40:43 GMT  
		Size: 12.4 MB (12436135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8c7175831e70cb59aa0f9dc724c94261245fad5b0cd77329d681d0063e0924a`  
		Last Modified: Fri, 17 Apr 2020 14:40:41 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bde1c17b4642662ca79bafbfe8d32a8fd1c44474280aad63e73f8e0355c7794`  
		Last Modified: Fri, 17 Apr 2020 14:40:47 GMT  
		Size: 26.3 MB (26319740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fcdc4434c6dfbebe8c63ece8fc7c099639a28ca2ed0ce23f84c3e0d384f9366`  
		Last Modified: Fri, 17 Apr 2020 14:40:40 GMT  
		Size: 2.2 KB (2222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e145315daa7aff7930fd84a2c2b78bf3c5c3f6b01b77dcf0605fb00f926aa947`  
		Last Modified: Fri, 17 Apr 2020 14:40:39 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4656499e92423acd536b82697fd4408f5329e9b98b39dd0cab41f959177d702`  
		Last Modified: Fri, 17 Apr 2020 14:40:39 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a50b59830e24aaa2a71a28b7ac62237a7408efb7396279b3467b51709b01ab22`  
		Last Modified: Fri, 17 Apr 2020 14:40:39 GMT  
		Size: 8.4 KB (8416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74db9a12a590eac42994464670207965b996967b126a9993174525a86aa19880`  
		Last Modified: Fri, 17 Apr 2020 16:25:52 GMT  
		Size: 1.4 MB (1425165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc69f9e5138e826dcb41094f96761e4c445ee9e762e966e5ee02dbff8aa6895e`  
		Last Modified: Fri, 17 Apr 2020 16:25:53 GMT  
		Size: 13.8 MB (13847526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153f21671c76cc1e8619f33d8fe15c4cec612f560a87ed3bcc203431f56e6957`  
		Last Modified: Fri, 17 Apr 2020 16:25:49 GMT  
		Size: 534.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bbe823c40c23fa17f06f7f0a4a4a48894dfc6c7f4292a33d72196472d41a88d`  
		Last Modified: Fri, 17 Apr 2020 16:26:15 GMT  
		Size: 73.0 MB (73022158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c95da47cade331a0d373c1e6eafab6971c41c50bf6d47225efe17b30f3a67579`  
		Last Modified: Fri, 17 Apr 2020 16:25:49 GMT  
		Size: 2.6 KB (2553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bfdbc2f060f7a98b41213a40d6aa69e861e055abd09abceb175138030163592`  
		Last Modified: Mon, 20 Apr 2020 17:29:59 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:17-fpm` - linux; arm64 variant v8

```console
$ docker pull nextcloud@sha256:caec608a8c1ead3ea34ac57e2eae707cf44d7482982520614b527dec9af15cf7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.4 MB (226368618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b460cb9c05a2d15920aa5d5c28ef85bc498417ee124fe06411c40cd01005426a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 16 Apr 2020 02:41:52 GMT
ADD file:1aab17002a9095c31dd6928277a045cb26846ac58c3d2d63316332c99a5f90bd in / 
# Thu, 16 Apr 2020 02:41:57 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 13:31:42 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 16 Apr 2020 13:31:44 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 16 Apr 2020 13:32:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 13:32:20 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 16 Apr 2020 13:32:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 16 Apr 2020 13:40:52 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Thu, 16 Apr 2020 13:40:53 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Apr 2020 13:40:54 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Apr 2020 13:10:05 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 17 Apr 2020 13:52:42 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Fri, 17 Apr 2020 13:52:43 GMT
ENV PHP_VERSION=7.3.17
# Fri, 17 Apr 2020 13:52:43 GMT
ENV PHP_URL=https://www.php.net/get/php-7.3.17.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.3.17.tar.xz.asc/from/this/mirror
# Fri, 17 Apr 2020 13:52:44 GMT
ENV PHP_SHA256=6a30304c27f7e7a94538f5ffec599f600ee93aedbbecad8aa4f8bec539b10ad8 PHP_MD5=
# Fri, 17 Apr 2020 13:53:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 17 Apr 2020 13:53:07 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 17 Apr 2020 13:56:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 17 Apr 2020 13:56:36 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Fri, 17 Apr 2020 13:56:38 GMT
RUN docker-php-ext-enable sodium
# Fri, 17 Apr 2020 13:56:40 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Fri, 17 Apr 2020 13:56:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 17 Apr 2020 13:56:41 GMT
WORKDIR /var/www/html
# Fri, 17 Apr 2020 13:56:43 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 17 Apr 2020 13:56:43 GMT
STOPSIGNAL SIGQUIT
# Fri, 17 Apr 2020 13:56:44 GMT
EXPOSE 9000
# Fri, 17 Apr 2020 13:56:45 GMT
CMD ["php-fpm"]
# Fri, 17 Apr 2020 17:10:12 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         busybox-static     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Fri, 17 Apr 2020 17:14:51 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libxml2-dev         libmagickwand-dev         libzip-dev         libwebp-dev         libgmp-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     if [ ! -e /usr/include/gmp.h ]; then ln -s /usr/include/$debMultiarch/gmp.h /usr/include/gmp.h; fi;    docker-php-ext-configure gd --with-freetype-dir=/usr --with-png-dir=/usr --with-jpeg-dir=/usr --with-webp-dir=/usr;     docker-php-ext-configure gmp --with-gmp="/usr/include/$debMultiarch";     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         exif         gd         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         zip         gmp     ;         pecl install APCu-5.1.18;     pecl install memcached-3.1.5;     pecl install redis-4.3.0;     pecl install imagick-3.4.4;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 17 Apr 2020 17:14:54 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 17 Apr 2020 17:14:55 GMT
VOLUME [/var/www/html]
# Fri, 17 Apr 2020 17:14:56 GMT
ENV NEXTCLOUD_VERSION=17.0.5
# Fri, 17 Apr 2020 17:15:48 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm -r "$GNUPGHOME" nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Fri, 17 Apr 2020 17:15:53 GMT
COPY multi:57de70033920dd582f0dbb812d28f0cfdcf6a102d5b4374faf9435d87a0a7585 in / 
# Mon, 20 Apr 2020 16:50:04 GMT
COPY multi:965c5cb843579fcde0cf3c9edb975639cbd2d55de5f645b1061d46855979394d in /usr/src/nextcloud/config/ 
# Mon, 20 Apr 2020 16:50:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Apr 2020 16:50:08 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:3d48095d71a365b5910cea98e5566c152a3f9aa11657560568259bf93ff2f4cb`  
		Last Modified: Thu, 16 Apr 2020 02:48:58 GMT  
		Size: 25.9 MB (25857715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90fdd0b0f5914e23b97e6b4c85e72419571f773834e9c5d730f39161697995d`  
		Last Modified: Thu, 16 Apr 2020 15:02:24 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1efc35f6808c49c804fbb7d49d5dc0cfb27df6b557216ae986e2d002c542c78b`  
		Last Modified: Thu, 16 Apr 2020 15:02:46 GMT  
		Size: 70.3 MB (70334995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d50046d41b1b2f8266660f05392abbe78af7f9798529c7b42d0860191555ea`  
		Last Modified: Thu, 16 Apr 2020 15:02:24 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:932dde0b03fbeb3c68ede07bfff7614888e18c554653b6c837da018ff849a041`  
		Last Modified: Fri, 17 Apr 2020 15:40:59 GMT  
		Size: 12.4 MB (12436858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8731b74a5bf3f575f49760168c933e953c149078657bfe3deb4c12c895c3a1c6`  
		Last Modified: Fri, 17 Apr 2020 15:40:56 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a393b5cb3da892356619da4d0eb8b61097c8a7bdaaeb8ecef59dfa608065f858`  
		Last Modified: Fri, 17 Apr 2020 15:41:02 GMT  
		Size: 28.4 MB (28436050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6a367bccb15a9cfe88094b3f0a36b9093ade0d388a7c3765a66e8f37762c56c`  
		Last Modified: Fri, 17 Apr 2020 15:40:55 GMT  
		Size: 2.2 KB (2221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c423438aca74299eafc163781cdff8aeee9d65e3feb5a47a9e47e79e2134fb37`  
		Last Modified: Fri, 17 Apr 2020 15:40:55 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca71e5096ae73477176c49ecadd10abafc9de1dcb34d4fd0bbefc14a83755fd9`  
		Last Modified: Fri, 17 Apr 2020 15:40:55 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:135b71d2a8281d519667efb7d14a4c02702dc9a4d89c77ef4f1b2f7b0dc05d09`  
		Last Modified: Fri, 17 Apr 2020 15:40:55 GMT  
		Size: 8.4 KB (8414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baee5f14557da8c63d5730a9eeca3ef4d6a7810eee1a2e8b03eb93cd754ceabe`  
		Last Modified: Fri, 17 Apr 2020 17:33:04 GMT  
		Size: 1.6 MB (1601835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b08bf18ade232a3c08e716f20ba350c0c36929196b00c44530604c522c0093e7`  
		Last Modified: Fri, 17 Apr 2020 17:33:06 GMT  
		Size: 14.7 MB (14660998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc49814315bce88fba5f32cf8956993dbdd047e66de7f8adba6ae0129c996a86`  
		Last Modified: Fri, 17 Apr 2020 17:33:03 GMT  
		Size: 532.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:024cbac2af4c87555d56d4cd75c1175b328d08a8e5c84ea906a18d6e69efd0f1`  
		Last Modified: Fri, 17 Apr 2020 17:33:23 GMT  
		Size: 73.0 MB (73023638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a855531b137c5c22e2a4d137aeb5561a3c3d026219a0afe6851802850333637d`  
		Last Modified: Fri, 17 Apr 2020 17:33:02 GMT  
		Size: 2.6 KB (2553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f5a75604118c487890d571863c01f8cadccfaa9e8acb24dbfae3df8d3daf62`  
		Last Modified: Mon, 20 Apr 2020 17:05:24 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:17-fpm` - linux; 386

```console
$ docker pull nextcloud@sha256:67408f5f9449c320a682e370e05b7a2e8ea875b50102ec6a95b7fa901960cc93
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.2 MB (241238471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e17e6568818209b5af406ea8dde4b8e1cc41c19e0280f3ed3a38a9c1f5813028`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 23 Apr 2020 00:39:36 GMT
ADD file:ca6a74f6b738c738c033152fab2a9aacf22bec5f19a994e6a02b5f919ee33ee9 in / 
# Thu, 23 Apr 2020 00:39:36 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 11:58:12 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 23 Apr 2020 11:58:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 23 Apr 2020 11:58:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 11:58:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 23 Apr 2020 11:58:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 23 Apr 2020 12:12:09 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Thu, 23 Apr 2020 12:12:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Apr 2020 12:12:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Apr 2020 12:12:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 23 Apr 2020 12:42:39 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Thu, 23 Apr 2020 12:42:40 GMT
ENV PHP_VERSION=7.3.17
# Thu, 23 Apr 2020 12:42:40 GMT
ENV PHP_URL=https://www.php.net/get/php-7.3.17.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.3.17.tar.xz.asc/from/this/mirror
# Thu, 23 Apr 2020 12:42:40 GMT
ENV PHP_SHA256=6a30304c27f7e7a94538f5ffec599f600ee93aedbbecad8aa4f8bec539b10ad8 PHP_MD5=
# Thu, 23 Apr 2020 12:42:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Apr 2020 12:42:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Apr 2020 12:51:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 23 Apr 2020 12:51:01 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Thu, 23 Apr 2020 12:51:02 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Apr 2020 12:51:03 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Thu, 23 Apr 2020 12:51:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Apr 2020 12:51:04 GMT
WORKDIR /var/www/html
# Thu, 23 Apr 2020 12:51:05 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 23 Apr 2020 12:51:06 GMT
STOPSIGNAL SIGQUIT
# Thu, 23 Apr 2020 12:51:06 GMT
EXPOSE 9000
# Thu, 23 Apr 2020 12:51:06 GMT
CMD ["php-fpm"]
# Thu, 23 Apr 2020 19:58:47 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         busybox-static     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Thu, 23 Apr 2020 20:01:48 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libxml2-dev         libmagickwand-dev         libzip-dev         libwebp-dev         libgmp-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     if [ ! -e /usr/include/gmp.h ]; then ln -s /usr/include/$debMultiarch/gmp.h /usr/include/gmp.h; fi;    docker-php-ext-configure gd --with-freetype-dir=/usr --with-png-dir=/usr --with-jpeg-dir=/usr --with-webp-dir=/usr;     docker-php-ext-configure gmp --with-gmp="/usr/include/$debMultiarch";     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         exif         gd         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         zip         gmp     ;         pecl install APCu-5.1.18;     pecl install memcached-3.1.5;     pecl install redis-4.3.0;     pecl install imagick-3.4.4;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 20:01:48 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Thu, 23 Apr 2020 20:01:49 GMT
VOLUME [/var/www/html]
# Thu, 23 Apr 2020 20:01:49 GMT
ENV NEXTCLOUD_VERSION=17.0.6
# Thu, 23 Apr 2020 20:02:21 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm -r "$GNUPGHOME" nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 20:02:22 GMT
COPY multi:57de70033920dd582f0dbb812d28f0cfdcf6a102d5b4374faf9435d87a0a7585 in / 
# Thu, 23 Apr 2020 20:02:22 GMT
COPY multi:965c5cb843579fcde0cf3c9edb975639cbd2d55de5f645b1061d46855979394d in /usr/src/nextcloud/config/ 
# Thu, 23 Apr 2020 20:02:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Apr 2020 20:02:23 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:5d3da8f33b97fc107a05b3255a55836b76df9f817de632b1fb63c6e9c024f0df`  
		Last Modified: Thu, 23 Apr 2020 00:44:35 GMT  
		Size: 27.8 MB (27753972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b6f6109ad6afc6066a9a9b19c9903065b90dc4ecb232ad312a50d2a3af7c20`  
		Last Modified: Thu, 23 Apr 2020 14:14:03 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79b8d4220a9dc78cfb17d7518deddaa4957545b12088485de215374ec8cd5fcd`  
		Last Modified: Thu, 23 Apr 2020 14:14:26 GMT  
		Size: 81.2 MB (81198126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd893e354bac0fa6072eb200ef4c28c499dce07f2bf148816b9b04550dc27082`  
		Last Modified: Thu, 23 Apr 2020 14:14:02 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82bf2441b571e39b8d8f18ee2cb6f54cbc684dce33fa1ec2cd3e74499b65cfc5`  
		Last Modified: Thu, 23 Apr 2020 14:16:43 GMT  
		Size: 12.4 MB (12437182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548feebb12880b80eb3597aa6521c4c95f54a809a5560d89fb9ffd20d4e673d3`  
		Last Modified: Thu, 23 Apr 2020 14:16:42 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:904f4f91d075a17fc5f859400314c4122995483ae9a1e7283411f5601cb21731`  
		Last Modified: Thu, 23 Apr 2020 14:16:49 GMT  
		Size: 29.3 MB (29326149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1bbe6d0eb29aaa4f7803082e522b19b90003b1cffab32570d138e88c1bb7774`  
		Last Modified: Thu, 23 Apr 2020 14:16:40 GMT  
		Size: 2.2 KB (2221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faccd3a036d0ba1df64d6de61753b8f823d61317aca90c3614bc699810e757e7`  
		Last Modified: Thu, 23 Apr 2020 14:16:40 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:889734f41aa69a643ac92c516d2d4ece9be584116485e9efaecc6ec66e9d4da4`  
		Last Modified: Thu, 23 Apr 2020 14:16:40 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be7417733132e7a6e4559e5f3e6c2ecafc3b8885e01af8a18869380f9bcf4db7`  
		Last Modified: Thu, 23 Apr 2020 14:16:40 GMT  
		Size: 8.4 KB (8417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3914339c50860827eb3ca4d71edef21cb5c02944b9bc690930d52af547761950`  
		Last Modified: Thu, 23 Apr 2020 20:10:36 GMT  
		Size: 1.7 MB (1659103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62354fe1da4fba0d7453ce202754d398c814f08a528c92fd1df05c135201cb13`  
		Last Modified: Thu, 23 Apr 2020 20:10:39 GMT  
		Size: 15.7 MB (15671759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b335e75709e50e4e53ceee056ea7faf527819efd481d9819520c4891e8f18011`  
		Last Modified: Thu, 23 Apr 2020 20:10:34 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2815e9b8e93e8e11ea037dada6d331d20a9552c81a6baf30edae3b2700aef3ed`  
		Last Modified: Thu, 23 Apr 2020 20:11:00 GMT  
		Size: 73.2 MB (73175710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8789634277eca48f934c22a3b9457a042506bfe7fb671c981d0fd77aae84824f`  
		Last Modified: Thu, 23 Apr 2020 20:10:34 GMT  
		Size: 2.6 KB (2553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512ab4e5e2a0677a9ca8a4946525253125045418a85b30ce467c2c4f9fc694ec`  
		Last Modified: Thu, 23 Apr 2020 20:10:34 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:17-fpm` - linux; mips64le

```console
$ docker pull nextcloud@sha256:1c15230414e2d0d046b6ce992c10b37ba612a005dbc686b41513676b2dc5213e
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.4 MB (217360012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:248fc1f2780822d9d05a7a9d16b6031688631e8b7d146c60a9af2fd5f82a39ea`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 23 Apr 2020 00:09:47 GMT
ADD file:7509945bd8a224048260e88b466aa3b156615e16b64e0a6702da277052fcb98b in / 
# Thu, 23 Apr 2020 00:09:48 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 06:05:56 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 23 Apr 2020 06:05:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 23 Apr 2020 06:06:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 06:06:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 23 Apr 2020 06:06:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 23 Apr 2020 06:34:10 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Thu, 23 Apr 2020 06:34:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Apr 2020 06:34:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Apr 2020 06:34:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 23 Apr 2020 07:35:13 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Thu, 23 Apr 2020 07:35:14 GMT
ENV PHP_VERSION=7.3.17
# Thu, 23 Apr 2020 07:35:14 GMT
ENV PHP_URL=https://www.php.net/get/php-7.3.17.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.3.17.tar.xz.asc/from/this/mirror
# Thu, 23 Apr 2020 07:35:14 GMT
ENV PHP_SHA256=6a30304c27f7e7a94538f5ffec599f600ee93aedbbecad8aa4f8bec539b10ad8 PHP_MD5=
# Thu, 23 Apr 2020 07:35:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Apr 2020 07:35:38 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Apr 2020 07:52:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 23 Apr 2020 07:52:11 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Thu, 23 Apr 2020 07:52:13 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Apr 2020 07:52:16 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Thu, 23 Apr 2020 07:52:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Apr 2020 07:52:16 GMT
WORKDIR /var/www/html
# Thu, 23 Apr 2020 07:52:19 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 23 Apr 2020 07:52:19 GMT
STOPSIGNAL SIGQUIT
# Thu, 23 Apr 2020 07:52:20 GMT
EXPOSE 9000
# Thu, 23 Apr 2020 07:52:20 GMT
CMD ["php-fpm"]
# Thu, 23 Apr 2020 18:43:00 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         busybox-static     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Thu, 23 Apr 2020 18:50:56 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libxml2-dev         libmagickwand-dev         libzip-dev         libwebp-dev         libgmp-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     if [ ! -e /usr/include/gmp.h ]; then ln -s /usr/include/$debMultiarch/gmp.h /usr/include/gmp.h; fi;    docker-php-ext-configure gd --with-freetype-dir=/usr --with-png-dir=/usr --with-jpeg-dir=/usr --with-webp-dir=/usr;     docker-php-ext-configure gmp --with-gmp="/usr/include/$debMultiarch";     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         exif         gd         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         zip         gmp     ;         pecl install APCu-5.1.18;     pecl install memcached-3.1.5;     pecl install redis-4.3.0;     pecl install imagick-3.4.4;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 18:50:59 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Thu, 23 Apr 2020 18:50:59 GMT
VOLUME [/var/www/html]
# Thu, 23 Apr 2020 19:44:39 GMT
ENV NEXTCLOUD_VERSION=17.0.6
# Thu, 23 Apr 2020 19:45:57 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm -r "$GNUPGHOME" nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 19:46:00 GMT
COPY multi:57de70033920dd582f0dbb812d28f0cfdcf6a102d5b4374faf9435d87a0a7585 in / 
# Thu, 23 Apr 2020 19:46:01 GMT
COPY multi:965c5cb843579fcde0cf3c9edb975639cbd2d55de5f645b1061d46855979394d in /usr/src/nextcloud/config/ 
# Thu, 23 Apr 2020 19:46:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Apr 2020 19:46:02 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:ae8f0fa6cb0d971b4b8fedf7fc9b00f61f780b383fe7d64e6c2e4be8d20c3987`  
		Last Modified: Thu, 23 Apr 2020 00:17:46 GMT  
		Size: 25.8 MB (25762125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40126b44a2da17b3b1ac47d34381ba6a16b24d65255dc01924d9b8c262f8d082`  
		Last Modified: Thu, 23 Apr 2020 09:13:18 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:027e198b736c35bc63dd89410b3f1b712ea296863eb6fc6c8a0d74dc5c61e85b`  
		Last Modified: Thu, 23 Apr 2020 09:14:18 GMT  
		Size: 61.4 MB (61383062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d28477260564a7b079978c5069cb78c9457f06dfe7057853924d0e4ca13b0a`  
		Last Modified: Thu, 23 Apr 2020 09:13:17 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41826fd1bff02a91a78ffce343e71f5e65d2466b62f1fe773e7712272bc93ed7`  
		Last Modified: Thu, 23 Apr 2020 09:20:33 GMT  
		Size: 12.4 MB (12435474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f3e7cdea3a7a8ae3cbe4c099bf2a63147b6592c59a18dbb956cce7e5308cf23`  
		Last Modified: Thu, 23 Apr 2020 09:20:29 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb6dc13e534917c0ecc9725fd58422f24cde43ff024a7913ce9878769960d7e9`  
		Last Modified: Thu, 23 Apr 2020 09:20:49 GMT  
		Size: 28.1 MB (28106272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8765afb6ef91d53c7ca2eaff97cc9e477fcb72bba5923a47423e3151354868`  
		Last Modified: Thu, 23 Apr 2020 09:20:26 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddb1ff12be50998d8efd451f10dcc4a9fe44a2e6546e39c72b9169c05ebb3ec`  
		Last Modified: Thu, 23 Apr 2020 09:20:26 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5917fa36e24ee2b5dccbe34c37542555fd9c6f1c1867aedc151392197f81009e`  
		Last Modified: Thu, 23 Apr 2020 09:20:26 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3312ca8dcb6a84d03fb28c32d092001ef48b33597ec427b5b0c6c3f54a351364`  
		Last Modified: Thu, 23 Apr 2020 09:20:26 GMT  
		Size: 8.4 KB (8416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b68022c670570477844840cd29727a2f562feffd177f1b6f2ae27118aa7b551d`  
		Last Modified: Thu, 23 Apr 2020 19:14:44 GMT  
		Size: 1.7 MB (1739633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8f506ff5d92cc2ef025dce7ad5794f1a20feb8f7164eaf4f37392198adfd77b`  
		Last Modified: Thu, 23 Apr 2020 19:14:53 GMT  
		Size: 14.7 MB (14742632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3675365a5e33835ab340908d19315f055c006afd94e716cf6a95b74686b6906e`  
		Last Modified: Thu, 23 Apr 2020 19:14:40 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9e54bfcb14ce8b098e756c7af7993731413d035d0c6d1022c9cbe90705ad9fb`  
		Last Modified: Thu, 23 Apr 2020 20:08:36 GMT  
		Size: 73.2 MB (73174343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45cdaa4cb292a34f8065cd03b20321dd6db909fcab60d5dd9c20522ff8dbe49b`  
		Last Modified: Thu, 23 Apr 2020 20:07:37 GMT  
		Size: 2.6 KB (2553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b96fd61d6ac2a3be0797368906ccdbb6d9ebb1ba69b801204c924463965827d`  
		Last Modified: Thu, 23 Apr 2020 20:07:37 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:17-fpm` - linux; ppc64le

```console
$ docker pull nextcloud@sha256:03d5fb1a13e8bff3f94cb2b7fb844bf62fc1c6476600cd47ba9d4aba4768a1f0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.1 MB (247097420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7263ec765841bc6c659590f972c8ba33c527babbebf0264db8ff364c6bfdf0b8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 16 Apr 2020 01:38:30 GMT
ADD file:9beea54416432abbd09d26b965c3c8e5bea8e233113f9bc308294c0008ee886f in / 
# Thu, 16 Apr 2020 01:38:39 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 09:23:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 16 Apr 2020 09:23:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 16 Apr 2020 09:26:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 09:26:37 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 16 Apr 2020 09:26:44 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 16 Apr 2020 09:43:24 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Thu, 16 Apr 2020 09:43:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Apr 2020 09:43:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Apr 2020 16:22:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 17 Apr 2020 17:19:31 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Fri, 17 Apr 2020 17:19:33 GMT
ENV PHP_VERSION=7.3.17
# Fri, 17 Apr 2020 17:19:37 GMT
ENV PHP_URL=https://www.php.net/get/php-7.3.17.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.3.17.tar.xz.asc/from/this/mirror
# Fri, 17 Apr 2020 17:19:40 GMT
ENV PHP_SHA256=6a30304c27f7e7a94538f5ffec599f600ee93aedbbecad8aa4f8bec539b10ad8 PHP_MD5=
# Fri, 17 Apr 2020 17:20:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 17 Apr 2020 17:21:00 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 17 Apr 2020 17:25:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 17 Apr 2020 17:25:22 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Fri, 17 Apr 2020 17:25:28 GMT
RUN docker-php-ext-enable sodium
# Fri, 17 Apr 2020 17:25:35 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Fri, 17 Apr 2020 17:25:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 17 Apr 2020 17:25:41 GMT
WORKDIR /var/www/html
# Fri, 17 Apr 2020 17:25:47 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 17 Apr 2020 17:25:49 GMT
STOPSIGNAL SIGQUIT
# Fri, 17 Apr 2020 17:25:51 GMT
EXPOSE 9000
# Fri, 17 Apr 2020 17:25:58 GMT
CMD ["php-fpm"]
# Fri, 17 Apr 2020 23:38:43 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         busybox-static     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Fri, 17 Apr 2020 23:54:03 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libxml2-dev         libmagickwand-dev         libzip-dev         libwebp-dev         libgmp-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     if [ ! -e /usr/include/gmp.h ]; then ln -s /usr/include/$debMultiarch/gmp.h /usr/include/gmp.h; fi;    docker-php-ext-configure gd --with-freetype-dir=/usr --with-png-dir=/usr --with-jpeg-dir=/usr --with-webp-dir=/usr;     docker-php-ext-configure gmp --with-gmp="/usr/include/$debMultiarch";     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         exif         gd         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         zip         gmp     ;         pecl install APCu-5.1.18;     pecl install memcached-3.1.5;     pecl install redis-4.3.0;     pecl install imagick-3.4.4;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 17 Apr 2020 23:54:12 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 17 Apr 2020 23:54:15 GMT
VOLUME [/var/www/html]
# Fri, 17 Apr 2020 23:54:19 GMT
ENV NEXTCLOUD_VERSION=17.0.5
# Fri, 17 Apr 2020 23:55:48 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm -r "$GNUPGHOME" nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Fri, 17 Apr 2020 23:55:54 GMT
COPY multi:57de70033920dd582f0dbb812d28f0cfdcf6a102d5b4374faf9435d87a0a7585 in / 
# Mon, 20 Apr 2020 19:15:59 GMT
COPY multi:965c5cb843579fcde0cf3c9edb975639cbd2d55de5f645b1061d46855979394d in /usr/src/nextcloud/config/ 
# Mon, 20 Apr 2020 19:16:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Apr 2020 19:16:04 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:f268991f8af64097bbfefa3f01dd3fdb7f715051a3681f352504a3ecaa9d3596`  
		Last Modified: Thu, 16 Apr 2020 01:54:39 GMT  
		Size: 30.5 MB (30524651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e55b2b55517816e89fca19add44833230f6d938d155804bd44365751b72b58`  
		Last Modified: Thu, 16 Apr 2020 11:51:46 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7db96afbffa71edfc2af1f0318952855246fcaefbc14e4126962213cdf8b5438`  
		Last Modified: Thu, 16 Apr 2020 11:52:31 GMT  
		Size: 82.3 MB (82260089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4f404cddbb9ad9a8c7b8c8044cb22bde7e41bf489799ff67e3b5d1345759a5e`  
		Last Modified: Thu, 16 Apr 2020 11:51:46 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03378dc34405fe61f1d7718e0045bf93f5967ff54e4a5f95105b13190f20786`  
		Last Modified: Fri, 17 Apr 2020 20:15:49 GMT  
		Size: 12.4 MB (12437867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c3ac10bb71e4bac959069d7955fe35eb9b784b8971283b9d8e4c0f2eb1a3dbe`  
		Last Modified: Fri, 17 Apr 2020 20:15:45 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f459ae96a3861f4f5f9a88ff1c23aca66fd5bde699b269be9c575f078309bac0`  
		Last Modified: Fri, 17 Apr 2020 20:15:56 GMT  
		Size: 30.5 MB (30462972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f594ae286212cd07844ce01fb6722a069128093213793b225c0b9ff345e391`  
		Last Modified: Fri, 17 Apr 2020 20:15:43 GMT  
		Size: 2.2 KB (2218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69fe7114c24ae50b01c4843d986d357d0b9004000490468f28e8a315d3d469d6`  
		Last Modified: Fri, 17 Apr 2020 20:15:43 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa91855c7409958ba67adff4d9bc3b87dd5b7a55725b43bb3de7989765fa4299`  
		Last Modified: Fri, 17 Apr 2020 20:15:42 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e3cbf9a37834203e3e6404479e83711b2080b8874b8197546f69ea623c2ed59`  
		Last Modified: Fri, 17 Apr 2020 20:15:43 GMT  
		Size: 8.4 KB (8415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5f469bd8edb7ae78046a9f083b550e82bdee58e5673a6a8240f3ce80c420511`  
		Last Modified: Sat, 18 Apr 2020 00:20:41 GMT  
		Size: 1.8 MB (1802608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d598691df31942663591b8340cbf4c85debee7592ac59bbe7f1a7cb80c73fccc`  
		Last Modified: Sat, 18 Apr 2020 00:20:51 GMT  
		Size: 16.6 MB (16566561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:411c6351df36e9c53c7f99f80c5668851ce18a501332f52d54ae9a4a68803340`  
		Last Modified: Sat, 18 Apr 2020 00:20:35 GMT  
		Size: 534.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09665802832db0671dd3028ae364aaf3fdff6292a95a391b02ee7548bfab8ae6`  
		Last Modified: Sat, 18 Apr 2020 00:21:51 GMT  
		Size: 73.0 MB (73026141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0353b675066db74e5500f9010b572184dcef389c643ce427a1a9b549dea55aef`  
		Last Modified: Sat, 18 Apr 2020 00:20:35 GMT  
		Size: 2.6 KB (2553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3dac81be7e45152e2780e23a1febc8c056bb2fbcf15ab1964f90f55565b8dc6`  
		Last Modified: Mon, 20 Apr 2020 20:40:39 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:17-fpm` - linux; s390x

```console
$ docker pull nextcloud@sha256:703a54ef1bbb03b2ae4d3467513c9f4a9377930b09202df7246ddf1386ce5bf4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.2 MB (220200810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d230df08261b870017fb5e1f5767dd061da1c52fc1fc941831f1cfd0b1f7c06`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 23 Apr 2020 00:51:48 GMT
ADD file:f6c2560f9185c1bcaff95e576e57449f606d51b85fad02646c1b0962bc9353c9 in / 
# Thu, 23 Apr 2020 00:51:50 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 07:06:58 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 23 Apr 2020 07:06:59 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 23 Apr 2020 07:07:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 07:07:20 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 23 Apr 2020 07:07:20 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 23 Apr 2020 07:12:25 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Thu, 23 Apr 2020 07:12:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Apr 2020 07:12:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Apr 2020 07:12:26 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 23 Apr 2020 07:23:02 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Thu, 23 Apr 2020 07:23:03 GMT
ENV PHP_VERSION=7.3.17
# Thu, 23 Apr 2020 07:23:03 GMT
ENV PHP_URL=https://www.php.net/get/php-7.3.17.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.3.17.tar.xz.asc/from/this/mirror
# Thu, 23 Apr 2020 07:23:03 GMT
ENV PHP_SHA256=6a30304c27f7e7a94538f5ffec599f600ee93aedbbecad8aa4f8bec539b10ad8 PHP_MD5=
# Thu, 23 Apr 2020 07:23:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Apr 2020 07:23:09 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Apr 2020 07:25:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 23 Apr 2020 07:25:23 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Thu, 23 Apr 2020 07:25:24 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Apr 2020 07:25:25 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Thu, 23 Apr 2020 07:25:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Apr 2020 07:25:25 GMT
WORKDIR /var/www/html
# Thu, 23 Apr 2020 07:25:26 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 23 Apr 2020 07:25:26 GMT
STOPSIGNAL SIGQUIT
# Thu, 23 Apr 2020 07:25:26 GMT
EXPOSE 9000
# Thu, 23 Apr 2020 07:25:26 GMT
CMD ["php-fpm"]
# Thu, 23 Apr 2020 15:02:53 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         busybox-static     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Thu, 23 Apr 2020 15:04:36 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libxml2-dev         libmagickwand-dev         libzip-dev         libwebp-dev         libgmp-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     if [ ! -e /usr/include/gmp.h ]; then ln -s /usr/include/$debMultiarch/gmp.h /usr/include/gmp.h; fi;    docker-php-ext-configure gd --with-freetype-dir=/usr --with-png-dir=/usr --with-jpeg-dir=/usr --with-webp-dir=/usr;     docker-php-ext-configure gmp --with-gmp="/usr/include/$debMultiarch";     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         exif         gd         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         zip         gmp     ;         pecl install APCu-5.1.18;     pecl install memcached-3.1.5;     pecl install redis-4.3.0;     pecl install imagick-3.4.4;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 15:04:37 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Thu, 23 Apr 2020 15:04:38 GMT
VOLUME [/var/www/html]
# Thu, 23 Apr 2020 15:07:01 GMT
ENV NEXTCLOUD_VERSION=17.0.5
# Thu, 23 Apr 2020 15:07:48 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm -r "$GNUPGHOME" nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 15:08:04 GMT
COPY multi:57de70033920dd582f0dbb812d28f0cfdcf6a102d5b4374faf9435d87a0a7585 in / 
# Thu, 23 Apr 2020 15:08:05 GMT
COPY multi:965c5cb843579fcde0cf3c9edb975639cbd2d55de5f645b1061d46855979394d in /usr/src/nextcloud/config/ 
# Thu, 23 Apr 2020 15:08:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Apr 2020 15:08:07 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:d89dc3741ad42b79c3d8545495c429f3100d3f22234ff993bd04017b0675e868`  
		Last Modified: Thu, 23 Apr 2020 00:56:00 GMT  
		Size: 25.7 MB (25712105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea08bde6b0b1d4817b549715812249f566ebbdb1c81c26581d3a34e9f0646ac7`  
		Last Modified: Thu, 23 Apr 2020 08:06:47 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb184ae545a538a5e99fa27bf76f21aeb7324f061ae0e6ed7ab6003f8ec8d861`  
		Last Modified: Thu, 23 Apr 2020 08:06:57 GMT  
		Size: 64.7 MB (64698982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3bff96336b89f3c42d3c1ca154c9bee84597dd2e1776952a82e47e94dac6e5c`  
		Last Modified: Thu, 23 Apr 2020 08:06:45 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f50122b6cf9abbf8da09ab7c094866cae6e8b716797cd5918a99aa45124400`  
		Last Modified: Thu, 23 Apr 2020 08:09:34 GMT  
		Size: 12.4 MB (12436340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d65341ecbe188200a28dc01abe61d4bc4947262412757364c76f1636251e94`  
		Last Modified: Thu, 23 Apr 2020 08:09:32 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b728c12258744c6ecf833dd0587ed78465959b71017846d45a984e9db5d89c7`  
		Last Modified: Thu, 23 Apr 2020 08:09:36 GMT  
		Size: 27.9 MB (27900250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5561c5d49def3a13a346f2dbbc8852b4976038ac450a4b8fb698fefc2ae41df9`  
		Last Modified: Thu, 23 Apr 2020 08:09:30 GMT  
		Size: 2.2 KB (2221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a76a17848b97308d6cc8a5529b6ed4c8774fa11af50ece273417e5b5abc78e28`  
		Last Modified: Thu, 23 Apr 2020 08:09:35 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b59368d4681e2341221f5f4765cce1f4b7ded831cb5df0bdf409cb335dccbc`  
		Last Modified: Thu, 23 Apr 2020 08:09:30 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c81bf671172cce6a34918e01e0bb7c77c892d4fa59120c6038777cf8fb893b`  
		Last Modified: Thu, 23 Apr 2020 08:09:35 GMT  
		Size: 8.4 KB (8416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d307232e523034634ba339ebc237533458dfde573e91da508d47a1ef9ec408`  
		Last Modified: Thu, 23 Apr 2020 15:18:05 GMT  
		Size: 1.6 MB (1594400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5086de6ff557b6da810807a6ae23859f3e32a9003400f43a8cd07fb64ba89c1d`  
		Last Modified: Thu, 23 Apr 2020 15:18:03 GMT  
		Size: 14.8 MB (14820377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47be3fe190e581a3a287443b9fb878efc1a221af17e17fb73fc3af06e781d872`  
		Last Modified: Thu, 23 Apr 2020 15:18:06 GMT  
		Size: 534.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f062ab7f22342d9a721e908dcfdb2b75b678e58ee0236ca8a876542d8f62c2b`  
		Last Modified: Thu, 23 Apr 2020 15:19:06 GMT  
		Size: 73.0 MB (73021830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c19f6c22ab9a6fe0c9c7202929c3cb970778863971adbd73c65da39f274287`  
		Last Modified: Thu, 23 Apr 2020 15:19:11 GMT  
		Size: 2.6 KB (2553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b23923bcd53639d09a2c8a9d5991e5dde61d6a0721eefd05b44b848f641f51aa`  
		Last Modified: Thu, 23 Apr 2020 15:18:56 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
