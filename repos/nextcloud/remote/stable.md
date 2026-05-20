## `nextcloud:stable`

```console
$ docker pull nextcloud@sha256:750e44fa0800b40274304841c970734cb249247cf6dab122aad51c644d905f32
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

### `nextcloud:stable` - linux; amd64

```console
$ docker pull nextcloud@sha256:80241648313b230e3546a8552260c17034a68b59c28271aecbf5317065bd0fd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **504.3 MB (504268356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e6e388f95a8348d6387e10abcf05440f5682a76d27f5c71b6b03e9533a3a611`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:08:14 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 May 2026 23:08:30 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 May 2026 23:08:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 23:08:30 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 May 2026 23:08:30 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 May 2026 23:08:30 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 19 May 2026 23:08:30 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 19 May 2026 23:08:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 19 May 2026 23:08:35 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 19 May 2026 23:08:35 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 19 May 2026 23:08:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:08:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:08:35 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 May 2026 23:08:35 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 19 May 2026 23:08:35 GMT
ENV PHP_VERSION=8.4.21
# Tue, 19 May 2026 23:08:35 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.21.tar.xz.asc
# Tue, 19 May 2026 23:08:35 GMT
ENV PHP_SHA256=7cf5d8ab12c3b2016875bcfaec71bef1ef0b07bed6148f2c447577074431f984
# Tue, 19 May 2026 23:08:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 May 2026 23:08:44 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:11:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 May 2026 23:11:07 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:11:07 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 May 2026 23:11:08 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 May 2026 23:11:08 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 May 2026 23:11:08 GMT
STOPSIGNAL SIGWINCH
# Tue, 19 May 2026 23:11:08 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:11:08 GMT
WORKDIR /var/www/html
# Tue, 19 May 2026 23:11:08 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 May 2026 23:11:08 GMT
CMD ["apache2-foreground"]
# Wed, 20 May 2026 00:35:31 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-7.q16-10-extra         rsync     ;     apt-get dist-clean;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Wed, 20 May 2026 00:37:51 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 20 May 2026 00:37:51 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 20 May 2026 00:37:51 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Wed, 20 May 2026 00:37:51 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         liblz4-dev         libmagickwand-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-ftp-ssl;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.28;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.1;     pecl install --configureoptions 'enable-memcached-igbinary="yes"'         memcached-3.4.0;     pecl install --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"'         redis-6.3.0;         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -rt dpkg-query --search         | awk 'sub(":$", "", $1) { print $1 }'         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:37:51 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Wed, 20 May 2026 00:37:51 GMT
VOLUME [/var/www/html]
# Wed, 20 May 2026 00:37:52 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip # buildkit
# Wed, 20 May 2026 00:37:52 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Wed, 20 May 2026 00:37:52 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits # buildkit
# Wed, 20 May 2026 00:37:52 GMT
ENV NEXTCLOUD_VERSION=33.0.3
# Wed, 20 May 2026 00:38:29 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://github.com/nextcloud-releases/server/releases/download/v33.0.3/nextcloud-33.0.3.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://github.com/nextcloud-releases/server/releases/download/v33.0.3/nextcloud-33.0.3.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:38:29 GMT
COPY *.sh upgrade.exclude / # buildkit
# Wed, 20 May 2026 00:38:29 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Wed, 20 May 2026 00:38:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 00:38:29 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fce99d4331344d80bebd4205a62d52d373f28e66a9be8ddc507498b2dbbb9189`  
		Last Modified: Tue, 19 May 2026 23:11:28 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc59ba4d66f8f31d50e207bda3d579a0c75849d686f3007a1a4963742a6fa11`  
		Last Modified: Tue, 19 May 2026 23:11:32 GMT  
		Size: 117.8 MB (117840120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e51ede2f9858efeb6379f9a0028ceb58ecfabeb661d4d73f7c3bfb4bb64d6f`  
		Last Modified: Tue, 19 May 2026 23:11:27 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf3043eabd98c7ee097cb971f13623f4e15de793bcf99ebadc34c23810e0009`  
		Last Modified: Tue, 19 May 2026 23:11:28 GMT  
		Size: 4.2 MB (4227823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc54b6f8f718bbd605e7197bf00c3549bf41ada3ed2fdc2929be321f3502f36`  
		Last Modified: Tue, 19 May 2026 23:11:29 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf37826b67c5a88f89754a9e055e5a5907d45e6a2fdcff8e2b4b0ad8d81bcc9`  
		Last Modified: Tue, 19 May 2026 23:11:29 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd1f3ffd4aea81a6d0f1e9f9b1d761b1789af4ca603f98e3c1293bf3f8f955d`  
		Last Modified: Tue, 19 May 2026 23:11:30 GMT  
		Size: 13.9 MB (13885179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c816e7ae5934a413293b7f57731c7a7cb861fdaff16bc3f1fe7c55815693e6`  
		Last Modified: Tue, 19 May 2026 23:11:30 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757aa5ba80cf7c23c95bee433f4f64f72b736d77ced083e48a49de37bc7a2e74`  
		Last Modified: Tue, 19 May 2026 23:11:30 GMT  
		Size: 13.7 MB (13682587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d52d450d192d140bfe27640cbdc2e82fc325dda72d85481eb9b30b97828999d`  
		Last Modified: Tue, 19 May 2026 23:11:31 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f92ce4677f604d86a41edd764fb6dc3b8f711bd665abe0e1d3b37f0075ef9ce`  
		Last Modified: Tue, 19 May 2026 23:11:31 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8acfac93d9f745555e4601c7a3b8fc10a0868cbebaa6d044c6998d0006e40c`  
		Last Modified: Tue, 19 May 2026 23:11:32 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c39bc0a3849ee7f8edcc2c8b113285595614d3fd1240ae7af4f5ffbcd7dae00`  
		Last Modified: Tue, 19 May 2026 23:11:32 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42589658aceab1dab0ea85ef83ee339033d38e7600c01406601d20054e3b4f58`  
		Last Modified: Wed, 20 May 2026 00:38:56 GMT  
		Size: 21.0 MB (20951955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12bb0871ffc6e7a1d59df96e9a8b1107a78d218591989e4318d9170a8710afd4`  
		Last Modified: Wed, 20 May 2026 00:38:57 GMT  
		Size: 36.9 MB (36894812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad882d36d1f75e17681b1dac5d2af54fa34980f332fd18a43e7a378008b389fb`  
		Last Modified: Wed, 20 May 2026 00:38:56 GMT  
		Size: 790.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd34488d449cd3f818255c15087301705d02bb9ddf3173dd759ff0d0356889f5`  
		Last Modified: Wed, 20 May 2026 00:38:56 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7140515482d1025c8ca26e697ae4c3abacaa3e8ff6b5713590c5fe536b4ef4c`  
		Last Modified: Wed, 20 May 2026 00:38:57 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f6bdeda4b72acb98a5a2de7593686c8852f3797a7acdb4c80eb776f61d8d5a`  
		Last Modified: Wed, 20 May 2026 00:39:02 GMT  
		Size: 267.0 MB (266991897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9026759413156b9381a884148bb8e8aedd2d691e2eb0265d9fa912f87158cdb2`  
		Last Modified: Wed, 20 May 2026 00:38:58 GMT  
		Size: 4.1 KB (4135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe8b2215c550bcf1af109fb4180fa33461f216b9c978bb1ac8ff43e387e2637`  
		Last Modified: Wed, 20 May 2026 00:38:58 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:stable` - unknown; unknown

```console
$ docker pull nextcloud@sha256:76fda80935f61872c3801350e5fb7abc7cf321623268615aba364aaac77ba977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 KB (64187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dbfa16f55f2790b0f4a33bc82c7c1a7908b78ee32b96564c3992fd85c7dc756`

```dockerfile
```

-	Layers:
	-	`sha256:82ca43c193f647263969a79ea187d41158e8fac7a2cd6df9f0ff78c2dfae41bd`  
		Last Modified: Wed, 20 May 2026 00:38:55 GMT  
		Size: 64.2 KB (64187 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:stable` - linux; arm variant v5

```console
$ docker pull nextcloud@sha256:9070feaf49660056915d7ccd0af2e8fc630a0b086906a278e34bba9739d72b7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **475.2 MB (475221974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42ad856e863184ae37573476c1bcfa8dd510de8d9cb97b4426731662c7c94e40`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 22:59:59 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 May 2026 23:00:21 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 May 2026 23:00:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 23:00:21 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 May 2026 23:00:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 May 2026 23:00:21 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 19 May 2026 23:00:21 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 19 May 2026 23:08:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 19 May 2026 23:08:23 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 19 May 2026 23:08:23 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 19 May 2026 23:08:23 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:08:23 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:08:23 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 May 2026 23:08:23 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 19 May 2026 23:08:23 GMT
ENV PHP_VERSION=8.4.21
# Tue, 19 May 2026 23:08:23 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.21.tar.xz.asc
# Tue, 19 May 2026 23:08:23 GMT
ENV PHP_SHA256=7cf5d8ab12c3b2016875bcfaec71bef1ef0b07bed6148f2c447577074431f984
# Tue, 19 May 2026 23:08:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 May 2026 23:08:36 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:11:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 May 2026 23:11:43 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:11:44 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 May 2026 23:11:44 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 May 2026 23:11:44 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 May 2026 23:11:44 GMT
STOPSIGNAL SIGWINCH
# Tue, 19 May 2026 23:11:44 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:11:44 GMT
WORKDIR /var/www/html
# Tue, 19 May 2026 23:11:44 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 May 2026 23:11:44 GMT
CMD ["apache2-foreground"]
# Wed, 20 May 2026 01:27:00 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-7.q16-10-extra         rsync     ;     apt-get dist-clean;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Wed, 20 May 2026 01:30:13 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 20 May 2026 01:30:13 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 20 May 2026 01:30:13 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Wed, 20 May 2026 01:30:13 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         liblz4-dev         libmagickwand-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-ftp-ssl;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.28;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.1;     pecl install --configureoptions 'enable-memcached-igbinary="yes"'         memcached-3.4.0;     pecl install --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"'         redis-6.3.0;         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -rt dpkg-query --search         | awk 'sub(":$", "", $1) { print $1 }'         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     apt-get dist-clean # buildkit
# Wed, 20 May 2026 01:30:13 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Wed, 20 May 2026 01:30:13 GMT
VOLUME [/var/www/html]
# Wed, 20 May 2026 01:30:13 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip # buildkit
# Wed, 20 May 2026 01:30:13 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Wed, 20 May 2026 01:30:13 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits # buildkit
# Wed, 20 May 2026 01:30:13 GMT
ENV NEXTCLOUD_VERSION=33.0.3
# Wed, 20 May 2026 01:31:03 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://github.com/nextcloud-releases/server/releases/download/v33.0.3/nextcloud-33.0.3.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://github.com/nextcloud-releases/server/releases/download/v33.0.3/nextcloud-33.0.3.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     apt-get dist-clean # buildkit
# Wed, 20 May 2026 01:31:03 GMT
COPY *.sh upgrade.exclude / # buildkit
# Wed, 20 May 2026 01:31:03 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Wed, 20 May 2026 01:31:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 01:31:03 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:37dea77b903ae642229487445fa64e20dcf83d60070467f9c7581fb71a2dd8a8`  
		Last Modified: Tue, 19 May 2026 22:36:45 GMT  
		Size: 28.0 MB (27953869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0443c80029b8a2ca9379fe635ba383703251fabfa25d301492db5bf9ae30adb6`  
		Last Modified: Tue, 19 May 2026 23:04:01 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a0b4a242d5e9b39c774a9accd7434938c289e873d17d8b16b43898e0866ec1a`  
		Last Modified: Tue, 19 May 2026 23:04:04 GMT  
		Size: 94.9 MB (94886050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3be848e3f9b8c1aad313e3d24aa3e2fa9ac4bc37af999f1e009e99d22b8b2523`  
		Last Modified: Tue, 19 May 2026 23:04:01 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdeab1feed2bbe5e63c6f75eb00740b986d17a5b4b52eb1753da48c72f981935`  
		Last Modified: Tue, 19 May 2026 23:11:54 GMT  
		Size: 4.1 MB (4090125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3fd54a63fd692f75521a6386c596e36010721111bfaa2254285f093b8ec3451`  
		Last Modified: Tue, 19 May 2026 23:11:54 GMT  
		Size: 437.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c255d3eed0ca51e329075fa8b85689b2894283a43a5c229f99f4b27de70b3e`  
		Last Modified: Tue, 19 May 2026 23:11:54 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5916902b2cc44c871068b87a83b9eb838c3a2edd582766f8c3cb35f683f28cf9`  
		Last Modified: Tue, 19 May 2026 23:11:55 GMT  
		Size: 13.9 MB (13882569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ea62b0cc9ef2fdb903e1750632b92cf9dad62ca191d09b091643e086a5b2e9`  
		Last Modified: Tue, 19 May 2026 23:11:55 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a52e1347330216a00d68167c62a9143e51667465b0d58d0b831c8e52c55ff15`  
		Last Modified: Tue, 19 May 2026 23:11:56 GMT  
		Size: 12.3 MB (12295218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f546a12f9d71f4b7583210fdf2d22785282bd359dcc133fcd80d60599cbec263`  
		Last Modified: Tue, 19 May 2026 23:11:56 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e4ea6372789213391ad90ff0c138b41518befd5822ee2ef64f670735f33ece2`  
		Last Modified: Tue, 19 May 2026 23:11:56 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:895488a967fa1e2a57bbcbf6b92bca14a5e39cb9730d64fe979c0bff6aae78b4`  
		Last Modified: Tue, 19 May 2026 23:11:57 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ca0d370282acd3c074bdaa205aacf6162028ed56bd56f5d21c2fe4c3929035`  
		Last Modified: Tue, 19 May 2026 23:11:57 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5c214af55de2a5913f5f95fa50bf96b78dfe8903ae536b089ceb3cffb856977`  
		Last Modified: Wed, 20 May 2026 01:31:34 GMT  
		Size: 20.1 MB (20053194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1627132151b50b25bb8e1ae8a14f231892ee115c1018063a9088a957690258`  
		Last Modified: Wed, 20 May 2026 01:31:35 GMT  
		Size: 35.1 MB (35059177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf590fe21bbb53cba7bc2c7b8647714cccacb6818e012b8d6eeb08acc0a760dc`  
		Last Modified: Wed, 20 May 2026 01:31:33 GMT  
		Size: 793.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0929f2d6213b3a586110a720ff4462d608558200336f9e28b16d62b4189a7995`  
		Last Modified: Wed, 20 May 2026 01:31:33 GMT  
		Size: 573.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f1801b6751593b591eadb980c74b49a89ed4cf8a1c280dea46916d09324aa1`  
		Last Modified: Wed, 20 May 2026 01:31:35 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f79a6ae90ee82ba5102df3d1b2f67320f2a9623cc5fb1e650ca57dbd93b7df9`  
		Last Modified: Wed, 20 May 2026 01:31:40 GMT  
		Size: 267.0 MB (266987710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45894bbed1a0876c3324b27701426e722e8550a627615bd3887f0cee58d9994f`  
		Last Modified: Wed, 20 May 2026 01:31:36 GMT  
		Size: 4.1 KB (4134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79480515b2f48b241720e81edfd75437f269bac8958be44ff94d05cf3e2132a9`  
		Last Modified: Wed, 20 May 2026 01:31:36 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:stable` - unknown; unknown

```console
$ docker pull nextcloud@sha256:8898ee4579a9b75a69f520e42dab47a0f5577075ebf7bb8da9cfd73de621ca6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.4 KB (64388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50f9d199b9cb87b0fe392d3523c17ad03b1ddc084943ecde6813a72ffc0008a9`

```dockerfile
```

-	Layers:
	-	`sha256:cf1eed27530d26e6d6591bb670c25523d974ca37f08f6c7ca80f39ce4605428d`  
		Last Modified: Wed, 20 May 2026 01:31:33 GMT  
		Size: 64.4 KB (64388 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:stable` - linux; arm variant v7

```console
$ docker pull nextcloud@sha256:f9c75544e0c97bf72140e7d979bf7da42c680cfb78bdfd39e013ed2455d17f75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **461.5 MB (461457113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c17632f687f61da5e3875d2cd81fec3a08e8c05da75fad9d33baf873e7bade`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:08:33 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 May 2026 23:08:51 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 May 2026 23:08:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 23:08:51 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 May 2026 23:08:51 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 May 2026 23:08:51 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 19 May 2026 23:08:51 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 19 May 2026 23:12:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 19 May 2026 23:12:32 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 19 May 2026 23:12:33 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 19 May 2026 23:12:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:12:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:12:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 May 2026 23:12:33 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 19 May 2026 23:12:33 GMT
ENV PHP_VERSION=8.4.21
# Tue, 19 May 2026 23:12:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.21.tar.xz.asc
# Tue, 19 May 2026 23:12:33 GMT
ENV PHP_SHA256=7cf5d8ab12c3b2016875bcfaec71bef1ef0b07bed6148f2c447577074431f984
# Tue, 19 May 2026 23:12:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 May 2026 23:12:44 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:15:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 May 2026 23:15:42 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:15:42 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 May 2026 23:15:42 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 May 2026 23:15:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 May 2026 23:15:42 GMT
STOPSIGNAL SIGWINCH
# Tue, 19 May 2026 23:15:42 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:15:42 GMT
WORKDIR /var/www/html
# Tue, 19 May 2026 23:15:42 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 May 2026 23:15:42 GMT
CMD ["apache2-foreground"]
# Wed, 20 May 2026 01:44:56 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-7.q16-10-extra         rsync     ;     apt-get dist-clean;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Wed, 20 May 2026 01:47:53 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 20 May 2026 01:47:53 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 20 May 2026 01:47:53 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Wed, 20 May 2026 01:47:53 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         liblz4-dev         libmagickwand-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-ftp-ssl;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.28;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.1;     pecl install --configureoptions 'enable-memcached-igbinary="yes"'         memcached-3.4.0;     pecl install --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"'         redis-6.3.0;         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -rt dpkg-query --search         | awk 'sub(":$", "", $1) { print $1 }'         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     apt-get dist-clean # buildkit
# Wed, 20 May 2026 01:47:53 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Wed, 20 May 2026 01:47:53 GMT
VOLUME [/var/www/html]
# Wed, 20 May 2026 01:47:53 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip # buildkit
# Wed, 20 May 2026 01:47:53 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Wed, 20 May 2026 01:47:54 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits # buildkit
# Wed, 20 May 2026 01:47:54 GMT
ENV NEXTCLOUD_VERSION=33.0.3
# Wed, 20 May 2026 01:48:43 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://github.com/nextcloud-releases/server/releases/download/v33.0.3/nextcloud-33.0.3.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://github.com/nextcloud-releases/server/releases/download/v33.0.3/nextcloud-33.0.3.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     apt-get dist-clean # buildkit
# Wed, 20 May 2026 01:48:43 GMT
COPY *.sh upgrade.exclude / # buildkit
# Wed, 20 May 2026 01:48:43 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Wed, 20 May 2026 01:48:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 01:48:43 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:5748b9c3873e7576b494d1d035f8385ff895b681d07cacf1540b737c38c00c8d`  
		Last Modified: Tue, 19 May 2026 22:36:18 GMT  
		Size: 26.2 MB (26205831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80663a52f952db5086478df376d16a1453349952589840b8ca097442ab14cd0`  
		Last Modified: Tue, 19 May 2026 23:12:12 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:514301f83bdb225277579f50588e6829724d3bb4841a4bd9b395db2279fdc9b7`  
		Last Modified: Tue, 19 May 2026 23:12:16 GMT  
		Size: 86.3 MB (86255720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8d537acfbe5e0ed1f39bf4dbf62e0972f207c66efa0236c4923f803929cba7`  
		Last Modified: Tue, 19 May 2026 23:12:12 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df07ddf8bb7bf114b7393188a3a09a3dde42d34aab799196b495413863548597`  
		Last Modified: Tue, 19 May 2026 23:15:53 GMT  
		Size: 3.8 MB (3756727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e246333f81bf4c767d0117e2e9aed7af4e85fb1f22c421312d06a05c4354645e`  
		Last Modified: Tue, 19 May 2026 23:15:53 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c2005f567285d1cecc792ab9910462f4a040ee0a264ced9cf3c29583920237`  
		Last Modified: Tue, 19 May 2026 23:15:52 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8bde70dd28dd0da6f86d033d9ea84c96693767acbceff05ae22f10012d1314`  
		Last Modified: Tue, 19 May 2026 23:15:53 GMT  
		Size: 13.9 MB (13882835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f939df7e700eacb26c21da1ddaa9161610d10bff7aaaba1a3bd511444069a907`  
		Last Modified: Tue, 19 May 2026 23:15:54 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68fd0f1300ce98b8d40b7c62e0e78d6e11bc4874d6a9ee669697950cc215e387`  
		Last Modified: Tue, 19 May 2026 23:15:54 GMT  
		Size: 11.7 MB (11711476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be6cd7b7bb55ef1cc2bc74ec67d40ca3364199b7688f4d69a8efba03f53341c`  
		Last Modified: Tue, 19 May 2026 23:15:54 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4241455cb69f1cb7ecd0fd5dfed1ab1d96d3650add01233dcb5450ebdb0a6d26`  
		Last Modified: Tue, 19 May 2026 23:15:54 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bff8cfbbb2aaa89540687ae8f12490fd81e4bd3d79cbce1468cd2e0242a2203`  
		Last Modified: Tue, 19 May 2026 23:15:55 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec890c4e16ccb54c6732524f94d89e6b2605bac6b3f87cb543195667470be9c`  
		Last Modified: Tue, 19 May 2026 23:15:55 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90d853049d0844915bb95f71115d36c822187e19c8718da880a72e4f8aeb00d`  
		Last Modified: Wed, 20 May 2026 01:49:15 GMT  
		Size: 18.0 MB (17992257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab910dc72b8fb681a212541887f3b92f25771e288d0976329efe0fd731635f2b`  
		Last Modified: Wed, 20 May 2026 01:49:16 GMT  
		Size: 34.6 MB (34649899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2443b578f10c61a31e60f57d123f2d6cf7b97a08449c00fd9e3e46997d61575a`  
		Last Modified: Wed, 20 May 2026 01:49:14 GMT  
		Size: 795.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:511824cf7978b53adb4c60209cf8435598bcdea3d294404543103187c40c88a2`  
		Last Modified: Wed, 20 May 2026 01:49:14 GMT  
		Size: 575.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:623c229e55f05d099c1c619b1a899666287f92d518eca9636d87efd9897eee42`  
		Last Modified: Wed, 20 May 2026 01:49:15 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d1ac2611c874874adca27ab8828fd410bbeda0eeb269e4e96f8add971550e7`  
		Last Modified: Wed, 20 May 2026 01:49:21 GMT  
		Size: 267.0 MB (266988314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9c3b4100e0136c9558ae930f26695d43e0be0750b46909bc273e46ce8e8151`  
		Last Modified: Wed, 20 May 2026 01:49:16 GMT  
		Size: 4.1 KB (4135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ec67a77c85c74b47ba1cf6ab60e77402687ae9b9fdf47db573bf2a52a72e61`  
		Last Modified: Wed, 20 May 2026 01:49:17 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:stable` - unknown; unknown

```console
$ docker pull nextcloud@sha256:5d7396ce1e45c7a2ce15a356be90daac8b8066fa62c55b5790a754cbf3357e5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.4 KB (64388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4ed6e63ad4c989d4a0d738f5c92a5a739b1812d2d0ae681f715b73979fca713`

```dockerfile
```

-	Layers:
	-	`sha256:ad5a824742b732b27b6399b896ba10a033d7743f8b76bf93aa51d6e8f82e066f`  
		Last Modified: Wed, 20 May 2026 01:49:14 GMT  
		Size: 64.4 KB (64388 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:stable` - linux; arm64 variant v8

```console
$ docker pull nextcloud@sha256:c9cedbb30072e7bc1546550fb6a4ca6a21782297f50cca9b073f4abf60a4a9d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **495.3 MB (495313898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03d510d3a94af55fb25228a49d2b2de9d5b56c81dfd71ba68ce787c75bff1fc7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:08:21 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 May 2026 23:08:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 May 2026 23:08:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 23:08:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 May 2026 23:08:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 May 2026 23:08:38 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 19 May 2026 23:08:38 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 19 May 2026 23:08:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 19 May 2026 23:08:44 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 19 May 2026 23:08:44 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 19 May 2026 23:08:44 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:08:44 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:08:44 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 May 2026 23:08:44 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 19 May 2026 23:08:44 GMT
ENV PHP_VERSION=8.4.21
# Tue, 19 May 2026 23:08:44 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.21.tar.xz.asc
# Tue, 19 May 2026 23:08:44 GMT
ENV PHP_SHA256=7cf5d8ab12c3b2016875bcfaec71bef1ef0b07bed6148f2c447577074431f984
# Tue, 19 May 2026 23:08:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 May 2026 23:08:54 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:11:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 May 2026 23:11:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:11:58 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 May 2026 23:11:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 May 2026 23:11:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 May 2026 23:11:58 GMT
STOPSIGNAL SIGWINCH
# Tue, 19 May 2026 23:11:58 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:11:59 GMT
WORKDIR /var/www/html
# Tue, 19 May 2026 23:11:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 May 2026 23:11:59 GMT
CMD ["apache2-foreground"]
# Wed, 20 May 2026 00:38:51 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-7.q16-10-extra         rsync     ;     apt-get dist-clean;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Wed, 20 May 2026 00:41:32 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 20 May 2026 00:41:32 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 20 May 2026 00:41:32 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Wed, 20 May 2026 00:41:32 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         liblz4-dev         libmagickwand-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-ftp-ssl;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.28;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.1;     pecl install --configureoptions 'enable-memcached-igbinary="yes"'         memcached-3.4.0;     pecl install --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"'         redis-6.3.0;         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -rt dpkg-query --search         | awk 'sub(":$", "", $1) { print $1 }'         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:41:32 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Wed, 20 May 2026 00:41:32 GMT
VOLUME [/var/www/html]
# Wed, 20 May 2026 00:41:33 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip # buildkit
# Wed, 20 May 2026 00:41:33 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Wed, 20 May 2026 00:41:33 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits # buildkit
# Wed, 20 May 2026 00:41:33 GMT
ENV NEXTCLOUD_VERSION=33.0.3
# Wed, 20 May 2026 00:42:09 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://github.com/nextcloud-releases/server/releases/download/v33.0.3/nextcloud-33.0.3.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://github.com/nextcloud-releases/server/releases/download/v33.0.3/nextcloud-33.0.3.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:42:09 GMT
COPY *.sh upgrade.exclude / # buildkit
# Wed, 20 May 2026 00:42:09 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Wed, 20 May 2026 00:42:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 00:42:09 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d5b5a36dca1e5b92d670201258e6eb21a7f1ddbd7962e42b1cc4aebb659f26`  
		Last Modified: Tue, 19 May 2026 23:12:19 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536de9c4c15e9f78ca996ab669b28d7ceeebdba2a94fc0e98965d4747b5b6f64`  
		Last Modified: Tue, 19 May 2026 23:12:23 GMT  
		Size: 110.2 MB (110168949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dff06c75883e058ceef56d0ac4f3023b4583d14fdb0cc7597e453b2d98cbb51a`  
		Last Modified: Tue, 19 May 2026 23:12:20 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58ca39218606bec14214775e838112e7a29066907a8ba8e6008199b72dd667e`  
		Last Modified: Tue, 19 May 2026 23:12:20 GMT  
		Size: 4.3 MB (4307754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebb1a39d4228ed2f7eaf2d52d5b5793cec4eb9bcde4f9027f5c20098a682f7b`  
		Last Modified: Tue, 19 May 2026 23:12:21 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142446d5adc5ca005def03fd448488ceb2a15d746803a5e83ba2896629472090`  
		Last Modified: Tue, 19 May 2026 23:12:21 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6fb3609dbd200fe21a32e450678c298349a0bc3a595e72fc75054cd97750692`  
		Last Modified: Tue, 19 May 2026 23:12:22 GMT  
		Size: 13.9 MB (13884748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f451f954588713077eba1528bdf576c62e36a2786b650e529c1312ca0779bf2b`  
		Last Modified: Tue, 19 May 2026 23:12:22 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f705090045184ba1ef36096ed379d8f219ba2a946008580360786a82fc7539`  
		Last Modified: Tue, 19 May 2026 23:12:23 GMT  
		Size: 13.3 MB (13334110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e475e0a28744bb8ff4007ba3f03123179fb7d05a1afea86c6f4a3d1c6a72324d`  
		Last Modified: Tue, 19 May 2026 23:12:23 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c8573b313e05de7cd6480731b2b6c9716f3e3707b2672aba650d78ce8d7ab1`  
		Last Modified: Tue, 19 May 2026 23:12:23 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2551f678d737d85c42d9aca42274a61b9a52e3c76ccb5aaf38de697ec9f15d94`  
		Last Modified: Tue, 19 May 2026 23:12:24 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfba6557d00f1426caccc2d950544ea65a12a6893d3fafccee56e3a49fa53f98`  
		Last Modified: Tue, 19 May 2026 23:12:24 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3d49887ef2001105abaaa488556832f5a3e5d280bda3cd115b3d6c243f9fc6`  
		Last Modified: Wed, 20 May 2026 00:42:37 GMT  
		Size: 19.7 MB (19677006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1643fd5ac3f8fdf1e5b011369ca79af04e2c64ccf2004920610db663ff1c0175`  
		Last Modified: Wed, 20 May 2026 00:42:38 GMT  
		Size: 36.8 MB (36793777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd01bdc2753782b412251b4092c530a5ffd68df5ab8f49243927221da4b7579`  
		Last Modified: Wed, 20 May 2026 00:42:37 GMT  
		Size: 789.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c9a243baa228d9e5b28dd0ec4ac3e889e46698600785e9267d09cd32aa664be`  
		Last Modified: Wed, 20 May 2026 00:42:36 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3409275b4984e73921af041880f1064d8b4c43f6d9e60799337aa98bc7c184`  
		Last Modified: Wed, 20 May 2026 00:42:38 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc11344fbeed6b7a614cd67172a49e55f2d75c6b981d4ed98675fa02a27a8461`  
		Last Modified: Wed, 20 May 2026 00:42:43 GMT  
		Size: 267.0 MB (266991574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:246f8cdf1432282070b81eaf2fec5f0a1317f865c042bc21df9ef6f118699a49`  
		Last Modified: Wed, 20 May 2026 00:42:39 GMT  
		Size: 4.1 KB (4135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218f3c2e91f74041ea38891ae036fbe85f69de6007ffdda23cebdc5656a857fc`  
		Last Modified: Wed, 20 May 2026 00:42:39 GMT  
		Size: 2.4 KB (2415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:stable` - unknown; unknown

```console
$ docker pull nextcloud@sha256:e69a7154cccc1212fd203f6c1026c8436c8790c525bf041ce9667bd94a731930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.5 KB (64463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0077eec2e48545b3871bc79f557a6e7d3a40dd07c3d7ec7121e11f218d1958a`

```dockerfile
```

-	Layers:
	-	`sha256:d796c4b574f190aa2b86697f6d25698c893611423f3a2aace8dd9b4a65c2756e`  
		Last Modified: Wed, 20 May 2026 00:42:36 GMT  
		Size: 64.5 KB (64463 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:stable` - linux; 386

```console
$ docker pull nextcloud@sha256:014470625e9e87bad7556a02cc63f06516247cf32dbb40df8676c0bfc929151b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **505.3 MB (505286659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d082e12766b4b5d21484878679cd8a3c7aea325460659756ee4384e954255ba4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 22:59:34 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 May 2026 22:59:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 May 2026 22:59:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 22:59:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 May 2026 22:59:52 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 May 2026 22:59:52 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 19 May 2026 22:59:52 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 19 May 2026 23:03:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 19 May 2026 23:03:54 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 19 May 2026 23:03:54 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 19 May 2026 23:03:54 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:03:54 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:03:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 May 2026 23:03:54 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 19 May 2026 23:03:54 GMT
ENV PHP_VERSION=8.4.21
# Tue, 19 May 2026 23:03:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.21.tar.xz.asc
# Tue, 19 May 2026 23:03:54 GMT
ENV PHP_SHA256=7cf5d8ab12c3b2016875bcfaec71bef1ef0b07bed6148f2c447577074431f984
# Tue, 19 May 2026 23:04:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 May 2026 23:04:04 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:07:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 May 2026 23:07:05 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:07:06 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 May 2026 23:07:06 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 May 2026 23:07:06 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 May 2026 23:07:06 GMT
STOPSIGNAL SIGWINCH
# Tue, 19 May 2026 23:07:06 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:07:06 GMT
WORKDIR /var/www/html
# Tue, 19 May 2026 23:07:06 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 May 2026 23:07:06 GMT
CMD ["apache2-foreground"]
# Wed, 20 May 2026 02:55:43 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-7.q16-10-extra         rsync     ;     apt-get dist-clean;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Wed, 20 May 2026 02:58:20 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 20 May 2026 02:58:20 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 20 May 2026 02:58:20 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Wed, 20 May 2026 02:58:20 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         liblz4-dev         libmagickwand-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-ftp-ssl;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.28;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.1;     pecl install --configureoptions 'enable-memcached-igbinary="yes"'         memcached-3.4.0;     pecl install --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"'         redis-6.3.0;         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -rt dpkg-query --search         | awk 'sub(":$", "", $1) { print $1 }'         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     apt-get dist-clean # buildkit
# Wed, 20 May 2026 02:58:20 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Wed, 20 May 2026 02:58:20 GMT
VOLUME [/var/www/html]
# Wed, 20 May 2026 02:58:20 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip # buildkit
# Wed, 20 May 2026 02:58:20 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Wed, 20 May 2026 02:58:20 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits # buildkit
# Wed, 20 May 2026 02:58:20 GMT
ENV NEXTCLOUD_VERSION=33.0.3
# Wed, 20 May 2026 02:59:03 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://github.com/nextcloud-releases/server/releases/download/v33.0.3/nextcloud-33.0.3.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://github.com/nextcloud-releases/server/releases/download/v33.0.3/nextcloud-33.0.3.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     apt-get dist-clean # buildkit
# Wed, 20 May 2026 02:59:03 GMT
COPY *.sh upgrade.exclude / # buildkit
# Wed, 20 May 2026 02:59:03 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Wed, 20 May 2026 02:59:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 02:59:03 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:05ced853378773a7168a29bae2e2f29a846f0a56beb260fd47a509a5e4ac966a`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 31.3 MB (31295335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7ef0e2b9b8831424e569f81adb803e123836986b90b85facc1082aff0e10ef`  
		Last Modified: Tue, 19 May 2026 23:03:36 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f81e1fbd7e8c7666219c63cd3fd7c04b90c6d3ea9a4cc7081909983cec74d4f`  
		Last Modified: Tue, 19 May 2026 23:03:40 GMT  
		Size: 116.1 MB (116142338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4a1e4fab902fc8e38f6c1e11f37967937f31b067ad0dacf2e8143071267a78`  
		Last Modified: Tue, 19 May 2026 23:03:36 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f110b68dd5333b080598c4f99cfea0e4f2fb066a957dbafee578356c73d7a0a4`  
		Last Modified: Tue, 19 May 2026 23:07:16 GMT  
		Size: 4.5 MB (4459220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7807629de4dddfc71738872769e6e2fff272bc313d237a5895efcd5028e43c9`  
		Last Modified: Tue, 19 May 2026 23:07:16 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef3e0eee4f7b5a2d277ad1759243ad63ee2cdead09d47231593a865b903c187f`  
		Last Modified: Tue, 19 May 2026 23:07:16 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5855bec8215b60ceec7b88ab06366e12930281a465289587b21203cece65a1`  
		Last Modified: Tue, 19 May 2026 23:07:17 GMT  
		Size: 13.9 MB (13884144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1fd255a001652510f95ed1906742ea6ebfe7c19658485062ea36f09323e45d3`  
		Last Modified: Tue, 19 May 2026 23:07:17 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44576d934420317703b71545fd9bdde8b762a2f9c806701eba3a8e0b736245f2`  
		Last Modified: Tue, 19 May 2026 23:07:18 GMT  
		Size: 14.0 MB (13985036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a41208d9007a2684e316ab71688d3be38ad1909c0ace36bc298927a6257383e`  
		Last Modified: Tue, 19 May 2026 23:07:18 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d49c8d9ecac46abcf0b5048e75e8c5dec65af5c4d62c40a57c36d6f05221e5`  
		Last Modified: Tue, 19 May 2026 23:07:18 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2935f5923823861b3bd1c19c09d06a52bb3027831c8cfb7c420fc7e875ee1816`  
		Last Modified: Tue, 19 May 2026 23:07:18 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232c1d432d5c14625d1d0c0b7ed47bd10db79d8a6c5202b0ef339f9cf3790f50`  
		Last Modified: Tue, 19 May 2026 23:07:19 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fef31ada0c61ca02408e5fe16bf245a9a5fa718f7204dac861d66356ba78a54`  
		Last Modified: Wed, 20 May 2026 02:59:31 GMT  
		Size: 21.2 MB (21211877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fb67d59df60ee49b9655da2574a8855f1f0ee4ad83af7d255e3cb16c6b7c84`  
		Last Modified: Wed, 20 May 2026 02:59:31 GMT  
		Size: 37.3 MB (37304664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd000eb00d2b78e498ea07ad355898912a2d49e7630f4e0d2d5e5bdeb017ba41`  
		Last Modified: Wed, 20 May 2026 02:59:30 GMT  
		Size: 793.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa94730f236d28717e7351bb5373a56152d29939012f240b4e7aa5f2c852d108`  
		Last Modified: Wed, 20 May 2026 02:59:30 GMT  
		Size: 572.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94d1acc492c30237a35dc7628fb4b08cf00004455e546f91a0a4e1e6ac85b73`  
		Last Modified: Wed, 20 May 2026 02:59:31 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386fbb9bb840736856e2bc8bb97f66f6eab44d7b13f70272f226c02285dbcc81`  
		Last Modified: Wed, 20 May 2026 02:59:37 GMT  
		Size: 267.0 MB (266990002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c1d787c76b888ed994d51bcbeef91ffd63104521839a98246dfdd36e4617aa4`  
		Last Modified: Wed, 20 May 2026 02:59:32 GMT  
		Size: 4.1 KB (4135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88efac2cb8b43c63c4b94a6a3fd68bdf3e29b807e62b42cb689d7254301f3822`  
		Last Modified: Wed, 20 May 2026 02:59:33 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:stable` - unknown; unknown

```console
$ docker pull nextcloud@sha256:db77c821755c235e151836291a627d8f2fabf2efc2c67f889db348be02f30bcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.1 KB (64106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e9f67da3c677677dedc127de6f54f3e49ff605146599d5c7f14257624fd693`

```dockerfile
```

-	Layers:
	-	`sha256:39ec398150fbf1baaf02f08c75120198dbc96358ee3b2069fd44684bb49694d1`  
		Last Modified: Wed, 20 May 2026 02:59:30 GMT  
		Size: 64.1 KB (64106 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:stable` - linux; ppc64le

```console
$ docker pull nextcloud@sha256:452e34bc89b666db17c32ed8360c26f0f54766be6ffdbaef4c951cd93a3adc2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **503.7 MB (503669118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:703eb94c29c9d239eaf591590056fb414f7e0dc3ec539b97f9e4523d564ff011`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:25:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 May 2026 23:26:01 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 May 2026 23:26:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 23:26:01 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 May 2026 23:26:01 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 May 2026 23:26:01 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 19 May 2026 23:26:01 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 19 May 2026 23:29:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 19 May 2026 23:29:19 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 19 May 2026 23:29:19 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 19 May 2026 23:29:19 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:29:19 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:29:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 May 2026 23:29:19 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 19 May 2026 23:29:19 GMT
ENV PHP_VERSION=8.4.21
# Tue, 19 May 2026 23:29:19 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.21.tar.xz.asc
# Tue, 19 May 2026 23:29:19 GMT
ENV PHP_SHA256=7cf5d8ab12c3b2016875bcfaec71bef1ef0b07bed6148f2c447577074431f984
# Tue, 19 May 2026 23:50:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 May 2026 23:50:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:55:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 May 2026 23:55:08 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:55:08 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 May 2026 23:55:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 May 2026 23:55:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 May 2026 23:55:09 GMT
STOPSIGNAL SIGWINCH
# Tue, 19 May 2026 23:55:09 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:55:09 GMT
WORKDIR /var/www/html
# Tue, 19 May 2026 23:55:09 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 May 2026 23:55:09 GMT
CMD ["apache2-foreground"]
# Wed, 20 May 2026 08:22:45 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-7.q16-10-extra         rsync     ;     apt-get dist-clean;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Wed, 20 May 2026 08:27:48 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 20 May 2026 08:27:48 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 20 May 2026 08:27:48 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Wed, 20 May 2026 08:27:48 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         liblz4-dev         libmagickwand-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-ftp-ssl;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.28;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.1;     pecl install --configureoptions 'enable-memcached-igbinary="yes"'         memcached-3.4.0;     pecl install --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"'         redis-6.3.0;         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -rt dpkg-query --search         | awk 'sub(":$", "", $1) { print $1 }'         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     apt-get dist-clean # buildkit
# Wed, 20 May 2026 08:27:48 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Wed, 20 May 2026 08:27:48 GMT
VOLUME [/var/www/html]
# Wed, 20 May 2026 08:27:49 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip # buildkit
# Wed, 20 May 2026 08:27:49 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Wed, 20 May 2026 08:27:49 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits # buildkit
# Wed, 20 May 2026 08:27:49 GMT
ENV NEXTCLOUD_VERSION=33.0.3
# Wed, 20 May 2026 08:28:45 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://github.com/nextcloud-releases/server/releases/download/v33.0.3/nextcloud-33.0.3.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://github.com/nextcloud-releases/server/releases/download/v33.0.3/nextcloud-33.0.3.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     apt-get dist-clean # buildkit
# Wed, 20 May 2026 08:28:46 GMT
COPY *.sh upgrade.exclude / # buildkit
# Wed, 20 May 2026 08:28:46 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Wed, 20 May 2026 08:28:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 08:28:46 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:4dea3595b4b879a8f487420dc7e601b4fe79f2769fed7f891c99b52fea019c27`  
		Last Modified: Tue, 19 May 2026 22:37:58 GMT  
		Size: 33.6 MB (33600453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b651a003498bd50572d1189161afddcb900241800cb6d5d0bd7a8ce4500633e3`  
		Last Modified: Tue, 19 May 2026 23:31:25 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd8ec5f6bfff3150dfdb7f9ba59b5b8bbd45b012ab504b03e5eb22da1815753`  
		Last Modified: Tue, 19 May 2026 23:31:29 GMT  
		Size: 109.6 MB (109598335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c429ba9d511a0b12b2e87806d0728dcd1c7b4dcadf247dfaf38502d93c30cd5e`  
		Last Modified: Tue, 19 May 2026 23:31:25 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0111aa5024092ef6e35218a2a5c87fabbd8071beebd70c36829523f28c0d71b2`  
		Last Modified: Tue, 19 May 2026 23:34:38 GMT  
		Size: 4.9 MB (4883387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73bd5ecf3703d3e85307529fda185e272f3b0c333f01de176345c03f9489ac78`  
		Last Modified: Tue, 19 May 2026 23:34:38 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89aa5d27bd8a219cd7f3cc53de0c430d125200a13be2bd7468c706ac1923bcc7`  
		Last Modified: Tue, 19 May 2026 23:34:38 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b832b98d28c4265bc674a61814ff3f37d771c7cd82daef8bccbc5e62b92590cc`  
		Last Modified: Tue, 19 May 2026 23:55:32 GMT  
		Size: 13.9 MB (13884231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0684242f06e6f3246f72cbf4b45d566d49ce1e298d40f4542c1bd6d9a7f2dc27`  
		Last Modified: Tue, 19 May 2026 23:55:31 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e017cfece40e398ade025b52760fbd76eef85f634ab4d741f135ecf563f89b41`  
		Last Modified: Tue, 19 May 2026 23:55:32 GMT  
		Size: 14.1 MB (14090791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818347d4ac11626ea1d9c390539e9769b0cbfd5c3a9518558eda127e510c8292`  
		Last Modified: Tue, 19 May 2026 23:55:31 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc7908419be88f32e37cf0bef05b786db1958deb1a359af14bf8a6841f0ef08`  
		Last Modified: Tue, 19 May 2026 23:55:32 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b47881d2425d854df90a03061525176160b28d667aee55eced80646dfe4b154`  
		Last Modified: Tue, 19 May 2026 23:55:32 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72bd71a193a350ecf0cc3a4f31317c08eac09678c5475713b1ba0e8c2b85b890`  
		Last Modified: Tue, 19 May 2026 23:55:33 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a31dabe150550a5091f83f3e642554f7c9020940e8aeb4762cd4131300db0a`  
		Last Modified: Wed, 20 May 2026 08:29:31 GMT  
		Size: 22.0 MB (22024050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43fafb2863f7bab454acc4cb16bb56fecd71d91b5a20f4ab9ef998a7285ddb99`  
		Last Modified: Wed, 20 May 2026 08:29:32 GMT  
		Size: 38.6 MB (38582495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8648c945b9d95432d68aa5a9448ad411ba65ce9a7bb891c2bafd1924e34964`  
		Last Modified: Wed, 20 May 2026 08:29:30 GMT  
		Size: 795.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90f4a52e763bd92c755cfac7ab33259c499e2daab50fe9cc0dfeb9613b6c83d`  
		Last Modified: Wed, 20 May 2026 08:29:31 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32a312e1575dc5de1c006627fce2d15c8c0dfa479775cc31b9484106d0041bc`  
		Last Modified: Wed, 20 May 2026 08:29:32 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea392adf09d3411964562cfb211f7d607639ce286c2bc09bd985ed222f8c984`  
		Last Modified: Wed, 20 May 2026 08:29:38 GMT  
		Size: 267.0 MB (266991318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cac278c0b61a40fb11e0478de8ee1b2cc548be58a817b5f7e313ab2313cb0d7`  
		Last Modified: Wed, 20 May 2026 08:29:33 GMT  
		Size: 4.1 KB (4134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:130c025efaa3d3aba2a76ade6ab4e4b10671c562a8d78b67e83ee7148a8916c1`  
		Last Modified: Wed, 20 May 2026 08:29:33 GMT  
		Size: 2.4 KB (2412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:stable` - unknown; unknown

```console
$ docker pull nextcloud@sha256:0648602654c21f5f94cf6e56ab8f1b7d1e823293e495d8ad3b348e3c7ac0c15b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.3 KB (64290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07ab6521909a5ba98827579821a4fcbbe9efb316fcf174e0811f5370f3dcb1ff`

```dockerfile
```

-	Layers:
	-	`sha256:f72d364f70e7aa2014eae4c9b4c831515a86d00497274e7218bb51140ae02786`  
		Last Modified: Wed, 20 May 2026 08:29:30 GMT  
		Size: 64.3 KB (64290 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:stable` - linux; riscv64

```console
$ docker pull nextcloud@sha256:222f52c3066b18b15f2532595f4842d6cf0b28cd5a68bc02c70ec0b335d62b8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.1 MB (538092921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5e3d7e008f38f30120f4ce3654a0e76ff3fd3c3e434898136853d756c056f21`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 21:54:02 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 09 May 2026 21:56:04 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 09 May 2026 21:56:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Sat, 09 May 2026 21:56:04 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 09 May 2026 21:56:04 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 09 May 2026 21:56:04 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 09 May 2026 21:56:04 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 09 May 2026 23:01:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Sat, 09 May 2026 23:01:52 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Sat, 09 May 2026 23:01:53 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Sat, 09 May 2026 23:01:53 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 09 May 2026 23:01:53 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 09 May 2026 23:01:53 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 09 May 2026 23:01:53 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Sat, 09 May 2026 23:01:53 GMT
ENV PHP_VERSION=8.4.21
# Sat, 09 May 2026 23:01:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.21.tar.xz.asc
# Sat, 09 May 2026 23:01:53 GMT
ENV PHP_SHA256=7cf5d8ab12c3b2016875bcfaec71bef1ef0b07bed6148f2c447577074431f984
# Sun, 10 May 2026 03:06:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sun, 10 May 2026 03:06:01 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sun, 10 May 2026 04:00:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sun, 10 May 2026 04:00:17 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sun, 10 May 2026 04:00:18 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sun, 10 May 2026 04:00:18 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sun, 10 May 2026 04:00:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sun, 10 May 2026 04:00:18 GMT
STOPSIGNAL SIGWINCH
# Sun, 10 May 2026 04:00:19 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Sun, 10 May 2026 04:00:19 GMT
WORKDIR /var/www/html
# Sun, 10 May 2026 04:00:19 GMT
EXPOSE map[80/tcp:{}]
# Sun, 10 May 2026 04:00:19 GMT
CMD ["apache2-foreground"]
# Tue, 12 May 2026 12:33:40 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-7.q16-10-extra         rsync     ;     apt-get dist-clean;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Tue, 12 May 2026 13:03:06 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 12 May 2026 13:03:06 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 12 May 2026 13:03:06 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Tue, 12 May 2026 13:03:06 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         liblz4-dev         libmagickwand-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-ftp-ssl;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.28;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.1;     pecl install --configureoptions 'enable-memcached-igbinary="yes"'         memcached-3.4.0;     pecl install --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"'         redis-6.3.0;         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -rt dpkg-query --search         | awk 'sub(":$", "", $1) { print $1 }'         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     apt-get dist-clean # buildkit
# Tue, 12 May 2026 13:03:07 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Tue, 12 May 2026 13:03:07 GMT
VOLUME [/var/www/html]
# Tue, 12 May 2026 13:03:08 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip # buildkit
# Tue, 12 May 2026 13:03:08 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Tue, 12 May 2026 13:03:08 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits # buildkit
# Tue, 12 May 2026 13:03:08 GMT
ENV NEXTCLOUD_VERSION=33.0.3
# Tue, 12 May 2026 13:07:30 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://github.com/nextcloud-releases/server/releases/download/v33.0.3/nextcloud-33.0.3.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://github.com/nextcloud-releases/server/releases/download/v33.0.3/nextcloud-33.0.3.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     apt-get dist-clean # buildkit
# Tue, 12 May 2026 13:07:32 GMT
COPY *.sh upgrade.exclude / # buildkit
# Tue, 12 May 2026 13:07:32 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Tue, 12 May 2026 13:07:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 May 2026 13:07:32 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:1e9edef871271ebe58c5a713c7c062e88ff414be0976a2c7baf0aba83823c954`  
		Last Modified: Fri, 08 May 2026 20:38:39 GMT  
		Size: 28.3 MB (28280232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a851920f3b2b9f32390e534dcffd1a0f98fdc6aa8d5199bfd378e81a327288ff`  
		Last Modified: Sat, 09 May 2026 22:59:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0821c675bc014f36787754eae800bec2700775366123fdb7b93402865c4af1`  
		Last Modified: Sat, 09 May 2026 23:00:25 GMT  
		Size: 146.6 MB (146579482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757b3119d655d94203c15aecf1cc2d93402f4523740a2527b967e186d7693c42`  
		Last Modified: Sat, 09 May 2026 22:59:56 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40fef68a865e77649624e332fc135889fa3e311fd92fbd55efb9283eaf669560`  
		Last Modified: Sun, 10 May 2026 00:03:23 GMT  
		Size: 4.0 MB (4031575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b336a94a4c9567b8427e54f2733c24a8a5678559cf7b51711a20ec3f8d801d63`  
		Last Modified: Sun, 10 May 2026 00:03:21 GMT  
		Size: 437.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110b6e8491a8e810371841937507898364acf2bcba097426fe8b034aea28f887`  
		Last Modified: Sun, 10 May 2026 00:03:21 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad14a7cd9f525f145d8b68bc568a45c7f8eed62f31450e37a0979b423f58004`  
		Last Modified: Sun, 10 May 2026 04:03:28 GMT  
		Size: 13.9 MB (13891753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f633ff895c52cea1d7e23f223dd2169dceb2ead861cb4fa93f3860a0f6f42a`  
		Last Modified: Sun, 10 May 2026 04:03:24 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92db3100a06dbc49cd00dc24ced28077a601f0dd17edaefd2ffb52aa9dbac2c8`  
		Last Modified: Sun, 10 May 2026 04:03:28 GMT  
		Size: 13.1 MB (13101555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd089c8865d458928236f3d1942e8c49508f51b272e349cc22374ea1c4693b53`  
		Last Modified: Sun, 10 May 2026 04:03:24 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06867bb7db06feddf5516c50b44d2c2eb8f61c2f1f1614ca2d747135554590a2`  
		Last Modified: Sun, 10 May 2026 04:03:26 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf66af8612a9f071b4f7eb21a871b3557bb8d207e3886c7ea064c21b286bc0c`  
		Last Modified: Sun, 10 May 2026 04:03:26 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d72b6fdbd97c9f4a0691d7888582e0fabc2e030a6b3af0607a1fb05721c0769`  
		Last Modified: Sun, 10 May 2026 04:03:28 GMT  
		Size: 896.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3edea6aa893192185a725d60c1e713e7da64112f61d91e3fcc070e1a8290d592`  
		Last Modified: Tue, 12 May 2026 13:14:11 GMT  
		Size: 19.5 MB (19451175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d134d4b6aa5516ae0ed74a214516a5cdf92c2a2f8f727cd7002b201915baaf77`  
		Last Modified: Tue, 12 May 2026 13:14:19 GMT  
		Size: 45.8 MB (45751864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20fc5453f3ffc3ed19215f1c7be6139ab49465556ae1d2c6d5caa84b3e92ce22`  
		Last Modified: Tue, 12 May 2026 13:14:03 GMT  
		Size: 804.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad95c6043d9af24bc322e62abaedafaf51de0a4e632851e6e5fcf78eb846ab79`  
		Last Modified: Tue, 12 May 2026 13:14:03 GMT  
		Size: 600.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9bbce2c79e7432ed81896038f46781943c741dc06623db851551214e0295ef`  
		Last Modified: Tue, 12 May 2026 13:14:05 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4811dd883aee0cd0977e63e45f336fb66c22a95acd3718af5ce418acac27725`  
		Last Modified: Tue, 12 May 2026 13:14:53 GMT  
		Size: 267.0 MB (266991154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f3e27b434169a5a87aee7f4fc506fbde9c948bbd4b0ee3406015f798fef5ee`  
		Last Modified: Tue, 12 May 2026 13:14:07 GMT  
		Size: 4.1 KB (4136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:498167e4c59994557b8ffebacb5f328d4c5b9e1f2828933687af8866d9f101d6`  
		Last Modified: Tue, 12 May 2026 13:14:10 GMT  
		Size: 2.4 KB (2420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:stable` - unknown; unknown

```console
$ docker pull nextcloud@sha256:fdb36079379a0ae6e5d0314c4000610165d9bbe366e378e7c7a8fc938d1d7ee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.3 KB (64290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:225369adc2a030797d2c7553698606cecba7038e6f8ef91d53f38096cfd79164`

```dockerfile
```

-	Layers:
	-	`sha256:09b728765b928c0a99d72fe48676c4934308f6f36a30278624dfb6d90257a7f1`  
		Last Modified: Tue, 12 May 2026 13:14:02 GMT  
		Size: 64.3 KB (64290 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:stable` - linux; s390x

```console
$ docker pull nextcloud@sha256:a9e96a88c1eeec43a289e48ea4859b2e60ae4c627940ea353a034056c9def83b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **478.4 MB (478400184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89dc0a15a19fa8a8d0c472cfcda09ca12ec07f4ccf050dc08383bc76192f4aea`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:02:02 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 May 2026 23:02:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 May 2026 23:02:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 23:02:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 May 2026 23:02:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 May 2026 23:02:17 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 19 May 2026 23:02:17 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 19 May 2026 23:15:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 19 May 2026 23:15:45 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 19 May 2026 23:15:45 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 19 May 2026 23:15:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:15:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:15:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 May 2026 23:15:45 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 19 May 2026 23:15:45 GMT
ENV PHP_VERSION=8.4.21
# Tue, 19 May 2026 23:15:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.21.tar.xz.asc
# Tue, 19 May 2026 23:15:45 GMT
ENV PHP_SHA256=7cf5d8ab12c3b2016875bcfaec71bef1ef0b07bed6148f2c447577074431f984
# Tue, 19 May 2026 23:15:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 May 2026 23:15:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:20:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 May 2026 23:20:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:20:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 May 2026 23:20:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 May 2026 23:20:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 May 2026 23:20:15 GMT
STOPSIGNAL SIGWINCH
# Tue, 19 May 2026 23:20:15 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:20:15 GMT
WORKDIR /var/www/html
# Tue, 19 May 2026 23:20:15 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 May 2026 23:20:15 GMT
CMD ["apache2-foreground"]
# Wed, 20 May 2026 02:30:44 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-7.q16-10-extra         rsync     ;     apt-get dist-clean;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Wed, 20 May 2026 02:33:18 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 20 May 2026 02:33:18 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 20 May 2026 02:33:18 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Wed, 20 May 2026 02:33:18 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         liblz4-dev         libmagickwand-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-ftp-ssl;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.28;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.1;     pecl install --configureoptions 'enable-memcached-igbinary="yes"'         memcached-3.4.0;     pecl install --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"'         redis-6.3.0;         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -rt dpkg-query --search         | awk 'sub(":$", "", $1) { print $1 }'         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     apt-get dist-clean # buildkit
# Wed, 20 May 2026 02:33:18 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Wed, 20 May 2026 02:33:18 GMT
VOLUME [/var/www/html]
# Wed, 20 May 2026 02:33:18 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip # buildkit
# Wed, 20 May 2026 02:33:18 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Wed, 20 May 2026 02:33:18 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits # buildkit
# Wed, 20 May 2026 02:33:18 GMT
ENV NEXTCLOUD_VERSION=33.0.3
# Wed, 20 May 2026 02:33:54 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://github.com/nextcloud-releases/server/releases/download/v33.0.3/nextcloud-33.0.3.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://github.com/nextcloud-releases/server/releases/download/v33.0.3/nextcloud-33.0.3.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     apt-get dist-clean # buildkit
# Wed, 20 May 2026 02:33:54 GMT
COPY *.sh upgrade.exclude / # buildkit
# Wed, 20 May 2026 02:33:54 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Wed, 20 May 2026 02:33:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 02:33:54 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:3a7bf300ab749fc8aaa5ec872160f889b9f1fd11db31bb5e8fe4d9ec131347b0`  
		Last Modified: Tue, 19 May 2026 22:36:59 GMT  
		Size: 29.8 MB (29845924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1087ace6d8a95de6d5ba6626cddbda1ecb704acfedcab9fc24bbddaeebaa5b09`  
		Last Modified: Tue, 19 May 2026 23:06:06 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:513d8548dfe51b95cc99361a5b774bcb84552bc0e57dcd5972f102b817050b1e`  
		Last Modified: Tue, 19 May 2026 23:06:08 GMT  
		Size: 92.6 MB (92572581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:368b4298afa76b8d0d3fe67adad21cd322ad1fbe8cafe7a6fc389402a64f720c`  
		Last Modified: Tue, 19 May 2026 23:06:06 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69802b23e76e35fbdb804fc768929bb7d0d9730c1794074087914838e039dfb1`  
		Last Modified: Tue, 19 May 2026 23:20:33 GMT  
		Size: 4.3 MB (4331254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf14ea595e215f29b109496dcba14ac0984ae8902bfa7af6f9b156c5e218e59b`  
		Last Modified: Tue, 19 May 2026 23:20:33 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33986b7717407e319d3f2841bc991f0b444cff0b2b8bda61be7f014154d2484c`  
		Last Modified: Tue, 19 May 2026 23:20:33 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90dd1bb006d4fa2ea4d386e4128baf591fc08e19c231dfa8e5d185f380dca614`  
		Last Modified: Tue, 19 May 2026 23:20:33 GMT  
		Size: 13.9 MB (13883468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4562bfda7be6e3ce7f03c6c857f903469a262444401732867dca5443f21038d0`  
		Last Modified: Tue, 19 May 2026 23:20:34 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c6117bb68dabc9db1f86809e1fb835e09db5db4adb1a611c728052e79ee424`  
		Last Modified: Tue, 19 May 2026 23:20:34 GMT  
		Size: 13.4 MB (13447813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae748546640b4e239e2d7fe2d5b223daba33faa30c905df2b95f4f970bd4402`  
		Last Modified: Tue, 19 May 2026 23:20:35 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80741973cd9dc49165a0743446985e0dc3011a88b18b0040ba7472451cd999e1`  
		Last Modified: Tue, 19 May 2026 23:20:35 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089bd7034fca1399f94b7df5b5efa272e0da65a3b4dce908ac3a8d012db3b536`  
		Last Modified: Tue, 19 May 2026 23:20:35 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d11fb92a10bccc78327eec98081d653627591d93fb43c9fc6a0ddb55674beccc`  
		Last Modified: Tue, 19 May 2026 23:20:36 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab95fa154aaf347d9db76885f1a453760c75e714edab2c74e80cf6a69da93080`  
		Last Modified: Wed, 20 May 2026 02:34:34 GMT  
		Size: 20.3 MB (20266730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fbbd7156832d18990240d5c3622298a739a36d8b42b177c2e947c397f168500`  
		Last Modified: Wed, 20 May 2026 02:34:34 GMT  
		Size: 37.0 MB (37049517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffab168651a2ac23974c289847d49e2a85a6759d5e4fc3769f00569e818b5a9e`  
		Last Modified: Wed, 20 May 2026 02:34:33 GMT  
		Size: 790.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:244389f39b125955ec21493688a79da713a1b47af2a8aaaf698ec8c95289cf03`  
		Last Modified: Wed, 20 May 2026 02:34:34 GMT  
		Size: 576.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1c830cd8c17bbe9378c4a79919d65e417025b7b2dcf79d609cf1c594a9f7da7`  
		Last Modified: Wed, 20 May 2026 02:34:34 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab906e78fb0da5346476832083a1f7e195c4e64ed08c67ddedb722eb0ed60241`  
		Last Modified: Wed, 20 May 2026 02:34:44 GMT  
		Size: 267.0 MB (266988829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170d39e1b70e1cd196553bb481ed499ec350d622787ecfc4df39637140c8c702`  
		Last Modified: Wed, 20 May 2026 02:34:35 GMT  
		Size: 4.1 KB (4136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ae83b1979208040b4ccc503a9b8e73487c983427f56fa2e303c2026fac4b41`  
		Last Modified: Wed, 20 May 2026 02:34:35 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:stable` - unknown; unknown

```console
$ docker pull nextcloud@sha256:25e31749d58ccbff02b8799ec9334b27212f9e307ce1211299b20598b9fc035f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 KB (64179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:509d806e9dc6c3f293626aea43616325ce2e13450046c711785f9ffa629a901a`

```dockerfile
```

-	Layers:
	-	`sha256:e6d66d2421c4c4d8b801ca1ccf5569861d800587dd3208d292e020849f12333f`  
		Last Modified: Wed, 20 May 2026 02:34:33 GMT  
		Size: 64.2 KB (64179 bytes)  
		MIME: application/vnd.in-toto+json
