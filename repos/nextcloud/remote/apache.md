## `nextcloud:apache`

```console
$ docker pull nextcloud@sha256:4e5093699a03ce0b2e8d43f1a00a687209db63394e2cd49f1e0851294d9f368f
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

### `nextcloud:apache` - linux; amd64

```console
$ docker pull nextcloud@sha256:a22c962dd5247931975ac73dbc21b1e383a664eda0c892b6ece7188b7fc55c9e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.5 MB (353524718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0360c985567379a4352972575b73e8ccc097525590acb3319106e260b7e876ec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:27 GMT
ADD file:60911afdacfdc216e44115addb5f3cc07f4166e8a4adf7be94a58aacc327ad63 in / 
# Thu, 23 Mar 2023 01:30:27 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 09:31:02 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 23 Mar 2023 09:31:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 23 Mar 2023 09:31:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 09:31:19 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 27 Mar 2023 22:33:07 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Mon, 27 Mar 2023 22:36:30 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 27 Mar 2023 22:36:30 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 27 Mar 2023 22:36:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Mon, 27 Mar 2023 22:36:41 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Mon, 27 Mar 2023 22:36:41 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Mon, 27 Mar 2023 22:36:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 27 Mar 2023 22:36:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 27 Mar 2023 22:36:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 27 Mar 2023 23:26:08 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Mon, 27 Mar 2023 23:26:08 GMT
ENV PHP_VERSION=8.1.17
# Mon, 27 Mar 2023 23:26:08 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.17.tar.xz.asc
# Mon, 27 Mar 2023 23:26:08 GMT
ENV PHP_SHA256=b5c48f95b8e1d8624dd05fc2eab7be13277f9a203ccba97bdca5a1a0fb4a1460
# Mon, 27 Mar 2023 23:26:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 27 Mar 2023 23:26:19 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Mon, 27 Mar 2023 23:29:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Mon, 27 Mar 2023 23:29:12 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Mon, 27 Mar 2023 23:29:13 GMT
RUN docker-php-ext-enable sodium
# Mon, 27 Mar 2023 23:29:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 27 Mar 2023 23:29:13 GMT
STOPSIGNAL SIGWINCH
# Mon, 27 Mar 2023 23:29:13 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Mon, 27 Mar 2023 23:29:13 GMT
WORKDIR /var/www/html
# Mon, 27 Mar 2023 23:29:13 GMT
EXPOSE 80
# Mon, 27 Mar 2023 23:29:13 GMT
CMD ["apache2-foreground"]
# Tue, 28 Mar 2023 04:31:41 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Tue, 28 Mar 2023 04:31:41 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 28 Mar 2023 04:31:41 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 28 Mar 2023 04:44:49 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.22;     pecl install imagick-3.7.0;     pecl install memcached-3.2.0;     pecl install redis-5.3.7;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Tue, 28 Mar 2023 04:44:50 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Tue, 28 Mar 2023 04:44:50 GMT
VOLUME [/var/www/html]
# Tue, 28 Mar 2023 04:44:50 GMT
RUN a2enmod headers rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip
# Tue, 28 Mar 2023 04:44:50 GMT
ENV NEXTCLOUD_VERSION=26.0.0
# Tue, 28 Mar 2023 04:45:38 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Tue, 28 Mar 2023 04:45:40 GMT
COPY multi:38a4739a7ce38db03075117346fff2453db5ff29d27e30f506b9d2fc6a4b4a9a in / 
# Tue, 28 Mar 2023 04:45:40 GMT
COPY multi:5ae4d3e2c333d07b72b698ef5d54be9ec19b520851d7d23aff0a612bc28d533d in /usr/src/nextcloud/config/ 
# Tue, 28 Mar 2023 04:45:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Mar 2023 04:45:40 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:f1f26f5702560b7e591bef5c4d840f76a232bf13fd5aefc4e22077a1ae4440c7`  
		Last Modified: Thu, 23 Mar 2023 01:34:23 GMT  
		Size: 31.4 MB (31411405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee0a4e40ccac1c58f6ca3cf6c0cbb0a5897abd33dee49b641509d5627df02b46`  
		Last Modified: Thu, 23 Mar 2023 10:51:34 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ca9fb408faadb7bf25d58bd66104b2e93e7ba37e961bb24b245abcc09230187`  
		Last Modified: Thu, 23 Mar 2023 10:51:46 GMT  
		Size: 91.6 MB (91636283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25862b797d8786d6655c181772787e4fa6c932aafd6853e429409590e9f6d99b`  
		Last Modified: Tue, 28 Mar 2023 00:51:20 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c128100b25a1cf17b571b5c0c8d316f25c03b14b0315f97302a72713953847a`  
		Last Modified: Tue, 28 Mar 2023 00:52:02 GMT  
		Size: 19.2 MB (19247833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c471030ba37f74280181f8e9174e2e45192728be49c4023d12ea165263852174`  
		Last Modified: Tue, 28 Mar 2023 00:51:59 GMT  
		Size: 471.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285a5ec09eb5e2d43e7ad5c490ed118f537ed46d9be12e573a5fa8aa24632f51`  
		Last Modified: Tue, 28 Mar 2023 00:51:59 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3223d84bfe59cb2dff37372377ac66fdfe790a99f5a87d457a5197b9dda90f3`  
		Last Modified: Tue, 28 Mar 2023 00:57:03 GMT  
		Size: 12.2 MB (12160367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbd1867e192e2831aeb9356e57a63292bd145f2ce08bdc9d905da2dad2304fd4`  
		Last Modified: Tue, 28 Mar 2023 00:57:00 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50aa2f131f8fb1a1db507299feabd53307d0d603c9c524c64007954f8c7a3116`  
		Last Modified: Tue, 28 Mar 2023 00:57:02 GMT  
		Size: 11.1 MB (11051889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8657c361c97237a620853299cdc8bee49687d03283f2ddbdaa1798682fdfa3d`  
		Last Modified: Tue, 28 Mar 2023 00:57:00 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee2a08bc4627d4d9673c56b7874b08354ce3f0c51d8dbf7da3895ddf2bdd4153`  
		Last Modified: Tue, 28 Mar 2023 00:57:00 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35cd0b63238c99d1993779ed0edefd2c9cec3f18616e08100a8a818553f9d6ae`  
		Last Modified: Tue, 28 Mar 2023 00:57:00 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80801b7118d7d78a56b233c6fece6f6d2c44ee45329b8f69f1e0e58ba8e834d7`  
		Last Modified: Tue, 28 Mar 2023 04:54:24 GMT  
		Size: 19.4 MB (19362521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:679409f042f29d42bfbcba3ef912469b2113214a066122c8be18b64c24dbc01a`  
		Last Modified: Tue, 28 Mar 2023 04:56:01 GMT  
		Size: 4.0 MB (4048502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2576e81ad12e38dfe7465e2ed567e35ea627c6ee0a18bc87d042d5c2d506daf3`  
		Last Modified: Tue, 28 Mar 2023 04:55:58 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cc4e2dcea1ba36736998fd205f178756b0a94aa74d8ffabb75750808683a1da`  
		Last Modified: Tue, 28 Mar 2023 04:55:58 GMT  
		Size: 575.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:310ba167d7a500ba53fd8a9cfe1ee9054ad21d6be2d8900efff2cea89fe6519d`  
		Last Modified: Tue, 28 Mar 2023 04:56:18 GMT  
		Size: 164.6 MB (164593884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446f68b9a37d06fc42568c36afdfb43ed8e24b63e2d356089404728b773bdae5`  
		Last Modified: Tue, 28 Mar 2023 04:55:58 GMT  
		Size: 3.1 KB (3056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bef552048a1001dac64c2407c7d7770547aa6a3e9bf5f656e6ff55a0c2df112`  
		Last Modified: Tue, 28 Mar 2023 04:55:58 GMT  
		Size: 2.2 KB (2218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:apache` - linux; arm variant v5

```console
$ docker pull nextcloud@sha256:aa9c3d85cd60e287f077f3aec23dfc057587353ff144c4c7fc84bca257fa0410
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.8 MB (328789886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05546db39b4213edb2b7afbb177fdbbe6aeb2da4b1606c8c47dc5fe36046fe73`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 23 Mar 2023 00:48:44 GMT
ADD file:7595c7bfa6b3741f57a3ec7790e3108bb526244e52bb4a54548b8b5541e66616 in / 
# Thu, 23 Mar 2023 00:48:44 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 04:35:50 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 23 Mar 2023 04:35:50 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 23 Mar 2023 04:36:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 04:36:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 23 Mar 2023 04:36:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 25 Mar 2023 01:22:41 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 25 Mar 2023 01:22:41 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 25 Mar 2023 01:22:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 25 Mar 2023 01:22:55 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 25 Mar 2023 01:22:56 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 25 Mar 2023 01:22:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 25 Mar 2023 01:22:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 25 Mar 2023 01:22:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 25 Mar 2023 01:33:17 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 25 Mar 2023 01:33:17 GMT
ENV PHP_VERSION=8.1.17
# Sat, 25 Mar 2023 01:33:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.17.tar.xz.asc
# Sat, 25 Mar 2023 01:33:18 GMT
ENV PHP_SHA256=b5c48f95b8e1d8624dd05fc2eab7be13277f9a203ccba97bdca5a1a0fb4a1460
# Sat, 25 Mar 2023 01:33:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 25 Mar 2023 01:33:31 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 25 Mar 2023 01:35:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 25 Mar 2023 01:35:51 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Sat, 25 Mar 2023 01:35:51 GMT
RUN docker-php-ext-enable sodium
# Sat, 25 Mar 2023 01:35:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 25 Mar 2023 01:35:51 GMT
STOPSIGNAL SIGWINCH
# Sat, 25 Mar 2023 01:35:51 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Sat, 25 Mar 2023 01:35:51 GMT
WORKDIR /var/www/html
# Sat, 25 Mar 2023 01:35:51 GMT
EXPOSE 80
# Sat, 25 Mar 2023 01:35:52 GMT
CMD ["apache2-foreground"]
# Sat, 25 Mar 2023 08:37:24 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Sat, 25 Mar 2023 08:37:24 GMT
ENV PHP_MEMORY_LIMIT=512M
# Sat, 25 Mar 2023 08:37:24 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Sat, 25 Mar 2023 08:46:48 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.22;     pecl install imagick-3.7.0;     pecl install memcached-3.2.0;     pecl install redis-5.3.7;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Sat, 25 Mar 2023 08:46:48 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Sat, 25 Mar 2023 08:46:49 GMT
VOLUME [/var/www/html]
# Sat, 25 Mar 2023 08:46:49 GMT
RUN a2enmod headers rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip
# Sat, 25 Mar 2023 08:46:49 GMT
ENV NEXTCLOUD_VERSION=26.0.0
# Sat, 25 Mar 2023 08:47:48 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Sat, 25 Mar 2023 08:47:51 GMT
COPY multi:38a4739a7ce38db03075117346fff2453db5ff29d27e30f506b9d2fc6a4b4a9a in / 
# Sat, 25 Mar 2023 08:47:51 GMT
COPY multi:5ae4d3e2c333d07b72b698ef5d54be9ec19b520851d7d23aff0a612bc28d533d in /usr/src/nextcloud/config/ 
# Sat, 25 Mar 2023 08:47:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 25 Mar 2023 08:47:52 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:b83d345710cdef1626d1940689dd3160e5ce3e4f63b3154cf612c52b704baa66`  
		Last Modified: Thu, 23 Mar 2023 02:22:00 GMT  
		Size: 28.9 MB (28915852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca57ccfd8856601954ebd3b2457e5a69c056c4d963ce14194b256a62835cf4bc`  
		Last Modified: Sat, 25 Mar 2023 06:03:15 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e7e09b6251efeda02d5db993f49bbfce41c1b302cbdb1fc9f848c28bae71fd`  
		Last Modified: Sat, 25 Mar 2023 06:03:28 GMT  
		Size: 73.7 MB (73685421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af491393884a4a8cd9d9c39268733f91db98720bcf3b93a04a4cf1b0e7151e42`  
		Last Modified: Sat, 25 Mar 2023 06:03:14 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de589f44ca5cd14dce768c7da899d7a12ac43a792fe5f4ab2e81ee7cee42b2d`  
		Last Modified: Sat, 25 Mar 2023 06:04:11 GMT  
		Size: 18.5 MB (18548395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8881276682c7ecaa254971e8970959f9ce039471fb0506e787230643ce7a64`  
		Last Modified: Sat, 25 Mar 2023 06:04:07 GMT  
		Size: 479.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8533d87b032a0e6314f04fd95fa52f2da27165de282dfeb5f60e974185715c`  
		Last Modified: Sat, 25 Mar 2023 06:04:08 GMT  
		Size: 516.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3100e1f0e892399b54ea5c91c2afbee018b1781400dbcc619e1c9adf14bb7f2c`  
		Last Modified: Sat, 25 Mar 2023 06:05:53 GMT  
		Size: 12.2 MB (12158785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fd552838ba6a839e03c4b7f0a1250ce606a280943b77cb096fe55da958529db`  
		Last Modified: Sat, 25 Mar 2023 06:05:50 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3dafd00f1062ed09d3c456133c3c1df3be55c6733916a76db102a575c16aef6`  
		Last Modified: Sat, 25 Mar 2023 06:05:52 GMT  
		Size: 10.1 MB (10068299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce4eb929edf4b65e36561b0b3e092fb0277b6e405e3259861e3e2a2d77e30800`  
		Last Modified: Sat, 25 Mar 2023 06:05:49 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91291129b2ba2f6233135b8dba136a004ebd9fddfd37e694ed85fea61381c342`  
		Last Modified: Sat, 25 Mar 2023 06:05:49 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4885661df8b3a39a722f436924bb15e72e67f3fed6d58139fb4f3eda5c99263`  
		Last Modified: Sat, 25 Mar 2023 06:05:49 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7044c62ec926f75d924006c3d01a44c266c20542c9fc91657f9a0a5f9cf73757`  
		Last Modified: Sat, 25 Mar 2023 08:52:57 GMT  
		Size: 17.3 MB (17332540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5f8103434ac2ce05ec0db1be581f8af382dd8c9f89afc9cdcdd0701ffef856`  
		Last Modified: Sat, 25 Mar 2023 08:54:33 GMT  
		Size: 3.5 MB (3476536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9287105258eab8a103a348d8cb2c41c0602666936319b61d6d881852311b6e9a`  
		Last Modified: Sat, 25 Mar 2023 08:54:30 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfdaac89fae1083b20a76a7e916cba49d8ef1c398a15d4f667a5edbd0a24ff16`  
		Last Modified: Sat, 25 Mar 2023 08:54:30 GMT  
		Size: 574.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2c64ed9cfd7467e35aab652b22a5bf1d1379e538df4ebc2530a624720ad03e`  
		Last Modified: Sat, 25 Mar 2023 08:54:54 GMT  
		Size: 164.6 MB (164592015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ac2b6cc19b04285aaa0a44fac1baacb84b35aedf2e6006f124272618bba1cb7`  
		Last Modified: Sat, 25 Mar 2023 08:54:30 GMT  
		Size: 3.1 KB (3057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53252b34c6e124e25abb9db02a8ba99e0f22b0740dd82af463b36d54f456dd76`  
		Last Modified: Sat, 25 Mar 2023 08:54:30 GMT  
		Size: 2.2 KB (2216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:apache` - linux; arm variant v7

```console
$ docker pull nextcloud@sha256:ceaa0d81406416f2b3987c4441317958aa7bd5647e06915cd20ab61c3ede4911
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.4 MB (319371227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:381918c00996a356b1136cc0918052fae65433c103c2a97ca0d8978da1a30aaa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 23 Mar 2023 01:16:59 GMT
ADD file:1c83b99ee21091150a1c9ee8ef7c40bec3d6cb0d64b8bc0ef40fb97e6233aa5b in / 
# Thu, 23 Mar 2023 01:17:00 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 09:52:05 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 23 Mar 2023 09:52:05 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 23 Mar 2023 09:52:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 09:52:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 23 Mar 2023 09:52:26 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 23 Mar 2023 09:54:57 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 23 Mar 2023 09:54:57 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 23 Mar 2023 09:55:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 23 Mar 2023 09:55:09 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 23 Mar 2023 09:55:09 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 23 Mar 2023 09:55:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Mar 2023 09:55:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Mar 2023 09:55:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 23 Mar 2023 10:14:48 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 23 Mar 2023 10:14:48 GMT
ENV PHP_VERSION=8.1.17
# Thu, 23 Mar 2023 10:14:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.17.tar.xz.asc
# Thu, 23 Mar 2023 10:14:48 GMT
ENV PHP_SHA256=b5c48f95b8e1d8624dd05fc2eab7be13277f9a203ccba97bdca5a1a0fb4a1460
# Thu, 23 Mar 2023 10:14:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Mar 2023 10:15:00 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Mar 2023 10:17:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 23 Mar 2023 10:17:03 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 23 Mar 2023 10:17:04 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Mar 2023 10:17:04 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Mar 2023 10:17:04 GMT
STOPSIGNAL SIGWINCH
# Thu, 23 Mar 2023 10:17:04 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 23 Mar 2023 10:17:04 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 10:17:04 GMT
EXPOSE 80
# Thu, 23 Mar 2023 10:17:04 GMT
CMD ["apache2-foreground"]
# Thu, 23 Mar 2023 18:40:39 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Thu, 23 Mar 2023 18:40:40 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 23 Mar 2023 18:40:40 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 23 Mar 2023 18:49:19 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.22;     pecl install imagick-3.7.0;     pecl install memcached-3.2.0;     pecl install redis-5.3.7;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 18:49:20 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Thu, 23 Mar 2023 18:49:20 GMT
VOLUME [/var/www/html]
# Thu, 23 Mar 2023 18:49:20 GMT
RUN a2enmod headers rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip
# Thu, 23 Mar 2023 18:49:21 GMT
ENV NEXTCLOUD_VERSION=26.0.0
# Thu, 23 Mar 2023 18:50:19 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 18:50:20 GMT
COPY multi:38a4739a7ce38db03075117346fff2453db5ff29d27e30f506b9d2fc6a4b4a9a in / 
# Thu, 23 Mar 2023 18:50:21 GMT
COPY multi:5ae4d3e2c333d07b72b698ef5d54be9ec19b520851d7d23aff0a612bc28d533d in /usr/src/nextcloud/config/ 
# Thu, 23 Mar 2023 18:50:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Mar 2023 18:50:21 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:2bc24e24d213c286ca4011c8b5cb7a3cf2a51f3bbedee8eeced46382bb5507bc`  
		Last Modified: Thu, 23 Mar 2023 01:33:18 GMT  
		Size: 26.6 MB (26577330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5859d7bd0331fdd3db36460ff2a1ddaaccba37d32aa3dbefd1438b3d6c296aaa`  
		Last Modified: Thu, 23 Mar 2023 10:50:12 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84701bd5e662e452c2d0a2061b7bdb9e457f6d7b3906d4f95854508811c6f3e2`  
		Last Modified: Thu, 23 Mar 2023 10:50:22 GMT  
		Size: 69.3 MB (69321562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a1c39fa5884115ea1e894ce28b8d8d20f2a1cdf23ad91ae04fb9f1ed9ce3297`  
		Last Modified: Thu, 23 Mar 2023 10:50:11 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c132170b343ee67ff7ccd55233891c325b8bc3dc681156240432ccb1556fea`  
		Last Modified: Thu, 23 Mar 2023 10:51:01 GMT  
		Size: 18.0 MB (18007713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf440a3650cbad2d5c9c00ef3930ad0da1f12171c6e12988c9988fbcf59c55c`  
		Last Modified: Thu, 23 Mar 2023 10:50:59 GMT  
		Size: 484.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:899aa2a2b01ac8dfb2816d6c9cc7753d3f54e882d8b21963c32fea6a9bb0b883`  
		Last Modified: Thu, 23 Mar 2023 10:50:59 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52dc2638802c07591f004b7dc83d044d8cd5ae56a0043b2bfcc1b7d80d0e33c1`  
		Last Modified: Thu, 23 Mar 2023 10:54:11 GMT  
		Size: 12.2 MB (12158707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4645df05a937f138605bd19c20e2cebf7483b1386c2419ea402afea11058736`  
		Last Modified: Thu, 23 Mar 2023 10:54:08 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcbd54d0329847435786ddf3a5bf5412b5f11da572fcee1ee1b3522b24e06048`  
		Last Modified: Thu, 23 Mar 2023 10:54:10 GMT  
		Size: 9.5 MB (9539568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dae72039b529aa54de641da05fd65e090430097d75e498e4460bb94cc4f82dd0`  
		Last Modified: Thu, 23 Mar 2023 10:54:08 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeeb259444e981f78ccd64b505aaae6ffa5ee3f4ae8edae7b84787d81a903d2a`  
		Last Modified: Thu, 23 Mar 2023 10:54:08 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf51aedecf9d64442c5e4e4e71fb7f732932942b31937cdf3a8cb71e8476ecc1`  
		Last Modified: Thu, 23 Mar 2023 10:54:08 GMT  
		Size: 889.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5700ffa683f81327dc8e0a608579cc4dbb10a80db2b8eca3511b379eb5981b63`  
		Last Modified: Thu, 23 Mar 2023 18:55:06 GMT  
		Size: 15.8 MB (15784833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9057dbac3eef7246f278c9dd6335783cdffb478be6baa990b0932444da8799ff`  
		Last Modified: Thu, 23 Mar 2023 18:56:41 GMT  
		Size: 3.4 MB (3377471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba475f74968c19b3aa985a2fde9379652fc7091fa299f852afcb4d5a84ba478a`  
		Last Modified: Thu, 23 Mar 2023 18:56:39 GMT  
		Size: 614.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d876cfea6e9838248815f63259acc3d13d6500530e1cfcb2e1b0d939b32adcf3`  
		Last Modified: Thu, 23 Mar 2023 18:56:39 GMT  
		Size: 570.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9edd883e8e4663a31e5667ee78cda8c5ece8a7b8266b0d79b4c863e604ba65fb`  
		Last Modified: Thu, 23 Mar 2023 18:57:04 GMT  
		Size: 164.6 MB (164592029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f8923ab659f9233237a0065e6dba237c76eb745fad5bf62c1486110054f08f8`  
		Last Modified: Thu, 23 Mar 2023 18:56:39 GMT  
		Size: 3.1 KB (3057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:740ffb8c0108586e876170ac658c11e7e80ef69b920734cdbacfef7b39ee3896`  
		Last Modified: Thu, 23 Mar 2023 18:56:39 GMT  
		Size: 2.2 KB (2209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:apache` - linux; arm64 variant v8

```console
$ docker pull nextcloud@sha256:49c4deee365b244c60ddbfb9b7f0d4e94735b3f716ab9cc1c20a7ad2b25d037a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.4 MB (345387437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24fa42762aa0bc881a6715ea3d2ace7b180042788e04e5ea4afa92ba620a9af6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:10 GMT
ADD file:83beb883b699cd442f1dbd4baf29c23f4cd15f7a5f9f120979df16a77455c69f in / 
# Thu, 23 Mar 2023 00:45:10 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 12:12:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 23 Mar 2023 12:12:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 23 Mar 2023 12:12:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 12:12:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 27 Mar 2023 22:59:42 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Mon, 27 Mar 2023 23:02:49 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 27 Mar 2023 23:02:49 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 27 Mar 2023 23:02:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Mon, 27 Mar 2023 23:02:57 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Mon, 27 Mar 2023 23:02:57 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Mon, 27 Mar 2023 23:02:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 27 Mar 2023 23:02:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 27 Mar 2023 23:02:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 27 Mar 2023 23:54:48 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Mon, 27 Mar 2023 23:54:48 GMT
ENV PHP_VERSION=8.1.17
# Mon, 27 Mar 2023 23:54:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.17.tar.xz.asc
# Mon, 27 Mar 2023 23:54:49 GMT
ENV PHP_SHA256=b5c48f95b8e1d8624dd05fc2eab7be13277f9a203ccba97bdca5a1a0fb4a1460
# Mon, 27 Mar 2023 23:54:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 27 Mar 2023 23:54:59 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Mon, 27 Mar 2023 23:57:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Mon, 27 Mar 2023 23:57:50 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Mon, 27 Mar 2023 23:57:50 GMT
RUN docker-php-ext-enable sodium
# Mon, 27 Mar 2023 23:57:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 27 Mar 2023 23:57:50 GMT
STOPSIGNAL SIGWINCH
# Mon, 27 Mar 2023 23:57:50 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Mon, 27 Mar 2023 23:57:50 GMT
WORKDIR /var/www/html
# Mon, 27 Mar 2023 23:57:50 GMT
EXPOSE 80
# Mon, 27 Mar 2023 23:57:50 GMT
CMD ["apache2-foreground"]
# Tue, 28 Mar 2023 03:00:38 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Tue, 28 Mar 2023 03:00:38 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 28 Mar 2023 03:00:38 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 28 Mar 2023 03:14:14 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.22;     pecl install imagick-3.7.0;     pecl install memcached-3.2.0;     pecl install redis-5.3.7;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Tue, 28 Mar 2023 03:14:14 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Tue, 28 Mar 2023 03:14:14 GMT
VOLUME [/var/www/html]
# Tue, 28 Mar 2023 03:14:15 GMT
RUN a2enmod headers rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip
# Tue, 28 Mar 2023 03:14:15 GMT
ENV NEXTCLOUD_VERSION=26.0.0
# Tue, 28 Mar 2023 03:15:01 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Tue, 28 Mar 2023 03:15:05 GMT
COPY multi:38a4739a7ce38db03075117346fff2453db5ff29d27e30f506b9d2fc6a4b4a9a in / 
# Tue, 28 Mar 2023 03:15:05 GMT
COPY multi:5ae4d3e2c333d07b72b698ef5d54be9ec19b520851d7d23aff0a612bc28d533d in /usr/src/nextcloud/config/ 
# Tue, 28 Mar 2023 03:15:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Mar 2023 03:15:06 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:fcdb9667c46b09d1c1d058681ea4a1db41e66bbc1a71d873a0c9da4f7a92947d`  
		Last Modified: Thu, 23 Mar 2023 00:48:09 GMT  
		Size: 30.1 MB (30062700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65bdd3f1135f89f0c6a453b25e0224ee49243ee4c2af5759ee6b592bbf84a11e`  
		Last Modified: Thu, 23 Mar 2023 13:20:28 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:183fcacf85bd0d1bea414ac64e3d6ac2272a67e46b1b296d847900d3126a39fc`  
		Last Modified: Thu, 23 Mar 2023 13:20:37 GMT  
		Size: 86.9 MB (86928489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c19018479f3e7280fbf09f9a84003c15a8cdd69eab5d36617ed4ab96196eef`  
		Last Modified: Tue, 28 Mar 2023 01:08:44 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f5f780e80a182a1a1ce556d8f64736ed58b824b8b811fe7165fa2ba0aaa8e1`  
		Last Modified: Tue, 28 Mar 2023 01:09:27 GMT  
		Size: 19.2 MB (19170041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0e926cb069f4983873645f7c6aa9a2d2239194f0e98c2089a70383eb409707a`  
		Last Modified: Tue, 28 Mar 2023 01:09:24 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bd87af51c0299565f8470a6828973cea6058cd68e5a3aa842be7df652d6bf15`  
		Last Modified: Tue, 28 Mar 2023 01:09:24 GMT  
		Size: 515.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8793bf32bd785c71366f5d9ecb61b28b7f705b7a8af00b0c59a7e62a83477af6`  
		Last Modified: Tue, 28 Mar 2023 01:14:24 GMT  
		Size: 12.2 MB (12159646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec8c6e8d7177bbd11b27bd2e157cdbf17fa242a53bd0280f1cb44c2a37570bf`  
		Last Modified: Tue, 28 Mar 2023 01:14:21 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b5af7a3c88f80a20e13301b43c498cf2010b635cb90a95b98d18495b0b1a0f`  
		Last Modified: Tue, 28 Mar 2023 01:14:23 GMT  
		Size: 11.1 MB (11118189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ea7e08375c74461edb5f4147f7c754c60b00686940480aeec627c1d47bd94b`  
		Last Modified: Tue, 28 Mar 2023 01:14:21 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283fc8aa67c0928161ad7def0fe924108c4a6fc32e74f8a117d1fb127f69dd3f`  
		Last Modified: Tue, 28 Mar 2023 01:14:21 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d05668607728ba3612a343c9c9e577ec083a497726e7cb660739c18b5e09cca`  
		Last Modified: Tue, 28 Mar 2023 01:14:21 GMT  
		Size: 892.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bd7112c57121e9ae3b088d3a271c79ae3ed848517674886c48ce62eb5d69284`  
		Last Modified: Tue, 28 Mar 2023 03:23:50 GMT  
		Size: 17.1 MB (17074118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22c7147e606bf10e4d26e0607500b799c615936cabd7ef9c18d8da6e1b6216ee`  
		Last Modified: Tue, 28 Mar 2023 03:25:17 GMT  
		Size: 4.3 MB (4269072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c00e9fa45fba01c04485718d6e9b461ff0b3657158dae9200e3bbec4bb511d1b`  
		Last Modified: Tue, 28 Mar 2023 03:25:14 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160efa5f817c19ace35fa489ccd84c959b1601ee8d9d37799be82f7d44f553e1`  
		Last Modified: Tue, 28 Mar 2023 03:25:14 GMT  
		Size: 573.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eee7217ba57037bc23fc563bd0f25850d7edcb92d52e6cf0dd7004ff6227447`  
		Last Modified: Tue, 28 Mar 2023 03:25:30 GMT  
		Size: 164.6 MB (164593146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2c114055cc99aee8710f5d05e760d77e9002bbcb3cc8f6a70229b59e5e97064`  
		Last Modified: Tue, 28 Mar 2023 03:25:14 GMT  
		Size: 3.1 KB (3058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:479d30c0abf9ca1370981923044e2ae69c0cd6ac588bfabeb3bd014f4ec1bb3e`  
		Last Modified: Tue, 28 Mar 2023 03:25:14 GMT  
		Size: 2.2 KB (2215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:apache` - linux; 386

```console
$ docker pull nextcloud@sha256:4c1fe999eccf8ec672ca8f8f250497486a19b094bd33ced2f9a4bbe1f03e3d75
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.9 MB (355859324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecf550738bc0baf42edbe4962743eab84ee39f5caa9baf25f2c58cfdcef2a4c0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 23 Mar 2023 00:39:18 GMT
ADD file:315d843eefd4a8bb2345366dcd6bab00a06fca4a7970e220ae8946123d07d7ed in / 
# Thu, 23 Mar 2023 00:39:19 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 08:48:38 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 23 Mar 2023 08:48:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 23 Mar 2023 08:49:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 08:49:02 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 27 Mar 2023 22:40:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Mon, 27 Mar 2023 22:45:47 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 27 Mar 2023 22:45:47 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 27 Mar 2023 22:45:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Mon, 27 Mar 2023 22:45:58 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Mon, 27 Mar 2023 22:45:58 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Mon, 27 Mar 2023 22:45:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 27 Mar 2023 22:45:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 27 Mar 2023 22:45:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 28 Mar 2023 00:07:49 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 28 Mar 2023 00:07:49 GMT
ENV PHP_VERSION=8.1.17
# Tue, 28 Mar 2023 00:07:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.17.tar.xz.asc
# Tue, 28 Mar 2023 00:07:49 GMT
ENV PHP_SHA256=b5c48f95b8e1d8624dd05fc2eab7be13277f9a203ccba97bdca5a1a0fb4a1460
# Tue, 28 Mar 2023 00:08:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 28 Mar 2023 00:08:02 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 28 Mar 2023 00:12:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 28 Mar 2023 00:12:50 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 28 Mar 2023 00:12:51 GMT
RUN docker-php-ext-enable sodium
# Tue, 28 Mar 2023 00:12:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 28 Mar 2023 00:12:51 GMT
STOPSIGNAL SIGWINCH
# Tue, 28 Mar 2023 00:12:51 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 28 Mar 2023 00:12:51 GMT
WORKDIR /var/www/html
# Tue, 28 Mar 2023 00:12:51 GMT
EXPOSE 80
# Tue, 28 Mar 2023 00:12:51 GMT
CMD ["apache2-foreground"]
# Tue, 28 Mar 2023 03:59:54 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Tue, 28 Mar 2023 03:59:54 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 28 Mar 2023 03:59:54 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 28 Mar 2023 04:15:03 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.22;     pecl install imagick-3.7.0;     pecl install memcached-3.2.0;     pecl install redis-5.3.7;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Tue, 28 Mar 2023 04:15:04 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Tue, 28 Mar 2023 04:15:04 GMT
VOLUME [/var/www/html]
# Tue, 28 Mar 2023 04:15:05 GMT
RUN a2enmod headers rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip
# Tue, 28 Mar 2023 04:15:05 GMT
ENV NEXTCLOUD_VERSION=26.0.0
# Tue, 28 Mar 2023 04:16:03 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Tue, 28 Mar 2023 04:16:07 GMT
COPY multi:38a4739a7ce38db03075117346fff2453db5ff29d27e30f506b9d2fc6a4b4a9a in / 
# Tue, 28 Mar 2023 04:16:08 GMT
COPY multi:5ae4d3e2c333d07b72b698ef5d54be9ec19b520851d7d23aff0a612bc28d533d in /usr/src/nextcloud/config/ 
# Tue, 28 Mar 2023 04:16:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Mar 2023 04:16:08 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:3e638a975ea99fe8646002726dcb1ccdccc49ad33967b30337b9b2413e0619b5`  
		Last Modified: Thu, 23 Mar 2023 00:43:09 GMT  
		Size: 32.4 MB (32396277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06aa6a41a038993b857528270326d42c797e0a981b2766ad831ae3df77110f1b`  
		Last Modified: Thu, 23 Mar 2023 10:50:14 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2e6018ce44943ea0d18b41430c9f4e71fbdf0256d6d048e01fc4b488e3dcb3c`  
		Last Modified: Thu, 23 Mar 2023 10:50:33 GMT  
		Size: 92.7 MB (92720414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9b403e42a4f652ad3a0d3a5a14c26ec7754b08b9a682399215f0820684474b9`  
		Last Modified: Tue, 28 Mar 2023 02:25:08 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40b0f7da47cf2fc993777c07da3fdea1609c867a66ba38703a3fd8485a236605`  
		Last Modified: Tue, 28 Mar 2023 02:25:56 GMT  
		Size: 19.7 MB (19737065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8456dbc544f338a5902dcbf530bfa28580898cc2ed3d0dc7fb3e23dfe7ff7c83`  
		Last Modified: Tue, 28 Mar 2023 02:25:52 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bddc2ad7973999bab2938f826d5fb20cea29ee74dcef96c9dee110823226f767`  
		Last Modified: Tue, 28 Mar 2023 02:25:52 GMT  
		Size: 511.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:394fd16eef9a144eaa9d973515de51bff63e1afa6111956bd3e11d9a440197be`  
		Last Modified: Tue, 28 Mar 2023 02:31:25 GMT  
		Size: 12.2 MB (12159673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:384d690298fb2885885886cc71c7b74dce9764d8851854437ec6c1e81ac02adf`  
		Last Modified: Tue, 28 Mar 2023 02:31:22 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e4e340a7c234778f90e5af0e1d5fd4dabc1832df986ee6a2e1f4088d0c3eaf7`  
		Last Modified: Tue, 28 Mar 2023 02:31:25 GMT  
		Size: 11.3 MB (11279072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66005bbaf9aee7d8c984ac194d2496fe062a5e17fbd8223be3f8dc259d34dff`  
		Last Modified: Tue, 28 Mar 2023 02:31:22 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8325efb2a7ba128f0f56fd3e935b69eb5f119320f8337d1a586648b73268e731`  
		Last Modified: Tue, 28 Mar 2023 02:31:22 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ea32c5f2a98f156342dcb4a1cc83c2799e40afad01eae57a67982a25c10492`  
		Last Modified: Tue, 28 Mar 2023 02:31:22 GMT  
		Size: 897.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be572ecc02c90e84cad2630e914a305058c2b3d131280823607a347870409144`  
		Last Modified: Tue, 28 Mar 2023 04:26:20 GMT  
		Size: 19.0 MB (18962489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:581621da1ebf895e820aa8e0cfdc0d433746cb813670c4a9d6a1cdc94112b3df`  
		Last Modified: Tue, 28 Mar 2023 04:28:30 GMT  
		Size: 4.0 MB (3999035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b1b11d7f4b27f4acd6d6c15f91ddd099a1e4c9f737839d18edd744aaf84b872`  
		Last Modified: Tue, 28 Mar 2023 04:28:27 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce84dee3d82343f82f088fca566a791698d942ac23824f5666fb16141556cb2c`  
		Last Modified: Tue, 28 Mar 2023 04:28:27 GMT  
		Size: 574.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db1f9557edc4f9e3cdbbd3625e0d299e5ec0273992f5443bfb5cda066a8bb6e`  
		Last Modified: Tue, 28 Mar 2023 04:28:56 GMT  
		Size: 164.6 MB (164593260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:480e5e7e4d6394efeeaeec5814ed1efd582fcb9586c581cca8a9523a272a672b`  
		Last Modified: Tue, 28 Mar 2023 04:28:27 GMT  
		Size: 3.1 KB (3058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe2e474314973e563cc5ff182f5095ff250a63e526de34a249d8eb64dd05413`  
		Last Modified: Tue, 28 Mar 2023 04:28:27 GMT  
		Size: 2.2 KB (2213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:apache` - linux; mips64le

```console
$ docker pull nextcloud@sha256:a6ab84a5f0c038aa4edbb40993db32e3ec19165196344bd284cbea7f23ea1c9a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.4 MB (327437430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be1ce81d0c84148b211ecfe7d5855e5cebd223947ef0b3ed3a11cd14e6d117cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 23 Mar 2023 05:17:57 GMT
ADD file:fd3a8eec4ae8f6058f522536ca9af1b391f3032504c085d8ddb6f4878ca478d5 in / 
# Thu, 23 Mar 2023 05:18:02 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 20:46:36 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 23 Mar 2023 20:46:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 23 Mar 2023 20:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 20:48:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 27 Mar 2023 22:09:30 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Mon, 27 Mar 2023 22:24:31 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 27 Mar 2023 22:24:34 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 27 Mar 2023 22:25:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Mon, 27 Mar 2023 22:25:34 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Mon, 27 Mar 2023 22:25:40 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Mon, 27 Mar 2023 22:25:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 27 Mar 2023 22:25:47 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 27 Mar 2023 22:25:50 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 27 Mar 2023 23:23:19 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Mon, 27 Mar 2023 23:23:23 GMT
ENV PHP_VERSION=8.1.17
# Mon, 27 Mar 2023 23:23:26 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.17.tar.xz.asc
# Mon, 27 Mar 2023 23:23:30 GMT
ENV PHP_SHA256=b5c48f95b8e1d8624dd05fc2eab7be13277f9a203ccba97bdca5a1a0fb4a1460
# Mon, 27 Mar 2023 23:24:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 27 Mar 2023 23:24:20 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Mon, 27 Mar 2023 23:37:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Mon, 27 Mar 2023 23:38:02 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Mon, 27 Mar 2023 23:38:09 GMT
RUN docker-php-ext-enable sodium
# Mon, 27 Mar 2023 23:38:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 27 Mar 2023 23:38:16 GMT
STOPSIGNAL SIGWINCH
# Mon, 27 Mar 2023 23:38:19 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Mon, 27 Mar 2023 23:38:23 GMT
WORKDIR /var/www/html
# Mon, 27 Mar 2023 23:38:27 GMT
EXPOSE 80
# Mon, 27 Mar 2023 23:38:30 GMT
CMD ["apache2-foreground"]
# Tue, 28 Mar 2023 05:26:18 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Tue, 28 Mar 2023 05:26:22 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 28 Mar 2023 05:26:25 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 28 Mar 2023 06:05:41 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.22;     pecl install imagick-3.7.0;     pecl install memcached-3.2.0;     pecl install redis-5.3.7;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Tue, 28 Mar 2023 06:05:47 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Tue, 28 Mar 2023 06:05:51 GMT
VOLUME [/var/www/html]
# Tue, 28 Mar 2023 06:05:57 GMT
RUN a2enmod headers rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip
# Tue, 28 Mar 2023 06:06:01 GMT
ENV NEXTCLOUD_VERSION=26.0.0
# Tue, 28 Mar 2023 06:08:52 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Tue, 28 Mar 2023 06:09:03 GMT
COPY multi:38a4739a7ce38db03075117346fff2453db5ff29d27e30f506b9d2fc6a4b4a9a in / 
# Tue, 28 Mar 2023 06:09:13 GMT
COPY multi:5ae4d3e2c333d07b72b698ef5d54be9ec19b520851d7d23aff0a612bc28d533d in /usr/src/nextcloud/config/ 
# Tue, 28 Mar 2023 06:09:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Mar 2023 06:09:30 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:735f9e60414e17ec59baef702f7013b7327899801df2ecf10123ce2727d8dea5`  
		Last Modified: Thu, 23 Mar 2023 05:25:53 GMT  
		Size: 29.6 MB (29634483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdaed7fbf45d20bf0dcaf24949531440ccb33b76239b932e0caa3f080e337c11`  
		Last Modified: Tue, 28 Mar 2023 01:02:19 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:303aa2a4dd7ba9f132f3f0a45fcc1c3ac0c712e946516555e7b75dd61e41da28`  
		Last Modified: Tue, 28 Mar 2023 01:03:10 GMT  
		Size: 71.8 MB (71814424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877c805149e9b40916c02cf22d8b5e6c77e471e4f0d03ec38b647980d5f0c10d`  
		Last Modified: Tue, 28 Mar 2023 01:02:19 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b76d3e7de1b5fe0c26def6bf2da72ca9f3aed76989cff0880613e60930bd822`  
		Last Modified: Tue, 28 Mar 2023 01:04:06 GMT  
		Size: 18.9 MB (18946932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c0cca9b8642c98734e2c49cb1649f0c4ac27255b2b2500a3344a2c077bcb28`  
		Last Modified: Tue, 28 Mar 2023 01:03:54 GMT  
		Size: 437.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeeabc4ff238327e980134334ce86530be50279626dd10fe63441e6b8c046887`  
		Last Modified: Tue, 28 Mar 2023 01:03:54 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1ca2e00c00e6cd50a4991f7541f34b9b28422df5f8df6e181349535307284ef`  
		Last Modified: Tue, 28 Mar 2023 01:06:40 GMT  
		Size: 11.9 MB (11941972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:717a457e6f1e66759889c09f7154c1ad890a008789e6726f931ffcd9af40bc2f`  
		Last Modified: Tue, 28 Mar 2023 01:06:34 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9d16cc457bb30604c5070c6c41265b78426076263f1ffde8f10de89c0849f97`  
		Last Modified: Tue, 28 Mar 2023 01:06:42 GMT  
		Size: 10.2 MB (10198099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83ee57631e7d244858034f274d47afa2a5bb9f1a90c817d7664f7e99e7b59298`  
		Last Modified: Tue, 28 Mar 2023 01:06:34 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b388f7e8ff396f9fafdac31b59ea392f4cf68aee77d4e7ef79293aeb6282006`  
		Last Modified: Tue, 28 Mar 2023 01:06:34 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:241c05e302538050c9d777f91bcd87e468a16941b204a6a4ed59d05c28b11c6b`  
		Last Modified: Tue, 28 Mar 2023 01:06:34 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:057cc07e75894812a7d215b12bb528bec0efbdcaa017808a7dcc83e8946d3315`  
		Last Modified: Tue, 28 Mar 2023 06:27:39 GMT  
		Size: 17.2 MB (17187692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f2b820712304b33bb687aeaf478ee7ae67c0763d10946910d1d3d90bb42ef6`  
		Last Modified: Tue, 28 Mar 2023 06:31:31 GMT  
		Size: 3.4 MB (3360296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc968dc665dcbb657a21ce4fbd49ace99a4f1747ef5f5d998cc784486c0e17db`  
		Last Modified: Tue, 28 Mar 2023 06:31:24 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbeb96344037c8eb6f94c3b99d263269383b7e431219b671c57a745c065e7b49`  
		Last Modified: Tue, 28 Mar 2023 06:31:24 GMT  
		Size: 580.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be815dde777d273997ab65bcbecb07b05f0440d710aefea57be5eb2bec4c7954`  
		Last Modified: Tue, 28 Mar 2023 06:33:06 GMT  
		Size: 164.3 MB (164341606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfc9c06264defe9fb545ff3a8b9a96a793c0753860ac3179bf474b4a37ed34a4`  
		Last Modified: Tue, 28 Mar 2023 06:31:24 GMT  
		Size: 3.1 KB (3057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc974b1720d79d290337d7ccc57f2b19b0f9edc066e9402d9c2b59facb0288a`  
		Last Modified: Tue, 28 Mar 2023 06:31:24 GMT  
		Size: 2.2 KB (2221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:apache` - linux; ppc64le

```console
$ docker pull nextcloud@sha256:e2aa657a7a4e538b9c7084a4918754531fe0da3963424d410044eaee2c76e160
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.0 MB (353997074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:520218d0c9f8e8894a616944743dd32db88c44b80130f6f578ef321ce7c67db5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 23 Mar 2023 01:19:48 GMT
ADD file:fbd36b7667327dd30171fc49b8e028b8371fdbc7d30ee673808d508557f78bf1 in / 
# Thu, 23 Mar 2023 01:19:49 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 11:16:43 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 23 Mar 2023 11:16:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 23 Mar 2023 11:17:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 11:17:26 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 27 Mar 2023 22:30:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Mon, 27 Mar 2023 22:36:03 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 27 Mar 2023 22:36:04 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 27 Mar 2023 22:36:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Mon, 27 Mar 2023 22:36:37 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Mon, 27 Mar 2023 22:36:38 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Mon, 27 Mar 2023 22:36:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 27 Mar 2023 22:36:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 27 Mar 2023 22:36:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 27 Mar 2023 23:25:40 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Mon, 27 Mar 2023 23:25:40 GMT
ENV PHP_VERSION=8.1.17
# Mon, 27 Mar 2023 23:25:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.17.tar.xz.asc
# Mon, 27 Mar 2023 23:25:40 GMT
ENV PHP_SHA256=b5c48f95b8e1d8624dd05fc2eab7be13277f9a203ccba97bdca5a1a0fb4a1460
# Mon, 27 Mar 2023 23:26:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 27 Mar 2023 23:26:02 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Mon, 27 Mar 2023 23:30:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Mon, 27 Mar 2023 23:30:03 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Mon, 27 Mar 2023 23:30:04 GMT
RUN docker-php-ext-enable sodium
# Mon, 27 Mar 2023 23:30:05 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 27 Mar 2023 23:30:05 GMT
STOPSIGNAL SIGWINCH
# Mon, 27 Mar 2023 23:30:05 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Mon, 27 Mar 2023 23:30:05 GMT
WORKDIR /var/www/html
# Mon, 27 Mar 2023 23:30:06 GMT
EXPOSE 80
# Mon, 27 Mar 2023 23:30:06 GMT
CMD ["apache2-foreground"]
# Tue, 28 Mar 2023 05:27:27 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Tue, 28 Mar 2023 05:27:28 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 28 Mar 2023 05:27:29 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 28 Mar 2023 05:49:09 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.22;     pecl install imagick-3.7.0;     pecl install memcached-3.2.0;     pecl install redis-5.3.7;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Tue, 28 Mar 2023 05:49:10 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Tue, 28 Mar 2023 05:49:10 GMT
VOLUME [/var/www/html]
# Tue, 28 Mar 2023 05:49:11 GMT
RUN a2enmod headers rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip
# Tue, 28 Mar 2023 05:49:12 GMT
ENV NEXTCLOUD_VERSION=26.0.0
# Tue, 28 Mar 2023 05:50:24 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Tue, 28 Mar 2023 05:50:33 GMT
COPY multi:38a4739a7ce38db03075117346fff2453db5ff29d27e30f506b9d2fc6a4b4a9a in / 
# Tue, 28 Mar 2023 05:50:33 GMT
COPY multi:5ae4d3e2c333d07b72b698ef5d54be9ec19b520851d7d23aff0a612bc28d533d in /usr/src/nextcloud/config/ 
# Tue, 28 Mar 2023 05:50:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Mar 2023 05:50:34 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:8f472ad0a3fa58b4e304d1a974f25615d5bd3b7a99dff9c8202bd30facef0155`  
		Last Modified: Thu, 23 Mar 2023 01:24:22 GMT  
		Size: 35.3 MB (35288050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5512e0497df21360191b849f72d51f7703c3bd5d51e3a86e99f5f29e75c133f1`  
		Last Modified: Thu, 23 Mar 2023 12:17:14 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62cd33d778b1f35bc7aba19bc6c01a581af85ccbdf01838e9cc40a2acb4da1e8`  
		Last Modified: Thu, 23 Mar 2023 12:17:36 GMT  
		Size: 86.6 MB (86632853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f90b7c47f5163af25830b86afe3a61c91bf54c82e24fabb73932f775777313aa`  
		Last Modified: Tue, 28 Mar 2023 00:39:24 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3813e33ceba2822cebad8a55186e17e52c37dc98f131d69ed84daf710cc9c5`  
		Last Modified: Tue, 28 Mar 2023 00:40:20 GMT  
		Size: 20.5 MB (20464031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7aa3d186f11f473d7cb7e8b38a24f4a1c83c2e9f68d2d13abe8ec1bce9a4dae`  
		Last Modified: Tue, 28 Mar 2023 00:40:14 GMT  
		Size: 480.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419ecfb0060dde1a708439075d5653353f3de3d58ae2c99d7b68937aa1b3c4ce`  
		Last Modified: Tue, 28 Mar 2023 00:40:14 GMT  
		Size: 517.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3846021368b8476abc4ac9d728d083c4fda37d960b79805afce6c1a4c2f654c`  
		Last Modified: Tue, 28 Mar 2023 00:45:05 GMT  
		Size: 12.2 MB (12160246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f60af8db14291cd3ae1c1222cb92f72ac330853e1831bae5b5220806963dcba1`  
		Last Modified: Tue, 28 Mar 2023 00:45:01 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd07026cda9c703dfa763dc983d972ed5193923b0e4f89e65f4fb8a34f03a0d2`  
		Last Modified: Tue, 28 Mar 2023 00:45:05 GMT  
		Size: 11.4 MB (11448852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b79ba4a35b08c95971c5699c466af2316767b27c9b01dbb4612cad21fa3d5b`  
		Last Modified: Tue, 28 Mar 2023 00:45:01 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a48633be68a62b3cc6897f815666854200853bee6e230eb4070a22a853f4777`  
		Last Modified: Tue, 28 Mar 2023 00:45:01 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18d1b0298b25808342ca3125353af4e8587fca1c9a48d43ac0bda211ac3bdab8`  
		Last Modified: Tue, 28 Mar 2023 00:45:01 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b9df5da40afea5faf088a436d0071e6119d7b9448914c88ae905c9cc881bb4`  
		Last Modified: Tue, 28 Mar 2023 06:07:04 GMT  
		Size: 19.5 MB (19533608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:180737e2c92bc85690f9415e90e050f70033cdd622be85270d7a6d20ff27973e`  
		Last Modified: Tue, 28 Mar 2023 06:09:33 GMT  
		Size: 3.9 MB (3862860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698ad8b60e8696734afb518f558c29be1203b52d5256ce4c9fa757b00507101f`  
		Last Modified: Tue, 28 Mar 2023 06:09:30 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976d6ee5b82f1843722f2d299d51c222ba5e25df6e5300304035cb6b8ce2d691`  
		Last Modified: Tue, 28 Mar 2023 06:09:30 GMT  
		Size: 580.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9902cf594f4f806b1fce4f9987850e1f1af7d0012419a92d2097e106623cc905`  
		Last Modified: Tue, 28 Mar 2023 06:10:05 GMT  
		Size: 164.6 MB (164594515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94f5c696bce78b5116140dc9926bbd8bff8f7625252f784c7d54f89e842ffb9a`  
		Last Modified: Tue, 28 Mar 2023 06:09:30 GMT  
		Size: 3.1 KB (3058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e467f92a95239589e102fbf6a077650dd7d2b6481822cc19372b0a1b014776`  
		Last Modified: Tue, 28 Mar 2023 06:09:30 GMT  
		Size: 2.2 KB (2216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:apache` - linux; s390x

```console
$ docker pull nextcloud@sha256:e2590cc3b0585bba1298193052595290d1232c347e212c04a65cd1de5a0621e9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.0 MB (328010429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36257c7efe112d730c3cd855dee2b9ce6263c14eb8cd45183655aa7e0617f413`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 23 Mar 2023 00:44:06 GMT
ADD file:8b6d3f57adaa8af2e0599a6468c50b713d281165b4e61150850bedf587f7ad4f in / 
# Thu, 23 Mar 2023 00:44:08 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 08:34:52 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 23 Mar 2023 08:34:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 23 Mar 2023 08:35:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 08:35:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 27 Mar 2023 22:45:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Mon, 27 Mar 2023 22:48:20 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 27 Mar 2023 22:48:20 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 27 Mar 2023 22:48:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Mon, 27 Mar 2023 22:48:29 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Mon, 27 Mar 2023 22:48:30 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Mon, 27 Mar 2023 22:48:30 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 27 Mar 2023 22:48:30 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 27 Mar 2023 22:48:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 27 Mar 2023 23:17:22 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Mon, 27 Mar 2023 23:17:22 GMT
ENV PHP_VERSION=8.1.17
# Mon, 27 Mar 2023 23:17:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.17.tar.xz.asc
# Mon, 27 Mar 2023 23:17:22 GMT
ENV PHP_SHA256=b5c48f95b8e1d8624dd05fc2eab7be13277f9a203ccba97bdca5a1a0fb4a1460
# Mon, 27 Mar 2023 23:17:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 27 Mar 2023 23:17:30 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Mon, 27 Mar 2023 23:19:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Mon, 27 Mar 2023 23:19:32 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Mon, 27 Mar 2023 23:19:33 GMT
RUN docker-php-ext-enable sodium
# Mon, 27 Mar 2023 23:19:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 27 Mar 2023 23:19:33 GMT
STOPSIGNAL SIGWINCH
# Mon, 27 Mar 2023 23:19:33 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Mon, 27 Mar 2023 23:19:33 GMT
WORKDIR /var/www/html
# Mon, 27 Mar 2023 23:19:33 GMT
EXPOSE 80
# Mon, 27 Mar 2023 23:19:33 GMT
CMD ["apache2-foreground"]
# Tue, 28 Mar 2023 01:50:25 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Tue, 28 Mar 2023 01:50:26 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 28 Mar 2023 01:50:26 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 28 Mar 2023 02:00:48 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.22;     pecl install imagick-3.7.0;     pecl install memcached-3.2.0;     pecl install redis-5.3.7;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Tue, 28 Mar 2023 02:00:49 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Tue, 28 Mar 2023 02:00:50 GMT
VOLUME [/var/www/html]
# Tue, 28 Mar 2023 02:00:50 GMT
RUN a2enmod headers rewrite remoteip ;    {     echo RemoteIPHeader X-Real-IP ;     echo RemoteIPTrustedProxy 10.0.0.0/8 ;     echo RemoteIPTrustedProxy 172.16.0.0/12 ;     echo RemoteIPTrustedProxy 192.168.0.0/16 ;    } > /etc/apache2/conf-available/remoteip.conf;    a2enconf remoteip
# Tue, 28 Mar 2023 02:00:50 GMT
ENV NEXTCLOUD_VERSION=26.0.0
# Tue, 28 Mar 2023 02:01:34 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc         "https://download.nextcloud.com/server/releases/nextcloud-${NEXTCLOUD_VERSION}.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Tue, 28 Mar 2023 02:01:43 GMT
COPY multi:38a4739a7ce38db03075117346fff2453db5ff29d27e30f506b9d2fc6a4b4a9a in / 
# Tue, 28 Mar 2023 02:01:44 GMT
COPY multi:5ae4d3e2c333d07b72b698ef5d54be9ec19b520851d7d23aff0a612bc28d533d in /usr/src/nextcloud/config/ 
# Tue, 28 Mar 2023 02:01:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Mar 2023 02:01:44 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:25d08e051bb75230bad82e3a7a054083beec6b4f6a46c8345c731582c297a408`  
		Last Modified: Thu, 23 Mar 2023 00:47:20 GMT  
		Size: 29.6 MB (29646820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fb65f262bf8becde8c3368266a1f67c2bb663b8697df528b2b273d3053d898d`  
		Last Modified: Thu, 23 Mar 2023 09:05:16 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39eb42b7764a8cf9191ccafca9cfb745e96522d012b55e818afa39062a75f45`  
		Last Modified: Thu, 23 Mar 2023 09:05:26 GMT  
		Size: 71.6 MB (71628851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d4a6b504798f4e993e8c14ad74738d9021100d324f4c26cf5303de749f996f`  
		Last Modified: Tue, 28 Mar 2023 00:02:05 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1ea420b4d61f7c058c6b3b7160e02a3c072d222e29672d0e1dce78ac454e61c`  
		Last Modified: Tue, 28 Mar 2023 00:02:31 GMT  
		Size: 19.1 MB (19077330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f224a7abb7caf2c480c53a8d442b51223991b3aa1e50851f78e190cbca3acf92`  
		Last Modified: Tue, 28 Mar 2023 00:02:29 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696bc7cacf0b07fcc6dd744662fa945d62f19a153a64def0dd4ae14754e723c5`  
		Last Modified: Tue, 28 Mar 2023 00:02:29 GMT  
		Size: 512.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd0f81aef9c606f3ed35cdbbb188312ac218daeef15f48c40f8f19cee0c4588`  
		Last Modified: Tue, 28 Mar 2023 00:05:00 GMT  
		Size: 12.2 MB (12159297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4db57883d5c8df1ecf89a905163c15b113e8bded5af283df7a33489b023d779`  
		Last Modified: Tue, 28 Mar 2023 00:04:55 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf03bce3e7ab072a71f8b55451b8263f94be9a24b82ce9b04998638402020826`  
		Last Modified: Tue, 28 Mar 2023 00:04:59 GMT  
		Size: 10.2 MB (10186801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03bb9628d60ca78a13db0c5935a8514141d334d45d4859394beb48d6ed6af163`  
		Last Modified: Tue, 28 Mar 2023 00:04:55 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdd7f7f8c096ccf5cbb24e8aa396c14e709c106f7a8c1ba70e8df781b10b3ec8`  
		Last Modified: Tue, 28 Mar 2023 00:04:55 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c7fbc40412a44e740c73844325a2a84d4afd90d22ddd8cd0b300a2cc0611d2d`  
		Last Modified: Tue, 28 Mar 2023 00:04:55 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d91f0932a2ea57d63d8ce07e2c10c32feb576bca121a5ad1e9dc6f743b44c594`  
		Last Modified: Tue, 28 Mar 2023 02:08:20 GMT  
		Size: 17.1 MB (17050287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41a5529ef48ad76b10c7d642485e04d5bfcfbade1da2c47eb6353df4cfad6bd`  
		Last Modified: Tue, 28 Mar 2023 02:09:39 GMT  
		Size: 3.7 MB (3656572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:134c45bed31545fa86092b115b1c605e471083da2f1799fdc67b07971b9dd560`  
		Last Modified: Tue, 28 Mar 2023 02:09:37 GMT  
		Size: 613.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca87cd4332896e3db97a00442a8bafa4711b849639171f61745a3df7d5ea712`  
		Last Modified: Tue, 28 Mar 2023 02:09:37 GMT  
		Size: 573.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a32c9cb4e3dd2172c230675aa852dc01782afa750dc158ea06c089ff9c7bfd63`  
		Last Modified: Tue, 28 Mar 2023 02:09:56 GMT  
		Size: 164.6 MB (164592447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5ec3183d71d7b3d5c18f19c2a988b44ceb2a6afc58c5878e058d9a83a7d4e9b`  
		Last Modified: Tue, 28 Mar 2023 02:09:38 GMT  
		Size: 3.1 KB (3057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:264c284f1743b6c0188ed7ddb4c96f69cccaba87847b28a4168ae771693edd90`  
		Last Modified: Tue, 28 Mar 2023 02:09:37 GMT  
		Size: 2.2 KB (2215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
