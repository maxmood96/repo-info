## `nextcloud:production-fpm`

```console
$ docker pull nextcloud@sha256:1afc148a702baaa8bf42788d7b9915d240a67080e2bd7cc9cf7df9d6f07bfbfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `nextcloud:production-fpm` - linux; amd64

```console
$ docker pull nextcloud@sha256:60f4e07328f50315aea350addbc569baacbacb263fad63e41d52ebe63384a6a9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.4 MB (354449998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56eea6cccb94d4b2a3afc92b9039b26dba1e8f76a9b96a56ff2d463aedc5d53a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:23 GMT
ADD file:4a063d4e089ef10c6806d7042a0040078674ac2db61df02df8bbb8fa4894910a in / 
# Tue, 04 Jul 2023 01:20:23 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 13:39:51 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 04 Jul 2023 13:39:51 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 04 Jul 2023 13:40:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 13:40:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 04 Jul 2023 13:40:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 04 Jul 2023 13:40:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Jul 2023 13:40:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Jul 2023 13:40:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 04 Jul 2023 14:08:58 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Mon, 10 Jul 2023 22:05:15 GMT
ENV PHP_VERSION=8.2.8
# Mon, 10 Jul 2023 22:05:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.8.tar.xz.asc
# Mon, 10 Jul 2023 22:05:16 GMT
ENV PHP_SHA256=cfe1055fbcd486de7d3312da6146949aae577365808790af6018205567609801
# Mon, 10 Jul 2023 22:05:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 10 Jul 2023 22:05:31 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Mon, 10 Jul 2023 22:14:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Mon, 10 Jul 2023 22:14:57 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Mon, 10 Jul 2023 22:14:57 GMT
RUN docker-php-ext-enable sodium
# Mon, 10 Jul 2023 22:14:57 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 10 Jul 2023 22:14:57 GMT
WORKDIR /var/www/html
# Mon, 10 Jul 2023 22:14:58 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Mon, 10 Jul 2023 22:14:58 GMT
STOPSIGNAL SIGQUIT
# Mon, 10 Jul 2023 22:14:58 GMT
EXPOSE 9000
# Mon, 10 Jul 2023 22:14:58 GMT
CMD ["php-fpm"]
# Tue, 11 Jul 2023 03:25:59 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Tue, 11 Jul 2023 03:25:59 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 11 Jul 2023 03:25:59 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 11 Jul 2023 03:28:23 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.22;     pecl install imagick-3.7.0;     pecl install memcached-3.2.0;     pecl install redis-5.3.7;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 03:28:23 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Tue, 11 Jul 2023 03:28:23 GMT
VOLUME [/var/www/html]
# Tue, 11 Jul 2023 03:28:24 GMT
ENV NEXTCLOUD_VERSION=26.0.3
# Tue, 11 Jul 2023 03:29:14 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-26.0.3.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-26.0.3.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 03:29:15 GMT
COPY multi:f14917ef3f8441cf73a9faa81b54c7e51061a07185e365974d47ddb315426c8f in / 
# Tue, 11 Jul 2023 03:29:16 GMT
COPY multi:1aa0c68034f207c7e2fb6f047fda45b55878afe2781ef10723107e35ee22547e in /usr/src/nextcloud/config/ 
# Tue, 11 Jul 2023 03:29:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 11 Jul 2023 03:29:16 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:9d21b12d5fab9ab82969054d72411ce627c209257df64b6057016c981e163c30`  
		Last Modified: Tue, 04 Jul 2023 01:25:43 GMT  
		Size: 31.4 MB (31417388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2f438b30581593b3d4296a477ca4f824e7d5d680b7e34281e3a3d309ce7f28`  
		Last Modified: Tue, 04 Jul 2023 16:17:15 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f04ed8a9ea49fbc2a12ed1b0d62952138c95ae060eaa94a8a8e71469eb6d4424`  
		Last Modified: Tue, 04 Jul 2023 16:17:26 GMT  
		Size: 91.6 MB (91635583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10478cdfe5dae28f47467d50b3247339d7d7dcda74203fe83b5be38ab63603e3`  
		Last Modified: Tue, 04 Jul 2023 16:17:14 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8275da7b7714915d0d85690b691b6fcf97362cbe77df56a08779a804ce0cef48`  
		Last Modified: Mon, 10 Jul 2023 23:51:38 GMT  
		Size: 12.4 MB (12354515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93e00a9b8328b3a0d9e1f53bcc8ee0aeaee02fdefc84bf8371511c13727e5929`  
		Last Modified: Mon, 10 Jul 2023 23:51:37 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1ec810e620405b09041be8a6c46bd279832c9f194e0422f59499f89410bb20`  
		Last Modified: Mon, 10 Jul 2023 23:52:23 GMT  
		Size: 26.5 MB (26540810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43bb6aa87f7bb87bac84f08f1a90505a7501334c27bc2f30aa339383a89422be`  
		Last Modified: Mon, 10 Jul 2023 23:52:19 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:323b79ac8ffb98993d7ae42bbecd4ccb179ded5c5acccedffcad8725461fbca5`  
		Last Modified: Mon, 10 Jul 2023 23:52:19 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ff4d784caf6dc6d665552a5a6e96da0a16cc61631ff18c7b1ab9d517285cca`  
		Last Modified: Mon, 10 Jul 2023 23:52:19 GMT  
		Size: 9.2 KB (9176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e64f54457b0e118c1d1fb50bd05827473417cabc8d4d5481e06a5e71285e340e`  
		Last Modified: Tue, 11 Jul 2023 03:39:01 GMT  
		Size: 19.5 MB (19482229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dca98e13d35c0ce08cb4739eeda53a884f22efb65922c5cfc8fb297490ca07a`  
		Last Modified: Tue, 11 Jul 2023 03:38:57 GMT  
		Size: 4.1 MB (4081493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4365445fcf3c588893b41304227682a33ce4d641da989017e207d7720283f27`  
		Last Modified: Tue, 11 Jul 2023 03:38:56 GMT  
		Size: 762.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5990a88a81ddd99d99de477e8f122537dab318dce4e3c13e355144fbe2fbee7`  
		Last Modified: Tue, 11 Jul 2023 03:39:15 GMT  
		Size: 168.9 MB (168918671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4d995b335bc85acab83755369119aad3806ca7904d13ef3d67bd291206f1ed9`  
		Last Modified: Tue, 11 Jul 2023 03:38:56 GMT  
		Size: 3.5 KB (3470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03978128d92d566d5fcf56f49c8fbfba2e084246edc128e5e8051de98e10f464`  
		Last Modified: Tue, 11 Jul 2023 03:38:56 GMT  
		Size: 2.2 KB (2223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:production-fpm` - linux; arm variant v5

```console
$ docker pull nextcloud@sha256:c00aef64a20b9d859f4ad5fd9b2da8796ca40c799cadef02c2c0199d2488bd3f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.0 MB (329964905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9073f721c71029efdfc8c126e424678a184d7d08aa4ec86e2873006ab6e0631`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 04 Jul 2023 00:48:47 GMT
ADD file:2dc75d45982de1ae93d7466556a8d6f806e24a837046bd3445b5df6853b0b5bb in / 
# Tue, 04 Jul 2023 00:48:47 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:48:42 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 04 Jul 2023 04:48:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 04 Jul 2023 04:49:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:49:11 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 04 Jul 2023 04:49:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 04 Jul 2023 04:49:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Jul 2023 04:49:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Jul 2023 04:49:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 04 Jul 2023 05:12:30 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Mon, 10 Jul 2023 22:02:22 GMT
ENV PHP_VERSION=8.2.8
# Mon, 10 Jul 2023 22:02:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.8.tar.xz.asc
# Mon, 10 Jul 2023 22:02:22 GMT
ENV PHP_SHA256=cfe1055fbcd486de7d3312da6146949aae577365808790af6018205567609801
# Mon, 10 Jul 2023 22:02:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 10 Jul 2023 22:02:40 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Mon, 10 Jul 2023 22:23:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Mon, 10 Jul 2023 22:23:14 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Mon, 10 Jul 2023 22:23:15 GMT
RUN docker-php-ext-enable sodium
# Mon, 10 Jul 2023 22:23:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 10 Jul 2023 22:23:16 GMT
WORKDIR /var/www/html
# Mon, 10 Jul 2023 22:23:17 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Mon, 10 Jul 2023 22:23:17 GMT
STOPSIGNAL SIGQUIT
# Mon, 10 Jul 2023 22:23:17 GMT
EXPOSE 9000
# Mon, 10 Jul 2023 22:23:18 GMT
CMD ["php-fpm"]
# Tue, 11 Jul 2023 00:52:56 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Tue, 11 Jul 2023 00:52:57 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 11 Jul 2023 00:52:57 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 11 Jul 2023 00:55:20 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.22;     pecl install imagick-3.7.0;     pecl install memcached-3.2.0;     pecl install redis-5.3.7;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 00:55:21 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Tue, 11 Jul 2023 00:55:21 GMT
VOLUME [/var/www/html]
# Tue, 11 Jul 2023 00:55:21 GMT
ENV NEXTCLOUD_VERSION=26.0.3
# Tue, 11 Jul 2023 00:56:20 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-26.0.3.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-26.0.3.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 00:56:23 GMT
COPY multi:f14917ef3f8441cf73a9faa81b54c7e51061a07185e365974d47ddb315426c8f in / 
# Tue, 11 Jul 2023 00:56:23 GMT
COPY multi:1aa0c68034f207c7e2fb6f047fda45b55878afe2781ef10723107e35ee22547e in /usr/src/nextcloud/config/ 
# Tue, 11 Jul 2023 00:56:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 11 Jul 2023 00:56:23 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:e5c23077f8d036e239b1eb6572155131327f3345abd95ce868b997d2e1d969f3`  
		Last Modified: Tue, 04 Jul 2023 00:52:38 GMT  
		Size: 28.9 MB (28918872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5947d74e493c12b73269bb337a8bfc7bc3b554fe645538cdbcc95d4e0213f0`  
		Last Modified: Tue, 04 Jul 2023 06:44:19 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9743ee9ea82452e98206395affa9250c55176663db53538325eddb00ec7473d`  
		Last Modified: Tue, 04 Jul 2023 06:44:33 GMT  
		Size: 73.7 MB (73687070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08282735eb62bf10fb1f77d6c5a591e49b267feb5001b8eb6fbb4779f5eb84cd`  
		Last Modified: Tue, 04 Jul 2023 06:44:19 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d9a62ae6407662c0376c5e7517c7e82e240172e14ebcc7a722874a680c0e7e`  
		Last Modified: Mon, 10 Jul 2023 23:31:13 GMT  
		Size: 12.4 MB (12353079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76e78d53d8e11d71160fda067374bbdf95bf343a524d20e00065b408a7cfd28f`  
		Last Modified: Mon, 10 Jul 2023 23:31:12 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d378e094a8971646a8cfacc21fb10c142fedaf0ace341a72b25ea53de89d12cb`  
		Last Modified: Mon, 10 Jul 2023 23:32:08 GMT  
		Size: 25.1 MB (25120090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75615565abbad59dcc627f4871787879c621a37139b4c44cc1a1a5eaaff20844`  
		Last Modified: Mon, 10 Jul 2023 23:32:03 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0dd1d721382b5fa25c6464e16f75fef2f674c2005091ca30d655c7bba06579d`  
		Last Modified: Mon, 10 Jul 2023 23:32:03 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0cd0197ec109cc617e09e9360017c045e222f4fe0f7169723ab12178e854316`  
		Last Modified: Mon, 10 Jul 2023 23:32:03 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:651ef385e1f0c5427b6d5b9d2ded1e4c83297cf568f4c5d24bb972c30f1fd114`  
		Last Modified: Tue, 11 Jul 2023 01:02:30 GMT  
		Size: 17.4 MB (17427594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8274f700a630558951f370a02f3d762933aeae49ed7d02c88e39fa748574632`  
		Last Modified: Tue, 11 Jul 2023 01:02:27 GMT  
		Size: 3.5 MB (3521871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7cbeb4d44f86c6e830b8562e6a934ea52b04d26e6e36ef540b5ca763a551888`  
		Last Modified: Tue, 11 Jul 2023 01:02:25 GMT  
		Size: 759.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:767fe73cd1b37b18ece9ff6af33a792e60e7d890ba21d5b254a1a0f796ebb419`  
		Last Modified: Tue, 11 Jul 2023 01:02:57 GMT  
		Size: 168.9 MB (168917020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7042b8279dde07f4eb668e642dea8cb2b540c8e6e9c05e6811214f42b6e0b6`  
		Last Modified: Tue, 11 Jul 2023 01:02:25 GMT  
		Size: 3.5 KB (3469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc3dadfbd104fe493e7dc25a230c88b8bc7ae609dc16c2eab41bc03305eb948d`  
		Last Modified: Tue, 11 Jul 2023 01:02:25 GMT  
		Size: 2.2 KB (2221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:production-fpm` - linux; arm variant v7

```console
$ docker pull nextcloud@sha256:a9c99638f6178966e76f015a51092d2a8fd9c059eb17d0aea6e043e2821f77f3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.7 MB (320720805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d3020e6ab68b8d3ae6351c3c3d52113608fd0683153c66b4c2bfa1b0ccc4733`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 04 Jul 2023 00:58:20 GMT
ADD file:c023c66ee4b7cdae5c542f2ad2dd35aef94ad24e1b3b479a16538c46013ae6a5 in / 
# Tue, 04 Jul 2023 00:58:21 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 10:20:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 04 Jul 2023 10:20:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 04 Jul 2023 10:20:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 10:20:57 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 04 Jul 2023 10:20:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 04 Jul 2023 10:20:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Jul 2023 10:20:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Jul 2023 10:20:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 04 Jul 2023 10:44:28 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Mon, 10 Jul 2023 21:55:12 GMT
ENV PHP_VERSION=8.2.8
# Mon, 10 Jul 2023 21:55:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.8.tar.xz.asc
# Mon, 10 Jul 2023 21:55:13 GMT
ENV PHP_SHA256=cfe1055fbcd486de7d3312da6146949aae577365808790af6018205567609801
# Mon, 10 Jul 2023 21:55:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 10 Jul 2023 21:55:28 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Mon, 10 Jul 2023 22:09:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Mon, 10 Jul 2023 22:09:02 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Mon, 10 Jul 2023 22:09:03 GMT
RUN docker-php-ext-enable sodium
# Mon, 10 Jul 2023 22:09:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 10 Jul 2023 22:09:04 GMT
WORKDIR /var/www/html
# Mon, 10 Jul 2023 22:09:05 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Mon, 10 Jul 2023 22:09:05 GMT
STOPSIGNAL SIGQUIT
# Mon, 10 Jul 2023 22:09:06 GMT
EXPOSE 9000
# Mon, 10 Jul 2023 22:09:06 GMT
CMD ["php-fpm"]
# Tue, 11 Jul 2023 03:08:32 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Tue, 11 Jul 2023 03:08:32 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 11 Jul 2023 03:08:32 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 11 Jul 2023 03:10:34 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.22;     pecl install imagick-3.7.0;     pecl install memcached-3.2.0;     pecl install redis-5.3.7;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 03:10:35 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Tue, 11 Jul 2023 03:10:35 GMT
VOLUME [/var/www/html]
# Tue, 11 Jul 2023 03:10:35 GMT
ENV NEXTCLOUD_VERSION=26.0.3
# Tue, 11 Jul 2023 03:11:33 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-26.0.3.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-26.0.3.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 03:11:37 GMT
COPY multi:f14917ef3f8441cf73a9faa81b54c7e51061a07185e365974d47ddb315426c8f in / 
# Tue, 11 Jul 2023 03:11:37 GMT
COPY multi:1aa0c68034f207c7e2fb6f047fda45b55878afe2781ef10723107e35ee22547e in /usr/src/nextcloud/config/ 
# Tue, 11 Jul 2023 03:11:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 11 Jul 2023 03:11:38 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:d9e6a8b782e380f447723ac26499c5014f2d383b9210819b9e73e97abaf81249`  
		Last Modified: Tue, 04 Jul 2023 01:03:35 GMT  
		Size: 26.6 MB (26578754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f8587a474187205cd66b629c8f61d29df91612c819f78fe0c76c2e4fc36769c`  
		Last Modified: Tue, 04 Jul 2023 12:32:26 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bf694dd69f04ad96b686a1d38ddd61b07af4c3d91de73f3c756104350813313`  
		Last Modified: Tue, 04 Jul 2023 12:32:37 GMT  
		Size: 69.3 MB (69320403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43cf4a5de622c49ed3e252ac429a60fbbffc3b7d4a179b31bd5ebfa24469f62`  
		Last Modified: Tue, 04 Jul 2023 12:32:26 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780d6df591745d860fde3ab73e809a6c917ebdf70266f44ef74698e7feab9e68`  
		Last Modified: Tue, 11 Jul 2023 00:10:11 GMT  
		Size: 12.4 MB (12353012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d4550be153076ec6bd08b9a9dad2b751d9d0dcf2f8637a57b83955313090ae7`  
		Last Modified: Tue, 11 Jul 2023 00:10:10 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0e8d90d6225b8d3027a42c0081d4c788161cd3a369ff82d8598b5afe9427373`  
		Last Modified: Tue, 11 Jul 2023 00:11:00 GMT  
		Size: 24.3 MB (24250740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3718b7fef2807eea298fd115a056c83b791a4746c07b0fb9d1d1023e9c95f1d0`  
		Last Modified: Tue, 11 Jul 2023 00:10:56 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbcb269e245420f9da9de473dfc61006c5045483031d37d39ae931d4d831afeb`  
		Last Modified: Tue, 11 Jul 2023 00:10:56 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4373e6efb187ca6e6543c618f8209e254dd7a6a6e5ea54dc18f267b081cf24ee`  
		Last Modified: Tue, 11 Jul 2023 00:10:56 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe859ecb0e44390ad196a35b19db2b69e7fbf4fbdee19b83c77cfb7b596893e8`  
		Last Modified: Tue, 11 Jul 2023 03:21:51 GMT  
		Size: 15.9 MB (15869417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883c4478d5d58efb88253cc6a0d8947b3bd357e8f81ebef1c045e12923a7f47d`  
		Last Modified: Tue, 11 Jul 2023 03:21:48 GMT  
		Size: 3.4 MB (3411994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61a575fc165493f2a8fe377368ae0b820dedb409852e19b7b3e0fe2769e7eeb`  
		Last Modified: Tue, 11 Jul 2023 03:21:47 GMT  
		Size: 759.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef611fcff1639fe4cdd9fdb58df8e20fbcc36f4abe4e330d98764fe9f413922`  
		Last Modified: Tue, 11 Jul 2023 03:22:12 GMT  
		Size: 168.9 MB (168917172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e030d23f591d95163e91f704a08992fe146e6ac5d58db62e31d215e4659f8a6`  
		Last Modified: Tue, 11 Jul 2023 03:21:47 GMT  
		Size: 3.5 KB (3470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81c6b2b57db4a20ada489c2407245b991c6aaadf6271a492683836c43ee76eb1`  
		Last Modified: Tue, 11 Jul 2023 03:21:47 GMT  
		Size: 2.2 KB (2220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:production-fpm` - linux; arm64 variant v8

```console
$ docker pull nextcloud@sha256:8aff9e2b19daca1d58a3dd52056b648780c3dbb85632088a8203f2bf716398af
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.4 MB (346376775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d704c2b58a0ce32bb8683254f00452652f34c41a6d43e48b15d0d1310d74714`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 10:09:30 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 04 Jul 2023 10:09:30 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 04 Jul 2023 10:09:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 10:09:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 04 Jul 2023 10:09:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 04 Jul 2023 10:09:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Jul 2023 10:09:57 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Jul 2023 10:09:57 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 04 Jul 2023 10:36:56 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Mon, 10 Jul 2023 22:50:36 GMT
ENV PHP_VERSION=8.2.8
# Mon, 10 Jul 2023 22:50:36 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.8.tar.xz.asc
# Mon, 10 Jul 2023 22:50:36 GMT
ENV PHP_SHA256=cfe1055fbcd486de7d3312da6146949aae577365808790af6018205567609801
# Mon, 10 Jul 2023 22:50:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 10 Jul 2023 22:50:50 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Mon, 10 Jul 2023 22:59:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Mon, 10 Jul 2023 22:59:31 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Mon, 10 Jul 2023 22:59:32 GMT
RUN docker-php-ext-enable sodium
# Mon, 10 Jul 2023 22:59:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 10 Jul 2023 22:59:32 GMT
WORKDIR /var/www/html
# Mon, 10 Jul 2023 22:59:33 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Mon, 10 Jul 2023 22:59:33 GMT
STOPSIGNAL SIGQUIT
# Mon, 10 Jul 2023 22:59:33 GMT
EXPOSE 9000
# Mon, 10 Jul 2023 22:59:33 GMT
CMD ["php-fpm"]
# Tue, 11 Jul 2023 02:14:20 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Tue, 11 Jul 2023 02:14:20 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 11 Jul 2023 02:14:20 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 11 Jul 2023 02:16:50 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.22;     pecl install imagick-3.7.0;     pecl install memcached-3.2.0;     pecl install redis-5.3.7;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 02:16:51 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Tue, 11 Jul 2023 02:16:51 GMT
VOLUME [/var/www/html]
# Tue, 11 Jul 2023 02:16:51 GMT
ENV NEXTCLOUD_VERSION=26.0.3
# Tue, 11 Jul 2023 02:17:42 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-26.0.3.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-26.0.3.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 02:17:46 GMT
COPY multi:f14917ef3f8441cf73a9faa81b54c7e51061a07185e365974d47ddb315426c8f in / 
# Tue, 11 Jul 2023 02:17:46 GMT
COPY multi:1aa0c68034f207c7e2fb6f047fda45b55878afe2781ef10723107e35ee22547e in /usr/src/nextcloud/config/ 
# Tue, 11 Jul 2023 02:17:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 11 Jul 2023 02:17:46 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c3328f3ce997e7bc0f2b47ad766b6c760dd65095a9c1ad9090e66d25a90c09`  
		Last Modified: Tue, 04 Jul 2023 12:30:30 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30726b692873954b2e0584bc53be8a051244a3d0cfb76833bd6b2915f61e1588`  
		Last Modified: Tue, 04 Jul 2023 12:30:39 GMT  
		Size: 86.9 MB (86928257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2cfdeca8ab9e389a7c0e5b3a7cb7c02e9bd2fdf2a147dc8728c81065865a1f2`  
		Last Modified: Tue, 04 Jul 2023 12:30:29 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebc269b4ffa933a2cc8e47f5f75477e3087bc42a491b9496a73253fcc5278b2e`  
		Last Modified: Tue, 11 Jul 2023 00:33:28 GMT  
		Size: 12.4 MB (12353817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af15847c304de3fe8a4d97f4a01b8e3a2f22d0109f5dfbabe0d58ca813dcf501`  
		Last Modified: Tue, 11 Jul 2023 00:33:27 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88dba7b342a8ba5209cce11a9afdfdfad18ebf2ea68a071b1f82845021755226`  
		Last Modified: Tue, 11 Jul 2023 00:34:12 GMT  
		Size: 26.6 MB (26593794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:495aa3ec0cfdc4ab101083b92a745f9f901bc6fc7855f17532d77a637b0d5765`  
		Last Modified: Tue, 11 Jul 2023 00:34:09 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f78df806510b9594b3d043bd6a87bcb001d763142e9101439b8a132ef0b122`  
		Last Modified: Tue, 11 Jul 2023 00:34:08 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a585999980cb37e85a774a923019c44748de002ad45a283273fef8a4a779a3`  
		Last Modified: Tue, 11 Jul 2023 00:34:08 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a917d361c23c35d1c19304e1c98cae1649a4cb29a50d4b63505abc88b4b5a5ed`  
		Last Modified: Tue, 11 Jul 2023 02:27:23 GMT  
		Size: 17.2 MB (17188355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bae9c815d005f7f17abfb07cb5c056b4755ab49b1ee057420471a44c16e5c33`  
		Last Modified: Tue, 11 Jul 2023 02:27:20 GMT  
		Size: 4.3 MB (4312047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0dfdc86f0ca04ba138232285815c3e3752d7eb66a970abf79c904219a888a76`  
		Last Modified: Tue, 11 Jul 2023 02:27:19 GMT  
		Size: 756.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cda372a18edb1580ac2c11386fa9b2809e8292afe51f0a62c798169f72e1e0b`  
		Last Modified: Tue, 11 Jul 2023 02:27:35 GMT  
		Size: 168.9 MB (168918246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a449de9542e2ee0a2954206b09ed313b7a6c4fa260c707dc09e265f9bdbb8ee`  
		Last Modified: Tue, 11 Jul 2023 02:27:19 GMT  
		Size: 3.5 KB (3470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce09be07184daa05a0a28b8875ae9994296e980dca3d2abf6dc71f3b571b394d`  
		Last Modified: Tue, 11 Jul 2023 02:27:19 GMT  
		Size: 2.2 KB (2220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:production-fpm` - linux; 386

```console
$ docker pull nextcloud@sha256:0ff931a8821eb73a0a81be3081a1020c1b936d93e498a8cf5445fe9283288819
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.6 MB (356561387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48c632b1462cee5abbf7829fae95de26af0d6a7537b4ab3f93f24802cb342f7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 04 Jul 2023 01:38:59 GMT
ADD file:c39e332ccb9cb890ba7896a09e9f074b3c8d67094b4eaf73d5c67e8949c2e0be in / 
# Tue, 04 Jul 2023 01:39:00 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 14:55:16 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 04 Jul 2023 14:55:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 04 Jul 2023 14:55:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 14:55:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 04 Jul 2023 14:55:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 04 Jul 2023 14:55:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Jul 2023 14:55:42 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Jul 2023 14:55:42 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 04 Jul 2023 15:42:13 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Mon, 10 Jul 2023 21:35:49 GMT
ENV PHP_VERSION=8.2.8
# Mon, 10 Jul 2023 21:35:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.8.tar.xz.asc
# Mon, 10 Jul 2023 21:35:49 GMT
ENV PHP_SHA256=cfe1055fbcd486de7d3312da6146949aae577365808790af6018205567609801
# Mon, 10 Jul 2023 21:36:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 10 Jul 2023 21:36:05 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Mon, 10 Jul 2023 21:51:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Mon, 10 Jul 2023 21:51:32 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Mon, 10 Jul 2023 21:51:33 GMT
RUN docker-php-ext-enable sodium
# Mon, 10 Jul 2023 21:51:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 10 Jul 2023 21:51:33 GMT
WORKDIR /var/www/html
# Mon, 10 Jul 2023 21:51:33 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Mon, 10 Jul 2023 21:51:34 GMT
STOPSIGNAL SIGQUIT
# Mon, 10 Jul 2023 21:51:34 GMT
EXPOSE 9000
# Mon, 10 Jul 2023 21:51:34 GMT
CMD ["php-fpm"]
# Tue, 11 Jul 2023 01:16:03 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Tue, 11 Jul 2023 01:16:03 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 11 Jul 2023 01:16:03 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 11 Jul 2023 01:18:48 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.22;     pecl install imagick-3.7.0;     pecl install memcached-3.2.0;     pecl install redis-5.3.7;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 01:18:49 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Tue, 11 Jul 2023 01:18:49 GMT
VOLUME [/var/www/html]
# Tue, 11 Jul 2023 01:18:49 GMT
ENV NEXTCLOUD_VERSION=26.0.3
# Tue, 11 Jul 2023 01:19:50 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-26.0.3.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-26.0.3.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 01:19:54 GMT
COPY multi:f14917ef3f8441cf73a9faa81b54c7e51061a07185e365974d47ddb315426c8f in / 
# Tue, 11 Jul 2023 01:19:54 GMT
COPY multi:1aa0c68034f207c7e2fb6f047fda45b55878afe2781ef10723107e35ee22547e in /usr/src/nextcloud/config/ 
# Tue, 11 Jul 2023 01:19:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 11 Jul 2023 01:19:54 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:3466e7f9e8ec982697fc130dbb1706d708f5c53e348a638019a955c15c7395af`  
		Last Modified: Tue, 04 Jul 2023 01:44:12 GMT  
		Size: 32.4 MB (32397496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a522191f1e2738a8ed7b674328a98f04012963db292659f2f152ea8bc6a7f3f`  
		Last Modified: Tue, 04 Jul 2023 19:06:06 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a006b3de843c6964b852743273a0074a21907dedee23983faa87e9ff58abad4a`  
		Last Modified: Tue, 04 Jul 2023 19:06:26 GMT  
		Size: 92.7 MB (92720074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51e37b369620e6a54a25a7738bb74545560b7ea79a095943219dc22c2dd1636`  
		Last Modified: Tue, 04 Jul 2023 19:06:06 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc7ffacd0d8ece1fddc8723d7c9be5c9198806471e060d33a6b1ff85fb9638b`  
		Last Modified: Tue, 11 Jul 2023 00:30:15 GMT  
		Size: 12.4 MB (12353758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18137f43237fce0c0bde1de5c6a0cd94fdf7e41dfabfac893596058f5bb0bee7`  
		Last Modified: Tue, 11 Jul 2023 00:30:14 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d1eda1c6644d0540bd482a9ca666e4d40836e9d6be9ecd3f39b8cf362148ad1`  
		Last Modified: Tue, 11 Jul 2023 00:31:06 GMT  
		Size: 27.0 MB (27033225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7e08cd9e77fd9a2b1e4a631f14d5c0cbaa736f543231c1284a35f26ecc71e93`  
		Last Modified: Tue, 11 Jul 2023 00:31:01 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b3340f9453f5694923b588b11197844f2f5b77f9fa8bf2375140f6ae37752d7`  
		Last Modified: Tue, 11 Jul 2023 00:31:01 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a48919b9d5eb37d87d111b883d575b32d1cf2fe7cb665644a7e9aa3d46d17ddc`  
		Last Modified: Tue, 11 Jul 2023 00:31:01 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b69bc49d3609aebb7c656fef203200a067526a94eef7b3ea40d2217babd3a8b`  
		Last Modified: Tue, 11 Jul 2023 01:32:15 GMT  
		Size: 19.1 MB (19086311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761a273b4fcf7df4bec43f0d2a56171057fdc1295e78995eacd79374c96869b5`  
		Last Modified: Tue, 11 Jul 2023 01:32:10 GMT  
		Size: 4.0 MB (4033399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9f2c9ae7ef52a61502ae018e3d5dbc4a723f351369b0aec1f1e3b1cd117cabe`  
		Last Modified: Tue, 11 Jul 2023 01:32:09 GMT  
		Size: 762.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edcfc1ee384460ec78b7eec65df540fef2f94e7e1d7ffad1d11434ba93c5fa13`  
		Last Modified: Tue, 11 Jul 2023 01:32:41 GMT  
		Size: 168.9 MB (168917811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3c34beb4fe05809aa471313fad9433edc0f814b40f15c2cf50b3f2889bb7da`  
		Last Modified: Tue, 11 Jul 2023 01:32:09 GMT  
		Size: 3.5 KB (3469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7395e8078eeb8465d6f83d9ab9d32bc27648df9c6542c44705b4767a436f35a7`  
		Last Modified: Tue, 11 Jul 2023 01:32:09 GMT  
		Size: 2.2 KB (2220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:production-fpm` - linux; mips64le

```console
$ docker pull nextcloud@sha256:20726cc37fd349d9c8463ed0162f31f5b407284f7a31e557c6dd3e872373c6f7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.5 MB (328510454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69fff5f342555d79fdea44505b29e729cada10c04ad2ffa62dd67890df0fbc1d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 04 Jul 2023 01:10:44 GMT
ADD file:fa125b6265458c9912ef0f591e20d187cdc4b3a5222cb3f066e997a9baa4d699 in / 
# Tue, 04 Jul 2023 01:10:48 GMT
CMD ["bash"]
# Wed, 05 Jul 2023 03:09:33 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 05 Jul 2023 03:09:36 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 05 Jul 2023 03:11:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jul 2023 03:11:21 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 05 Jul 2023 03:11:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 05 Jul 2023 03:11:30 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Jul 2023 03:11:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Jul 2023 03:11:37 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 05 Jul 2023 05:17:54 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Mon, 10 Jul 2023 22:31:09 GMT
ENV PHP_VERSION=8.2.8
# Mon, 10 Jul 2023 22:31:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.8.tar.xz.asc
# Mon, 10 Jul 2023 22:31:16 GMT
ENV PHP_SHA256=cfe1055fbcd486de7d3312da6146949aae577365808790af6018205567609801
# Mon, 10 Jul 2023 22:32:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 10 Jul 2023 22:32:08 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Mon, 10 Jul 2023 23:14:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Mon, 10 Jul 2023 23:14:13 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Mon, 10 Jul 2023 23:14:18 GMT
RUN docker-php-ext-enable sodium
# Mon, 10 Jul 2023 23:14:21 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 10 Jul 2023 23:14:25 GMT
WORKDIR /var/www/html
# Mon, 10 Jul 2023 23:14:30 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Mon, 10 Jul 2023 23:14:33 GMT
STOPSIGNAL SIGQUIT
# Mon, 10 Jul 2023 23:14:37 GMT
EXPOSE 9000
# Mon, 10 Jul 2023 23:14:40 GMT
CMD ["php-fpm"]
# Tue, 11 Jul 2023 05:03:25 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Tue, 11 Jul 2023 05:03:28 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 11 Jul 2023 05:03:32 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 11 Jul 2023 05:14:13 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.22;     pecl install imagick-3.7.0;     pecl install memcached-3.2.0;     pecl install redis-5.3.7;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 05:14:20 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Tue, 11 Jul 2023 05:14:24 GMT
VOLUME [/var/www/html]
# Tue, 11 Jul 2023 05:14:28 GMT
ENV NEXTCLOUD_VERSION=26.0.3
# Tue, 11 Jul 2023 05:17:22 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-26.0.3.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-26.0.3.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 05:17:34 GMT
COPY multi:f14917ef3f8441cf73a9faa81b54c7e51061a07185e365974d47ddb315426c8f in / 
# Tue, 11 Jul 2023 05:17:43 GMT
COPY multi:1aa0c68034f207c7e2fb6f047fda45b55878afe2781ef10723107e35ee22547e in /usr/src/nextcloud/config/ 
# Tue, 11 Jul 2023 05:17:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 11 Jul 2023 05:18:00 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:5fa30c60fbae4cff4aa6f1626e53313c5fd7d3ed439bb87d067b66af6b1c07fd`  
		Last Modified: Tue, 04 Jul 2023 01:21:20 GMT  
		Size: 29.6 MB (29634364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c44299c512fc7c3b4ef5deea6c631da07e728f01ef59dd99f530be1a74ccb2`  
		Last Modified: Wed, 05 Jul 2023 13:26:08 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb6860f12e3795ea004540f55331d6c99e9e2bb59f3e5b57bf858ca56f618033`  
		Last Modified: Wed, 05 Jul 2023 13:26:59 GMT  
		Size: 71.8 MB (71815163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d5f6271fac28182afc4329f3f382212fc306029e84643cf1e084a7cf886a39`  
		Last Modified: Wed, 05 Jul 2023 13:26:07 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d38db22af618832261673f07c9db24f584898ca77d34d2ecc8030f2ec67a042f`  
		Last Modified: Tue, 11 Jul 2023 01:36:40 GMT  
		Size: 12.1 MB (12136287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a05777141ca39d45feaf700f86d5169fcd32535d19add912967c5fb295887e`  
		Last Modified: Tue, 11 Jul 2023 01:36:37 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb1c8daefa4d284623d5d50a9431b0954223892aaf2983603040ad772bd3f4c`  
		Last Modified: Tue, 11 Jul 2023 01:38:04 GMT  
		Size: 25.5 MB (25525183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee212e0f1be14b2e2b185ae816b0e869e90f1f7ec4bec25bc84cbd4a15878f9c`  
		Last Modified: Tue, 11 Jul 2023 01:37:49 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38043d3225c82a7e309e25b2a94c2f001133bd11dd823c27b7e651f44d51658a`  
		Last Modified: Tue, 11 Jul 2023 01:37:49 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad216365b717abf0df47e5f0ed9904a6f6e685a3993a572517a845d647b6656`  
		Last Modified: Tue, 11 Jul 2023 01:37:49 GMT  
		Size: 9.2 KB (9187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e23314bb97ef077e83d16a9dcd4f7bebba74b71e34cc1c9bbbc596f2d302ba`  
		Last Modified: Tue, 11 Jul 2023 05:33:45 GMT  
		Size: 17.3 MB (17312240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b0f1c8fd247f49f65194f64a4185aaa34c790698ca7387bafa7aa25117784b1`  
		Last Modified: Tue, 11 Jul 2023 05:33:36 GMT  
		Size: 3.4 MB (3394065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833bdb63fa2ce47a43580c98583f7582110566a77fcb35fb247630be90cd2319`  
		Last Modified: Tue, 11 Jul 2023 05:33:30 GMT  
		Size: 712.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8995fefb8eb51ca0b908ecc20ed50b46e5f42588f4cc614176b5540102df6b85`  
		Last Modified: Tue, 11 Jul 2023 05:35:17 GMT  
		Size: 168.7 MB (168673918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6cd19a468132751b36c49744a7b94458aa451f1ec9575a90896d0160dfe7109`  
		Last Modified: Tue, 11 Jul 2023 05:33:30 GMT  
		Size: 3.5 KB (3469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60b5f1c43478299abc936f1b23d7da8c90534bd16f4a076cc23cc891d6566d6`  
		Last Modified: Tue, 11 Jul 2023 05:33:30 GMT  
		Size: 2.2 KB (2222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:production-fpm` - linux; ppc64le

```console
$ docker pull nextcloud@sha256:c39903e7178497356968de3d8a24df54c4734130c8899cb0128f26252a8f6d3f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.4 MB (354413732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae7009cec3511716f3949e5ae7cff093d654013644896f2dc6de0e4a5278068c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 04 Jul 2023 01:18:33 GMT
ADD file:37fa020aca7253d41d395ed529c38db73caaa4da098754836244552f65fa7d5d in / 
# Tue, 04 Jul 2023 01:18:35 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 07:15:56 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 04 Jul 2023 07:15:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 04 Jul 2023 07:16:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 07:16:59 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 04 Jul 2023 07:17:01 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 04 Jul 2023 07:17:02 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Jul 2023 07:17:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Jul 2023 07:17:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 04 Jul 2023 08:12:09 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Mon, 10 Jul 2023 23:15:09 GMT
ENV PHP_VERSION=8.2.8
# Mon, 10 Jul 2023 23:15:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.8.tar.xz.asc
# Mon, 10 Jul 2023 23:15:10 GMT
ENV PHP_SHA256=cfe1055fbcd486de7d3312da6146949aae577365808790af6018205567609801
# Mon, 10 Jul 2023 23:15:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 10 Jul 2023 23:15:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Mon, 10 Jul 2023 23:29:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Mon, 10 Jul 2023 23:29:53 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Mon, 10 Jul 2023 23:29:55 GMT
RUN docker-php-ext-enable sodium
# Mon, 10 Jul 2023 23:29:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 10 Jul 2023 23:29:56 GMT
WORKDIR /var/www/html
# Mon, 10 Jul 2023 23:29:58 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Mon, 10 Jul 2023 23:29:58 GMT
STOPSIGNAL SIGQUIT
# Mon, 10 Jul 2023 23:29:59 GMT
EXPOSE 9000
# Mon, 10 Jul 2023 23:29:59 GMT
CMD ["php-fpm"]
# Tue, 11 Jul 2023 05:47:48 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Tue, 11 Jul 2023 05:47:50 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 11 Jul 2023 05:47:50 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 11 Jul 2023 05:53:25 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.22;     pecl install imagick-3.7.0;     pecl install memcached-3.2.0;     pecl install redis-5.3.7;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 05:53:27 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Tue, 11 Jul 2023 05:53:27 GMT
VOLUME [/var/www/html]
# Tue, 11 Jul 2023 05:53:28 GMT
ENV NEXTCLOUD_VERSION=26.0.3
# Tue, 11 Jul 2023 05:54:51 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-26.0.3.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-26.0.3.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Tue, 11 Jul 2023 05:55:00 GMT
COPY multi:f14917ef3f8441cf73a9faa81b54c7e51061a07185e365974d47ddb315426c8f in / 
# Tue, 11 Jul 2023 05:55:01 GMT
COPY multi:1aa0c68034f207c7e2fb6f047fda45b55878afe2781ef10723107e35ee22547e in /usr/src/nextcloud/config/ 
# Tue, 11 Jul 2023 05:55:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 11 Jul 2023 05:55:01 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:147bb8b5828c99cd6b07d252d2987490463c142099eaa0815025685f8fa4f3d8`  
		Last Modified: Tue, 04 Jul 2023 01:25:40 GMT  
		Size: 35.3 MB (35291082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4008b50277f3fc796cb78111576e1cc16705084a745cbe13aa78a920c63de829`  
		Last Modified: Tue, 04 Jul 2023 11:00:31 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e1a0e4bafc8d5664d51f0522c15e7928ea7ed2d9ced19a3c3db354c9354d8a`  
		Last Modified: Tue, 04 Jul 2023 11:00:55 GMT  
		Size: 86.6 MB (86634715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e7dcfbef24820d4d0817e454696ec2c86ae1563dafc34895489f6e41a94a8b`  
		Last Modified: Tue, 04 Jul 2023 11:00:31 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b1d69ed5d47a98e25fee2c3457302f4f7674fe70b61c784c9b672de6825e47d`  
		Last Modified: Tue, 11 Jul 2023 01:37:22 GMT  
		Size: 12.4 MB (12354477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:199bea462b87c2e09542bb0809e179dcc074be4d9b655b3fe59b19556ad4973a`  
		Last Modified: Tue, 11 Jul 2023 01:37:21 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd3d88716fd663ba3c2b033030875606d966c7c048ea0153eb091e8fd34a8d3f`  
		Last Modified: Tue, 11 Jul 2023 01:38:35 GMT  
		Size: 27.6 MB (27626952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6520d2233f49afbba2858ad1477d6463ca36df509bb0cd18732775334a25c2`  
		Last Modified: Tue, 11 Jul 2023 01:38:28 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44af64462ee870decb6c18bff319c0c866d52a07fbcfe055126526cdb7edafb9`  
		Last Modified: Tue, 11 Jul 2023 01:38:28 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f3e68fd23acb2c5fb1c2df03624a3d9d53c34019c18a1a16e0a6c0bc6b9fe8`  
		Last Modified: Tue, 11 Jul 2023 01:38:28 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea36193aec15fdb67bc57433efcb3ef62e132de3b53044228058893a1ea94a89`  
		Last Modified: Tue, 11 Jul 2023 06:10:31 GMT  
		Size: 19.7 MB (19664109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10cdcd0263fdd3e3bfb63420545c78b80db9e67ea1ccccfd2fd62552e6a6c53f`  
		Last Modified: Tue, 11 Jul 2023 06:10:25 GMT  
		Size: 3.9 MB (3903739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4368e78ad65e3fc2d64e12524bd85be3cd5a48e10f8c1c69f0d9409061d871b`  
		Last Modified: Tue, 11 Jul 2023 06:10:24 GMT  
		Size: 759.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39796972c93e2baf7e27cbec429bbd61a184f04a1d4fa4daf3c3643415b9859`  
		Last Modified: Tue, 11 Jul 2023 06:11:00 GMT  
		Size: 168.9 MB (168919346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d10c4a9b95629a25befb29b09a9e4310b58f668907a35b87fd988277cbf49f4`  
		Last Modified: Tue, 11 Jul 2023 06:10:24 GMT  
		Size: 3.5 KB (3470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f524d5fa09b8d6077ac8ad5b044bc31cf9d2b8e94249c37b065bffbfddbe53f`  
		Last Modified: Tue, 11 Jul 2023 06:10:24 GMT  
		Size: 2.2 KB (2222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:production-fpm` - linux; s390x

```console
$ docker pull nextcloud@sha256:d11ffdfb0eac7f788c0b50d18f1d16115cbdf8ec0617bd17889ed9b87ba7e965
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.0 MB (328994599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c02bd7e3272495538b54905fa87ca0c9466f70d2fa091cfd61e416514bea86b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 04 Jul 2023 01:32:44 GMT
ADD file:799c0afa70fa3bf4bb7804964481cba79e80aa3fad5c7a25beadde206ed6a8ff in / 
# Tue, 04 Jul 2023 01:32:46 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 10:30:04 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 04 Jul 2023 10:30:04 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 04 Jul 2023 10:30:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 10:30:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 04 Jul 2023 10:30:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 04 Jul 2023 10:30:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Jul 2023 10:30:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Jul 2023 10:30:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 04 Jul 2023 10:52:50 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Tue, 04 Jul 2023 11:15:22 GMT
ENV PHP_VERSION=8.2.7
# Tue, 04 Jul 2023 11:15:23 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.7.tar.xz.asc
# Tue, 04 Jul 2023 11:15:23 GMT
ENV PHP_SHA256=4b9fb3dcd7184fe7582d7e44544ec7c5153852a2528de3b6754791258ffbdfa0
# Tue, 04 Jul 2023 11:15:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 04 Jul 2023 11:15:33 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 04 Jul 2023 11:22:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 04 Jul 2023 11:22:41 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Tue, 04 Jul 2023 11:22:42 GMT
RUN docker-php-ext-enable sodium
# Tue, 04 Jul 2023 11:22:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 04 Jul 2023 11:22:42 GMT
WORKDIR /var/www/html
# Tue, 04 Jul 2023 11:22:42 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Tue, 04 Jul 2023 11:22:43 GMT
STOPSIGNAL SIGQUIT
# Tue, 04 Jul 2023 11:22:43 GMT
EXPOSE 9000
# Tue, 04 Jul 2023 11:22:43 GMT
CMD ["php-fpm"]
# Tue, 04 Jul 2023 17:45:43 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Tue, 04 Jul 2023 17:45:44 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 04 Jul 2023 17:45:44 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 04 Jul 2023 17:47:13 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.22;     pecl install imagick-3.7.0;     pecl install memcached-3.2.0;     pecl install redis-5.3.7;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 17:47:13 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Tue, 04 Jul 2023 17:47:13 GMT
VOLUME [/var/www/html]
# Tue, 04 Jul 2023 17:47:14 GMT
ENV NEXTCLOUD_VERSION=26.0.3
# Tue, 04 Jul 2023 17:50:16 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-26.0.3.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-26.0.3.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 17:50:26 GMT
COPY multi:f14917ef3f8441cf73a9faa81b54c7e51061a07185e365974d47ddb315426c8f in / 
# Tue, 04 Jul 2023 17:50:26 GMT
COPY multi:1aa0c68034f207c7e2fb6f047fda45b55878afe2781ef10723107e35ee22547e in /usr/src/nextcloud/config/ 
# Tue, 04 Jul 2023 17:50:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Jul 2023 17:50:26 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:bbee891481f2623da9c7d37a49947926519c858c2b06773370a6189440d4b4de`  
		Last Modified: Tue, 04 Jul 2023 01:37:37 GMT  
		Size: 29.7 MB (29652540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd328442d003020bede3c4c6597e95db31e93bb5a9266708b94d64c223b8439`  
		Last Modified: Tue, 04 Jul 2023 12:22:50 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3244c4a5c5675af046c9b96a90f0e48eb13ce1f372acefdfa4289f57b03b918`  
		Last Modified: Tue, 04 Jul 2023 12:23:00 GMT  
		Size: 71.6 MB (71629851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e5a674234138e2a62789138dad9371cd2c536308a8a25acaac16cdf9e4610f`  
		Last Modified: Tue, 04 Jul 2023 12:22:50 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aea13efa8728e8fde7abbebb2eda5c8835a81abb8ec6330ccb49e129e17d9de6`  
		Last Modified: Tue, 04 Jul 2023 12:27:04 GMT  
		Size: 12.3 MB (12335717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:258ff572bb322f037e55010111803742d4650e4593fa100f11215a4051c19c7f`  
		Last Modified: Tue, 04 Jul 2023 12:27:04 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d14e141694bfe1160b35120d537f04325ae5ac1f39ea47eac337da879a58a20`  
		Last Modified: Tue, 04 Jul 2023 12:27:34 GMT  
		Size: 25.6 MB (25577827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f65135f5d673f2d2e1f2e6741df11db435324779d9c2eeb502e04fdfd70d536a`  
		Last Modified: Tue, 04 Jul 2023 12:27:30 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae2188d5a21011bce03542549837e28e880f5f94c30bda30ef1e6ae42eb04d2`  
		Last Modified: Tue, 04 Jul 2023 12:27:30 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:766ecdb5bcd57c9017f7fdb90a21472f8aad00ecec2f2cdb88357a60cd532976`  
		Last Modified: Tue, 04 Jul 2023 12:27:30 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef82924d6289b8f4ac026cc8eb3c0db0a84b20f6c760e0b3ac3a48677f34adb6`  
		Last Modified: Tue, 04 Jul 2023 17:56:27 GMT  
		Size: 17.2 MB (17163870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cc99de9f32658c4ffcdb52037de91bf86bf4f0da440730e98ef196c075e81da`  
		Last Modified: Tue, 04 Jul 2023 17:56:24 GMT  
		Size: 3.7 MB (3697994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d3a233805cc488170b4393cc72d308e8d951c09396681f60d477ee70acdc69`  
		Last Modified: Tue, 04 Jul 2023 17:56:24 GMT  
		Size: 760.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb687a0aed7d7c8e41e2eb9589af70fa97d50d4c9e50c92582349f1f1d7b5b25`  
		Last Modified: Tue, 04 Jul 2023 17:56:43 GMT  
		Size: 168.9 MB (168917492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cdd8b292389ed8b3d79e31d7875439b5d19f1b4a5364cabdf34a46a8d6b58b0`  
		Last Modified: Tue, 04 Jul 2023 17:56:24 GMT  
		Size: 3.5 KB (3468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2fcb01f3948a81ad2a2a96b42a6f419b188de6411fbc08b9d961a8d77aff3ff`  
		Last Modified: Tue, 04 Jul 2023 17:56:24 GMT  
		Size: 2.2 KB (2222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
