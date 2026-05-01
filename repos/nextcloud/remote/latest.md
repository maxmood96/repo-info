## `nextcloud:latest`

```console
$ docker pull nextcloud@sha256:76f04e434a82572dbfee7ad6dca313229eade89ee538fccd2bf6396f4440d48b
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

### `nextcloud:latest` - linux; amd64

```console
$ docker pull nextcloud@sha256:f3fd5b703e175d9330b8b2a2c82b9357782f1f0d75e3e82988d686bd588ee3b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **504.1 MB (504124816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c9c19bf274f627738f87a7cf5292f2ac2dbce7d4286b793c68d60fb111bd79c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:24:41 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 22 Apr 2026 01:24:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Apr 2026 01:24:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:24:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Apr 2026 01:24:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 22 Apr 2026 01:24:58 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 22 Apr 2026 01:24:58 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 22 Apr 2026 01:25:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 22 Apr 2026 01:25:04 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 22 Apr 2026 01:25:04 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 22 Apr 2026 01:25:04 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:25:04 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:25:04 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Apr 2026 01:25:04 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 22 Apr 2026 01:25:04 GMT
ENV PHP_VERSION=8.4.20
# Wed, 22 Apr 2026 01:25:04 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 22 Apr 2026 01:25:04 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 22 Apr 2026 01:25:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 01:25:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:27:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 01:27:56 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:27:56 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 22 Apr 2026 01:27:56 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 01:27:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 01:27:56 GMT
STOPSIGNAL SIGWINCH
# Wed, 22 Apr 2026 01:27:56 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:27:56 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 01:27:56 GMT
EXPOSE map[80/tcp:{}]
# Wed, 22 Apr 2026 01:27:56 GMT
CMD ["apache2-foreground"]
# Fri, 01 May 2026 08:35:31 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-7.q16-10-extra         rsync     ;     apt-get dist-clean;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Fri, 01 May 2026 08:37:34 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 01 May 2026 08:37:34 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 01 May 2026 08:37:34 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Fri, 01 May 2026 08:37:34 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         liblz4-dev         libmagickwand-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-ftp-ssl;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.28;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.1;     pecl install --configureoptions 'enable-memcached-igbinary="yes"'         memcached-3.4.0;     pecl install --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"'         redis-6.3.0;         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -rt dpkg-query --search         | awk 'sub(":$", "", $1) { print $1 }'         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     apt-get dist-clean # buildkit
# Fri, 01 May 2026 08:37:34 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Fri, 01 May 2026 08:37:34 GMT
VOLUME [/var/www/html]
# Fri, 01 May 2026 08:37:34 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip # buildkit
# Fri, 01 May 2026 08:37:34 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Fri, 01 May 2026 08:37:34 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits # buildkit
# Fri, 01 May 2026 08:37:34 GMT
ENV NEXTCLOUD_VERSION=33.0.3
# Fri, 01 May 2026 08:38:07 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://github.com/nextcloud-releases/server/releases/download/v33.0.3/nextcloud-33.0.3.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://github.com/nextcloud-releases/server/releases/download/v33.0.3/nextcloud-33.0.3.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     apt-get dist-clean # buildkit
# Fri, 01 May 2026 08:38:07 GMT
COPY *.sh upgrade.exclude / # buildkit
# Fri, 01 May 2026 08:38:07 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Fri, 01 May 2026 08:38:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 May 2026 08:38:07 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d023baa873c0991ddaa7419301cf610d5e56ceb38356f1845ae0e94eb05dc3c9`  
		Last Modified: Wed, 22 Apr 2026 01:28:18 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:574faee95b5376fc2f0f3f093a9e6780a97d7eedc2da840e55380b1d36f85a89`  
		Last Modified: Wed, 22 Apr 2026 01:28:21 GMT  
		Size: 117.8 MB (117843202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfa6ce5874bc20b89543cd80d41f58507e071af1977b4fc38fe6a13ca83fdeb`  
		Last Modified: Wed, 22 Apr 2026 01:28:18 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcafbe281a6757cd10d2aea9b90f3636b474dd2516c0980d602df86c6d4781b`  
		Last Modified: Wed, 22 Apr 2026 01:28:18 GMT  
		Size: 4.2 MB (4226905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c19f6aeb84e92127e2e3d01ae0c2404b696e34500cff3e1730ca85603f24ae`  
		Last Modified: Wed, 22 Apr 2026 01:28:19 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ed48780967058ba90258dfa165a33a65ef90d6260c78464947bb8732c2091f`  
		Last Modified: Wed, 22 Apr 2026 01:28:19 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3a3c22f89f33eacca27643c304fbf4cdced1a494513ba0684cd5faf51ff50a`  
		Last Modified: Wed, 22 Apr 2026 01:28:20 GMT  
		Size: 13.9 MB (13852567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce7e42314878fa75790cd20ec64c41553110fe17f16b9c26967a225173a8acf`  
		Last Modified: Wed, 22 Apr 2026 01:28:21 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9c72387956fde81883201db10160d5778cbc5b4846c394578385ffadd64ade`  
		Last Modified: Wed, 22 Apr 2026 01:28:21 GMT  
		Size: 13.6 MB (13557477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae044dcde24485109733a3bc78f06686efea05cd32c03f0c38c68e2f825a8b00`  
		Last Modified: Wed, 22 Apr 2026 01:28:22 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de552cfaae1b01c9edff1ddfa947b594abc5c5cd7e5935083ef66faf36a2e64`  
		Last Modified: Wed, 22 Apr 2026 01:28:22 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a166fb5f1996a6802829599fa567e0f5051d57568f2922b032eb0402fe03cdff`  
		Last Modified: Wed, 22 Apr 2026 01:28:22 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28aafaa0f9a2d4557c2e9c1f953def4005d036064e46b0d8226bd8aa3047f10c`  
		Last Modified: Wed, 22 Apr 2026 01:28:23 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26165b5804639bcc2d7b8375d0897a1b5f15fb2f1f2b833d743ec85479ada21e`  
		Last Modified: Fri, 01 May 2026 08:38:34 GMT  
		Size: 21.0 MB (20965595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50e04f3b5ecd4bd71f6075def04fec8526e9e9c708020b84bd2ec50241c8b2b`  
		Last Modified: Fri, 01 May 2026 08:38:35 GMT  
		Size: 36.9 MB (36893039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7db8db7a82edd15981576f6aac21b7fd98c1630fa86e112cac2f08abda3207e`  
		Last Modified: Fri, 01 May 2026 08:38:33 GMT  
		Size: 794.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c27297979e6d83e0c3f7f66992ae4e29b735e8bc5faeb743d7f2d8f6ecf51d4`  
		Last Modified: Fri, 01 May 2026 08:38:33 GMT  
		Size: 576.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf2dbe490ad7293eb789efea8a573454b6911f5484626d16400207f2ff96943`  
		Last Modified: Fri, 01 May 2026 08:38:35 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7346d70f9dfb088b2ac159f5952f6294b6dd1b60c6e89adf55f2cdf0782179af`  
		Last Modified: Fri, 01 May 2026 08:38:40 GMT  
		Size: 267.0 MB (266991799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1edd26fa8b7bea7367c9a05595fb244550bec7c5e8179b897186f3642d5e16f2`  
		Last Modified: Fri, 01 May 2026 08:38:36 GMT  
		Size: 4.1 KB (4136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c72297bdb82b31c81b8b11c14ee45cce8734fd5ff6b2bf50a7135ec4d795406`  
		Last Modified: Fri, 01 May 2026 08:38:36 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:latest` - unknown; unknown

```console
$ docker pull nextcloud@sha256:391595625d2598f92098d633abace2d78eb8bd2b0cbfc7ecc8ab995c09ebec5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 KB (64188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adaf282f1da0fbdf8988b5588684d33173454fd6b64cb9c244794509454de9fe`

```dockerfile
```

-	Layers:
	-	`sha256:87d9081261efda8db843f658567bc7ec65fd3dbe76ee0be98887aee557b7e731`  
		Last Modified: Fri, 01 May 2026 08:38:33 GMT  
		Size: 64.2 KB (64188 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:latest` - linux; arm variant v5

```console
$ docker pull nextcloud@sha256:e115c7a84ccbc172e9bf9312953e6803e7c1d552768cec6ac8d0744c3028a36d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **475.1 MB (475081120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42278eb9d58c298a096404a9d513b2b1e97631424c97db63600aa59a14517b5c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:27:37 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 22 Apr 2026 01:28:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Apr 2026 01:28:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:28:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Apr 2026 01:28:00 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 22 Apr 2026 01:28:00 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 22 Apr 2026 01:28:00 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 22 Apr 2026 01:28:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 22 Apr 2026 01:28:09 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 22 Apr 2026 01:28:10 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 22 Apr 2026 01:28:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:28:10 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:28:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Apr 2026 01:28:10 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 22 Apr 2026 01:28:10 GMT
ENV PHP_VERSION=8.4.20
# Wed, 22 Apr 2026 01:28:10 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 22 Apr 2026 01:28:10 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 22 Apr 2026 01:28:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 01:28:23 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:31:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 01:31:37 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:31:37 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 22 Apr 2026 01:31:37 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 01:31:37 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 01:31:37 GMT
STOPSIGNAL SIGWINCH
# Wed, 22 Apr 2026 01:31:37 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:31:37 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 01:31:37 GMT
EXPOSE map[80/tcp:{}]
# Wed, 22 Apr 2026 01:31:37 GMT
CMD ["apache2-foreground"]
# Fri, 01 May 2026 05:48:08 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-7.q16-10-extra         rsync     ;     apt-get dist-clean;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Fri, 01 May 2026 05:51:27 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 01 May 2026 05:51:27 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 01 May 2026 05:51:27 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Fri, 01 May 2026 05:51:27 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         liblz4-dev         libmagickwand-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-ftp-ssl;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.28;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.1;     pecl install --configureoptions 'enable-memcached-igbinary="yes"'         memcached-3.4.0;     pecl install --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"'         redis-6.3.0;         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -rt dpkg-query --search         | awk 'sub(":$", "", $1) { print $1 }'         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     apt-get dist-clean # buildkit
# Fri, 01 May 2026 05:51:27 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Fri, 01 May 2026 05:51:27 GMT
VOLUME [/var/www/html]
# Fri, 01 May 2026 05:51:27 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip # buildkit
# Fri, 01 May 2026 05:51:27 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Fri, 01 May 2026 05:51:27 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits # buildkit
# Fri, 01 May 2026 05:51:27 GMT
ENV NEXTCLOUD_VERSION=33.0.3
# Fri, 01 May 2026 05:54:09 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://github.com/nextcloud-releases/server/releases/download/v33.0.3/nextcloud-33.0.3.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://github.com/nextcloud-releases/server/releases/download/v33.0.3/nextcloud-33.0.3.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     apt-get dist-clean # buildkit
# Fri, 01 May 2026 05:54:09 GMT
COPY *.sh upgrade.exclude / # buildkit
# Fri, 01 May 2026 05:54:10 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Fri, 01 May 2026 05:54:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 May 2026 05:54:10 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:6496d93bca0663211b9252da346044ecb734ee5b3ecaae5b1fbd230753faee2f`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 27.9 MB (27948180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ab8cd142c874a4a2116214700713c2dec92f9352b96761c33107037fb9f0d57`  
		Last Modified: Wed, 22 Apr 2026 01:31:11 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ccd9fa364a1786b392bac2e6ddd6745d7ce20e23d3d55e5dea7f9550e1299d7`  
		Last Modified: Wed, 22 Apr 2026 01:31:59 GMT  
		Size: 94.9 MB (94884502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2affe866774915b1ac9a46a4e1ac18de29da227b2d5a68bcfd8c3c538e7b7d6`  
		Last Modified: Wed, 22 Apr 2026 01:31:56 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d80b088c9aeb209cf831aef8b763b0ec951fff041e9f33eb8457a075d2631ccb`  
		Last Modified: Wed, 22 Apr 2026 01:31:56 GMT  
		Size: 4.1 MB (4089308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6d32ed0510893abbd91f5e84dca0a9241e463b74e591f0100df6bb9c725623`  
		Last Modified: Wed, 22 Apr 2026 01:31:57 GMT  
		Size: 425.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66c8c0d10e5b9e10c1dd295649dd23ec4b53c92bca9182c071138a5e19d42d9`  
		Last Modified: Wed, 22 Apr 2026 01:31:57 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c21a080db7c5dc718990269dc0f1f41e1ff18d27fefe892e5d28132340c72c9`  
		Last Modified: Wed, 22 Apr 2026 01:31:59 GMT  
		Size: 13.8 MB (13849980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1c211cec5c80e05741841fad4f75d84ce5ae2e3f18171df44c774b5de93330`  
		Last Modified: Wed, 22 Apr 2026 01:31:58 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729daea6a9d1fe569b7a314fda12a22849a3e8fca3f0f6258dfe0b5d8222098d`  
		Last Modified: Wed, 22 Apr 2026 01:31:59 GMT  
		Size: 12.2 MB (12206143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378076dd33dadd4c5e3699bb5f0d22530b9631762f33e38ace0f9ced22b890ed`  
		Last Modified: Wed, 22 Apr 2026 01:31:59 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2380879c990070fe22833595bddb7e02c9b0ee05c886afd7343a6a0f1eff2a`  
		Last Modified: Wed, 22 Apr 2026 01:32:00 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff707614457b67b0eb77d55973fc3d28054243f45091bf9d0997d370f60df5d4`  
		Last Modified: Wed, 22 Apr 2026 01:32:01 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5655cb2fd9ecf9b2f590ce94143aaf2a2b527fbe2489f5b3780216e7ae9c24`  
		Last Modified: Wed, 22 Apr 2026 01:32:01 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3df6bf5821243abf4c4ca65bbd5a23ee06f89e5b458aff38bc03de703cef9eb4`  
		Last Modified: Fri, 01 May 2026 05:54:41 GMT  
		Size: 20.1 MB (20064743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c11a682738544611d5c09ee3b0f14065fe01489edd120f959b361d0ec47049c`  
		Last Modified: Fri, 01 May 2026 05:54:42 GMT  
		Size: 35.0 MB (35036650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e18a811089afc56d5e47e23c6de822c81d3129bd1ab6874040bbbf5af4cfba`  
		Last Modified: Fri, 01 May 2026 05:54:41 GMT  
		Size: 792.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cfcd03034571aab7e9308105f4e297d95b70cbd0d6c74519c59376e83d51d7f`  
		Last Modified: Fri, 01 May 2026 05:54:41 GMT  
		Size: 571.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd36c802646e4a2ada5d86b984bcb770aa9902b256746ded074a38d8287fecd`  
		Last Modified: Fri, 01 May 2026 05:54:42 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3a6fe8f27f9229e870b2bf5f514d1e03ca13f05b45ce42c4d1ff003514af28b`  
		Last Modified: Fri, 01 May 2026 05:54:47 GMT  
		Size: 267.0 MB (266987591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec3f4834664569a121b0412311558ce3b40e48be81bab6573500ad852686e55`  
		Last Modified: Fri, 01 May 2026 05:52:57 GMT  
		Size: 4.1 KB (4136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d1f4fdaabb89a9245d50d3583edee298f7f94b5123727f2cfe010d717ef76a9`  
		Last Modified: Fri, 01 May 2026 05:54:43 GMT  
		Size: 2.4 KB (2415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:latest` - unknown; unknown

```console
$ docker pull nextcloud@sha256:5e6b9e7f2048749b17db5785314ea737719c35cf488cc99eef6a85701ec64e3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.4 KB (64388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f1a09969eae139714016a1ea1e0c27a693318deb73c688809ccd4c4b0974ebe`

```dockerfile
```

-	Layers:
	-	`sha256:5e7f7d5d0a434154c6248ad89a2e58233d54c117d7373e6eb5cfa43d4428687b`  
		Last Modified: Fri, 01 May 2026 05:54:40 GMT  
		Size: 64.4 KB (64388 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:latest` - linux; arm variant v7

```console
$ docker pull nextcloud@sha256:20554b391402c9abc9e5ade1147ee7406e33a247ea3f8c2ee86a9acbefdb68c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **461.3 MB (461317727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91d24a4a1912802e6257359abe47beae1ffae69c1501111487b79503193bb886`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:29:19 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 22 Apr 2026 01:29:37 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Apr 2026 01:29:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:29:37 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Apr 2026 01:29:37 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 22 Apr 2026 01:29:37 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 22 Apr 2026 01:29:37 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 22 Apr 2026 01:29:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 22 Apr 2026 01:29:45 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 22 Apr 2026 01:29:45 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 22 Apr 2026 01:29:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:29:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:29:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Apr 2026 01:29:45 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 22 Apr 2026 01:29:45 GMT
ENV PHP_VERSION=8.4.20
# Wed, 22 Apr 2026 01:29:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 22 Apr 2026 01:29:45 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 22 Apr 2026 01:29:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 01:29:56 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:32:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 01:32:52 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:32:52 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 22 Apr 2026 01:32:53 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 01:32:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 01:32:53 GMT
STOPSIGNAL SIGWINCH
# Wed, 22 Apr 2026 01:32:53 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:32:53 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 01:32:53 GMT
EXPOSE map[80/tcp:{}]
# Wed, 22 Apr 2026 01:32:53 GMT
CMD ["apache2-foreground"]
# Fri, 01 May 2026 05:48:01 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-7.q16-10-extra         rsync     ;     apt-get dist-clean;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Fri, 01 May 2026 05:50:59 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 01 May 2026 05:50:59 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 01 May 2026 05:50:59 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Fri, 01 May 2026 05:50:59 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         liblz4-dev         libmagickwand-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-ftp-ssl;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.28;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.1;     pecl install --configureoptions 'enable-memcached-igbinary="yes"'         memcached-3.4.0;     pecl install --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"'         redis-6.3.0;         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -rt dpkg-query --search         | awk 'sub(":$", "", $1) { print $1 }'         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     apt-get dist-clean # buildkit
# Fri, 01 May 2026 05:50:59 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Fri, 01 May 2026 05:50:59 GMT
VOLUME [/var/www/html]
# Fri, 01 May 2026 05:50:59 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip # buildkit
# Fri, 01 May 2026 05:50:59 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Fri, 01 May 2026 05:51:00 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits # buildkit
# Fri, 01 May 2026 05:51:00 GMT
ENV NEXTCLOUD_VERSION=33.0.3
# Fri, 01 May 2026 05:52:01 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://github.com/nextcloud-releases/server/releases/download/v33.0.3/nextcloud-33.0.3.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://github.com/nextcloud-releases/server/releases/download/v33.0.3/nextcloud-33.0.3.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     apt-get dist-clean # buildkit
# Fri, 01 May 2026 05:52:02 GMT
COPY *.sh upgrade.exclude / # buildkit
# Fri, 01 May 2026 05:52:02 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Fri, 01 May 2026 05:52:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 May 2026 05:52:02 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5106b06fd3c072093bded94807949d02b5d151d8aa469eeb46a006453a7965c5`  
		Last Modified: Wed, 22 Apr 2026 01:33:10 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e355c944c4093dc300ebcdafb3bda8a6c9ec4d565280f4214da78dcb5c72d8e8`  
		Last Modified: Wed, 22 Apr 2026 01:33:14 GMT  
		Size: 86.2 MB (86247520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666a3ee64c140bf6e6df68932390ad89442245fc71e2957dffcd5fd91b5d25c5`  
		Last Modified: Wed, 22 Apr 2026 01:33:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee8490fa290792bd4ae1508b2e69453cf84b93a093779bd2af997a7ac80f5e85`  
		Last Modified: Wed, 22 Apr 2026 01:33:10 GMT  
		Size: 3.8 MB (3757190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19a76912f0330b5a8e70a8fe111b069c3d44062696c997577bb47dd4a4b8b525`  
		Last Modified: Wed, 22 Apr 2026 01:33:12 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40ef1f39e2cbd10d3c21fd5b455d521b8f52edac13cb84361830d0401e056cac`  
		Last Modified: Wed, 22 Apr 2026 01:33:12 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efef0f29c620f3102b1cb37a57abdb740e18afa37345163f546b45b7e315db3`  
		Last Modified: Wed, 22 Apr 2026 01:33:12 GMT  
		Size: 13.9 MB (13850104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178f3b58b928248d5313cea7c2af0b1191a4134e5a2ea89dcefbeee3867e9558`  
		Last Modified: Wed, 22 Apr 2026 01:33:13 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9701abf00c86fb9ba5d35d547ea7424a7005a7054ac5a6a99ac57e7f7b0bfa52`  
		Last Modified: Wed, 22 Apr 2026 01:33:14 GMT  
		Size: 11.6 MB (11617459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1893df0361b2d097c967eb96fb1a8ed66537461ffa47cfaacbd00525053417`  
		Last Modified: Wed, 22 Apr 2026 01:33:14 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9137d5f6e1867a22561c5d4852fe69d4d5871d641401476fa35959cefd60b9`  
		Last Modified: Wed, 22 Apr 2026 01:33:14 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:344333c00c42b7386ac635f2edc6f7eea53ca2fa38185bcfb85c9c47cfccd2f0`  
		Last Modified: Wed, 22 Apr 2026 01:33:15 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d097e3f5dc408f7a2ec0f1811eeef125ae55df101558b0b59f1472f8ccfaa7`  
		Last Modified: Wed, 22 Apr 2026 01:33:15 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d04dcea12a9dfb6729cb544c3a7c4651e347ce515821c14b688958f51112e8fe`  
		Last Modified: Fri, 01 May 2026 05:52:29 GMT  
		Size: 18.0 MB (18005077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc5a13cb9ae9a70ce552e700e9c392b6b257d4e44ecf2c4175bd24d5733071c7`  
		Last Modified: Fri, 01 May 2026 05:52:30 GMT  
		Size: 34.6 MB (34623305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa7b85cf25a572a3550367c1092f9056003604f987ceee5eb84b5792ed4747ae`  
		Last Modified: Fri, 01 May 2026 05:52:29 GMT  
		Size: 790.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48db2fc3a130b114f05242641620483a8e7c150ae0e1c35d6b66a534b5f91f78`  
		Last Modified: Fri, 01 May 2026 05:52:29 GMT  
		Size: 573.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855592f951c01e7801bc66c2aa8b585b58dd8a31f7ebfe3add0982982f8d2ef5`  
		Last Modified: Fri, 01 May 2026 05:52:30 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0860edeaf8e7d83c3c3af8d33af40f4430c11b3aee4c9e5b36f613e4ff80b93d`  
		Last Modified: Fri, 01 May 2026 05:52:35 GMT  
		Size: 267.0 MB (266988194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7056b8630d29efc3798640521563dd7e6555182290d2058f185c5d313c3ec3`  
		Last Modified: Fri, 01 May 2026 05:51:37 GMT  
		Size: 4.1 KB (4136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e37d3ebf6f983f03002f963ef91f9594f31e6da0dc0b01e14d6f37ca0db2068`  
		Last Modified: Fri, 01 May 2026 05:52:31 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:latest` - unknown; unknown

```console
$ docker pull nextcloud@sha256:13a8ab0dd7b8ba20a4e2c6a76107940ba682c487ff090cf6b77c5a2c5d09909d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.4 KB (64388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f39b33484fcb3c645c75c59c726e962bbaf8fc27548e2f64ac9eb61ad2cb148`

```dockerfile
```

-	Layers:
	-	`sha256:92dea3b72765451c82864551a3d499eae05cc39fc99a79336aa4bb40af000d39`  
		Last Modified: Fri, 01 May 2026 05:52:28 GMT  
		Size: 64.4 KB (64388 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:latest` - linux; arm64 variant v8

```console
$ docker pull nextcloud@sha256:7bf11a9bd39ac17b4f4278c97053c0005d6af8be0e1caf19e3eb496821e2c511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **495.2 MB (495157071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ef75f078faa356aa2e3070ae8d1380fd642a1b72faf67094d94110ed5786f64`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:15:27 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 22 Apr 2026 01:15:44 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Apr 2026 01:15:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:15:44 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Apr 2026 01:15:44 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 22 Apr 2026 01:15:44 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 22 Apr 2026 01:15:44 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 22 Apr 2026 01:15:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 22 Apr 2026 01:15:51 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 22 Apr 2026 01:15:51 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 22 Apr 2026 01:15:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:15:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:15:51 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Apr 2026 01:15:51 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 22 Apr 2026 01:15:51 GMT
ENV PHP_VERSION=8.4.20
# Wed, 22 Apr 2026 01:15:51 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 22 Apr 2026 01:15:51 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 22 Apr 2026 01:24:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 01:24:46 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:27:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 01:27:46 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:27:46 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 22 Apr 2026 01:27:46 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 01:27:46 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 01:27:46 GMT
STOPSIGNAL SIGWINCH
# Wed, 22 Apr 2026 01:27:46 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:27:46 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 01:27:46 GMT
EXPOSE map[80/tcp:{}]
# Wed, 22 Apr 2026 01:27:46 GMT
CMD ["apache2-foreground"]
# Fri, 01 May 2026 08:47:10 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-7.q16-10-extra         rsync     ;     apt-get dist-clean;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Fri, 01 May 2026 08:49:44 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 01 May 2026 08:49:44 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 01 May 2026 08:49:44 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Fri, 01 May 2026 08:49:44 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         liblz4-dev         libmagickwand-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-ftp-ssl;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.28;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.1;     pecl install --configureoptions 'enable-memcached-igbinary="yes"'         memcached-3.4.0;     pecl install --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"'         redis-6.3.0;         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -rt dpkg-query --search         | awk 'sub(":$", "", $1) { print $1 }'         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     apt-get dist-clean # buildkit
# Fri, 01 May 2026 08:49:44 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Fri, 01 May 2026 08:49:44 GMT
VOLUME [/var/www/html]
# Fri, 01 May 2026 08:49:44 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip # buildkit
# Fri, 01 May 2026 08:49:44 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Fri, 01 May 2026 08:49:44 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits # buildkit
# Fri, 01 May 2026 08:49:44 GMT
ENV NEXTCLOUD_VERSION=33.0.3
# Fri, 01 May 2026 08:50:19 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://github.com/nextcloud-releases/server/releases/download/v33.0.3/nextcloud-33.0.3.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://github.com/nextcloud-releases/server/releases/download/v33.0.3/nextcloud-33.0.3.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     apt-get dist-clean # buildkit
# Fri, 01 May 2026 08:50:19 GMT
COPY *.sh upgrade.exclude / # buildkit
# Fri, 01 May 2026 08:50:19 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Fri, 01 May 2026 08:50:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 May 2026 08:50:19 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:887e7361c4edf16eb4272307ea2ee57447cf2ec134af0f0326596d3c94a90d7c`  
		Last Modified: Wed, 22 Apr 2026 01:19:35 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b391fd317e2422a2b998a5b8f46476782dda67b0195c064eccf5d895e482ad1b`  
		Last Modified: Wed, 22 Apr 2026 01:19:38 GMT  
		Size: 110.2 MB (110165312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18568485fa5a6e44bf015471b704446b95da6eba7e85f8f6cac1dc351aba16c5`  
		Last Modified: Wed, 22 Apr 2026 01:19:35 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc61f4154b4e36f9f3303c2b5d7cc39748b46c166e3b463351a9e8cd220f168`  
		Last Modified: Wed, 22 Apr 2026 01:19:36 GMT  
		Size: 4.3 MB (4305491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc86735d128f1fbd8106cc32d6afae7a900147daa337150c4739d4f1da4346a`  
		Last Modified: Wed, 22 Apr 2026 01:19:36 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a5795b9e26f314196881b133a91769e53e2828131d098f8db7d9a800b3e89e`  
		Last Modified: Wed, 22 Apr 2026 01:19:36 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5502f96df57cbf4d7939c397fd68491b3e4dc7ff372c63a924fa619428d5ce55`  
		Last Modified: Wed, 22 Apr 2026 01:27:58 GMT  
		Size: 13.9 MB (13852179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c671d94ce0c6c5a51de7fc69370d23707fb0718409f951b587be6798c77cdb`  
		Last Modified: Wed, 22 Apr 2026 01:27:57 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0325d25ee42064c543212ea6c19bbac76a85d4adc1cf6dfcd77fcbd4fe2382b1`  
		Last Modified: Wed, 22 Apr 2026 01:27:58 GMT  
		Size: 13.2 MB (13206146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b47d3caf75cacc27de055e12f70c9488af4a77ec463a8a8803aea30d969715`  
		Last Modified: Wed, 22 Apr 2026 01:27:57 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ab2816bd1e826aae48479663d523550acd969be5b93285569dd982e03a671af`  
		Last Modified: Wed, 22 Apr 2026 01:27:58 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c0f0dbec67a1da7c28e365dadc3da7041014b5b9baf54c270e51e230514fa8`  
		Last Modified: Wed, 22 Apr 2026 01:27:58 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:426e7217b1331d5942ccaacf9df0f007a688d6cc47181ba879aa1f856ac11fcc`  
		Last Modified: Wed, 22 Apr 2026 01:27:59 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe2cc56f6e180e5935d531c8ecf0e5058b82cb3914a08b2397af3afb1757ad6`  
		Last Modified: Fri, 01 May 2026 08:50:47 GMT  
		Size: 19.7 MB (19690574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea89754bee2dd706780edfc2fb9731ad546dea21ef80c3582dae9d1a1b1655a`  
		Last Modified: Fri, 01 May 2026 08:50:48 GMT  
		Size: 36.8 MB (36788312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46f4bbb4099969c25b82e36e653c6e42f8d224901b8d5cb2f5423f2dc161dab0`  
		Last Modified: Fri, 01 May 2026 08:50:47 GMT  
		Size: 793.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9970bef4123754c2d1fa90669dce5c12632f892d9e1d9eb70a6656129d265532`  
		Last Modified: Fri, 01 May 2026 08:50:47 GMT  
		Size: 572.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8295f121b8f52261c14d6ddd99a5687cc77f7ad9faabd1bb91118199e4c51d4c`  
		Last Modified: Fri, 01 May 2026 08:50:48 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e0a349a58b128eaed0aa9b5267851bc1a5f9124e94338ddfb8423418245539`  
		Last Modified: Fri, 01 May 2026 08:50:53 GMT  
		Size: 267.0 MB (266991408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c9266e5023c78dea9725a0b70d49794201492a2ffb32e8cde867189e786ca6`  
		Last Modified: Fri, 01 May 2026 08:50:49 GMT  
		Size: 4.1 KB (4136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b89b0a4eb41d6a9d11606373d82a85e1c28d930943a7a20413b56275801b0f6`  
		Last Modified: Fri, 01 May 2026 08:50:49 GMT  
		Size: 2.4 KB (2415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:latest` - unknown; unknown

```console
$ docker pull nextcloud@sha256:855822b1fe1bfe5b39a89e7cd980398c5189998778ad51af390fb6d94bc07d94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.5 KB (64463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25aa390703a2bd9315805dc603adb1854f57504a81f4b5f7ce1462a812444db7`

```dockerfile
```

-	Layers:
	-	`sha256:cbd647e231566108d7921fd22598c3a687f1ee6a3aa4f407e7a99a3ea4bd60b1`  
		Last Modified: Fri, 01 May 2026 08:50:46 GMT  
		Size: 64.5 KB (64463 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:latest` - linux; 386

```console
$ docker pull nextcloud@sha256:f290734fcbf6caf1ad0c02c914ca63870bd40fb099b0b01d997202f3c67ac7d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **505.1 MB (505123914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f07f204d7e0d2e5b787d32532b3d61206c6a127d436ba838823ab58dab51b28`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:22:00 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 22 Apr 2026 01:22:19 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Apr 2026 01:22:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:22:19 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Apr 2026 01:22:19 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 22 Apr 2026 01:22:19 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 22 Apr 2026 01:22:19 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 22 Apr 2026 01:22:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 22 Apr 2026 01:22:25 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 22 Apr 2026 01:22:25 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 22 Apr 2026 01:22:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:22:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:22:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Apr 2026 01:22:25 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 22 Apr 2026 01:22:25 GMT
ENV PHP_VERSION=8.4.20
# Wed, 22 Apr 2026 01:22:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 22 Apr 2026 01:22:25 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 22 Apr 2026 01:22:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 01:22:36 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:25:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 01:25:34 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:25:34 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 22 Apr 2026 01:25:34 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 01:25:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 01:25:34 GMT
STOPSIGNAL SIGWINCH
# Wed, 22 Apr 2026 01:25:34 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:25:34 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 01:25:34 GMT
EXPOSE map[80/tcp:{}]
# Wed, 22 Apr 2026 01:25:34 GMT
CMD ["apache2-foreground"]
# Fri, 01 May 2026 08:35:58 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-7.q16-10-extra         rsync     ;     apt-get dist-clean;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Fri, 01 May 2026 08:38:19 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 01 May 2026 08:38:19 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 01 May 2026 08:38:19 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Fri, 01 May 2026 08:38:19 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         liblz4-dev         libmagickwand-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-ftp-ssl;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.28;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.1;     pecl install --configureoptions 'enable-memcached-igbinary="yes"'         memcached-3.4.0;     pecl install --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"'         redis-6.3.0;         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -rt dpkg-query --search         | awk 'sub(":$", "", $1) { print $1 }'         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     apt-get dist-clean # buildkit
# Fri, 01 May 2026 08:38:19 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Fri, 01 May 2026 08:38:19 GMT
VOLUME [/var/www/html]
# Fri, 01 May 2026 08:38:19 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip # buildkit
# Fri, 01 May 2026 08:38:19 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Fri, 01 May 2026 08:38:19 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits # buildkit
# Fri, 01 May 2026 08:38:19 GMT
ENV NEXTCLOUD_VERSION=33.0.3
# Fri, 01 May 2026 08:38:55 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://github.com/nextcloud-releases/server/releases/download/v33.0.3/nextcloud-33.0.3.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://github.com/nextcloud-releases/server/releases/download/v33.0.3/nextcloud-33.0.3.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     apt-get dist-clean # buildkit
# Fri, 01 May 2026 08:38:55 GMT
COPY *.sh upgrade.exclude / # buildkit
# Fri, 01 May 2026 08:38:55 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Fri, 01 May 2026 08:38:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 May 2026 08:38:55 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:dacd7cda306bf5bd7a2030f9b0c2e9d71fda44ea58493a33450d210b74a8ec75`  
		Last Modified: Wed, 22 Apr 2026 00:17:04 GMT  
		Size: 31.3 MB (31296327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3ad892368f928cf2c1259fdac7b49dec39b5e0100dc38505086d1f04fb0223`  
		Last Modified: Wed, 22 Apr 2026 01:25:55 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac4a854b9375cf76c04d007410d1b4f9960253c91e039f3fcb12bd3c7da649d1`  
		Last Modified: Wed, 22 Apr 2026 01:25:58 GMT  
		Size: 116.1 MB (116144340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d11b221c038be8eef2d78c984f7ad0d2dc0453d8cdf3bfc51ad75822776b02c5`  
		Last Modified: Wed, 22 Apr 2026 01:25:55 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ea166db99c0aa8459ec40867c9181d68e865592724270ab960b87a59316cef`  
		Last Modified: Wed, 22 Apr 2026 01:25:55 GMT  
		Size: 4.5 MB (4458361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e72ff3928a5ae8b1b558eef86bacf78c1a2d3acee46fe57fbd521c584e8e925`  
		Last Modified: Wed, 22 Apr 2026 01:25:56 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4831e8917f639e8f5338c7edb49dc14aa2d40befe0ab2492f12791411ce60c42`  
		Last Modified: Wed, 22 Apr 2026 01:25:56 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba0ba05e513a80b82c62a1f5983b0933fbd3dfee5e689cea629457ebedbb230`  
		Last Modified: Wed, 22 Apr 2026 01:25:59 GMT  
		Size: 13.9 MB (13851522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ab312dab66ebf333df3271b5f453521908be468732a06d8501f0c05010dcbb`  
		Last Modified: Wed, 22 Apr 2026 01:25:57 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0409a251efd274db5d34c0539ddf36b203537156fff65d0dd99d6206eb755da`  
		Last Modified: Wed, 22 Apr 2026 01:25:58 GMT  
		Size: 13.9 MB (13858390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c38f71c21793b514dafb1af49df5345e3a36057bd995386b1721dad70ae5c1`  
		Last Modified: Wed, 22 Apr 2026 01:25:59 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148e3ac463e003ef2a90ed29684c1fec4adb899f721d8ca37df7bdc97f93e810`  
		Last Modified: Wed, 22 Apr 2026 01:25:59 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6abb31896c1032bcf7ef68bd4c309fec9e010b234c4f1ce7bf73c77d7e652cc4`  
		Last Modified: Wed, 22 Apr 2026 01:26:00 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2e5cc369f5d824ad4e235d2ad3a85a02ecec99498753828309af3d8497942d`  
		Last Modified: Wed, 22 Apr 2026 01:26:00 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7a15fcc66afcb11809b01a6b529632f8143f3cc7a6a8d5e8a2fff2e38ee4ba`  
		Last Modified: Fri, 01 May 2026 08:39:23 GMT  
		Size: 21.2 MB (21215226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9618fbfa494454afd42971dc44ee19b7435ad41a4039dfbd7d55a255a8f2e110`  
		Last Modified: Fri, 01 May 2026 08:39:25 GMT  
		Size: 37.3 MB (37295923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:613784ce7b3456e23169089e1a965f8bfea9625aea1c9333365eb2b63e7fad6c`  
		Last Modified: Fri, 01 May 2026 08:39:22 GMT  
		Size: 790.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f7e8a987b6a67d6ceca475cba37888987155691a9e226df5499f7e094fd091f`  
		Last Modified: Fri, 01 May 2026 08:39:22 GMT  
		Size: 570.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05790ba864808680112f6512cc8f64f2af4e183505b5e28213b93e1e49a3a32b`  
		Last Modified: Fri, 01 May 2026 08:39:23 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291c6268c75f22aea203ef46df7e706c9af9038f0c05747c8a74f115ac894dca`  
		Last Modified: Fri, 01 May 2026 08:39:28 GMT  
		Size: 267.0 MB (266989792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d6476bf8627bedd6d2e19a552c872db2e9780e7d0e93cd16f7f19b28d4f792`  
		Last Modified: Fri, 01 May 2026 08:39:24 GMT  
		Size: 4.1 KB (4136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78757ce2bf1108c04395011e8876f31df53ccc68cdbc6eca30ef54217333566e`  
		Last Modified: Fri, 01 May 2026 08:39:24 GMT  
		Size: 2.4 KB (2412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:latest` - unknown; unknown

```console
$ docker pull nextcloud@sha256:fbea80c742168abcee5304ae5bc69dd7431bfc6747264aac5668b271fce622c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.1 KB (64105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e74ff7d104650c34193389d2ca1339a5013ffde9cdf83382e213fd75480cbba8`

```dockerfile
```

-	Layers:
	-	`sha256:a00cb79680911de4e84464c8cf123406b585bbad4f3c2ae980a73b6895851ac4`  
		Last Modified: Fri, 01 May 2026 08:39:21 GMT  
		Size: 64.1 KB (64105 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:latest` - linux; ppc64le

```console
$ docker pull nextcloud@sha256:691096dc5b31f0dc5f2b916e17d8f8be5a706370c30b9feda168e9c849dd0266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **503.5 MB (503508447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92282f4cb5f53aa4423118df54e37a14a47486d85b150c42aadbf7d6bbe9d3ac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:53:38 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 22 Apr 2026 01:54:50 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Apr 2026 01:54:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:54:50 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Apr 2026 01:54:51 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 22 Apr 2026 01:54:51 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 22 Apr 2026 01:54:51 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 22 Apr 2026 01:55:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 22 Apr 2026 01:55:45 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 22 Apr 2026 01:55:46 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 22 Apr 2026 01:55:46 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:55:46 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:55:46 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Apr 2026 01:55:46 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 22 Apr 2026 01:55:46 GMT
ENV PHP_VERSION=8.4.20
# Wed, 22 Apr 2026 01:55:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 22 Apr 2026 01:55:46 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 22 Apr 2026 02:19:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 02:19:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 02:24:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 02:24:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 02:24:29 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 22 Apr 2026 02:24:29 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 02:24:29 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 02:24:29 GMT
STOPSIGNAL SIGWINCH
# Wed, 22 Apr 2026 02:24:30 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 02:24:30 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 02:24:30 GMT
EXPOSE map[80/tcp:{}]
# Wed, 22 Apr 2026 02:24:30 GMT
CMD ["apache2-foreground"]
# Fri, 01 May 2026 05:57:20 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-7.q16-10-extra         rsync     ;     apt-get dist-clean;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Fri, 01 May 2026 06:02:13 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 01 May 2026 06:02:13 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 01 May 2026 06:02:13 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Fri, 01 May 2026 06:02:13 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         liblz4-dev         libmagickwand-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-ftp-ssl;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.28;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.1;     pecl install --configureoptions 'enable-memcached-igbinary="yes"'         memcached-3.4.0;     pecl install --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"'         redis-6.3.0;         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -rt dpkg-query --search         | awk 'sub(":$", "", $1) { print $1 }'         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     apt-get dist-clean # buildkit
# Fri, 01 May 2026 06:02:13 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Fri, 01 May 2026 06:02:13 GMT
VOLUME [/var/www/html]
# Fri, 01 May 2026 06:02:14 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip # buildkit
# Fri, 01 May 2026 06:02:14 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Fri, 01 May 2026 06:02:14 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits # buildkit
# Fri, 01 May 2026 06:02:14 GMT
ENV NEXTCLOUD_VERSION=33.0.3
# Fri, 01 May 2026 06:04:50 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://github.com/nextcloud-releases/server/releases/download/v33.0.3/nextcloud-33.0.3.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://github.com/nextcloud-releases/server/releases/download/v33.0.3/nextcloud-33.0.3.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     apt-get dist-clean # buildkit
# Fri, 01 May 2026 06:04:51 GMT
COPY *.sh upgrade.exclude / # buildkit
# Fri, 01 May 2026 06:04:52 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Fri, 01 May 2026 06:04:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 May 2026 06:04:52 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:b5fd051d0fcd0789e7358cba300f83befdba943416041497be86050e282a6d02`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 33.6 MB (33598032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec9edacdb8f24d449ea1be53da1f3932bc82a28fd406dd1c8475cd2914e5241`  
		Last Modified: Wed, 22 Apr 2026 01:59:54 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b71f6d43ed1a8d00b3f34912982730d421bfd59fc7192b9463baff89769b29b0`  
		Last Modified: Wed, 22 Apr 2026 01:59:58 GMT  
		Size: 109.6 MB (109599283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673e750ff637e0d2354924e824bffee749521f15eda887d7ff34983e1c535855`  
		Last Modified: Wed, 22 Apr 2026 01:59:54 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab63631568fe36922db06d590c893408dd270fd36872c90416de60627387ddce`  
		Last Modified: Wed, 22 Apr 2026 02:01:32 GMT  
		Size: 4.9 MB (4881692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8438bcf1abed6360e9adac08f804567924b049146c3294914aa102a3f7c41821`  
		Last Modified: Wed, 22 Apr 2026 02:01:32 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5e295926cdc5af3d791955667e4175ebedf05ec97080bd65bd6d11dabf8992`  
		Last Modified: Wed, 22 Apr 2026 02:01:32 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:286ae5221aff2ed1a4a8a4baf4172ad032a7bc332f63f890612205f59604724d`  
		Last Modified: Wed, 22 Apr 2026 02:25:09 GMT  
		Size: 13.9 MB (13851763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67505e93e2a17315b3576e01845784735fd7612b2eba5ee18fb5e1825fc5a4ec`  
		Last Modified: Wed, 22 Apr 2026 02:25:08 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a06c411040503656e63e555235609eca014c8a578020fd6fde25775feb51770f`  
		Last Modified: Wed, 22 Apr 2026 02:25:09 GMT  
		Size: 14.0 MB (13956005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d038fd0dacac84a920cc05f508ee5bb0e0c9d08d1a72f3d96e5f75fe524595`  
		Last Modified: Wed, 22 Apr 2026 02:25:08 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce972e1f08c44df934bf2f5a50d413fa96defc3a3e5af20f6031c30f82275300`  
		Last Modified: Wed, 22 Apr 2026 02:25:09 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c414f8be1c63ac3c42a432d3030e7c783159d103fd4e5ea6b8df58e8ddfab0d`  
		Last Modified: Wed, 22 Apr 2026 02:25:09 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53be4ec9fb48b51715a67384041424d5e3e0e3468e2d9182dc45ad510e144a87`  
		Last Modified: Wed, 22 Apr 2026 02:25:11 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891570a03c25c9dd2bfb7d69d2aecfdf206cd5d34131475fe0ba923ede7b8acc`  
		Last Modified: Fri, 01 May 2026 06:05:44 GMT  
		Size: 22.0 MB (22028767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed2b98a1faf274e6a20541e0ef372866585238e6f6eb56fb6e0f7ec51c5e63a1`  
		Last Modified: Fri, 01 May 2026 06:05:45 GMT  
		Size: 38.6 MB (38587334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c106af2e36dfc57c3252afaf698dcdb0d221098eebea5eac8c53b195cd65e921`  
		Last Modified: Fri, 01 May 2026 06:05:43 GMT  
		Size: 798.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e804e8194339b5b6333968110de0d84ecb1d640516d9ed370b81f65fd58270`  
		Last Modified: Fri, 01 May 2026 06:05:43 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af8662f73dafa661918380f024d4e442f595ebbe672c02d4f0269dccafb5f760`  
		Last Modified: Fri, 01 May 2026 06:05:44 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3293cd11fcdb979895617ea11a201013d94bdc126f8dd78ecdcf49d4102bb03`  
		Last Modified: Fri, 01 May 2026 06:05:50 GMT  
		Size: 267.0 MB (266991500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63cfe228a69fe40485e020021b18e5233d2accef0d87d60279b90b9df01eada`  
		Last Modified: Fri, 01 May 2026 06:05:46 GMT  
		Size: 4.1 KB (4136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e92ae4696b64c6d5316f09a78d97dcf8bdf30e3f33abe4bba8725b28d7963aa4`  
		Last Modified: Fri, 01 May 2026 06:05:46 GMT  
		Size: 2.4 KB (2412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:latest` - unknown; unknown

```console
$ docker pull nextcloud@sha256:45b385a4541d2fe3d3d7fdcd08f4b6970664b2259810acc42cf5af3c3fac02ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.3 KB (64289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ad1b210c7122ad37cef0c9c8eb2b6225d4cc970ad89ac21c83aa64cfc2b8a0c`

```dockerfile
```

-	Layers:
	-	`sha256:f750c9ecf584c946877ab449dbcef9f794a4d109af6ac53208f92722f16e6873`  
		Last Modified: Fri, 01 May 2026 06:05:43 GMT  
		Size: 64.3 KB (64289 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:latest` - linux; riscv64

```console
$ docker pull nextcloud@sha256:a027af19aaddc8fe8c6ba2f872b99ce4b9998a49eae60d277a1f610294b409d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **537.9 MB (537945561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:866e519bd9fb5c1fe3f776c486fa11810adebec4da045145f7938b49179bd6e9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 14:28:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 22 Apr 2026 14:30:21 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Apr 2026 14:30:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 14:30:21 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Apr 2026 14:30:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 22 Apr 2026 14:30:22 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 22 Apr 2026 14:30:22 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 22 Apr 2026 15:35:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 22 Apr 2026 15:35:29 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 22 Apr 2026 15:35:29 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 22 Apr 2026 15:35:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 15:35:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 15:35:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Apr 2026 15:35:29 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 22 Apr 2026 15:35:29 GMT
ENV PHP_VERSION=8.4.20
# Wed, 22 Apr 2026 15:35:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 22 Apr 2026 15:35:29 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 22 Apr 2026 19:36:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 19:36:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 20:31:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 20:31:20 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 20:31:20 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 22 Apr 2026 20:31:21 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 20:31:21 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 20:31:21 GMT
STOPSIGNAL SIGWINCH
# Wed, 22 Apr 2026 20:31:21 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 20:31:21 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 20:31:21 GMT
EXPOSE map[80/tcp:{}]
# Wed, 22 Apr 2026 20:31:21 GMT
CMD ["apache2-foreground"]
# Fri, 01 May 2026 10:06:03 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-7.q16-10-extra         rsync     ;     apt-get dist-clean;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Fri, 01 May 2026 10:35:24 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 01 May 2026 10:35:24 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 01 May 2026 10:35:24 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Fri, 01 May 2026 10:35:24 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         liblz4-dev         libmagickwand-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-ftp-ssl;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.28;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.1;     pecl install --configureoptions 'enable-memcached-igbinary="yes"'         memcached-3.4.0;     pecl install --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"'         redis-6.3.0;         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -rt dpkg-query --search         | awk 'sub(":$", "", $1) { print $1 }'         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     apt-get dist-clean # buildkit
# Fri, 01 May 2026 10:35:25 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Fri, 01 May 2026 10:35:25 GMT
VOLUME [/var/www/html]
# Fri, 01 May 2026 10:35:26 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip # buildkit
# Fri, 01 May 2026 10:35:26 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Fri, 01 May 2026 10:35:26 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits # buildkit
# Fri, 01 May 2026 10:35:26 GMT
ENV NEXTCLOUD_VERSION=33.0.3
# Fri, 01 May 2026 10:39:53 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://github.com/nextcloud-releases/server/releases/download/v33.0.3/nextcloud-33.0.3.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://github.com/nextcloud-releases/server/releases/download/v33.0.3/nextcloud-33.0.3.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     apt-get dist-clean # buildkit
# Fri, 01 May 2026 10:39:55 GMT
COPY *.sh upgrade.exclude / # buildkit
# Fri, 01 May 2026 10:39:55 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Fri, 01 May 2026 10:39:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 May 2026 10:39:55 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48840fceecc8e73012b670476b1f8c5f728f434774a763b7cc1269fce314564f`  
		Last Modified: Wed, 22 Apr 2026 15:33:18 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac60e5404292aec444c5e71111c9196ffd4f75603b3203d43ed8034e0ec9a6c`  
		Last Modified: Wed, 22 Apr 2026 15:33:49 GMT  
		Size: 146.6 MB (146578956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f266893967c3439d4e5dced7f7d20ba4b866ef794fb589fc2b6f367491933e`  
		Last Modified: Wed, 22 Apr 2026 15:33:18 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ace1d1a3fbf428ce3c6cf6c14fe5dbaed0e558761e8a399769f69ff8ec54dc8`  
		Last Modified: Wed, 22 Apr 2026 16:36:05 GMT  
		Size: 4.0 MB (4038663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace8e01b8d5c8675919ea77812b6278a9b6285cfc55c841336c6360438b08577`  
		Last Modified: Wed, 22 Apr 2026 16:36:03 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1b296f62e503f232ec9bc208648e71429d73307711507f18f1133bc6a265b94`  
		Last Modified: Wed, 22 Apr 2026 16:36:03 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b496e7fbae6f2c7c87cdefe87ccd4b681554a851c4d4fc35aa818d036e44e521`  
		Last Modified: Wed, 22 Apr 2026 20:34:31 GMT  
		Size: 13.9 MB (13851734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698e5770e46fc34963913ab63d1ee896a4fa3ca59c1075ce5c5573821a57e523`  
		Last Modified: Wed, 22 Apr 2026 20:34:27 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38106517597fd6b84785512ec188a05729a9ca636c7bdaf993f37aa3f7d193b6`  
		Last Modified: Wed, 22 Apr 2026 20:34:31 GMT  
		Size: 13.0 MB (12980011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:490522e7c530a9b12ed2ab32735abc6197b561e3dd32d9abc04c2778de244d0d`  
		Last Modified: Wed, 22 Apr 2026 20:34:27 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c1fc7f6f68ae3a0dd42fe7885072e26d199668495a55a43a858fa53f69a75f`  
		Last Modified: Wed, 22 Apr 2026 20:34:29 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b846356aaf5d368cec78c462914970b6f64b017dee588582d5fe6d1d8a9b6104`  
		Last Modified: Wed, 22 Apr 2026 20:34:29 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39f868aa6a26a202cd94ad3d51381165454fbf1ce94b558e40ddeb6705ca24e`  
		Last Modified: Wed, 22 Apr 2026 20:34:31 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf510ceefa6c1a3713334d061e910d6415bdf3ffe7eccd362ba6374bd1ddbaf`  
		Last Modified: Fri, 01 May 2026 10:46:32 GMT  
		Size: 19.4 MB (19449801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32ada4cc7b08187c64805616353d7cfddc4beaa77f91c3c005b7d0deda993ef`  
		Last Modified: Fri, 01 May 2026 10:46:39 GMT  
		Size: 45.8 MB (45751833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ff2d7ffadbfe8986cce64a32cd76b72d274fd5534672f06313cdd829869a70`  
		Last Modified: Fri, 01 May 2026 10:46:24 GMT  
		Size: 797.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda00c7e6bb222d4c66dc9a1a8bfa95731bc68b5c020e0f6cb50cdba3f365ca5`  
		Last Modified: Fri, 01 May 2026 10:46:24 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74fec373622ff422fb8ff8ed9c4470f2ae9e27147286804c35daf1b63ea9e65e`  
		Last Modified: Fri, 01 May 2026 10:46:26 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab26a260e4484f40792a6fd6d30e2b8556dea31056f665e9d790aaf34b35736`  
		Last Modified: Fri, 01 May 2026 10:47:12 GMT  
		Size: 267.0 MB (267000246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a57b3f332d5c9000a7d9ce95742b11f2b738791f575941e96d4be02475b4a8`  
		Last Modified: Fri, 01 May 2026 10:46:29 GMT  
		Size: 4.1 KB (4134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5709267525f09ed37f34894a3c44228f8414ac44f6fca0421d647a347cf2de4`  
		Last Modified: Fri, 01 May 2026 10:46:31 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:latest` - unknown; unknown

```console
$ docker pull nextcloud@sha256:979270f6c7e528a395af25dac37d004713bd86b3ad87c0ee2a884eba565bd4ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.3 KB (64289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:092932f643b5b59a5f4c46906a8fa840d3ecf1871bc4dea437ced71c3c61f0c5`

```dockerfile
```

-	Layers:
	-	`sha256:f6c9e1961225ccfb2c649411938f60328d3a207f227f559d0897ed7b7e76c51f`  
		Last Modified: Fri, 01 May 2026 10:46:23 GMT  
		Size: 64.3 KB (64289 bytes)  
		MIME: application/vnd.in-toto+json

### `nextcloud:latest` - linux; s390x

```console
$ docker pull nextcloud@sha256:494df019bc9b1d1bb1f0d9430ca846da48e4625bd00e22a6cdf555efeaee79f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **478.2 MB (478241024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d91741363f16200521de65dceb886f618e66f54de9ade4886f2a4a5f226c9852`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:23:00 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 22 Apr 2026 01:23:19 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Apr 2026 01:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:23:19 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Apr 2026 01:23:19 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 22 Apr 2026 01:23:19 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 22 Apr 2026 01:23:19 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 22 Apr 2026 01:23:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 22 Apr 2026 01:23:27 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 22 Apr 2026 01:23:27 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 22 Apr 2026 01:23:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:23:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:23:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Apr 2026 01:23:27 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 22 Apr 2026 01:23:27 GMT
ENV PHP_VERSION=8.4.20
# Wed, 22 Apr 2026 01:23:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 22 Apr 2026 01:23:27 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 22 Apr 2026 01:34:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 01:34:37 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:37:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 01:37:39 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:37:39 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 22 Apr 2026 01:37:39 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 01:37:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 01:37:39 GMT
STOPSIGNAL SIGWINCH
# Wed, 22 Apr 2026 01:37:39 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:37:39 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 01:37:39 GMT
EXPOSE map[80/tcp:{}]
# Wed, 22 Apr 2026 01:37:39 GMT
CMD ["apache2-foreground"]
# Fri, 01 May 2026 05:44:29 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-7.q16-10-extra         rsync     ;     apt-get dist-clean;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data # buildkit
# Fri, 01 May 2026 05:47:21 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 01 May 2026 05:47:21 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 01 May 2026 05:47:21 GMT
ENV PHP_OPCACHE_MEMORY_CONSUMPTION=128
# Fri, 01 May 2026 05:47:21 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         liblz4-dev         libmagickwand-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-ftp-ssl;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.28;     pecl install igbinary-3.2.16;     pecl install imagick-3.8.1;     pecl install --configureoptions 'enable-memcached-igbinary="yes"'         memcached-3.4.0;     pecl install --configureoptions 'enable-redis-igbinary="yes" enable-redis-zstd="yes" enable-redis-lz4="yes"'         redis-6.3.0;         docker-php-ext-enable         apcu         igbinary         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -rt dpkg-query --search         | awk 'sub(":$", "", $1) { print $1 }'         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     apt-get dist-clean # buildkit
# Fri, 01 May 2026 05:47:21 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=${PHP_OPCACHE_MEMORY_CONSUMPTION}';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=8M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'apc.serializer=igbinary';         echo 'session.serialize_handler=igbinary';     } >> "${PHP_INI_DIR}/conf.d/docker-php-ext-igbinary.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www # buildkit
# Fri, 01 May 2026 05:47:21 GMT
VOLUME [/var/www/html]
# Fri, 01 May 2026 05:47:22 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip # buildkit
# Fri, 01 May 2026 05:47:22 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Fri, 01 May 2026 05:47:22 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits # buildkit
# Fri, 01 May 2026 05:47:22 GMT
ENV NEXTCLOUD_VERSION=33.0.3
# Fri, 01 May 2026 05:48:29 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://github.com/nextcloud-releases/server/releases/download/v33.0.3/nextcloud-33.0.3.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://github.com/nextcloud-releases/server/releases/download/v33.0.3/nextcloud-33.0.3.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     apt-get dist-clean # buildkit
# Fri, 01 May 2026 05:48:30 GMT
COPY *.sh upgrade.exclude / # buildkit
# Fri, 01 May 2026 05:48:30 GMT
COPY config/* /usr/src/nextcloud/config/ # buildkit
# Fri, 01 May 2026 05:48:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 May 2026 05:48:30 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:71574deb335f1e823f938f4a215de00a90d63866898f1f354a0b15e8b9c30577`  
		Last Modified: Wed, 22 Apr 2026 00:17:08 GMT  
		Size: 29.8 MB (29840300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ece9a9560b771b29f91d1b2fa69377a7a6998382890ab15dc4a92ce806048b`  
		Last Modified: Wed, 22 Apr 2026 01:27:53 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ccbb849cf7d524fb26003a40a6f2ddbd73713723d4bf57178fec331c8472df`  
		Last Modified: Wed, 22 Apr 2026 01:27:55 GMT  
		Size: 92.6 MB (92573082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbdb404da573a86ead75a2c55d7c0f8bd69a0480a6e1e9d1e17b114c37703861`  
		Last Modified: Wed, 22 Apr 2026 01:27:52 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7964dc0539da49b7d15124dd7f7170a7706b36795438d37e1b510fef67d922`  
		Last Modified: Wed, 22 Apr 2026 01:27:53 GMT  
		Size: 4.3 MB (4329303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d928c48d6c321d2eeb66c3c389766cf9ae0d3b52927919a0fb9928aa3790f1`  
		Last Modified: Wed, 22 Apr 2026 01:27:53 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:505cc4503afd2ec97db21c3221acd45b9429c93ad112050f26555547d7899269`  
		Last Modified: Wed, 22 Apr 2026 01:27:54 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e7ccf2ac717c82b15002dd84ef1d42b8130bd9336b5ee96c48db314d863c1a`  
		Last Modified: Wed, 22 Apr 2026 01:37:58 GMT  
		Size: 13.9 MB (13850951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d18571a8b1fd3a48f17e0ed57746721b5633a3d9d6fa17bea75e647e5dadb2`  
		Last Modified: Wed, 22 Apr 2026 01:37:58 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4af7cd74da0af1e5075282c2cb414e4d83acaeeb6bd637c46acbf94b5414eaa`  
		Last Modified: Wed, 22 Apr 2026 01:37:59 GMT  
		Size: 13.3 MB (13311877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d5c986b0140b3c1c0aadeb97c7c15b48faacd44db4831ea9d0d2fffab85e97`  
		Last Modified: Wed, 22 Apr 2026 01:37:58 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfd187c896be49dc43ba8e03a8e69c5e53fe53aec2711d75d512f702105a9e6`  
		Last Modified: Wed, 22 Apr 2026 01:37:59 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c1dcabe41bbe8315743a1f135c7e213230ec4c4802210eac62355753a21234`  
		Last Modified: Wed, 22 Apr 2026 01:37:59 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f3b59bcfa40537a6d7da3db395965ad05e8bb13ba9c58d1bd555b7be4cdcd0`  
		Last Modified: Wed, 22 Apr 2026 01:37:59 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc60b4053c6bd163513178586c8478299cfb78e017474daa37954bc2e09ea54c`  
		Last Modified: Fri, 01 May 2026 05:49:06 GMT  
		Size: 20.3 MB (20282131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b310543e0e6f90fc4a4b085a2364ef292514e4ccb92a113d66bbc5a94fdc87`  
		Last Modified: Fri, 01 May 2026 05:49:07 GMT  
		Size: 37.1 MB (37050616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39cc1895f69d877f1aa0eb51e484ba434cce67734d18004cd271861e6989f27a`  
		Last Modified: Fri, 01 May 2026 05:49:06 GMT  
		Size: 790.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb2809401c474074a6b05422bc4ad30f4a4df4f5c4c08a21091fabb98e99c7c`  
		Last Modified: Fri, 01 May 2026 05:49:06 GMT  
		Size: 575.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc84eb53c9ed46af7962f6440a4792b729b91b50ab0d9f7c4c1289b910f235c`  
		Last Modified: Fri, 01 May 2026 05:49:07 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87093924e3f22ea1a885396c556192f3acb4bd23c565c0c336c0dcd259729dc6`  
		Last Modified: Fri, 01 May 2026 05:49:11 GMT  
		Size: 267.0 MB (266988713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ec3a4a851cd5b47a8e584a7ba9f156d97b5cdc5de4db8a4f1ee0eb21fab8057`  
		Last Modified: Fri, 01 May 2026 05:49:07 GMT  
		Size: 4.1 KB (4136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e43a483ea684de0c2287745988fa7821bd201d7109c1bc7b75cda6a9b8c227e`  
		Last Modified: Fri, 01 May 2026 05:49:08 GMT  
		Size: 2.4 KB (2412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nextcloud:latest` - unknown; unknown

```console
$ docker pull nextcloud@sha256:b99457279db36d0c9eb54c9b93f664d8294ebf09f3841d832b93fc34a90a0bb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 KB (64179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d92c720c34495a7d5670133207eb10027c91e3baffc5b411da10920fe161bcc`

```dockerfile
```

-	Layers:
	-	`sha256:217ab3b79f092af7fbc4bfcb33cea3806183a538dcd5556d9b437d5c875ee777`  
		Last Modified: Fri, 01 May 2026 05:49:06 GMT  
		Size: 64.2 KB (64179 bytes)  
		MIME: application/vnd.in-toto+json
