## `nextcloud:fpm`

```console
$ docker pull nextcloud@sha256:043ad29d7423bc750c3bff8210413d8ca591f971c98680ee1edd1367b950cc49
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
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

### `nextcloud:fpm` - linux; amd64

```console
$ docker pull nextcloud@sha256:c240d98a6f77237956bba6ffb26ad1c8fb24febd9a6e4868a84a03a7d33d0922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **499.7 MB (499656933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b466a05fcd8aabec0bd92dd4812a43528bc41b8168132b7dc2b377916e121fe2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:23:25 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 11 Jun 2026 00:23:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Jun 2026 00:23:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 00:23:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jun 2026 00:23:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 11 Jun 2026 00:23:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 00:23:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 00:23:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jun 2026 00:23:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 11 Jun 2026 00:23:40 GMT
ENV PHP_VERSION=8.4.22
# Thu, 11 Jun 2026 00:23:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.22.tar.xz.asc
# Thu, 11 Jun 2026 00:23:40 GMT
ENV PHP_SHA256=696c0f6ad92e94c59059c1eb6e300842b8d050934226efcdf00f2a413cb083cf
# Thu, 11 Jun 2026 00:27:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 11 Jun 2026 00:27:02 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:29:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 11 Jun 2026 00:29:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:29:27 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 11 Jun 2026 00:29:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 11 Jun 2026 00:29:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Jun 2026 00:29:27 GMT
WORKDIR /var/www/html
# Thu, 11 Jun 2026 00:29:27 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 11 Jun 2026 00:29:27 GMT
STOPSIGNAL SIGQUIT
# Thu, 11 Jun 2026 00:29:27 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 11 Jun 2026 00:29:27 GMT
CMD ["php-fpm"]
# Thu, 11 Jun 2026 02:34:49 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-7.q16-10-extra         rsync     ;     apt-get dist-clean;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Thu, 11 Jun 2026 02:36:52 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 11 Jun 2026 02:36:52 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 11 Jun 2026 02:36:52 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Thu, 11 Jun 2026 02:36:52 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         liblz4-dev         libmagickwand-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-ftp-ssl;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.28;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.1;     pecl install --configureoptions 'enable-memcached-igbinary="yes"'         memcached-3.4.0;     pecl install --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"'         redis-6.3.0;         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -rt dpkg-query --search         | awk 'sub(":$", "", $1) { print $1 }'         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 02:36:52 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Thu, 11 Jun 2026 02:36:52 GMT
VOLUME [/var/www/html]
# Thu, 11 Jun 2026 02:36:52 GMT
ENV NEXTCLOUD_VERSION=34.0.0
# Thu, 11 Jun 2026 02:37:28 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://github.com/nextcloud-releases/server/releases/download/v34.0.0/nextcloud-34.0.0.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://github.com/nextcloud-releases/server/releases/download/v34.0.0/nextcloud-34.0.0.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 02:37:28 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 11 Jun 2026 02:37:28 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Thu, 11 Jun 2026 02:37:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 02:37:28 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31286d3e114de62428f973c0ea02bd1fd3ff12c3fe3cd873a637fdb0f9d5b73`  
		Last Modified: Thu, 11 Jun 2026 00:26:43 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc44fbd21b93bbc79720df170b74e2438f416ff1b4d0f24e1f1399fb5e78cf4`  
		Last Modified: Thu, 11 Jun 2026 00:26:46 GMT  
		Size: 117.8 MB (117840203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aed6ebc6db9b49ae92bdc5261b2b22bc08a468662695516ca79d7eb25a654e87`  
		Last Modified: Thu, 11 Jun 2026 00:26:42 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769ef4ae211ddcfe38a1dbad2b6194ddc9b426e477f8150778d9b3aff0912e51`  
		Last Modified: Thu, 11 Jun 2026 00:29:38 GMT  
		Size: 13.9 MB (13879600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d21251bfc54accd3d08074872509b432d78a7dd8f11734c50c226ecd004d5bdb`  
		Last Modified: Thu, 11 Jun 2026 00:29:37 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c71479fcf094d010ad7023f90b21ff7393e45dd7236d5c39a3264be33c22be`  
		Last Modified: Thu, 11 Jun 2026 00:29:38 GMT  
		Size: 13.8 MB (13809218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a1ec66c96550424601ed892d6e3aa12817502d60658ddd0ca6046d4d6af0a56`  
		Last Modified: Thu, 11 Jun 2026 00:29:38 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec60ab8df23f5d451a11482d5d7e5620b2df5aba20cfbc2d8747cacfd141c9ec`  
		Last Modified: Thu, 11 Jun 2026 00:29:38 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c2b27b2469ef4130a6b429614ce3c44719abac24c7711d742fd4ce0b7d12c1`  
		Last Modified: Thu, 11 Jun 2026 00:29:39 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d375ec8c45274067ae37cfe3218e6b9d3191aeaed02f35750675750760158684`  
		Last Modified: Thu, 11 Jun 2026 00:29:40 GMT  
		Size: 9.3 KB (9266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6264b9733e824cd59f648edc5827f4f10368337fbaf52c9525e8643b5ec0fa30`  
		Last Modified: Thu, 11 Jun 2026 02:37:56 GMT  
		Size: 21.1 MB (21091992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bd1aab17666d58936a3426230b8131e8b58113df3c5068006d5ec4c19492526`  
		Last Modified: Thu, 11 Jun 2026 02:37:57 GMT  
		Size: 37.1 MB (37066672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d803260b94b49d40fa9e773f9da35e8249c61a91719b9a467114ee96fab0cfc6`  
		Last Modified: Thu, 11 Jun 2026 02:37:55 GMT  
		Size: 790.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4fb948051f9dd7dac2be9fe9b08f7e7797b2586ae7133a7e4092d514a7f65f9`  
		Last Modified: Thu, 11 Jun 2026 02:38:01 GMT  
		Size: 266.2 MB (266163373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb07b7951e38a6940fe44a3937be9700c4389852c6a371f2b2e8d0f560c552d`  
		Last Modified: Thu, 11 Jun 2026 02:37:57 GMT  
		Size: 4.1 KB (4134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:692db0305d520639f06cf1379e4db2d3a60cc18cf32580efdd56a6781b8dd381`  
		Last Modified: Thu, 11 Jun 2026 02:37:58 GMT  
		Size: 2.4 KB (2355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:fpm` - unknown; unknown

```console
$ docker pull nextcloud@sha256:8f12e8bb54d45d28e55516eca4fce4cdc9c584c9a487c91e12a318dbe476fd8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 KB (46722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:578d2a982b9365e78b756c95ae2cd081fa1908cf9e9d8fe17b58a56d019f39c6`

```dockerfile
```

-	Layers:
	-	`sha256:682dfd85a22f5a9c5b104410f9f610ccff5f92befb23e9e35eac0cb8d0c67732`  
		Last Modified: Thu, 11 Jun 2026 02:37:55 GMT  
		Size: 46.7 KB (46722 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:fpm` - linux; arm variant v5

```console
$ docker pull nextcloud@sha256:7d577fbb9a1dad957f5f34bbeb503d44570f8ae63453d836f559bf2c0dcef024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **470.6 MB (470591803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2a6201cf44d7b877e89c8e3f85598dddbe042d449369452991ffcbcb24c199`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:29:50 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 11 Jun 2026 00:30:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Jun 2026 00:30:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 00:30:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jun 2026 00:30:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 11 Jun 2026 00:30:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 00:30:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 00:30:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jun 2026 00:30:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 11 Jun 2026 00:30:13 GMT
ENV PHP_VERSION=8.4.22
# Thu, 11 Jun 2026 00:30:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.22.tar.xz.asc
# Thu, 11 Jun 2026 00:30:13 GMT
ENV PHP_SHA256=696c0f6ad92e94c59059c1eb6e300842b8d050934226efcdf00f2a413cb083cf
# Thu, 11 Jun 2026 00:30:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 11 Jun 2026 00:30:25 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:33:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 11 Jun 2026 00:33:23 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:33:23 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 11 Jun 2026 00:33:23 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 11 Jun 2026 00:33:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Jun 2026 00:33:23 GMT
WORKDIR /var/www/html
# Thu, 11 Jun 2026 00:33:23 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 11 Jun 2026 00:33:23 GMT
STOPSIGNAL SIGQUIT
# Thu, 11 Jun 2026 00:33:23 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 11 Jun 2026 00:33:23 GMT
CMD ["php-fpm"]
# Thu, 11 Jun 2026 02:59:43 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-7.q16-10-extra         rsync     ;     apt-get dist-clean;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Thu, 11 Jun 2026 03:02:48 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 11 Jun 2026 03:02:48 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 11 Jun 2026 03:02:48 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Thu, 11 Jun 2026 03:02:48 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         liblz4-dev         libmagickwand-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-ftp-ssl;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.28;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.1;     pecl install --configureoptions 'enable-memcached-igbinary="yes"'         memcached-3.4.0;     pecl install --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"'         redis-6.3.0;         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -rt dpkg-query --search         | awk 'sub(":$", "", $1) { print $1 }'         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 03:02:48 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Thu, 11 Jun 2026 03:02:48 GMT
VOLUME [/var/www/html]
# Thu, 11 Jun 2026 03:02:48 GMT
ENV NEXTCLOUD_VERSION=34.0.0
# Thu, 11 Jun 2026 03:03:35 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://github.com/nextcloud-releases/server/releases/download/v34.0.0/nextcloud-34.0.0.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://github.com/nextcloud-releases/server/releases/download/v34.0.0/nextcloud-34.0.0.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 03:03:36 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 11 Jun 2026 03:03:36 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Thu, 11 Jun 2026 03:03:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 03:03:36 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:ed883f3fd95b7edef302d7ca9520eefdae280af081509bd7e9e5b5ff8f4cda7c`  
		Last Modified: Wed, 10 Jun 2026 23:41:17 GMT  
		Size: 28.0 MB (27959200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f6e579abf0c86d6b8dd776d4fc7a6b3eeb0a3469171c31f940e9afb169bfca`  
		Last Modified: Thu, 11 Jun 2026 00:33:41 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afb291233af920ba1686772623724bdf2fa620d3364736ede4b877ccd24dede`  
		Last Modified: Thu, 11 Jun 2026 00:33:44 GMT  
		Size: 94.9 MB (94885609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58740c84dd2329ffe8b938650bfc52a096fe228047d2da433cef043cb1ae45b9`  
		Last Modified: Thu, 11 Jun 2026 00:33:41 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6f454626cbbf9cff5c51f4c6fe92f3e05e9b2e519c4ff316712376493c8672`  
		Last Modified: Thu, 11 Jun 2026 00:33:42 GMT  
		Size: 13.9 MB (13876728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a7af7683fce71305a72757abf200231b136ffa527ca90b988b4e9d142138bfa`  
		Last Modified: Thu, 11 Jun 2026 00:33:43 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1137e944d7151edad169f1e8fc38cea7f90bee940e545e7e27b8214c7b9288`  
		Last Modified: Thu, 11 Jun 2026 00:33:43 GMT  
		Size: 12.3 MB (12320720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d53743bfc1c2e25afa1875d7820e850f62a7e6ff159e4fb91066ebb423a8aac`  
		Last Modified: Thu, 11 Jun 2026 00:33:44 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc2571afe17be4b56c513fdcc0b23d17e0be3a59a62c6f63cb7d33d3db0d30e`  
		Last Modified: Thu, 11 Jun 2026 00:33:44 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8065a8b793a6d01352179e64a69e1051ed377aaf9c1b0babeea5a3fbb32c681f`  
		Last Modified: Thu, 11 Jun 2026 00:33:45 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c279c08462e2024b185317d323f45873759cbd02badc07cfd0846ddf1f3ac4`  
		Last Modified: Thu, 11 Jun 2026 00:33:45 GMT  
		Size: 9.3 KB (9265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e3aecbbff71fdd836c96cd3fe2b7259e3fa8154e3148aa5ffb936bd56d06072`  
		Last Modified: Thu, 11 Jun 2026 03:04:07 GMT  
		Size: 20.2 MB (20177626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dcf8db474f4368b068ec31018e91ae5e9494b85c9e72cbb3d42130c38f30b7b`  
		Last Modified: Thu, 11 Jun 2026 03:04:07 GMT  
		Size: 35.2 MB (35199431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa15b041af31e32260bfb63e1f8f83129fa2fa9622d657366a69a762bfe8fb8`  
		Last Modified: Thu, 11 Jun 2026 03:04:07 GMT  
		Size: 792.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a19fd24b12fcb64dd1ed22cb8bd78582c3192aab204fa5076084069082924d`  
		Last Modified: Thu, 11 Jun 2026 03:04:15 GMT  
		Size: 266.2 MB (266152021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447c2aa88c0241910a51100100939c49024f0ca2df587be983669b672dc989f2`  
		Last Modified: Thu, 11 Jun 2026 03:04:08 GMT  
		Size: 4.1 KB (4135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd82f4adf06b8db58ddb76dd8fd93a685b7555fd3d0874b98ead6afbcfd31516`  
		Last Modified: Thu, 11 Jun 2026 03:04:09 GMT  
		Size: 2.4 KB (2357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:fpm` - unknown; unknown

```console
$ docker pull nextcloud@sha256:eba16ca80f43cc0b9771b3444be82deff2419e1cb6c2d35bcfde7045a988ea17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 KB (46834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6487eb067f2a63d897a0686acf3aa4dca228ec1a1d5a77590a8dfb68fc7bd462`

```dockerfile
```

-	Layers:
	-	`sha256:ed4e99d98f9dc84965f3088c54526195d3cdd811bc49d7cdb7888d42f47bbc63`  
		Last Modified: Thu, 11 Jun 2026 03:04:06 GMT  
		Size: 46.8 KB (46834 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:fpm` - linux; arm variant v7

```console
$ docker pull nextcloud@sha256:0b92447a2a0fb3c14eefc1426a5db5718ca91733b49d0dd7785930c40132ac86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **457.0 MB (457048309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:025e81cb2a641da359725a4911246e78114ef0520dd059325184213d3c631579`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:33:06 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 11 Jun 2026 00:33:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Jun 2026 00:33:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 00:33:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jun 2026 00:33:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 11 Jun 2026 00:33:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 00:33:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 00:33:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jun 2026 00:33:24 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 11 Jun 2026 00:33:24 GMT
ENV PHP_VERSION=8.4.22
# Thu, 11 Jun 2026 00:33:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.22.tar.xz.asc
# Thu, 11 Jun 2026 00:33:24 GMT
ENV PHP_SHA256=696c0f6ad92e94c59059c1eb6e300842b8d050934226efcdf00f2a413cb083cf
# Thu, 11 Jun 2026 00:33:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 11 Jun 2026 00:33:34 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:36:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 11 Jun 2026 00:36:18 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:36:18 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 11 Jun 2026 00:36:18 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 11 Jun 2026 00:36:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Jun 2026 00:36:18 GMT
WORKDIR /var/www/html
# Thu, 11 Jun 2026 00:36:18 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 11 Jun 2026 00:36:18 GMT
STOPSIGNAL SIGQUIT
# Thu, 11 Jun 2026 00:36:18 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 11 Jun 2026 00:36:18 GMT
CMD ["php-fpm"]
# Thu, 11 Jun 2026 03:11:05 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-7.q16-10-extra         rsync     ;     apt-get dist-clean;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Thu, 11 Jun 2026 03:14:01 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 11 Jun 2026 03:14:01 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 11 Jun 2026 03:14:01 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Thu, 11 Jun 2026 03:14:01 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         liblz4-dev         libmagickwand-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-ftp-ssl;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.28;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.1;     pecl install --configureoptions 'enable-memcached-igbinary="yes"'         memcached-3.4.0;     pecl install --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"'         redis-6.3.0;         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -rt dpkg-query --search         | awk 'sub(":$", "", $1) { print $1 }'         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 03:14:01 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Thu, 11 Jun 2026 03:14:01 GMT
VOLUME [/var/www/html]
# Thu, 11 Jun 2026 03:14:01 GMT
ENV NEXTCLOUD_VERSION=34.0.0
# Thu, 11 Jun 2026 03:14:50 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://github.com/nextcloud-releases/server/releases/download/v34.0.0/nextcloud-34.0.0.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://github.com/nextcloud-releases/server/releases/download/v34.0.0/nextcloud-34.0.0.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 03:14:50 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 11 Jun 2026 03:14:51 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Thu, 11 Jun 2026 03:14:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 03:14:51 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:4bd6ddea06d5009ee47ddb0f254a2569aff0230c005869ebd416b20295d945c0`  
		Last Modified: Wed, 10 Jun 2026 23:42:34 GMT  
		Size: 26.2 MB (26211004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d76dfd5197907ecf06904d2d44dd9eca5d7efe835b3af650b95f2ee9e8a109`  
		Last Modified: Thu, 11 Jun 2026 00:36:34 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e0b9011a52547ee2debec07290e7fce07fd2df6481d7744eb01b46f139d483`  
		Last Modified: Thu, 11 Jun 2026 00:36:37 GMT  
		Size: 86.3 MB (86255673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6113e7bcac76a543cacf47cd0ba049a2a530199e3dfc61520aa7f4c2e45b08`  
		Last Modified: Thu, 11 Jun 2026 00:36:34 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce39f73b93db5b5541c6898b32692be4cb3778864b24977701a7d9618f75d20a`  
		Last Modified: Thu, 11 Jun 2026 00:36:35 GMT  
		Size: 13.9 MB (13876989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332f759d6a9d4c5d7802719b0a0749432ff138f9e8a452172cc75e5a0f93b72d`  
		Last Modified: Thu, 11 Jun 2026 00:36:36 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd30d6a3613dff1248bc5001cea91df1640abc295b7799558b464fe557871ad`  
		Last Modified: Thu, 11 Jun 2026 00:36:36 GMT  
		Size: 11.7 MB (11654242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628c01047d48b205bede8f8fda1d74baaa8b8c0a7f6e546cfd63ddca1490849b`  
		Last Modified: Thu, 11 Jun 2026 00:36:37 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:605244642a3646cc0864772dd917cd40a4dc11d728ed6cf5787336b139387378`  
		Last Modified: Thu, 11 Jun 2026 00:36:37 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b44f94939e1b8ce602bee7862d8160e860468eb011d1ed019ba21f4897f45c1`  
		Last Modified: Thu, 11 Jun 2026 00:36:38 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7887b7e4520dfbf3122f3f7b2aede6326a820e84dc71e551c64e277ffa1d0e82`  
		Last Modified: Thu, 11 Jun 2026 00:36:38 GMT  
		Size: 9.3 KB (9267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4ea97db2e7cad5bfc0f75ca5ed7402b4d611c0bf6edcc31598ece9c832371b`  
		Last Modified: Thu, 11 Jun 2026 03:15:22 GMT  
		Size: 18.1 MB (18097633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1624886cfdab3c925bcf4f04090477defc5a0de171e5361f452b23d03391c664`  
		Last Modified: Thu, 11 Jun 2026 03:15:23 GMT  
		Size: 34.8 MB (34780135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24334ff429878f53958ec169b06f402c4655532ecd93140aab5c18540c3ea9d1`  
		Last Modified: Thu, 11 Jun 2026 03:15:21 GMT  
		Size: 792.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95324ea5e9ae64ffe859cf4bea7eaa71dbee4cf10d3737bcf92d4f991b34bfe0`  
		Last Modified: Thu, 11 Jun 2026 03:15:30 GMT  
		Size: 266.2 MB (266152169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5afc3fb93c0436ed0b963d8680ca8bc13a2846efc3c29d059796fd5e77014f0`  
		Last Modified: Thu, 11 Jun 2026 03:15:23 GMT  
		Size: 4.1 KB (4136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1bb138483f29e3437ebd456992e5a8601de441cdaa269f455ee76033d3ee18`  
		Last Modified: Thu, 11 Jun 2026 03:15:24 GMT  
		Size: 2.4 KB (2357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:fpm` - unknown; unknown

```console
$ docker pull nextcloud@sha256:1785ee53a7a266bbc7b472598b2cd3a401e081d5bb08c62907ca7bf9f2ec217b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 KB (46834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1241e1a06e4e5e70e104dd75b3fd642d334084c3e027a59128f62c46556654e5`

```dockerfile
```

-	Layers:
	-	`sha256:5c0e86a6280285a384cba85f8c9e7ab2b028f348dc33cce819138d22b63fc445`  
		Last Modified: Thu, 11 Jun 2026 03:15:20 GMT  
		Size: 46.8 KB (46834 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:fpm` - linux; arm64 variant v8

```console
$ docker pull nextcloud@sha256:1e302fc51b32ff98809a0f04c32c84e8d8107f8564a9c72c9e272598a8d46aff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **490.6 MB (490617647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59a67f4165e653ed7b2cbcc5695fa7b9ad6a3ed864913f98746187b46e8e3dbe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:27:59 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 11 Jun 2026 00:28:21 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Jun 2026 00:28:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 00:28:21 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jun 2026 00:28:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 11 Jun 2026 00:28:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 00:28:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 00:28:21 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jun 2026 00:28:21 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 11 Jun 2026 00:28:21 GMT
ENV PHP_VERSION=8.4.22
# Thu, 11 Jun 2026 00:28:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.22.tar.xz.asc
# Thu, 11 Jun 2026 00:28:21 GMT
ENV PHP_SHA256=696c0f6ad92e94c59059c1eb6e300842b8d050934226efcdf00f2a413cb083cf
# Thu, 11 Jun 2026 00:28:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 11 Jun 2026 00:28:29 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:31:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 11 Jun 2026 00:31:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:31:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 11 Jun 2026 00:31:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 11 Jun 2026 00:31:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Jun 2026 00:31:25 GMT
WORKDIR /var/www/html
# Thu, 11 Jun 2026 00:31:25 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 11 Jun 2026 00:31:25 GMT
STOPSIGNAL SIGQUIT
# Thu, 11 Jun 2026 00:31:25 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 11 Jun 2026 00:31:25 GMT
CMD ["php-fpm"]
# Thu, 11 Jun 2026 02:37:04 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-7.q16-10-extra         rsync     ;     apt-get dist-clean;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Thu, 11 Jun 2026 02:39:30 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 11 Jun 2026 02:39:30 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 11 Jun 2026 02:39:30 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Thu, 11 Jun 2026 02:39:30 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         liblz4-dev         libmagickwand-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-ftp-ssl;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.28;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.1;     pecl install --configureoptions 'enable-memcached-igbinary="yes"'         memcached-3.4.0;     pecl install --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"'         redis-6.3.0;         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -rt dpkg-query --search         | awk 'sub(":$", "", $1) { print $1 }'         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 02:39:31 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Thu, 11 Jun 2026 02:39:31 GMT
VOLUME [/var/www/html]
# Thu, 11 Jun 2026 02:39:31 GMT
ENV NEXTCLOUD_VERSION=34.0.0
# Thu, 11 Jun 2026 02:40:06 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://github.com/nextcloud-releases/server/releases/download/v34.0.0/nextcloud-34.0.0.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://github.com/nextcloud-releases/server/releases/download/v34.0.0/nextcloud-34.0.0.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 02:40:06 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 11 Jun 2026 02:40:06 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Thu, 11 Jun 2026 02:40:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 02:40:06 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:688c1b8a20d59eaa9f080eff757ab08f8a7f24a6c66e539d7f3b607dca35e400`  
		Last Modified: Thu, 11 Jun 2026 00:31:44 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0922577b528c0b884216291c6c0b7920ef121caead896669721c37826abe7c4`  
		Last Modified: Thu, 11 Jun 2026 00:31:48 GMT  
		Size: 110.2 MB (110168539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0570d8d8450026024176866385722f911479ee1990f7839788e9189f1c93349`  
		Last Modified: Thu, 11 Jun 2026 00:31:44 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e40b4dee1ddd6ebca291249192b5c3c5ee95912e83051969debb0b7bc6a00314`  
		Last Modified: Thu, 11 Jun 2026 00:31:45 GMT  
		Size: 13.9 MB (13879138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7afb5801704d0009d148a022abaf0e0ac3cac6f1f432553bf58a2d5a09fb5e6f`  
		Last Modified: Thu, 11 Jun 2026 00:31:46 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a84f2193c16a0ea802cc7d0bc8bdab3f6b9d79be3fcb37545995300e64ecf2f`  
		Last Modified: Thu, 11 Jun 2026 00:31:46 GMT  
		Size: 13.5 MB (13476408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6f854364f75295f7a4bce264d10e6b203ab380b7ba3bdd8583a99352e982737`  
		Last Modified: Thu, 11 Jun 2026 00:31:47 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72f9bc940a2094aeaaaba936eeffeda10818c16b0bc988899f4130db3efbb5a`  
		Last Modified: Thu, 11 Jun 2026 00:31:47 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:135fbed6fbd9d8f5aef4270fa99587ccc15e3770b70346bc7ad412476380542b`  
		Last Modified: Thu, 11 Jun 2026 00:31:48 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:439a1d54d1dd27c6ff27d7c6eb62bab2fcb1903eb0979638370b1b6f2a274864`  
		Last Modified: Thu, 11 Jun 2026 00:31:48 GMT  
		Size: 9.3 KB (9270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f86ebd73c01381c55038d183d1b6ce2714b26ba150bb5b071f8225d54febff`  
		Last Modified: Thu, 11 Jun 2026 02:40:34 GMT  
		Size: 19.8 MB (19801849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb07ffa081265e5629c9260f5229def7eb1f8fface0108276e41ec9fc12e4a36`  
		Last Modified: Thu, 11 Jun 2026 02:40:35 GMT  
		Size: 37.0 MB (36967536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38779f4f9b048b2b75d6d35b1843358bfb143fcc8060cf90e3bfac76a8543e7e`  
		Last Modified: Thu, 11 Jun 2026 02:40:33 GMT  
		Size: 792.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9faf3a3c88f8a13a0c0795a58d664b8cb32801e17b07b4e187d1ada3e531f9d`  
		Last Modified: Thu, 11 Jun 2026 02:40:39 GMT  
		Size: 266.2 MB (266155182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0688b3a0baf92ba8cca61c58c1ae980427e60de03565ab901bfad7d6c031983c`  
		Last Modified: Thu, 11 Jun 2026 02:40:34 GMT  
		Size: 4.1 KB (4134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfba54a18fa617346d121a11ce3aa26d989e34bf67acf8151c8276bd67b87cfd`  
		Last Modified: Thu, 11 Jun 2026 02:40:36 GMT  
		Size: 2.4 KB (2354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:fpm` - unknown; unknown

```console
$ docker pull nextcloud@sha256:8e49102496e6527056b99c6ee6be6270aadb9d9d65ec0718650b6a4674a4e086
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 KB (46871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e1bfe04f289dd0eb753b2135e8f5e66f834950896e6b88b48f33b5d67a3ed8`

```dockerfile
```

-	Layers:
	-	`sha256:90012d9128988587be2769758baeeb46d621513176002c504ac6eeda58fd6201`  
		Last Modified: Thu, 11 Jun 2026 02:40:33 GMT  
		Size: 46.9 KB (46871 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:fpm` - linux; 386

```console
$ docker pull nextcloud@sha256:92104a880704c85e41014ba5a40ac4e34e2cb35a2b58a977b3799af3dbb7aab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **500.5 MB (500452097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:513e0b460fce905b6afc41e019d55e56cf175d86c62a5490c5145eb4967a8210`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:19:06 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 11 Jun 2026 00:19:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Jun 2026 00:19:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 00:19:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jun 2026 00:19:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 11 Jun 2026 00:19:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 00:19:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 00:19:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jun 2026 00:19:24 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 11 Jun 2026 00:19:24 GMT
ENV PHP_VERSION=8.4.22
# Thu, 11 Jun 2026 00:19:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.22.tar.xz.asc
# Thu, 11 Jun 2026 00:19:24 GMT
ENV PHP_SHA256=696c0f6ad92e94c59059c1eb6e300842b8d050934226efcdf00f2a413cb083cf
# Thu, 11 Jun 2026 00:23:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 11 Jun 2026 00:23:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:26:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 11 Jun 2026 00:26:39 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:26:39 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 11 Jun 2026 00:26:39 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 11 Jun 2026 00:26:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Jun 2026 00:26:39 GMT
WORKDIR /var/www/html
# Thu, 11 Jun 2026 00:26:39 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 11 Jun 2026 00:26:39 GMT
STOPSIGNAL SIGQUIT
# Thu, 11 Jun 2026 00:26:39 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 11 Jun 2026 00:26:39 GMT
CMD ["php-fpm"]
# Thu, 11 Jun 2026 02:35:29 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-7.q16-10-extra         rsync     ;     apt-get dist-clean;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Thu, 11 Jun 2026 02:37:37 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 11 Jun 2026 02:37:37 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 11 Jun 2026 02:37:37 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Thu, 11 Jun 2026 02:37:37 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         liblz4-dev         libmagickwand-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-ftp-ssl;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.28;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.1;     pecl install --configureoptions 'enable-memcached-igbinary="yes"'         memcached-3.4.0;     pecl install --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"'         redis-6.3.0;         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -rt dpkg-query --search         | awk 'sub(":$", "", $1) { print $1 }'         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 02:37:37 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Thu, 11 Jun 2026 02:37:37 GMT
VOLUME [/var/www/html]
# Thu, 11 Jun 2026 02:37:37 GMT
ENV NEXTCLOUD_VERSION=34.0.0
# Thu, 11 Jun 2026 02:38:13 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://github.com/nextcloud-releases/server/releases/download/v34.0.0/nextcloud-34.0.0.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://github.com/nextcloud-releases/server/releases/download/v34.0.0/nextcloud-34.0.0.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 02:38:13 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 11 Jun 2026 02:38:13 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Thu, 11 Jun 2026 02:38:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 02:38:13 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:720f951a68f4f9ab464e52b53cf88cfb86bc876b3f00956d000420777ab93c0c`  
		Last Modified: Wed, 10 Jun 2026 23:40:30 GMT  
		Size: 31.3 MB (31301194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b774c28ecbe633143c5640dc1f8f65a8e93b1db9a88a9f8fe4aa108cce9f3d45`  
		Last Modified: Thu, 11 Jun 2026 00:23:11 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b278706aad66551ce362285547af135f0fd9e6a240e2a326a82052d789a55d`  
		Last Modified: Thu, 11 Jun 2026 00:23:15 GMT  
		Size: 116.1 MB (116142269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea11b6ee5bcd9e7d652076f123746f9357f0fb71cf2b8a6dc39c2279103425dc`  
		Last Modified: Thu, 11 Jun 2026 00:23:11 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71eece14f52e7ab6dff6a9f6c58da380c4a2fc4a5294115855c571be9164dcf5`  
		Last Modified: Thu, 11 Jun 2026 00:26:51 GMT  
		Size: 13.9 MB (13878436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502cc5c6848574ef589e8da0bef6d67325d8a60622e4f6a5948c3a313043e1e2`  
		Last Modified: Thu, 11 Jun 2026 00:26:50 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea51d98fa26a009d394def78581c969c019682a6c2a67c8fceed65a6add4a05`  
		Last Modified: Thu, 11 Jun 2026 00:26:50 GMT  
		Size: 14.1 MB (14106547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a530980c51b2cf815a464df9f158714246ecdfd7be40d1b1d4e6d649f061a0ec`  
		Last Modified: Thu, 11 Jun 2026 00:26:50 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:874956e0001d6794683d041ca39fc5bffaead9870d51ae57082482a62130ccad`  
		Last Modified: Thu, 11 Jun 2026 00:26:51 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3779d515d2a9e765fc2a42dfe82ca91e505aa9dcc8f5ea88c45c00cd2a67a654`  
		Last Modified: Thu, 11 Jun 2026 00:26:51 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:490d66a77c1f741bd75e1860dbc343c14f672d0e7db75ab0777d22033615a5e0`  
		Last Modified: Thu, 11 Jun 2026 00:26:52 GMT  
		Size: 9.3 KB (9265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e784e822b1d08ff26cd856917132f8a0545cae5e130b90623d0e433f0f46e5`  
		Last Modified: Thu, 11 Jun 2026 02:38:38 GMT  
		Size: 21.3 MB (21343819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:117b174b6102b1b2ac27802805f2b6ef9c15aab2759225be9b1e164db8667895`  
		Last Modified: Thu, 11 Jun 2026 02:38:39 GMT  
		Size: 37.5 MB (37498525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e15fdcd3e8b0977d8cbf6c7a7b97cf025fa801e0bbe505d7d24c41d589bfb9a`  
		Last Modified: Thu, 11 Jun 2026 02:38:37 GMT  
		Size: 787.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582c856d176316424daf3f32ed8f683c1e777b2d8621aa91a31b1d70481d10a5`  
		Last Modified: Thu, 11 Jun 2026 02:38:44 GMT  
		Size: 266.2 MB (266160842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a91221f68b397c67a324172d11e074e778038a66ad3a0b7bb407c0fae60e4c`  
		Last Modified: Thu, 11 Jun 2026 02:38:38 GMT  
		Size: 4.1 KB (4134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83caef30fb9b2c3629df9bcdda6d2bf68860c9ba9e16cd311c3160b4043ac215`  
		Last Modified: Thu, 11 Jun 2026 02:38:40 GMT  
		Size: 2.4 KB (2355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:fpm` - unknown; unknown

```console
$ docker pull nextcloud@sha256:7e712d455cabce175286af26a87d05ad5fe4c96330f2f5bd1313601eea3f3e08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 KB (46684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e15ba9ab89dc90b288555a09bf05f9e2b62d4ce1170923efbc5f4aa933f4d9e`

```dockerfile
```

-	Layers:
	-	`sha256:55341d875f7de93debadbc7f49b3c5af8ea1713b3cf43fb14a58ce6f6fec924b`  
		Last Modified: Thu, 11 Jun 2026 02:38:37 GMT  
		Size: 46.7 KB (46684 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:fpm` - linux; ppc64le

```console
$ docker pull nextcloud@sha256:328c5e3292485b7536b96ef79af4535aea8056fba61f45103d224bd5aca2265e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **498.6 MB (498571334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57090b5ca463eec6b9c59acbc9eb5e4619313b58f9149ee1b50916fcb9a61ef2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 03:00:24 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 11 Jun 2026 03:01:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Jun 2026 03:01:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 03:01:02 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jun 2026 03:01:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 11 Jun 2026 03:01:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 03:01:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 03:01:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jun 2026 03:01:03 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 11 Jun 2026 03:01:03 GMT
ENV PHP_VERSION=8.4.22
# Thu, 11 Jun 2026 03:01:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.22.tar.xz.asc
# Thu, 11 Jun 2026 03:01:03 GMT
ENV PHP_SHA256=696c0f6ad92e94c59059c1eb6e300842b8d050934226efcdf00f2a413cb083cf
# Thu, 11 Jun 2026 03:22:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 11 Jun 2026 03:22:41 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 03:31:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 11 Jun 2026 03:31:18 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 03:31:18 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 11 Jun 2026 03:31:19 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 11 Jun 2026 03:31:19 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Jun 2026 03:31:19 GMT
WORKDIR /var/www/html
# Thu, 11 Jun 2026 03:31:19 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 11 Jun 2026 03:31:19 GMT
STOPSIGNAL SIGQUIT
# Thu, 11 Jun 2026 03:31:19 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 11 Jun 2026 03:31:19 GMT
CMD ["php-fpm"]
# Thu, 11 Jun 2026 12:12:04 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-7.q16-10-extra         rsync     ;     apt-get dist-clean;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Thu, 11 Jun 2026 12:16:33 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 11 Jun 2026 12:16:33 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 11 Jun 2026 12:16:33 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Thu, 11 Jun 2026 12:16:33 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         liblz4-dev         libmagickwand-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-ftp-ssl;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.28;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.1;     pecl install --configureoptions 'enable-memcached-igbinary="yes"'         memcached-3.4.0;     pecl install --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"'         redis-6.3.0;         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -rt dpkg-query --search         | awk 'sub(":$", "", $1) { print $1 }'         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 12:16:34 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Thu, 11 Jun 2026 12:16:34 GMT
VOLUME [/var/www/html]
# Thu, 11 Jun 2026 12:16:34 GMT
ENV NEXTCLOUD_VERSION=34.0.0
# Thu, 11 Jun 2026 12:17:24 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://github.com/nextcloud-releases/server/releases/download/v34.0.0/nextcloud-34.0.0.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://github.com/nextcloud-releases/server/releases/download/v34.0.0/nextcloud-34.0.0.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 12:17:25 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 11 Jun 2026 12:17:25 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Thu, 11 Jun 2026 12:17:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 12:17:25 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:9d6b2e320e2b74843186d830e8202c50ebfaeccf823d239e3e3e349a8a508d80`  
		Last Modified: Thu, 11 Jun 2026 00:24:42 GMT  
		Size: 33.6 MB (33606340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76942a34176bffe275c52bbf371c6a83affed73bab30526f495165cbc094b557`  
		Last Modified: Thu, 11 Jun 2026 03:06:17 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d446e1e0a4b12d658b3e858628249ee37b9a22d29bee0c2dd4686159c2e43988`  
		Last Modified: Thu, 11 Jun 2026 03:06:22 GMT  
		Size: 109.6 MB (109598344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e8bcde33298859f8eb941222505617b97a665c07395dc23100212e1d7a25d8`  
		Last Modified: Thu, 11 Jun 2026 03:06:17 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e16120f0e14a8b6a5673d64c49b3126a843ff8af5a37ba62b0f5f9725979f64`  
		Last Modified: Thu, 11 Jun 2026 03:27:17 GMT  
		Size: 13.9 MB (13878523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0add12a0a36b7e6a3359e44e5c379f682b427da27f977a51a0e87700d6c50c6d`  
		Last Modified: Thu, 11 Jun 2026 03:27:17 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b2868a12b085c5487e8c446f30681210ad035029b12cf898e725639bed2a2ea`  
		Last Modified: Thu, 11 Jun 2026 03:31:50 GMT  
		Size: 14.3 MB (14348297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da986ada0a3630c3001374aa0b12bcffaa865272195d760f0f9547e1bd57bee`  
		Last Modified: Thu, 11 Jun 2026 03:31:50 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb65de290f5f1d75b0f41f301283ddfeb80ed7c81e992ecd8c2fb80c3a91c6e`  
		Last Modified: Thu, 11 Jun 2026 03:31:50 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089cfdf72973aa92371417dc861312a50981c175411d8c79efb74b174fd738a2`  
		Last Modified: Thu, 11 Jun 2026 03:31:50 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3df1744de7b46be471a6c3bc45bf78cf4ed9cc76601ea3ff2f438a4c020c34b0`  
		Last Modified: Thu, 11 Jun 2026 03:31:51 GMT  
		Size: 9.3 KB (9268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa05f0aa0c9ef2c349476f86d750fd21999cfb986e75cc2bc578f366dca36f0`  
		Last Modified: Thu, 11 Jun 2026 12:18:13 GMT  
		Size: 22.2 MB (22171913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7176fc35ee3e1da668646ade8adc48ce8cf32407410e7a29d0d1176407376c65`  
		Last Modified: Thu, 11 Jun 2026 12:18:14 GMT  
		Size: 38.8 MB (38792027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477e07aea565b85053d0bbe8b879924f79c098545ae760606f1fe33fd4d278ad`  
		Last Modified: Thu, 11 Jun 2026 12:18:12 GMT  
		Size: 795.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af87e154095c6741a8ba24ac1db74d3d2b7dc78e41e76f9d28c2adf46017241`  
		Last Modified: Thu, 11 Jun 2026 12:18:20 GMT  
		Size: 266.2 MB (266155413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70f2470c4d8286886490c30df354316ac97fa36acbc458d351a869258132bf7`  
		Last Modified: Thu, 11 Jun 2026 12:18:13 GMT  
		Size: 4.1 KB (4134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b02ef7be4d98c26d5af6caa6c31a4983483fb24d345eec21d6116dec9dce1c`  
		Last Modified: Thu, 11 Jun 2026 12:18:15 GMT  
		Size: 2.4 KB (2356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:fpm` - unknown; unknown

```console
$ docker pull nextcloud@sha256:ee523ca650448537bdaec6ae1eb7728e73cb0d0fcd5869d83494b2144e7015eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 KB (46772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d435ec7d90f1d63e8b8b177f4f66fbadb9f59df5525170b75bb7148199715c1`

```dockerfile
```

-	Layers:
	-	`sha256:d8ec8e0f6954c5dcaf94fc7c6c2a732709bdde6bfa888aee42774cf35ad108a0`  
		Last Modified: Thu, 11 Jun 2026 12:18:11 GMT  
		Size: 46.8 KB (46772 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:fpm` - linux; riscv64

```console
$ docker pull nextcloud@sha256:8244e855009d5be683266d28258c5c70e3a9a382ca1db26036541788545e4307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **533.7 MB (533696687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28cc2fcaafdf1d0d1e581d46166ad1ee1a3d61fdcb071a0b20176a88fb743f70`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1781049600'
# Fri, 12 Jun 2026 06:14:57 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 12 Jun 2026 06:17:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 12 Jun 2026 06:17:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jun 2026 06:17:02 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 12 Jun 2026 06:17:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 12 Jun 2026 06:17:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Jun 2026 06:17:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Jun 2026 06:17:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 12 Jun 2026 06:17:03 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 12 Jun 2026 06:17:03 GMT
ENV PHP_VERSION=8.4.22
# Fri, 12 Jun 2026 06:17:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.22.tar.xz.asc
# Fri, 12 Jun 2026 06:17:03 GMT
ENV PHP_SHA256=696c0f6ad92e94c59059c1eb6e300842b8d050934226efcdf00f2a413cb083cf
# Mon, 15 Jun 2026 05:11:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 15 Jun 2026 05:11:12 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 15 Jun 2026 08:03:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 15 Jun 2026 08:03:08 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 15 Jun 2026 08:03:09 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 15 Jun 2026 08:03:10 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 15 Jun 2026 08:03:10 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 15 Jun 2026 08:03:10 GMT
WORKDIR /var/www/html
# Mon, 15 Jun 2026 08:03:10 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 15 Jun 2026 08:03:10 GMT
STOPSIGNAL SIGQUIT
# Mon, 15 Jun 2026 08:03:10 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 15 Jun 2026 08:03:10 GMT
CMD ["php-fpm"]
# Tue, 16 Jun 2026 04:52:10 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-7.q16-10-extra         rsync     ;     apt-get dist-clean;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Tue, 16 Jun 2026 05:21:08 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 16 Jun 2026 05:21:08 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 16 Jun 2026 05:21:08 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Tue, 16 Jun 2026 05:21:08 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         liblz4-dev         libmagickwand-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-ftp-ssl;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.28;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.1;     pecl install --configureoptions 'enable-memcached-igbinary="yes"'         memcached-3.4.0;     pecl install --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"'         redis-6.3.0;         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -rt dpkg-query --search         | awk 'sub(":$", "", $1) { print $1 }'         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     apt-get dist-clean # buildkit
# Tue, 16 Jun 2026 05:21:08 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Tue, 16 Jun 2026 05:21:08 GMT
VOLUME [/var/www/html]
# Tue, 16 Jun 2026 05:21:08 GMT
ENV NEXTCLOUD_VERSION=34.0.0
# Tue, 16 Jun 2026 05:49:51 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://github.com/nextcloud-releases/server/releases/download/v34.0.0/nextcloud-34.0.0.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://github.com/nextcloud-releases/server/releases/download/v34.0.0/nextcloud-34.0.0.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     apt-get dist-clean # buildkit
# Tue, 16 Jun 2026 05:49:52 GMT
COPY *.sh upgrade.exclude / # buildkit
# Tue, 16 Jun 2026 05:49:53 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Tue, 16 Jun 2026 05:49:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Jun 2026 05:49:53 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:0b510fe8545cab831b696965b5a825649c5c945581e912d31a08a0b30ff940c0`  
		Last Modified: Thu, 11 Jun 2026 03:01:06 GMT  
		Size: 28.3 MB (28282305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d877ba68e482a33a75fd5c2ad03cd220a291d8e1a9914f9501f41f97050fdf6`  
		Last Modified: Fri, 12 Jun 2026 07:21:36 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcbcfd8d49be980430164d80eb573cd408281b5735067cbdbe0d0ff42f6a5f62`  
		Last Modified: Fri, 12 Jun 2026 07:22:03 GMT  
		Size: 146.6 MB (146585237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cccce4250e607f18d72142d293e6bb27d27ab552c53e10d06fef4ba0a75bca2`  
		Last Modified: Fri, 12 Jun 2026 07:21:36 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e48b93d11829454c64d4a03656d5a2ab7f676977e48f914da4deee8c44c300`  
		Last Modified: Mon, 15 Jun 2026 06:08:09 GMT  
		Size: 13.9 MB (13894036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812837b8db071ce4a87a4a260773987b2941fb0e07bbfa16044e9f852c270662`  
		Last Modified: Mon, 15 Jun 2026 06:08:04 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4036f37277ecd62c094d4356dd6fa47d8fe3f4fa263735d30b77deb89c74b37`  
		Last Modified: Mon, 15 Jun 2026 08:06:10 GMT  
		Size: 13.3 MB (13257949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a5fc108b92ddf0b9ffc2f4d2ecd30eca7abb7194c8879a0c29d4c2735a1fac`  
		Last Modified: Mon, 15 Jun 2026 08:06:07 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e26c4b35856528a60d47bb3e544f2901d1f41ca70c842a5c41659e769a7af51`  
		Last Modified: Mon, 15 Jun 2026 08:06:07 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853b60ab19fe309f7953c59ddfcef3af308b366a5ce7314b0491d2bfc30eefbe`  
		Last Modified: Mon, 15 Jun 2026 08:06:07 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac557c3cf8d23eaf2622d7cfe687e6ba17addb8131feaf8b334e91855ed5108d`  
		Last Modified: Mon, 15 Jun 2026 08:06:09 GMT  
		Size: 9.3 KB (9268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91328348f8f2cd36fa91c6aed76671218cb25ca682fd245a15d8ea58f01dda56`  
		Last Modified: Tue, 16 Jun 2026 05:32:20 GMT  
		Size: 19.6 MB (19569449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8205395754190957dbc8c05320dc389bb4363ddedb6752bcf07927c6efc73090`  
		Last Modified: Tue, 16 Jun 2026 05:32:28 GMT  
		Size: 45.9 MB (45932036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86875f2e284c5a0703c853bd508dd3f1633062560c06be47e26d53326c359162`  
		Last Modified: Tue, 16 Jun 2026 05:32:12 GMT  
		Size: 792.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88013dd6f7dee6e9b3991491076f7debaa1159bbf612c74245d384a29b63d6d`  
		Last Modified: Tue, 16 Jun 2026 05:57:02 GMT  
		Size: 266.2 MB (266155194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102025c73babad1b70e59f987525766c42541d947a93e65b9a2e74c9d62b52b5`  
		Last Modified: Tue, 16 Jun 2026 05:56:22 GMT  
		Size: 4.1 KB (4136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9cc5b7dd418eb8342b12543fcb4dc54ecb14e73b26e73e7461c608eb49ddd99`  
		Last Modified: Tue, 16 Jun 2026 05:56:22 GMT  
		Size: 2.4 KB (2359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:fpm` - unknown; unknown

```console
$ docker pull nextcloud@sha256:e841dc41b5d1fb1007f6a4bdefbc2ffd66220c128e507fe920506f9db70a427c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 KB (46769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceaa8879b28a1446c466395a9821e57768aa15dbc8932b3afe0a4b24a1212325`

```dockerfile
```

-	Layers:
	-	`sha256:a3576650eda49fddbb5feb4b3acadf779e815d9480efa2f8e9a987c5cf1f4a64`  
		Last Modified: Tue, 16 Jun 2026 05:56:22 GMT  
		Size: 46.8 KB (46769 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:fpm` - linux; s390x

```console
$ docker pull nextcloud@sha256:0bb5952a5be85195023d7c079288dee35e0499dfd9d0b71b93da28772813bd11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **473.7 MB (473732656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d8adb5e2f21a1ede91f201fd03143d70a03dd02642ee35d369d3ee25699390`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:21:26 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 11 Jun 2026 00:21:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Jun 2026 00:21:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 00:21:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jun 2026 00:21:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 11 Jun 2026 00:21:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 00:21:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 00:21:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jun 2026 00:21:41 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 11 Jun 2026 00:21:41 GMT
ENV PHP_VERSION=8.4.22
# Thu, 11 Jun 2026 00:21:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.22.tar.xz.asc
# Thu, 11 Jun 2026 00:21:41 GMT
ENV PHP_SHA256=696c0f6ad92e94c59059c1eb6e300842b8d050934226efcdf00f2a413cb083cf
# Thu, 11 Jun 2026 00:35:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 11 Jun 2026 00:35:50 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:40:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 11 Jun 2026 00:40:18 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:40:18 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 11 Jun 2026 00:40:18 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 11 Jun 2026 00:40:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Jun 2026 00:40:18 GMT
WORKDIR /var/www/html
# Thu, 11 Jun 2026 00:40:18 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 11 Jun 2026 00:40:18 GMT
STOPSIGNAL SIGQUIT
# Thu, 11 Jun 2026 00:40:18 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 11 Jun 2026 00:40:18 GMT
CMD ["php-fpm"]
# Thu, 11 Jun 2026 03:53:52 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-7.q16-10-extra         rsync     ;     apt-get dist-clean;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Thu, 11 Jun 2026 03:56:06 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 11 Jun 2026 03:56:06 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 11 Jun 2026 03:56:06 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Thu, 11 Jun 2026 03:56:06 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         liblz4-dev         libmagickwand-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-ftp-ssl;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.28;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.1;     pecl install --configureoptions 'enable-memcached-igbinary="yes"'         memcached-3.4.0;     pecl install --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"'         redis-6.3.0;         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -rt dpkg-query --search         | awk 'sub(":$", "", $1) { print $1 }'         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 03:56:06 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Thu, 11 Jun 2026 03:56:06 GMT
VOLUME [/var/www/html]
# Thu, 11 Jun 2026 03:56:06 GMT
ENV NEXTCLOUD_VERSION=34.0.0
# Thu, 11 Jun 2026 03:56:40 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://github.com/nextcloud-releases/server/releases/download/v34.0.0/nextcloud-34.0.0.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://github.com/nextcloud-releases/server/releases/download/v34.0.0/nextcloud-34.0.0.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 03:56:41 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 11 Jun 2026 03:56:41 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Thu, 11 Jun 2026 03:56:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 03:56:41 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:760dcf74fdfe93300ce15b5b23adf9aa4af45b6ba9d69925863198f64881a537`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 29.9 MB (29851354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31ad3e73b8cdb7ce428b4db4a7406f5cdaba7fa5ca3da43d600aa5d3a542427`  
		Last Modified: Thu, 11 Jun 2026 00:26:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c85435c8606500c59db786c99673bf9dca6ad3e039f9eb843e32670663f1d4`  
		Last Modified: Thu, 11 Jun 2026 00:26:07 GMT  
		Size: 92.6 MB (92572593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f26a046c66c96683a2d97217fae99364f5759c3f629f89e2acd659296dd5c23`  
		Last Modified: Thu, 11 Jun 2026 00:26:05 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8e4ed1f56148189cd4f076286be7103eca9e84bc663683ccea88219d50a91a`  
		Last Modified: Thu, 11 Jun 2026 00:40:14 GMT  
		Size: 13.9 MB (13877693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9675a28df4b1f66ec1115d676c9f8ba7f865bbd3e2daffe61eac6cebb4d51850`  
		Last Modified: Thu, 11 Jun 2026 00:40:14 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de96746c109d9d730665dca0ed0e151fcd25b1d96589d5b977e4ccb1dbf4cbd4`  
		Last Modified: Thu, 11 Jun 2026 00:40:34 GMT  
		Size: 13.6 MB (13594527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c9cd0ff56679d7a8c7eb4f330bc0965e98fa872826e792f764ad0e524d86bd`  
		Last Modified: Thu, 11 Jun 2026 00:40:34 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a7d32e20c39ac2d665b0a96699b88969f984dfe20d23e2d0ff8aadebca343b`  
		Last Modified: Thu, 11 Jun 2026 00:40:34 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf364688543eed09ddf160e8ef3b583554b375a7afc0229b5106bb086141a5ea`  
		Last Modified: Thu, 11 Jun 2026 00:40:34 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31a2999bbb45583db75570741735afba0d7499ce5d80b9ae9c916896142ae9e8`  
		Last Modified: Thu, 11 Jun 2026 00:40:35 GMT  
		Size: 9.3 KB (9267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d73ff9735008cedc3a529a6102933128b7ef82169cc39d5cd1bd909bbc30fd`  
		Last Modified: Thu, 11 Jun 2026 03:57:20 GMT  
		Size: 20.4 MB (20426494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bea425e7ead463dd00267ef6721c7e46851db2223c9600ec24f92ac625ff88fa`  
		Last Modified: Thu, 11 Jun 2026 03:57:21 GMT  
		Size: 37.2 MB (37236458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee810e8a4d977a003d9aadd5874c64fff00c51d22488fcaaf4a3c6a9ff2f93a`  
		Last Modified: Thu, 11 Jun 2026 03:57:19 GMT  
		Size: 791.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fdb04ed099a93fe24b4a495a5c6a24dfe0bb641375c39fd24d3336a5c061368`  
		Last Modified: Thu, 11 Jun 2026 03:57:26 GMT  
		Size: 266.2 MB (266153070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:664517fc7cf30334c26df95f5b4a2f60e867abd3faa5d5cd4bf55e8fbb578086`  
		Last Modified: Thu, 11 Jun 2026 03:57:21 GMT  
		Size: 4.1 KB (4136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1582372666c41e7e4b77995a29d2eb23d1fd38f6b2d877b1a769e55a099f648e`  
		Last Modified: Thu, 11 Jun 2026 03:57:22 GMT  
		Size: 2.4 KB (2354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:fpm` - unknown; unknown

```console
$ docker pull nextcloud@sha256:400275ffd3e5e03290c2f91ca9e802afb7fecf628f47599be567246e5254a78b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 KB (46715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23384bde5ece6aa1462548b4d7b9af8d8a515ff7376fe903eab9e4d601a2ce9c`

```dockerfile
```

-	Layers:
	-	`sha256:32f59af7bab44d565b0a4939d83299fa2c55ec188542f9ed8f2cc0a641cc645f`  
		Last Modified: Thu, 11 Jun 2026 03:57:19 GMT  
		Size: 46.7 KB (46715 bytes)  
		MIME: application/vnd.in-toto+json
