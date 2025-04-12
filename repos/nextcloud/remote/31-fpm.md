## `nextcloud:31-fpm`

```console
$ docker pull nextcloud@sha256:dcff0b12c4b301ca85074068b262cde17888170cb7f779397e9ee07adaf0aa45
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

### `nextcloud:31-fpm` - linux; amd64

```console
$ docker pull nextcloud@sha256:7d940fe84565fded7ee471554c7bacbedf04d4e7e5b46cbd6b08da9882acbefa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **462.1 MB (462102762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fddc41fd5ca6de6779d91a9ce4ce8c1e0c6f8bbd035c71d5112b7f91e962097`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 19 Mar 2025 22:47:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 19 Mar 2025 22:47:36 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_VERSION=8.3.20
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.20.tar.xz.asc
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_SHA256=f15914e071b5bddaf1475b5f2ba68107e8b8846655f9e89690fb7cd410b0db6c
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 19 Mar 2025 22:47:36 GMT
WORKDIR /var/www/html
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
STOPSIGNAL SIGQUIT
# Wed, 19 Mar 2025 22:47:36 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 19 Mar 2025 22:47:36 GMT
CMD ["php-fpm"]
# Wed, 19 Mar 2025 22:47:36 GMT
ENV IMAGICK_COMMIT_HASH=d7d3c24af1b4f599897408f1714600b69a56473b
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         curl -fsSL -o imagick.tar.gz "https://github.com/Imagick/imagick/archive/$IMAGICK_COMMIT_HASH.tar.gz";     tar -xzf imagick.tar.gz -C /tmp;     rm imagick.tar.gz;     cd "/tmp/imagick-$IMAGICK_COMMIT_HASH";     sed -i "s/@PACKAGE_VERSION@/git-$(echo ${IMAGICK_COMMIT_HASH} | cut -c 1-7)/" php_imagick.h;     phpize;     ./configure;     make;     make install;     cd;     rm -r "/tmp/imagick-$IMAGICK_COMMIT_HASH";         pecl install APCu-5.1.24;     pecl install igbinary-3.2.16;     pecl install memcached-3.3.0         --configureoptions 'enable-memcached-igbinary="yes"';     pecl install redis-6.1.0         --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"';         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
VOLUME [/var/www/html]
# Wed, 19 Mar 2025 22:47:36 GMT
ENV NEXTCLOUD_VERSION=31.0.2
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-31.0.2.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-31.0.2.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
COPY *.sh upgrade.exclude / # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 19 Mar 2025 22:47:36 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee24669c675717916b917f1dca5720218a8f50cc64b575a81fdf0a20490a70a`  
		Last Modified: Fri, 11 Apr 2025 17:02:54 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24f54e653c936212c89a3e477f9f3821f48ca3740973aa01a51e9edc7025f82`  
		Last Modified: Fri, 11 Apr 2025 17:03:34 GMT  
		Size: 104.3 MB (104329137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab31e43fa6140bbbba130fdf0df10137fcbd9d9c29dcc6cbe2e445f721bb77bc`  
		Last Modified: Fri, 11 Apr 2025 17:02:26 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4667119a4b3a2ed0648a982868757eed6b20b8c6e6ce5129019df7c3a81e48c`  
		Last Modified: Fri, 11 Apr 2025 17:03:31 GMT  
		Size: 12.7 MB (12658308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fdd49ba3a2ce9a5208e406f2cdcbc2c7fefe74b695a8ff38ab7356db7c8ded9`  
		Last Modified: Fri, 11 Apr 2025 17:02:32 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a975de79c294328516e2123daaaffdba48a05e0fd7772b920ed66170c2c063a`  
		Last Modified: Fri, 11 Apr 2025 17:03:32 GMT  
		Size: 27.8 MB (27827312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c8a807bba011bd52daedc90993e0b35b6e3efdef4fa243c11e787683122d9e`  
		Last Modified: Fri, 11 Apr 2025 17:03:32 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba26aa90ac75ceabd864e269f7ee1e20270bb7c8062eef092e4d55d3cc005d9`  
		Last Modified: Fri, 11 Apr 2025 17:03:33 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0bfd6800f7580921bac2745602d6f29a70025a8dc6d5845be8177cc05b90fea`  
		Last Modified: Fri, 11 Apr 2025 17:03:33 GMT  
		Size: 9.2 KB (9184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b31da8a2c7c4d3ad28982b3bc7ac4611452240374a84a7ed154936655307e593`  
		Last Modified: Fri, 11 Apr 2025 17:14:22 GMT  
		Size: 22.9 MB (22905196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2071f722f4fb6bfb8aea188e7738f6c6b01bb9fd658f4385a1d7e91ef54d35f4`  
		Last Modified: Fri, 11 Apr 2025 17:14:21 GMT  
		Size: 21.0 MB (20964169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43d97842c2a5608f85ced2a97b965f438345dc82790beca02e5d52b19d8b3c2`  
		Last Modified: Fri, 11 Apr 2025 17:14:21 GMT  
		Size: 799.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39c546bc1dc97744e682cabac975227c27d2c6c02c0d2f28f64726d741172921`  
		Last Modified: Fri, 11 Apr 2025 17:14:31 GMT  
		Size: 245.2 MB (245171494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba0a5fe95b6911daf48e37d88c153efd9943895af3a67dc291966cf6d3227ea5`  
		Last Modified: Fri, 11 Apr 2025 17:14:22 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b5c2e56f751e221258d11f37e615d725a782c3bb609ddf49bdc973b2baae29`  
		Last Modified: Fri, 11 Apr 2025 17:14:23 GMT  
		Size: 2.4 KB (2356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:31-fpm` - unknown; unknown

```console
$ docker pull nextcloud@sha256:01afd5db82b2cfd4015c8b69a8327c7d4e2c8ba08c0ebf90a9cdabe67b8c71ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 KB (47637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4055bae991a2e3d86e7c47209a4d8ce2542b479ef39a4e8035b15a40d4414110`

```dockerfile
```

-	Layers:
	-	`sha256:0aa5931bfb8a47a2a23b87c3e19c6be590a0fecdac3f200746a65ceec2f77699`  
		Last Modified: Fri, 11 Apr 2025 17:14:20 GMT  
		Size: 47.6 KB (47637 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:31-fpm` - linux; arm variant v5

```console
$ docker pull nextcloud@sha256:5e599d933942876d49c54e6ab03b2b75858106c6eae408eb8986e1807652cec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.5 MB (431498337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ace4fd4254515f0e31befc589a1884c448b3da127edafdac0848c6d584cfca`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 19 Mar 2025 22:47:36 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1743984000'
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 19 Mar 2025 22:47:36 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_VERSION=8.3.20
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.20.tar.xz.asc
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_SHA256=f15914e071b5bddaf1475b5f2ba68107e8b8846655f9e89690fb7cd410b0db6c
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 19 Mar 2025 22:47:36 GMT
WORKDIR /var/www/html
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
STOPSIGNAL SIGQUIT
# Wed, 19 Mar 2025 22:47:36 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 19 Mar 2025 22:47:36 GMT
CMD ["php-fpm"]
# Wed, 19 Mar 2025 22:47:36 GMT
ENV IMAGICK_COMMIT_HASH=d7d3c24af1b4f599897408f1714600b69a56473b
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         curl -fsSL -o imagick.tar.gz "https://github.com/Imagick/imagick/archive/$IMAGICK_COMMIT_HASH.tar.gz";     tar -xzf imagick.tar.gz -C /tmp;     rm imagick.tar.gz;     cd "/tmp/imagick-$IMAGICK_COMMIT_HASH";     sed -i "s/@PACKAGE_VERSION@/git-$(echo ${IMAGICK_COMMIT_HASH} | cut -c 1-7)/" php_imagick.h;     phpize;     ./configure;     make;     make install;     cd;     rm -r "/tmp/imagick-$IMAGICK_COMMIT_HASH";         pecl install APCu-5.1.24;     pecl install igbinary-3.2.16;     pecl install memcached-3.3.0         --configureoptions 'enable-memcached-igbinary="yes"';     pecl install redis-6.1.0         --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"';         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
VOLUME [/var/www/html]
# Wed, 19 Mar 2025 22:47:36 GMT
ENV NEXTCLOUD_VERSION=31.0.2
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-31.0.2.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-31.0.2.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
COPY *.sh upgrade.exclude / # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 19 Mar 2025 22:47:36 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:bee0b90cda85f033e5343bbd7872c95c9de54d2dbe2fe864e9cb4b10716bc994`  
		Last Modified: Tue, 08 Apr 2025 00:23:07 GMT  
		Size: 25.8 MB (25757818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede7f8a7a1736b2e1b1ffe73c183b355dc5ee08397a7422bb32c05c5d814665b`  
		Last Modified: Tue, 08 Apr 2025 02:08:18 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b061af77698181b6bb0dd67d0bb746c766d8bd85efe5f88c650b068d46e81b14`  
		Last Modified: Tue, 08 Apr 2025 02:08:21 GMT  
		Size: 82.0 MB (81993897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f8695a0bd1bfac037b09588f9a6fc30e41235265df32436850260ead851069`  
		Last Modified: Tue, 08 Apr 2025 02:08:18 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c9f8563028ce0cddbc1d3f096560d362a5246f891ea2b471376a4fedf7d5d23`  
		Last Modified: Fri, 11 Apr 2025 17:26:52 GMT  
		Size: 12.7 MB (12656536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f733a6817815039899cd4f03e524701044432adf20b8cfa1200ee321bbbefae8`  
		Last Modified: Fri, 11 Apr 2025 17:26:52 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc521631211c803fc095d7a9daebd29295f110e352ab1b11e14788e1cb29c0f`  
		Last Modified: Fri, 11 Apr 2025 17:37:03 GMT  
		Size: 26.3 MB (26304571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20258ef9937826cc381bc3045c1fd9f98cc7268584d651e879b1dc2262c9d0a`  
		Last Modified: Fri, 11 Apr 2025 17:37:01 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f8bcb0677772cf012e69acd77ee77b794640e8d3ca02fcafbc18631cb5656c`  
		Last Modified: Fri, 11 Apr 2025 17:37:02 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dbfaef644a7c22da266d83023154a815eddc6e29181348980496ee322cf4010`  
		Last Modified: Fri, 11 Apr 2025 17:37:02 GMT  
		Size: 9.2 KB (9187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70060fedca9c2d453c8b4f85eeae056ee67ae8e9db327fedadff6422565cb691`  
		Last Modified: Fri, 11 Apr 2025 18:56:41 GMT  
		Size: 20.0 MB (19990801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d19b799a1469883a35f094f220a967266e28874046d8ad54f534668acdbdd1`  
		Last Modified: Fri, 11 Apr 2025 18:56:41 GMT  
		Size: 19.6 MB (19605836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3161e20c17e90af12706ed5ddc7639acfc5c297067400e6c776c7e7e8810dc0`  
		Last Modified: Fri, 11 Apr 2025 18:56:40 GMT  
		Size: 795.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:780b6c0123d0234a861b7b7724fb568f26cb97a705c9eee48d69258c2fc3c238`  
		Last Modified: Fri, 11 Apr 2025 18:56:46 GMT  
		Size: 245.2 MB (245168993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19b6a918d87c21dd94a7fbb02d64b2f8b0b7d3488ebccb9795e294bb25f7ef2`  
		Last Modified: Fri, 11 Apr 2025 18:56:41 GMT  
		Size: 3.9 KB (3882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa95a8705160f8c5c0579eb81edb8bdd97404cc7c128cd8f66a7db4bd098d0f`  
		Last Modified: Fri, 11 Apr 2025 18:56:42 GMT  
		Size: 2.4 KB (2354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:31-fpm` - unknown; unknown

```console
$ docker pull nextcloud@sha256:540ad442a9ab444a735c9426b27e62150aa490dd539a68e648c9fc4c51772981
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 KB (47745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e760981d4ad64d9356df2e02dff7d4abb10f2b0301493c07e3fb28ed1868e7b`

```dockerfile
```

-	Layers:
	-	`sha256:b22b87ed5140a400f7100c6b592814dedc066a5143b599630402b96fe8a789a4`  
		Last Modified: Fri, 11 Apr 2025 18:56:40 GMT  
		Size: 47.7 KB (47745 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:31-fpm` - linux; arm variant v7

```console
$ docker pull nextcloud@sha256:1b1c307cd33e468b1b2a2231ca72316943a4f0fea48471e29fa5550610b0cb89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **420.5 MB (420479473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:486458bb48d5fbcd2b1dc1ec68a1b696e5b99ef4198367768dc5ad80924aa5d1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 19 Mar 2025 22:47:36 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 19 Mar 2025 22:47:36 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_VERSION=8.3.20
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.20.tar.xz.asc
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_SHA256=f15914e071b5bddaf1475b5f2ba68107e8b8846655f9e89690fb7cd410b0db6c
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 19 Mar 2025 22:47:36 GMT
WORKDIR /var/www/html
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
STOPSIGNAL SIGQUIT
# Wed, 19 Mar 2025 22:47:36 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 19 Mar 2025 22:47:36 GMT
CMD ["php-fpm"]
# Wed, 19 Mar 2025 22:47:36 GMT
ENV IMAGICK_COMMIT_HASH=d7d3c24af1b4f599897408f1714600b69a56473b
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         curl -fsSL -o imagick.tar.gz "https://github.com/Imagick/imagick/archive/$IMAGICK_COMMIT_HASH.tar.gz";     tar -xzf imagick.tar.gz -C /tmp;     rm imagick.tar.gz;     cd "/tmp/imagick-$IMAGICK_COMMIT_HASH";     sed -i "s/@PACKAGE_VERSION@/git-$(echo ${IMAGICK_COMMIT_HASH} | cut -c 1-7)/" php_imagick.h;     phpize;     ./configure;     make;     make install;     cd;     rm -r "/tmp/imagick-$IMAGICK_COMMIT_HASH";         pecl install APCu-5.1.24;     pecl install igbinary-3.2.16;     pecl install memcached-3.3.0         --configureoptions 'enable-memcached-igbinary="yes"';     pecl install redis-6.1.0         --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"';         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
VOLUME [/var/www/html]
# Wed, 19 Mar 2025 22:47:36 GMT
ENV NEXTCLOUD_VERSION=31.0.2
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-31.0.2.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-31.0.2.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
COPY *.sh upgrade.exclude / # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 19 Mar 2025 22:47:36 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:addc1be20d0979aa781d79a726ebf749adbc030186e63a44319274194e89cfa3`  
		Last Modified: Tue, 08 Apr 2025 00:23:15 GMT  
		Size: 23.9 MB (23937867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d4b097a6bd1e1c6005148baf6fe5c3fc8f71c3806b0533176b9e71d30fae09`  
		Last Modified: Tue, 08 Apr 2025 02:06:12 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b59a7abdeed6ca1e9edaa9c4d716d1e51f3acd76ac9b8a9593379251477a15`  
		Last Modified: Tue, 08 Apr 2025 02:06:14 GMT  
		Size: 76.2 MB (76162685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:911e77faae9141f2a82370cde20bb002409354ce3554b28663322cebbfd4d775`  
		Last Modified: Tue, 08 Apr 2025 02:06:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95b007d63693a137d0530e05acff194ffbec67d707ffca14557868ca4200791`  
		Last Modified: Fri, 11 Apr 2025 18:10:14 GMT  
		Size: 12.7 MB (12656445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c0df582645b730071b5782f9ec1dbaedcb05431cd5bbee6c9a246f1c2dc79f`  
		Last Modified: Fri, 11 Apr 2025 18:10:13 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5dbce30b48b91803678f9e60f587c59fb00aed69f4d1334fccb7c1954d195d`  
		Last Modified: Fri, 11 Apr 2025 18:17:35 GMT  
		Size: 25.4 MB (25406826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88462611138e8d046e509465fd4dcd738d2299d77106d5ae0e5cc8dc11213d11`  
		Last Modified: Fri, 11 Apr 2025 18:17:33 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ce177622e3597e6b7e63d8d92e154db4a9514921b2858e73c997b460e70884`  
		Last Modified: Fri, 11 Apr 2025 18:17:33 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b077f263de673fcae80aa5866950cba9dfec979dab7306166a04c0cd07131290`  
		Last Modified: Fri, 11 Apr 2025 18:17:34 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980664a19f173390ba0d6dc883db70ec264d965f3d7115d21c3e6cff87eee339`  
		Last Modified: Fri, 11 Apr 2025 20:14:09 GMT  
		Size: 18.2 MB (18229631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619455adc70b0c7cf9c8e5af50cb701e4b21e29a359b6d415c8709fcdcf901b4`  
		Last Modified: Fri, 11 Apr 2025 20:14:09 GMT  
		Size: 18.9 MB (18897279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c603aefb2e61dc7c234e2aec3c662be68bc6453eceae3cad0be658175c30463d`  
		Last Modified: Fri, 11 Apr 2025 20:14:08 GMT  
		Size: 794.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f995253bfdc8ca3cbddd4af1536a7402822b5b22323db156aef2ad3c49818df0`  
		Last Modified: Fri, 11 Apr 2025 20:14:14 GMT  
		Size: 245.2 MB (245168864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8fa9cf3aa11173f079e74afbdaf7835151a51f30d5056ccca0c2536b5face8`  
		Last Modified: Fri, 11 Apr 2025 20:14:09 GMT  
		Size: 3.9 KB (3881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7496490923c2d3e6e1980065fd5be902452787a7ddfea4d4f7f45eec185a6b17`  
		Last Modified: Fri, 11 Apr 2025 20:14:10 GMT  
		Size: 2.4 KB (2354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:31-fpm` - unknown; unknown

```console
$ docker pull nextcloud@sha256:8d4be29935a372ca224fd1e0c0b2b28680c8966bd40341265aab57c11761190b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 KB (47744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2347ecbbc34deaefdcd50d45884e3f7f00f7bbe1a0b11dfa3eb6398f315ff269`

```dockerfile
```

-	Layers:
	-	`sha256:a6c505bf3373ada83321aab61ab99094c17f6ebef29f6ce163452029ef97d09c`  
		Last Modified: Fri, 11 Apr 2025 20:14:08 GMT  
		Size: 47.7 KB (47744 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:31-fpm` - linux; arm64 variant v8

```console
$ docker pull nextcloud@sha256:9156f2f230cbfe3d4b2f6ddeb4bdafff13202e69703c7a27c16d692b7530e1e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **453.3 MB (453252213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06c8337edf9d2a7ec31726ba6b31a0833d4ad6cbe515847f75619d3a6c31776a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 19 Mar 2025 22:47:36 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 19 Mar 2025 22:47:36 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_VERSION=8.3.20
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.20.tar.xz.asc
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_SHA256=f15914e071b5bddaf1475b5f2ba68107e8b8846655f9e89690fb7cd410b0db6c
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 19 Mar 2025 22:47:36 GMT
WORKDIR /var/www/html
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
STOPSIGNAL SIGQUIT
# Wed, 19 Mar 2025 22:47:36 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 19 Mar 2025 22:47:36 GMT
CMD ["php-fpm"]
# Wed, 19 Mar 2025 22:47:36 GMT
ENV IMAGICK_COMMIT_HASH=d7d3c24af1b4f599897408f1714600b69a56473b
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         curl -fsSL -o imagick.tar.gz "https://github.com/Imagick/imagick/archive/$IMAGICK_COMMIT_HASH.tar.gz";     tar -xzf imagick.tar.gz -C /tmp;     rm imagick.tar.gz;     cd "/tmp/imagick-$IMAGICK_COMMIT_HASH";     sed -i "s/@PACKAGE_VERSION@/git-$(echo ${IMAGICK_COMMIT_HASH} | cut -c 1-7)/" php_imagick.h;     phpize;     ./configure;     make;     make install;     cd;     rm -r "/tmp/imagick-$IMAGICK_COMMIT_HASH";         pecl install APCu-5.1.24;     pecl install igbinary-3.2.16;     pecl install memcached-3.3.0         --configureoptions 'enable-memcached-igbinary="yes"';     pecl install redis-6.1.0         --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"';         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
VOLUME [/var/www/html]
# Wed, 19 Mar 2025 22:47:36 GMT
ENV NEXTCLOUD_VERSION=31.0.2
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-31.0.2.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-31.0.2.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
COPY *.sh upgrade.exclude / # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 19 Mar 2025 22:47:36 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705c5f6dffca44b4205f0e945a57290bb8e3e1ae585f26eccc2c9828d7f9ccda`  
		Last Modified: Tue, 08 Apr 2025 02:20:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc8e5730fe526cc83387586aee6b7883edb46c1cbf4028dd372d5e9cc4aa7ec`  
		Last Modified: Tue, 08 Apr 2025 02:20:36 GMT  
		Size: 98.1 MB (98130393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d28e77e2da9013ba78046a81e9835f08797c66738b7838294afd4c12822ca8c`  
		Last Modified: Tue, 08 Apr 2025 02:20:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec1e173b3d4f7a6ecb666e5808530783144c61d44ff83b32c0b9c9a20678f392`  
		Last Modified: Fri, 11 Apr 2025 17:49:21 GMT  
		Size: 12.7 MB (12658206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19826dbe8767f2bbe44fdf3395133de0ce1092769d5bf24953f1b5037b6d0403`  
		Last Modified: Fri, 11 Apr 2025 17:49:20 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc05c4eec7dd263d6a85fcc12639896b5a0f2c8a5bca0a5b7458fa857beea224`  
		Last Modified: Fri, 11 Apr 2025 17:57:23 GMT  
		Size: 27.8 MB (27774292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4792428ab744b600142aca44e5d53aff9674a0fe632191f05880e6d5856778dd`  
		Last Modified: Fri, 11 Apr 2025 17:57:22 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6302b4d700562a8ff9210e6eb9be1229614b7d37a6c83a9afa3f88947339684b`  
		Last Modified: Fri, 11 Apr 2025 17:57:22 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56eb4d4954360998d6010785e062855d8dafe2903767dc9d50cf278ea189d4f0`  
		Last Modified: Fri, 11 Apr 2025 17:57:22 GMT  
		Size: 9.2 KB (9185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c275b7b4c10c56a4939b27c2c89f0c5fb164aab4448e829930eb2175eb3b30d7`  
		Last Modified: Fri, 11 Apr 2025 19:55:58 GMT  
		Size: 20.3 MB (20259274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd5c36e2bc89fa8d2190c94924c6c91b6f4a96fe0565e633acb5ab2c7d90a8b`  
		Last Modified: Fri, 11 Apr 2025 19:55:59 GMT  
		Size: 21.2 MB (21172608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc41c7982ac03f1a0296857ed07f9099443d9c56a95c36e1d9891e407c6b460`  
		Last Modified: Fri, 11 Apr 2025 19:55:58 GMT  
		Size: 794.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e241ed522557ea0b536d8a06593fa2ad61dae4b404c2395e5e5810e1418cbc9`  
		Last Modified: Fri, 11 Apr 2025 19:56:04 GMT  
		Size: 245.2 MB (245171240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab651804db4957d61645b6a7c84917d39adbd88de1400c49070f9a5e04fc0dd`  
		Last Modified: Fri, 11 Apr 2025 19:55:58 GMT  
		Size: 3.9 KB (3882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84569e177255a0c8d3b2e89fe736796a1784f549280024aeb818d178583619e0`  
		Last Modified: Fri, 11 Apr 2025 19:56:00 GMT  
		Size: 2.4 KB (2356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:31-fpm` - unknown; unknown

```console
$ docker pull nextcloud@sha256:01038a77f09f0b566525accd0058a387aca8d47a68f497b9adcd7cbcc7c2be55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 KB (47779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3af8ada92bf91580712c94229e6d8b1bc3b918f7ba96c928d93a1e36acd0fa06`

```dockerfile
```

-	Layers:
	-	`sha256:1df3af9227fb049ff8b818de0eb01344d01a15f3ba26d829cc3db958bab333cd`  
		Last Modified: Fri, 11 Apr 2025 19:55:57 GMT  
		Size: 47.8 KB (47779 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:31-fpm` - linux; 386

```console
$ docker pull nextcloud@sha256:e5520f9fbb01c19925829bc73d85bb26c3801fbc162096be65eef8d0ea6542d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **460.5 MB (460469358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbb38dee87c0075663e7e1ff77934eed27a6a970dd2b694bb585aace7ac48112`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 19 Mar 2025 22:47:36 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1743984000'
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 19 Mar 2025 22:47:36 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_VERSION=8.3.20
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.20.tar.xz.asc
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_SHA256=f15914e071b5bddaf1475b5f2ba68107e8b8846655f9e89690fb7cd410b0db6c
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 19 Mar 2025 22:47:36 GMT
WORKDIR /var/www/html
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
STOPSIGNAL SIGQUIT
# Wed, 19 Mar 2025 22:47:36 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 19 Mar 2025 22:47:36 GMT
CMD ["php-fpm"]
# Wed, 19 Mar 2025 22:47:36 GMT
ENV IMAGICK_COMMIT_HASH=d7d3c24af1b4f599897408f1714600b69a56473b
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         curl -fsSL -o imagick.tar.gz "https://github.com/Imagick/imagick/archive/$IMAGICK_COMMIT_HASH.tar.gz";     tar -xzf imagick.tar.gz -C /tmp;     rm imagick.tar.gz;     cd "/tmp/imagick-$IMAGICK_COMMIT_HASH";     sed -i "s/@PACKAGE_VERSION@/git-$(echo ${IMAGICK_COMMIT_HASH} | cut -c 1-7)/" php_imagick.h;     phpize;     ./configure;     make;     make install;     cd;     rm -r "/tmp/imagick-$IMAGICK_COMMIT_HASH";         pecl install APCu-5.1.24;     pecl install igbinary-3.2.16;     pecl install memcached-3.3.0         --configureoptions 'enable-memcached-igbinary="yes"';     pecl install redis-6.1.0         --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"';         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
VOLUME [/var/www/html]
# Wed, 19 Mar 2025 22:47:36 GMT
ENV NEXTCLOUD_VERSION=31.0.2
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-31.0.2.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-31.0.2.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
COPY *.sh upgrade.exclude / # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 19 Mar 2025 22:47:36 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:e4fab02059329179b6416bda7cdc389d26699f1c93a02194f146c047031c4748`  
		Last Modified: Tue, 08 Apr 2025 00:23:49 GMT  
		Size: 29.2 MB (29210731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69de6a895de582a1e3fa49e432b7dc3dd9af5bd74502cd33381c1629a23907b6`  
		Last Modified: Fri, 11 Apr 2025 17:02:26 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4bd26e45f91e207e116b61929981a01ff41d924b3ec500997d8e1540ba64081`  
		Last Modified: Fri, 11 Apr 2025 17:03:48 GMT  
		Size: 101.5 MB (101512145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab31e43fa6140bbbba130fdf0df10137fcbd9d9c29dcc6cbe2e445f721bb77bc`  
		Last Modified: Fri, 11 Apr 2025 17:02:26 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ecc371b892adea7e6d6def011e8ef83ba32e43730634d6497b9ed90a27b684`  
		Last Modified: Fri, 11 Apr 2025 17:03:46 GMT  
		Size: 12.7 MB (12657506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12239138f233e83d4dd2a7498a67a60a8b156f27f9acb9f5867a8b563c9ac655`  
		Last Modified: Fri, 11 Apr 2025 17:03:45 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:613ac9078115a8dfd2e109131bab1371102a86cd350763c762f26699b2a55f67`  
		Last Modified: Fri, 11 Apr 2025 17:03:46 GMT  
		Size: 28.3 MB (28336943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94cad11ce6a8bb688ab9285fcf47689311cb81f52e8524c3086bcc70d0df5474`  
		Last Modified: Fri, 11 Apr 2025 17:03:46 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:213531093f2238dfed124e0dba3d6d00cd4915ae985c26ec29655624f4a5eb3f`  
		Last Modified: Fri, 11 Apr 2025 17:03:47 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be88455df9000b6cb7f1db690462bbc8239daa551487718ad2367f3a186e0f7a`  
		Last Modified: Fri, 11 Apr 2025 17:03:47 GMT  
		Size: 9.2 KB (9185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16cf20fa9a57f7802837fed57baae3d66dbdf8374b4db2b7683ad3877b84368e`  
		Last Modified: Fri, 11 Apr 2025 17:15:02 GMT  
		Size: 22.4 MB (22388191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bcb25c95e26e9550faea0da546a77389f557379eceb5b2ae55242887ce837f9`  
		Last Modified: Fri, 11 Apr 2025 17:15:01 GMT  
		Size: 21.2 MB (21173750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c6d62c48e088329d96766bce3786ba9bbeaf5817ca0e7e024ca3af63a6db318`  
		Last Modified: Fri, 11 Apr 2025 17:15:00 GMT  
		Size: 798.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a524d32358708b1cc5d3972340fa6b5de12b690dc477a39e4b19b3ed149abed7`  
		Last Modified: Fri, 11 Apr 2025 17:15:06 GMT  
		Size: 245.2 MB (245170204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cdddf6787f5bb51cd228df1c6f2c8641bbc81cb7819615e8a16adb3c834e1d5`  
		Last Modified: Fri, 11 Apr 2025 17:15:01 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc697ef130815a7218b9a5030cd2d9d312c2d64121052a14dc78a0abcddbee7b`  
		Last Modified: Fri, 11 Apr 2025 17:15:02 GMT  
		Size: 2.4 KB (2357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:31-fpm` - unknown; unknown

```console
$ docker pull nextcloud@sha256:b2c76e179ad3e795cb9330dd28a4c0747236ee80a4aa875a51ac4dce4b6c1b9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 KB (47598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6462e9b590d9610f3ef4438f8e12b14a71f3c2852f7b3fba106335e75c2636b`

```dockerfile
```

-	Layers:
	-	`sha256:9eaa3f5bb5f3a8af6ef39b20479ed63b754c60492562d205df997ce72421e5eb`  
		Last Modified: Fri, 11 Apr 2025 17:15:00 GMT  
		Size: 47.6 KB (47598 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:31-fpm` - linux; mips64le

```console
$ docker pull nextcloud@sha256:3d441612cdd7f0ff14814ad0a0d6d2b2b77d8d08a1f60903d3103c1e787f2c3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.6 MB (434597142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca7b1a38fdc5bf08f2edf7a3f5822d61bd398abdd5864484d627531ee56730ef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 19 Mar 2025 22:47:36 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1743984000'
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 19 Mar 2025 22:47:36 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_VERSION=8.3.20
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.20.tar.xz.asc
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_SHA256=f15914e071b5bddaf1475b5f2ba68107e8b8846655f9e89690fb7cd410b0db6c
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 19 Mar 2025 22:47:36 GMT
WORKDIR /var/www/html
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
STOPSIGNAL SIGQUIT
# Wed, 19 Mar 2025 22:47:36 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 19 Mar 2025 22:47:36 GMT
CMD ["php-fpm"]
# Wed, 19 Mar 2025 22:47:36 GMT
ENV IMAGICK_COMMIT_HASH=d7d3c24af1b4f599897408f1714600b69a56473b
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         curl -fsSL -o imagick.tar.gz "https://github.com/Imagick/imagick/archive/$IMAGICK_COMMIT_HASH.tar.gz";     tar -xzf imagick.tar.gz -C /tmp;     rm imagick.tar.gz;     cd "/tmp/imagick-$IMAGICK_COMMIT_HASH";     sed -i "s/@PACKAGE_VERSION@/git-$(echo ${IMAGICK_COMMIT_HASH} | cut -c 1-7)/" php_imagick.h;     phpize;     ./configure;     make;     make install;     cd;     rm -r "/tmp/imagick-$IMAGICK_COMMIT_HASH";         pecl install APCu-5.1.24;     pecl install igbinary-3.2.16;     pecl install memcached-3.3.0         --configureoptions 'enable-memcached-igbinary="yes"';     pecl install redis-6.1.0         --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"';         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
VOLUME [/var/www/html]
# Wed, 19 Mar 2025 22:47:36 GMT
ENV NEXTCLOUD_VERSION=31.0.2
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-31.0.2.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-31.0.2.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
COPY *.sh upgrade.exclude / # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 19 Mar 2025 22:47:36 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c5170849255c666bce01dd02c1afbe442b1ecb682c342680d91dcd7cd477b57d`  
		Last Modified: Tue, 08 Apr 2025 00:23:28 GMT  
		Size: 28.5 MB (28513953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba0a04c9b2bb07ebbbf1ff9838da10bb162c6ac637a662105936e8b0cfe6c4`  
		Last Modified: Tue, 08 Apr 2025 03:33:44 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb1f9e949a7943e3a44c47922361d3e69b1969a2cea4dec89ae36496be4b8b2`  
		Last Modified: Tue, 08 Apr 2025 03:33:53 GMT  
		Size: 80.7 MB (80670501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ea48728e7911587bf93013dabc6b5148fd156c8e821390a2fcc1d7e3112bc8`  
		Last Modified: Tue, 08 Apr 2025 03:33:44 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe3dbefe2dd5efcf65ebe04b1c17607412583f409608eaf8bde2880bece13ac`  
		Last Modified: Fri, 11 Apr 2025 18:27:43 GMT  
		Size: 12.7 MB (12656125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a428ccaba8e786ea69bb505ec32af151038f67f2bc661c6de814ec2c0516c885`  
		Last Modified: Fri, 11 Apr 2025 18:27:41 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08e98d8115c07759b321b8738fde7c886f24676c65c9782b9ec2bba3c047248`  
		Last Modified: Fri, 11 Apr 2025 19:02:13 GMT  
		Size: 26.9 MB (26916022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7faa419b698b304e9d1141965a3d7c5c66a5cd25c744569682dc601a7142732`  
		Last Modified: Fri, 11 Apr 2025 19:02:10 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1314d584f41bdc6f816ba12a99dfd3f571188300595f5e2e9b83b64d2479b20`  
		Last Modified: Fri, 11 Apr 2025 19:02:10 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f9a6afeefd0d2fda677f0b0f84ab1419977706e14cb01e45fe9e61d15e08d8`  
		Last Modified: Fri, 11 Apr 2025 19:02:10 GMT  
		Size: 9.2 KB (9184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3142e55c3b63011880a170dea0aadec22a7171f0afa186f4bef356319e232d17`  
		Last Modified: Fri, 11 Apr 2025 22:56:44 GMT  
		Size: 19.9 MB (19929552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:132e1b2dcae7418b4c0ee4834ec0383adb8fcc9d3f5822f0b398cd0ac473ebd9`  
		Last Modified: Fri, 11 Apr 2025 22:56:44 GMT  
		Size: 20.7 MB (20720326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14bfdb17c59ca64b74aa8bc7b09c88c3d815e53192e7641a9179b630f9d30846`  
		Last Modified: Fri, 11 Apr 2025 22:56:42 GMT  
		Size: 800.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf4aecaff3c602de26ed590d0a19fa5fa3b03ac60164eea950fcdd757c02b12`  
		Last Modified: Fri, 11 Apr 2025 22:57:04 GMT  
		Size: 245.2 MB (245170770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d4132a67c6b5703a56092a36f0242114f3a865357b16a44acd9fdea1792eda`  
		Last Modified: Fri, 11 Apr 2025 22:56:43 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c0bb284c7026b30466842b1496cd598273587f525cf10f9c40010c7fbdf7741`  
		Last Modified: Fri, 11 Apr 2025 22:56:44 GMT  
		Size: 2.4 KB (2358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:31-fpm` - unknown; unknown

```console
$ docker pull nextcloud@sha256:dbff495f5e9f28c6b6cce0735675cfd1dd68f0b40a0f217237a2b046070f42fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 KB (47705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e5d0b10d37e273bc2d05c2cddac76e8e10b3f959efcf520de29832934ea57b`

```dockerfile
```

-	Layers:
	-	`sha256:51ba275268e521d76ff3f9d6d12f4ac0699fe0f94a7b315c249d074b721f8575`  
		Last Modified: Fri, 11 Apr 2025 22:56:41 GMT  
		Size: 47.7 KB (47705 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:31-fpm` - linux; ppc64le

```console
$ docker pull nextcloud@sha256:f81363a6478ff27ba2be76dfba23231df8393853254c6955245346ff620ed334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **466.8 MB (466815840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecd936d9604d52e4cb726fa9acb9d478af1ac2d2187455d35c1506c0c4144e02`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 19 Mar 2025 22:47:36 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1743984000'
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 19 Mar 2025 22:47:36 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_VERSION=8.3.20
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.20.tar.xz.asc
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_SHA256=f15914e071b5bddaf1475b5f2ba68107e8b8846655f9e89690fb7cd410b0db6c
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 19 Mar 2025 22:47:36 GMT
WORKDIR /var/www/html
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
STOPSIGNAL SIGQUIT
# Wed, 19 Mar 2025 22:47:36 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 19 Mar 2025 22:47:36 GMT
CMD ["php-fpm"]
# Wed, 19 Mar 2025 22:47:36 GMT
ENV IMAGICK_COMMIT_HASH=d7d3c24af1b4f599897408f1714600b69a56473b
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         curl -fsSL -o imagick.tar.gz "https://github.com/Imagick/imagick/archive/$IMAGICK_COMMIT_HASH.tar.gz";     tar -xzf imagick.tar.gz -C /tmp;     rm imagick.tar.gz;     cd "/tmp/imagick-$IMAGICK_COMMIT_HASH";     sed -i "s/@PACKAGE_VERSION@/git-$(echo ${IMAGICK_COMMIT_HASH} | cut -c 1-7)/" php_imagick.h;     phpize;     ./configure;     make;     make install;     cd;     rm -r "/tmp/imagick-$IMAGICK_COMMIT_HASH";         pecl install APCu-5.1.24;     pecl install igbinary-3.2.16;     pecl install memcached-3.3.0         --configureoptions 'enable-memcached-igbinary="yes"';     pecl install redis-6.1.0         --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"';         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
VOLUME [/var/www/html]
# Wed, 19 Mar 2025 22:47:36 GMT
ENV NEXTCLOUD_VERSION=31.0.2
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-31.0.2.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-31.0.2.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
COPY *.sh upgrade.exclude / # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 19 Mar 2025 22:47:36 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:eda04574e09a8e08ba343dd01ac61bceb64282d2e992a997bd2102897b52d004`  
		Last Modified: Tue, 08 Apr 2025 00:23:44 GMT  
		Size: 32.1 MB (32068231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b9a46967066ae4671f168da66f36a8b5a2975183ce39c8dd4a2b10bf95a917f`  
		Last Modified: Tue, 08 Apr 2025 02:10:40 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c687d4e4921b0609438b51c7d318fa414c7011636641c6b89f5fd3f8f3fc315`  
		Last Modified: Tue, 08 Apr 2025 02:10:43 GMT  
		Size: 103.3 MB (103324796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e3514f5d628c2a9213004449181d4a82ac680ebdb792bc18d335a66bc84e0a`  
		Last Modified: Tue, 08 Apr 2025 02:10:40 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e2f82f2b3cddeb4da1d543503584c09427c3e2176c3708274e437650d38cc6`  
		Last Modified: Fri, 11 Apr 2025 17:41:40 GMT  
		Size: 12.7 MB (12657884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bebe801446acde2d93e3af90ed24a1235b53e76229808578fbdd841f096fbe1`  
		Last Modified: Fri, 11 Apr 2025 17:41:39 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2b5a7ca32b6cff843d0d8d193a6103da1eff3ff45f86da90827c8e2191de2f`  
		Last Modified: Fri, 11 Apr 2025 17:49:36 GMT  
		Size: 28.9 MB (28894056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bfdadee978375601e1fcd3ef495ba0da81483f69b8565258c7ca1833431ccac`  
		Last Modified: Fri, 11 Apr 2025 17:49:35 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99b845e27e47947d446f6638fcc41ae199aa33e09cd7dd1931e32f73b40d592`  
		Last Modified: Fri, 11 Apr 2025 17:49:35 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32486ebf676052ba863ee0e3b74ed97b208623599c5c6e7874926b7082a3dbe`  
		Last Modified: Fri, 11 Apr 2025 17:49:35 GMT  
		Size: 9.2 KB (9185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce95d35816c4f02623de43d3762e04bed521a560da1bd866d974250576a2f6f`  
		Last Modified: Fri, 11 Apr 2025 20:33:45 GMT  
		Size: 22.8 MB (22760834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eecc1c173e05c2df560cc4bc8a1b3f0f1f48d7dcae0870c6ee10dd47ccfc42d`  
		Last Modified: Fri, 11 Apr 2025 20:33:43 GMT  
		Size: 21.9 MB (21917851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b995c627bce8904a57ada62b4b99d784a50a4069ff18dda10d106f316409fc`  
		Last Modified: Fri, 11 Apr 2025 20:33:41 GMT  
		Size: 796.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1348a11f9e0adeffb8f7b0c09cfb47b646706dc27f972c2797604835a707bf1f`  
		Last Modified: Fri, 11 Apr 2025 20:34:04 GMT  
		Size: 245.2 MB (245172301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d88c88f1d7cd8d999b498dff5ef376890ba7c7df57f1a52a2e64f996a0d6209`  
		Last Modified: Fri, 11 Apr 2025 20:33:42 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fda36925630e7fcfccc68e7f10503359b426771b8222ff3b7a046c3bd750433`  
		Last Modified: Fri, 11 Apr 2025 20:33:43 GMT  
		Size: 2.4 KB (2358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:31-fpm` - unknown; unknown

```console
$ docker pull nextcloud@sha256:801834e92231f8fcee68397fc5a2af94c1f857b8929f4c7c23abf382402c0276
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 KB (47686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a6211752c098cbbf577179ba2ab47b6b15d4c8f8214906da65bf1f2b4f9502b`

```dockerfile
```

-	Layers:
	-	`sha256:6c1de22bedbc1cb519a16a97162079ccd67fb186927e352cbf40189891b3f312`  
		Last Modified: Fri, 11 Apr 2025 20:33:41 GMT  
		Size: 47.7 KB (47686 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:31-fpm` - linux; s390x

```console
$ docker pull nextcloud@sha256:cbf5042e06cd64fca8df132d69080ed8826c80d454dbfbb30f7b7dbdff603bdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **432.0 MB (432041633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0a35e1b1e81ff309ccf40037ceaf0504758701f6c1f86e5f9a72b3893f920b0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 19 Mar 2025 22:47:36 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1743984000'
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 19 Mar 2025 22:47:36 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_VERSION=8.3.20
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.20.tar.xz.asc
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_SHA256=f15914e071b5bddaf1475b5f2ba68107e8b8846655f9e89690fb7cd410b0db6c
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 19 Mar 2025 22:47:36 GMT
WORKDIR /var/www/html
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
STOPSIGNAL SIGQUIT
# Wed, 19 Mar 2025 22:47:36 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 19 Mar 2025 22:47:36 GMT
CMD ["php-fpm"]
# Wed, 19 Mar 2025 22:47:36 GMT
ENV IMAGICK_COMMIT_HASH=d7d3c24af1b4f599897408f1714600b69a56473b
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 19 Mar 2025 22:47:36 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         curl -fsSL -o imagick.tar.gz "https://github.com/Imagick/imagick/archive/$IMAGICK_COMMIT_HASH.tar.gz";     tar -xzf imagick.tar.gz -C /tmp;     rm imagick.tar.gz;     cd "/tmp/imagick-$IMAGICK_COMMIT_HASH";     sed -i "s/@PACKAGE_VERSION@/git-$(echo ${IMAGICK_COMMIT_HASH} | cut -c 1-7)/" php_imagick.h;     phpize;     ./configure;     make;     make install;     cd;     rm -r "/tmp/imagick-$IMAGICK_COMMIT_HASH";         pecl install APCu-5.1.24;     pecl install igbinary-3.2.16;     pecl install memcached-3.3.0         --configureoptions 'enable-memcached-igbinary="yes"';     pecl install redis-6.1.0         --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"';         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
VOLUME [/var/www/html]
# Wed, 19 Mar 2025 22:47:36 GMT
ENV NEXTCLOUD_VERSION=31.0.2
# Wed, 19 Mar 2025 22:47:36 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-31.0.2.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-31.0.2.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
COPY *.sh upgrade.exclude / # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Wed, 19 Mar 2025 22:47:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 19 Mar 2025 22:47:36 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:4d39bd57bcf7f4854587de5b4defd11e1b3b354bad1320b74c6994d07d7b3671`  
		Last Modified: Tue, 08 Apr 2025 00:24:14 GMT  
		Size: 26.9 MB (26884606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0629663656342054d2f9f2b005107659a6c173bb5f0b7cb64dc8cb1ee42b441c`  
		Last Modified: Tue, 08 Apr 2025 02:00:47 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687a798e29fb2285c77a2ed089ffb98dd2ae622d769dfc8b8796f747270caa16`  
		Last Modified: Tue, 08 Apr 2025 02:00:49 GMT  
		Size: 80.8 MB (80816477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8881dcc114cdc5cc5dfd6ca5beca1e2ac5ae137a5266f40776b68c106d43cac9`  
		Last Modified: Tue, 08 Apr 2025 02:00:47 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8045de39131261a4a21feb89466d3badd6d5742ce2880473a038de5e5d211331`  
		Last Modified: Fri, 11 Apr 2025 17:55:35 GMT  
		Size: 12.7 MB (12656930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbef11a9cdc6533038d6afac7e72d2bc1388b5d89db605c2c92eeab0260d4603`  
		Last Modified: Fri, 11 Apr 2025 17:55:34 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1c5372a59b357230967efafde8ced190573bc9c14047d6a77887afcb4681b7`  
		Last Modified: Fri, 11 Apr 2025 17:55:35 GMT  
		Size: 26.9 MB (26927677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef92d3969309500f493389b0ebd756b408c7bc58ba284ee065a632dc026c06ac`  
		Last Modified: Fri, 11 Apr 2025 17:55:34 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5772da205816d549ad261972bc294367f6736785699b2b9a5d2f7596718c8b67`  
		Last Modified: Fri, 11 Apr 2025 17:55:35 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4bf41038f890601cf89f474e8446a39c7c4eeec3cbb8a55427c26722d9dc4f`  
		Last Modified: Fri, 11 Apr 2025 17:55:35 GMT  
		Size: 9.2 KB (9183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acef3ed8b4142faf8ccb73f81a6889225541b58dddb40a6a46c639f77735387e`  
		Last Modified: Fri, 11 Apr 2025 20:10:39 GMT  
		Size: 19.4 MB (19421901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aec7232580a1465ce8594e4182cf62b77ca0ff031d8afae2b4e0448db5ed618`  
		Last Modified: Fri, 11 Apr 2025 20:10:39 GMT  
		Size: 20.1 MB (20145472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cea9659c83aaaad58a373b38bef49612d1e4bf0a8539a695cba479f85e175cf0`  
		Last Modified: Fri, 11 Apr 2025 20:10:38 GMT  
		Size: 793.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e62754b7a6653e4496bf27625c1fe07d3f7bb65e776731edf3c1b4e52c461d7`  
		Last Modified: Fri, 11 Apr 2025 20:10:44 GMT  
		Size: 245.2 MB (245168697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a69d53d1584e89d92ca07988455bc34816fe543eabc2e645713b8127820eae`  
		Last Modified: Fri, 11 Apr 2025 20:10:39 GMT  
		Size: 3.9 KB (3880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa3be83ab59ca59c0f5b62caf883776bc31bec759383280b946c202abc27f726`  
		Last Modified: Fri, 11 Apr 2025 20:10:40 GMT  
		Size: 2.4 KB (2353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:31-fpm` - unknown; unknown

```console
$ docker pull nextcloud@sha256:7fe92c9fc7d25cf801c6a547d00217da93d0e81ed1b98feaa2483deeb86917c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 KB (47630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9cb61aaba1ea90c28d5a9a7ce85e41bb8c772a9c1efd474b5693d1cb95cb6dd`

```dockerfile
```

-	Layers:
	-	`sha256:ba5bb3bc9b188f1efbdad44d241c719dc5811d1359f7030e9b52b7f826102e83`  
		Last Modified: Fri, 11 Apr 2025 20:10:38 GMT  
		Size: 47.6 KB (47630 bytes)  
		MIME: application/vnd.in-toto+json
