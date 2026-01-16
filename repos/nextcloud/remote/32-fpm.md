## `nextcloud:32-fpm`

```console
$ docker pull nextcloud@sha256:3a3abf0eafeeb18920e69ebd74ae0c8079d93d3188791c554fb701b773df004c
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

### `nextcloud:32-fpm` - linux; amd64

```console
$ docker pull nextcloud@sha256:49c381bb1685ced4aa7fe255bada34ffb73343aaf3e89f17c3ffdb22d5dac922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **526.1 MB (526126823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a0bd8fb16e956e562faeb833670d7378da1634d0480f8d84a25ee0889eb24ca`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:28:36 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 13 Jan 2026 01:28:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 13 Jan 2026 01:28:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 01:28:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 13 Jan 2026 01:28:52 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 13 Jan 2026 01:28:52 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jan 2026 01:28:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jan 2026 01:28:52 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 13 Jan 2026 01:28:52 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 13 Jan 2026 01:28:52 GMT
ENV PHP_VERSION=8.3.29
# Tue, 13 Jan 2026 01:28:52 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Tue, 13 Jan 2026 01:28:52 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Tue, 13 Jan 2026 01:40:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 13 Jan 2026 01:40:04 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:42:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 13 Jan 2026 01:42:21 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:42:22 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 13 Jan 2026 01:42:22 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 13 Jan 2026 01:42:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 13 Jan 2026 01:42:22 GMT
WORKDIR /var/www/html
# Tue, 13 Jan 2026 01:42:22 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 13 Jan 2026 01:42:22 GMT
STOPSIGNAL SIGQUIT
# Tue, 13 Jan 2026 01:42:22 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 13 Jan 2026 01:42:22 GMT
CMD ["php-fpm"]
# Fri, 16 Jan 2026 00:43:55 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-7.q16-10-extra         rsync     ;     apt-get dist-clean;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Fri, 16 Jan 2026 00:46:05 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 16 Jan 2026 00:46:05 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 16 Jan 2026 00:46:05 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Fri, 16 Jan 2026 00:46:05 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         liblz4-dev         libmagickwand-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.28;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.1;     pecl install --configureoptions 'enable-memcached-igbinary="yes"'         memcached-3.4.0;     pecl install --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"'         redis-6.3.0;         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -rt dpkg-query --search         | awk 'sub(":$", "", $1) { print $1 }'         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     apt-get dist-clean # buildkit
# Fri, 16 Jan 2026 00:46:05 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Fri, 16 Jan 2026 00:46:05 GMT
VOLUME [/var/www/html]
# Fri, 16 Jan 2026 00:46:05 GMT
ENV NEXTCLOUD_VERSION=32.0.4
# Fri, 16 Jan 2026 00:46:42 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://github.com/nextcloud-releases/server/releases/download/v32.0.4/nextcloud-32.0.4.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://github.com/nextcloud-releases/server/releases/download/v32.0.4/nextcloud-32.0.4.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     apt-get dist-clean # buildkit
# Fri, 16 Jan 2026 00:46:42 GMT
COPY *.sh upgrade.exclude / # buildkit
# Fri, 16 Jan 2026 00:46:42 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Fri, 16 Jan 2026 00:46:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Jan 2026 00:46:42 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:34 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:017a971add4f0db7df84e90bc5fe3a65f01671c9900203c68ebee633d64e61b2`  
		Last Modified: Tue, 13 Jan 2026 01:32:01 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1976b087334a4c6755a6b795b29983f219e2c354531e0337a682c1b36063fc`  
		Last Modified: Tue, 13 Jan 2026 01:32:23 GMT  
		Size: 117.8 MB (117839377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5afa1535a374897eadbdd5bb3a5df5ffb1327bbee841892920cc3bda343f0809`  
		Last Modified: Tue, 13 Jan 2026 01:31:59 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a84c9b8b62fe364325416a4c75ba904323246caafc8882ef2a27af055bdd6ea6`  
		Last Modified: Tue, 13 Jan 2026 01:42:45 GMT  
		Size: 12.8 MB (12750052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aecb7d78d92d6e2a8ace206cfd897cd2e0f7e2050cee95c0cb8011a81a2ca7a9`  
		Last Modified: Tue, 13 Jan 2026 01:42:43 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c472ec7030fad44789be16ae5a172a34d649c6a6938e1c15af376ce54cd17be6`  
		Last Modified: Tue, 13 Jan 2026 01:42:44 GMT  
		Size: 11.9 MB (11898235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4dd15f9ca9f4a5135be6cdf98e1ee4a25d8ed91c1def38bb7e5a4a43a46869d`  
		Last Modified: Tue, 13 Jan 2026 01:42:44 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05c0e1e2914add847f958b4995cec47830428e740d0b97146970fd185f546d7`  
		Last Modified: Tue, 13 Jan 2026 01:42:44 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e4cea4c41e507ef3dc30def1b357a72f90f1882c1910ba6a8d331671738800`  
		Last Modified: Tue, 13 Jan 2026 01:42:44 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6922df709ec8acd58a61cc0a579e98add91fbb54f40d7d6c6999f20a27f496bd`  
		Last Modified: Tue, 13 Jan 2026 01:42:44 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60b3d73777b0fa9313911c59c3483da00fe3fb7a41935c5301cef6d08720eec`  
		Last Modified: Fri, 16 Jan 2026 00:47:21 GMT  
		Size: 21.1 MB (21084399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:598f79630fcf41091f7f62576fe337656377fdb3049e7ab4e86b108d1711ae03`  
		Last Modified: Fri, 16 Jan 2026 00:47:24 GMT  
		Size: 37.0 MB (37000086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d161f0077700c6e50c3d9b81004818587e2cacc8eb95aed4c482c6593d69697`  
		Last Modified: Fri, 16 Jan 2026 00:47:20 GMT  
		Size: 791.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da0220763bbe5d0f53b35a3e7300676551aa3b30f9df0941ca6af16eda4b5e36`  
		Last Modified: Fri, 16 Jan 2026 00:47:26 GMT  
		Size: 295.8 MB (295760696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3721afa4689a36f6a7a1fa534586c03581119ab31ffd77687ad250f7d1d7a9ad`  
		Last Modified: Fri, 16 Jan 2026 00:47:20 GMT  
		Size: 4.0 KB (4047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9e995c071fbc67ae6b2e1ba34fd2a0ac6ab97774aebe6cd05b69019baf48c0c`  
		Last Modified: Fri, 16 Jan 2026 01:31:25 GMT  
		Size: 2.4 KB (2358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:32-fpm` - unknown; unknown

```console
$ docker pull nextcloud@sha256:919245e086c6a805a31469eb38acfaea0aec1d4907a85a43303d270d9fa3d551
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 KB (46743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e350220e6665fc1e05429f91fbb1924ab9cea341cebd9088ce023345cb43318`

```dockerfile
```

-	Layers:
	-	`sha256:943e9aabd1f88680377afc6b8ac8ba3c39a892528ea208c85792bce0925b8985`  
		Last Modified: Fri, 16 Jan 2026 03:51:22 GMT  
		Size: 46.7 KB (46743 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:32-fpm` - linux; arm variant v5

```console
$ docker pull nextcloud@sha256:8a416e74be0ec706efbca0eefd210e83429ae3be35ba36d4a291928648b4dfc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **497.3 MB (497327698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf0d8ad9c5ae4540bf6b026255ca86c3fe2a6689436b6dddb1488f0c84bfa39f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:16:05 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 13 Jan 2026 01:16:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 13 Jan 2026 01:16:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 01:16:29 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 13 Jan 2026 01:16:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 13 Jan 2026 01:16:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jan 2026 01:16:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jan 2026 01:16:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 13 Jan 2026 01:16:29 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 13 Jan 2026 01:16:29 GMT
ENV PHP_VERSION=8.3.29
# Tue, 13 Jan 2026 01:16:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Tue, 13 Jan 2026 01:16:29 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Tue, 13 Jan 2026 01:54:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 13 Jan 2026 01:54:34 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:57:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 13 Jan 2026 01:57:23 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:57:23 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 13 Jan 2026 01:57:23 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 13 Jan 2026 01:57:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 13 Jan 2026 01:57:23 GMT
WORKDIR /var/www/html
# Tue, 13 Jan 2026 01:57:24 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 13 Jan 2026 01:57:24 GMT
STOPSIGNAL SIGQUIT
# Tue, 13 Jan 2026 01:57:24 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 13 Jan 2026 01:57:24 GMT
CMD ["php-fpm"]
# Thu, 15 Jan 2026 23:22:04 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-7.q16-10-extra         rsync     ;     apt-get dist-clean;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Thu, 15 Jan 2026 23:25:22 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 15 Jan 2026 23:25:22 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 15 Jan 2026 23:25:22 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Thu, 15 Jan 2026 23:25:22 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         liblz4-dev         libmagickwand-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.28;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.1;     pecl install --configureoptions 'enable-memcached-igbinary="yes"'         memcached-3.4.0;     pecl install --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"'         redis-6.3.0;         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -rt dpkg-query --search         | awk 'sub(":$", "", $1) { print $1 }'         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     apt-get dist-clean # buildkit
# Thu, 15 Jan 2026 23:25:22 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Thu, 15 Jan 2026 23:25:22 GMT
VOLUME [/var/www/html]
# Thu, 15 Jan 2026 23:25:22 GMT
ENV NEXTCLOUD_VERSION=32.0.4
# Thu, 15 Jan 2026 23:26:12 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://github.com/nextcloud-releases/server/releases/download/v32.0.4/nextcloud-32.0.4.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://github.com/nextcloud-releases/server/releases/download/v32.0.4/nextcloud-32.0.4.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     apt-get dist-clean # buildkit
# Thu, 15 Jan 2026 23:26:12 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 15 Jan 2026 23:26:12 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Thu, 15 Jan 2026 23:26:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jan 2026 23:26:12 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c113d410d30c2c035a105b56d3937958c81fbe2530f44add3bae903be6864324`  
		Last Modified: Tue, 13 Jan 2026 00:42:30 GMT  
		Size: 27.9 MB (27942724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e7be526e7f2aae15d02636bd56985cdd6d3496f92903ceab1265dc81401486`  
		Last Modified: Tue, 13 Jan 2026 01:20:25 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7c21895b5d9edc00c028a48a0ad6521cb9a9d7a2a02f514629e88412680b18`  
		Last Modified: Tue, 13 Jan 2026 01:20:32 GMT  
		Size: 94.9 MB (94876513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f733d0e1fc41b31ef82e6988dd6007e55f6ad27329a5d0d88beb4b4df46450`  
		Last Modified: Tue, 13 Jan 2026 01:20:25 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35efc510b309734a7243f3c6a5ba0eca1ce94e1e0bda9a45e83fe8008602462`  
		Last Modified: Tue, 13 Jan 2026 01:57:42 GMT  
		Size: 12.7 MB (12747386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf58d88dd618807fb2dca946d456aed818ffc5655a9e3cf61b477cdb6eb73a98`  
		Last Modified: Tue, 13 Jan 2026 01:57:41 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20bb909a4861c8645b41d8bd3b7dde4b08c6e35785effaf327e4ee75ef80612a`  
		Last Modified: Tue, 13 Jan 2026 01:57:42 GMT  
		Size: 10.7 MB (10691085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5c8bd0eef5b831bdc3da7a71ad370b07555ad93feb7053013ffabcd3ea7b0e`  
		Last Modified: Tue, 13 Jan 2026 01:57:41 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a0220b9052a72b32bb88403dd5782e9edfa229f6ce7304cfdce5fb16d29623a`  
		Last Modified: Tue, 13 Jan 2026 01:57:41 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0aa456bbdb526836dd6b6b14ca798aad6aff6fcb413f468055c3e1a0fa11339`  
		Last Modified: Tue, 13 Jan 2026 01:57:41 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7455b0df64b5f9a9b278fb9dea154d38fef53a1f2eeb419e87b393f5c80fbe`  
		Last Modified: Tue, 13 Jan 2026 01:57:41 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3dad5cc60faa1825bf793b7dc064e89239589d62df2789a6de48e25fe7860a6`  
		Last Modified: Thu, 15 Jan 2026 23:26:57 GMT  
		Size: 20.2 MB (20163438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:911bf5803e6f865b14dc2246e88f061ff709088fe56bd4843841e56cf4d19b34`  
		Last Modified: Thu, 15 Jan 2026 23:26:58 GMT  
		Size: 35.1 MB (35129625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d7c7643ff5454eda5048e04079f548cbed43558c06ae4b5795927bae4e9d18`  
		Last Modified: Thu, 15 Jan 2026 23:26:56 GMT  
		Size: 795.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f311528600d42a6130469a2d2f2a21340f82f575a1ddae04ed53ebc22c49389f`  
		Last Modified: Thu, 15 Jan 2026 23:27:04 GMT  
		Size: 295.8 MB (295756625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74591ee9fc1bc85f5b32e60549b36ab5a506b8a18e87803c897526642c5619f`  
		Last Modified: Thu, 15 Jan 2026 23:26:56 GMT  
		Size: 4.0 KB (4047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e334fd0713b3b14de91d0d8f42e2065d3c0bfed94f30473ce66dd2e151534a22`  
		Last Modified: Thu, 15 Jan 2026 23:26:56 GMT  
		Size: 2.4 KB (2358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:32-fpm` - unknown; unknown

```console
$ docker pull nextcloud@sha256:2b9a112f9efca92bb43525c19007f3a49a966a63102747b38965027f037736f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 KB (46855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c0b04a6e0a87a1eb2bdbf0916526561dd8381e9fa8f2399db59b74aa145f3e`

```dockerfile
```

-	Layers:
	-	`sha256:37e43e95725f9253b55760e6becd3082b76a5ea76eff2533763a919393e60e66`  
		Last Modified: Fri, 16 Jan 2026 00:53:16 GMT  
		Size: 46.9 KB (46855 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:32-fpm` - linux; arm variant v7

```console
$ docker pull nextcloud@sha256:d5db9284d24c2a6012f75108c1d5ad2db1c937823ab18d37cdc74586c98171aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **483.9 MB (483866118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35885b57fbc905f66204c279d95905685e9c9bdd9de8a7e8a37b0ad302e8890b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:30:08 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 13 Jan 2026 01:30:26 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 13 Jan 2026 01:30:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 01:30:26 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 13 Jan 2026 01:30:26 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 13 Jan 2026 01:30:26 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jan 2026 01:30:26 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jan 2026 01:30:26 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 13 Jan 2026 01:30:26 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 13 Jan 2026 01:30:26 GMT
ENV PHP_VERSION=8.3.29
# Tue, 13 Jan 2026 01:30:26 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Tue, 13 Jan 2026 01:30:26 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Tue, 13 Jan 2026 02:04:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 13 Jan 2026 02:04:26 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 02:07:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 13 Jan 2026 02:07:01 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 02:07:01 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 13 Jan 2026 02:07:01 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 13 Jan 2026 02:07:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 13 Jan 2026 02:07:01 GMT
WORKDIR /var/www/html
# Tue, 13 Jan 2026 02:07:01 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 13 Jan 2026 02:07:01 GMT
STOPSIGNAL SIGQUIT
# Tue, 13 Jan 2026 02:07:01 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 13 Jan 2026 02:07:01 GMT
CMD ["php-fpm"]
# Thu, 15 Jan 2026 23:31:48 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-7.q16-10-extra         rsync     ;     apt-get dist-clean;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Thu, 15 Jan 2026 23:34:48 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 15 Jan 2026 23:34:48 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 15 Jan 2026 23:34:48 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Thu, 15 Jan 2026 23:34:48 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         liblz4-dev         libmagickwand-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.28;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.1;     pecl install --configureoptions 'enable-memcached-igbinary="yes"'         memcached-3.4.0;     pecl install --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"'         redis-6.3.0;         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -rt dpkg-query --search         | awk 'sub(":$", "", $1) { print $1 }'         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     apt-get dist-clean # buildkit
# Thu, 15 Jan 2026 23:34:49 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Thu, 15 Jan 2026 23:34:49 GMT
VOLUME [/var/www/html]
# Thu, 15 Jan 2026 23:34:49 GMT
ENV NEXTCLOUD_VERSION=32.0.4
# Thu, 15 Jan 2026 23:35:38 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://github.com/nextcloud-releases/server/releases/download/v32.0.4/nextcloud-32.0.4.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://github.com/nextcloud-releases/server/releases/download/v32.0.4/nextcloud-32.0.4.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     apt-get dist-clean # buildkit
# Thu, 15 Jan 2026 23:35:38 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 15 Jan 2026 23:35:38 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Thu, 15 Jan 2026 23:35:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jan 2026 23:35:38 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:33 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36491688ff9ae8bfc74b55b789c22535732fca45414c5ddb17bc6ce4794330e6`  
		Last Modified: Tue, 13 Jan 2026 01:33:59 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320ee626e0f97eedc4aadf2ebf2c0e99680b08b5ab80c3c22bf0ac1bd7719325`  
		Last Modified: Tue, 13 Jan 2026 01:34:14 GMT  
		Size: 86.2 MB (86244928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e688a941b6fc2fb8e3c8f8d8deb19b2de430c87ef77aa0b8608cafc4fef0844e`  
		Last Modified: Tue, 13 Jan 2026 01:33:51 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2183213553f6f0bc62d3e713fc8cb0122ecb02c6b6a7c62c72d5e8e1a3974f`  
		Last Modified: Tue, 13 Jan 2026 02:07:18 GMT  
		Size: 12.7 MB (12747463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6769fcdecadb41b5acf8eb6f70038a9eb7c16472154663391f830c9bf91d7ce9`  
		Last Modified: Tue, 13 Jan 2026 02:07:17 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1506cc215aa13e29f47eebd486c7b358a900685ebd24adb4a0121ce668007e`  
		Last Modified: Tue, 13 Jan 2026 02:07:18 GMT  
		Size: 10.1 MB (10080525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd086c008ac300640cd1de2c3dd20e45b491e3687056a8f95d6e0e5f67d7fae`  
		Last Modified: Tue, 13 Jan 2026 02:07:17 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c28f9ed81086a266390c14910d96fd1069f1b434025cbe119f660437626507`  
		Last Modified: Tue, 13 Jan 2026 02:07:17 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d97b85bf28fdcf7e99bb1ef20369d13da2cdbbb377815aa54e3a088f42005d`  
		Last Modified: Tue, 13 Jan 2026 02:07:17 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ccba46ecd0869b2705bd846296f85847c79eb3fc69859f5877e77ba58cd0c8b`  
		Last Modified: Tue, 13 Jan 2026 02:07:17 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5448bc3a8f04885d0f266e7366764bc09ac9cb8db0877a9e334e0e368730c8c9`  
		Last Modified: Thu, 15 Jan 2026 23:36:32 GMT  
		Size: 18.1 MB (18086955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae135ad825f73bdc990c163c8d174ee9cfc028d34da50261e732eb528122a4c`  
		Last Modified: Thu, 15 Jan 2026 23:36:26 GMT  
		Size: 34.7 MB (34720578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a16c14f16557fe50a2abc6ecc1ecb60b7ab8c120286049b40a2526af8482f7`  
		Last Modified: Thu, 15 Jan 2026 23:36:23 GMT  
		Size: 792.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1e6225ce91f41a3a5b352086ff67a09bbfa449d559ae4c163c936d9acd0a6d`  
		Last Modified: Thu, 15 Jan 2026 23:36:33 GMT  
		Size: 295.8 MB (295756796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27264ca7345737062e89eae2b261e94e0655292923043f911985b8b8c9fffa8`  
		Last Modified: Thu, 15 Jan 2026 23:36:23 GMT  
		Size: 4.0 KB (4047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0784b4b162ca822429d24adf84d1f8e6c2120e25960a9a45798cf12347892f43`  
		Last Modified: Thu, 15 Jan 2026 23:36:23 GMT  
		Size: 2.4 KB (2358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:32-fpm` - unknown; unknown

```console
$ docker pull nextcloud@sha256:4da3a43cce14d7bdc8dce13c3f88365174672fb6dd4d6df38729ea39a8c0c0cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 KB (46855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ed60755b20ca36affa230795f5c55e2e00db4402e1c664f6de2da51e44ff833`

```dockerfile
```

-	Layers:
	-	`sha256:f381bad4f57c425d736d156d9943b85e4ca46f27ee048aada0720d79b08d726f`  
		Last Modified: Fri, 16 Jan 2026 00:53:20 GMT  
		Size: 46.9 KB (46855 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:32-fpm` - linux; arm64 variant v8

```console
$ docker pull nextcloud@sha256:714ae022c4f4f1e4cb69a19ace2e0abec1860428f31663a5d43e6adf735b95b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **517.4 MB (517443002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c23fae981355035f9d6234d3acf1508347054277b1a49d8a477cbf9f7d8cae1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:23:47 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 13 Jan 2026 01:24:04 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 13 Jan 2026 01:24:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 01:24:04 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 13 Jan 2026 01:24:04 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 13 Jan 2026 01:24:04 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jan 2026 01:24:04 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jan 2026 01:24:04 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 13 Jan 2026 01:24:04 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 13 Jan 2026 01:24:04 GMT
ENV PHP_VERSION=8.3.29
# Tue, 13 Jan 2026 01:24:04 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Tue, 13 Jan 2026 01:24:04 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Tue, 13 Jan 2026 01:42:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 13 Jan 2026 01:42:36 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:46:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 13 Jan 2026 01:46:23 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:46:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 13 Jan 2026 01:46:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 13 Jan 2026 01:46:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 13 Jan 2026 01:46:24 GMT
WORKDIR /var/www/html
# Tue, 13 Jan 2026 01:46:24 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 13 Jan 2026 01:46:24 GMT
STOPSIGNAL SIGQUIT
# Tue, 13 Jan 2026 01:46:24 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 13 Jan 2026 01:46:24 GMT
CMD ["php-fpm"]
# Fri, 16 Jan 2026 00:43:31 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-7.q16-10-extra         rsync     ;     apt-get dist-clean;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Fri, 16 Jan 2026 00:46:18 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 16 Jan 2026 00:46:18 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 16 Jan 2026 00:46:18 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Fri, 16 Jan 2026 00:46:18 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         liblz4-dev         libmagickwand-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.28;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.1;     pecl install --configureoptions 'enable-memcached-igbinary="yes"'         memcached-3.4.0;     pecl install --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"'         redis-6.3.0;         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -rt dpkg-query --search         | awk 'sub(":$", "", $1) { print $1 }'         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     apt-get dist-clean # buildkit
# Fri, 16 Jan 2026 00:46:18 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Fri, 16 Jan 2026 00:46:18 GMT
VOLUME [/var/www/html]
# Fri, 16 Jan 2026 00:46:18 GMT
ENV NEXTCLOUD_VERSION=32.0.4
# Fri, 16 Jan 2026 00:46:56 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://github.com/nextcloud-releases/server/releases/download/v32.0.4/nextcloud-32.0.4.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://github.com/nextcloud-releases/server/releases/download/v32.0.4/nextcloud-32.0.4.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     apt-get dist-clean # buildkit
# Fri, 16 Jan 2026 00:46:56 GMT
COPY *.sh upgrade.exclude / # buildkit
# Fri, 16 Jan 2026 00:46:56 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Fri, 16 Jan 2026 00:46:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Jan 2026 00:46:56 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13d132b40432b5921ea4a0d8f8e7ba1498cf5d180ee6b838e8784fc68b4f290`  
		Last Modified: Tue, 13 Jan 2026 01:27:28 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84214cabe7a0b52ad7e20794f8212067692bcb023d5919c21a52fc3f4e89fed2`  
		Last Modified: Tue, 13 Jan 2026 01:28:11 GMT  
		Size: 110.2 MB (110164212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e530eb23a62e9f74602d358b91329caecc881f4add6938b4c0b366bff913917e`  
		Last Modified: Tue, 13 Jan 2026 01:28:03 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5b69d3488458e872204811902e41919e41e3e8a3d5265f284ceea2242f1aa3`  
		Last Modified: Tue, 13 Jan 2026 01:46:42 GMT  
		Size: 12.7 MB (12749554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2206ee6bf8726ab655595b41953e70d19657a515422f73867157962969e7134d`  
		Last Modified: Tue, 13 Jan 2026 01:46:41 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc3e2097092bb77be0c9ff8a42b9f064273554e439de1898dc6b8b097192059`  
		Last Modified: Tue, 13 Jan 2026 01:46:42 GMT  
		Size: 11.9 MB (11925293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec13ddc9ed29ced5267644073be831e01cc6bbe71e2b3e641de37370fef59e94`  
		Last Modified: Tue, 13 Jan 2026 01:46:41 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e30b03ff955fcec114030a1a2af5be6bfe1f1433882abedf1fc98978a12a5af2`  
		Last Modified: Tue, 13 Jan 2026 01:46:41 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbfe2bac31f2101999887cdeada1f9589faea34a47220e606f591414c23cf4ac`  
		Last Modified: Tue, 13 Jan 2026 01:46:41 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48508da8ee9af15207883b68bc470f83e474cf979bf1aa3a6b1e0a236a47d8d`  
		Last Modified: Tue, 13 Jan 2026 01:46:42 GMT  
		Size: 9.2 KB (9183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa38c0fa6a1ec920a667d339d805dd204b90eccf9f03b9bdb3e9fc0a5f166843`  
		Last Modified: Fri, 16 Jan 2026 00:47:42 GMT  
		Size: 19.8 MB (19792568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea966dfc91fb3e4c71015b9e4ee70eab9515e160a5dc536458cdf101946db91c`  
		Last Modified: Fri, 16 Jan 2026 00:47:45 GMT  
		Size: 36.9 MB (36897223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165ce3640d01fd534c9d0302160ef82c37aabce64e63b8a97c11e9acda80172d`  
		Last Modified: Fri, 16 Jan 2026 00:47:41 GMT  
		Size: 793.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9dabef486758a4a8e53d6d439f41a7e5c4fb9ca6dd5cee2c6a8b5d0263ad08`  
		Last Modified: Fri, 16 Jan 2026 00:48:00 GMT  
		Size: 295.8 MB (295759815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aed99b1cf128b4e2e41a5baaf8c7acad424d2a13562331c3d25a9a69ceca1b98`  
		Last Modified: Fri, 16 Jan 2026 00:47:41 GMT  
		Size: 4.0 KB (4047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970c135253ab07b3a4affff5300d308438b48ade6f0a9ade77054c279b26cf8e`  
		Last Modified: Fri, 16 Jan 2026 00:47:41 GMT  
		Size: 2.4 KB (2358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:32-fpm` - unknown; unknown

```console
$ docker pull nextcloud@sha256:35c03dcc0d5fe0d2766aa7e39e58ac0219ccc389c3be635c842fc5b13d25b02d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 KB (46892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7689fddd3ce367cf887ff88ccfdaf721f72b844c09192ad2651fcc8b7f62186`

```dockerfile
```

-	Layers:
	-	`sha256:085d41cfc566fdec5327797ebdba5dab30731f516b3ffe5dc15ff415a5688dca`  
		Last Modified: Fri, 16 Jan 2026 03:51:50 GMT  
		Size: 46.9 KB (46892 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:32-fpm` - linux; 386

```console
$ docker pull nextcloud@sha256:e489635db05fdbe749294ecfcbcbf858c4871673688fbaad4dd16a42d63323f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **526.8 MB (526806628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:addbdc3fd2a25a0b75fc491cd4c4e1ecf7d3d52b03bb9617bf1cb4a86a4871a8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:33:37 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 13 Jan 2026 01:33:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 13 Jan 2026 01:33:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 01:33:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 13 Jan 2026 01:33:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 13 Jan 2026 01:33:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jan 2026 01:33:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jan 2026 01:33:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 13 Jan 2026 01:33:56 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 13 Jan 2026 01:33:56 GMT
ENV PHP_VERSION=8.3.29
# Tue, 13 Jan 2026 01:33:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Tue, 13 Jan 2026 01:33:56 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Tue, 13 Jan 2026 01:38:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 13 Jan 2026 01:38:16 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:41:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 13 Jan 2026 01:41:04 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:41:05 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 13 Jan 2026 01:41:05 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 13 Jan 2026 01:41:05 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 13 Jan 2026 01:41:05 GMT
WORKDIR /var/www/html
# Tue, 13 Jan 2026 01:41:05 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 13 Jan 2026 01:41:05 GMT
STOPSIGNAL SIGQUIT
# Tue, 13 Jan 2026 01:41:05 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 13 Jan 2026 01:41:05 GMT
CMD ["php-fpm"]
# Thu, 15 Jan 2026 23:25:10 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-7.q16-10-extra         rsync     ;     apt-get dist-clean;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Thu, 15 Jan 2026 23:27:54 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 15 Jan 2026 23:27:54 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 15 Jan 2026 23:27:54 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Thu, 15 Jan 2026 23:27:54 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         liblz4-dev         libmagickwand-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.28;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.1;     pecl install --configureoptions 'enable-memcached-igbinary="yes"'         memcached-3.4.0;     pecl install --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"'         redis-6.3.0;         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -rt dpkg-query --search         | awk 'sub(":$", "", $1) { print $1 }'         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     apt-get dist-clean # buildkit
# Thu, 15 Jan 2026 23:27:54 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Thu, 15 Jan 2026 23:27:54 GMT
VOLUME [/var/www/html]
# Thu, 15 Jan 2026 23:27:54 GMT
ENV NEXTCLOUD_VERSION=32.0.4
# Thu, 15 Jan 2026 23:28:37 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://github.com/nextcloud-releases/server/releases/download/v32.0.4/nextcloud-32.0.4.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://github.com/nextcloud-releases/server/releases/download/v32.0.4/nextcloud-32.0.4.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     apt-get dist-clean # buildkit
# Thu, 15 Jan 2026 23:28:37 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 15 Jan 2026 23:28:37 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Thu, 15 Jan 2026 23:28:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jan 2026 23:28:37 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:27bb6d39eda5ced7626db280c3902aacdfade5acd11a16ef9618e3185f69b102`  
		Last Modified: Tue, 13 Jan 2026 00:43:03 GMT  
		Size: 31.3 MB (31288476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27230fde851a8ba195adcb6333cfa67957c7a83f33fac0533fd0c5f0fafc92c`  
		Last Modified: Tue, 13 Jan 2026 01:37:32 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234fdaa90e96d4f83a73e02e5002d69553b0c70b6c2a2b40e01e0807e5983e0d`  
		Last Modified: Tue, 13 Jan 2026 01:37:40 GMT  
		Size: 116.1 MB (116138984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8db1614bf6fdc0be392b449bb12139cda1e22744df69e5feb36db38681645723`  
		Last Modified: Tue, 13 Jan 2026 01:37:32 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837b04c1b6065253bf0fd798d14b28d0c2c7c44a70e14b706adbba72d1a4fbfc`  
		Last Modified: Tue, 13 Jan 2026 01:41:25 GMT  
		Size: 12.7 MB (12748848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13314703fb70eb9ec7afea8c694e92b171488d7b3cbb686f73ea063a436d0e1`  
		Last Modified: Tue, 13 Jan 2026 01:41:22 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05f78f0e933428e9aee99771b99c57d823a4ab0ec1603f1b3fcb2c24874c06e`  
		Last Modified: Tue, 13 Jan 2026 01:41:23 GMT  
		Size: 12.1 MB (12105001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e5c6d929a425179fa29ca7584bd1c39ae300cdc6d748afbf71b48c646411fe`  
		Last Modified: Tue, 13 Jan 2026 01:41:22 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b400f08edbd70de57d322aa98be3ca3d6cd700d331c95bbfe4ab9de1286a7e3e`  
		Last Modified: Tue, 13 Jan 2026 01:41:22 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29a54e9f6bcaa79e204e16117d7bab16eb8755b1bdb6411dd63e68f010890fe8`  
		Last Modified: Tue, 13 Jan 2026 01:41:23 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2548b308ec28d77103351d2f776b9271787db62edcb1ae38636a3a6eafef73f6`  
		Last Modified: Tue, 13 Jan 2026 01:41:23 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97bcf315dc0d1871ea7bd98cbc1b8f447b6d3e82aac75588f887dd2a94943549`  
		Last Modified: Thu, 15 Jan 2026 23:29:19 GMT  
		Size: 21.3 MB (21328067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28477d04e8cc4272a99fe9cf873470c0dfd7c6ca60faa3a2785ab0f8b88a4b5c`  
		Last Modified: Thu, 15 Jan 2026 23:29:20 GMT  
		Size: 37.4 MB (37418270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d186c851fdbc95c1a17ae6373987a2181e97b6b296ac4930acfa321d7b78ca`  
		Last Modified: Thu, 15 Jan 2026 23:29:17 GMT  
		Size: 791.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc01d2e0795e877eb48f1643ce0d5c8f7b9b545e8b31dec624e1c37d290be32f`  
		Last Modified: Thu, 15 Jan 2026 23:29:56 GMT  
		Size: 295.8 MB (295758691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e902544fbd67c97e582841155811154556815bc084e5d392e0fac6e238528ff`  
		Last Modified: Thu, 15 Jan 2026 23:29:17 GMT  
		Size: 4.0 KB (4046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff37c002abb24503dcf98f4096dc2e5377807a118841911eccd64634ca01a00e`  
		Last Modified: Thu, 15 Jan 2026 23:29:17 GMT  
		Size: 2.4 KB (2355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:32-fpm` - unknown; unknown

```console
$ docker pull nextcloud@sha256:70cd38f20553ed7eac8bc2b3e5ebbc7a79660fb3fffe705ef1406a1ad9d2efa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 KB (46705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01b26e9c46cd5c4fff6f28ea9fa2239a4c55f7e74722ecdf542cac4a23891fe7`

```dockerfile
```

-	Layers:
	-	`sha256:cf9472c09aba6526533f016f46300c153367554c2cd40574c1e4b3343d5451cb`  
		Last Modified: Fri, 16 Jan 2026 00:53:25 GMT  
		Size: 46.7 KB (46705 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:32-fpm` - linux; ppc64le

```console
$ docker pull nextcloud@sha256:21d33fb59e6d83649446c506aed46af8b1ab5dc93676d208e95f93ddc678d8a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.1 MB (525060169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2f6627c2f31d4e55a4910a35f4b8bccd3e0f446d2d62a06e01b77265ce73d60`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:49:24 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 13 Jan 2026 01:50:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 13 Jan 2026 01:50:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 01:50:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 13 Jan 2026 01:50:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 13 Jan 2026 01:50:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jan 2026 01:50:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jan 2026 01:50:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 13 Jan 2026 01:50:29 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 13 Jan 2026 01:50:29 GMT
ENV PHP_VERSION=8.3.29
# Tue, 13 Jan 2026 01:50:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Tue, 13 Jan 2026 01:50:29 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Tue, 13 Jan 2026 02:51:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 13 Jan 2026 02:51:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 03:01:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 13 Jan 2026 03:01:02 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 03:01:02 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 13 Jan 2026 03:01:03 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 13 Jan 2026 03:01:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 13 Jan 2026 03:01:04 GMT
WORKDIR /var/www/html
# Tue, 13 Jan 2026 03:01:04 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 13 Jan 2026 03:01:04 GMT
STOPSIGNAL SIGQUIT
# Tue, 13 Jan 2026 03:01:04 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 13 Jan 2026 03:01:04 GMT
CMD ["php-fpm"]
# Fri, 16 Jan 2026 01:11:56 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-7.q16-10-extra         rsync     ;     apt-get dist-clean;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Fri, 16 Jan 2026 01:17:59 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 16 Jan 2026 01:17:59 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 16 Jan 2026 01:17:59 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Fri, 16 Jan 2026 01:17:59 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         liblz4-dev         libmagickwand-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.28;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.1;     pecl install --configureoptions 'enable-memcached-igbinary="yes"'         memcached-3.4.0;     pecl install --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"'         redis-6.3.0;         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -rt dpkg-query --search         | awk 'sub(":$", "", $1) { print $1 }'         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     apt-get dist-clean # buildkit
# Fri, 16 Jan 2026 01:18:00 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Fri, 16 Jan 2026 01:18:00 GMT
VOLUME [/var/www/html]
# Fri, 16 Jan 2026 01:18:00 GMT
ENV NEXTCLOUD_VERSION=32.0.4
# Fri, 16 Jan 2026 01:19:12 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://github.com/nextcloud-releases/server/releases/download/v32.0.4/nextcloud-32.0.4.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://github.com/nextcloud-releases/server/releases/download/v32.0.4/nextcloud-32.0.4.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     apt-get dist-clean # buildkit
# Fri, 16 Jan 2026 01:19:13 GMT
COPY *.sh upgrade.exclude / # buildkit
# Fri, 16 Jan 2026 01:19:14 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Fri, 16 Jan 2026 01:19:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Jan 2026 01:19:14 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:13 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4729c2d5c144b66bc0a7de79ce37a807764c298349e33d3b4d2b9ffc6e4f86da`  
		Last Modified: Tue, 13 Jan 2026 01:56:13 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b5312002cd976a0822f64d1b71b8a785c0ab1242111634934907ad0ff8cd084`  
		Last Modified: Tue, 13 Jan 2026 01:56:21 GMT  
		Size: 109.6 MB (109597601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c320c737217d4d4f5283740cc3e07729118082922eab5fedf369acbd762089c`  
		Last Modified: Tue, 13 Jan 2026 01:56:13 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079babc83266d1b422a9e33afbea7ebf587db197d12fc3dd5a38ed158cc219e6`  
		Last Modified: Tue, 13 Jan 2026 02:56:13 GMT  
		Size: 12.8 MB (12757195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da6cac6ede5a772b3b4d425e7c9815ff095e155220110674e6be4b29b4d8f60`  
		Last Modified: Tue, 13 Jan 2026 02:56:10 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1971f055611683789d641dbf83c840e6483c547db1910a1e41f07bc03f3fd56d`  
		Last Modified: Tue, 13 Jan 2026 03:01:41 GMT  
		Size: 12.4 MB (12438207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87378c2bc748ef177e1d3793e6a5e87b8d82e6b63bee0a2b25d26cf305812641`  
		Last Modified: Tue, 13 Jan 2026 03:01:40 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9770f04d48f8082f296be54ea32909631fa4ebedd336d9d372a00643fdc3385c`  
		Last Modified: Tue, 13 Jan 2026 03:01:40 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c2cf33f9cc41e3901a358ca65b2f4df4fa978d50019faa28a029d9ef582f2dc`  
		Last Modified: Tue, 13 Jan 2026 03:01:40 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa4b9405e794c280607969333629c134e954fdb10a5ca568b55ff04e4b86b1d`  
		Last Modified: Tue, 13 Jan 2026 03:01:40 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d62a3227e26c5b30798954db8be2c4b18cf7f2e94f5274f7833e81639f7e6b45`  
		Last Modified: Fri, 16 Jan 2026 01:20:48 GMT  
		Size: 22.2 MB (22163435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0c7f87fb59197658bda657e85bc79dd24bd9c3f45588577538864398fcc38e`  
		Last Modified: Fri, 16 Jan 2026 01:20:50 GMT  
		Size: 38.7 MB (38727083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21149967ec1ac0b8e5b076b49408c01e002ea1815f961815ee1524a9a2702746`  
		Last Modified: Fri, 16 Jan 2026 01:20:46 GMT  
		Size: 794.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6281d86cc937c48cbbe1c80e8ee3fb3c2f2da3cca6dde83569aa1b9dbd15a61c`  
		Last Modified: Fri, 16 Jan 2026 01:21:33 GMT  
		Size: 295.8 MB (295760749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00717ed74891f8958468afb14131bec7dbefdf32095a65e8afa0f517971ff6d9`  
		Last Modified: Fri, 16 Jan 2026 01:20:46 GMT  
		Size: 4.0 KB (4046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16611ec1544674e4fd2ca1e678e25136ae06f80166b7de6ab620fcef51eb014d`  
		Last Modified: Fri, 16 Jan 2026 01:20:46 GMT  
		Size: 2.4 KB (2360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:32-fpm` - unknown; unknown

```console
$ docker pull nextcloud@sha256:e300c3e440807debdf27571345f3bc651bd3d3bed1438496563ce3e07b11b822
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 KB (46793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5efd153fcca7616ca0e49870c77cce8e3b492da42a4029c61555d66c9b137d4`

```dockerfile
```

-	Layers:
	-	`sha256:796fc09381bbbe5739188c3589c8374a1a1379f652b3eec98ed51f89d3eeda0f`  
		Last Modified: Fri, 16 Jan 2026 03:52:07 GMT  
		Size: 46.8 KB (46793 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:32-fpm` - linux; riscv64

```console
$ docker pull nextcloud@sha256:0f737005087dbd0c5938804e55039d6dd9081f3a1e589b0db583a06d7e1214d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **557.5 MB (557543621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f5b9b29604eed2c0503213f4ea5f7c8441070fe1b2aa5c801eab608b18545d8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 08:15:35 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 30 Dec 2025 08:17:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 30 Dec 2025 08:17:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 08:17:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Dec 2025 08:17:35 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 30 Dec 2025 08:17:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Dec 2025 08:17:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Dec 2025 08:17:35 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Dec 2025 08:17:35 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 30 Dec 2025 08:17:35 GMT
ENV PHP_VERSION=8.3.29
# Tue, 30 Dec 2025 08:17:35 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Tue, 30 Dec 2025 08:17:35 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Tue, 30 Dec 2025 16:24:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 30 Dec 2025 16:24:12 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 30 Dec 2025 18:31:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 30 Dec 2025 18:31:53 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 30 Dec 2025 18:31:54 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 30 Dec 2025 18:31:54 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 30 Dec 2025 18:31:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 30 Dec 2025 18:31:55 GMT
WORKDIR /var/www/html
# Tue, 30 Dec 2025 18:31:55 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 30 Dec 2025 18:31:55 GMT
STOPSIGNAL SIGQUIT
# Tue, 30 Dec 2025 18:31:55 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 30 Dec 2025 18:31:55 GMT
CMD ["php-fpm"]
# Thu, 01 Jan 2026 22:24:54 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-7.q16-10-extra         rsync     ;     apt-get dist-clean;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Thu, 01 Jan 2026 22:52:33 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 01 Jan 2026 22:52:33 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 01 Jan 2026 22:52:33 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Thu, 01 Jan 2026 22:52:33 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         liblz4-dev         libmagickwand-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.28;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.1;     pecl install --configureoptions 'enable-memcached-igbinary="yes"'         memcached-3.4.0;     pecl install --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"'         redis-6.3.0;         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -rt dpkg-query --search         | awk 'sub(":$", "", $1) { print $1 }'         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     apt-get dist-clean # buildkit
# Thu, 01 Jan 2026 22:52:34 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Thu, 01 Jan 2026 22:52:34 GMT
VOLUME [/var/www/html]
# Thu, 01 Jan 2026 22:52:34 GMT
ENV NEXTCLOUD_VERSION=32.0.3
# Thu, 01 Jan 2026 22:57:03 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://github.com/nextcloud-releases/server/releases/download/v32.0.3/nextcloud-32.0.3.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://github.com/nextcloud-releases/server/releases/download/v32.0.3/nextcloud-32.0.3.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     apt-get dist-clean # buildkit
# Thu, 01 Jan 2026 22:57:04 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 01 Jan 2026 22:57:04 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Thu, 01 Jan 2026 22:57:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 01 Jan 2026 22:57:04 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:96d8ad310358e2403b7b44cf38db606dc1ea6b58b915684d38e13f573860f64e`  
		Last Modified: Tue, 30 Dec 2025 00:53:22 GMT  
		Size: 28.3 MB (28273129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a44b1edad4acbdf2eb79bc4ed79ff402d6af38c94857a826c4e8f406f68b8b4`  
		Last Modified: Tue, 30 Dec 2025 09:22:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43a8c50b15f754f42cc587a4d423f958f4de65b8cc8da75adfbac833ca87e54`  
		Last Modified: Tue, 30 Dec 2025 11:32:37 GMT  
		Size: 146.6 MB (146578538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4346525b0d45631b779c99bb99caa2632c2822ec686a160c5f4d23f9cfac4217`  
		Last Modified: Tue, 30 Dec 2025 09:22:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee18ea173c5c5c6c9d55d60606ccc2c666bd742a0bfb4960873bb2e4dbcafa7`  
		Last Modified: Tue, 30 Dec 2025 18:35:04 GMT  
		Size: 12.8 MB (12764103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f1ef83fc744884472718d56538d0b64b61d15bbe8ea1eeb9ad097e8d9fc59f`  
		Last Modified: Tue, 30 Dec 2025 18:34:59 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461a4b551a343a39a0b2a023efe9a67f5f45d7e47ca7c663d78feed3b09230d1`  
		Last Modified: Tue, 30 Dec 2025 18:35:01 GMT  
		Size: 11.5 MB (11467654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ebc7eb814238ee4ab75b90938a361cbe8dff404e4a1ab4fb792478727f8aeab`  
		Last Modified: Tue, 30 Dec 2025 18:34:59 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3e66753effcba44cb202465ae6c1b51282949ef5efc010151bb01f28ae35f3`  
		Last Modified: Tue, 30 Dec 2025 18:34:59 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db2e3596c89a7e2cf845d48a7cc8b915c14e11317097cf671bf40b2a9f7cd85`  
		Last Modified: Tue, 30 Dec 2025 18:34:59 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acbfbbe5168ab0c2eb8da9c82a09fdee2d96e7041e7ff63aa3a796dc8023aa5b`  
		Last Modified: Tue, 30 Dec 2025 18:34:59 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e114c1cda37cd3222706eb507cf7391dd19eab0bc7b8aee9f0a2106a176c52`  
		Last Modified: Thu, 01 Jan 2026 23:04:44 GMT  
		Size: 19.6 MB (19556037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9f2b6e5d39e9ddac6f4d790fe306189568bd351805169d41acda279374de66`  
		Last Modified: Thu, 01 Jan 2026 23:04:48 GMT  
		Size: 45.9 MB (45866346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a98b0e8b2ff611db44e4210ecc902c3d8f36a0d02560275e6d979b4a818dbf`  
		Last Modified: Thu, 01 Jan 2026 23:04:42 GMT  
		Size: 790.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682f24184d51416644929a45be9b1d8fd42656f897087be3010442e1762aa4d6`  
		Last Modified: Thu, 01 Jan 2026 23:04:56 GMT  
		Size: 293.0 MB (293017525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e3a2bdcce1356bda5acf0a8078cccab507d604e9d7673564cb0db483c50ae6`  
		Last Modified: Thu, 01 Jan 2026 23:04:42 GMT  
		Size: 4.0 KB (4047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20441019cb626a6b743051ef21f8f430838efe3a1c947e5659caeb9c55e4839`  
		Last Modified: Thu, 01 Jan 2026 23:04:42 GMT  
		Size: 2.4 KB (2354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:32-fpm` - unknown; unknown

```console
$ docker pull nextcloud@sha256:a88f58bdb734ab472d650c9a085dd13d8ab6998e18425777cd179064b8dd6a7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 KB (46793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8449f9f789df4d6b9fbcaac7a7c151b2d05e47961a9771630723037c8222f4fc`

```dockerfile
```

-	Layers:
	-	`sha256:f878a1f93d23430dc9c06f5b23f9c139994adda95d736788b6f0b1dca32da5b9`  
		Last Modified: Fri, 02 Jan 2026 00:50:12 GMT  
		Size: 46.8 KB (46793 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:32-fpm` - linux; s390x

```console
$ docker pull nextcloud@sha256:3d37df240b13794f0f886962debceb05f8e5db9048d5a4e54141976fa771b2b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **500.3 MB (500263074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74556d39acbc7fa7f0f62f0acf5a3561d976ebdcb545cae30908b2907cb7390f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 14:16:13 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 13 Jan 2026 14:16:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 13 Jan 2026 14:16:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 14:16:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 13 Jan 2026 14:16:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 13 Jan 2026 14:16:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jan 2026 14:16:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jan 2026 14:16:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 13 Jan 2026 14:16:27 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 13 Jan 2026 14:16:27 GMT
ENV PHP_VERSION=8.3.29
# Tue, 13 Jan 2026 14:16:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Tue, 13 Jan 2026 14:16:27 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Tue, 13 Jan 2026 14:35:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 13 Jan 2026 14:35:56 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 14:40:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 13 Jan 2026 14:40:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 14:40:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 13 Jan 2026 14:40:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 13 Jan 2026 14:40:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 13 Jan 2026 14:40:55 GMT
WORKDIR /var/www/html
# Tue, 13 Jan 2026 14:40:56 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 13 Jan 2026 14:40:56 GMT
STOPSIGNAL SIGQUIT
# Tue, 13 Jan 2026 14:40:56 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 13 Jan 2026 14:40:56 GMT
CMD ["php-fpm"]
# Thu, 15 Jan 2026 23:43:54 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-7.q16-10-extra         rsync     ;     apt-get dist-clean;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Thu, 15 Jan 2026 23:46:14 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 15 Jan 2026 23:46:14 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 15 Jan 2026 23:46:14 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Thu, 15 Jan 2026 23:46:14 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         liblz4-dev         libmagickwand-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.28;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.1;     pecl install --configureoptions 'enable-memcached-igbinary="yes"'         memcached-3.4.0;     pecl install --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"'         redis-6.3.0;         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -rt dpkg-query --search         | awk 'sub(":$", "", $1) { print $1 }'         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     apt-get dist-clean # buildkit
# Thu, 15 Jan 2026 23:46:14 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Thu, 15 Jan 2026 23:46:14 GMT
VOLUME [/var/www/html]
# Thu, 15 Jan 2026 23:46:14 GMT
ENV NEXTCLOUD_VERSION=32.0.4
# Thu, 15 Jan 2026 23:47:48 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://github.com/nextcloud-releases/server/releases/download/v32.0.4/nextcloud-32.0.4.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://github.com/nextcloud-releases/server/releases/download/v32.0.4/nextcloud-32.0.4.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     apt-get dist-clean # buildkit
# Thu, 15 Jan 2026 23:47:49 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 15 Jan 2026 23:47:49 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Thu, 15 Jan 2026 23:47:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jan 2026 23:47:49 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:2b46bc94baaae0a37e5e04b1babf7e1f37c4390b83d49c3c6820188deba770e3`  
		Last Modified: Tue, 13 Jan 2026 13:10:43 GMT  
		Size: 29.8 MB (29833411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9894d072f7628fb4f530bf099e2fb54499100da0b90309f847ed180921428d3b`  
		Last Modified: Tue, 13 Jan 2026 14:20:27 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9abe68d0a255199bdc5f33b8ae5aad991c2cd83ff816e91c885b0f731c587632`  
		Last Modified: Tue, 13 Jan 2026 14:20:34 GMT  
		Size: 92.6 MB (92566268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913be1d555d6c22e2b9e74c8919dec667845fa89c7ca3a0be23e91a59ae08c46`  
		Last Modified: Tue, 13 Jan 2026 14:20:30 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a234c5349e533abbd7faded0ce7fed4496c5e68fca1a06b3ae35944c5d895181`  
		Last Modified: Tue, 13 Jan 2026 14:39:12 GMT  
		Size: 12.7 MB (12748215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0e200882b887bebf51d03dcce7e940fd86b8da41e3afe9223cf5ddac7319d0`  
		Last Modified: Tue, 13 Jan 2026 14:39:11 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95fd9c18fea2515bb9d83d6f2851b94e36d2a913e0618fb6901e1b4d1f93b07c`  
		Last Modified: Tue, 13 Jan 2026 14:41:20 GMT  
		Size: 11.8 MB (11769863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19af0ec6bdbef3433d4e57900b1eefe0a92cb5494d747a6cd46640dbc24aadf`  
		Last Modified: Tue, 13 Jan 2026 14:41:18 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ffb22fdd18b93c5a717dea3bd810b4eda9354cc197f22584e2eeeb54c97e68`  
		Last Modified: Tue, 13 Jan 2026 14:41:19 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e267ee40aa278b286d992e53a98f31c6d802620120a16e7a5083f9d214308122`  
		Last Modified: Tue, 13 Jan 2026 14:41:19 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3a7fe5f272f72b2d53835baed308caa51dd4d619fcc27384658c9fa6903d27`  
		Last Modified: Tue, 13 Jan 2026 14:41:19 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d771ab93987f2ab8339c50aec7d08d1653256c15c43b2c92ebda193a924b0ccf`  
		Last Modified: Thu, 15 Jan 2026 23:47:41 GMT  
		Size: 20.4 MB (20403054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195327992db28976d209c410e4ee45e91b1fed77059b15262ef96295201902f9`  
		Last Modified: Thu, 15 Jan 2026 23:47:42 GMT  
		Size: 37.2 MB (37164486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b50d475b053317c70b5af34a6691acefc3cf3d60fba976690526f32cd767f3b`  
		Last Modified: Thu, 15 Jan 2026 23:47:39 GMT  
		Size: 791.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c9a4448dcd3c9bce4eeb1c2bc3fbb1af278d5d874cf603572b32f1c3a700cb4`  
		Last Modified: Thu, 15 Jan 2026 23:50:10 GMT  
		Size: 295.8 MB (295757494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cd651192982553f4b9a5e626628b085c7a8e37e8b6cc542e657f1424563e95`  
		Last Modified: Thu, 15 Jan 2026 23:48:40 GMT  
		Size: 4.0 KB (4046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:367ee19127fdb7a4c39b57225638b5834dce3ccfe18a1922154ca093a5ce4c76`  
		Last Modified: Thu, 15 Jan 2026 23:48:40 GMT  
		Size: 2.4 KB (2352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:32-fpm` - unknown; unknown

```console
$ docker pull nextcloud@sha256:5ebd0bf5bb3dafe2737ca0397a9424085ebf1241aa5a751e6ec85b4d49fea4cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 KB (46736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea2b4604fd4cc4fbd433bcd173c32e075955883596352ae2008e058f3708bf59`

```dockerfile
```

-	Layers:
	-	`sha256:e0f608cc55f27148653666f95063fa6d5f9a7604e4e0606f0d75d298532e0ee9`  
		Last Modified: Fri, 16 Jan 2026 00:53:32 GMT  
		Size: 46.7 KB (46736 bytes)  
		MIME: application/vnd.in-toto+json
