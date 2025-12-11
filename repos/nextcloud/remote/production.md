## `nextcloud:production`

```console
$ docker pull nextcloud@sha256:ef4b05678fc0a7fcced9ecc1faabadf0ef5f9c99996ff31a1c4ff333c544058f
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

### `nextcloud:production` - linux; amd64

```console
$ docker pull nextcloud@sha256:e16a7b2f4e494c2ab83eb0c23e5af7f89e9715db5ef9c78c71dae79e0479d1d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **482.4 MB (482409511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121bf01112587845531a11189a72037cf35b117697ec60d3e7a90d84528d5c83`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:39:06 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 08 Dec 2025 22:39:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 08 Dec 2025 22:39:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 08 Dec 2025 22:39:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 08 Dec 2025 22:39:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 08 Dec 2025 22:39:22 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 08 Dec 2025 22:39:22 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 08 Dec 2025 22:53:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Mon, 08 Dec 2025 22:53:34 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Mon, 08 Dec 2025 22:53:34 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Mon, 08 Dec 2025 22:53:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Dec 2025 22:53:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Dec 2025 22:53:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 08 Dec 2025 22:53:34 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 08 Dec 2025 22:53:34 GMT
ENV PHP_VERSION=8.3.28
# Mon, 08 Dec 2025 22:53:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.28.tar.xz.asc
# Mon, 08 Dec 2025 22:53:34 GMT
ENV PHP_SHA256=25e3860f30198a386242891c0bf9e2955931f7b666b96c3e3103d36a2a322326
# Mon, 08 Dec 2025 22:53:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 08 Dec 2025 22:53:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:56:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 08 Dec 2025 22:56:17 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:56:17 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 08 Dec 2025 22:56:17 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 08 Dec 2025 22:56:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 08 Dec 2025 22:56:17 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Dec 2025 22:56:17 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:56:17 GMT
WORKDIR /var/www/html
# Mon, 08 Dec 2025 22:56:17 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Dec 2025 22:56:17 GMT
CMD ["apache2-foreground"]
# Tue, 09 Dec 2025 00:19:56 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-7.q16-10-extra         rsync     ;     apt-get dist-clean;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Tue, 09 Dec 2025 00:22:03 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 09 Dec 2025 00:22:03 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 09 Dec 2025 00:22:03 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Tue, 09 Dec 2025 00:22:03 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.27;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.0;     pecl install memcached-3.4.0         --configureoptions 'enable-memcached-igbinary="yes"';     pecl install redis-6.3.0         --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"';         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -rt dpkg-query --search         | awk 'sub(":$", "", $1) { print $1 }'         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:22:03 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Tue, 09 Dec 2025 00:22:03 GMT
VOLUME [/var/www/html]
# Tue, 09 Dec 2025 00:22:04 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip # buildkit
# Tue, 09 Dec 2025 00:22:04 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Tue, 09 Dec 2025 00:22:04 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits # buildkit
# Tue, 09 Dec 2025 00:22:04 GMT
ENV NEXTCLOUD_VERSION=31.0.11
# Tue, 09 Dec 2025 00:22:47 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-31.0.11.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-31.0.11.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:22:47 GMT
COPY *.sh upgrade.exclude / # buildkit
# Tue, 09 Dec 2025 00:22:47 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Tue, 09 Dec 2025 00:22:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Dec 2025 00:22:47 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60df91c45d0a86e1db8d1d912fb5cf26d490f2284dac0daa5f35109768e26545`  
		Last Modified: Mon, 08 Dec 2025 22:42:47 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f8710b0f16836f0a18a496d19ba862ec3b1cea366c4521ef644d9b073f1524`  
		Last Modified: Mon, 08 Dec 2025 22:42:56 GMT  
		Size: 117.8 MB (117838586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e4542c4381529b61bface7c43a625307bba7d14bf252ab1b57a2f24cfb5b332`  
		Last Modified: Mon, 08 Dec 2025 22:42:47 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce7470ee1455546c25b2680a49cdb78d0d7c65d1e4170192fbad3e729813792`  
		Last Modified: Mon, 08 Dec 2025 22:56:36 GMT  
		Size: 4.2 MB (4224526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99cb708df8f05272a256d8e92d2096f7eab3290fb84bb6c7a502b916bf3ddcdf`  
		Last Modified: Mon, 08 Dec 2025 22:56:36 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d0d313218aba7dc3fc5855e6b355961ad12f0e396a34bae518c80238534dd3`  
		Last Modified: Mon, 08 Dec 2025 22:56:36 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33e61c85737cca7294530dcd669d76a12cee0dbd9d1f4d2c7c0237c1634273b`  
		Last Modified: Mon, 08 Dec 2025 22:56:37 GMT  
		Size: 12.8 MB (12770195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543828ab9fd42599e7a1c381e754d023c357c3bec8b88ff7ecc1adac437aaf64`  
		Last Modified: Mon, 08 Dec 2025 22:56:36 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ab8f1d104c541ba44266eee56e79b97f9c2c3c097e01dbbef481430d678b2cb`  
		Last Modified: Mon, 08 Dec 2025 22:56:37 GMT  
		Size: 11.7 MB (11713288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ce6266145199e14d29ffe22bb0795d38978130f9e08f29165d401acf30f89f`  
		Last Modified: Mon, 08 Dec 2025 22:56:36 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e16d68226cddedf8a1b4b217a45e36897d229d6b283ebf47b16e2b24836ad0bc`  
		Last Modified: Mon, 08 Dec 2025 22:56:36 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1c5c71ad84360684503dc8ceae651b6a1721ac66e4c236b410139ac78dbdc25`  
		Last Modified: Mon, 08 Dec 2025 22:56:36 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da081f25a1b30f03de3aa9ac768679d36bdec758603631177fe2dc4ac6195edb`  
		Last Modified: Mon, 08 Dec 2025 22:56:36 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d7819e25219b5f5148b16e8700c2f1415bc6da3c910a002fab34418c178ca7`  
		Last Modified: Tue, 09 Dec 2025 00:23:28 GMT  
		Size: 21.0 MB (20950124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cd164064a394474be2828edabe48b9a2705c2f165309541f51e8e6bb5f06dab`  
		Last Modified: Tue, 09 Dec 2025 00:23:26 GMT  
		Size: 36.8 MB (36811930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52bf861025c9bf68f6ddf403ed45137a0be2abef9d0267e9d508a17727bde5a9`  
		Last Modified: Tue, 09 Dec 2025 00:23:23 GMT  
		Size: 793.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2586bfa6aed809bf00865df0f709207109802f0b80aa4eb3a65ec208f4077ddb`  
		Last Modified: Tue, 09 Dec 2025 00:23:23 GMT  
		Size: 576.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e9dad1ebeae58e2a96f3303a71299052b00a5563fe1ad9cdbd4a3f4499dd7d`  
		Last Modified: Tue, 09 Dec 2025 00:23:23 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93fa265d03499f5959552b2bd3137dc0ae2f0f4d72349590e8fd1359bf34a1d`  
		Last Modified: Tue, 09 Dec 2025 00:24:15 GMT  
		Size: 248.3 MB (248310398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e28a769cff35a5b3692d0996302afb9dca071e381ec444ef8bcce93398d3b0`  
		Last Modified: Tue, 09 Dec 2025 00:23:23 GMT  
		Size: 4.0 KB (4047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff8b18e2a6a130a93bc21d53422160f35e216ff9931d5f4af7c38aca34eacc5`  
		Last Modified: Tue, 09 Dec 2025 00:23:23 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:production` - unknown; unknown

```console
$ docker pull nextcloud@sha256:5fa61a52ccb2452aadb85cbb4736e2936c5e39071813625b7c80f62c61588839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 KB (63413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83abb5f2930584ae63608783b19930fbd6cf4d89b8c571d11e2720681b57dc7f`

```dockerfile
```

-	Layers:
	-	`sha256:41852330e228b211c71319a1e4b7b94a606191cd24921be2d2ca07e404bd2256`  
		Last Modified: Tue, 09 Dec 2025 03:49:58 GMT  
		Size: 63.4 KB (63413 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:production` - linux; arm variant v5

```console
$ docker pull nextcloud@sha256:8b90c9a4ae665cfd937a5c502e474928ce747fd53a5142e446b1abbb55093c32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **453.6 MB (453584577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bc99ad29ec89dacb3f5d21c186c55aad8998ab154b0248c8525aa5213476451`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:35:47 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 08 Dec 2025 22:36:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 08 Dec 2025 22:36:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 08 Dec 2025 22:36:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 08 Dec 2025 22:36:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 08 Dec 2025 22:36:09 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 08 Dec 2025 22:36:09 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 08 Dec 2025 23:07:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Mon, 08 Dec 2025 23:07:15 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Mon, 08 Dec 2025 23:07:15 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Mon, 08 Dec 2025 23:07:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Dec 2025 23:07:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Dec 2025 23:07:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 08 Dec 2025 23:07:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 08 Dec 2025 23:07:15 GMT
ENV PHP_VERSION=8.3.28
# Mon, 08 Dec 2025 23:07:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.28.tar.xz.asc
# Mon, 08 Dec 2025 23:07:15 GMT
ENV PHP_SHA256=25e3860f30198a386242891c0bf9e2955931f7b666b96c3e3103d36a2a322326
# Mon, 08 Dec 2025 23:07:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 08 Dec 2025 23:07:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 23:10:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 08 Dec 2025 23:10:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 23:10:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 08 Dec 2025 23:10:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 08 Dec 2025 23:10:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 08 Dec 2025 23:10:24 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Dec 2025 23:10:24 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 23:10:24 GMT
WORKDIR /var/www/html
# Mon, 08 Dec 2025 23:10:24 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Dec 2025 23:10:24 GMT
CMD ["apache2-foreground"]
# Tue, 09 Dec 2025 01:26:36 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-7.q16-10-extra         rsync     ;     apt-get dist-clean;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Tue, 09 Dec 2025 01:29:54 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 09 Dec 2025 01:29:54 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 09 Dec 2025 01:29:54 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Tue, 09 Dec 2025 01:29:54 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.27;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.0;     pecl install memcached-3.4.0         --configureoptions 'enable-memcached-igbinary="yes"';     pecl install redis-6.3.0         --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"';         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -rt dpkg-query --search         | awk 'sub(":$", "", $1) { print $1 }'         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:29:54 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Tue, 09 Dec 2025 01:29:54 GMT
VOLUME [/var/www/html]
# Tue, 09 Dec 2025 01:29:55 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip # buildkit
# Tue, 09 Dec 2025 01:29:55 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Tue, 09 Dec 2025 01:29:55 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits # buildkit
# Tue, 09 Dec 2025 01:29:55 GMT
ENV NEXTCLOUD_VERSION=31.0.11
# Tue, 09 Dec 2025 01:30:54 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-31.0.11.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-31.0.11.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:30:54 GMT
COPY *.sh upgrade.exclude / # buildkit
# Tue, 09 Dec 2025 01:30:54 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Tue, 09 Dec 2025 01:30:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Dec 2025 01:30:54 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:d97bc71d0fa535127863fdab265dfddb07b3cda35b80de4dd2b9b67fe154c856`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 27.9 MB (27944187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435caa21eb7a92a952703c3f8c75f4c55a42454eca61e576bb048e4acdd0c61d`  
		Last Modified: Mon, 08 Dec 2025 22:40:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d7e20c5899cd32afa89fc93bc06a9ae97f2208b4811a1499ec42cb4ca3f239`  
		Last Modified: Mon, 08 Dec 2025 22:40:12 GMT  
		Size: 94.9 MB (94874317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d062cbcf654880d0305c9a6985c08013d60d9c644008ae3caa212738dd9ffc5`  
		Last Modified: Mon, 08 Dec 2025 22:40:06 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c4315882e4a7c083abb1758dd3a2dfd2921669a88324990c4e1e3ba4c1c740`  
		Last Modified: Mon, 08 Dec 2025 23:10:44 GMT  
		Size: 4.1 MB (4082057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c94a6b7f53129c8e4595f942be0774e0eee037d1464f7b94df784d43cdfa44c`  
		Last Modified: Mon, 08 Dec 2025 23:10:44 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eb11b3f73f496a615aca457b32e91b2d5754d4d429abe42e315cc6816743ecf`  
		Last Modified: Mon, 08 Dec 2025 23:10:43 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a19eb8210a3e9d158b06fb87def3014743a460257bedba1c53c8f005989b5fb6`  
		Last Modified: Mon, 08 Dec 2025 23:10:48 GMT  
		Size: 12.8 MB (12767652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b25c31a74d36fb3ef436e38577b62e56435e0d4fdfe2b9501f1e6844ac000d01`  
		Last Modified: Mon, 08 Dec 2025 23:10:43 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3e99d28e8c48680067c5fe73b1b6be53ab3026de9cc08235d5e090aff8f8f7`  
		Last Modified: Mon, 08 Dec 2025 23:10:44 GMT  
		Size: 10.6 MB (10597463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4432ce4269dc3aed57128d1bfadf7117c2c7b889083002c40c65e0779ae693e4`  
		Last Modified: Mon, 08 Dec 2025 23:10:44 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf434aa165ef5c99709285a0841634850fb1afa77f6fa495c9636a8df74101f`  
		Last Modified: Mon, 08 Dec 2025 23:10:43 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f322609af38a22e072f097ae5ad295b5e36700f87fb9807159a385bc9e597507`  
		Last Modified: Mon, 08 Dec 2025 23:10:43 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c18aaa93d22705dea1cc07e8b1999c796594e1af185dd8b920fef2d1974a9759`  
		Last Modified: Mon, 08 Dec 2025 23:10:44 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11acd3359aa7245afded073a17677427fe35aa46741f4f5aea425b4f94b10d0`  
		Last Modified: Tue, 09 Dec 2025 01:31:43 GMT  
		Size: 20.0 MB (20040889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7dddce8c9435df1601c7ca8f8fb215c51628e56eb647881d54e2459b14162b1`  
		Last Modified: Tue, 09 Dec 2025 01:31:43 GMT  
		Size: 35.0 MB (34957428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11a35fc7a32f1a848a4096ca075135fe90c1f8504007e343592799450a87c44d`  
		Last Modified: Tue, 09 Dec 2025 01:31:38 GMT  
		Size: 792.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df2ba88cc4cf598ae019c990cdb884ba908103e48d98fc2c5149a08038da6ea`  
		Last Modified: Tue, 09 Dec 2025 01:31:38 GMT  
		Size: 575.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5773345e00c23bd0368f760f4f1010bcc6b5c1775c90891f9716aa6ddb1459cb`  
		Last Modified: Tue, 09 Dec 2025 01:31:38 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3245c4e27bb249d6e9e2e870a28591ca1c02f62f1569174f317815f93e41d80e`  
		Last Modified: Tue, 09 Dec 2025 01:31:45 GMT  
		Size: 248.3 MB (248306620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66bc7fe2e9f473c3fb9165485af6d54c4e2f1373e005e40cc46d24193df88b4b`  
		Last Modified: Tue, 09 Dec 2025 01:31:39 GMT  
		Size: 4.0 KB (4047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee258b16cadee9c099a5c42040aac9b30f5baf2104ad77396069d3ca672560ce`  
		Last Modified: Tue, 09 Dec 2025 01:31:38 GMT  
		Size: 2.4 KB (2412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:production` - unknown; unknown

```console
$ docker pull nextcloud@sha256:23a7f2a1fca883adf160ae5bd300d47081ab38e39720b5975c27326d7afd946c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.6 KB (63597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92d0249b135dea6cf12cc8c764ba90c0508a42c3d0f63a69477655a1620095b5`

```dockerfile
```

-	Layers:
	-	`sha256:056d222204598672759203f127691ca39159ddd1caa63302cb27bed93bd79a12`  
		Last Modified: Tue, 09 Dec 2025 03:50:01 GMT  
		Size: 63.6 KB (63597 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:production` - linux; arm variant v7

```console
$ docker pull nextcloud@sha256:9e79b11a9e4be48162da99605b34868e7e0ba65d6e6de5b6f0ff50a25ff4f0af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **439.9 MB (439902681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbb33efcb3d2e1ead106fe5ff6e5230ad151b03a276ef781561225b85c4168b2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:12:14 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 08 Dec 2025 23:12:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 08 Dec 2025 23:12:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 08 Dec 2025 23:12:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 08 Dec 2025 23:12:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 08 Dec 2025 23:12:32 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 08 Dec 2025 23:12:32 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 08 Dec 2025 23:12:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Mon, 08 Dec 2025 23:12:39 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Mon, 08 Dec 2025 23:12:39 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Mon, 08 Dec 2025 23:12:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Dec 2025 23:12:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Dec 2025 23:12:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 08 Dec 2025 23:12:39 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 08 Dec 2025 23:12:39 GMT
ENV PHP_VERSION=8.3.28
# Mon, 08 Dec 2025 23:12:39 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.28.tar.xz.asc
# Mon, 08 Dec 2025 23:12:39 GMT
ENV PHP_SHA256=25e3860f30198a386242891c0bf9e2955931f7b666b96c3e3103d36a2a322326
# Mon, 08 Dec 2025 23:12:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 08 Dec 2025 23:12:50 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 23:15:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 08 Dec 2025 23:15:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 23:15:28 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 08 Dec 2025 23:15:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 08 Dec 2025 23:15:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 08 Dec 2025 23:15:28 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Dec 2025 23:15:28 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 23:15:28 GMT
WORKDIR /var/www/html
# Mon, 08 Dec 2025 23:15:28 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Dec 2025 23:15:28 GMT
CMD ["apache2-foreground"]
# Tue, 09 Dec 2025 01:47:02 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-7.q16-10-extra         rsync     ;     apt-get dist-clean;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Tue, 09 Dec 2025 01:50:03 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 09 Dec 2025 01:50:03 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 09 Dec 2025 01:50:03 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Tue, 09 Dec 2025 01:50:03 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.27;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.0;     pecl install memcached-3.4.0         --configureoptions 'enable-memcached-igbinary="yes"';     pecl install redis-6.3.0         --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"';         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -rt dpkg-query --search         | awk 'sub(":$", "", $1) { print $1 }'         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:50:03 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Tue, 09 Dec 2025 01:50:03 GMT
VOLUME [/var/www/html]
# Tue, 09 Dec 2025 01:50:03 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip # buildkit
# Tue, 09 Dec 2025 01:50:03 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Tue, 09 Dec 2025 01:50:04 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits # buildkit
# Tue, 09 Dec 2025 01:50:04 GMT
ENV NEXTCLOUD_VERSION=31.0.11
# Tue, 09 Dec 2025 01:51:01 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-31.0.11.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-31.0.11.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:51:01 GMT
COPY *.sh upgrade.exclude / # buildkit
# Tue, 09 Dec 2025 01:51:02 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Tue, 09 Dec 2025 01:51:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Dec 2025 01:51:02 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:cfc411ffeb71f696e2a89e33e91be9b70084d6c3383474344babe3a4a21eb843`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 26.2 MB (26210013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b777f680ea5ed6244de9922459aca5e8f721dd50afe3ad69bd160d32b03fed74`  
		Last Modified: Mon, 08 Dec 2025 23:15:55 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892beb557407f1ac713d96f814f3d44dc1f4b7577c30e3232053ccc0ecc1acfe`  
		Last Modified: Mon, 08 Dec 2025 23:16:01 GMT  
		Size: 86.2 MB (86246508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e34241676ecd248c3c604ff9ff8e3c42a09b306a317700fe1b02c144f79a28`  
		Last Modified: Mon, 08 Dec 2025 23:15:55 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae3fb9ca4fa496585289c07a64816f09c57ae2629a92f8925148a56e408597e`  
		Last Modified: Mon, 08 Dec 2025 23:15:56 GMT  
		Size: 3.8 MB (3752414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39bc52f4c6d03d2de94f2aa9db372c265d3d80df3430c29c3f82bbb6e08d0939`  
		Last Modified: Mon, 08 Dec 2025 23:15:55 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5521d93ca8953e3b2971412de188672c166ca9d93e56b2cbac405a9d351769`  
		Last Modified: Mon, 08 Dec 2025 23:15:56 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e236f7bb7fb4d00df90682ec06f4b237ae2adefcdced42a1a5a7fda8753c7b3d`  
		Last Modified: Mon, 08 Dec 2025 23:15:57 GMT  
		Size: 12.8 MB (12767793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc6eeabbbde0f4cf8be66d73f09608ebcac2a8e41ed202124bc8a0cd22e95a8`  
		Last Modified: Mon, 08 Dec 2025 23:15:56 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0548c2ee49539f86c5f116cd4f0f50c3b9eaac2a5f6bb1ecd8a3596a47ecec3e`  
		Last Modified: Mon, 08 Dec 2025 23:15:57 GMT  
		Size: 10.1 MB (10069913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3263787bde47d23cc53f47de8f560681087a55e9e28284702e77a64f055ec0dc`  
		Last Modified: Mon, 08 Dec 2025 23:15:56 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4da6e3a92cd906f34cb8f02d0fb40bff471e0d825cfad4e9e8cdc6dfa3eab37`  
		Last Modified: Mon, 08 Dec 2025 23:15:55 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001a9b8ff0f7c25a1c5e9a9bd32de2d1f381f35bd7ff0b60537a0410d5c7bfc0`  
		Last Modified: Mon, 08 Dec 2025 23:15:55 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bfa2ad1dd9fe7b67dcb31090ea75ddefb49570e62891cd44b295650829bb12`  
		Last Modified: Mon, 08 Dec 2025 23:15:55 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac05fa63b7cfaf499a71694f2852f9c5e5e5b96b0906d9d66c11bedee270b770`  
		Last Modified: Tue, 09 Dec 2025 01:51:47 GMT  
		Size: 18.0 MB (17978025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdda1898a32fd176b75188098e4e29722a40f21291fcbf2e8166088cdf8a22aa`  
		Last Modified: Tue, 09 Dec 2025 01:51:52 GMT  
		Size: 34.6 MB (34557118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4139f0244b4cad70c93bdc12015662b14df4657b98e137c9af26790d113bd1a0`  
		Last Modified: Tue, 09 Dec 2025 01:51:45 GMT  
		Size: 791.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f212d9c530f6180708256f5120c631082b4052b91cd61ac6e0ee5e5d4fe3580a`  
		Last Modified: Tue, 09 Dec 2025 01:51:46 GMT  
		Size: 571.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b7977e75b78bf830b0d3b5d3ea88c10b226bf01451f64b9517c6e27f4ff12ed`  
		Last Modified: Tue, 09 Dec 2025 01:51:45 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba2743fcfd43f4644d55f3dcc586dacee3941574feed4b03d5f098927a1ba46`  
		Last Modified: Tue, 09 Dec 2025 01:51:54 GMT  
		Size: 248.3 MB (248306939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd084e0f29ba965d840264eee6e887ae0d39678519f9edc0a7b4d6108c9dadf`  
		Last Modified: Tue, 09 Dec 2025 01:51:45 GMT  
		Size: 4.0 KB (4047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0c62c232866dd39217a745e6cfdc94770c72aee46853447130a21d3f01945b`  
		Last Modified: Tue, 09 Dec 2025 01:51:46 GMT  
		Size: 2.4 KB (2415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:production` - unknown; unknown

```console
$ docker pull nextcloud@sha256:fa5068c42bb3a9569770f5f1e67298b4bf872575e43a045f6852b41d03ee5a36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.6 KB (63596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d534bc8709b9dc2cbe5f999388515b4584af67f8e6b53cd731f725f73335f29d`

```dockerfile
```

-	Layers:
	-	`sha256:5b35073256c1d8f01ba3a1ddce06edfe4b19e521ea54db2b13e5a752b6870a34`  
		Last Modified: Tue, 09 Dec 2025 03:50:05 GMT  
		Size: 63.6 KB (63596 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:production` - linux; arm64 variant v8

```console
$ docker pull nextcloud@sha256:ade162dce91da4acf58283a8f522ba46bc975113f77e21e5c04ff8724e2eadca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **473.8 MB (473811777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19a6141fbea9998a697a203f801a501f57fe6892d70dfd9be46d55f73a6ae332`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:38:47 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 08 Dec 2025 22:39:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 08 Dec 2025 22:39:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 08 Dec 2025 22:39:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 08 Dec 2025 22:39:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 08 Dec 2025 22:39:03 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 08 Dec 2025 22:39:03 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 08 Dec 2025 22:39:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Mon, 08 Dec 2025 22:39:09 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Mon, 08 Dec 2025 22:39:10 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Mon, 08 Dec 2025 22:39:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Dec 2025 22:39:10 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Dec 2025 22:39:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 08 Dec 2025 22:39:10 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 08 Dec 2025 22:39:10 GMT
ENV PHP_VERSION=8.3.28
# Mon, 08 Dec 2025 22:39:10 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.28.tar.xz.asc
# Mon, 08 Dec 2025 22:39:10 GMT
ENV PHP_SHA256=25e3860f30198a386242891c0bf9e2955931f7b666b96c3e3103d36a2a322326
# Mon, 08 Dec 2025 22:55:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 08 Dec 2025 22:55:05 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:58:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 08 Dec 2025 22:58:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:58:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 08 Dec 2025 22:58:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 08 Dec 2025 22:58:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 08 Dec 2025 22:58:55 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Dec 2025 22:58:55 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:58:55 GMT
WORKDIR /var/www/html
# Mon, 08 Dec 2025 22:58:55 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Dec 2025 22:58:55 GMT
CMD ["apache2-foreground"]
# Tue, 09 Dec 2025 00:26:51 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-7.q16-10-extra         rsync     ;     apt-get dist-clean;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Tue, 09 Dec 2025 00:29:39 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 09 Dec 2025 00:29:39 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 09 Dec 2025 00:29:39 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Tue, 09 Dec 2025 00:29:39 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.27;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.0;     pecl install memcached-3.4.0         --configureoptions 'enable-memcached-igbinary="yes"';     pecl install redis-6.3.0         --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"';         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -rt dpkg-query --search         | awk 'sub(":$", "", $1) { print $1 }'         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:29:39 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Tue, 09 Dec 2025 00:29:39 GMT
VOLUME [/var/www/html]
# Tue, 09 Dec 2025 00:29:39 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip # buildkit
# Tue, 09 Dec 2025 00:29:39 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Tue, 09 Dec 2025 00:29:39 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits # buildkit
# Tue, 09 Dec 2025 00:29:39 GMT
ENV NEXTCLOUD_VERSION=31.0.11
# Tue, 09 Dec 2025 00:30:27 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-31.0.11.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-31.0.11.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:30:27 GMT
COPY *.sh upgrade.exclude / # buildkit
# Tue, 09 Dec 2025 00:30:27 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Tue, 09 Dec 2025 00:30:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Dec 2025 00:30:27 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db55d306a36fab75ed7d777aa9d49e7ff8f8d56b31b5ab58baec1feb7cd8ed6`  
		Last Modified: Mon, 08 Dec 2025 22:43:07 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f917fdde723bb9eeffdac3800d7c39abcd722fc080e2db6cd3a9bf35764fd07`  
		Last Modified: Mon, 08 Dec 2025 22:43:19 GMT  
		Size: 110.2 MB (110162673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d87be9b989aa856a793b7ddc0d880ba4ee5b7217f0d5ff25b541d7084ee566`  
		Last Modified: Mon, 08 Dec 2025 22:43:07 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3e9469eb184f28f35ced71fc9f3eebb692ac5c738982e61a304e2437aa67c75`  
		Last Modified: Mon, 08 Dec 2025 22:43:08 GMT  
		Size: 4.3 MB (4302241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a25a5c5337ccd28d55e0797d93bcfff4539dc555079083a227332c312cab9e`  
		Last Modified: Mon, 08 Dec 2025 22:43:08 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d0c8a8ae6e76d72b08c7db07500e8804384f40605d5a0eca0f37e82ea46be4`  
		Last Modified: Mon, 08 Dec 2025 22:43:08 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b08d1d3fb794d1a56c1a01ebf8500672da1f55c427e6924c85159d4c04946f6`  
		Last Modified: Mon, 08 Dec 2025 22:59:15 GMT  
		Size: 12.8 MB (12769808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62bf3154bb243ec992fe49167ecab6bba6488c6a14ba3eb2d4eea1827aed254f`  
		Last Modified: Mon, 08 Dec 2025 22:59:14 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811f0f2fa87c8d325b8946a90b3284c4f0651dd20374d9c7752bfb8944c754bd`  
		Last Modified: Mon, 08 Dec 2025 22:59:17 GMT  
		Size: 11.7 MB (11729803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b3de5a445d66564dd814bf63b4b3a350602ffec3fb2ef12f9a90ce59a31338`  
		Last Modified: Mon, 08 Dec 2025 22:59:14 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1bf44af048c36422962fbb5c0145c9d816af3edc1c624723f3d899896d0e82`  
		Last Modified: Mon, 08 Dec 2025 22:59:14 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df96ec1e97ee77dc168b947a2d0c87605cf360bdee0e30a11be1fdd26d28b15b`  
		Last Modified: Mon, 08 Dec 2025 22:59:14 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17722d9f32ff2de17cb65701c07e026e726f4a178298df205a25a148376db94a`  
		Last Modified: Mon, 08 Dec 2025 22:59:14 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f749734cd87532bbfb84518ba00ce33fdacdcefaa506ea959c3b4e07c223558`  
		Last Modified: Tue, 09 Dec 2025 00:31:13 GMT  
		Size: 19.7 MB (19669500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3046150b2173d931059d5ff33245686cc24dafc2793888192544fc15725d5bd9`  
		Last Modified: Tue, 09 Dec 2025 00:31:19 GMT  
		Size: 36.7 MB (36715418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b04ae5ffdcc8db15c8d78c7688562ee2def822f84ba8dcbdd71f101e057870`  
		Last Modified: Tue, 09 Dec 2025 00:31:12 GMT  
		Size: 790.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed33bccb049a284917de74d42cfecee424d802231064506370819d4a093b175`  
		Last Modified: Tue, 09 Dec 2025 00:31:12 GMT  
		Size: 576.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e38f3617e9fbb9d9d520132f5515419caf95f72693560043352e3d43671874`  
		Last Modified: Tue, 09 Dec 2025 00:31:12 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bfa5167176aad51071367ea44fabee7188ffc13592bf46a411986e7c3b370e`  
		Last Modified: Tue, 09 Dec 2025 00:31:18 GMT  
		Size: 248.3 MB (248309752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84fa74ddf68bf05e5ac9eae49457641e28b80129eaeb32774b908eee3bc9d244`  
		Last Modified: Tue, 09 Dec 2025 00:31:08 GMT  
		Size: 4.0 KB (4047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed293754772ddc88dc011197785996c2e0734bf6f2e50d239b6fd53caf436040`  
		Last Modified: Tue, 09 Dec 2025 00:31:12 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:production` - unknown; unknown

```console
$ docker pull nextcloud@sha256:aa958a9c418610c6e9db4b41360098f381ceacbd4b2e597ed7ec93915823e643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.7 KB (63664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51fe314dd59fc97946e7963c902155bae7e9b33dcae72835a18e12a02a3413b1`

```dockerfile
```

-	Layers:
	-	`sha256:657af14724835d0cf9f47ab93a12120e16e51e3f21658e03e3a485590bad0f45`  
		Last Modified: Tue, 09 Dec 2025 03:50:08 GMT  
		Size: 63.7 KB (63664 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:production` - linux; 386

```console
$ docker pull nextcloud@sha256:66c4483f6da81b9e82725828a99bd7fea6c01fc7cfbe3b786bec8134201a3c2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **483.3 MB (483306672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11dc382a164f3ce5c4083cbc135dd5f768a0e6898bd423d036718eb98bab3ee2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:35:44 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 08 Dec 2025 22:36:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 08 Dec 2025 22:36:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 08 Dec 2025 22:36:02 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 08 Dec 2025 22:36:02 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 08 Dec 2025 22:36:02 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 08 Dec 2025 22:36:02 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 08 Dec 2025 22:51:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Mon, 08 Dec 2025 22:51:35 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Mon, 08 Dec 2025 22:51:36 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Mon, 08 Dec 2025 22:51:36 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Dec 2025 22:51:36 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Dec 2025 22:51:36 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 08 Dec 2025 22:51:36 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 08 Dec 2025 22:51:36 GMT
ENV PHP_VERSION=8.3.28
# Mon, 08 Dec 2025 22:51:36 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.28.tar.xz.asc
# Mon, 08 Dec 2025 22:51:36 GMT
ENV PHP_SHA256=25e3860f30198a386242891c0bf9e2955931f7b666b96c3e3103d36a2a322326
# Mon, 08 Dec 2025 22:51:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 08 Dec 2025 22:51:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:54:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 08 Dec 2025 22:54:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:54:32 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 08 Dec 2025 22:54:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 08 Dec 2025 22:54:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 08 Dec 2025 22:54:32 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Dec 2025 22:54:32 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:54:32 GMT
WORKDIR /var/www/html
# Mon, 08 Dec 2025 22:54:32 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Dec 2025 22:54:32 GMT
CMD ["apache2-foreground"]
# Tue, 09 Dec 2025 00:14:43 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-7.q16-10-extra         rsync     ;     apt-get dist-clean;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Tue, 09 Dec 2025 00:17:26 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 09 Dec 2025 00:17:26 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 09 Dec 2025 00:17:26 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Tue, 09 Dec 2025 00:17:26 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.27;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.0;     pecl install memcached-3.4.0         --configureoptions 'enable-memcached-igbinary="yes"';     pecl install redis-6.3.0         --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"';         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -rt dpkg-query --search         | awk 'sub(":$", "", $1) { print $1 }'         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:17:26 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Tue, 09 Dec 2025 00:17:26 GMT
VOLUME [/var/www/html]
# Tue, 09 Dec 2025 00:17:27 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip # buildkit
# Tue, 09 Dec 2025 00:17:27 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Tue, 09 Dec 2025 00:17:27 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits # buildkit
# Tue, 09 Dec 2025 00:17:27 GMT
ENV NEXTCLOUD_VERSION=31.0.11
# Tue, 09 Dec 2025 00:18:19 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-31.0.11.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-31.0.11.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:18:19 GMT
COPY *.sh upgrade.exclude / # buildkit
# Tue, 09 Dec 2025 00:18:19 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Tue, 09 Dec 2025 00:18:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Dec 2025 00:18:19 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:2648c88d9207cd6090be83f4a97e2aa4080930987d8fb62195cc994194160e67`  
		Last Modified: Mon, 08 Dec 2025 22:17:03 GMT  
		Size: 31.3 MB (31293070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:154524b7be3749cfa72d3bbb2e8d095db97110da5060ceb7e4f1473e9e61790d`  
		Last Modified: Mon, 08 Dec 2025 22:39:57 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd631d2861c5c3a023b3ea0aaa64fa40fa6346b13d7b39ed45652f7e9987632`  
		Last Modified: Mon, 08 Dec 2025 22:40:08 GMT  
		Size: 116.1 MB (116138575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c90bac1aca55e1ea704979c288343f39f70510215a9cf6b945e40b6feec2ce06`  
		Last Modified: Mon, 08 Dec 2025 22:39:57 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53acc81ce731ef4a4d465cb8a583291202dee016a0120a19261fb3a5845b4e4c`  
		Last Modified: Mon, 08 Dec 2025 22:54:51 GMT  
		Size: 4.5 MB (4455999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548db23afcf0fb44a20278337a2d0ae10b3d88e365e609bc2359f06447deb7df`  
		Last Modified: Mon, 08 Dec 2025 22:54:51 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e74b5b7c6ce77596201b5299e77e44b14037ada823b0b47879fd5669475b9d1`  
		Last Modified: Mon, 08 Dec 2025 22:54:50 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d02c5939f502ede48e83231474b4a29f515d4a4973c4e8f006febf34142717`  
		Last Modified: Mon, 08 Dec 2025 22:54:52 GMT  
		Size: 12.8 MB (12769206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd529f9cf71080d89aab96bd9d156dc40abd62fbd99947e2bb1de01e2be85d6`  
		Last Modified: Mon, 08 Dec 2025 22:54:51 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c46361a7b7e61932b252074c133ca58c96a16c4035dc5bf14ccb8cb67484e2a0`  
		Last Modified: Mon, 08 Dec 2025 22:54:51 GMT  
		Size: 11.9 MB (11919408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d249c3ac14675eab656e934c20be7760d64b4ccf05edfa4b96eac2d35abd04c4`  
		Last Modified: Mon, 08 Dec 2025 22:54:50 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ccefa0e3b73973b55bbd0cd753631ba859cebe2c5577770522e47f8ed047b95`  
		Last Modified: Mon, 08 Dec 2025 22:54:51 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0016a305cac02834a5b6c83a6bdcff0f6efb48b78c56de27fdc2edae81bb309`  
		Last Modified: Mon, 08 Dec 2025 22:54:50 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb5d52512d83589b07bc92be254b256a860514a73c3a62881cba7284e6591c04`  
		Last Modified: Mon, 08 Dec 2025 22:54:51 GMT  
		Size: 888.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b94d1185bf44d415cd89811e2c9137110ce6f464faef6f5f90ba2c88979d4a3`  
		Last Modified: Tue, 09 Dec 2025 00:19:01 GMT  
		Size: 21.2 MB (21187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a478c3449daa12aa77376e8b383387d382bf0afd458d866e9a8270587cd8fbae`  
		Last Modified: Tue, 09 Dec 2025 00:19:01 GMT  
		Size: 37.2 MB (37220252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7360e64b1a37c3b4e0fbe4323ec9b986cf8c4e5f77bde38ba38f327a8df36209`  
		Last Modified: Tue, 09 Dec 2025 00:18:59 GMT  
		Size: 790.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8c2b424f512a5b77234c17e39f2cc81fcfa03eba593d6ceba7575f25e48463`  
		Last Modified: Tue, 09 Dec 2025 00:18:59 GMT  
		Size: 573.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d41e3b838901384d37999197acbb00fe1ec65496a2b829314756ce59b61ed0`  
		Last Modified: Tue, 09 Dec 2025 00:18:59 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75739ac17087501f8999a9ae715cc65bf7339024485163235d898e0660b129d1`  
		Last Modified: Tue, 09 Dec 2025 00:19:51 GMT  
		Size: 248.3 MB (248308757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1937eb4937a4f0a83ea30dfdfa8c57c42ee08676a6f2c36f0daaff47b304a0ad`  
		Last Modified: Tue, 09 Dec 2025 00:18:59 GMT  
		Size: 4.0 KB (4048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2539b468275b82feb8af0278808bf63597fb483f6dba9ee310e9133e53497062`  
		Last Modified: Tue, 09 Dec 2025 00:18:59 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:production` - unknown; unknown

```console
$ docker pull nextcloud@sha256:865642405b97618d0bfad82bbf6574498f10065858fad7225081693c590b676b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.3 KB (63341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d185de6428bf86dea37a598874da109186975a5c4f6ab087de3324c5dd502956`

```dockerfile
```

-	Layers:
	-	`sha256:39698197d60dc1cb02b4e989a6d60f5dc456ecd0cbd122e4e519da263509ef5c`  
		Last Modified: Tue, 09 Dec 2025 03:50:11 GMT  
		Size: 63.3 KB (63341 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:production` - linux; ppc64le

```console
$ docker pull nextcloud@sha256:0a0ef6683c91dc38bb133881644d17222bf4f5e25e7ee3edd6d0fd71a79b43b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **481.8 MB (481811824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:624ba230806ef8c282ff1eb9bf1579b92031c3575ec26f61178fce35d46cfe3f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 00:35:58 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 09 Dec 2025 00:36:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 09 Dec 2025 00:36:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:36:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 09 Dec 2025 00:36:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 09 Dec 2025 00:36:49 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 09 Dec 2025 00:36:49 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 09 Dec 2025 00:41:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 09 Dec 2025 00:41:46 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 09 Dec 2025 00:41:46 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 09 Dec 2025 00:41:46 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Dec 2025 00:41:46 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Dec 2025 00:41:46 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 09 Dec 2025 00:41:46 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 09 Dec 2025 00:41:46 GMT
ENV PHP_VERSION=8.3.28
# Tue, 09 Dec 2025 00:41:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.28.tar.xz.asc
# Tue, 09 Dec 2025 00:41:46 GMT
ENV PHP_SHA256=25e3860f30198a386242891c0bf9e2955931f7b666b96c3e3103d36a2a322326
# Tue, 09 Dec 2025 01:33:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 09 Dec 2025 01:33:29 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 01:37:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 09 Dec 2025 01:37:53 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 01:37:54 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 09 Dec 2025 01:37:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 09 Dec 2025 01:37:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 09 Dec 2025 01:37:55 GMT
STOPSIGNAL SIGWINCH
# Tue, 09 Dec 2025 01:37:56 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 01:37:57 GMT
WORKDIR /var/www/html
# Tue, 09 Dec 2025 01:37:57 GMT
EXPOSE map[80/tcp:{}]
# Tue, 09 Dec 2025 01:37:57 GMT
CMD ["apache2-foreground"]
# Tue, 09 Dec 2025 07:11:09 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-7.q16-10-extra         rsync     ;     apt-get dist-clean;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Tue, 09 Dec 2025 07:16:33 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 09 Dec 2025 07:16:33 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 09 Dec 2025 07:16:33 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Tue, 09 Dec 2025 07:16:33 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.27;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.0;     pecl install memcached-3.4.0         --configureoptions 'enable-memcached-igbinary="yes"';     pecl install redis-6.3.0         --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"';         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -rt dpkg-query --search         | awk 'sub(":$", "", $1) { print $1 }'         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 07:16:33 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Tue, 09 Dec 2025 07:16:33 GMT
VOLUME [/var/www/html]
# Tue, 09 Dec 2025 07:16:34 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip # buildkit
# Tue, 09 Dec 2025 07:16:34 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Tue, 09 Dec 2025 07:16:35 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits # buildkit
# Tue, 09 Dec 2025 07:16:35 GMT
ENV NEXTCLOUD_VERSION=31.0.11
# Tue, 09 Dec 2025 07:17:52 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-31.0.11.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-31.0.11.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 07:17:52 GMT
COPY *.sh upgrade.exclude / # buildkit
# Tue, 09 Dec 2025 07:17:53 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Tue, 09 Dec 2025 07:17:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Dec 2025 07:17:53 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e968a4c552b5d63962c849d9412a26339a7f50c4b8dee90079284c674840b8`  
		Last Modified: Tue, 09 Dec 2025 00:41:49 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d30124c487aeb9dddde3de1f906a208cb9bd0ae4a03d96c1622924a8622e568`  
		Last Modified: Tue, 09 Dec 2025 00:41:59 GMT  
		Size: 109.6 MB (109597911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd51466d9c6ea60e911a8b8d548a3ce159de7cc08df81891f748149917d7196`  
		Last Modified: Tue, 09 Dec 2025 00:41:49 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80cdd7fdbb4f498b6540140a43b62e20227e731c816b54e09c4166f8ff8637fb`  
		Last Modified: Tue, 09 Dec 2025 00:55:22 GMT  
		Size: 4.9 MB (4876044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8662dc1d5e5e4a3977cad81ad0301a23d9a7c393028d08dafd0f088f67701014`  
		Last Modified: Tue, 09 Dec 2025 00:47:34 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76e1761af690f425f7869d904bbd39508f379bcb057f9a915bfe9e5a5ffac93d`  
		Last Modified: Tue, 09 Dec 2025 00:47:35 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df386b317f873f24c954490897003afc0cd48be0e216913d2700314a12cf667d`  
		Last Modified: Tue, 09 Dec 2025 01:38:32 GMT  
		Size: 12.8 MB (12769347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beafe4867fe44992b5e9da2f31f9f093454e8333307cc103ad864f491e636990`  
		Last Modified: Tue, 09 Dec 2025 01:38:30 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b6641e9f23a6e17563d111f9c04952240793978906b18abbb29c3bc0320dc0b`  
		Last Modified: Tue, 09 Dec 2025 01:38:30 GMT  
		Size: 12.1 MB (12119745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3fb9d439a4c14195727e33767c51d42645f95622ee76b4f4beeac52113766c`  
		Last Modified: Tue, 09 Dec 2025 01:38:31 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:138a4d96d15997e661c28682350dfb784f9048e5d641a2cc94d921759c95881e`  
		Last Modified: Tue, 09 Dec 2025 01:38:30 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885efa4b912c17f55261ee92c49f5db0bfc72d1e54b25223a1e04b17b6a54a80`  
		Last Modified: Tue, 09 Dec 2025 01:38:30 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f1e3f3d801f7432dd31097d645a3fc6b24c89639455efcf4cc2c9b4e7e6aad0`  
		Last Modified: Tue, 09 Dec 2025 01:38:30 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340510d785ab9eb7914ceca6338ffb98cb4e5357a4c61bb584e8801b57266881`  
		Last Modified: Tue, 09 Dec 2025 07:19:36 GMT  
		Size: 22.0 MB (22017587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12eef0ee95928316a4dfbb437d1cd96bb556cae2f57c814a436e984167f4538f`  
		Last Modified: Tue, 09 Dec 2025 07:19:40 GMT  
		Size: 38.5 MB (38509124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7719e02f5349dedea797c2e29cef403cd8058c9303a9fa39c45be5cad29e45e3`  
		Last Modified: Tue, 09 Dec 2025 07:19:34 GMT  
		Size: 791.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbe43accd34867fdb42bd5a3a55a10450fbd00d270d3a327aadf90f6cc3ce93f`  
		Last Modified: Tue, 09 Dec 2025 07:19:33 GMT  
		Size: 576.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec6bf24f143a5c52ad1eef74295ad675ce777f619f0dfb294fcac6669c65f110`  
		Last Modified: Tue, 09 Dec 2025 07:19:33 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364dc49c2e0d9c6967b7ff8a622e4617d274d756469d54a70b1b078154aca92c`  
		Last Modified: Tue, 09 Dec 2025 07:19:42 GMT  
		Size: 248.3 MB (248311205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72a2ed1032df0b551f23991f3daa6ae1e6e1cb502c9c2d57f1a1cab0e6c7f2c8`  
		Last Modified: Tue, 09 Dec 2025 07:19:33 GMT  
		Size: 4.0 KB (4046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66cdab072389a201d28095f3ae6302a55fa6b76ee69dc53409b860cb121151cc`  
		Last Modified: Tue, 09 Dec 2025 07:19:34 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:production` - unknown; unknown

```console
$ docker pull nextcloud@sha256:89219ff977d28aca49bd4cc3eb92437b1633cb9f5f392411d544fbb2ec46f5e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 KB (63502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47ec30c3358ba6c62bd24efecc74adffb45125fc20e9409058089a83ef0ad0de`

```dockerfile
```

-	Layers:
	-	`sha256:d1dd1fe6dde51be6b961411fa9d3ecf45a4719a4afaf2a3c0ddbbeadde97d051`  
		Last Modified: Tue, 09 Dec 2025 09:49:37 GMT  
		Size: 63.5 KB (63502 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:production` - linux; riscv64

```console
$ docker pull nextcloud@sha256:d7634b0aa190d92db6a3a7c979a44456ff491d1987539c169618ed9e7ecee89d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **516.4 MB (516355410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08d3c50477695c9e7a529ffcba0dd79a317a360e0f97cddf9d9df9088689d0fd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 08:01:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 09 Dec 2025 08:03:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 09 Dec 2025 08:03:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 08:03:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 09 Dec 2025 08:03:04 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 09 Dec 2025 08:03:04 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 09 Dec 2025 08:03:04 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 09 Dec 2025 09:08:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 09 Dec 2025 09:08:25 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 09 Dec 2025 09:08:26 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 09 Dec 2025 09:08:26 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Dec 2025 09:08:26 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Dec 2025 09:08:26 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 09 Dec 2025 09:08:26 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 09 Dec 2025 09:08:26 GMT
ENV PHP_VERSION=8.3.28
# Tue, 09 Dec 2025 09:08:26 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.28.tar.xz.asc
# Tue, 09 Dec 2025 09:08:26 GMT
ENV PHP_SHA256=25e3860f30198a386242891c0bf9e2955931f7b666b96c3e3103d36a2a322326
# Wed, 10 Dec 2025 04:41:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 10 Dec 2025 04:41:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 10 Dec 2025 05:31:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 10 Dec 2025 05:31:30 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 10 Dec 2025 05:31:31 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 10 Dec 2025 05:31:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 10 Dec 2025 05:31:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 10 Dec 2025 05:31:32 GMT
STOPSIGNAL SIGWINCH
# Wed, 10 Dec 2025 05:31:32 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 10 Dec 2025 05:31:32 GMT
WORKDIR /var/www/html
# Wed, 10 Dec 2025 05:31:32 GMT
EXPOSE map[80/tcp:{}]
# Wed, 10 Dec 2025 05:31:32 GMT
CMD ["apache2-foreground"]
# Thu, 11 Dec 2025 16:01:17 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-7.q16-10-extra         rsync     ;     apt-get dist-clean;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Thu, 11 Dec 2025 16:28:46 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 11 Dec 2025 16:28:46 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 11 Dec 2025 16:28:46 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Thu, 11 Dec 2025 16:28:46 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.27;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.0;     pecl install memcached-3.4.0         --configureoptions 'enable-memcached-igbinary="yes"';     pecl install redis-6.3.0         --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"';         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -rt dpkg-query --search         | awk 'sub(":$", "", $1) { print $1 }'         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     apt-get dist-clean # buildkit
# Thu, 11 Dec 2025 16:28:46 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Thu, 11 Dec 2025 16:28:46 GMT
VOLUME [/var/www/html]
# Thu, 11 Dec 2025 16:28:47 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip # buildkit
# Thu, 11 Dec 2025 16:28:47 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Thu, 11 Dec 2025 16:28:48 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits # buildkit
# Thu, 11 Dec 2025 16:28:48 GMT
ENV NEXTCLOUD_VERSION=31.0.11
# Thu, 11 Dec 2025 16:33:06 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-31.0.11.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-31.0.11.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     apt-get dist-clean # buildkit
# Thu, 11 Dec 2025 16:33:08 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 11 Dec 2025 16:33:08 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Thu, 11 Dec 2025 16:33:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Dec 2025 16:33:08 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:c5d5473ebdeca51d00ece2f72c173b54f0060da7fbd8ab9486aaa33eee6a0d8c`  
		Last Modified: Tue, 09 Dec 2025 02:06:40 GMT  
		Size: 28.3 MB (28273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53d28a615a791c3859b4a1756ba700dc2c4f69377eb59f2058ba63d00e0869a`  
		Last Modified: Tue, 09 Dec 2025 09:06:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f8434337c0c50639ecc5b6dc774986d4e9420e3476e8e2468932a6a85632eb`  
		Last Modified: Tue, 09 Dec 2025 09:07:07 GMT  
		Size: 146.6 MB (146578870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e90ba410db15c99bcf35ee3bbf15863cbe2650207953ae1e912e0e6bf7fda0b`  
		Last Modified: Tue, 09 Dec 2025 09:06:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e74b4e149c4738e4a9c37f39d8a642897edbd74a4bf14ea4f27d976938c2b0f`  
		Last Modified: Tue, 09 Dec 2025 10:10:34 GMT  
		Size: 4.0 MB (4033863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:951f674e0bc56dc657de8b096a1cd8ed3c4b0cbb2de5d3a05d6e50989e9b86ab`  
		Last Modified: Tue, 09 Dec 2025 10:10:34 GMT  
		Size: 438.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c810195650744e7970d6163d3e7b56ea79e2877073201e867cf1c229807a8924`  
		Last Modified: Tue, 09 Dec 2025 10:10:34 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d8c89e9c8266f23df81e4917c667e6a55d083099a7cb2c5674a314c777849e`  
		Last Modified: Wed, 10 Dec 2025 05:34:48 GMT  
		Size: 12.8 MB (12784363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4b368a5452d55e873afc7d6d29e186a3441a8b16ae867912ee2fbbd39aaedd`  
		Last Modified: Wed, 10 Dec 2025 05:34:47 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17455589b1346603d5296e357363ff4b50a946e88b11a0e15560e36f06af1ef9`  
		Last Modified: Wed, 10 Dec 2025 05:34:48 GMT  
		Size: 11.2 MB (11247364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a08419333caa3163f67626f2f942fe0e89fc9d279a20f1671a491330b0d2d96`  
		Last Modified: Wed, 10 Dec 2025 05:34:47 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66ac980d464dc957c311aa0fa7a57b03d1742235889c9c26925c9d6ad2e94da4`  
		Last Modified: Wed, 10 Dec 2025 05:34:47 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb9abf6be49c309ff343e17d1bce8e68f7735df756f43d0a1466c5dca60aa8f`  
		Last Modified: Wed, 10 Dec 2025 05:34:47 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b5fbda606bc41ae64465512ef135803603b9d975fe3faeef94b2e950404e6f1`  
		Last Modified: Wed, 10 Dec 2025 05:34:47 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e17b1ea01c600abaeb5f2e363893ca8506b25a21d8a9d27d803de3d8cf28269f`  
		Last Modified: Thu, 11 Dec 2025 16:40:26 GMT  
		Size: 19.4 MB (19433405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a31a00add0a3c7b540c8d94efcc362185892afdf019b1146f3d97e4e038de78`  
		Last Modified: Thu, 11 Dec 2025 16:40:23 GMT  
		Size: 45.7 MB (45680284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98296de61f9641841de91c5fa87260e4f2b28d22a204672bda943125dcab9b9e`  
		Last Modified: Thu, 11 Dec 2025 16:40:23 GMT  
		Size: 793.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f4d9cf103b26315c6f20fc34331819d196d90eeb244c2d5a034d71cf0001d2`  
		Last Modified: Thu, 11 Dec 2025 16:40:20 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dc7f81bdd3a5ff5066f9684db9ea619e2f49fed4a62932d84e9120a5021841e`  
		Last Modified: Thu, 11 Dec 2025 16:40:20 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe078b86edfb49f6d7fb34393671226eb27f3dc9b92e675ae8ff648a26e640b`  
		Last Modified: Thu, 11 Dec 2025 16:40:30 GMT  
		Size: 248.3 MB (248310094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:481c9803029673f97eb1da48f7692aaee4efc01325dab26dc3819ff0fb6dbd8c`  
		Last Modified: Thu, 11 Dec 2025 16:40:20 GMT  
		Size: 4.0 KB (4047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0318e4c947c1c989515387566cf78f2ca5e6aa30931e02a513965f433ba4ded5`  
		Last Modified: Thu, 11 Dec 2025 16:40:20 GMT  
		Size: 2.4 KB (2417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:production` - unknown; unknown

```console
$ docker pull nextcloud@sha256:b5358b12a1c4ecbc271a7f54ffc8ff4d0c1bd11b2cdae6b9ec0755a3d973fd21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 KB (63503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59fdc5b70cbfaad6cec7d79926613b2378d13aca80bccf6f599836f17712db32`

```dockerfile
```

-	Layers:
	-	`sha256:5130230e25c07dd5b0c5bce568e12eb0ec9047a371596778b5ed5f120b017dad`  
		Last Modified: Thu, 11 Dec 2025 18:49:38 GMT  
		Size: 63.5 KB (63503 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:production` - linux; s390x

```console
$ docker pull nextcloud@sha256:a72db46026e673b233ce38315f314c82727263af789ef09ade72ed2d1b7ca175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **456.6 MB (456616972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cbb7319453787246d931e23ad004e8cb88c9cdce1bd6dc53862778783001fa4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:37:09 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 08 Dec 2025 22:37:23 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 08 Dec 2025 22:37:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 08 Dec 2025 22:37:23 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 08 Dec 2025 22:37:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 08 Dec 2025 22:37:24 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 08 Dec 2025 22:37:24 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 08 Dec 2025 22:37:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Mon, 08 Dec 2025 22:37:30 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Mon, 08 Dec 2025 22:37:30 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Mon, 08 Dec 2025 22:37:30 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Dec 2025 22:37:30 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Dec 2025 22:37:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 08 Dec 2025 22:37:30 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 08 Dec 2025 22:37:30 GMT
ENV PHP_VERSION=8.3.28
# Mon, 08 Dec 2025 22:37:30 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.28.tar.xz.asc
# Mon, 08 Dec 2025 22:37:30 GMT
ENV PHP_SHA256=25e3860f30198a386242891c0bf9e2955931f7b666b96c3e3103d36a2a322326
# Mon, 08 Dec 2025 23:17:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 08 Dec 2025 23:17:17 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 23:19:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 08 Dec 2025 23:19:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 23:19:38 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 08 Dec 2025 23:19:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 08 Dec 2025 23:19:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 08 Dec 2025 23:19:38 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Dec 2025 23:19:39 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 23:19:39 GMT
WORKDIR /var/www/html
# Mon, 08 Dec 2025 23:19:39 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Dec 2025 23:19:39 GMT
CMD ["apache2-foreground"]
# Tue, 09 Dec 2025 02:23:38 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-7.q16-10-extra         rsync     ;     apt-get dist-clean;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Tue, 09 Dec 2025 02:28:36 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 09 Dec 2025 02:28:36 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 09 Dec 2025 02:28:36 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Tue, 09 Dec 2025 02:28:36 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.27;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.0;     pecl install memcached-3.4.0         --configureoptions 'enable-memcached-igbinary="yes"';     pecl install redis-6.3.0         --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"';         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -rt dpkg-query --search         | awk 'sub(":$", "", $1) { print $1 }'         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 02:28:36 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Tue, 09 Dec 2025 02:28:36 GMT
VOLUME [/var/www/html]
# Tue, 09 Dec 2025 02:28:37 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip # buildkit
# Tue, 09 Dec 2025 02:28:37 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Tue, 09 Dec 2025 02:28:37 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits # buildkit
# Tue, 09 Dec 2025 02:28:37 GMT
ENV NEXTCLOUD_VERSION=31.0.11
# Tue, 09 Dec 2025 02:29:17 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-31.0.11.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-31.0.11.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 02:29:17 GMT
COPY *.sh upgrade.exclude / # buildkit
# Tue, 09 Dec 2025 02:29:18 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Tue, 09 Dec 2025 02:29:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Dec 2025 02:29:18 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:deacec5e6af82b258c59e95e3e86abeef36fad06b1d9ff2de33e88544ffb79ff`  
		Last Modified: Mon, 08 Dec 2025 22:20:52 GMT  
		Size: 29.8 MB (29834400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06325ac7d48e9543412848e1fa70a7cb9a579c86f688b2e2e9bd944346590fce`  
		Last Modified: Mon, 08 Dec 2025 22:41:03 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9a4b708d85d9501bc1929ab5cadbcf5d4c4bca40490257ace724e13a60fcbe4`  
		Last Modified: Mon, 08 Dec 2025 22:41:12 GMT  
		Size: 92.6 MB (92564698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e8d9f5a2f9a70ca9e903eb070a1168477352c4a37bbecf3ddf16c7afe71c0e`  
		Last Modified: Mon, 08 Dec 2025 22:41:03 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92dc5e34b4915edbdad5123bd5ae0d2c6a40e6471d283ad84545bd68e81f92a`  
		Last Modified: Mon, 08 Dec 2025 22:41:03 GMT  
		Size: 4.3 MB (4320856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5ee5f503eaad0fe4d32cdc7ac6d3f69c18294139afbeddfa165cfa252fda81`  
		Last Modified: Mon, 08 Dec 2025 22:41:03 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdeb52f4bcf5819a6d5437fcce1e1e4325546addfcf171571a63a6d4fcf38a2d`  
		Last Modified: Mon, 08 Dec 2025 22:41:03 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d54cd27f2dbadc5d04ec0756d2663d5a3d1526eb890efb948b0c4773a98966a`  
		Last Modified: Mon, 08 Dec 2025 23:20:03 GMT  
		Size: 12.8 MB (12768507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ce765fa4dfde18b09096c237dbbb6ba8b05a96ad5fc13d2cf6e63ca73a574a`  
		Last Modified: Mon, 08 Dec 2025 23:20:01 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8ce7ddf74a104be45192626f720a78a38b4b07f38aa9feb4c9e023b7d66031`  
		Last Modified: Mon, 08 Dec 2025 23:20:02 GMT  
		Size: 11.6 MB (11566453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb12c8a0f4ced6cc8e82ec3127a06e92266977dcc4f852ba8ba155b2d8998a0`  
		Last Modified: Mon, 08 Dec 2025 23:20:01 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f12de441af61860b987b76efd830daffcaabca7645deaa9211f7fe37d4cb932c`  
		Last Modified: Mon, 08 Dec 2025 23:20:01 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90da7b15f48264e2611f86bcff3a935289958cdc605d1dd53a4f31472dd0612b`  
		Last Modified: Mon, 08 Dec 2025 23:20:01 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b327abbc493408dabfa8841e0cf290ebda99298ef44a05d738985362cd2c97`  
		Last Modified: Mon, 08 Dec 2025 23:20:01 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d34aaeeed98df3b5d4d44d87caa7cf2af6b4586c479a1ef638df3d8ebdde7ad`  
		Last Modified: Tue, 09 Dec 2025 02:30:14 GMT  
		Size: 20.3 MB (20265652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ba3d926a957cd38ba298394adf30eb63903e790e7eeaacfd5c4809338c3a1b`  
		Last Modified: Tue, 09 Dec 2025 02:30:14 GMT  
		Size: 37.0 MB (36974504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb7a16c2fb3059391fa9e0c082dc0882e77deecfbc57581306da6f77e5595e6`  
		Last Modified: Tue, 09 Dec 2025 02:30:13 GMT  
		Size: 794.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4a59c6c1dcd341c08281e56461fe19c0c6c687d9c33599f5df6d080045a507`  
		Last Modified: Tue, 09 Dec 2025 02:30:12 GMT  
		Size: 574.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1d0899133d70c727764844cf65109d938adc1295574479859a60b20dad35ce`  
		Last Modified: Tue, 09 Dec 2025 02:30:12 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c87346ecddef07cd73c33224dcbb27315f67103c63843bc0e0ad5306d7a655b`  
		Last Modified: Tue, 09 Dec 2025 02:30:56 GMT  
		Size: 248.3 MB (248307948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b66444bf4fee04290b652aa48302874fe25f4c2e65b68a98539f5c07ef376dcf`  
		Last Modified: Tue, 09 Dec 2025 02:30:12 GMT  
		Size: 4.0 KB (4046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:887387e7d8dc77120e2ba1d2a130515e8738a140bbbcda41079c425782d65433`  
		Last Modified: Tue, 09 Dec 2025 02:30:12 GMT  
		Size: 2.4 KB (2412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:production` - unknown; unknown

```console
$ docker pull nextcloud@sha256:baa946ee15d0901a2d04671050064f7aebff15e2a1385be2ded20c4742fec390
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 KB (63404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:150f30a500b2fac62583389bb30418974403b3e55ff2aacf1adfe2ac76e62426`

```dockerfile
```

-	Layers:
	-	`sha256:d9b66dff2731bc92188e6421657288f7014e3e2982f06116f193fafe6ee09b07`  
		Last Modified: Tue, 09 Dec 2025 03:50:18 GMT  
		Size: 63.4 KB (63404 bytes)  
		MIME: application/vnd.in-toto+json
