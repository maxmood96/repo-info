## `nextcloud:28-fpm`

```console
$ docker pull nextcloud@sha256:e6edc90016d19ab9a1fb82e510bb6be909119efe1c7cbe77ce02b0a0843d3241
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

### `nextcloud:28-fpm` - linux; amd64

```console
$ docker pull nextcloud@sha256:80f784375c19ed21a27cdf661c2e38a8bcf7de682016293dec0999c3652eaba2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.8 MB (422821839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4fd3e504b0f8dc8139bdfd6ee9de9fd15bae6f4a5aa71c63cf01b343dd02d52`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:48 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
# Wed, 10 Apr 2024 01:50:48 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 09:54:38 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 10 Apr 2024 09:54:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 10 Apr 2024 09:55:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:55:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 10 Apr 2024 09:55:01 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 10 Apr 2024 09:55:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Apr 2024 09:55:01 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Apr 2024 09:55:01 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 10 Apr 2024 10:55:19 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 10 Apr 2024 11:24:21 GMT
ENV PHP_VERSION=8.2.17
# Wed, 10 Apr 2024 11:24:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.17.tar.xz.asc
# Wed, 10 Apr 2024 11:24:22 GMT
ENV PHP_SHA256=1cc4ef733ba58f6557db648012471f1916e5bac316303aa165535bedab08ee35
# Wed, 10 Apr 2024 11:24:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 10 Apr 2024 11:24:34 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 10 Apr 2024 11:35:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 10 Apr 2024 11:35:39 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 10 Apr 2024 11:35:40 GMT
RUN docker-php-ext-enable sodium
# Wed, 10 Apr 2024 11:35:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 10 Apr 2024 11:35:40 GMT
WORKDIR /var/www/html
# Wed, 10 Apr 2024 11:35:41 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 10 Apr 2024 11:35:41 GMT
STOPSIGNAL SIGQUIT
# Wed, 10 Apr 2024 11:35:41 GMT
EXPOSE 9000
# Wed, 10 Apr 2024 11:35:41 GMT
CMD ["php-fpm"]
# Wed, 10 Apr 2024 18:45:04 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Wed, 10 Apr 2024 18:45:05 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 10 Apr 2024 18:45:05 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 10 Apr 2024 18:47:55 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.23;     pecl install imagick-3.7.0;     pecl install memcached-3.2.0;     pecl install redis-6.0.2;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 18:47:56 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Wed, 10 Apr 2024 18:47:56 GMT
VOLUME [/var/www/html]
# Wed, 10 Apr 2024 18:52:38 GMT
ENV NEXTCLOUD_VERSION=28.0.4
# Wed, 10 Apr 2024 18:53:41 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-28.0.4.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-28.0.4.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 18:53:43 GMT
COPY multi:9585a9602f24ff6c37b7e8821d7e5fca4a450cd9cc8c66163bc629028ca3df5c in / 
# Wed, 10 Apr 2024 18:53:44 GMT
COPY multi:78125c707b59ef0f6f1ecce97806e1bec0bbbd71be245d580e78e8ceb5133056 in /usr/src/nextcloud/config/ 
# Wed, 10 Apr 2024 18:53:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 18:53:44 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ea9cef6db5ae39468fddf65e05346ec1b672585e014df044d40c60c280f4af6`  
		Last Modified: Wed, 10 Apr 2024 12:25:27 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff65b997523ed8926becf7a45fbeab5cc1741dea6f7be0c518e8f7e6294201c8`  
		Last Modified: Wed, 10 Apr 2024 12:25:42 GMT  
		Size: 104.4 MB (104355298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46d87a00aaae1ae22413715f1cacb07a29aa3dfb4fd90561b2966e73bd2efbc8`  
		Last Modified: Wed, 10 Apr 2024 12:25:27 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b6ff750e2cad7eca97a92c8787bf943cc8afa5610f674c02bd09add07be52e`  
		Last Modified: Wed, 10 Apr 2024 12:33:47 GMT  
		Size: 12.4 MB (12406505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe8f0077ca2dcf1057c3b931c605b73726acc9a8241fd0a30a7e7444972590b`  
		Last Modified: Wed, 10 Apr 2024 12:33:46 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b70c2810ada07a8fbd2a01b950544840e972d1c1ffa5dc345fc86ddcc815cee3`  
		Last Modified: Wed, 10 Apr 2024 12:34:31 GMT  
		Size: 27.8 MB (27775715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4693fe6035102576b284099b58c3c2b356cb8acded547bfa585621b6f1cb25c`  
		Last Modified: Wed, 10 Apr 2024 12:34:27 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9db8b4721046178c49ac7e37c88b368a00ed12e945a1c569e75c213096780c`  
		Last Modified: Wed, 10 Apr 2024 12:34:27 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f662136a90da2259cd2d6d2acaa35e4611bff9a07f450ec9bcf0ce6e5d417eae`  
		Last Modified: Wed, 10 Apr 2024 12:34:27 GMT  
		Size: 9.2 KB (9185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:507a27ba7f98d412c0f750c8e8937adadc3309f40149e748cfee890bcbeb31c3`  
		Last Modified: Wed, 10 Apr 2024 18:55:01 GMT  
		Size: 22.9 MB (22881538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a98172e777dbe93fb0857647810eaf3ab2a34ef0b2bcb9ec18bea4a5747899f`  
		Last Modified: Wed, 10 Apr 2024 18:54:59 GMT  
		Size: 21.1 MB (21099983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3281a73bf20d924ec36fc0cb79f47137c0504e2ce731ed13f60e4ec800b6c34`  
		Last Modified: Wed, 10 Apr 2024 18:54:56 GMT  
		Size: 759.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed320c74dc1f4fdfc142e4be851135999341fd6aa8240f5672203c97e0878b6`  
		Last Modified: Wed, 10 Apr 2024 18:58:26 GMT  
		Size: 205.2 MB (205151855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f1b4bc43094b1dfa048ccd599917ef9f20ab5b362bd17b2abdbd5c8758f499a`  
		Last Modified: Wed, 10 Apr 2024 18:58:01 GMT  
		Size: 3.6 KB (3614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b4cbef37d3c3d10a9936caa7a78893b32ebe65401663570e9dc02dd12c8091`  
		Last Modified: Wed, 10 Apr 2024 18:58:02 GMT  
		Size: 2.3 KB (2338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:28-fpm` - linux; arm variant v5

```console
$ docker pull nextcloud@sha256:bc03d5dd5b14fe0567beb44e785be54fc0e1c9814a7184a2e3118841be1c27b7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.5 MB (392504934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4233c2c09ebafa2cb2b99cea8617d521da7ea905ea9ab14091e8f351bc7d6104`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 10 Apr 2024 00:49:04 GMT
ADD file:bfe2e0ed45dd2920845bd9283b7d13266c82fe9f48ba261b6529c28dc246d3e4 in / 
# Wed, 10 Apr 2024 00:49:04 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:40:50 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 10 Apr 2024 06:40:50 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 10 Apr 2024 06:41:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:41:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 10 Apr 2024 06:41:30 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 10 Apr 2024 06:41:30 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Apr 2024 06:41:30 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Apr 2024 06:41:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 10 Apr 2024 08:19:13 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 10 Apr 2024 09:13:09 GMT
ENV PHP_VERSION=8.2.17
# Wed, 10 Apr 2024 09:13:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.17.tar.xz.asc
# Wed, 10 Apr 2024 09:13:09 GMT
ENV PHP_SHA256=1cc4ef733ba58f6557db648012471f1916e5bac316303aa165535bedab08ee35
# Wed, 10 Apr 2024 09:13:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 10 Apr 2024 09:13:28 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 10 Apr 2024 09:34:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 10 Apr 2024 09:34:31 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 10 Apr 2024 09:34:33 GMT
RUN docker-php-ext-enable sodium
# Wed, 10 Apr 2024 09:34:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 10 Apr 2024 09:34:33 GMT
WORKDIR /var/www/html
# Wed, 10 Apr 2024 09:34:34 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 10 Apr 2024 09:34:34 GMT
STOPSIGNAL SIGQUIT
# Wed, 10 Apr 2024 09:34:35 GMT
EXPOSE 9000
# Wed, 10 Apr 2024 09:34:35 GMT
CMD ["php-fpm"]
# Wed, 10 Apr 2024 15:49:31 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Wed, 10 Apr 2024 15:49:31 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 10 Apr 2024 15:49:31 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 10 Apr 2024 15:51:59 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.23;     pecl install imagick-3.7.0;     pecl install memcached-3.2.0;     pecl install redis-6.0.2;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 15:52:00 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Wed, 10 Apr 2024 15:52:00 GMT
VOLUME [/var/www/html]
# Wed, 10 Apr 2024 15:57:20 GMT
ENV NEXTCLOUD_VERSION=28.0.4
# Wed, 10 Apr 2024 15:58:31 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-28.0.4.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-28.0.4.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 15:58:36 GMT
COPY multi:9585a9602f24ff6c37b7e8821d7e5fca4a450cd9cc8c66163bc629028ca3df5c in / 
# Wed, 10 Apr 2024 15:58:36 GMT
COPY multi:78125c707b59ef0f6f1ecce97806e1bec0bbbd71be245d580e78e8ceb5133056 in /usr/src/nextcloud/config/ 
# Wed, 10 Apr 2024 15:58:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 15:58:37 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:60d288182f6883c1ed662f82d32316348aac8ca45c943f1093aed5c0ed01b45c`  
		Last Modified: Wed, 10 Apr 2024 00:54:34 GMT  
		Size: 26.9 MB (26890564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fad62fa190e47c7d0b669199b1248bb9f5603827fcbbaa1c754b0c75c725f43a`  
		Last Modified: Wed, 10 Apr 2024 11:07:12 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a47d3b8c72ce4af4ce7f47cc2abfe2ee828d22277abab63e12835ec08470b43`  
		Last Modified: Wed, 10 Apr 2024 11:07:35 GMT  
		Size: 82.0 MB (81999426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1451f776953297b40a2d209e77a10c6bf244b0b4709a923151a72d03f8e47452`  
		Last Modified: Wed, 10 Apr 2024 11:07:12 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6bbaac65f23f8d4abe9dc6d510b7bba4c16757222360bfaa252ded19c2986d2`  
		Last Modified: Wed, 10 Apr 2024 11:16:38 GMT  
		Size: 12.4 MB (12404465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bdf288d27c7157161c77539b4827d70fece667f4c47f87ba256b14282f15621`  
		Last Modified: Wed, 10 Apr 2024 11:16:36 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed58abc77ec0f397c54ea0a9333c434e436e15443159e43ddb8af9fb42d33b04`  
		Last Modified: Wed, 10 Apr 2024 11:17:30 GMT  
		Size: 26.3 MB (26275727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1de30d0baf455d999c3529bd475b8b3ec6b8392d4dfc0d30b23b4c264e715b`  
		Last Modified: Wed, 10 Apr 2024 11:17:24 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdaa671809d0f4e539ed0b9b51a2bc73dbb3834231694b482777148ae909f7ca`  
		Last Modified: Wed, 10 Apr 2024 11:17:24 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7207370b130eba3f6abca8c869f754d8306bf357dc8b89b8c725ea710833db53`  
		Last Modified: Wed, 10 Apr 2024 11:17:24 GMT  
		Size: 9.2 KB (9185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93dab61c1e1e040390bcd267acefbb73cf9dc8ed15db58750c4dcda323225536`  
		Last Modified: Wed, 10 Apr 2024 16:00:13 GMT  
		Size: 20.0 MB (19993941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fce11924f69136e442d3a9a9cdc923e86c9daa7b53abc5a56490991003120212`  
		Last Modified: Wed, 10 Apr 2024 16:00:13 GMT  
		Size: 19.8 MB (19771839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55ed5233becc0f6cc86da80f25823d8b8028a7d0a7f389fbee7d689163cd3c83`  
		Last Modified: Wed, 10 Apr 2024 16:00:06 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a553726b2e7d94bb35d854df1ca3bd8f0f069a5347184413d428dd63a92cd31`  
		Last Modified: Wed, 10 Apr 2024 16:04:36 GMT  
		Size: 205.1 MB (205149381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e93fad897ea35a8bdd09a18d2cf759c738f2ed1e17b85ef2546d25a6a905f332`  
		Last Modified: Wed, 10 Apr 2024 16:04:05 GMT  
		Size: 3.6 KB (3613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8eb76372598cfb82034e45c56a50c32d90ae6920093ec5f1d5f2d1f972fdd48`  
		Last Modified: Wed, 10 Apr 2024 16:04:04 GMT  
		Size: 2.3 KB (2337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:28-fpm` - linux; arm variant v7

```console
$ docker pull nextcloud@sha256:b5f57f1298b2ed58a02d16b80c498c8a529b91a8b8a14d8914424af69015c759
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.2 MB (381160863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b442e6297e97b0f0eb3e0a09dffd7c7210782b0f3b42531dd6b3cb3b71e0dcd8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 10 Apr 2024 00:58:11 GMT
ADD file:405264a6fec3e83d872f4297605fa82dd8f7a7724cbccbb7ebf06438266aa933 in / 
# Wed, 10 Apr 2024 00:58:12 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 11:41:42 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 10 Apr 2024 11:41:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 10 Apr 2024 11:42:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 11:42:19 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 10 Apr 2024 11:42:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 10 Apr 2024 11:42:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Apr 2024 11:42:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Apr 2024 11:42:21 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 10 Apr 2024 13:32:05 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 10 Apr 2024 14:24:47 GMT
ENV PHP_VERSION=8.2.17
# Wed, 10 Apr 2024 14:24:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.17.tar.xz.asc
# Wed, 10 Apr 2024 14:24:48 GMT
ENV PHP_SHA256=1cc4ef733ba58f6557db648012471f1916e5bac316303aa165535bedab08ee35
# Wed, 10 Apr 2024 14:25:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 10 Apr 2024 14:25:05 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 10 Apr 2024 14:35:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 10 Apr 2024 14:35:47 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 10 Apr 2024 14:35:47 GMT
RUN docker-php-ext-enable sodium
# Wed, 10 Apr 2024 14:35:47 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 10 Apr 2024 14:35:47 GMT
WORKDIR /var/www/html
# Wed, 10 Apr 2024 14:35:48 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 10 Apr 2024 14:35:48 GMT
STOPSIGNAL SIGQUIT
# Wed, 10 Apr 2024 14:35:48 GMT
EXPOSE 9000
# Wed, 10 Apr 2024 14:35:48 GMT
CMD ["php-fpm"]
# Wed, 10 Apr 2024 23:39:34 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Wed, 10 Apr 2024 23:39:35 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 10 Apr 2024 23:39:35 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 10 Apr 2024 23:42:23 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.23;     pecl install imagick-3.7.0;     pecl install memcached-3.2.0;     pecl install redis-6.0.2;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 23:42:24 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Wed, 10 Apr 2024 23:42:24 GMT
VOLUME [/var/www/html]
# Wed, 10 Apr 2024 23:48:36 GMT
ENV NEXTCLOUD_VERSION=28.0.4
# Wed, 10 Apr 2024 23:50:07 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-28.0.4.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-28.0.4.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 23:50:09 GMT
COPY multi:9585a9602f24ff6c37b7e8821d7e5fca4a450cd9cc8c66163bc629028ca3df5c in / 
# Wed, 10 Apr 2024 23:50:11 GMT
COPY multi:78125c707b59ef0f6f1ecce97806e1bec0bbbd71be245d580e78e8ceb5133056 in /usr/src/nextcloud/config/ 
# Wed, 10 Apr 2024 23:50:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 23:50:12 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c774609c4cd3f6537d30d03e0ad1c935b83618698a710164c43debe51dadfd87`  
		Last Modified: Wed, 10 Apr 2024 01:04:25 GMT  
		Size: 24.7 MB (24722923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ee1195c94850562f1733f5b87b30bcfc56b0d97b73c92fd2dddaec1a8fabc3`  
		Last Modified: Wed, 10 Apr 2024 15:49:11 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:726ef34ac105ce4f5566a2059d21267972e2f14880d04d22f096516b9778f788`  
		Last Modified: Wed, 10 Apr 2024 15:49:23 GMT  
		Size: 76.2 MB (76169814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edcd3deb16d20ecb363e17df9fa908c73080267e98a7e7a701541dabc5264993`  
		Last Modified: Wed, 10 Apr 2024 15:49:09 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd396d180a8d5fa54a8b8e64802ac18ef7f81c4ca67e91325e234b28baa05d5`  
		Last Modified: Wed, 10 Apr 2024 15:57:58 GMT  
		Size: 12.4 MB (12404467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1310a81af49cb08c114682f430afd71cc759b01a0a1473a86270985b5754dca5`  
		Last Modified: Wed, 10 Apr 2024 15:57:57 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ff57cfaa9bd7ab59f434e1578b6cdadb9d535d1124e4a60acad2c38258ddd9e`  
		Last Modified: Wed, 10 Apr 2024 15:58:46 GMT  
		Size: 25.4 MB (25387313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:390ac215ab0ccb5e1b9331e10a61716762ad82d49e3906194eb7363092dd0bf0`  
		Last Modified: Wed, 10 Apr 2024 15:58:40 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4af8d06ca7280d80557f10750153044a9520d37292352709fab8cbc1062c2bd`  
		Last Modified: Wed, 10 Apr 2024 15:58:40 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba5244b5ac9e9e5518b4e5fdbd71f121aae5072c3e3acf4f13bcf789b1346ba`  
		Last Modified: Wed, 10 Apr 2024 15:58:40 GMT  
		Size: 9.2 KB (9185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b13e958186cf2c3daf120d80ba15bf372a50549bb3bbe5234fae7b974e1098cf`  
		Last Modified: Wed, 10 Apr 2024 23:52:13 GMT  
		Size: 18.2 MB (18227640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04d74d9ed1c86050d7211ef11ddf8361db70dd4cc1d26b815de315e63e5ca09e`  
		Last Modified: Wed, 10 Apr 2024 23:52:16 GMT  
		Size: 19.1 MB (19079569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1abca44345e046ea0c392bd0d180cf740b21cf0207d84983a2ebe8a4149b3736`  
		Last Modified: Wed, 10 Apr 2024 23:52:06 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0461bd84c34c5a6a9c6430fca7ec0bd3ae48ef249487b644ca205e287cb67b6e`  
		Last Modified: Wed, 10 Apr 2024 23:57:45 GMT  
		Size: 205.1 MB (205149544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b2715259a35b2ce000515842ac650b79c9d3d9c82f31960908fb3e9022c0ff`  
		Last Modified: Wed, 10 Apr 2024 23:57:03 GMT  
		Size: 3.6 KB (3613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73336fc31ffc63c2e9478575060caa2ad6bf1c38a7ed654abee3df6328adabe9`  
		Last Modified: Wed, 10 Apr 2024 23:57:03 GMT  
		Size: 2.3 KB (2336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:28-fpm` - linux; arm64 variant v8

```console
$ docker pull nextcloud@sha256:de500b7fdf91a45ea86c49fb64af016fadfdda696a82c6c78e5b2265cda61e0e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.2 MB (414182611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c6b70f6f42387f9b62800ab434369ca1957d7ae9507a80864d238e35251f8e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:23 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Wed, 10 Apr 2024 00:40:23 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:43:00 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 10 Apr 2024 07:43:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 10 Apr 2024 07:43:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:43:19 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 10 Apr 2024 07:43:19 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 10 Apr 2024 07:43:19 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Apr 2024 07:43:19 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Apr 2024 07:43:20 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 10 Apr 2024 08:41:31 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 10 Apr 2024 09:08:02 GMT
ENV PHP_VERSION=8.2.17
# Wed, 10 Apr 2024 09:08:02 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.17.tar.xz.asc
# Wed, 10 Apr 2024 09:08:02 GMT
ENV PHP_SHA256=1cc4ef733ba58f6557db648012471f1916e5bac316303aa165535bedab08ee35
# Wed, 10 Apr 2024 09:08:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 10 Apr 2024 09:08:13 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 10 Apr 2024 09:18:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 10 Apr 2024 09:18:34 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 10 Apr 2024 09:18:34 GMT
RUN docker-php-ext-enable sodium
# Wed, 10 Apr 2024 09:18:35 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 10 Apr 2024 09:18:35 GMT
WORKDIR /var/www/html
# Wed, 10 Apr 2024 09:18:35 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 10 Apr 2024 09:18:35 GMT
STOPSIGNAL SIGQUIT
# Wed, 10 Apr 2024 09:18:35 GMT
EXPOSE 9000
# Wed, 10 Apr 2024 09:18:35 GMT
CMD ["php-fpm"]
# Wed, 10 Apr 2024 14:45:30 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Wed, 10 Apr 2024 14:45:30 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 10 Apr 2024 14:45:30 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 10 Apr 2024 14:48:32 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.23;     pecl install imagick-3.7.0;     pecl install memcached-3.2.0;     pecl install redis-6.0.2;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 14:48:33 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Wed, 10 Apr 2024 14:48:33 GMT
VOLUME [/var/www/html]
# Wed, 10 Apr 2024 14:53:14 GMT
ENV NEXTCLOUD_VERSION=28.0.4
# Wed, 10 Apr 2024 14:54:12 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-28.0.4.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-28.0.4.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 14:54:17 GMT
COPY multi:9585a9602f24ff6c37b7e8821d7e5fca4a450cd9cc8c66163bc629028ca3df5c in / 
# Wed, 10 Apr 2024 14:54:17 GMT
COPY multi:78125c707b59ef0f6f1ecce97806e1bec0bbbd71be245d580e78e8ceb5133056 in /usr/src/nextcloud/config/ 
# Wed, 10 Apr 2024 14:54:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 14:54:17 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2633671d3fa6d324767f0bccbf66f1d2c638759d9ab02502e5c471b27f381b42`  
		Last Modified: Wed, 10 Apr 2024 10:03:13 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62e0fda5a8219f239a7c88d867bbdb13b7bd0e1e3f84ac14cf037b9eaf0260a4`  
		Last Modified: Wed, 10 Apr 2024 10:03:24 GMT  
		Size: 98.1 MB (98126521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:594d5d6c1ef842e0a902c5f1bab3c7e92b482d32566a66b64777cd088c736c7a`  
		Last Modified: Wed, 10 Apr 2024 10:03:13 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317a5a451e5a5460a578fbcfec97f2758dfd9d405e17092b3796dcfc80361002`  
		Last Modified: Wed, 10 Apr 2024 10:11:17 GMT  
		Size: 12.4 MB (12406358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4dcae673d38e8d07d908d04feceee05f6c4faf06b212aaeed4f62a6e9fa4446`  
		Last Modified: Wed, 10 Apr 2024 10:11:16 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a26eabf3d84c38c0848277f28b902953bd103215c202830fe44be9fd56305b3`  
		Last Modified: Wed, 10 Apr 2024 10:11:59 GMT  
		Size: 27.7 MB (27734004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64980e66d9ba243f54166810b9ade5e86b9d61b789877ff90ceef13b97fb6710`  
		Last Modified: Wed, 10 Apr 2024 10:11:56 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e97b55ae1699a738a3698461107fbe8ff7164a2b6eb4d829cb093f8a1a389d8`  
		Last Modified: Wed, 10 Apr 2024 10:11:56 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee8cf044b931b45ce6579f08cc3e2f37e25be009dee88173eedd2b93a0d2739`  
		Last Modified: Wed, 10 Apr 2024 10:11:56 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00aeaafc840959d184cb0152f476c36f067c817b96657889be971cb570c4ce24`  
		Last Modified: Wed, 10 Apr 2024 14:55:30 GMT  
		Size: 20.3 MB (20258071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e6e057a30b843519db301eeb49386bbe93005df6630390f87578103c5c31033`  
		Last Modified: Wed, 10 Apr 2024 14:55:28 GMT  
		Size: 21.3 MB (21324341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b67b89e9f52091d469bf714b843158e843fb582a6dea1655771818e466530f27`  
		Last Modified: Wed, 10 Apr 2024 14:55:25 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5684970d2f39a101ce01e7f4c269a8947c3899643cf24f8fffb214aab4b129c7`  
		Last Modified: Wed, 10 Apr 2024 14:58:32 GMT  
		Size: 205.2 MB (205151577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c14cd67b07877c9ba6e8d638a575d24d06ba6da5882d1c535809f6c9e9479f2`  
		Last Modified: Wed, 10 Apr 2024 14:58:12 GMT  
		Size: 3.6 KB (3613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1a877d720c1bee0c7a1c9d38f88d0ccc194f4f654577033a4859ef2cfb33898`  
		Last Modified: Wed, 10 Apr 2024 14:58:12 GMT  
		Size: 2.3 KB (2336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:28-fpm` - linux; 386

```console
$ docker pull nextcloud@sha256:2cc667ed025e4b59f185ff932813218c3aa7d66151f29dc59ae8f9278863395d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **421.3 MB (421254081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8973fffbe51a62b455a30a66e70ddd83847dc652421e36b28b1f6f3959c1a03`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 10 Apr 2024 00:57:11 GMT
ADD file:d160efeeb02e2200784dd8312a13a11d9d791581efc7756ed999f76c79445b54 in / 
# Wed, 10 Apr 2024 00:57:11 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 11:45:04 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 10 Apr 2024 11:45:04 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 10 Apr 2024 11:45:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 11:45:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 10 Apr 2024 11:45:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 10 Apr 2024 11:45:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Apr 2024 11:45:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Apr 2024 11:45:35 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 10 Apr 2024 13:28:26 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 10 Apr 2024 14:18:16 GMT
ENV PHP_VERSION=8.2.17
# Wed, 10 Apr 2024 14:18:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.17.tar.xz.asc
# Wed, 10 Apr 2024 14:18:16 GMT
ENV PHP_SHA256=1cc4ef733ba58f6557db648012471f1916e5bac316303aa165535bedab08ee35
# Wed, 10 Apr 2024 14:18:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 10 Apr 2024 14:18:31 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 10 Apr 2024 14:38:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 10 Apr 2024 14:38:07 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 10 Apr 2024 14:38:08 GMT
RUN docker-php-ext-enable sodium
# Wed, 10 Apr 2024 14:38:08 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 10 Apr 2024 14:38:08 GMT
WORKDIR /var/www/html
# Wed, 10 Apr 2024 14:38:08 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 10 Apr 2024 14:38:08 GMT
STOPSIGNAL SIGQUIT
# Wed, 10 Apr 2024 14:38:09 GMT
EXPOSE 9000
# Wed, 10 Apr 2024 14:38:09 GMT
CMD ["php-fpm"]
# Wed, 10 Apr 2024 20:13:03 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Wed, 10 Apr 2024 20:13:04 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 10 Apr 2024 20:13:04 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 10 Apr 2024 20:16:56 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.23;     pecl install imagick-3.7.0;     pecl install memcached-3.2.0;     pecl install redis-6.0.2;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 20:16:57 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Wed, 10 Apr 2024 20:16:57 GMT
VOLUME [/var/www/html]
# Wed, 10 Apr 2024 20:23:26 GMT
ENV NEXTCLOUD_VERSION=28.0.4
# Wed, 10 Apr 2024 20:24:47 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-28.0.4.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-28.0.4.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 20:24:51 GMT
COPY multi:9585a9602f24ff6c37b7e8821d7e5fca4a450cd9cc8c66163bc629028ca3df5c in / 
# Wed, 10 Apr 2024 20:24:52 GMT
COPY multi:78125c707b59ef0f6f1ecce97806e1bec0bbbd71be245d580e78e8ceb5133056 in /usr/src/nextcloud/config/ 
# Wed, 10 Apr 2024 20:24:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 20:24:52 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:8a3830119a16769024de35d2dfa3d32147da5ea747ec336166bdca1049655803`  
		Last Modified: Wed, 10 Apr 2024 01:02:04 GMT  
		Size: 30.1 MB (30146515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c09ef08c63f65c53bebb8d9c9ab11116ced4413de8735933ca362f298edaba98`  
		Last Modified: Wed, 10 Apr 2024 16:00:50 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60e903bb01a30db718f8e6cfbc041db1ceda75766a754906ac45dcac72915d98`  
		Last Modified: Wed, 10 Apr 2024 16:01:13 GMT  
		Size: 101.5 MB (101519808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:447b37792cd88a52c3152c993c59946a9d84e2467ff7e7661e565ba2f3b6665a`  
		Last Modified: Wed, 10 Apr 2024 16:00:49 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0246ac4b53528a115b27c598c6f884f492e9490dcabee11b36365c0976b1c12`  
		Last Modified: Wed, 10 Apr 2024 16:11:18 GMT  
		Size: 12.4 MB (12405673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41851838b2ec4fdb927d7e3be29ada0f6b3bf289ef4c64f5ec1401148c7c32d1`  
		Last Modified: Wed, 10 Apr 2024 16:11:17 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13af37df740139f39e11a9565cd24321d65a7cd84bc343eaa96ddcb3364b07f7`  
		Last Modified: Wed, 10 Apr 2024 16:12:22 GMT  
		Size: 28.3 MB (28294329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96c66ac73a69adb5adbcbbda585c88ea40df8b287a2e11884ca01fc2d0033a4b`  
		Last Modified: Wed, 10 Apr 2024 16:12:15 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9efb419a6944d3b2edf94c684ecf5920c09be9f330ab3f161d0443a65650cfd`  
		Last Modified: Wed, 10 Apr 2024 16:12:15 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69aa08cd3d70f042d947a569b77795115d7d6eb9ec67f0005fea590df4dfce45`  
		Last Modified: Wed, 10 Apr 2024 16:12:15 GMT  
		Size: 9.2 KB (9183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0fa3be23047046a21f6f68d2a2b3e3a83509c97f7c5490ca624e457b3e6dce`  
		Last Modified: Wed, 10 Apr 2024 20:26:43 GMT  
		Size: 22.4 MB (22380641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eed02e92a0af113cd76e416e4b33adcb9dbc663584556841daeb79ef0f0c5fd`  
		Last Modified: Wed, 10 Apr 2024 20:26:41 GMT  
		Size: 21.3 MB (21336656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9a3f6b0a4df70fc5e390e0017f3f6382b45939fed7ae9209b35ac6f395a6c77`  
		Last Modified: Wed, 10 Apr 2024 20:26:34 GMT  
		Size: 757.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:230b54a84fb9e8847c65e8a348aa9d790b08127fcdea50fd0cca871c461c51da`  
		Last Modified: Wed, 10 Apr 2024 20:31:25 GMT  
		Size: 205.2 MB (205150890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c966eb1d0b96833b0330fbfb0136033338bd4b4195c844c6e865b73406efca34`  
		Last Modified: Wed, 10 Apr 2024 20:30:45 GMT  
		Size: 3.6 KB (3613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf7193090f3f52b720869d6ef0d5011016f40bb3c3d6492380b9ba01f7d0babc`  
		Last Modified: Wed, 10 Apr 2024 20:30:45 GMT  
		Size: 2.3 KB (2333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:28-fpm` - linux; mips64le

```console
$ docker pull nextcloud@sha256:0515f3461eae116a138a45e4b5b7d94d09dc194474277bd92a53b63251e10f30
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.2 MB (394185595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2b13c78582b41325a7afb933cd1a91b686d2a6626b9d930fee6441380540881`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 10 Apr 2024 01:10:04 GMT
ADD file:c07831a1f2abb22986c788bb198b484a259e7e68ee8b03da0daeb4b41d8d83ce in / 
# Wed, 10 Apr 2024 01:10:09 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:24:20 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 10 Apr 2024 04:24:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 10 Apr 2024 04:26:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 04:26:10 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 10 Apr 2024 04:26:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 10 Apr 2024 04:26:19 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Apr 2024 04:26:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Apr 2024 04:26:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 10 Apr 2024 08:37:57 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 10 Apr 2024 10:39:05 GMT
ENV PHP_VERSION=8.2.17
# Wed, 10 Apr 2024 10:39:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.17.tar.xz.asc
# Wed, 10 Apr 2024 10:39:12 GMT
ENV PHP_SHA256=1cc4ef733ba58f6557db648012471f1916e5bac316303aa165535bedab08ee35
# Wed, 10 Apr 2024 10:40:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 10 Apr 2024 10:40:09 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 10 Apr 2024 11:26:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 10 Apr 2024 11:26:33 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 10 Apr 2024 11:26:39 GMT
RUN docker-php-ext-enable sodium
# Wed, 10 Apr 2024 11:26:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 10 Apr 2024 11:26:46 GMT
WORKDIR /var/www/html
# Wed, 10 Apr 2024 11:26:52 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 10 Apr 2024 11:26:56 GMT
STOPSIGNAL SIGQUIT
# Wed, 10 Apr 2024 11:27:00 GMT
EXPOSE 9000
# Wed, 10 Apr 2024 11:27:03 GMT
CMD ["php-fpm"]
# Wed, 10 Apr 2024 18:37:49 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Wed, 10 Apr 2024 18:37:53 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 10 Apr 2024 18:37:56 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 10 Apr 2024 18:56:37 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.23;     pecl install imagick-3.7.0;     pecl install memcached-3.2.0;     pecl install redis-6.0.2;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 18:56:43 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Wed, 10 Apr 2024 18:56:47 GMT
VOLUME [/var/www/html]
# Wed, 10 Apr 2024 19:13:31 GMT
ENV NEXTCLOUD_VERSION=28.0.4
# Wed, 10 Apr 2024 19:16:50 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-28.0.4.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-28.0.4.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 19:17:02 GMT
COPY multi:9585a9602f24ff6c37b7e8821d7e5fca4a450cd9cc8c66163bc629028ca3df5c in / 
# Wed, 10 Apr 2024 19:17:11 GMT
COPY multi:78125c707b59ef0f6f1ecce97806e1bec0bbbd71be245d580e78e8ceb5133056 in /usr/src/nextcloud/config/ 
# Wed, 10 Apr 2024 19:17:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 19:17:29 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:a99180cf1634aa211024be7ce3258cac9c0823e82f09b97870da9d9b21ea68ca`  
		Last Modified: Wed, 10 Apr 2024 01:21:58 GMT  
		Size: 29.1 MB (29124665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a34f75e84a486095ed4b9494bb7a787778509c1141f23a283516ca77bb1d317b`  
		Last Modified: Wed, 10 Apr 2024 14:43:26 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45d33207e6cd90f4f28435e042103d5c48a1cf6cce17eb9acf9b20659062c129`  
		Last Modified: Wed, 10 Apr 2024 14:44:23 GMT  
		Size: 80.7 MB (80667297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2939b1e00da3d25558cbb8ad2c613043d4eaaa57d2f72ca78bc574efbad6c7`  
		Last Modified: Wed, 10 Apr 2024 14:43:26 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df0ad4d274ea5dac3667c25f265ff8e8e14496770d288bfb19055f7895fbcd43`  
		Last Modified: Wed, 10 Apr 2024 14:58:46 GMT  
		Size: 12.2 MB (12200177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f60951547ce5c90a5e00d95e858d4cb9764d1cc51afd67cf395217980301524`  
		Last Modified: Wed, 10 Apr 2024 14:58:42 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f287cec673228ff0b8cdd040aa289f4e5fcf52633c90156d0cb67aa4991f36c7`  
		Last Modified: Wed, 10 Apr 2024 15:00:11 GMT  
		Size: 26.7 MB (26668373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:800138c113075abf64ee114724022e59ad2369ea7a6ed312670153ad686dee83`  
		Last Modified: Wed, 10 Apr 2024 14:59:54 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae73f4aacb61b977ed9e5f27c5dd91404692cd46defe54228c468275f3aaae4`  
		Last Modified: Wed, 10 Apr 2024 14:59:54 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da699faa97a57ec609c08ac5c5f2f27136d07d6abd9f78565cf183127d84f6a5`  
		Last Modified: Wed, 10 Apr 2024 14:59:54 GMT  
		Size: 9.2 KB (9189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:236e7cf74e0bbd014a960681a44ee0d6aca9615bd5c1daa0a2cb7a88da146d91`  
		Last Modified: Wed, 10 Apr 2024 19:20:57 GMT  
		Size: 19.9 MB (19926339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59dc9a21d09de842734fc227be3a5bc0165eaea23b53cd814463b0caafc7b561`  
		Last Modified: Wed, 10 Apr 2024 19:21:04 GMT  
		Size: 20.6 MB (20646599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cfe12428073612bde6480da9fbe56ca4e76f6d736c792fec65d406cfff320e8`  
		Last Modified: Wed, 10 Apr 2024 19:20:37 GMT  
		Size: 714.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea70a32efd5217334eeb3afa36ef593a0b0b08490f79decdff30f5e21041fd9d`  
		Last Modified: Wed, 10 Apr 2024 19:32:45 GMT  
		Size: 204.9 MB (204932644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3520fcd8fe9ff8d54f872a0934f78b878af422fbc92a9a6c5a2d6e5a1efe41ed`  
		Last Modified: Wed, 10 Apr 2024 19:30:40 GMT  
		Size: 3.6 KB (3613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfcd49bdc946698f339300fa222a7473342f1affd56097186443e819300392bf`  
		Last Modified: Wed, 10 Apr 2024 19:30:40 GMT  
		Size: 2.3 KB (2339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:28-fpm` - linux; ppc64le

```console
$ docker pull nextcloud@sha256:46a43024138c11c3a60a9349b1813505c6e445031cf4b765c28a749e1f178e92
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **427.7 MB (427658608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ab17903349752e50a9c42b4aa4095a515b67cfb0034a43da49751570a9d79b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 10 Apr 2024 01:26:33 GMT
ADD file:fd6cd6147fc95a907a092392fe95b8ed685d7ed84c60593cd7e9c64a7d574b64 in / 
# Wed, 10 Apr 2024 01:26:35 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 08:48:02 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 10 Apr 2024 08:48:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 10 Apr 2024 08:49:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 08:49:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 10 Apr 2024 08:49:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 10 Apr 2024 08:49:19 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Apr 2024 08:49:20 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Apr 2024 08:49:21 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 10 Apr 2024 10:01:31 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 10 Apr 2024 10:34:22 GMT
ENV PHP_VERSION=8.2.17
# Wed, 10 Apr 2024 10:34:23 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.17.tar.xz.asc
# Wed, 10 Apr 2024 10:34:24 GMT
ENV PHP_SHA256=1cc4ef733ba58f6557db648012471f1916e5bac316303aa165535bedab08ee35
# Wed, 10 Apr 2024 10:34:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 10 Apr 2024 10:34:55 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 10 Apr 2024 10:45:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 10 Apr 2024 10:45:20 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 10 Apr 2024 10:45:23 GMT
RUN docker-php-ext-enable sodium
# Wed, 10 Apr 2024 10:45:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 10 Apr 2024 10:45:24 GMT
WORKDIR /var/www/html
# Wed, 10 Apr 2024 10:45:26 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 10 Apr 2024 10:45:26 GMT
STOPSIGNAL SIGQUIT
# Wed, 10 Apr 2024 10:45:28 GMT
EXPOSE 9000
# Wed, 10 Apr 2024 10:45:28 GMT
CMD ["php-fpm"]
# Wed, 10 Apr 2024 16:28:03 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Wed, 10 Apr 2024 16:28:04 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 10 Apr 2024 16:28:04 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 10 Apr 2024 16:31:52 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.23;     pecl install imagick-3.7.0;     pecl install memcached-3.2.0;     pecl install redis-6.0.2;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 16:31:54 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Wed, 10 Apr 2024 16:31:54 GMT
VOLUME [/var/www/html]
# Wed, 10 Apr 2024 16:37:47 GMT
ENV NEXTCLOUD_VERSION=28.0.4
# Wed, 10 Apr 2024 16:38:56 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-28.0.4.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-28.0.4.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 16:39:02 GMT
COPY multi:9585a9602f24ff6c37b7e8821d7e5fca4a450cd9cc8c66163bc629028ca3df5c in / 
# Wed, 10 Apr 2024 16:39:03 GMT
COPY multi:78125c707b59ef0f6f1ecce97806e1bec0bbbd71be245d580e78e8ceb5133056 in /usr/src/nextcloud/config/ 
# Wed, 10 Apr 2024 16:39:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 16:39:03 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:4d891dca051cd29ed554a21d46a9f98401d3ae8b7b85da23513e7b4b1e86008c`  
		Last Modified: Wed, 10 Apr 2024 01:31:08 GMT  
		Size: 33.1 MB (33124837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:514d17bf792c44f547b7e10eed284ae1836db8d921fa5ff3b7442bf2b3bdf76b`  
		Last Modified: Wed, 10 Apr 2024 11:49:56 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f380bd7e47edf018d9afb351576809853ca384148a0af4fb2ec41d2261320882`  
		Last Modified: Wed, 10 Apr 2024 11:50:13 GMT  
		Size: 103.3 MB (103313184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf4dbaadfb46a67d690bd0e078f5f0deb5d7a990f1d7c50aaa2afec603b4823`  
		Last Modified: Wed, 10 Apr 2024 11:49:56 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49de83c67b2f58ef0e2f2761e9bd8aedd90912737d424dfe5a6de66b040a11c`  
		Last Modified: Wed, 10 Apr 2024 11:59:32 GMT  
		Size: 12.4 MB (12405968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f69a6664f2d37b55b680d4f6fe351f5d88c0add66071f2eb93739349333144`  
		Last Modified: Wed, 10 Apr 2024 11:59:31 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d758fd17bab1684d31f47885ee693a3c5e4683903894e93f03ab7f1867f8e62`  
		Last Modified: Wed, 10 Apr 2024 12:00:27 GMT  
		Size: 28.8 MB (28832321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07eb9f8efba63cc7a1eec13c0fab89ed02103324bb1093cd7cce1f27d0fa3a8d`  
		Last Modified: Wed, 10 Apr 2024 12:00:22 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2db8a7aa282dfa2b20407a4682094b4c1a50c71f77e1533508e3fbaf9202b92`  
		Last Modified: Wed, 10 Apr 2024 12:00:23 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bab41db6be76e5ab205cbb2b9d9bca875d587848a10ae813a932ea911d018a2`  
		Last Modified: Wed, 10 Apr 2024 12:00:22 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b0b382a68d128b9378855a8978271752b4111801a17c43c8529314e60f78ef`  
		Last Modified: Wed, 10 Apr 2024 16:40:31 GMT  
		Size: 22.8 MB (22755836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2534efbc0d2bafe1894df87e3e6aa3febbfcfa65a3458129224c3880cdb5f5a7`  
		Last Modified: Wed, 10 Apr 2024 16:40:30 GMT  
		Size: 22.1 MB (22054921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7b45d9395f5dbeccfc1450548285cf1f7ee04b1087356680348ed05e07acf9`  
		Last Modified: Wed, 10 Apr 2024 16:40:26 GMT  
		Size: 762.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a2774436c731326346c8f265d0e8ea27cea0c811cb2bf2113e42098f27e7468`  
		Last Modified: Wed, 10 Apr 2024 16:44:22 GMT  
		Size: 205.2 MB (205151956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5503382c52901207458839b760a9fabbad92de44c3da3da7154932f176a55330`  
		Last Modified: Wed, 10 Apr 2024 16:43:54 GMT  
		Size: 3.6 KB (3613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1684c7551f4f26fbe411db54479f0e9e7ee2dc4c6f660c160163efb346fc77f`  
		Last Modified: Wed, 10 Apr 2024 16:43:55 GMT  
		Size: 2.3 KB (2339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:28-fpm` - linux; s390x

```console
$ docker pull nextcloud@sha256:7ef58bdef217a0135ff2b0a09284251ba72e852b335845a70d05c0d269463a1e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.3 MB (392290973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9360b6b2573d9851ca4a311907f14311c19e9979dc78ed2e45ed8a370bed0f01`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 10 Apr 2024 01:14:52 GMT
ADD file:0e66ba8384d53d3671a6a148f8bad9decf482a97ef81d0740132e74b8e30c670 in / 
# Wed, 10 Apr 2024 01:14:57 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 11:47:26 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 10 Apr 2024 11:47:26 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 10 Apr 2024 11:48:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 11:48:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 10 Apr 2024 11:48:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 10 Apr 2024 11:48:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Apr 2024 11:48:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Apr 2024 11:48:52 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 10 Apr 2024 14:07:16 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 10 Apr 2024 14:59:40 GMT
ENV PHP_VERSION=8.2.17
# Wed, 10 Apr 2024 14:59:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.17.tar.xz.asc
# Wed, 10 Apr 2024 14:59:40 GMT
ENV PHP_SHA256=1cc4ef733ba58f6557db648012471f1916e5bac316303aa165535bedab08ee35
# Wed, 10 Apr 2024 15:00:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 10 Apr 2024 15:00:01 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 10 Apr 2024 15:16:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 10 Apr 2024 15:16:38 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 10 Apr 2024 15:16:39 GMT
RUN docker-php-ext-enable sodium
# Wed, 10 Apr 2024 15:16:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 10 Apr 2024 15:16:40 GMT
WORKDIR /var/www/html
# Wed, 10 Apr 2024 15:16:41 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 10 Apr 2024 15:16:41 GMT
STOPSIGNAL SIGQUIT
# Wed, 10 Apr 2024 15:16:41 GMT
EXPOSE 9000
# Wed, 10 Apr 2024 15:16:41 GMT
CMD ["php-fpm"]
# Thu, 11 Apr 2024 02:20:38 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Thu, 11 Apr 2024 02:20:39 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 11 Apr 2024 02:20:39 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 11 Apr 2024 02:22:39 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.23;     pecl install imagick-3.7.0;     pecl install memcached-3.2.0;     pecl install redis-6.0.2;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Apr 2024 02:22:42 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Thu, 11 Apr 2024 02:22:43 GMT
VOLUME [/var/www/html]
# Thu, 11 Apr 2024 02:34:09 GMT
ENV NEXTCLOUD_VERSION=28.0.4
# Thu, 11 Apr 2024 02:34:48 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-28.0.4.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-28.0.4.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Apr 2024 02:34:59 GMT
COPY multi:9585a9602f24ff6c37b7e8821d7e5fca4a450cd9cc8c66163bc629028ca3df5c in / 
# Thu, 11 Apr 2024 02:34:59 GMT
COPY multi:78125c707b59ef0f6f1ecce97806e1bec0bbbd71be245d580e78e8ceb5133056 in /usr/src/nextcloud/config/ 
# Thu, 11 Apr 2024 02:34:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Apr 2024 02:34:59 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:06d33788df65214dbd82280e1b49e32ce4580d4f3df100d32090f4eae8ccd99c`  
		Last Modified: Wed, 10 Apr 2024 01:48:29 GMT  
		Size: 27.5 MB (27494178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b27b7df89cf8d24e9440ecd58af5c1f1c53c18a9b3c7a989928cf022fe5c5b62`  
		Last Modified: Wed, 10 Apr 2024 16:53:59 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab9a5052adf2e7e4ea84998835514691e3f6a0ebf9a65f2e64e4ed911343891`  
		Last Modified: Wed, 10 Apr 2024 16:54:12 GMT  
		Size: 80.8 MB (80809462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d948c793bbe2a69532fffe739761843580ad814b5079d25c8a62e2898d53ea0`  
		Last Modified: Wed, 10 Apr 2024 16:53:59 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c14005bee43a65e5ced8e09287c101893d26ed18a9f88c5b43cb00f939f58af`  
		Last Modified: Wed, 10 Apr 2024 17:02:37 GMT  
		Size: 12.4 MB (12405038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ca5233022ea06debc26cb810b62eaa40dfd78588c0733d0e0715e8236052b8`  
		Last Modified: Wed, 10 Apr 2024 17:02:36 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3bd03483cb7d3d9b404281158149b0c684f93eb264f151cd5b1d0af38b31c36`  
		Last Modified: Wed, 10 Apr 2024 17:03:19 GMT  
		Size: 26.7 MB (26708949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01b62ecfae08c43b38dfe618c3564a4d776d360f7ef9461c086cf916f8906d1`  
		Last Modified: Wed, 10 Apr 2024 17:03:15 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33ea6be094b3ce1d1622914334df109e365616bcccf3204f2d6b3cd48ecaf43`  
		Last Modified: Wed, 10 Apr 2024 17:03:15 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83edfbb67f856397fcfc0aacbc402d4a836d9445728fcc63acdba35259fe2aef`  
		Last Modified: Wed, 10 Apr 2024 17:03:15 GMT  
		Size: 9.2 KB (9184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e42e65f7b47cd83762554edb3fdd6cc6566994e7600a27913109a2379950926e`  
		Last Modified: Thu, 11 Apr 2024 02:38:35 GMT  
		Size: 19.4 MB (19401337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7d43cf30eefb6e8bdb8defbdc03117430845ce5866ac78ef653a385a46d6e1`  
		Last Modified: Thu, 11 Apr 2024 02:38:34 GMT  
		Size: 20.3 MB (20302876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cfedadbce718e301e0086b03477413d05d8e4ec5776503d91cb3c9744785aea`  
		Last Modified: Thu, 11 Apr 2024 02:38:31 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:987847186939768d358c534b211cf0b507765b78aabc9e145b26e4d3e7dc7a85`  
		Last Modified: Thu, 11 Apr 2024 02:41:43 GMT  
		Size: 205.1 MB (205149545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42ddda10a70f7b7b1a86bbe618bb1821f216928baeeebc5fc609a2be972d93d6`  
		Last Modified: Thu, 11 Apr 2024 02:41:19 GMT  
		Size: 3.6 KB (3613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db24662f468a3603870a2e2d97e5fed62ac8c3f775454782f55da606288d4bcb`  
		Last Modified: Thu, 11 Apr 2024 02:41:19 GMT  
		Size: 2.3 KB (2335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
