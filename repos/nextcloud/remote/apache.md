## `nextcloud:apache`

```console
$ docker pull nextcloud@sha256:2917ee185932590ed607a050a50f3f2a297eb375835763e377e2b1a9b1c84e99
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
$ docker pull nextcloud@sha256:115fae98ba0da1753f559a043daf487e09eeea3f2d1a2f7c6131a0b8e14f99b4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.6 MB (422636395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ce2ae88829ab492e1f2b578fd11aa4bf6a8663e3767e91b6afc35d159551aab`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:01 GMT
ADD file:b86ae1c7ca3586d8feedcd9ff1b2b1e8ab872caf6587618f1da689045a5d7ae4 in / 
# Tue, 12 Mar 2024 01:21:01 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:57:10 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 12 Mar 2024 02:57:10 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 12 Mar 2024 02:57:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:57:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 12 Mar 2024 02:57:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 12 Mar 2024 03:01:33 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 12 Mar 2024 03:01:33 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 12 Mar 2024 03:01:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 12 Mar 2024 03:01:42 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 12 Mar 2024 03:01:43 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 12 Mar 2024 03:01:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Mar 2024 03:01:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Mar 2024 03:01:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 12 Mar 2024 04:00:42 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Tue, 12 Mar 2024 04:29:22 GMT
ENV PHP_VERSION=8.2.16
# Tue, 12 Mar 2024 04:29:23 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.16.tar.xz.asc
# Tue, 12 Mar 2024 04:29:23 GMT
ENV PHP_SHA256=28cdc995b7d5421711c7044294885fcde4390c9f67504a994b4cf9bc1b5cc593
# Tue, 12 Mar 2024 04:29:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 12 Mar 2024 04:29:35 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 12 Mar 2024 04:33:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 12 Mar 2024 04:33:08 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 12 Mar 2024 04:33:08 GMT
RUN docker-php-ext-enable sodium
# Tue, 12 Mar 2024 04:33:08 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 12 Mar 2024 04:33:08 GMT
STOPSIGNAL SIGWINCH
# Tue, 12 Mar 2024 04:33:08 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 12 Mar 2024 04:33:08 GMT
WORKDIR /var/www/html
# Tue, 12 Mar 2024 04:33:09 GMT
EXPOSE 80
# Tue, 12 Mar 2024 04:33:09 GMT
CMD ["apache2-foreground"]
# Tue, 12 Mar 2024 14:52:00 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Tue, 12 Mar 2024 14:52:00 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 12 Mar 2024 14:52:01 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 12 Mar 2024 14:54:53 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.23;     pecl install imagick-3.7.0;     pecl install memcached-3.2.0;     pecl install redis-6.0.2;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 14:54:53 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Tue, 12 Mar 2024 14:54:53 GMT
VOLUME [/var/www/html]
# Tue, 12 Mar 2024 14:54:54 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip
# Tue, 12 Mar 2024 14:54:54 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Tue, 12 Mar 2024 14:54:55 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits
# Tue, 12 Mar 2024 15:02:30 GMT
ENV NEXTCLOUD_VERSION=28.0.3
# Tue, 12 Mar 2024 15:03:29 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-28.0.3.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-28.0.3.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 15:03:32 GMT
COPY multi:9585a9602f24ff6c37b7e8821d7e5fca4a450cd9cc8c66163bc629028ca3df5c in / 
# Tue, 12 Mar 2024 15:03:33 GMT
COPY multi:325eebb30e6912e4cdbb030d4d22b6dd14fe18ca007f50df3afe27a136e1e383 in /usr/src/nextcloud/config/ 
# Tue, 12 Mar 2024 15:03:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Mar 2024 15:03:33 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:8a1e25ce7c4f75e372e9884f8f7b1bedcfe4a7a7d452eb4b0a1c7477c9a90345`  
		Last Modified: Tue, 12 Mar 2024 01:25:41 GMT  
		Size: 29.1 MB (29124181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de14226e1706b621fe796af63b375db247a2490752558ed4f5ea40648234129`  
		Last Modified: Tue, 12 Mar 2024 05:25:23 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5aaf617d1d2bc41efbec77e9f05370e6f35d8f4363fb26fa04883ec538b7d66`  
		Last Modified: Tue, 12 Mar 2024 05:25:37 GMT  
		Size: 104.4 MB (104355586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ba065e262ff15c57d91609cae32d80920edac1e9b0826e0d8cf5f0f3c60107`  
		Last Modified: Tue, 12 Mar 2024 05:25:22 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:142ecae067f5d5cbf3c2a3cf42d5677472bc8cc633b8ccea33d011749bb84661`  
		Last Modified: Tue, 12 Mar 2024 05:26:03 GMT  
		Size: 20.3 MB (20303886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f1b407f7499799755557f8769bbeb98d0573d6092913d5303cf951acdace0b`  
		Last Modified: Tue, 12 Mar 2024 05:26:00 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a1b2cfb806df514ad4cf5cffa00c66aaa6322c1ef8f3b1c597592771925569b`  
		Last Modified: Tue, 12 Mar 2024 05:26:00 GMT  
		Size: 512.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4662be59c549e5a80d398ff5e56563e860d3c363ecf5baee2a92b06d6a1345`  
		Last Modified: Tue, 12 Mar 2024 05:34:12 GMT  
		Size: 12.4 MB (12418774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:956a2debd5aa861d8c0838c9279661773d4df5cbb95167132302ec4e5c83b503`  
		Last Modified: Tue, 12 Mar 2024 05:34:09 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4225639e1e5ad16afbff89e489788d431c4ccb6ce9cd5bb10d005781aa6a998`  
		Last Modified: Tue, 12 Mar 2024 05:34:11 GMT  
		Size: 11.4 MB (11404751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98126239f7b5269efda422b9c4a53912fe31fcc78d6497aba04b4dab4a21d0f7`  
		Last Modified: Tue, 12 Mar 2024 05:34:09 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab652e74a9352177ea7527a269845c0e22a5004e5d7857a63e579b061af544f9`  
		Last Modified: Tue, 12 Mar 2024 05:34:09 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61a4268149e6de53bee6e88897e498b0eed6b7cda5f68d6fdd227d89f048039`  
		Last Modified: Tue, 12 Mar 2024 05:34:09 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba80cf1673b716c8b7cae30120246f9933a6fffdaaf4616253d2f474ed9b6a1`  
		Last Modified: Tue, 12 Mar 2024 15:05:20 GMT  
		Size: 22.8 MB (22762006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe8d8af36fcdb5debd71478b132af655b1f26d0f80b4683500d5954daccb87e`  
		Last Modified: Tue, 12 Mar 2024 15:05:20 GMT  
		Size: 20.9 MB (20928034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e98afcf339fd985a0819fcb1a11bbaafb02371692395550949c3e15d96214d3b`  
		Last Modified: Tue, 12 Mar 2024 15:05:16 GMT  
		Size: 762.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a172f7e49cb262497502e9d11bf78ff378864f8da09750d59a588fa46d6fdcf`  
		Last Modified: Tue, 12 Mar 2024 15:05:14 GMT  
		Size: 578.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48526732c4418d5baab55e9012c80a0047650301aafd681b28882306425f2e51`  
		Last Modified: Tue, 12 Mar 2024 15:05:14 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f90989339fe05a4a6c47139215f873aa135ece7ab3584d9118b2f916162f432c`  
		Last Modified: Tue, 12 Mar 2024 15:08:17 GMT  
		Size: 201.3 MB (201325855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:314e25b96f05f432ed7d0d40ed5810f7d9d5831e82c3606e49acd5ef370291dd`  
		Last Modified: Tue, 12 Mar 2024 15:07:53 GMT  
		Size: 3.6 KB (3613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d2b676a849996c166710e34a77a488af6a5596ed92c99f4bf93b08e3ab938b`  
		Last Modified: Tue, 12 Mar 2024 15:07:54 GMT  
		Size: 2.4 KB (2393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:apache` - linux; arm variant v5

```console
$ docker pull nextcloud@sha256:28e4ead2da04e66ec30d7009f72ceacf143e6b06a2d76185e27657713b1c8e61
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.1 MB (392140774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f58d266609ef30fac9195a30440b7abc9e69027e444901438186be02c6810669`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 12 Mar 2024 00:48:31 GMT
ADD file:b1bd2ec7dd2a8894ea7b5837afba4e15ba798f4809586f0ac1b8855bd0032651 in / 
# Tue, 12 Mar 2024 00:48:31 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:47:14 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 12 Mar 2024 01:47:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 12 Mar 2024 01:47:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:47:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 12 Mar 2024 01:47:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 12 Mar 2024 01:50:51 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 12 Mar 2024 01:50:51 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 12 Mar 2024 01:51:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 12 Mar 2024 01:51:04 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 12 Mar 2024 01:51:04 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 12 Mar 2024 01:51:04 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Mar 2024 01:51:04 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Mar 2024 01:51:04 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 12 Mar 2024 02:41:15 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Tue, 12 Mar 2024 03:05:04 GMT
ENV PHP_VERSION=8.2.16
# Tue, 12 Mar 2024 03:05:05 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.16.tar.xz.asc
# Tue, 12 Mar 2024 03:05:05 GMT
ENV PHP_SHA256=28cdc995b7d5421711c7044294885fcde4390c9f67504a994b4cf9bc1b5cc593
# Tue, 12 Mar 2024 03:05:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 12 Mar 2024 03:05:18 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 12 Mar 2024 03:08:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 12 Mar 2024 03:08:35 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 12 Mar 2024 03:08:36 GMT
RUN docker-php-ext-enable sodium
# Tue, 12 Mar 2024 03:08:37 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 12 Mar 2024 03:08:37 GMT
STOPSIGNAL SIGWINCH
# Tue, 12 Mar 2024 03:08:37 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 12 Mar 2024 03:08:37 GMT
WORKDIR /var/www/html
# Tue, 12 Mar 2024 03:08:38 GMT
EXPOSE 80
# Tue, 12 Mar 2024 03:08:38 GMT
CMD ["apache2-foreground"]
# Tue, 12 Mar 2024 08:56:59 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Tue, 12 Mar 2024 08:56:59 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 12 Mar 2024 08:56:59 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 12 Mar 2024 09:00:23 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.23;     pecl install imagick-3.7.0;     pecl install memcached-3.2.0;     pecl install redis-6.0.2;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 09:00:24 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Tue, 12 Mar 2024 09:00:24 GMT
VOLUME [/var/www/html]
# Tue, 12 Mar 2024 09:00:25 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip
# Tue, 12 Mar 2024 09:00:25 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Tue, 12 Mar 2024 09:00:26 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits
# Tue, 12 Mar 2024 09:09:06 GMT
ENV NEXTCLOUD_VERSION=28.0.3
# Tue, 12 Mar 2024 09:10:23 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-28.0.3.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-28.0.3.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 09:10:26 GMT
COPY multi:9585a9602f24ff6c37b7e8821d7e5fca4a450cd9cc8c66163bc629028ca3df5c in / 
# Tue, 12 Mar 2024 09:10:27 GMT
COPY multi:325eebb30e6912e4cdbb030d4d22b6dd14fe18ca007f50df3afe27a136e1e383 in /usr/src/nextcloud/config/ 
# Tue, 12 Mar 2024 09:10:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Mar 2024 09:10:27 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:64806d9455193063a6bd4aebf47380e94fad8313f6ad1b5d831882c453f43261`  
		Last Modified: Tue, 12 Mar 2024 00:51:39 GMT  
		Size: 26.9 MB (26884021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75d115fea1b4a8106e263db629be1619e1687e09620739ce2ec2b09ef0f7216b`  
		Last Modified: Tue, 12 Mar 2024 03:51:12 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83e1c5741512c603cc1e5fdb27395ab09059c53c3871664e3c0fa08051670462`  
		Last Modified: Tue, 12 Mar 2024 03:51:27 GMT  
		Size: 82.0 MB (81999306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af0a94ea1638e6635c0e4c239bab002203d65e36eb7b12bb6d9fdfece6154dc1`  
		Last Modified: Tue, 12 Mar 2024 03:51:11 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf3328c6af612c3f7b6b1a513414b09fa7245d3b85239f38bbcc86311ab073ba`  
		Last Modified: Tue, 12 Mar 2024 03:51:52 GMT  
		Size: 19.6 MB (19608292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc33c91c9d6d19b16182a5fd63f18bd28413c720fd6f8873b8680eaab541a13a`  
		Last Modified: Tue, 12 Mar 2024 03:51:49 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03347d119d00160ae7ff93fb281dbde1a946587dcfab5c36cf718aff026bb858`  
		Last Modified: Tue, 12 Mar 2024 03:51:49 GMT  
		Size: 511.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:921e405c9b2cef84c655d258b46e1e802f8425070f223ea8b5e76f1b2d5482cf`  
		Last Modified: Tue, 12 Mar 2024 04:00:03 GMT  
		Size: 12.4 MB (12416813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeef8a2eba53ee4472bdeebf72df297e3ba8e77cc5246b949a943d10cbd329d5`  
		Last Modified: Tue, 12 Mar 2024 04:00:00 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a65fbaa53a688bce1ad469c8f674b9a21db9a762a62ada91aa3e3b2c1c977bd`  
		Last Modified: Tue, 12 Mar 2024 04:00:02 GMT  
		Size: 10.4 MB (10387277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dfa47c3ae052316b3f36fefaad139e95aface38fda84a120d46651ed6de0ece`  
		Last Modified: Tue, 12 Mar 2024 04:00:00 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f22bbde3179e2115b13e16349604cc89fe27f9b9d09fe2c1b2af02a872d311b`  
		Last Modified: Tue, 12 Mar 2024 03:59:59 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcdd545bcad7641cb274173a6a58def9014c23b13fa6b4685c740871ea0fa862`  
		Last Modified: Tue, 12 Mar 2024 04:00:00 GMT  
		Size: 891.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:182e6f0e0deb9520a854867c9dee04e7c36e013fedffbc9d405d1dce6ab29ff0`  
		Last Modified: Tue, 12 Mar 2024 09:12:29 GMT  
		Size: 19.9 MB (19880836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad39e6742ba692dc9b2c197f4f55579fb09eb5fadd8071553e0d8c89388d4092`  
		Last Modified: Tue, 12 Mar 2024 09:12:30 GMT  
		Size: 19.6 MB (19626939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e868b1f3885f45f84c4cbb78297629aea910f1f5967f953e244e27e994e3a6d1`  
		Last Modified: Tue, 12 Mar 2024 09:12:25 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb2ba7921df869f46a531bafe3102e31a11c063b530c9de08192b4e097167979`  
		Last Modified: Tue, 12 Mar 2024 09:12:23 GMT  
		Size: 580.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8956f7681a5e06a92ac61c41f13d5265adc8e72e34db8ea170eaf08d16a5187a`  
		Last Modified: Tue, 12 Mar 2024 09:12:23 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ef97a0584b513e170c17f46f6d3a5fafa5e439fb3259cb74792885127b7b25`  
		Last Modified: Tue, 12 Mar 2024 09:16:17 GMT  
		Size: 201.3 MB (201323974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c88d2f7ea33494b3aaa64acc17cdb9d959df68f08928e9719f61031b7b76ddc4`  
		Last Modified: Tue, 12 Mar 2024 09:15:40 GMT  
		Size: 3.6 KB (3613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e85cd76c6f3e53a2532867d147580c62b97f1edb6429ee406c2fbc65a8814e58`  
		Last Modified: Tue, 12 Mar 2024 09:15:40 GMT  
		Size: 2.4 KB (2395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:apache` - linux; arm variant v7

```console
$ docker pull nextcloud@sha256:ce43cd33a63dbbcc16d6cfa4cf85c0323627a5e7f03a1cc1a08760341b39126f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.6 MB (380576944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7956999754597231135c5e855be5dd6eeeb0d7a68cbca6f75f3cb03f0d616cc7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:15 GMT
ADD file:6c18cdac8d96366de6fc24521b972b80d34639ac5484f27a5d4e355fca934e5d in / 
# Tue, 12 Mar 2024 00:59:16 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 07:23:17 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 12 Mar 2024 07:23:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 12 Mar 2024 07:23:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 07:23:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 12 Mar 2024 07:23:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 12 Mar 2024 07:26:38 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 12 Mar 2024 07:26:38 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 12 Mar 2024 07:26:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 12 Mar 2024 07:26:49 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 12 Mar 2024 07:26:49 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 12 Mar 2024 07:26:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Mar 2024 07:26:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Mar 2024 07:26:50 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 12 Mar 2024 08:17:21 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Tue, 12 Mar 2024 08:41:33 GMT
ENV PHP_VERSION=8.2.16
# Tue, 12 Mar 2024 08:41:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.16.tar.xz.asc
# Tue, 12 Mar 2024 08:41:34 GMT
ENV PHP_SHA256=28cdc995b7d5421711c7044294885fcde4390c9f67504a994b4cf9bc1b5cc593
# Tue, 12 Mar 2024 08:41:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 12 Mar 2024 08:41:46 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 12 Mar 2024 08:44:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 12 Mar 2024 08:44:20 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 12 Mar 2024 08:44:20 GMT
RUN docker-php-ext-enable sodium
# Tue, 12 Mar 2024 08:44:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 12 Mar 2024 08:44:21 GMT
STOPSIGNAL SIGWINCH
# Tue, 12 Mar 2024 08:44:21 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 12 Mar 2024 08:44:21 GMT
WORKDIR /var/www/html
# Tue, 12 Mar 2024 08:44:21 GMT
EXPOSE 80
# Tue, 12 Mar 2024 08:44:21 GMT
CMD ["apache2-foreground"]
# Tue, 12 Mar 2024 13:14:01 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Tue, 12 Mar 2024 13:14:01 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 12 Mar 2024 13:14:01 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 12 Mar 2024 13:16:51 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.23;     pecl install imagick-3.7.0;     pecl install memcached-3.2.0;     pecl install redis-6.0.2;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 13:16:52 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Tue, 12 Mar 2024 13:16:53 GMT
VOLUME [/var/www/html]
# Tue, 12 Mar 2024 13:16:53 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip
# Tue, 12 Mar 2024 13:16:53 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Tue, 12 Mar 2024 13:16:54 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits
# Tue, 12 Mar 2024 13:25:19 GMT
ENV NEXTCLOUD_VERSION=28.0.3
# Tue, 12 Mar 2024 13:26:36 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-28.0.3.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-28.0.3.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 13:26:40 GMT
COPY multi:9585a9602f24ff6c37b7e8821d7e5fca4a450cd9cc8c66163bc629028ca3df5c in / 
# Tue, 12 Mar 2024 13:26:42 GMT
COPY multi:325eebb30e6912e4cdbb030d4d22b6dd14fe18ca007f50df3afe27a136e1e383 in /usr/src/nextcloud/config/ 
# Tue, 12 Mar 2024 13:26:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Mar 2024 13:26:43 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:c5c3540d9b4f416003fa1e21822e15ea4bbe0749e6d1104e7af5c8a1a30b26fd`  
		Last Modified: Tue, 12 Mar 2024 01:03:36 GMT  
		Size: 24.7 MB (24716725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dd82a33324e79052aa5fed0978c223b7d05b5a41532eca869d5602ee24d0c7c`  
		Last Modified: Tue, 12 Mar 2024 09:24:29 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57829c9789b8ee6e6ebe4a80c39f9393df7fcf20975d1d8135fc2142cad63d8`  
		Last Modified: Tue, 12 Mar 2024 09:24:42 GMT  
		Size: 76.2 MB (76169934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff1e9e48950eb6ede1065099dd2b976917707ffa4953e5c351638a845668823`  
		Last Modified: Tue, 12 Mar 2024 09:24:29 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98245a88fa6adc9fd93e0af245463b9d9dc7cbea417c92646663e9f7375ffa93`  
		Last Modified: Tue, 12 Mar 2024 09:25:08 GMT  
		Size: 19.0 MB (19045529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dff6ef8d01cdfd6ba1026fbed3898bbc602bc4e92c1a6879b933c622d36a7a42`  
		Last Modified: Tue, 12 Mar 2024 09:25:05 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7b18f3b6afb527e3463e62dae0e34a48ea21bcfdf1bfb8a5bbe5c978746c3e6`  
		Last Modified: Tue, 12 Mar 2024 09:25:05 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4a7a0cf0b8e737a0c8a3f87117814564d987ca845279225bebdfe599b380bec`  
		Last Modified: Tue, 12 Mar 2024 09:33:23 GMT  
		Size: 12.4 MB (12416809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11694ab6c97c3c68a6f46ec88fef6c3482791b88f6ec1982e0a0f7463b58e4a1`  
		Last Modified: Tue, 12 Mar 2024 09:33:20 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a489b4a2a4ec722d474fbe91321b9708c83896df14dcaac41d1868c4dc5a38ca`  
		Last Modified: Tue, 12 Mar 2024 09:33:22 GMT  
		Size: 9.8 MB (9817044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c43909584fba915d2c784f820c00cbf8e6fcf57c684d1dbf971b3d553d54310`  
		Last Modified: Tue, 12 Mar 2024 09:33:20 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e5a609ae8cedc215921a0a47a07150db62ce6f2aae33c93f8e9b76b50cc36d`  
		Last Modified: Tue, 12 Mar 2024 09:33:20 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:928726f5295591fbc0ac9052dc33f32501772bcec914edf2f7fa86f1ae637598`  
		Last Modified: Tue, 12 Mar 2024 09:33:20 GMT  
		Size: 891.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57631126754aa24235dfb02a4dd8e3cc93c31b274ff4c1f43963472506efac1d`  
		Last Modified: Tue, 12 Mar 2024 13:28:52 GMT  
		Size: 18.1 MB (18130102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:becf1e54bfa0cee425394525cc66045c8433964a469efb7c670377ba41496fff`  
		Last Modified: Tue, 12 Mar 2024 13:28:54 GMT  
		Size: 18.9 MB (18943613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24c3ea17508494fdaceaa98e5ac69ec3474f7b8b5b804606be1add3c1b4d21de`  
		Last Modified: Tue, 12 Mar 2024 13:28:49 GMT  
		Size: 758.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e2927b74f984d345d9126ac985edd861d76025984d565c9bf567d512530cd32`  
		Last Modified: Tue, 12 Mar 2024 13:28:47 GMT  
		Size: 570.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83fc3ce405ae00661881fbaccaac6a5361fba690a4cac6feb486d3c96db95ce5`  
		Last Modified: Tue, 12 Mar 2024 13:28:47 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3843ab47abee50738adc645e8491ee45b2afa71fff2e2b7aa4a5bb171f19b394`  
		Last Modified: Tue, 12 Mar 2024 13:33:07 GMT  
		Size: 201.3 MB (201323888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a312a47a13c158fb4dee7aca6096454b664411388cac6104af0947d50827abba`  
		Last Modified: Tue, 12 Mar 2024 13:32:28 GMT  
		Size: 3.6 KB (3613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed5b91d8f1aa08ee9230092e9b666d24bb4edc8d90faadf8ff4ca5e485f42e77`  
		Last Modified: Tue, 12 Mar 2024 13:32:28 GMT  
		Size: 2.4 KB (2396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:apache` - linux; arm64 variant v8

```console
$ docker pull nextcloud@sha256:04283f68746685aaaffa88a7e3e1e8bdd4626d2558d22918bb993309247ccaa3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.1 MB (414058646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f21c22f2c3e4ea776dd3aaaf522c0f9976c4edb48ea4b9f8a8ec38198909cf04`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:36 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Tue, 12 Mar 2024 00:45:37 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 04:38:53 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 12 Mar 2024 04:38:53 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 12 Mar 2024 04:39:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 04:39:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 12 Mar 2024 04:39:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 12 Mar 2024 04:43:01 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 12 Mar 2024 04:43:01 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 12 Mar 2024 04:43:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 12 Mar 2024 04:43:09 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 12 Mar 2024 04:43:09 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 12 Mar 2024 04:43:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Mar 2024 04:43:10 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Mar 2024 04:43:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 12 Mar 2024 05:39:43 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Tue, 12 Mar 2024 06:06:26 GMT
ENV PHP_VERSION=8.2.16
# Tue, 12 Mar 2024 06:06:26 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.16.tar.xz.asc
# Tue, 12 Mar 2024 06:06:26 GMT
ENV PHP_SHA256=28cdc995b7d5421711c7044294885fcde4390c9f67504a994b4cf9bc1b5cc593
# Tue, 12 Mar 2024 06:06:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 12 Mar 2024 06:06:37 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 12 Mar 2024 06:09:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 12 Mar 2024 06:09:53 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 12 Mar 2024 06:09:54 GMT
RUN docker-php-ext-enable sodium
# Tue, 12 Mar 2024 06:09:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 12 Mar 2024 06:09:54 GMT
STOPSIGNAL SIGWINCH
# Tue, 12 Mar 2024 06:09:54 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 12 Mar 2024 06:09:54 GMT
WORKDIR /var/www/html
# Tue, 12 Mar 2024 06:09:54 GMT
EXPOSE 80
# Tue, 12 Mar 2024 06:09:54 GMT
CMD ["apache2-foreground"]
# Tue, 12 Mar 2024 12:15:48 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Tue, 12 Mar 2024 12:15:48 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 12 Mar 2024 12:15:48 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 12 Mar 2024 12:18:39 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.23;     pecl install imagick-3.7.0;     pecl install memcached-3.2.0;     pecl install redis-6.0.2;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 12:18:39 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Tue, 12 Mar 2024 12:18:39 GMT
VOLUME [/var/www/html]
# Tue, 12 Mar 2024 12:18:40 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip
# Tue, 12 Mar 2024 12:18:40 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Tue, 12 Mar 2024 12:18:40 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits
# Tue, 12 Mar 2024 12:26:15 GMT
ENV NEXTCLOUD_VERSION=28.0.3
# Tue, 12 Mar 2024 12:27:11 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-28.0.3.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-28.0.3.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 12:27:16 GMT
COPY multi:9585a9602f24ff6c37b7e8821d7e5fca4a450cd9cc8c66163bc629028ca3df5c in / 
# Tue, 12 Mar 2024 12:27:16 GMT
COPY multi:325eebb30e6912e4cdbb030d4d22b6dd14fe18ca007f50df3afe27a136e1e383 in /usr/src/nextcloud/config/ 
# Tue, 12 Mar 2024 12:27:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Mar 2024 12:27:16 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b17d6e35656ac020a43a3f9453f06b61a9c61212e0437b31bac9d2b974cb4d`  
		Last Modified: Tue, 12 Mar 2024 06:57:18 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8431cb294ec999c969b368afe1f6bb5484654b2ce2932cb1a6780d9c52781090`  
		Last Modified: Tue, 12 Mar 2024 06:57:29 GMT  
		Size: 98.1 MB (98126016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:735009beb2cceac6bf57add7c26d3a77c8d92fc49ea5e05d8b2452e84a09b61d`  
		Last Modified: Tue, 12 Mar 2024 06:57:18 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:036053896963520b5ce13f9151d0ad3dd4aff6d300c0cf85402700844e48dff6`  
		Last Modified: Tue, 12 Mar 2024 06:57:52 GMT  
		Size: 20.3 MB (20305130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9751366e208c9511ed7ed698080806c444f2effdd9f321b90fa1055b14a79e9`  
		Last Modified: Tue, 12 Mar 2024 06:57:50 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f53fc5dec6a2ddf288e227b9388cda0cb816d4b7e952c795bb0af42afafc9c3`  
		Last Modified: Tue, 12 Mar 2024 06:57:50 GMT  
		Size: 512.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7067a818e71e39e88ac6d93510917dc8db001d6e7d0ab5dd8cafc505819a0c96`  
		Last Modified: Tue, 12 Mar 2024 07:05:33 GMT  
		Size: 12.4 MB (12418472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89908ceea943ba21f562e082c23bfd2921385bc2c5397939261eac7c8db9a64b`  
		Last Modified: Tue, 12 Mar 2024 07:05:31 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1c2ada5bc06c4773a7382e4f25a85b5d7cef426e91ac30653c019b95bc88981`  
		Last Modified: Tue, 12 Mar 2024 07:05:32 GMT  
		Size: 11.4 MB (11410650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3d89349ad173769080731eff01c50bc4a0bcc404c0f531a123bb7abe08dfd0`  
		Last Modified: Tue, 12 Mar 2024 07:05:30 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:587d082176e4ad86bd65147d1e33a3efa89e9272696b68e8eb2bd209cf1c471f`  
		Last Modified: Tue, 12 Mar 2024 07:05:30 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af16231a435384036d968828186bb9d1f9c7dca3ea11dbdc2ccc85b5a330e6fd`  
		Last Modified: Tue, 12 Mar 2024 07:05:30 GMT  
		Size: 891.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:180f0d9352b9aa4fc2bc35161614b9253b0367b595a22fca9d8c45f4d10abaf9`  
		Last Modified: Tue, 12 Mar 2024 12:29:01 GMT  
		Size: 20.1 MB (20146825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ee75c133f193de5fa5682ca11f1b6ba81ae78a2d99468520feaac5a74b93eaf`  
		Last Modified: Tue, 12 Mar 2024 12:29:01 GMT  
		Size: 21.2 MB (21156221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f517e926f7b323513d60a6f636ac1bc15e926c80fb05bc28867ea2d7cee816f7`  
		Last Modified: Tue, 12 Mar 2024 12:28:58 GMT  
		Size: 761.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9edacc060e5cdcd524b230fa73731d6b5346d56dc39e7226fadfdb40696b1ed7`  
		Last Modified: Tue, 12 Mar 2024 12:28:57 GMT  
		Size: 578.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c247243e3f377e6e24eb374861a9e44dd44277bf561dc90e9ceb595aec3f2d52`  
		Last Modified: Tue, 12 Mar 2024 12:28:56 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19663fe1c578ea3dc6536ce0f65ca09cc853adb969a09d801eb03a52a777527d`  
		Last Modified: Tue, 12 Mar 2024 12:31:33 GMT  
		Size: 201.3 MB (201325581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65a7296d99086d248a2673e88343b8768646f6ea6e21e3ba32307a349a5c6419`  
		Last Modified: Tue, 12 Mar 2024 12:31:14 GMT  
		Size: 3.6 KB (3614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f60da495bc9ff895086ce61fc3b41ae7d93ecba0bc52e6fb9a7fad4a043f316`  
		Last Modified: Tue, 12 Mar 2024 12:31:15 GMT  
		Size: 2.4 KB (2396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:apache` - linux; 386

```console
$ docker pull nextcloud@sha256:8420f4bc550941cb4fff870d17bcf49da1efa27d6c7a2730882d9cab02eda89c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **421.3 MB (421273033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63369f3d426e12e075c666bf0d276537931bd5a9356c03e214aad46b0c030987`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 12 Mar 2024 00:57:59 GMT
ADD file:88f04d79dc9f1691544c636ff52d6744a2ff68d504793ea8034b797d0bfc6fd3 in / 
# Tue, 12 Mar 2024 00:58:00 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:39:14 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 12 Mar 2024 01:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 12 Mar 2024 01:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:39:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 12 Mar 2024 01:39:44 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 12 Mar 2024 01:46:37 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 12 Mar 2024 01:46:37 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 12 Mar 2024 01:46:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 12 Mar 2024 01:46:49 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 12 Mar 2024 01:46:50 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 12 Mar 2024 01:46:50 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Mar 2024 01:46:50 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Mar 2024 01:46:50 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 12 Mar 2024 03:28:54 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Tue, 12 Mar 2024 04:18:13 GMT
ENV PHP_VERSION=8.2.16
# Tue, 12 Mar 2024 04:18:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.16.tar.xz.asc
# Tue, 12 Mar 2024 04:18:13 GMT
ENV PHP_SHA256=28cdc995b7d5421711c7044294885fcde4390c9f67504a994b4cf9bc1b5cc593
# Tue, 12 Mar 2024 04:18:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 12 Mar 2024 04:18:27 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 12 Mar 2024 04:24:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 12 Mar 2024 04:24:46 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 12 Mar 2024 04:24:47 GMT
RUN docker-php-ext-enable sodium
# Tue, 12 Mar 2024 04:24:47 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 12 Mar 2024 04:24:47 GMT
STOPSIGNAL SIGWINCH
# Tue, 12 Mar 2024 04:24:47 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 12 Mar 2024 04:24:47 GMT
WORKDIR /var/www/html
# Tue, 12 Mar 2024 04:24:47 GMT
EXPOSE 80
# Tue, 12 Mar 2024 04:24:48 GMT
CMD ["apache2-foreground"]
# Tue, 12 Mar 2024 15:38:23 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Tue, 12 Mar 2024 15:38:23 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 12 Mar 2024 15:38:23 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 12 Mar 2024 15:42:16 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.23;     pecl install imagick-3.7.0;     pecl install memcached-3.2.0;     pecl install redis-6.0.2;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 15:42:17 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Tue, 12 Mar 2024 15:42:17 GMT
VOLUME [/var/www/html]
# Tue, 12 Mar 2024 15:42:18 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip
# Tue, 12 Mar 2024 15:42:18 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Tue, 12 Mar 2024 15:42:18 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits
# Tue, 12 Mar 2024 15:52:12 GMT
ENV NEXTCLOUD_VERSION=28.0.3
# Tue, 12 Mar 2024 15:53:25 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-28.0.3.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-28.0.3.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 15:53:29 GMT
COPY multi:9585a9602f24ff6c37b7e8821d7e5fca4a450cd9cc8c66163bc629028ca3df5c in / 
# Tue, 12 Mar 2024 15:53:29 GMT
COPY multi:325eebb30e6912e4cdbb030d4d22b6dd14fe18ca007f50df3afe27a136e1e383 in /usr/src/nextcloud/config/ 
# Tue, 12 Mar 2024 15:53:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Mar 2024 15:53:30 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:576af7ffb10b3f3b8d5523e6b91da8667eb39393cdfd50fb26dfc178e504ba70`  
		Last Modified: Tue, 12 Mar 2024 01:02:43 GMT  
		Size: 30.1 MB (30141873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc8b418f2e8ebe03c4a8d60a403099d5bd9956664693b358caef9096763fabd`  
		Last Modified: Tue, 12 Mar 2024 05:53:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:572f25d2333bd6d54c124fa174175081a9c95780122966ffb6532bd93757a9bd`  
		Last Modified: Tue, 12 Mar 2024 05:53:38 GMT  
		Size: 101.5 MB (101519737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29f6e71adc002ea9786257601b0d391da402881cf3c46d70b1bf238b5e218a47`  
		Last Modified: Tue, 12 Mar 2024 05:53:12 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:589ac2ec3c620e7a371533497b0cfd74ea84db2b079763c0c27f094625f447cf`  
		Last Modified: Tue, 12 Mar 2024 05:54:05 GMT  
		Size: 20.8 MB (20826115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef95ebea38d5ed66df38918c6398211026347c3a649d8cc4c3d081f4e7c6290`  
		Last Modified: Tue, 12 Mar 2024 05:54:01 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ea05f91953dd8b5d5da845bf416fd786a74c12a214cd690ab7a3fe6bc5a5774`  
		Last Modified: Tue, 12 Mar 2024 05:54:01 GMT  
		Size: 517.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa7f0d4d147922f81f06c94d1851bc0875e7cf9f3ee1e01865c59743c3c20dd`  
		Last Modified: Tue, 12 Mar 2024 06:03:26 GMT  
		Size: 12.4 MB (12417869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe9e27551ae3761b2ecbed4dcdf067c625c7220aaa101c648c0c74dfc62c7040`  
		Last Modified: Tue, 12 Mar 2024 06:03:23 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855de880fd97665d0207fd4121d45dcc01af785bccd57b24abbddb2b5d2a4b1f`  
		Last Modified: Tue, 12 Mar 2024 06:03:26 GMT  
		Size: 11.6 MB (11638731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:330aeee62a14aebec070e9868a704ef0ecd33da9610e630e81aa609e6ebabcbb`  
		Last Modified: Tue, 12 Mar 2024 06:03:23 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f59f23c59850d8c1f8f1373e5f0902b0bd2c2ec1fa32b2e437742dcdd7cf96`  
		Last Modified: Tue, 12 Mar 2024 06:03:23 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5a22b7331a2ba915bf1bf77a9605316694355297bf6798fad3f8e8cf7637ee9`  
		Last Modified: Tue, 12 Mar 2024 06:03:23 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee2e43424d515bc6deaaf11ee07e92fad8f7374fdf5fc7fe5035e7f94e1e8bf2`  
		Last Modified: Tue, 12 Mar 2024 15:55:35 GMT  
		Size: 22.3 MB (22252546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:308d6918e8dd725b0567eaefc34047fc72a2b43e41f85030b99b8255249408e8`  
		Last Modified: Tue, 12 Mar 2024 15:55:35 GMT  
		Size: 21.1 MB (21137963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5adfc2f46114d0d82080e6f11d2dc8e9ea167c6f0abce67457b5b793e8521483`  
		Last Modified: Tue, 12 Mar 2024 15:55:28 GMT  
		Size: 762.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9d4b9fcfa8d783fc42e6521e2d8896fb6f155926327637255262050a3c13ec4`  
		Last Modified: Tue, 12 Mar 2024 15:55:26 GMT  
		Size: 579.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89eff8a7d63a075b4bb824ad90884268c40348c96be32684d1d14da6e1674fe5`  
		Last Modified: Tue, 12 Mar 2024 15:55:26 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24fbed3497a29dc8d72a1e37adf685d72b1be89aa555a06827eb81ecabdde9b2`  
		Last Modified: Tue, 12 Mar 2024 15:59:50 GMT  
		Size: 201.3 MB (201324873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0393e8890759cb24facf6a2c5fd0df06c0dc5e0a9d827ce75f4191e08c9ba52e`  
		Last Modified: Tue, 12 Mar 2024 15:59:11 GMT  
		Size: 3.6 KB (3614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb5b08e8a7c3f0e39d5e7e243d2d46f57473f14145188a31ada7f8f9f8f86fa0`  
		Last Modified: Tue, 12 Mar 2024 15:59:11 GMT  
		Size: 2.4 KB (2392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:apache` - linux; mips64le

```console
$ docker pull nextcloud@sha256:e510ed02140f539540a7bda7120bb26ae95fcb5c3a1d555263fbc511218cc7a7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.9 MB (393936270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d0e2cbad0024df9e4d31026bcef84216fdddf22db645f99ddeda78ebdf89bd1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 12 Mar 2024 01:06:19 GMT
ADD file:c03c59e261bb08f39e6a97df2fd4b82f1e11b49a62d1859a8f8efac680b80a88 in / 
# Tue, 12 Mar 2024 01:06:23 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 07:04:45 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 12 Mar 2024 07:04:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 12 Mar 2024 07:06:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 07:06:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 12 Mar 2024 07:06:47 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 12 Mar 2024 07:23:21 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 12 Mar 2024 07:23:25 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 12 Mar 2024 07:24:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 12 Mar 2024 07:24:25 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 12 Mar 2024 07:24:31 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 12 Mar 2024 07:24:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Mar 2024 07:24:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Mar 2024 07:24:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 12 Mar 2024 11:33:26 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Tue, 12 Mar 2024 13:33:49 GMT
ENV PHP_VERSION=8.2.16
# Tue, 12 Mar 2024 13:33:52 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.16.tar.xz.asc
# Tue, 12 Mar 2024 13:33:56 GMT
ENV PHP_SHA256=28cdc995b7d5421711c7044294885fcde4390c9f67504a994b4cf9bc1b5cc593
# Tue, 12 Mar 2024 13:34:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 12 Mar 2024 13:34:48 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 12 Mar 2024 13:50:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 12 Mar 2024 13:50:04 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 12 Mar 2024 13:50:10 GMT
RUN docker-php-ext-enable sodium
# Tue, 12 Mar 2024 13:50:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 12 Mar 2024 13:50:17 GMT
STOPSIGNAL SIGWINCH
# Tue, 12 Mar 2024 13:50:20 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 12 Mar 2024 13:50:24 GMT
WORKDIR /var/www/html
# Tue, 12 Mar 2024 13:50:27 GMT
EXPOSE 80
# Tue, 12 Mar 2024 13:50:30 GMT
CMD ["apache2-foreground"]
# Tue, 12 Mar 2024 20:40:54 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Tue, 12 Mar 2024 20:40:58 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 12 Mar 2024 20:41:01 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 12 Mar 2024 20:52:10 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.23;     pecl install imagick-3.7.0;     pecl install memcached-3.2.0;     pecl install redis-6.0.2;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 20:52:17 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Tue, 12 Mar 2024 20:52:21 GMT
VOLUME [/var/www/html]
# Tue, 12 Mar 2024 20:52:28 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip
# Tue, 12 Mar 2024 20:52:32 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Tue, 12 Mar 2024 20:52:39 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits
# Tue, 12 Mar 2024 21:21:44 GMT
ENV NEXTCLOUD_VERSION=28.0.3
# Tue, 12 Mar 2024 21:24:59 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-28.0.3.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-28.0.3.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 21:25:11 GMT
COPY multi:9585a9602f24ff6c37b7e8821d7e5fca4a450cd9cc8c66163bc629028ca3df5c in / 
# Tue, 12 Mar 2024 21:25:21 GMT
COPY multi:325eebb30e6912e4cdbb030d4d22b6dd14fe18ca007f50df3afe27a136e1e383 in /usr/src/nextcloud/config/ 
# Tue, 12 Mar 2024 21:25:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Mar 2024 21:25:39 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:aad79459a0f767fcded51c9547150a1cfd96638972389ab8621b5f3eb4a9c280`  
		Last Modified: Tue, 12 Mar 2024 01:17:09 GMT  
		Size: 29.1 MB (29119205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75ad2ee86d932791e83ef3c48546f89d80fb95dbd7bde823e4a9130d9736fb56`  
		Last Modified: Tue, 12 Mar 2024 17:21:30 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59af68362cd81b3b6952f94bf5c46f86937fd9ee619806471611d4b37183a423`  
		Last Modified: Tue, 12 Mar 2024 17:22:26 GMT  
		Size: 80.7 MB (80667080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4246e7c869e89c6228ff595bb4f1a52c830d5330d9f60d1e5f4618e5f6810f4b`  
		Last Modified: Tue, 12 Mar 2024 17:21:30 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeefc470438982acc7af1e3500db532d2a0137661a5afa9cedc9d47c72b00a93`  
		Last Modified: Tue, 12 Mar 2024 17:23:11 GMT  
		Size: 20.1 MB (20054112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c1debd2235578eaa9b06654657c84e6a19afaadba378c1984d6c326e658889d`  
		Last Modified: Tue, 12 Mar 2024 17:22:56 GMT  
		Size: 439.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a08577e3528f333903f82af2b816db146e6ed1a4a8ac828fd1be1f7eac7e617`  
		Last Modified: Tue, 12 Mar 2024 17:22:56 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb63c6212e5b63b950f91fed1c97e3dc7019d5c4e61ba2baca0a0e97c4ee020`  
		Last Modified: Tue, 12 Mar 2024 17:39:16 GMT  
		Size: 12.2 MB (12211332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1905d2eaa31dba40edc7a4865542d1fac0278c98930f2ef5fda6aceafba9525b`  
		Last Modified: Tue, 12 Mar 2024 17:39:10 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:878d0474f5004bd6a405b831c79297dcb8b6ddf5c27f6dfff82b3d667ad21132`  
		Last Modified: Tue, 12 Mar 2024 17:39:19 GMT  
		Size: 10.5 MB (10482449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02fabe2d52da0b729d91222fbeeb254864eb478ddd34f523d5a62b2017addd3c`  
		Last Modified: Tue, 12 Mar 2024 17:39:10 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5fb228878de6907a73e1056c2532c8d72980b299b143d586e8c8f49bb23cfc2`  
		Last Modified: Tue, 12 Mar 2024 17:39:10 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:915fde057f14d0efa5a9aa04db0480d9de70da6b32d1c6a277f6805806561be5`  
		Last Modified: Tue, 12 Mar 2024 17:39:10 GMT  
		Size: 891.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a42e1982be78e84322444b9963183041da3a32464211a0a5699d898d87be109b`  
		Last Modified: Tue, 12 Mar 2024 21:30:57 GMT  
		Size: 19.8 MB (19796471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae227893d6fc8b77d89d3dda0630350dc72e6bec1221a4371d970ee6db9be18`  
		Last Modified: Tue, 12 Mar 2024 21:31:03 GMT  
		Size: 20.5 MB (20484585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:491d8eea8a7aa42e2140a9804a643d437ee88d201324980525b70b161d213114`  
		Last Modified: Tue, 12 Mar 2024 21:30:39 GMT  
		Size: 708.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6acaab8f74dcd853c646ab99c43388bb9454e57a27b90cfaf6c458242e34d0da`  
		Last Modified: Tue, 12 Mar 2024 21:30:36 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f5e7f3f7400894ad423d1b8a7d9aa17ec102755f3033333265cfdd41b6c94f`  
		Last Modified: Tue, 12 Mar 2024 21:30:37 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68eb93a85b2c693f7fd3107e713e4d1636eed0c442f9c9fc6c92fe6f1ee38e29`  
		Last Modified: Tue, 12 Mar 2024 21:42:09 GMT  
		Size: 201.1 MB (201107868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813d78748d4327b6179a5bdcf7b761dafd90df4edac99f4aedb48d1315f0624d`  
		Last Modified: Tue, 12 Mar 2024 21:40:08 GMT  
		Size: 3.6 KB (3614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8dc1334d0fe75758c2997f840e50f30e6f1015ed500699207d93b2bdef5bcb`  
		Last Modified: Tue, 12 Mar 2024 21:40:08 GMT  
		Size: 2.4 KB (2396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:apache` - linux; ppc64le

```console
$ docker pull nextcloud@sha256:67802d3aa1324c862c6de5cc3b1c7a77cabeec5f739470defe1d154245e0c5df
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.0 MB (427965574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e06b581e8e10bcbc4d435b470399270c520df9b986e66c6d282e1eaa5421c692`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 12 Mar 2024 00:30:19 GMT
ADD file:9273ef56d086dbc93b46b7e8ae424eb04096fb00c693dd6cda1f48346290d4d5 in / 
# Tue, 12 Mar 2024 00:30:24 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 03:44:38 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 12 Mar 2024 03:44:39 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 12 Mar 2024 03:48:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 03:48:51 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 12 Mar 2024 03:48:57 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 12 Mar 2024 03:57:49 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 12 Mar 2024 03:57:51 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 12 Mar 2024 03:58:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 12 Mar 2024 03:59:07 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 12 Mar 2024 03:59:09 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 12 Mar 2024 03:59:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Mar 2024 03:59:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Mar 2024 03:59:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 12 Mar 2024 05:43:59 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Tue, 12 Mar 2024 06:30:04 GMT
ENV PHP_VERSION=8.2.16
# Tue, 12 Mar 2024 06:30:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.16.tar.xz.asc
# Tue, 12 Mar 2024 06:30:11 GMT
ENV PHP_SHA256=28cdc995b7d5421711c7044294885fcde4390c9f67504a994b4cf9bc1b5cc593
# Tue, 12 Mar 2024 06:31:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 12 Mar 2024 06:31:51 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 12 Mar 2024 06:38:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 12 Mar 2024 06:38:55 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 12 Mar 2024 06:38:58 GMT
RUN docker-php-ext-enable sodium
# Tue, 12 Mar 2024 06:39:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 12 Mar 2024 06:39:09 GMT
STOPSIGNAL SIGWINCH
# Tue, 12 Mar 2024 06:39:09 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 12 Mar 2024 06:39:12 GMT
WORKDIR /var/www/html
# Tue, 12 Mar 2024 06:39:18 GMT
EXPOSE 80
# Tue, 12 Mar 2024 06:39:20 GMT
CMD ["apache2-foreground"]
# Tue, 12 Mar 2024 16:26:49 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Tue, 12 Mar 2024 16:26:50 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 12 Mar 2024 16:26:50 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 12 Mar 2024 16:31:49 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.23;     pecl install imagick-3.7.0;     pecl install memcached-3.2.0;     pecl install redis-6.0.2;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 16:31:52 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Tue, 12 Mar 2024 16:31:53 GMT
VOLUME [/var/www/html]
# Tue, 12 Mar 2024 16:31:55 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip
# Tue, 12 Mar 2024 16:31:55 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Tue, 12 Mar 2024 16:31:56 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits
# Tue, 12 Mar 2024 16:43:39 GMT
ENV NEXTCLOUD_VERSION=28.0.3
# Tue, 12 Mar 2024 16:44:48 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-28.0.3.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-28.0.3.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 16:44:54 GMT
COPY multi:9585a9602f24ff6c37b7e8821d7e5fca4a450cd9cc8c66163bc629028ca3df5c in / 
# Tue, 12 Mar 2024 16:44:54 GMT
COPY multi:325eebb30e6912e4cdbb030d4d22b6dd14fe18ca007f50df3afe27a136e1e383 in /usr/src/nextcloud/config/ 
# Tue, 12 Mar 2024 16:44:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Mar 2024 16:44:56 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:c28cd0e276dcdeb4d44f5cc5bb958610750ff902a081b668e3863c2f38eef054`  
		Last Modified: Tue, 12 Mar 2024 00:38:06 GMT  
		Size: 33.1 MB (33119023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729fb27eaa92097ad878499ec6403a23c58d8214dac659ab72a1e323819ef57a`  
		Last Modified: Tue, 12 Mar 2024 08:08:35 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cce4a728b9ae2c7eefcd9b8c3b9dc1d62b72c1c071f16bc427f26b3053a56b1`  
		Last Modified: Tue, 12 Mar 2024 08:08:52 GMT  
		Size: 103.3 MB (103313606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e40564a51615fdea74995b1c4e47872bc1cb06986eab253f3b5c5bb070cb76e`  
		Last Modified: Tue, 12 Mar 2024 08:08:34 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62d0172ecc888b93bd448b82bc6d9f857b3d92b715a3dbf98063659ae5aeb9c4`  
		Last Modified: Tue, 12 Mar 2024 08:09:23 GMT  
		Size: 21.5 MB (21490020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3644f81176bc8772d0ef995fb85eb87ab44e5d4ec0edc420255e9c461846490`  
		Last Modified: Tue, 12 Mar 2024 08:09:20 GMT  
		Size: 480.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:136812f7b93f984042c6fc7d609a2cafb56b8f103e463590d92b4795c71c2dbe`  
		Last Modified: Tue, 12 Mar 2024 08:09:20 GMT  
		Size: 516.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e0da14b330c743a92ad932601ff54f0788e917da57e23267bbe85b6fc05c603`  
		Last Modified: Tue, 12 Mar 2024 08:19:09 GMT  
		Size: 12.4 MB (12418958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c1bc905e769d12007842f2a524f640f71f424ed1e1e84023c14f59bbeed262`  
		Last Modified: Tue, 12 Mar 2024 08:19:05 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173229033e28c1b7678a7bf6f784d0394b5488a8218665b4c3f53a5458e55633`  
		Last Modified: Tue, 12 Mar 2024 08:19:09 GMT  
		Size: 11.8 MB (11815408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b90609f38d91e44786f36c8f22fcbb38434d15eb1b14ae6dc0de9ae0e783fe1`  
		Last Modified: Tue, 12 Mar 2024 08:19:05 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0540272e90e3d96a7ef971f41ab46de12fc9720b86b85d277f05c57d8bc3ed`  
		Last Modified: Tue, 12 Mar 2024 08:19:06 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b33e96d5c520a52244009e083df152ab8c2a84c6b11210c2dd36f4e1dca64e9`  
		Last Modified: Tue, 12 Mar 2024 08:19:05 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae978611111a16010b3c5253b64c377e7784aab03e94cc0800d4d07745ca2e45`  
		Last Modified: Tue, 12 Mar 2024 16:47:16 GMT  
		Size: 22.6 MB (22619083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed53087fe74cfec2e95878a0c99871f7f87b77a49832c4c21a1cb6c5c94784c`  
		Last Modified: Tue, 12 Mar 2024 16:47:16 GMT  
		Size: 21.8 MB (21848917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b05705783d3489e2275f65e0216cba873d5f84462a0be975bdffe54a356a8ee3`  
		Last Modified: Tue, 12 Mar 2024 16:47:12 GMT  
		Size: 760.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ddb7543475c0cff9cbff9bcce0dbcc84211f4de2733b241943b93a50cbd6bb`  
		Last Modified: Tue, 12 Mar 2024 16:47:09 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:541c7853749048befb5273565455f692eb5dce577ef1e2c0a24057291a3d9f3f`  
		Last Modified: Tue, 12 Mar 2024 16:47:09 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a5ae5796a6d3b8182cba276bf8362b1f1b2f2656bb25d2119036d3cc9818995`  
		Last Modified: Tue, 12 Mar 2024 16:50:42 GMT  
		Size: 201.3 MB (201327222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85405f2309930188a4a42a6d1b77ab497bcb639b4552bc67a7074fbcc95e2271`  
		Last Modified: Tue, 12 Mar 2024 16:50:13 GMT  
		Size: 3.6 KB (3613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8845d6c30f3cc4a680fd27aa2a8fd4b52167ad51614009d0892b4ec501371b5e`  
		Last Modified: Tue, 12 Mar 2024 16:50:13 GMT  
		Size: 2.4 KB (2394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:apache` - linux; s390x

```console
$ docker pull nextcloud@sha256:009be11689cef66532905cb8f8513436cd0b108330ff875b430da96a7f28433f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.0 MB (392006525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2922b085b701a2075d1291ebaf5e411ac41cc2c0c8d901be4d5684fb4eee3d5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 12 Mar 2024 00:54:02 GMT
ADD file:80ab985d4871ca6a72156bedfe1038e6b1a89591fc2fd86c4ef778d293223aff in / 
# Tue, 12 Mar 2024 00:54:03 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 08:04:49 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 12 Mar 2024 08:04:50 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 12 Mar 2024 08:05:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 08:05:26 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 12 Mar 2024 08:05:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 12 Mar 2024 08:09:37 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 12 Mar 2024 08:09:37 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 12 Mar 2024 08:09:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 12 Mar 2024 08:09:45 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 12 Mar 2024 08:09:46 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 12 Mar 2024 08:09:46 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Mar 2024 08:09:46 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Mar 2024 08:09:46 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 12 Mar 2024 09:26:06 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Tue, 12 Mar 2024 10:04:02 GMT
ENV PHP_VERSION=8.2.16
# Tue, 12 Mar 2024 10:04:02 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.16.tar.xz.asc
# Tue, 12 Mar 2024 10:04:02 GMT
ENV PHP_SHA256=28cdc995b7d5421711c7044294885fcde4390c9f67504a994b4cf9bc1b5cc593
# Tue, 12 Mar 2024 10:04:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 12 Mar 2024 10:04:10 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 12 Mar 2024 10:06:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 12 Mar 2024 10:06:41 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 12 Mar 2024 10:06:42 GMT
RUN docker-php-ext-enable sodium
# Tue, 12 Mar 2024 10:06:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 12 Mar 2024 10:06:42 GMT
STOPSIGNAL SIGWINCH
# Tue, 12 Mar 2024 10:06:42 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 12 Mar 2024 10:06:42 GMT
WORKDIR /var/www/html
# Tue, 12 Mar 2024 10:06:42 GMT
EXPOSE 80
# Tue, 12 Mar 2024 10:06:42 GMT
CMD ["apache2-foreground"]
# Tue, 12 Mar 2024 17:21:29 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Tue, 12 Mar 2024 17:21:30 GMT
ENV PHP_MEMORY_LIMIT=512M
# Tue, 12 Mar 2024 17:21:30 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Tue, 12 Mar 2024 17:23:14 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.23;     pecl install imagick-3.7.0;     pecl install memcached-3.2.0;     pecl install redis-6.0.2;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 17:23:15 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Tue, 12 Mar 2024 17:23:15 GMT
VOLUME [/var/www/html]
# Tue, 12 Mar 2024 17:23:16 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip
# Tue, 12 Mar 2024 17:23:16 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Tue, 12 Mar 2024 17:23:16 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits
# Tue, 12 Mar 2024 17:35:21 GMT
ENV NEXTCLOUD_VERSION=28.0.3
# Tue, 12 Mar 2024 17:36:02 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-28.0.3.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-28.0.3.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 17:36:12 GMT
COPY multi:9585a9602f24ff6c37b7e8821d7e5fca4a450cd9cc8c66163bc629028ca3df5c in / 
# Tue, 12 Mar 2024 17:36:12 GMT
COPY multi:325eebb30e6912e4cdbb030d4d22b6dd14fe18ca007f50df3afe27a136e1e383 in /usr/src/nextcloud/config/ 
# Tue, 12 Mar 2024 17:36:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Mar 2024 17:36:12 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:9cada496cd2b8a88571bf23d513e7fce34888d13321fcf23c6613bffe4c37297`  
		Last Modified: Tue, 12 Mar 2024 01:21:14 GMT  
		Size: 27.5 MB (27488684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83d4ad3e3b59b6f54b9dcef6cff0e4615b6fa3f96f1de12d8fbeb94f7acd29b7`  
		Last Modified: Tue, 12 Mar 2024 11:15:26 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d83835687d69ef2513b8d805100ebc4726b162f3aa9efd0cddf617127b689d25`  
		Last Modified: Tue, 12 Mar 2024 11:15:38 GMT  
		Size: 80.8 MB (80808055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e8349341cc698ac8bb86ba42ea145c47faa3f81cf9c660f105f493fc148300`  
		Last Modified: Tue, 12 Mar 2024 11:15:25 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f500bb0818505be871db98ada53fff2905523f39443d3b8203de073d18275d0a`  
		Last Modified: Tue, 12 Mar 2024 11:15:58 GMT  
		Size: 20.1 MB (20083383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e602f9cc745a947e1f5e2c99c194cfdeb52cdca3fd07aa735f0135752b146e3`  
		Last Modified: Tue, 12 Mar 2024 11:15:55 GMT  
		Size: 470.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f8dc84c4882804775f8abd94bf231325b2f7e4b4812cc6aba73dfb838aad26`  
		Last Modified: Tue, 12 Mar 2024 11:15:55 GMT  
		Size: 511.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca468ba526cd2c7fec037653707562d5916cd168db8c0859fcabec26c70510c0`  
		Last Modified: Tue, 12 Mar 2024 11:22:14 GMT  
		Size: 12.4 MB (12417176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9a550616984a065d30e4e9b3e6262b6c57f7ad313d9f9a60a32fa1b501d0755`  
		Last Modified: Tue, 12 Mar 2024 11:22:12 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29eebbfaf5193017e67d8c128bb37da490087139a0d750138e3108aa5ff62773`  
		Last Modified: Tue, 12 Mar 2024 11:22:14 GMT  
		Size: 10.4 MB (10448899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b05d0d2639b28164885bef365c56a15fc7801c06bda449cfe60a45a8b37104`  
		Last Modified: Tue, 12 Mar 2024 11:22:12 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e87cf9b379057c46e298974204c7789553679d139545c3d6c3b0cbe83e761542`  
		Last Modified: Tue, 12 Mar 2024 11:22:13 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c009efc65d3b963fe0e596fab3081ab0fae8f60a353c51a34eb771274ddc82a0`  
		Last Modified: Tue, 12 Mar 2024 11:22:12 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5bd17428d5cd71315017aaea6ee56e1f87a0dafa7557ae9e8bc62e3fe13118d`  
		Last Modified: Tue, 12 Mar 2024 17:40:59 GMT  
		Size: 19.3 MB (19294865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd89855147a08b9b2d494cdd87d5d65b9b43cd0337009b70bae0c5c8f83462c`  
		Last Modified: Tue, 12 Mar 2024 17:41:00 GMT  
		Size: 20.1 MB (20128934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a935d50392e0ba342f4a6baf3b518e098687ebf48d9b0147514f137456c0008`  
		Last Modified: Tue, 12 Mar 2024 17:40:57 GMT  
		Size: 761.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c77b5a825ca8211dffac056b634c59cb598be0d4a08047b67e1c205551b8589`  
		Last Modified: Tue, 12 Mar 2024 17:40:56 GMT  
		Size: 573.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c4dd78fb015b2366bba74772dc0e25d4a43531d85f868b55887f53d66a943e`  
		Last Modified: Tue, 12 Mar 2024 17:40:56 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e6cfff583b3de718b919c23349274dc3f7c8418949ba28be1267d04954b54ae`  
		Last Modified: Tue, 12 Mar 2024 17:43:36 GMT  
		Size: 201.3 MB (201323226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42bca10110acc7f2c327fc7d9a36c98894677a436ef9667a988906302fd42d60`  
		Last Modified: Tue, 12 Mar 2024 17:43:14 GMT  
		Size: 3.6 KB (3613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0906b3c82e75a960fb0e20c57a1f91020500f329c287b0be7dd9cfab4aeb228`  
		Last Modified: Tue, 12 Mar 2024 17:43:14 GMT  
		Size: 2.4 KB (2395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
