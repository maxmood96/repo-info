## `nextcloud:production-fpm`

```console
$ docker pull nextcloud@sha256:02acd0e639f8e3c885ce49b4f0e544c1df7bfd65c1754b520cbba07432a34231
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nextcloud:production-fpm` - linux; amd64

```console
$ docker pull nextcloud@sha256:32978a2c0e570665aefddb42cb0875389493c69ef50c4f27607dfb9c7c381b0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.4 MB (424404814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b099efac306e2f1d0c82e4ba0d743ddea1a75381c6a616b33c647fd40057f53`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 13 Mar 2025 21:54:41 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Thu, 13 Mar 2025 21:54:41 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 13 Mar 2025 21:54:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Mar 2025 21:54:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 21:54:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 21:54:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Mar 2025 21:54:41 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 13 Mar 2025 21:54:41 GMT
ENV PHP_VERSION=8.2.28
# Thu, 13 Mar 2025 21:54:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.28.tar.xz.asc
# Thu, 13 Mar 2025 21:54:41 GMT
ENV PHP_SHA256=af8c9153153a7f489153b7a74f2f29a5ee36f5cb2c6c6929c98411a577e89c91
# Thu, 13 Mar 2025 21:54:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Mar 2025 21:54:41 GMT
WORKDIR /var/www/html
# Thu, 13 Mar 2025 21:54:41 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Mar 2025 21:54:41 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 13 Mar 2025 21:54:41 GMT
CMD ["php-fpm"]
# Fri, 14 Mar 2025 00:34:18 GMT
ENV IMAGICK_COMMIT_HASH=d7d3c24af1b4f599897408f1714600b69a56473b
# Fri, 14 Mar 2025 00:34:18 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Fri, 14 Mar 2025 00:34:18 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 14 Mar 2025 00:34:18 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 14 Mar 2025 00:34:18 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Fri, 14 Mar 2025 00:34:18 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         curl -fsSL -o imagick.tar.gz "https://github.com/Imagick/imagick/archive/$IMAGICK_COMMIT_HASH.tar.gz";     tar -xzf imagick.tar.gz -C /tmp;     rm imagick.tar.gz;     cd "/tmp/imagick-$IMAGICK_COMMIT_HASH";     sed -i "s/@PACKAGE_VERSION@/git-$(echo ${IMAGICK_COMMIT_HASH} | cut -c 1-7)/" php_imagick.h;     phpize;     ./configure;     make;     make install;     cd;     rm -r "/tmp/imagick-$IMAGICK_COMMIT_HASH";         pecl install APCu-5.1.24;     pecl install igbinary-3.2.16;     pecl install memcached-3.3.0         --configureoptions 'enable-memcached-igbinary="yes"';     pecl install redis-6.1.0         --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"';         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Mar 2025 00:34:18 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Fri, 14 Mar 2025 00:34:18 GMT
VOLUME [/var/www/html]
# Fri, 14 Mar 2025 00:34:18 GMT
ENV NEXTCLOUD_VERSION=30.0.7
# Fri, 14 Mar 2025 00:34:18 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-30.0.7.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-30.0.7.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Mar 2025 00:34:18 GMT
COPY *.sh upgrade.exclude / # buildkit
# Fri, 14 Mar 2025 00:34:18 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Fri, 14 Mar 2025 00:34:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 14 Mar 2025 00:34:18 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ac5e2fa4b03fb07137b84ea7150232706e5334b3ec3c0715624ad23d1227034`  
		Last Modified: Mon, 17 Mar 2025 23:22:55 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10826182397f681033d1c9798a0c3fddbcb0e142e43251bb9b288a13bae14e4`  
		Last Modified: Mon, 17 Mar 2025 23:22:58 GMT  
		Size: 104.3 MB (104329064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfd77ec8e8b92d03c31b08b7d5d05e2a084313af539548e1883b4fc616ee110`  
		Last Modified: Mon, 17 Mar 2025 23:22:54 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b92331c142d99e0a02d29242d771320bc38a73a2799919f15eca4c9a3d160f3`  
		Last Modified: Mon, 17 Mar 2025 23:22:56 GMT  
		Size: 12.3 MB (12257341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8a9341d6d2d03a2c133b490e5562a2c86e0a7319a64c054a101324a9f2eac3`  
		Last Modified: Mon, 17 Mar 2025 23:22:56 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f012687f14e447d3133ad7b9dd2fa11fb2a174c9c9a5cec0a72ca3e4b6b5643`  
		Last Modified: Mon, 17 Mar 2025 23:22:57 GMT  
		Size: 27.6 MB (27587411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4267a4e73cff66756462ed8cd3f36a20b916a964c40e6957ad8f5e56787b1297`  
		Last Modified: Mon, 17 Mar 2025 23:22:57 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93750387fcc4d1128a6e342abad0997624551ad9642a426b3eb694e6e18c0b09`  
		Last Modified: Mon, 17 Mar 2025 23:22:57 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7987a1b53704b6066fc5d749a88266b529863ae0c7943aea919633c6cd9dc2c`  
		Last Modified: Mon, 17 Mar 2025 23:22:58 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20354fd829f659b308a9eece58c4650adb8704f2834a5a7772e675acf9d0f073`  
		Last Modified: Tue, 18 Mar 2025 00:25:25 GMT  
		Size: 22.9 MB (22905129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e858b1ee1a3776232595dda78e6fe4516096db86951fc1bbc764091e95c3b1a`  
		Last Modified: Tue, 18 Mar 2025 00:25:25 GMT  
		Size: 21.0 MB (20951610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9e940954871141adf8614e4a223e2f952eb67a3348a1e78fe4f18299ecbfe9`  
		Last Modified: Tue, 18 Mar 2025 00:25:24 GMT  
		Size: 792.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db8c978bbcdd05873df72edfe2e30a5b4bfef541dbe002a50df444d9613eaa9e`  
		Last Modified: Tue, 18 Mar 2025 00:25:28 GMT  
		Size: 208.1 MB (208149516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4c1d3d8c7006742daf8ce9ffbfec9206487b72d603a218f2ada58d6882e7ff7`  
		Last Modified: Tue, 18 Mar 2025 00:25:25 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9dbfe2b31cb059bfa87939db0770eff78ca33573d071f420156bc246894ab0`  
		Last Modified: Tue, 18 Mar 2025 00:25:26 GMT  
		Size: 2.4 KB (2355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:production-fpm` - unknown; unknown

```console
$ docker pull nextcloud@sha256:4623b5cd9d8e75b61b0055a390d5b6044281661a2d866bf379bb379e5a7a873d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 KB (47971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36f7fa3f17c37789d1307e453d777b71348d88f4c72184e225f358d1f61d0bb0`

```dockerfile
```

-	Layers:
	-	`sha256:9f738aa32c37ce0371014ec9c7ae0efcb0581acf5883a717bf4f1c21d235f059`  
		Last Modified: Tue, 18 Mar 2025 00:25:24 GMT  
		Size: 48.0 KB (47971 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:production-fpm` - linux; arm variant v5

```console
$ docker pull nextcloud@sha256:f26e6b00d789f2615e6427db6810d6380e2c0c46a634bd8e32ecbc3f0f2448bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.8 MB (393833396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0648fe0cdbc03e09be08a1d69f1744051301d49d3b1c5e3af61bed699f975ef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1740355200'
# Thu, 13 Mar 2025 21:54:41 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 13 Mar 2025 21:54:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Mar 2025 21:54:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 21:54:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 21:54:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Mar 2025 21:54:41 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 13 Mar 2025 21:54:41 GMT
ENV PHP_VERSION=8.2.28
# Thu, 13 Mar 2025 21:54:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.28.tar.xz.asc
# Thu, 13 Mar 2025 21:54:41 GMT
ENV PHP_SHA256=af8c9153153a7f489153b7a74f2f29a5ee36f5cb2c6c6929c98411a577e89c91
# Thu, 13 Mar 2025 21:54:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Mar 2025 21:54:41 GMT
WORKDIR /var/www/html
# Thu, 13 Mar 2025 21:54:41 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Mar 2025 21:54:41 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 13 Mar 2025 21:54:41 GMT
CMD ["php-fpm"]
# Fri, 14 Mar 2025 00:34:18 GMT
ENV IMAGICK_COMMIT_HASH=d7d3c24af1b4f599897408f1714600b69a56473b
# Fri, 14 Mar 2025 00:34:18 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Fri, 14 Mar 2025 00:34:18 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 14 Mar 2025 00:34:18 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 14 Mar 2025 00:34:18 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Fri, 14 Mar 2025 00:34:18 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         curl -fsSL -o imagick.tar.gz "https://github.com/Imagick/imagick/archive/$IMAGICK_COMMIT_HASH.tar.gz";     tar -xzf imagick.tar.gz -C /tmp;     rm imagick.tar.gz;     cd "/tmp/imagick-$IMAGICK_COMMIT_HASH";     sed -i "s/@PACKAGE_VERSION@/git-$(echo ${IMAGICK_COMMIT_HASH} | cut -c 1-7)/" php_imagick.h;     phpize;     ./configure;     make;     make install;     cd;     rm -r "/tmp/imagick-$IMAGICK_COMMIT_HASH";         pecl install APCu-5.1.24;     pecl install igbinary-3.2.16;     pecl install memcached-3.3.0         --configureoptions 'enable-memcached-igbinary="yes"';     pecl install redis-6.1.0         --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"';         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Mar 2025 00:34:18 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Fri, 14 Mar 2025 00:34:18 GMT
VOLUME [/var/www/html]
# Fri, 14 Mar 2025 00:34:18 GMT
ENV NEXTCLOUD_VERSION=30.0.7
# Fri, 14 Mar 2025 00:34:18 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-30.0.7.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-30.0.7.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Mar 2025 00:34:18 GMT
COPY *.sh upgrade.exclude / # buildkit
# Fri, 14 Mar 2025 00:34:18 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Fri, 14 Mar 2025 00:34:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 14 Mar 2025 00:34:18 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:d8a77b84d73cc90f2bbd622ec970d928c4f14e4be51927c88b7c15b7b6772382`  
		Last Modified: Tue, 25 Feb 2025 01:30:58 GMT  
		Size: 25.7 MB (25740630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3014e21b6e4396df02c7cc3c5f126fa29d531fa5a1ad0b40b80de6794ae2694`  
		Last Modified: Tue, 25 Feb 2025 02:51:17 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858e0a56f6198eb0af5102ce28eda7b5a34384f5b54701b7346487229bff9e9c`  
		Last Modified: Tue, 25 Feb 2025 02:51:20 GMT  
		Size: 82.0 MB (81993202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24b0f2499da71327f565769347ea1f63e9070dfa8385025f0465d80e603c361`  
		Last Modified: Tue, 25 Feb 2025 02:51:17 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:174fac8933fd96ad2b4d9895010a9ca8188774a0fc61d763fbf1e3c87172a5b1`  
		Last Modified: Fri, 14 Mar 2025 00:17:47 GMT  
		Size: 12.3 MB (12255703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4587da7b68faab1496da9e291bb6c94baef8d06f3421d63afe1e030a34b954`  
		Last Modified: Fri, 14 Mar 2025 00:17:45 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e787692425ce9c5b94a54a76d7be0dc8c9248fe49116c88affca601e87a140`  
		Last Modified: Fri, 14 Mar 2025 01:21:45 GMT  
		Size: 26.1 MB (26086910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbba49c677c0b55142ea8238fce0d47a9b81da4967a8c6dee28b45241cf84c96`  
		Last Modified: Fri, 14 Mar 2025 01:21:44 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b55b3f69c0c5b87bc560f356072b6fb7980dc02816addfd2411f76f80551fc`  
		Last Modified: Fri, 14 Mar 2025 01:21:44 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aac5a740a4680921dbf093b1c0a3b64f4effb8de42c318dc89aa36b4b717819`  
		Last Modified: Fri, 14 Mar 2025 01:21:45 GMT  
		Size: 9.2 KB (9186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7fcdd73487b97a4064f06a71d6eacdf1cd7ca40e586b8c817dbe82e3ff6d151`  
		Last Modified: Fri, 14 Mar 2025 03:21:23 GMT  
		Size: 20.0 MB (19990851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd903dbb44aad190f327113d35155a19b7e2424bcc3df4efc68038b6b694c20c`  
		Last Modified: Fri, 14 Mar 2025 03:21:23 GMT  
		Size: 19.6 MB (19598907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5b3ae981e5e13cfb2ee90a32115547730660b28afc1f8b9449866f704c6f39`  
		Last Modified: Fri, 14 Mar 2025 03:21:22 GMT  
		Size: 795.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ced900674e1bb0f87ccebf6ce5dd20b99d2010aea041dba619857ce4c8347f`  
		Last Modified: Fri, 14 Mar 2025 19:22:41 GMT  
		Size: 208.1 MB (208147304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb5650d5cfcb540d71ac869b41af9ccd8831f9fcdca800cef1ddf61ad59fc4b`  
		Last Modified: Fri, 14 Mar 2025 19:22:36 GMT  
		Size: 3.9 KB (3879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d3bd3e5478652bcb37922feaf3bb030ca3e5693dbec95b4da9f2bbf136b3f4`  
		Last Modified: Fri, 14 Mar 2025 19:22:36 GMT  
		Size: 2.4 KB (2357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:production-fpm` - unknown; unknown

```console
$ docker pull nextcloud@sha256:3344856c331dd9c64342fa7a0f2c27bd8a40dab2503a0b305589633c47b0d189
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 KB (48087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f117e8830d8601e14536e80b8baf0d7a856297dc8155af5a7ef7d1c54651ccc`

```dockerfile
```

-	Layers:
	-	`sha256:887f87e0bf4ed11f87b4a605704bdcdd38a71b7d2e60345c9e71c0784525df95`  
		Last Modified: Fri, 14 Mar 2025 19:22:36 GMT  
		Size: 48.1 KB (48087 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:production-fpm` - linux; arm variant v7

```console
$ docker pull nextcloud@sha256:415d1b594bd3acb043db853ef3263a80429ade178877eb6d60a64cb4d6cf0db8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.8 MB (382820888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4adebab93d1e48ac9e8af1a55f7d07fe8b514cc5180b75a981a527054e9f31c7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Thu, 13 Mar 2025 21:54:41 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 13 Mar 2025 21:54:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Mar 2025 21:54:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 21:54:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 21:54:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Mar 2025 21:54:41 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 13 Mar 2025 21:54:41 GMT
ENV PHP_VERSION=8.2.28
# Thu, 13 Mar 2025 21:54:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.28.tar.xz.asc
# Thu, 13 Mar 2025 21:54:41 GMT
ENV PHP_SHA256=af8c9153153a7f489153b7a74f2f29a5ee36f5cb2c6c6929c98411a577e89c91
# Thu, 13 Mar 2025 21:54:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Mar 2025 21:54:41 GMT
WORKDIR /var/www/html
# Thu, 13 Mar 2025 21:54:41 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Mar 2025 21:54:41 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 13 Mar 2025 21:54:41 GMT
CMD ["php-fpm"]
# Fri, 14 Mar 2025 00:34:18 GMT
ENV IMAGICK_COMMIT_HASH=d7d3c24af1b4f599897408f1714600b69a56473b
# Fri, 14 Mar 2025 00:34:18 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Fri, 14 Mar 2025 00:34:18 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 14 Mar 2025 00:34:18 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 14 Mar 2025 00:34:18 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Fri, 14 Mar 2025 00:34:18 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         curl -fsSL -o imagick.tar.gz "https://github.com/Imagick/imagick/archive/$IMAGICK_COMMIT_HASH.tar.gz";     tar -xzf imagick.tar.gz -C /tmp;     rm imagick.tar.gz;     cd "/tmp/imagick-$IMAGICK_COMMIT_HASH";     sed -i "s/@PACKAGE_VERSION@/git-$(echo ${IMAGICK_COMMIT_HASH} | cut -c 1-7)/" php_imagick.h;     phpize;     ./configure;     make;     make install;     cd;     rm -r "/tmp/imagick-$IMAGICK_COMMIT_HASH";         pecl install APCu-5.1.24;     pecl install igbinary-3.2.16;     pecl install memcached-3.3.0         --configureoptions 'enable-memcached-igbinary="yes"';     pecl install redis-6.1.0         --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"';         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Mar 2025 00:34:18 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Fri, 14 Mar 2025 00:34:18 GMT
VOLUME [/var/www/html]
# Fri, 14 Mar 2025 00:34:18 GMT
ENV NEXTCLOUD_VERSION=30.0.7
# Fri, 14 Mar 2025 00:34:18 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-30.0.7.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-30.0.7.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Mar 2025 00:34:18 GMT
COPY *.sh upgrade.exclude / # buildkit
# Fri, 14 Mar 2025 00:34:18 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Fri, 14 Mar 2025 00:34:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 14 Mar 2025 00:34:18 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:b47565bb13c54d9e609fa36aeddfc2e70b47de981bac54a6d090c2148f2f4fc4`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 23.9 MB (23919734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d7e09b1d1dfb9227526dbb14ab0477c0b3e235584b36c16282a130f9eb0f3c`  
		Last Modified: Tue, 25 Feb 2025 02:45:28 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195d4e13a8d04cec48669402c294b437f110e69a04f231bf7f4fb038ce009feb`  
		Last Modified: Tue, 25 Feb 2025 02:45:31 GMT  
		Size: 76.2 MB (76162862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f86b4b4427af4c394c935ad45142cba4e205bc21eb933d83f2d2432a5bb3cb64`  
		Last Modified: Tue, 25 Feb 2025 02:45:28 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd292a4a13daa7cb1bb02b5239391a1bf6e5b2a51b7f308c154b00d7cdad293`  
		Last Modified: Fri, 14 Mar 2025 01:30:07 GMT  
		Size: 12.3 MB (12255707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a369bd6b33fc90ed98625cb023a271ae762566f55e6db7d5a1855b75981d3aa`  
		Last Modified: Fri, 14 Mar 2025 01:30:06 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e770874e1c2fedb62da4ac1dad703395c6ff98844ff540a1bb067ad019aa8eea`  
		Last Modified: Fri, 14 Mar 2025 01:35:41 GMT  
		Size: 25.2 MB (25194955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc40a33224ac137c40c67fb59f5da4ecc33ef905b66a280be3f4f8319f43f42`  
		Last Modified: Fri, 14 Mar 2025 01:35:40 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:380a235120ac91ff9b8d7c81b3fac77969236409230b0e67525f012a4f655c88`  
		Last Modified: Fri, 14 Mar 2025 01:35:40 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:268b04975060b6494c22108ad89e386e2817ceadda8f988d3a6a91dd64e0697e`  
		Last Modified: Fri, 14 Mar 2025 01:35:40 GMT  
		Size: 9.2 KB (9183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f1dad4f8da4c0ac0bbf2dac84ef838c71f512df26e33ada21d041e66736689`  
		Last Modified: Fri, 14 Mar 2025 19:16:30 GMT  
		Size: 18.2 MB (18229646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29da3d02cf27f0cfd3b620d612ea320085b352afac16ecb12a8e8b839d2c6ab4`  
		Last Modified: Fri, 14 Mar 2025 19:16:30 GMT  
		Size: 18.9 MB (18891427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2ced5124badfc8c44cd268bc45f9e828f810cb35dc1c008178c356568eb493b`  
		Last Modified: Fri, 14 Mar 2025 19:16:29 GMT  
		Size: 797.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671cc221c66600d6287eda42fe75e3f5ed67941af8311433959915185775eeb8`  
		Last Modified: Fri, 14 Mar 2025 19:39:26 GMT  
		Size: 208.1 MB (208146665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f29d2b41d3a370d323bbec701123342cb09fa60c0488d0e7e5531d973035aa`  
		Last Modified: Fri, 14 Mar 2025 19:39:21 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346dd05433068bfc19e13f5bc472c3b3ea54cb05c7b2c8882e48a46b5a5377c5`  
		Last Modified: Fri, 14 Mar 2025 19:39:21 GMT  
		Size: 2.4 KB (2356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:production-fpm` - unknown; unknown

```console
$ docker pull nextcloud@sha256:9588426d3c224df67f35179b2609be62ba702430611cad0ceaa91572bf2c59d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 KB (48087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c7e35abc2a47fc6a47c2e0fe52296337f490dab8dc635ec096381b9a2bd65e2`

```dockerfile
```

-	Layers:
	-	`sha256:f0ee1aabf4cd0b4d43a316e2c1ed92b70a74286f61613351699732671c80c5a8`  
		Last Modified: Fri, 14 Mar 2025 19:39:21 GMT  
		Size: 48.1 KB (48087 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:production-fpm` - linux; arm64 variant v8

```console
$ docker pull nextcloud@sha256:6cbf4bcd65fceb844d5abd42397943a14897b3e47cfd25424e514c2d8bc2f61a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.6 MB (415579182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30da05bce1020e67f87a0c791b24bacf2cdd31d1e7d4729cb99c6c15424e9f4e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Thu, 13 Mar 2025 21:54:41 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 13 Mar 2025 21:54:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Mar 2025 21:54:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 21:54:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 21:54:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Mar 2025 21:54:41 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 13 Mar 2025 21:54:41 GMT
ENV PHP_VERSION=8.2.28
# Thu, 13 Mar 2025 21:54:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.28.tar.xz.asc
# Thu, 13 Mar 2025 21:54:41 GMT
ENV PHP_SHA256=af8c9153153a7f489153b7a74f2f29a5ee36f5cb2c6c6929c98411a577e89c91
# Thu, 13 Mar 2025 21:54:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Mar 2025 21:54:41 GMT
WORKDIR /var/www/html
# Thu, 13 Mar 2025 21:54:41 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Mar 2025 21:54:41 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 13 Mar 2025 21:54:41 GMT
CMD ["php-fpm"]
# Fri, 14 Mar 2025 00:34:18 GMT
ENV IMAGICK_COMMIT_HASH=d7d3c24af1b4f599897408f1714600b69a56473b
# Fri, 14 Mar 2025 00:34:18 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Fri, 14 Mar 2025 00:34:18 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 14 Mar 2025 00:34:18 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 14 Mar 2025 00:34:18 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Fri, 14 Mar 2025 00:34:18 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         curl -fsSL -o imagick.tar.gz "https://github.com/Imagick/imagick/archive/$IMAGICK_COMMIT_HASH.tar.gz";     tar -xzf imagick.tar.gz -C /tmp;     rm imagick.tar.gz;     cd "/tmp/imagick-$IMAGICK_COMMIT_HASH";     sed -i "s/@PACKAGE_VERSION@/git-$(echo ${IMAGICK_COMMIT_HASH} | cut -c 1-7)/" php_imagick.h;     phpize;     ./configure;     make;     make install;     cd;     rm -r "/tmp/imagick-$IMAGICK_COMMIT_HASH";         pecl install APCu-5.1.24;     pecl install igbinary-3.2.16;     pecl install memcached-3.3.0         --configureoptions 'enable-memcached-igbinary="yes"';     pecl install redis-6.1.0         --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"';         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Mar 2025 00:34:18 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Fri, 14 Mar 2025 00:34:18 GMT
VOLUME [/var/www/html]
# Fri, 14 Mar 2025 00:34:18 GMT
ENV NEXTCLOUD_VERSION=30.0.7
# Fri, 14 Mar 2025 00:34:18 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-30.0.7.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-30.0.7.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Mar 2025 00:34:18 GMT
COPY *.sh upgrade.exclude / # buildkit
# Fri, 14 Mar 2025 00:34:18 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Fri, 14 Mar 2025 00:34:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 14 Mar 2025 00:34:18 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31676cd976ed7c1a1f79275ef2602fefb67765b353e429d88aab3fd76863e399`  
		Last Modified: Tue, 25 Feb 2025 03:03:46 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e6e69341e71d07089c45827b72bbbf8ca0698042a25ca2375d9c71797edd77e`  
		Last Modified: Tue, 25 Feb 2025 03:03:49 GMT  
		Size: 98.1 MB (98130460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ee28dda6888ebc4fc51f7f52c135986c07171dad8ce5a8fafed9d2f65d62ec`  
		Last Modified: Tue, 25 Feb 2025 03:03:47 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac4232823be0667c82b09e794eae937ac24dda36546c7ae38d52080401a0653`  
		Last Modified: Fri, 14 Mar 2025 01:22:19 GMT  
		Size: 12.3 MB (12257233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21523d24049a2c116a9d8d26d1b9c462f11346258e50e227b6dd6f5fa0e4c78b`  
		Last Modified: Fri, 14 Mar 2025 01:22:19 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a3f83ad69a4a708ff1b6bdfa0ab1ff3794d99f7f70d67f09c02170f438cf52`  
		Last Modified: Fri, 14 Mar 2025 01:26:11 GMT  
		Size: 27.5 MB (27549576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8ebc55aa4a9d187acfc67ca269db5955831d0ba92097cb36b2438a1b477c60`  
		Last Modified: Fri, 14 Mar 2025 01:26:09 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35b089c64ee6309ae23275a3e06ef5b4e72bfdcd93b7065edd603b98c50885d`  
		Last Modified: Fri, 14 Mar 2025 01:26:09 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640c64ee926f7a87025196c1fdaaafa650ead8b5826de4adc0f31ee065809f20`  
		Last Modified: Fri, 14 Mar 2025 01:26:10 GMT  
		Size: 9.2 KB (9186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49412f835c4ba55cbd55fb5667f3cb63712baac55579b75a789b089e99d27db0`  
		Last Modified: Fri, 14 Mar 2025 22:55:15 GMT  
		Size: 20.3 MB (20259344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62032d7b7f6efc77946681bb2c36351ca2be18da26a21b07416ca792693041a3`  
		Last Modified: Fri, 14 Mar 2025 22:55:15 GMT  
		Size: 21.2 MB (21165613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48124d6235acc3a5708fbcec5325e7e47a431bc42e4394379ee110f29e899bcd`  
		Last Modified: Fri, 14 Mar 2025 22:55:14 GMT  
		Size: 797.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c3c623d90fdf6d4b3c345b62c37b379aedc01de28e529e4b84647f47c3cbd4d`  
		Last Modified: Fri, 14 Mar 2025 22:55:20 GMT  
		Size: 208.1 MB (208148639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe350c17a82bc8a4a90f804a127683457b7859eef9e43a2f8877e21e8efd644`  
		Last Modified: Fri, 14 Mar 2025 22:55:15 GMT  
		Size: 3.9 KB (3882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd43c307c97caccd0bdfdc8f1d322b73b0faed83ababbaa7c81f0f7c343c9ec`  
		Last Modified: Fri, 14 Mar 2025 22:55:16 GMT  
		Size: 2.4 KB (2358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:production-fpm` - unknown; unknown

```console
$ docker pull nextcloud@sha256:181db68033403a9037efe9dc66ce3ced0d888c1d626d77108020b1f1cb21b0f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 KB (48125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0d7d40a977c173d6f4815834bcd925f9c16aa2a849509e0ccc67e1c38d83612`

```dockerfile
```

-	Layers:
	-	`sha256:a6e658a6f47444db489c5d05df818cb6ec36f04ae9f579b342102f30617ea033`  
		Last Modified: Fri, 14 Mar 2025 22:55:14 GMT  
		Size: 48.1 KB (48125 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:production-fpm` - linux; 386

```console
$ docker pull nextcloud@sha256:fa54659c6ab683262c732af88c9e444761280fd8d561da107361b4606b26098a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.8 MB (422797427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3875058407aa4681527c74050f934747d1fc642a786885650ef82948f7e939a2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 13 Mar 2025 21:54:41 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
# Thu, 13 Mar 2025 21:54:41 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 13 Mar 2025 21:54:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Mar 2025 21:54:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 21:54:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 21:54:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Mar 2025 21:54:41 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 13 Mar 2025 21:54:41 GMT
ENV PHP_VERSION=8.2.28
# Thu, 13 Mar 2025 21:54:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.28.tar.xz.asc
# Thu, 13 Mar 2025 21:54:41 GMT
ENV PHP_SHA256=af8c9153153a7f489153b7a74f2f29a5ee36f5cb2c6c6929c98411a577e89c91
# Thu, 13 Mar 2025 21:54:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Mar 2025 21:54:41 GMT
WORKDIR /var/www/html
# Thu, 13 Mar 2025 21:54:41 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Mar 2025 21:54:41 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 13 Mar 2025 21:54:41 GMT
CMD ["php-fpm"]
# Fri, 14 Mar 2025 00:34:18 GMT
ENV IMAGICK_COMMIT_HASH=d7d3c24af1b4f599897408f1714600b69a56473b
# Fri, 14 Mar 2025 00:34:18 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Fri, 14 Mar 2025 00:34:18 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 14 Mar 2025 00:34:18 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 14 Mar 2025 00:34:18 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Fri, 14 Mar 2025 00:34:18 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         curl -fsSL -o imagick.tar.gz "https://github.com/Imagick/imagick/archive/$IMAGICK_COMMIT_HASH.tar.gz";     tar -xzf imagick.tar.gz -C /tmp;     rm imagick.tar.gz;     cd "/tmp/imagick-$IMAGICK_COMMIT_HASH";     sed -i "s/@PACKAGE_VERSION@/git-$(echo ${IMAGICK_COMMIT_HASH} | cut -c 1-7)/" php_imagick.h;     phpize;     ./configure;     make;     make install;     cd;     rm -r "/tmp/imagick-$IMAGICK_COMMIT_HASH";         pecl install APCu-5.1.24;     pecl install igbinary-3.2.16;     pecl install memcached-3.3.0         --configureoptions 'enable-memcached-igbinary="yes"';     pecl install redis-6.1.0         --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"';         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Mar 2025 00:34:18 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Fri, 14 Mar 2025 00:34:18 GMT
VOLUME [/var/www/html]
# Fri, 14 Mar 2025 00:34:18 GMT
ENV NEXTCLOUD_VERSION=30.0.7
# Fri, 14 Mar 2025 00:34:18 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-30.0.7.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-30.0.7.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Mar 2025 00:34:18 GMT
COPY *.sh upgrade.exclude / # buildkit
# Fri, 14 Mar 2025 00:34:18 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Fri, 14 Mar 2025 00:34:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 14 Mar 2025 00:34:18 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:bdeb081d427d7feac6a8c0bd36a2c34506a1aa38143fe43a5c5a8c162698a854`  
		Last Modified: Mon, 17 Mar 2025 22:17:35 GMT  
		Size: 29.2 MB (29189528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9596f9c0b8e3ce49a4cc67011b539f6ab218232dadf750023fb585fa43088862`  
		Last Modified: Mon, 17 Mar 2025 23:31:46 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f8d950544d56dbde14aa4dc0ff613dba3f9144b59aade937837b6acc959347f`  
		Last Modified: Mon, 17 Mar 2025 23:31:50 GMT  
		Size: 101.5 MB (101512572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:020384233c948226bc1ecaf06a4d4059ae2d88754fcfdb5af84ffb9c7bafbb2c`  
		Last Modified: Mon, 17 Mar 2025 23:31:46 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f65680892e1874d0f8c9ec05898e323b15a0d8aa629c2c3eeb6a7eac436065`  
		Last Modified: Mon, 17 Mar 2025 23:31:47 GMT  
		Size: 12.3 MB (12256525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00949d838acc0e4f87175d4b08a01ec1ce5790b83618cedc777337dda8fe6c0c`  
		Last Modified: Mon, 17 Mar 2025 23:31:47 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cdf7b51e84d161b9783125245c9586814038c641eb890dad7870fbc86a18b22`  
		Last Modified: Mon, 17 Mar 2025 23:31:48 GMT  
		Size: 28.1 MB (28119193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74f434b5da9e8f30d7bc1a5d13ba3f55145235a867b7f8bb840b0ebd21f803c2`  
		Last Modified: Mon, 17 Mar 2025 23:31:48 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e0312e0e2e4521b999052abf383e427cbcef1701da05050fe01e55659e55cc0`  
		Last Modified: Mon, 17 Mar 2025 23:31:48 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e25d578b3e884d758b4be7e77d56044abd7bc5765daaea296d9db5b9739eca0f`  
		Last Modified: Mon, 17 Mar 2025 23:31:49 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089a38a487093ad05873ca11cbc1c2b5bc940072dafc0440f7f1361527a55994`  
		Last Modified: Tue, 18 Mar 2025 00:25:48 GMT  
		Size: 22.4 MB (22388127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70333a115549367bd75a97fb6093ef1c6f0f8bef354e10fc353c387272d94c3f`  
		Last Modified: Tue, 18 Mar 2025 00:25:48 GMT  
		Size: 21.2 MB (21163760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:265af454634be951d848eedd2fea7f11e3364b57e95311579ae8ec9036727c6b`  
		Last Modified: Tue, 18 Mar 2025 00:25:47 GMT  
		Size: 791.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ea51e576c1c802dbe7c2efc8749dd7d27120fc0ddbd0a518aba20babf457073`  
		Last Modified: Tue, 18 Mar 2025 00:25:52 GMT  
		Size: 208.1 MB (208147850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf789075d77f513d0318ff286b928c7a4c5d2d1aff31db0b71c4dba6c9b2e2e`  
		Last Modified: Tue, 18 Mar 2025 00:25:48 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a09bb0a1da1ca3d877c7997d658605d6cc9175c2f69d7d53e79a7bd97a4d5f49`  
		Last Modified: Tue, 18 Mar 2025 00:25:49 GMT  
		Size: 2.4 KB (2356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:production-fpm` - unknown; unknown

```console
$ docker pull nextcloud@sha256:d3448ce164b0fc05afa505c1d58d376fdc2b77e5ceee5594e5cabd4f9d37372b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 KB (47928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bc894477a16990eec965ce30eb785326ecf5d6e46b2b2017d578ff72e748aed`

```dockerfile
```

-	Layers:
	-	`sha256:84c9abdc4fdd23c971b69b66acef0b808e05f5fda868628ed64da6adc0f58499`  
		Last Modified: Tue, 18 Mar 2025 00:25:47 GMT  
		Size: 47.9 KB (47928 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:production-fpm` - linux; mips64le

```console
$ docker pull nextcloud@sha256:8d2604d3d23054e6e536fdf69a1e043b461623806cf190d3da6698f28c2f59b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.9 MB (396919830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d66e5284d2582e62a1080bcac9b7e5b0595709ad92ba0c0189750b086dc9abe3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1740355200'
# Thu, 13 Mar 2025 21:54:41 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 13 Mar 2025 21:54:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Mar 2025 21:54:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 21:54:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 21:54:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Mar 2025 21:54:41 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 13 Mar 2025 21:54:41 GMT
ENV PHP_VERSION=8.2.28
# Thu, 13 Mar 2025 21:54:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.28.tar.xz.asc
# Thu, 13 Mar 2025 21:54:41 GMT
ENV PHP_SHA256=af8c9153153a7f489153b7a74f2f29a5ee36f5cb2c6c6929c98411a577e89c91
# Thu, 13 Mar 2025 21:54:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Mar 2025 21:54:41 GMT
WORKDIR /var/www/html
# Thu, 13 Mar 2025 21:54:41 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Mar 2025 21:54:41 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 13 Mar 2025 21:54:41 GMT
CMD ["php-fpm"]
# Fri, 14 Mar 2025 00:34:18 GMT
ENV IMAGICK_COMMIT_HASH=d7d3c24af1b4f599897408f1714600b69a56473b
# Fri, 14 Mar 2025 00:34:18 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Fri, 14 Mar 2025 00:34:18 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 14 Mar 2025 00:34:18 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 14 Mar 2025 00:34:18 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Fri, 14 Mar 2025 00:34:18 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         curl -fsSL -o imagick.tar.gz "https://github.com/Imagick/imagick/archive/$IMAGICK_COMMIT_HASH.tar.gz";     tar -xzf imagick.tar.gz -C /tmp;     rm imagick.tar.gz;     cd "/tmp/imagick-$IMAGICK_COMMIT_HASH";     sed -i "s/@PACKAGE_VERSION@/git-$(echo ${IMAGICK_COMMIT_HASH} | cut -c 1-7)/" php_imagick.h;     phpize;     ./configure;     make;     make install;     cd;     rm -r "/tmp/imagick-$IMAGICK_COMMIT_HASH";         pecl install APCu-5.1.24;     pecl install igbinary-3.2.16;     pecl install memcached-3.3.0         --configureoptions 'enable-memcached-igbinary="yes"';     pecl install redis-6.1.0         --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"';         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Mar 2025 00:34:18 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Fri, 14 Mar 2025 00:34:18 GMT
VOLUME [/var/www/html]
# Fri, 14 Mar 2025 00:34:18 GMT
ENV NEXTCLOUD_VERSION=30.0.7
# Fri, 14 Mar 2025 00:34:18 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-30.0.7.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-30.0.7.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Mar 2025 00:34:18 GMT
COPY *.sh upgrade.exclude / # buildkit
# Fri, 14 Mar 2025 00:34:18 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Fri, 14 Mar 2025 00:34:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 14 Mar 2025 00:34:18 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:1851efe37d59b19d5c7092778464657e31dbfae35874c19fb94fb95542e2fba7`  
		Last Modified: Tue, 25 Feb 2025 01:30:49 GMT  
		Size: 28.5 MB (28493681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80d36a7b1e0c4904256c3222f554e2f9053a6ce6cb06dac686a36004c2968943`  
		Last Modified: Tue, 25 Feb 2025 04:23:17 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878fe44e60469208a4e6a6cc56a06ba4bd6418ae0d09468c66a29bce7fc35e03`  
		Last Modified: Tue, 25 Feb 2025 04:23:25 GMT  
		Size: 80.7 MB (80668722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03653780888887368ef36859920d833d269d38c1e54ffb86bae392b6bfcfde65`  
		Last Modified: Tue, 25 Feb 2025 04:23:17 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5e465553f8e6f88a155a82c9fbb8653291976a39dd74f3861791dc4ca1bd24`  
		Last Modified: Fri, 14 Mar 2025 01:51:49 GMT  
		Size: 12.3 MB (12255331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:286a3e02c77729b40d19312ef2ff51fb7fa57da178d19f86b90871cbd9c31a39`  
		Last Modified: Fri, 14 Mar 2025 01:51:47 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b954132be3b27fe3e7d2880c1d8e4a12341887ccd2df47baa8f6b837a7592f2e`  
		Last Modified: Fri, 14 Mar 2025 01:51:50 GMT  
		Size: 26.7 MB (26692165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d62bebb4ee1daac881baf11e482cfa5e3789b2c525ea4c40922d195b5626f4`  
		Last Modified: Fri, 14 Mar 2025 01:51:47 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e26951b05da5b647ffc72c1c382ced601a53db7eb49a62a78f4d762effba48`  
		Last Modified: Fri, 14 Mar 2025 01:51:48 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efc49f8653bfa106f950b85d26cbf2ce001e1982a1c9583f23d24552377cd1f`  
		Last Modified: Fri, 14 Mar 2025 01:51:48 GMT  
		Size: 9.2 KB (9186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa0f623aec2741229d91fd6b091a2333ae601776e7156c4e24d10c1c94b5b825`  
		Last Modified: Fri, 14 Mar 2025 05:17:20 GMT  
		Size: 19.9 MB (19929490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df5616000ef87c967ae7560be1cb2b48bc2ed0c422c81f9e72cb3eddaa1b08cc`  
		Last Modified: Fri, 14 Mar 2025 05:17:22 GMT  
		Size: 20.7 MB (20712129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84470549457b0d2e051f979d0aa48b08ae0ed569dda99318dd2b1976b2f2bf1d`  
		Last Modified: Fri, 14 Mar 2025 05:17:18 GMT  
		Size: 797.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4335ae91c2ea1c596525300304b7b196322f1b236f016233f850dd59e7b352f`  
		Last Modified: Fri, 14 Mar 2025 19:39:28 GMT  
		Size: 208.1 MB (208148412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5033dcd1df47e8f2ab85e87d4567d4e2a8c5a63ccab1af32172575ae6109e2`  
		Last Modified: Fri, 14 Mar 2025 19:39:09 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e751b3fba3d6bf71f692e420daaf83ea1c0db0b2a7f1eaeb9606dc4f579ba6`  
		Last Modified: Fri, 14 Mar 2025 19:39:09 GMT  
		Size: 2.4 KB (2359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:production-fpm` - unknown; unknown

```console
$ docker pull nextcloud@sha256:1523dd25bb3bce0fe907eacc9b828264ce0d176f0850b4ca998ae4400a1a561f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 KB (48048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eea246aa5e6aec38830f55555f7ef93d05a59eb98f18a6597c3b23ffd1faa30c`

```dockerfile
```

-	Layers:
	-	`sha256:cf93e20cd796f08651661e2e3449890c5bfbad8902d7326bcdc1f6e6d0d605d6`  
		Last Modified: Fri, 14 Mar 2025 19:39:09 GMT  
		Size: 48.0 KB (48048 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:production-fpm` - linux; ppc64le

```console
$ docker pull nextcloud@sha256:1a37ee6dd8d7a0484e489ef4ff8ca20c4f20abdbad639ebd119506f7d48f73e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.1 MB (429124849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f07e804cb92cbf111df92ba024edb23481c6cdff77c3f8583534bb272779c53b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Thu, 13 Mar 2025 21:54:41 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 13 Mar 2025 21:54:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Mar 2025 21:54:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 21:54:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 21:54:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Mar 2025 21:54:41 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 13 Mar 2025 21:54:41 GMT
ENV PHP_VERSION=8.2.28
# Thu, 13 Mar 2025 21:54:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.28.tar.xz.asc
# Thu, 13 Mar 2025 21:54:41 GMT
ENV PHP_SHA256=af8c9153153a7f489153b7a74f2f29a5ee36f5cb2c6c6929c98411a577e89c91
# Thu, 13 Mar 2025 21:54:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Mar 2025 21:54:41 GMT
WORKDIR /var/www/html
# Thu, 13 Mar 2025 21:54:41 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Mar 2025 21:54:41 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 13 Mar 2025 21:54:41 GMT
CMD ["php-fpm"]
# Fri, 14 Mar 2025 00:34:18 GMT
ENV IMAGICK_COMMIT_HASH=d7d3c24af1b4f599897408f1714600b69a56473b
# Fri, 14 Mar 2025 00:34:18 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Fri, 14 Mar 2025 00:34:18 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 14 Mar 2025 00:34:18 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 14 Mar 2025 00:34:18 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Fri, 14 Mar 2025 00:34:18 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         curl -fsSL -o imagick.tar.gz "https://github.com/Imagick/imagick/archive/$IMAGICK_COMMIT_HASH.tar.gz";     tar -xzf imagick.tar.gz -C /tmp;     rm imagick.tar.gz;     cd "/tmp/imagick-$IMAGICK_COMMIT_HASH";     sed -i "s/@PACKAGE_VERSION@/git-$(echo ${IMAGICK_COMMIT_HASH} | cut -c 1-7)/" php_imagick.h;     phpize;     ./configure;     make;     make install;     cd;     rm -r "/tmp/imagick-$IMAGICK_COMMIT_HASH";         pecl install APCu-5.1.24;     pecl install igbinary-3.2.16;     pecl install memcached-3.3.0         --configureoptions 'enable-memcached-igbinary="yes"';     pecl install redis-6.1.0         --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"';         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Mar 2025 00:34:18 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Fri, 14 Mar 2025 00:34:18 GMT
VOLUME [/var/www/html]
# Fri, 14 Mar 2025 00:34:18 GMT
ENV NEXTCLOUD_VERSION=30.0.7
# Fri, 14 Mar 2025 00:34:18 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-30.0.7.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-30.0.7.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Mar 2025 00:34:18 GMT
COPY *.sh upgrade.exclude / # buildkit
# Fri, 14 Mar 2025 00:34:18 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Fri, 14 Mar 2025 00:34:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 14 Mar 2025 00:34:18 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:4713de4e13d024eec0b1cb2d083909104c2a36ed3ffba92c5cf710577a33ad45`  
		Last Modified: Tue, 25 Feb 2025 01:30:47 GMT  
		Size: 32.1 MB (32052314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35bbbae4d2dc0350f7df1634e33daf64fe78cb672182650c700a26750b33b64c`  
		Last Modified: Tue, 25 Feb 2025 02:59:24 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7f7bed916e76b3a3b176b4e6a5bcfe6e10e39a6c423be8fc3575115d7b1e06`  
		Last Modified: Tue, 25 Feb 2025 02:59:28 GMT  
		Size: 103.3 MB (103323545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d9943a0d5cef1bf22e1a6d5df4b38af8052474c28fe7d9188d33c9e0190742`  
		Last Modified: Tue, 25 Feb 2025 02:59:24 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b183a9e9a626652b70cd5c8539551c8cb640af571a1c9042e0132f037d4b647`  
		Last Modified: Fri, 14 Mar 2025 00:29:55 GMT  
		Size: 12.3 MB (12256822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e56b8480c0833bf885706daaa24ae51671535d736d1bd6502f4ec24bee98fdf`  
		Last Modified: Fri, 14 Mar 2025 00:29:54 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c88581c8d587c4893c5d0e4f3ec9f4da6276370c261bf429c722590c5a22c891`  
		Last Modified: Fri, 14 Mar 2025 00:33:48 GMT  
		Size: 28.7 MB (28651590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d060d61f8218819b5d303c6753fc9b191fdbb4217767776b6b827de24183cbe`  
		Last Modified: Fri, 14 Mar 2025 00:33:46 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af774f56e0b9582a37b1689788bc10d7be95ddf0f7e9f52f79edfba6c4224caa`  
		Last Modified: Fri, 14 Mar 2025 00:33:47 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab9017bee2d3c3c1b999a96f6729cee863c91f221ddcaec49b3087c6a6e07f43`  
		Last Modified: Fri, 14 Mar 2025 00:33:47 GMT  
		Size: 9.2 KB (9185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a873b96d4a2d86be55e60029754c433113fa3dad0273b8572c2e46d7ce6502`  
		Last Modified: Fri, 14 Mar 2025 19:56:51 GMT  
		Size: 22.8 MB (22760616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:368c6e133f9ab4ee666ed47cb865ca73aed813d3067713eeda5f5a184063d113`  
		Last Modified: Fri, 14 Mar 2025 19:56:52 GMT  
		Size: 21.9 MB (21910627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d00c469a0d2271b56ae342e9f8caa4508fbf3b8de41ef933cff15e2814e6a47`  
		Last Modified: Fri, 14 Mar 2025 19:56:50 GMT  
		Size: 799.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56a92ac02ba728beb9cae6d5686175f9971dc69f7501d9b95f451183e5f9eb9`  
		Last Modified: Fri, 14 Mar 2025 19:57:02 GMT  
		Size: 208.1 MB (208149442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f3df22d5e02fbd61b8ba2b2ac1563339997177dc98bf22003aefea879c10e8`  
		Last Modified: Fri, 14 Mar 2025 19:56:51 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2288a5c7db24a4bc95f56d2e66486c00349c756b1c8c9a01d4e25955f57e8bf0`  
		Last Modified: Fri, 14 Mar 2025 19:56:52 GMT  
		Size: 2.4 KB (2356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:production-fpm` - unknown; unknown

```console
$ docker pull nextcloud@sha256:3ad2cba8f71ed0ce13236ea19e443dd309d44e7d4a5b3c3f8fcb847392b3f0e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 KB (48027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f25c06acffd518b9f2b7abc1335dfad0a37f7c8da64e780664de459d5b8df315`

```dockerfile
```

-	Layers:
	-	`sha256:eed78c7e706984a292dc92d7a899a209874468e30a8276c0889d5633457477da`  
		Last Modified: Fri, 14 Mar 2025 19:56:50 GMT  
		Size: 48.0 KB (48027 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:production-fpm` - linux; s390x

```console
$ docker pull nextcloud@sha256:daf1fcd0e2d72bf67db36023c3ed364f6f4720d12a83393582e9bf6f73a95c09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.4 MB (394370071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5584c5338aca48455c8ff9b3474da7adc5ba7e5ae30ffff73f5a88ba34fbec8d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1740355200'
# Thu, 13 Mar 2025 21:54:41 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 13 Mar 2025 21:54:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Mar 2025 21:54:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 21:54:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 21:54:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Mar 2025 21:54:41 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 13 Mar 2025 21:54:41 GMT
ENV PHP_VERSION=8.2.28
# Thu, 13 Mar 2025 21:54:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.28.tar.xz.asc
# Thu, 13 Mar 2025 21:54:41 GMT
ENV PHP_SHA256=af8c9153153a7f489153b7a74f2f29a5ee36f5cb2c6c6929c98411a577e89c91
# Thu, 13 Mar 2025 21:54:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Mar 2025 21:54:41 GMT
WORKDIR /var/www/html
# Thu, 13 Mar 2025 21:54:41 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 13 Mar 2025 21:54:41 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Mar 2025 21:54:41 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 13 Mar 2025 21:54:41 GMT
CMD ["php-fpm"]
# Fri, 14 Mar 2025 00:34:18 GMT
ENV IMAGICK_COMMIT_HASH=d7d3c24af1b4f599897408f1714600b69a56473b
# Fri, 14 Mar 2025 00:34:18 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Fri, 14 Mar 2025 00:34:18 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 14 Mar 2025 00:34:18 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 14 Mar 2025 00:34:18 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Fri, 14 Mar 2025 00:34:18 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         curl -fsSL -o imagick.tar.gz "https://github.com/Imagick/imagick/archive/$IMAGICK_COMMIT_HASH.tar.gz";     tar -xzf imagick.tar.gz -C /tmp;     rm imagick.tar.gz;     cd "/tmp/imagick-$IMAGICK_COMMIT_HASH";     sed -i "s/@PACKAGE_VERSION@/git-$(echo ${IMAGICK_COMMIT_HASH} | cut -c 1-7)/" php_imagick.h;     phpize;     ./configure;     make;     make install;     cd;     rm -r "/tmp/imagick-$IMAGICK_COMMIT_HASH";         pecl install APCu-5.1.24;     pecl install igbinary-3.2.16;     pecl install memcached-3.3.0         --configureoptions 'enable-memcached-igbinary="yes"';     pecl install redis-6.1.0         --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"';         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Mar 2025 00:34:18 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Fri, 14 Mar 2025 00:34:18 GMT
VOLUME [/var/www/html]
# Fri, 14 Mar 2025 00:34:18 GMT
ENV NEXTCLOUD_VERSION=30.0.7
# Fri, 14 Mar 2025 00:34:18 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-30.0.7.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-30.0.7.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Mar 2025 00:34:18 GMT
COPY *.sh upgrade.exclude / # buildkit
# Fri, 14 Mar 2025 00:34:18 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Fri, 14 Mar 2025 00:34:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 14 Mar 2025 00:34:18 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:6d4d169c55c2ee02478b6705c4ba9e6795bffbbb872a22adfd95fb2484f2e85c`  
		Last Modified: Tue, 25 Feb 2025 01:30:03 GMT  
		Size: 26.9 MB (26864838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f83dfaf87e0f897b620f8faafcd35d93785d305460fb8a1f24f178152dc8ef4`  
		Last Modified: Tue, 25 Feb 2025 02:47:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382c1a79d42d9a6f73ff6106cec8445a8fb8bc6a78380c02024ff5e71c740938`  
		Last Modified: Tue, 25 Feb 2025 02:47:06 GMT  
		Size: 80.8 MB (80817122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd5ce3ea58656e03c29355d087376523130702c7a182e93a6e6c775d2e795dd`  
		Last Modified: Tue, 25 Feb 2025 02:47:05 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7c8facef6e795e92eb04a072d6f2df6f57c3ab5c565e23b8e0ab5fcc77be98`  
		Last Modified: Fri, 14 Mar 2025 03:06:59 GMT  
		Size: 12.3 MB (12255961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:087f974a938c00046d2cb16a426c6e0df04dd1a77f6d0751b8ff75caf2acbd09`  
		Last Modified: Fri, 14 Mar 2025 03:06:59 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62afeed898980b6deb1d1d90c6af218e1acb11c5e87c74735053a8da184efdc`  
		Last Modified: Fri, 14 Mar 2025 03:14:03 GMT  
		Size: 26.7 MB (26704838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d5cd9919ebb6d665e8434db1ff9493ca684329a00a3b5c673712b9ef611056`  
		Last Modified: Fri, 14 Mar 2025 03:14:03 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc96856a1618bc7940aaea33faba6fd82bc6292ae57fa20a75438f91b3ccebe`  
		Last Modified: Fri, 14 Mar 2025 03:14:03 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64be4eacc53df96cb12ea257fbca81fbe23663b7c6881afb2d9a9b3c8bc6d402`  
		Last Modified: Fri, 14 Mar 2025 03:14:03 GMT  
		Size: 9.2 KB (9185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92cfe440dd20f998ff58aa5f1211ac227d1162ef36f423d702f46eca291d3328`  
		Last Modified: Fri, 14 Mar 2025 22:23:23 GMT  
		Size: 19.4 MB (19421843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3304882e2f322fdca6248ff8e8ec759d43d9384d5b789cd1e21e3cf4eb5fd390`  
		Last Modified: Fri, 14 Mar 2025 22:23:24 GMT  
		Size: 20.1 MB (20138768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd0f3221ff473e63fd205d8d4edbb45d275620f2bcc55d75496405409889d51`  
		Last Modified: Fri, 14 Mar 2025 22:23:23 GMT  
		Size: 798.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddfc72266e74aa33025173e5f07ec262afae86daa97f414a1a3ec16366e7004b`  
		Last Modified: Fri, 14 Mar 2025 22:23:27 GMT  
		Size: 208.1 MB (208146808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9b1666143e1231818ba671390f3626ec0cec470207112c9dd99837146409a6`  
		Last Modified: Fri, 14 Mar 2025 22:23:23 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d85189a377a64a1d9caf70138a7e2c5474fcf112292501d96fc575b31c20c4`  
		Last Modified: Fri, 14 Mar 2025 22:23:24 GMT  
		Size: 2.4 KB (2357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:production-fpm` - unknown; unknown

```console
$ docker pull nextcloud@sha256:7353558a9ac46adf11da818b6c5148610cf3d6627b2972733b821ff3a73eddf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 KB (47964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:187d0a36d2db6b59f68db099cd32b13c57038199d46aa7ac0a1ebd52433ea417`

```dockerfile
```

-	Layers:
	-	`sha256:cbc9bb8a09f6b05e2210d2c9ac27b6193a97e74ecc263342628d8ab07e19b829`  
		Last Modified: Fri, 14 Mar 2025 22:23:22 GMT  
		Size: 48.0 KB (47964 bytes)  
		MIME: application/vnd.in-toto+json
