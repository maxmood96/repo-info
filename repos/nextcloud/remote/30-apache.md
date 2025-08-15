## `nextcloud:30-apache`

```console
$ docker pull nextcloud@sha256:572ceaa0bffaa739dbb2146fa12ce6ee92e098f8fe1cc22420b72f4636c45887
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; s390x
	-	unknown; unknown

### `nextcloud:30-apache` - linux; amd64

```console
$ docker pull nextcloud@sha256:db3ca95ec48b1f1fb04b5658d1b5f7ed1c55cf210504f3d46f2d9273eee4cc16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **445.1 MB (445118812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bef8ce7bb0144dfc9fbba7c1384d17d2752ef6d99876138db92ea97e87bb673`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 08 Aug 2025 00:02:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 08 Aug 2025 00:02:22 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 Aug 2025 00:02:22 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_VERSION=8.3.24
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.24.tar.xz.asc
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_SHA256=388ee5fd111097e97bae439bff46aec4ea27f816d3f0c2cb5490a41410d44251
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 Aug 2025 00:02:22 GMT
STOPSIGNAL SIGWINCH
# Fri, 08 Aug 2025 00:02:22 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
WORKDIR /var/www/html
# Fri, 08 Aug 2025 00:02:22 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 Aug 2025 00:02:22 GMT
CMD ["apache2-foreground"]
# Thu, 14 Aug 2025 19:55:08 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-7.q16-10-extra         rsync     ;     apt-get dist-clean;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Thu, 14 Aug 2025 19:55:08 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 14 Aug 2025 19:55:08 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 14 Aug 2025 19:55:08 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Thu, 14 Aug 2025 19:55:08 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.26;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.0;     pecl install memcached-3.3.0         --configureoptions 'enable-memcached-igbinary="yes"';     pecl install redis-6.2.0         --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"';         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -rt dpkg-query --search         | awk 'sub(":$", "", $1) { print $1 }'         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     apt-get dist-clean # buildkit
# Thu, 14 Aug 2025 19:55:08 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Thu, 14 Aug 2025 19:55:08 GMT
VOLUME [/var/www/html]
# Thu, 14 Aug 2025 19:55:08 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip # buildkit
# Thu, 14 Aug 2025 19:55:08 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Thu, 14 Aug 2025 19:55:08 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits # buildkit
# Thu, 14 Aug 2025 19:55:08 GMT
ENV NEXTCLOUD_VERSION=30.0.14
# Thu, 14 Aug 2025 19:55:08 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-30.0.14.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-30.0.14.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     apt-get dist-clean # buildkit
# Thu, 14 Aug 2025 19:55:08 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 14 Aug 2025 19:55:08 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Thu, 14 Aug 2025 19:55:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 14 Aug 2025 19:55:08 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c25be817a835befbaadae87f2657fb370d8f40e4de6e20a0ce7fe0f95622d8`  
		Last Modified: Tue, 12 Aug 2025 22:31:58 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d62849df79d526cc0a1282079fd7b146f6159355501ac5c240de2f2cc968da`  
		Last Modified: Tue, 12 Aug 2025 22:32:09 GMT  
		Size: 117.8 MB (117833903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7993c6bc3e951174f25d2629444ab1d9ca97b3fd7f8410f197871f2acdfcc3a`  
		Last Modified: Tue, 12 Aug 2025 22:31:58 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137dc0a479929522b5b7a2827062f41052afd3735ac6f58813170cfccaff472b`  
		Last Modified: Tue, 12 Aug 2025 22:32:02 GMT  
		Size: 4.2 MB (4223744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d532d439586535777e3b31586c3eb6d43f391d25553986f0dc45c47d74b798a2`  
		Last Modified: Tue, 12 Aug 2025 22:31:46 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b50763a9795d3970c96be8d4d9fe42a2d5cd96b20b2a8368cecd8d3a2b6b3b`  
		Last Modified: Tue, 12 Aug 2025 22:31:46 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d6cbbfe929632203aa490a2abbe9a471c7572a5b18ab68459f31316d301f8e`  
		Last Modified: Tue, 12 Aug 2025 22:31:48 GMT  
		Size: 12.7 MB (12744237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb5014c9f8c78aba5c13fb3cbb0a66b015cbb71719d99d731dc6c658f6237973`  
		Last Modified: Tue, 12 Aug 2025 22:31:48 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db246118ae8ce97a78a65fc8032f0b58931a376c94827f8377bfcaedcbcddd91`  
		Last Modified: Tue, 12 Aug 2025 22:31:49 GMT  
		Size: 11.7 MB (11703521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad01fb378d8c4de83ab1c238f7c778e103a2d54b3c2f7357cca245baef3808c`  
		Last Modified: Tue, 12 Aug 2025 22:31:48 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e712978f1ff3138383f1d79b4e8d8e969985eec2b56d90d6a5535bd7c5c8ee2`  
		Last Modified: Tue, 12 Aug 2025 22:32:02 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e955ff1e785d3fe6e44f0f74232266fd480f00b1e48ab6a1331110ce887be64`  
		Last Modified: Tue, 12 Aug 2025 22:31:49 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c37b3e3497bc43f74d062f7ba33e6be6278f464328c1047c9bc164843789ff`  
		Last Modified: Tue, 12 Aug 2025 22:31:50 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed1328ed17f4045223e8249fe03d2c758f77c6bca27ad87a1490bc5b81649f0`  
		Last Modified: Thu, 14 Aug 2025 22:53:30 GMT  
		Size: 21.0 MB (20951460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa337135a978d3cb83f7eb6d666b44126a11af15f6ba70062005772e9ef667bb`  
		Last Modified: Thu, 14 Aug 2025 22:53:32 GMT  
		Size: 37.0 MB (36961216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00fa59a4ac9c24b38eb1ed55ecd1eab7b5b97672e3862716027f3447d545f1b7`  
		Last Modified: Thu, 14 Aug 2025 22:53:28 GMT  
		Size: 790.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c340785829f7e52045c1c65d273f55c68cc27e5070f3b16efeb2fa82560c9227`  
		Last Modified: Thu, 14 Aug 2025 22:53:28 GMT  
		Size: 572.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ffd7cadd24dc98255420b0676ee8e7d525f7eb32c9b820c2d185cca26390b5`  
		Last Modified: Thu, 14 Aug 2025 22:53:28 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e371f5a1da89826ae722519e76179ad1ed61f6a68e87cc636f6f5aeb8080817`  
		Last Modified: Thu, 14 Aug 2025 23:49:58 GMT  
		Size: 210.9 MB (210913499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f12bd35a14c5709f6beba37183fc49b9b79f0cba3636d62c1b07509f6d33d2`  
		Last Modified: Thu, 14 Aug 2025 22:53:28 GMT  
		Size: 4.0 KB (4047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae893c59e092733b42b58d7a8ed078ba64b8eee3bb9d276eb832bfe538e63ae`  
		Last Modified: Thu, 14 Aug 2025 22:53:28 GMT  
		Size: 2.4 KB (2412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:30-apache` - unknown; unknown

```console
$ docker pull nextcloud@sha256:5b9960ee11f0fc7198b9304f52498857c2238b1b6b2b452538842c18425d90e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 KB (62290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7af01f598d87074bd78328cef797ae55d7fdb2f8bfefafdbb60425a8364dc59`

```dockerfile
```

-	Layers:
	-	`sha256:8dd8f421fd07e90fc1f8d165f3917b2fa118614347f278972b2e5f6ab1525518`  
		Last Modified: Thu, 14 Aug 2025 23:49:28 GMT  
		Size: 62.3 KB (62290 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:30-apache` - linux; arm variant v5

```console
$ docker pull nextcloud@sha256:bc4674985fbaf24b3f23e3516f5185dce9105c11503d15de5c147dcdc2ea575e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.4 MB (398383366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60c774db0e0ddb352efabf9758979d550853e5cba14b66549524722d406a2297`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 06 Aug 2025 00:42:16 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1754870400'
# Wed, 06 Aug 2025 00:42:16 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 06 Aug 2025 00:42:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 06 Aug 2025 00:42:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 06 Aug 2025 00:42:16 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 06 Aug 2025 00:42:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Aug 2025 00:42:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Aug 2025 00:42:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 06 Aug 2025 00:42:16 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 06 Aug 2025 00:42:16 GMT
ENV PHP_VERSION=8.3.24
# Wed, 06 Aug 2025 00:42:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.24.tar.xz.asc
# Wed, 06 Aug 2025 00:42:16 GMT
ENV PHP_SHA256=388ee5fd111097e97bae439bff46aec4ea27f816d3f0c2cb5490a41410d44251
# Wed, 06 Aug 2025 00:42:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 06 Aug 2025 00:42:16 GMT
STOPSIGNAL SIGWINCH
# Wed, 06 Aug 2025 00:42:16 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
WORKDIR /var/www/html
# Wed, 06 Aug 2025 00:42:16 GMT
EXPOSE map[80/tcp:{}]
# Wed, 06 Aug 2025 00:42:16 GMT
CMD ["apache2-foreground"]
# Wed, 06 Aug 2025 00:42:16 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 06 Aug 2025 00:42:16 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 06 Aug 2025 00:42:16 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Wed, 06 Aug 2025 00:42:16 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.26;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.0;     pecl install memcached-3.3.0         --configureoptions 'enable-memcached-igbinary="yes"';     pecl install redis-6.2.0         --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"';         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
VOLUME [/var/www/html]
# Wed, 06 Aug 2025 00:42:16 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Wed, 06 Aug 2025 00:42:16 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
ENV NEXTCLOUD_VERSION=30.0.13
# Wed, 06 Aug 2025 00:42:16 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-30.0.13.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-30.0.13.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
COPY *.sh upgrade.exclude / # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 06 Aug 2025 00:42:16 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:53f325cb4b149fb7bd7e6ed7f8dfc1c5a37b5d828d75b4e6ba65a5cfd25aec56`  
		Last Modified: Tue, 12 Aug 2025 20:45:02 GMT  
		Size: 25.8 MB (25762718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f45607c9703b1623eae4308abc7d9dfac71b6d221b1313958be26dddd31bcd63`  
		Last Modified: Tue, 12 Aug 2025 22:03:30 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f6033c41c6a5cbd10e29711e09c8a94365510a58d88626385f53831b1bd04d5`  
		Last Modified: Tue, 12 Aug 2025 22:03:37 GMT  
		Size: 82.0 MB (81978153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de9e1469fd07000afb3b39a4178a2fa8409d180132e96dee6bffda0a65279f9e`  
		Last Modified: Tue, 12 Aug 2025 22:03:32 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abaa20572a4a3785129b37e835ffaf475213f1a14d056a625ef543e9ac026960`  
		Last Modified: Wed, 13 Aug 2025 06:13:16 GMT  
		Size: 19.4 MB (19418252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c437b13f40151972e7ef755276c4d92b4986a2d5412153e5db35eabff273e0d`  
		Last Modified: Tue, 12 Aug 2025 22:42:41 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04d698f1834ea5af3d28ed5a04bf6880643854221994f6fe45b0aa34c92258e2`  
		Last Modified: Tue, 12 Aug 2025 22:42:41 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a31dad4b75c952bdaf9cfc925ce9df8078d35f334cee4f6aa9a5245c29873a0b`  
		Last Modified: Wed, 13 Aug 2025 03:17:12 GMT  
		Size: 12.7 MB (12705340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8912b0ed0aa87b6ba8e163545421b88f8b30c89ba76d11ef878a37eec70d3800`  
		Last Modified: Wed, 13 Aug 2025 03:17:08 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3373782ef4810e01d1fb4834346c4c99e9b62428a40f6853372f33b0e28008`  
		Last Modified: Wed, 13 Aug 2025 03:17:10 GMT  
		Size: 10.6 MB (10629337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a1ff26fcacb66282dde77aaa4ab2b8683035bde9c2170edbd2f32c54e1ba653`  
		Last Modified: Wed, 13 Aug 2025 03:17:09 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec75188cef45419f16d03524fa1aa9f14b6c51950875771f6667e05a64b1650`  
		Last Modified: Wed, 13 Aug 2025 03:17:09 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba257581e8ce901c6fd78d4d24032d139e279d405b2e2646e1808803c50ab93b`  
		Last Modified: Wed, 13 Aug 2025 03:17:12 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9388e79a4c11a42ce9e0de3b5821d36070156c9a399edb35d6a72a37d7af7a94`  
		Last Modified: Wed, 13 Aug 2025 03:17:11 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6a0177eba4d8ed90b8dec52d6496472962e55ebeafaccc3f922863582d720e`  
		Last Modified: Wed, 13 Aug 2025 14:49:52 GMT  
		Size: 19.9 MB (19895647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7095b620066f1c7b391ba90c379f55ad5cd57644552807d669c9874a3cbf4a0`  
		Last Modified: Wed, 13 Aug 2025 14:49:54 GMT  
		Size: 19.6 MB (19643749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c18bd5330163b5c591395ec72d369a63b7fc8bbfe3a712a3d96d8642cebb49`  
		Last Modified: Wed, 13 Aug 2025 12:18:15 GMT  
		Size: 793.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23004f7a46370fd6fb8134fcdccba7edfa026307fed73d592265afa7d3cbdc91`  
		Last Modified: Wed, 13 Aug 2025 12:18:17 GMT  
		Size: 574.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4dd32f6cafba7351d7252a694e0f385c996ae8e88b5d48025cf0ee384fb7885`  
		Last Modified: Wed, 13 Aug 2025 12:18:21 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1abefbb75ea861aa9a16dc12f70a0f3d0536832a0611b26f8a2cafb094c4a9`  
		Last Modified: Wed, 13 Aug 2025 14:50:06 GMT  
		Size: 208.3 MB (208336201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c079eced8bc69738f657c09ff251048645eccf37ff4b0c5c63c0cc24b15d9f0`  
		Last Modified: Wed, 13 Aug 2025 12:18:24 GMT  
		Size: 4.0 KB (4046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94a88c5541ea065d37515fdfbb4172315dec841b11e4191a7a068f5c2c56da1`  
		Last Modified: Wed, 13 Aug 2025 12:18:28 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:30-apache` - unknown; unknown

```console
$ docker pull nextcloud@sha256:208293d5c0ba8835cab15adb03d023cc376c8f202007cfc59d000ca2cd0c9de2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 KB (62257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffcc5744f47f9e026642525473365b1fae9fb828d7a46ad74ee114f39dad2a5a`

```dockerfile
```

-	Layers:
	-	`sha256:57084ac3af20bb82a9bd35466e8be692941e3dc0e6c8ef92e510404b8f9b1866`  
		Last Modified: Wed, 13 Aug 2025 14:49:25 GMT  
		Size: 62.3 KB (62257 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:30-apache` - linux; arm variant v7

```console
$ docker pull nextcloud@sha256:0207b542f0a1949135f4bfd409a7998efa43bdf3a8beede44383b8e2ed42aad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.2 MB (387154570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2271573aca92bbfda1890080e54c9e84df8f321d0447688e2131c885a58002d8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 06 Aug 2025 00:42:16 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
# Wed, 06 Aug 2025 00:42:16 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 06 Aug 2025 00:42:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 06 Aug 2025 00:42:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 06 Aug 2025 00:42:16 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 06 Aug 2025 00:42:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Aug 2025 00:42:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Aug 2025 00:42:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 06 Aug 2025 00:42:16 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 06 Aug 2025 00:42:16 GMT
ENV PHP_VERSION=8.3.24
# Wed, 06 Aug 2025 00:42:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.24.tar.xz.asc
# Wed, 06 Aug 2025 00:42:16 GMT
ENV PHP_SHA256=388ee5fd111097e97bae439bff46aec4ea27f816d3f0c2cb5490a41410d44251
# Wed, 06 Aug 2025 00:42:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 06 Aug 2025 00:42:16 GMT
STOPSIGNAL SIGWINCH
# Wed, 06 Aug 2025 00:42:16 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
WORKDIR /var/www/html
# Wed, 06 Aug 2025 00:42:16 GMT
EXPOSE map[80/tcp:{}]
# Wed, 06 Aug 2025 00:42:16 GMT
CMD ["apache2-foreground"]
# Wed, 06 Aug 2025 00:42:16 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 06 Aug 2025 00:42:16 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 06 Aug 2025 00:42:16 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Wed, 06 Aug 2025 00:42:16 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.26;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.0;     pecl install memcached-3.3.0         --configureoptions 'enable-memcached-igbinary="yes"';     pecl install redis-6.2.0         --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"';         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
VOLUME [/var/www/html]
# Wed, 06 Aug 2025 00:42:16 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Wed, 06 Aug 2025 00:42:16 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
ENV NEXTCLOUD_VERSION=30.0.13
# Wed, 06 Aug 2025 00:42:16 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-30.0.13.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-30.0.13.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
COPY *.sh upgrade.exclude / # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 06 Aug 2025 00:42:16 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:a8db185805c54c045d888f7030794ebee970355b2336287cac0a0e22638ffc98`  
		Last Modified: Tue, 12 Aug 2025 20:46:38 GMT  
		Size: 23.9 MB (23938929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e03dd152e133ed3c4f7b6111971ebb032fa5347cab0e4ed3c3923003220f8ec4`  
		Last Modified: Tue, 12 Aug 2025 22:02:44 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48d5562d819ed1d81511a866ab9cfa69e1c7f0351806797ebf63ebbb4bacc7c`  
		Last Modified: Tue, 12 Aug 2025 22:02:48 GMT  
		Size: 76.2 MB (76153041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c4000aa6f8df46ea73922bba283db07ef24d97efded72dc7d1e798c0d32e96`  
		Last Modified: Tue, 12 Aug 2025 22:02:45 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98d5a646260be9143e0a73e8a380305b7011867058eac866e2fc96be1e40357d`  
		Last Modified: Tue, 12 Aug 2025 22:07:13 GMT  
		Size: 18.9 MB (18855896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec17d86983395657a14311f5bf8bb526dbcb02f4115a5efc0da9ecdd785b147`  
		Last Modified: Tue, 12 Aug 2025 22:07:09 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63aecbcda44b653e76bd7ff8168d1492421826ef90d182709984b36f3b556695`  
		Last Modified: Tue, 12 Aug 2025 22:07:08 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f34f4ebe21785253fff8096255ded12e036687a469eb433dd3b1c3a20447fc`  
		Last Modified: Wed, 13 Aug 2025 04:19:51 GMT  
		Size: 12.7 MB (12705290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f63410f92bfd2900d579d1e1dd023284e5fa53e93c128a6c2d6db74c2021b1`  
		Last Modified: Wed, 13 Aug 2025 04:19:51 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebfafb0413e5d741487453dd36b2af6ae3c189dbfd64589073d80942b6ba23e5`  
		Last Modified: Wed, 13 Aug 2025 04:19:53 GMT  
		Size: 10.1 MB (10056733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb1c9e7d389b064247ad1b2cd65e43f03687b19c5d15a96501d174b0c6d171b`  
		Last Modified: Wed, 13 Aug 2025 04:19:52 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae3eab3d66d64b7bb0d79ad91e346caa04fdfe5115f9d3544d3594ccd1b2826`  
		Last Modified: Wed, 13 Aug 2025 04:19:52 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16770d101632dccb628e2386e9a2376e36bc677762a8961966826c2e5fe391e4`  
		Last Modified: Wed, 13 Aug 2025 04:19:52 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72c6a42c4f10e0892461e993896cdc72b0d57bbcff50fd122f3c95ec292842a`  
		Last Modified: Wed, 13 Aug 2025 04:19:53 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbe8559e9983fe4e1440e473ff0bf531e3ef8759c534328b6caf3264ebdba3c8`  
		Last Modified: Wed, 13 Aug 2025 15:36:49 GMT  
		Size: 18.1 MB (18145908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec707979f7fbb14e98b5dad5d012b67784686fa82341ebc3d8ff5930611bdb4`  
		Last Modified: Wed, 13 Aug 2025 15:36:52 GMT  
		Size: 18.9 MB (18948646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a11a4bb0ce4ce7bde72f1ee15fe3b763cb09135eab79bf90715a4ae93d1cf69f`  
		Last Modified: Wed, 13 Aug 2025 15:36:48 GMT  
		Size: 793.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9914284132ce381eaed43c041835c400174c548ddd85b967d6f715c07d989791`  
		Last Modified: Wed, 13 Aug 2025 15:36:49 GMT  
		Size: 573.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afa9b7f2088405b1a2d9ba2b0e8100fc5f43b8ee50cfeaca2471bc7403338805`  
		Last Modified: Wed, 13 Aug 2025 15:36:50 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f808f2ce10450dd1ee84b5439b145431c85eced08ec6143c6000e34e5a6aa076`  
		Last Modified: Wed, 13 Aug 2025 17:50:10 GMT  
		Size: 208.3 MB (208336173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:becefb9eef6435717c623678627a2453c361e8e4ce3178e7ae2a83d33cc3dfb1`  
		Last Modified: Wed, 13 Aug 2025 15:36:50 GMT  
		Size: 4.0 KB (4047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81820b5e4511c048f442f3c83a4895be1b08bd20b9013a4ff5d13e0cd93d4ac9`  
		Last Modified: Wed, 13 Aug 2025 15:36:51 GMT  
		Size: 2.4 KB (2415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:30-apache` - unknown; unknown

```console
$ docker pull nextcloud@sha256:ebb08ecd9413c62fe4a725b527856347bbe26679a8028f2ae6215e1b17e42ed1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 KB (62257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8774ecb40cd73e494b094a62a96beafbe0ab0353809d9b4d6845ece52749f3e`

```dockerfile
```

-	Layers:
	-	`sha256:e8bc46c77dfeafb07affa53b3d018e13a46019e817932b43ca75df2ac2e7ae25`  
		Last Modified: Wed, 13 Aug 2025 17:49:31 GMT  
		Size: 62.3 KB (62257 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:30-apache` - linux; arm64 variant v8

```console
$ docker pull nextcloud@sha256:300807b4fa84b7ff8385de8b766585619c26a9f75b0b402bc13b63a1d2d259b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **420.4 MB (420448325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5afde42c6603f07a4dcab1ca70eb8128079c605d5b340c060a1f78ec34729b69`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 06 Aug 2025 00:42:16 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Wed, 06 Aug 2025 00:42:16 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 06 Aug 2025 00:42:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 06 Aug 2025 00:42:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 06 Aug 2025 00:42:16 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 06 Aug 2025 00:42:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Aug 2025 00:42:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Aug 2025 00:42:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 06 Aug 2025 00:42:16 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 06 Aug 2025 00:42:16 GMT
ENV PHP_VERSION=8.3.24
# Wed, 06 Aug 2025 00:42:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.24.tar.xz.asc
# Wed, 06 Aug 2025 00:42:16 GMT
ENV PHP_SHA256=388ee5fd111097e97bae439bff46aec4ea27f816d3f0c2cb5490a41410d44251
# Wed, 06 Aug 2025 00:42:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 06 Aug 2025 00:42:16 GMT
STOPSIGNAL SIGWINCH
# Wed, 06 Aug 2025 00:42:16 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
WORKDIR /var/www/html
# Wed, 06 Aug 2025 00:42:16 GMT
EXPOSE map[80/tcp:{}]
# Wed, 06 Aug 2025 00:42:16 GMT
CMD ["apache2-foreground"]
# Wed, 06 Aug 2025 00:42:16 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 06 Aug 2025 00:42:16 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 06 Aug 2025 00:42:16 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Wed, 06 Aug 2025 00:42:16 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.26;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.0;     pecl install memcached-3.3.0         --configureoptions 'enable-memcached-igbinary="yes"';     pecl install redis-6.2.0         --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"';         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
VOLUME [/var/www/html]
# Wed, 06 Aug 2025 00:42:16 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Wed, 06 Aug 2025 00:42:16 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
ENV NEXTCLOUD_VERSION=30.0.13
# Wed, 06 Aug 2025 00:42:16 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-30.0.13.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-30.0.13.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
COPY *.sh upgrade.exclude / # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 06 Aug 2025 00:42:16 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b489405183f5b9a8efdd3a37c57d3bebb68253f8352b3cc28d4c561af742934`  
		Last Modified: Wed, 13 Aug 2025 03:33:56 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c62173f3c06dd14e87e8ea952140162b61079d18bca9964b5d7193323dfb968`  
		Last Modified: Wed, 13 Aug 2025 03:34:13 GMT  
		Size: 98.2 MB (98153226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b333dd5f982a93ffa19de68383bcbeebbfee4cc755b55e6e4dc21b63a60875a0`  
		Last Modified: Wed, 13 Aug 2025 03:33:57 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d7ae5dabf4163f5b832c5021d3e097188e3238016627e001763e0ebf93c4617`  
		Last Modified: Wed, 13 Aug 2025 03:38:07 GMT  
		Size: 20.1 MB (20136109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f7fd6c8d4e47317e40b56c29e1f545ec42f8f5e1ecb535541ec55b49c48b59`  
		Last Modified: Wed, 13 Aug 2025 03:37:59 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5526e2be58d931602aaa7df69ee76b367775dc351ebba0b1ff2f6dc8f485999`  
		Last Modified: Wed, 13 Aug 2025 03:37:59 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31594fba8506a0a5659bbc7faea292feae95b1b8d5cf64cc6238694b5f315d98`  
		Last Modified: Wed, 13 Aug 2025 04:39:38 GMT  
		Size: 12.7 MB (12707182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d32d702122dc532c4ee4579a85f5b3d17dc29e6b0a4ab2eed065d7cff7ee26`  
		Last Modified: Wed, 13 Aug 2025 04:39:37 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64eed71798826296504c48c113779f3cea17ff6f583816e2cae28e919c947fb1`  
		Last Modified: Wed, 13 Aug 2025 04:39:40 GMT  
		Size: 11.7 MB (11681629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f46c47f97d1917407e1a8c740ea5d0e3b7217c1193a631ea26363342089915bb`  
		Last Modified: Wed, 13 Aug 2025 04:39:37 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e9b991d0ad159d3b3264234fc6e82781e1e510d78b30c1b7c558bcdd224cf6`  
		Last Modified: Wed, 13 Aug 2025 04:39:37 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:869cbb48f7445ee268b880745a4b4f7919b754edb0c1aff826221c1635d58f07`  
		Last Modified: Wed, 13 Aug 2025 04:39:38 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf0a6059d944e8e76787e8675b78fd8800c28586eec5e735fbcb44ccd028503`  
		Last Modified: Wed, 13 Aug 2025 04:39:38 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c24a8d8af9048f3752d860a1ec52d63fba8b88b7e1e39d836092b2664a0a15e`  
		Last Modified: Wed, 13 Aug 2025 17:41:41 GMT  
		Size: 20.2 MB (20155352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f69550026709cbd05bd87850e63b565705ce9ff5d47a7a8ac89b41010d61f0`  
		Last Modified: Wed, 13 Aug 2025 17:41:46 GMT  
		Size: 21.2 MB (21180198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f163c1437d61088b0a4a7554e294fe80e9a66178ad53d0b85c58bd53fad219`  
		Last Modified: Wed, 13 Aug 2025 17:41:40 GMT  
		Size: 795.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ca9449b81f9eae33d42c4b6b6ce9f19208e8bd0aaa19937eb79c20c37437dd`  
		Last Modified: Wed, 13 Aug 2025 17:41:41 GMT  
		Size: 574.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475c15a897b7d1d42d7cbf8ba5db6e6f6b74ca09d5741e8da201594c2526957c`  
		Last Modified: Wed, 13 Aug 2025 17:41:41 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39d5fc60447dbdeef3479ad2ebdbdf55f098c235943c343cd0b6cfeb6142591`  
		Last Modified: Wed, 13 Aug 2025 21:15:04 GMT  
		Size: 208.3 MB (208338664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f0b30f0fc1aa94352e256eacf882f42b5d380049d991faf59ab8251438d1d70`  
		Last Modified: Wed, 13 Aug 2025 17:41:41 GMT  
		Size: 4.0 KB (4046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:072f3ddf4a48505eecf7644b13020e0e0d6d7eb2b2c48d65fe5bb1b02667f839`  
		Last Modified: Wed, 13 Aug 2025 17:41:41 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:30-apache` - unknown; unknown

```console
$ docker pull nextcloud@sha256:946fba591da6c7d7c509074810013466fd0631cf49b284e12fcbfd29c3ca7df9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 KB (62303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65e5fd147d7544bc75b2e4e86af4b88e9fc7ac0625e5d0b46d692c01707532b6`

```dockerfile
```

-	Layers:
	-	`sha256:32d1fc985b605461a788fb6432b8da35baf8c7db155a0795d64ac2eeb53c5787`  
		Last Modified: Wed, 13 Aug 2025 20:49:28 GMT  
		Size: 62.3 KB (62303 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:30-apache` - linux; 386

```console
$ docker pull nextcloud@sha256:8e6ac455f3964327b823b261b2f65f517250d99add7aa99463918921a9788951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **446.0 MB (446020276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:539f943f12f74d95f9583fb90705075dc288895e04a2c0e79d2342f3577a7ffc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 08 Aug 2025 00:02:22 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1754870400'
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 08 Aug 2025 00:02:22 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 Aug 2025 00:02:22 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_VERSION=8.3.24
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.24.tar.xz.asc
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_SHA256=388ee5fd111097e97bae439bff46aec4ea27f816d3f0c2cb5490a41410d44251
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 Aug 2025 00:02:22 GMT
STOPSIGNAL SIGWINCH
# Fri, 08 Aug 2025 00:02:22 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
WORKDIR /var/www/html
# Fri, 08 Aug 2025 00:02:22 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 Aug 2025 00:02:22 GMT
CMD ["apache2-foreground"]
# Thu, 14 Aug 2025 19:55:08 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-7.q16-10-extra         rsync     ;     apt-get dist-clean;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Thu, 14 Aug 2025 19:55:08 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 14 Aug 2025 19:55:08 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 14 Aug 2025 19:55:08 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Thu, 14 Aug 2025 19:55:08 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.26;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.0;     pecl install memcached-3.3.0         --configureoptions 'enable-memcached-igbinary="yes"';     pecl install redis-6.2.0         --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"';         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -rt dpkg-query --search         | awk 'sub(":$", "", $1) { print $1 }'         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     apt-get dist-clean # buildkit
# Thu, 14 Aug 2025 19:55:08 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Thu, 14 Aug 2025 19:55:08 GMT
VOLUME [/var/www/html]
# Thu, 14 Aug 2025 19:55:08 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip # buildkit
# Thu, 14 Aug 2025 19:55:08 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Thu, 14 Aug 2025 19:55:08 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits # buildkit
# Thu, 14 Aug 2025 19:55:08 GMT
ENV NEXTCLOUD_VERSION=30.0.14
# Thu, 14 Aug 2025 19:55:08 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-30.0.14.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-30.0.14.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     apt-get dist-clean # buildkit
# Thu, 14 Aug 2025 19:55:08 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 14 Aug 2025 19:55:08 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Thu, 14 Aug 2025 19:55:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 14 Aug 2025 19:55:08 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:346d0c953bdbc38917a27a6f30726e5b46419d98ecaf4d2d8f201bc3b7025e57`  
		Last Modified: Tue, 12 Aug 2025 20:45:00 GMT  
		Size: 31.3 MB (31289378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6b38246eb5bdb9483680cbc38bea150ab28cf14c0f84a601382c6bb117bbfc`  
		Last Modified: Tue, 12 Aug 2025 22:52:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a808d1fdf3251d152671eb3210102f561cfbb985fd687ae51e550fabcb93d48a`  
		Last Modified: Tue, 12 Aug 2025 22:53:15 GMT  
		Size: 116.1 MB (116135228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf13ffda88425b0b5e3b7ea838f516d81504a3a882ffcbc800b567ddc856633d`  
		Last Modified: Tue, 12 Aug 2025 22:52:57 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8aab4238479571353eaa5d34f75b8e6f0dee3a3e7f28d815f0b3920a54a9b8`  
		Last Modified: Tue, 12 Aug 2025 22:52:59 GMT  
		Size: 4.5 MB (4455082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f69fe17afc6d7f0a8eafbc6a23e21199136a1746d89bf7039ee3537f6483530`  
		Last Modified: Tue, 12 Aug 2025 22:52:57 GMT  
		Size: 426.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43219ca10783635a08e24fc45985f1b59c3bb3e2325ea9e52cb460130c0928f`  
		Last Modified: Tue, 12 Aug 2025 22:52:57 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a294f29ff937f96dec58c3e863419809a8adb759708df5faa9bf57788d90cdc3`  
		Last Modified: Tue, 12 Aug 2025 22:53:00 GMT  
		Size: 12.7 MB (12743204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ba86522e967f55a94d3a6958184b2ab3984033b02b59f3c90bb28afb424df4`  
		Last Modified: Tue, 12 Aug 2025 22:52:56 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c881f0a34a87ed68af609e8fff95ea1fa4128df784c0b463addb74507597353`  
		Last Modified: Tue, 12 Aug 2025 22:53:01 GMT  
		Size: 11.9 MB (11914207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad3e68077db9aa2fecba92a9873385ee5e1400d2f408c082dfd9a4283703717`  
		Last Modified: Tue, 12 Aug 2025 22:53:00 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:971adc1a08f5938ac43eaeea416fcaad0b9c675606ab517b31fffd7d879d2ecb`  
		Last Modified: Tue, 12 Aug 2025 22:52:52 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:971218291aa3f1ddfffe5b6f13d766298e78ab278873c761c9c01ad0f0af6120`  
		Last Modified: Tue, 12 Aug 2025 22:52:52 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953ba78b6de6e70ba63f58b0c565ebca6f720ca5d6d78e7efa092ebacd49fa89`  
		Last Modified: Tue, 12 Aug 2025 22:52:52 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9ccb88b3bc1307b044f37958944884d99814012e85632781ee9715d3ad5527`  
		Last Modified: Thu, 14 Aug 2025 22:53:49 GMT  
		Size: 21.2 MB (21172394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054e8ea64c7bdca51713eede690fa60b04dcf3f43cca9ec4eb701574d96fd669`  
		Last Modified: Thu, 14 Aug 2025 22:53:56 GMT  
		Size: 37.4 MB (37384653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acce006f95dec709f0d7a32d309b650d490e23e1a9eed9708291fccc687182e`  
		Last Modified: Thu, 14 Aug 2025 22:53:46 GMT  
		Size: 792.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8a761033e6b89990514b67ee7287f09dfd95df541dbf3370d2c5696bae40db`  
		Last Modified: Thu, 14 Aug 2025 22:53:46 GMT  
		Size: 571.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9954c55cae39aa884a6dd018bdd5688476baac58454c72fd0e66550d9f471aa6`  
		Last Modified: Thu, 14 Aug 2025 22:53:46 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d7e5c6c52814b9dbb798450ae3a0f322ff6277b630be5f1c1b60314cf4cf14`  
		Last Modified: Thu, 14 Aug 2025 23:51:37 GMT  
		Size: 210.9 MB (210912189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7bdcb3cd85b1739567566dfd8331bc68d62b67b1532f7417892e19a366ce288`  
		Last Modified: Thu, 14 Aug 2025 22:53:46 GMT  
		Size: 4.0 KB (4047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb9ce0d68babc65423ad8b5b7ecbed9fb16e96fdabef06d3128917b24be5cad`  
		Last Modified: Thu, 14 Aug 2025 22:53:46 GMT  
		Size: 2.4 KB (2416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:30-apache` - unknown; unknown

```console
$ docker pull nextcloud@sha256:0eedffbef89dc5b7f7b7bd0397a1398e166fb4c0a9c6d3b9c5a4b04c3c856954
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 KB (62237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30b480fab5bab1345f2853daaaf52366d3e10a1190fb1316437cce07abb9603c`

```dockerfile
```

-	Layers:
	-	`sha256:b7d769f9de2d0f731f66cf8d48f0acb52b42aa1831b7656bfd9f1ef3752f49b6`  
		Last Modified: Thu, 14 Aug 2025 23:49:38 GMT  
		Size: 62.2 KB (62237 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:30-apache` - linux; ppc64le

```console
$ docker pull nextcloud@sha256:e9d55fd85e8c88827668d4c2a65111de03c79b7e15438e16b356820404ff27f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.4 MB (434360782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d02e47a9255ed3d2acaf2955d1caec3bab1af82c2923a02117480e77f2f5ce79`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 06 Aug 2025 00:42:16 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Wed, 06 Aug 2025 00:42:16 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 06 Aug 2025 00:42:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 06 Aug 2025 00:42:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 06 Aug 2025 00:42:16 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 06 Aug 2025 00:42:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Aug 2025 00:42:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Aug 2025 00:42:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 06 Aug 2025 00:42:16 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 06 Aug 2025 00:42:16 GMT
ENV PHP_VERSION=8.3.24
# Wed, 06 Aug 2025 00:42:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.24.tar.xz.asc
# Wed, 06 Aug 2025 00:42:16 GMT
ENV PHP_SHA256=388ee5fd111097e97bae439bff46aec4ea27f816d3f0c2cb5490a41410d44251
# Wed, 06 Aug 2025 00:42:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 06 Aug 2025 00:42:16 GMT
STOPSIGNAL SIGWINCH
# Wed, 06 Aug 2025 00:42:16 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
WORKDIR /var/www/html
# Wed, 06 Aug 2025 00:42:16 GMT
EXPOSE map[80/tcp:{}]
# Wed, 06 Aug 2025 00:42:16 GMT
CMD ["apache2-foreground"]
# Wed, 06 Aug 2025 00:42:16 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 06 Aug 2025 00:42:16 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 06 Aug 2025 00:42:16 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Wed, 06 Aug 2025 00:42:16 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.26;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.0;     pecl install memcached-3.3.0         --configureoptions 'enable-memcached-igbinary="yes"';     pecl install redis-6.2.0         --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"';         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
VOLUME [/var/www/html]
# Wed, 06 Aug 2025 00:42:16 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Wed, 06 Aug 2025 00:42:16 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
ENV NEXTCLOUD_VERSION=30.0.13
# Wed, 06 Aug 2025 00:42:16 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-30.0.13.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-30.0.13.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
COPY *.sh upgrade.exclude / # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 06 Aug 2025 00:42:16 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:a0acf07605078e5950db4f22a00d81ec636270d184a86cff95e60b78f012035c`  
		Last Modified: Tue, 12 Aug 2025 23:06:40 GMT  
		Size: 32.1 MB (32073420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a363500f88bae53ed85a0884af78492e18e2de8fc3862f1472e7a5a3e503dc87`  
		Last Modified: Wed, 13 Aug 2025 06:51:52 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1eb370a99493c04fbb6a54fc3c2fa12bf4afac30b54e58e473794b525eaca2d`  
		Last Modified: Wed, 13 Aug 2025 07:37:29 GMT  
		Size: 103.3 MB (103328754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc5ef6f8d35100f42cd71cdbcef48544c8e88e6827718d834112c80e310f368`  
		Last Modified: Wed, 13 Aug 2025 07:05:57 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab47dec8cdcec5cbb5349fb982256d14a603de3b3c8d8e7c6bd16f30d81de63`  
		Last Modified: Wed, 13 Aug 2025 08:51:58 GMT  
		Size: 21.3 MB (21308293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c723dfb22afab56884f3f5e825b4d8cf66f158c68932630708bc1ae2fb6b7b`  
		Last Modified: Wed, 13 Aug 2025 08:51:59 GMT  
		Size: 436.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bcd34966f4a680377a52a84288adf114ebb46153e83b68cdde845b06ea68fe3`  
		Last Modified: Wed, 13 Aug 2025 08:52:00 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf4e8d4d66a28473a0e70950d16eedc1ea3595c33cddc1fd0c35f577a4d89df`  
		Last Modified: Wed, 13 Aug 2025 07:02:06 GMT  
		Size: 12.7 MB (12706874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:074349ace2c7d71f161fb064b8126b0977b0fff5050eccb7e975bc84be5f0fb1`  
		Last Modified: Wed, 13 Aug 2025 07:02:04 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1a4bf9ea7968b9b591262abfb924b7457a01cc7d2b72ec6521c8f368cbcb8c`  
		Last Modified: Wed, 13 Aug 2025 07:02:05 GMT  
		Size: 12.1 MB (12075467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c18d85531515a4139ef934e77038fb5481f6783870c86a60c57c3767ff9d0f1c`  
		Last Modified: Wed, 13 Aug 2025 07:02:05 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f1e215a2e4617328d08a66761772e8427344c1924ae0a748f49cae16cb07b2`  
		Last Modified: Wed, 13 Aug 2025 07:02:05 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:960dcca7a4e1d585418045fff6d2cd42ed2ce37e4568323e8f4285bdd2748f81`  
		Last Modified: Wed, 13 Aug 2025 07:02:02 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00979487fa3792db0b6a415e08d0cfc9970d4c89d85c6cc23c3f261e83286ec4`  
		Last Modified: Wed, 13 Aug 2025 07:02:03 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1e441195de9bbb2d2ea768318aafc37abe7d156b907518ca7f1d2ad34e036c6`  
		Last Modified: Thu, 14 Aug 2025 02:50:05 GMT  
		Size: 22.6 MB (22624569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8f168e4d1ab0e8558cfc9b0814aa46e097bcf6556a1db9a3a8d285778efe6a`  
		Last Modified: Thu, 14 Aug 2025 02:49:56 GMT  
		Size: 21.9 MB (21890007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce0b234175ee60221087ff4bed9ee2cdf66d7872854c134b811240b52581ac4`  
		Last Modified: Thu, 14 Aug 2025 01:15:07 GMT  
		Size: 791.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d744befe1cd4241b3836860877476b17020cf4e2538b4e728fce6c4eecd1b4c5`  
		Last Modified: Thu, 14 Aug 2025 01:15:10 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:509b90445bed37a99cbc370336ebf7886cb9a68c66938dd7e1232ea5154917da`  
		Last Modified: Thu, 14 Aug 2025 01:15:12 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37775440e3bb0e29f186fa19bfecb9a20e1703095418807114e1308c8757884e`  
		Last Modified: Thu, 14 Aug 2025 02:50:08 GMT  
		Size: 208.3 MB (208339423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8763c0ac09ed4d155bbf9c24041083a9f1d20a76447b911fdf0b6f42b9d1493c`  
		Last Modified: Thu, 14 Aug 2025 01:15:15 GMT  
		Size: 4.0 KB (4046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6cc6fc29af2e9cbcec2dcb7d5a54e14ee134d62cc1ad84af996b42af1461725`  
		Last Modified: Thu, 14 Aug 2025 01:15:18 GMT  
		Size: 2.4 KB (2417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:30-apache` - unknown; unknown

```console
$ docker pull nextcloud@sha256:3cbdce4530d3c572a20c73c5e3002ba34758b0fca7efcdd60a76049142f49171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 KB (62175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e43b0d99dbe50426e325d73bce1a1619e07538d266d7f62e794eb28a016b3b5`

```dockerfile
```

-	Layers:
	-	`sha256:d61da7ac7e8ef3f45fec58775d9d66a34e1cdad4058e46b0439a7b5c5340b379`  
		Last Modified: Thu, 14 Aug 2025 02:49:33 GMT  
		Size: 62.2 KB (62175 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:30-apache` - linux; s390x

```console
$ docker pull nextcloud@sha256:4d16c101fb46aa2954e1c6529bbc928478be8dde64d7d785772eae838771631d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.0 MB (398998583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52f52376394f4d8a4bdd689516a32fc60c66fe449c304b269366df72a31355d7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 06 Aug 2025 00:42:16 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Wed, 06 Aug 2025 00:42:16 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 06 Aug 2025 00:42:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 06 Aug 2025 00:42:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 06 Aug 2025 00:42:16 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 06 Aug 2025 00:42:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Aug 2025 00:42:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Aug 2025 00:42:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 06 Aug 2025 00:42:16 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 06 Aug 2025 00:42:16 GMT
ENV PHP_VERSION=8.3.24
# Wed, 06 Aug 2025 00:42:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.24.tar.xz.asc
# Wed, 06 Aug 2025 00:42:16 GMT
ENV PHP_SHA256=388ee5fd111097e97bae439bff46aec4ea27f816d3f0c2cb5490a41410d44251
# Wed, 06 Aug 2025 00:42:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 06 Aug 2025 00:42:16 GMT
STOPSIGNAL SIGWINCH
# Wed, 06 Aug 2025 00:42:16 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
WORKDIR /var/www/html
# Wed, 06 Aug 2025 00:42:16 GMT
EXPOSE map[80/tcp:{}]
# Wed, 06 Aug 2025 00:42:16 GMT
CMD ["apache2-foreground"]
# Wed, 06 Aug 2025 00:42:16 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 06 Aug 2025 00:42:16 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 06 Aug 2025 00:42:16 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Wed, 06 Aug 2025 00:42:16 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.26;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.0;     pecl install memcached-3.3.0         --configureoptions 'enable-memcached-igbinary="yes"';     pecl install redis-6.2.0         --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"';         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
VOLUME [/var/www/html]
# Wed, 06 Aug 2025 00:42:16 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Wed, 06 Aug 2025 00:42:16 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
ENV NEXTCLOUD_VERSION=30.0.13
# Wed, 06 Aug 2025 00:42:16 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-30.0.13.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-30.0.13.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
COPY *.sh upgrade.exclude / # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Wed, 06 Aug 2025 00:42:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 06 Aug 2025 00:42:16 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160fd1a1a421ab2a967d88788fa69f4a8c0d0124bb8618a96dadd2d0b88b93ca`  
		Last Modified: Wed, 13 Aug 2025 10:57:35 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a62186e269f8e7afe7503ad0b95ed43cf9977a95fe4bf4276d7b309de1b2630`  
		Last Modified: Wed, 13 Aug 2025 11:56:29 GMT  
		Size: 80.8 MB (80826980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283e45bba3759ef3324f879c06fb1eebcda36d5470316f27b6e2fd8d86a8a0d2`  
		Last Modified: Wed, 13 Aug 2025 10:57:36 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a89f7c20ff77c478fb295cf8f66b8260fe7d9594c7da1d918e23894e507d5e3`  
		Last Modified: Wed, 13 Aug 2025 12:57:49 GMT  
		Size: 19.9 MB (19895051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa7f9b3cb117e520c58e1fed8ebca993aac8c5add667e0e6eba824c44117ebc6`  
		Last Modified: Wed, 13 Aug 2025 11:13:23 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e61f86598fd509db3d73f90a72a7b48d5a025fd2791a5be72d43645b236db1c`  
		Last Modified: Wed, 13 Aug 2025 11:13:25 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34eb30028cd35016a4662bf5342d70bdebf34680b6d8d6108828489c87c95527`  
		Last Modified: Wed, 13 Aug 2025 14:27:56 GMT  
		Size: 12.7 MB (12705711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7471fe8deb8248912a7837230fb85f7be12810e9a977b629a191b3d3898947c5`  
		Last Modified: Wed, 13 Aug 2025 11:46:47 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35cdba6c0064d40181f6fca5abcb30da0ca29e0fb8a370428b682c5458a9a0b`  
		Last Modified: Wed, 13 Aug 2025 14:27:58 GMT  
		Size: 10.9 MB (10878027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:048301ffe209ed6e610bb48eaca2dc65d4ee1ada3791afd49a1c1e628121602f`  
		Last Modified: Wed, 13 Aug 2025 11:15:11 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c58f54c7cb2959cdb2a820edc49d8e58b5a4a501324b3f1f41e6f52adbb82de`  
		Last Modified: Wed, 13 Aug 2025 11:15:14 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427184cabdc4c35b2786849b0bd34baca19cca107f4377108ec75fb2b32352d3`  
		Last Modified: Wed, 13 Aug 2025 11:15:17 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53aa66df002ed07b18ca7727ecb44ded7977d533c3963843a494fb2724d483ea`  
		Last Modified: Wed, 13 Aug 2025 11:15:20 GMT  
		Size: 887.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc057e9b73d7f8c2671f4fd11ec5a6567acd34a43128ee5a30ec422d812cc628`  
		Last Modified: Wed, 13 Aug 2025 17:50:04 GMT  
		Size: 19.3 MB (19300975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578ee62289393d648b38543842b98d793deff152e7096024c9156d95e9991e65`  
		Last Modified: Wed, 13 Aug 2025 17:50:09 GMT  
		Size: 20.2 MB (20153353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9ac2901e06718bf38608cd466b084f6d7bff980dbdd79ab922485d36a89127`  
		Last Modified: Wed, 13 Aug 2025 15:02:22 GMT  
		Size: 794.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5084f5aa179858083f1ee256e3a66395cad522d03764cd4d904b8c35410681d`  
		Last Modified: Wed, 13 Aug 2025 15:02:20 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0edd0e7773f1b9f9e24f863d5f047b451a0ca8c33c1f617b9f587985f9e410c0`  
		Last Modified: Wed, 13 Aug 2025 15:02:22 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88dda4dcac10c051cebc0fe7b9ba80700f78393f6ec726bee87835dac913dd55`  
		Last Modified: Wed, 13 Aug 2025 17:50:17 GMT  
		Size: 208.3 MB (208336678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaaf5484cde89508eaec3ae3a458617c92aca3b991e65c2486462fd4c7d2aa95`  
		Last Modified: Wed, 13 Aug 2025 15:02:23 GMT  
		Size: 4.0 KB (4046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:439752be688a9dc5dbee52cf121ffaef7ced26cb850febba82b1d1f1f36c5ca2`  
		Last Modified: Wed, 13 Aug 2025 15:02:20 GMT  
		Size: 2.4 KB (2415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:30-apache` - unknown; unknown

```console
$ docker pull nextcloud@sha256:9e6cc8aa09d22d652e08b10d61c18dceacd7b5b72ca69392ea2c1c906fea1908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.1 KB (62100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:283cd827b7388e8837e883466cc7b20a3b1a563af7102474055ec06998cb2d72`

```dockerfile
```

-	Layers:
	-	`sha256:ffaae73b5bc3750918b9c86789038ab14bb78c4ee34669e1ca33173f2d536700`  
		Last Modified: Wed, 13 Aug 2025 17:49:43 GMT  
		Size: 62.1 KB (62100 bytes)  
		MIME: application/vnd.in-toto+json
