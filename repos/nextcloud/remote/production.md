## `nextcloud:production`

```console
$ docker pull nextcloud@sha256:64c2ba8de9608b26c90b12df815b8fd4b8f0cddf1ce4ea699ff8a43e94fd0830
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

### `nextcloud:production` - linux; amd64

```console
$ docker pull nextcloud@sha256:14a4b28b0efec0cd8b7db4449c73ae43ef445cfabc4d720e4b9f8257a82b02a8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **442.8 MB (442773458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0173aea98add713ba583b49c13823e85b34bec82b5fb5f39bbc08666cbeeab4b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:32 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Fri, 27 Sep 2024 04:29:32 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:40:06 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 27 Sep 2024 05:40:06 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 27 Sep 2024 05:40:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:40:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 27 Sep 2024 05:40:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 27 Sep 2024 05:44:30 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 27 Sep 2024 05:44:30 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 27 Sep 2024 05:44:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 27 Sep 2024 05:44:38 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 27 Sep 2024 05:44:39 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 27 Sep 2024 05:44:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Sep 2024 05:44:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Sep 2024 05:44:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 27 Sep 2024 06:45:24 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 27 Sep 2024 06:45:24 GMT
ENV PHP_VERSION=8.2.24
# Fri, 27 Sep 2024 06:45:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.24.tar.xz.asc
# Fri, 27 Sep 2024 06:45:24 GMT
ENV PHP_SHA256=80a5225746a9eb484475b312d4c626c63a88a037d8e56d214f30205e1ba1411a
# Fri, 27 Sep 2024 06:45:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 27 Sep 2024 06:45:33 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 27 Sep 2024 06:49:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 27 Sep 2024 06:49:05 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 27 Sep 2024 06:49:06 GMT
RUN docker-php-ext-enable sodium
# Fri, 27 Sep 2024 06:49:06 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 27 Sep 2024 06:49:06 GMT
STOPSIGNAL SIGWINCH
# Fri, 27 Sep 2024 06:49:06 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 27 Sep 2024 06:49:06 GMT
WORKDIR /var/www/html
# Fri, 27 Sep 2024 06:49:06 GMT
EXPOSE 80
# Fri, 27 Sep 2024 06:49:06 GMT
CMD ["apache2-foreground"]
# Fri, 27 Sep 2024 09:55:39 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Fri, 27 Sep 2024 09:55:39 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 27 Sep 2024 09:55:39 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 27 Sep 2024 09:58:31 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.23;     pecl install imagick-3.7.0;     pecl install memcached-3.2.0;     pecl install redis-6.0.2;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 09:58:32 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 27 Sep 2024 09:58:32 GMT
VOLUME [/var/www/html]
# Fri, 27 Sep 2024 09:58:32 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip
# Fri, 27 Sep 2024 09:58:33 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Fri, 27 Sep 2024 09:58:33 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits
# Fri, 27 Sep 2024 10:04:01 GMT
ENV NEXTCLOUD_VERSION=29.0.7
# Fri, 27 Sep 2024 10:05:01 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-29.0.7.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-29.0.7.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 10:05:04 GMT
COPY multi:f3c1a1c702869b782886f0f296503f363039f205d0235bcaa3e4e0fa8b0d1d39 in / 
# Fri, 27 Sep 2024 10:05:05 GMT
COPY multi:26b6011f3864a7a1d1a6de6eafef4f376d2e08f7f7b1ef21b94e6d2658564826 in /usr/src/nextcloud/config/ 
# Fri, 27 Sep 2024 10:05:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 27 Sep 2024 10:05:05 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07fc0890b857ec241446d5da032bf36da2a006ce8868ba150a76a1ee16772b39`  
		Last Modified: Fri, 27 Sep 2024 07:40:54 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141aa7d58c576d5efbf995cfdd139044be15add60b2f0e5f7b295fdc4cc511d3`  
		Last Modified: Fri, 27 Sep 2024 07:41:08 GMT  
		Size: 104.3 MB (104345685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2720d4bca8b3db19acbea04618296e463e4cde1df16c277954505ad4e50893eb`  
		Last Modified: Fri, 27 Sep 2024 07:40:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82deca51468c5fb0464e6db26d14da0d5605682524cb4acfafbbc7cc55a2b20e`  
		Last Modified: Fri, 27 Sep 2024 07:41:32 GMT  
		Size: 20.3 MB (20327579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dec741dfa52689fcf27c3934a0b87bdaefb62c643d04fe352f88589f791315e9`  
		Last Modified: Fri, 27 Sep 2024 07:41:29 GMT  
		Size: 437.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e204b0efab9499a1608734207890fb199b60d100af89f57dc74f1ca26a00f8d5`  
		Last Modified: Fri, 27 Sep 2024 07:41:29 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a9b8825ee85fc4938aaf820f3caf1223417b94afec555058896f5b22507694b`  
		Last Modified: Fri, 27 Sep 2024 07:47:14 GMT  
		Size: 12.4 MB (12443162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef45e9da2633a738d27d41da1df46c1f67f160743fab61eba2df3a7c35a22289`  
		Last Modified: Fri, 27 Sep 2024 07:47:11 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b46378d521434bae6da351a128bfab45a8b2231106fd1bd946aa5220eea6a8`  
		Last Modified: Fri, 27 Sep 2024 07:47:13 GMT  
		Size: 11.4 MB (11410499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c104459ddadb2f472d9239c9d997b1f6163c8e5c7307aa24b0e78693c56cd9c`  
		Last Modified: Fri, 27 Sep 2024 07:47:11 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:282db878d4dda03bc59a283134735a2b602fad3e0d969b40d2159a55659cb8d8`  
		Last Modified: Fri, 27 Sep 2024 07:47:12 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a1f827cc210d8b001bc4c20ca2cb4dbc5679cff500d40ff52e89d8bc24c5b20`  
		Last Modified: Fri, 27 Sep 2024 07:47:11 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b0175ce22bc7e6bbc50e3ebb46367938d3c52b1fe274b782c7da94fc282385`  
		Last Modified: Fri, 27 Sep 2024 10:09:14 GMT  
		Size: 22.8 MB (22785245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c5a6809b8e4befd0016fd623fe0f056aa85ce1ee67807c7ed91ebb6f97c957`  
		Last Modified: Fri, 27 Sep 2024 10:09:14 GMT  
		Size: 20.9 MB (20941555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6e1898703957a9efaaf126ef6f87b71a70ef3435f724a91304e583c93c877e`  
		Last Modified: Fri, 27 Sep 2024 10:09:10 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b33e1abcd0dc26a54cc0c93a900abab2d4f19292fbd938019a4c7a8bdcba734`  
		Last Modified: Fri, 27 Sep 2024 10:09:08 GMT  
		Size: 572.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c562c44a9a3bad09a4a35c9f5106046be61aaa8a6859dc07ecef25bda9ed3e5`  
		Last Modified: Fri, 27 Sep 2024 10:09:08 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4abcea02ca67d859e825b582386e5ff820e808beacdfb07cf4d4086a921aa3`  
		Last Modified: Fri, 27 Sep 2024 10:11:03 GMT  
		Size: 221.4 MB (221380080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f337570d3f3afd2d2acc4aaa75893820e22e4722abf29d054311e03f9c23e6a6`  
		Last Modified: Fri, 27 Sep 2024 10:10:36 GMT  
		Size: 3.9 KB (3879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a7de34fbcd98e869dffbd15d24819cbdd43b263cf070cb9ec45b16fcd342f26`  
		Last Modified: Fri, 27 Sep 2024 10:10:37 GMT  
		Size: 2.4 KB (2369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:production` - linux; arm variant v5

```console
$ docker pull nextcloud@sha256:b1edc56dc0b303aedcdde9a2359a9fd82ef05724240cc1557931f2df0e7808b0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **412.3 MB (412261482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2705e44f78f8e47bf9a9d8dbe470e76009e30c4a8c24842cd13375c639b5f053`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 27 Sep 2024 03:19:20 GMT
ADD file:91b876c600b7d3198bc98296224f6861440f56fcbd15a2188c95a8785b94061a in / 
# Fri, 27 Sep 2024 03:19:20 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 04:06:51 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 27 Sep 2024 04:06:51 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 27 Sep 2024 04:07:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 04:07:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 27 Sep 2024 04:07:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 27 Sep 2024 04:10:28 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 27 Sep 2024 04:10:28 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 27 Sep 2024 04:10:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 27 Sep 2024 04:10:42 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 27 Sep 2024 04:10:43 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 27 Sep 2024 04:10:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Sep 2024 04:10:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Sep 2024 04:10:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 27 Sep 2024 04:36:01 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 27 Sep 2024 04:36:01 GMT
ENV PHP_VERSION=8.2.24
# Fri, 27 Sep 2024 04:36:01 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.24.tar.xz.asc
# Fri, 27 Sep 2024 04:36:01 GMT
ENV PHP_SHA256=80a5225746a9eb484475b312d4c626c63a88a037d8e56d214f30205e1ba1411a
# Fri, 27 Sep 2024 04:36:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 27 Sep 2024 04:36:12 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 27 Sep 2024 04:39:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 27 Sep 2024 04:39:02 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 27 Sep 2024 04:39:02 GMT
RUN docker-php-ext-enable sodium
# Fri, 27 Sep 2024 04:39:02 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 27 Sep 2024 04:39:03 GMT
STOPSIGNAL SIGWINCH
# Fri, 27 Sep 2024 04:39:03 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 27 Sep 2024 04:39:03 GMT
WORKDIR /var/www/html
# Fri, 27 Sep 2024 04:39:03 GMT
EXPOSE 80
# Fri, 27 Sep 2024 04:39:03 GMT
CMD ["apache2-foreground"]
# Fri, 27 Sep 2024 06:29:04 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Fri, 27 Sep 2024 06:29:04 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 27 Sep 2024 06:29:05 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 27 Sep 2024 06:31:48 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.23;     pecl install imagick-3.7.0;     pecl install memcached-3.2.0;     pecl install redis-6.0.2;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 06:31:49 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 27 Sep 2024 06:31:49 GMT
VOLUME [/var/www/html]
# Fri, 27 Sep 2024 06:31:50 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip
# Fri, 27 Sep 2024 06:31:50 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Fri, 27 Sep 2024 06:31:50 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits
# Fri, 27 Sep 2024 06:37:49 GMT
ENV NEXTCLOUD_VERSION=29.0.7
# Fri, 27 Sep 2024 06:38:52 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-29.0.7.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-29.0.7.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 06:38:53 GMT
COPY multi:f3c1a1c702869b782886f0f296503f363039f205d0235bcaa3e4e0fa8b0d1d39 in / 
# Fri, 27 Sep 2024 06:38:53 GMT
COPY multi:26b6011f3864a7a1d1a6de6eafef4f376d2e08f7f7b1ef21b94e6d2658564826 in /usr/src/nextcloud/config/ 
# Fri, 27 Sep 2024 06:38:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 27 Sep 2024 06:38:53 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:75a20c44e8becd141ba586ea413a1649251437a207502d4f8ad23d208f013e60`  
		Last Modified: Fri, 27 Sep 2024 03:21:44 GMT  
		Size: 26.9 MB (26887302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4abee9b0737593e9835dc555292a01c58c3fb19f389ffbb556e3ec83d8222c6`  
		Last Modified: Fri, 27 Sep 2024 04:57:48 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e5de77c609405dc64f2e8c8206bbec62da53ccc60aedc603672b7a337a412b`  
		Last Modified: Fri, 27 Sep 2024 04:58:03 GMT  
		Size: 82.0 MB (81995092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ddddd6ae7c7fda37305d6bc5117d36ac423f550ff4c6ad424d1de53e6b2a1e0`  
		Last Modified: Fri, 27 Sep 2024 04:57:48 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deccef66bda4d8995be278ceb309f484f6a52595d369da981611dc922e98e887`  
		Last Modified: Fri, 27 Sep 2024 04:58:27 GMT  
		Size: 19.6 MB (19624329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f63ad9166a15b4f481cc55af64fe92ea1c78d1a77d1d9d16f34bf495afdfae`  
		Last Modified: Fri, 27 Sep 2024 04:58:23 GMT  
		Size: 438.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5517924e644a07b5b6ba20a6189dc63a69c99f73da7e8bdb535bfaccaa37d098`  
		Last Modified: Fri, 27 Sep 2024 04:58:23 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5c677df6d5476e48e4baa887258617c6a7576a325e67648fc267a220d369f54`  
		Last Modified: Fri, 27 Sep 2024 05:01:39 GMT  
		Size: 12.4 MB (12441482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bda9f496be5aa5db0b1d6e3664dd26fe0666eb2a36923852b0868a36fb85d36`  
		Last Modified: Fri, 27 Sep 2024 05:01:36 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e0b7c20e5283235884f774e80308adf04635a2b1feca80c7ce774308998c08d`  
		Last Modified: Fri, 27 Sep 2024 05:01:38 GMT  
		Size: 10.4 MB (10393961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96d8ab1b0bf6a03e6e4f110b639f8253e8ed42d8f83384886aef8b2c3c03a9bd`  
		Last Modified: Fri, 27 Sep 2024 05:01:36 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98f7c1756f2245c74a6ba06a4ea90201af8defbdacb29d54cd600763ab088cfe`  
		Last Modified: Fri, 27 Sep 2024 05:01:36 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:954b26bee1c396a1d68f9a9d15f0e1916e6614cf9a064c105c0331fd6b4f9219`  
		Last Modified: Fri, 27 Sep 2024 05:01:36 GMT  
		Size: 892.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc06e5b61976e238d881dab8b55e62d7cad41cdd1495ea29dff910c067211b69`  
		Last Modified: Fri, 27 Sep 2024 06:43:41 GMT  
		Size: 19.9 MB (19896733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c71c47cef8ba92acf63e96a382cdf2179f896aefdb7d6ca6be4d1452e3911f1b`  
		Last Modified: Fri, 27 Sep 2024 06:43:42 GMT  
		Size: 19.6 MB (19631618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc85a4ca59fae41f2523cb73e57f0e1d882553a4e7c392553c3e8268c214fe69`  
		Last Modified: Fri, 27 Sep 2024 06:43:37 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8af97d624ae83b25ec1ff0c559f2f0ea50771bf8099e42dea1e59952b4ace8`  
		Last Modified: Fri, 27 Sep 2024 06:43:36 GMT  
		Size: 575.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e3bffaa3a0098f990fcbaa361e30d6c56ae5b7cc768ced2acea516871b1797`  
		Last Modified: Fri, 27 Sep 2024 06:43:36 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75dc58eb40b1dfc323cc83341779f0fc7b75a6ee562763a1602cfaf01eeb9976`  
		Last Modified: Fri, 27 Sep 2024 06:45:56 GMT  
		Size: 221.4 MB (221377569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2854b05199086023afa8eed494b36658750dbf17e6cef522842f5f9801b1795`  
		Last Modified: Fri, 27 Sep 2024 06:45:23 GMT  
		Size: 3.9 KB (3880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c7b503a859bb3222624d10a2cd9822beeaa96e2407d7310a29149ecf1b8b2c9`  
		Last Modified: Fri, 27 Sep 2024 06:45:23 GMT  
		Size: 2.4 KB (2368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:production` - linux; arm variant v7

```console
$ docker pull nextcloud@sha256:4b152a88a128ad65aa749f829febb272cc0bc7554ead0be3411662490af34bdd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.7 MB (400698455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:756d50d9e64937dd6aba846186f3ea6f8367910c74619500d63ed6484f4fba31`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 27 Sep 2024 05:13:46 GMT
ADD file:7eec8434e7851a0c9296426e66771b108dd584ea08a7e2aaec3ec3077c58bf89 in / 
# Fri, 27 Sep 2024 05:13:46 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:37:54 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 27 Sep 2024 05:37:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 27 Sep 2024 05:38:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:38:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 27 Sep 2024 05:38:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 27 Sep 2024 05:41:17 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 27 Sep 2024 05:41:17 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 27 Sep 2024 05:41:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 27 Sep 2024 05:41:29 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 27 Sep 2024 05:41:29 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 27 Sep 2024 05:41:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Sep 2024 05:41:30 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Sep 2024 05:41:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 27 Sep 2024 06:27:16 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 27 Sep 2024 06:27:16 GMT
ENV PHP_VERSION=8.2.24
# Fri, 27 Sep 2024 06:27:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.24.tar.xz.asc
# Fri, 27 Sep 2024 06:27:16 GMT
ENV PHP_SHA256=80a5225746a9eb484475b312d4c626c63a88a037d8e56d214f30205e1ba1411a
# Fri, 27 Sep 2024 06:27:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 27 Sep 2024 06:27:41 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 27 Sep 2024 06:30:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 27 Sep 2024 06:30:12 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 27 Sep 2024 06:30:13 GMT
RUN docker-php-ext-enable sodium
# Fri, 27 Sep 2024 06:30:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 27 Sep 2024 06:30:13 GMT
STOPSIGNAL SIGWINCH
# Fri, 27 Sep 2024 06:30:13 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 27 Sep 2024 06:30:13 GMT
WORKDIR /var/www/html
# Fri, 27 Sep 2024 06:30:13 GMT
EXPOSE 80
# Fri, 27 Sep 2024 06:30:13 GMT
CMD ["apache2-foreground"]
# Fri, 27 Sep 2024 07:48:20 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Fri, 27 Sep 2024 07:48:21 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 27 Sep 2024 07:48:21 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 27 Sep 2024 07:51:10 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.23;     pecl install imagick-3.7.0;     pecl install memcached-3.2.0;     pecl install redis-6.0.2;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 07:51:11 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 27 Sep 2024 07:51:11 GMT
VOLUME [/var/www/html]
# Fri, 27 Sep 2024 07:51:12 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip
# Fri, 27 Sep 2024 07:51:12 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Fri, 27 Sep 2024 07:51:12 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits
# Fri, 27 Sep 2024 08:00:29 GMT
ENV NEXTCLOUD_VERSION=29.0.7
# Fri, 27 Sep 2024 08:01:49 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-29.0.7.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-29.0.7.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 08:01:55 GMT
COPY multi:f3c1a1c702869b782886f0f296503f363039f205d0235bcaa3e4e0fa8b0d1d39 in / 
# Fri, 27 Sep 2024 08:01:59 GMT
COPY multi:26b6011f3864a7a1d1a6de6eafef4f376d2e08f7f7b1ef21b94e6d2658564826 in /usr/src/nextcloud/config/ 
# Fri, 27 Sep 2024 08:01:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 27 Sep 2024 08:02:00 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:2136499185ba9023c6db11bbc836b6c428da7969aa7db3ccaac576a10052c9ce`  
		Last Modified: Fri, 27 Sep 2024 05:17:12 GMT  
		Size: 24.7 MB (24718145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b4b796e3156825c9c7128cd43753f55a7b4846d8bb402dd9a77a8abe211f01`  
		Last Modified: Fri, 27 Sep 2024 07:09:08 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56632fe12bcb53322059eec59ebb6d32be677cd5a7660f8c58dcbae4c842f7f4`  
		Last Modified: Fri, 27 Sep 2024 07:09:25 GMT  
		Size: 76.2 MB (76163133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb66744d163056f62ac800c7c39d0b124a45a20946685aaa7af12a7294b6dd0`  
		Last Modified: Fri, 27 Sep 2024 07:09:08 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ee92f2ee8b075bcd1aeef5d185504ff3e36174d27b571c1d00d251e4aac01f2`  
		Last Modified: Fri, 27 Sep 2024 07:09:50 GMT  
		Size: 19.1 MB (19062052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43b487640b16be1e8dd3173f866dd400247e62d55fa7a367338223039daed09`  
		Last Modified: Fri, 27 Sep 2024 07:09:47 GMT  
		Size: 439.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d6909db46b1f42af9fe07c4658e5b551d5f0614c90d2978ebd00ec8d848ef4`  
		Last Modified: Fri, 27 Sep 2024 07:09:47 GMT  
		Size: 488.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac1fd045a39ba4953541f44d7851fd9b237e55adaeedea075bfe91032734c6c`  
		Last Modified: Fri, 27 Sep 2024 07:15:50 GMT  
		Size: 12.4 MB (12441480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6de6931d84a75584f61b609601c48975c336bc36f0a0521b0b418171309212e`  
		Last Modified: Fri, 27 Sep 2024 07:15:47 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48dc2fb30d7dec3cc4329141d1b25c214b16c99c1c9dbb3c6af56b780c87a77c`  
		Last Modified: Fri, 27 Sep 2024 07:15:50 GMT  
		Size: 9.8 MB (9825870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3981dd0e5135caf2c7aecbe83a4f7b9fc4186f5d9dabb45ca08a53e81bf8782`  
		Last Modified: Fri, 27 Sep 2024 07:15:47 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd176459f376d553b627b1d938e16095194a321ee199af16f8f8a43a20048084`  
		Last Modified: Fri, 27 Sep 2024 07:15:47 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9d2e67247d94640f766196e0f61a630acafb24ba54ae54526a29c8d877bc248`  
		Last Modified: Fri, 27 Sep 2024 07:15:47 GMT  
		Size: 892.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6893be54ac998ca295f11b2901752b13b9eeccfc249919f04beb13b27606399`  
		Last Modified: Fri, 27 Sep 2024 08:08:06 GMT  
		Size: 18.1 MB (18140931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef50e024cf921087ca2364d77945c8d37b3c2054dab8565b41d957ee73c8abe`  
		Last Modified: Fri, 27 Sep 2024 08:08:09 GMT  
		Size: 19.0 MB (18955936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:382c08baa25a6ee45bf85b5cfc703b1d6669d6717878d6db2c572b499308c9d4`  
		Last Modified: Fri, 27 Sep 2024 08:07:59 GMT  
		Size: 709.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e93ea1c8180a8c949c71f31d6a45e039ff216e1c0e0479684695361830fd0ef2`  
		Last Modified: Fri, 27 Sep 2024 08:07:58 GMT  
		Size: 575.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6adfb866e9b22184497518cb65e38309f6fcd7c4cebd774d06a494b20ed7d05b`  
		Last Modified: Fri, 27 Sep 2024 08:07:58 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e051919897bec0c0c5274fe1fdb6850d1c695946eb901183a0052fdf057571`  
		Last Modified: Fri, 27 Sep 2024 08:10:45 GMT  
		Size: 221.4 MB (221377512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03970451712d084eac011996cf8b06ca839f02067fb7b955d9940775ef90e889`  
		Last Modified: Fri, 27 Sep 2024 08:10:04 GMT  
		Size: 3.9 KB (3880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e371f823c14bdbc6249b0fae6594efbe5c53c43807ed6f7b4c994ebdffbc20`  
		Last Modified: Fri, 27 Sep 2024 08:10:04 GMT  
		Size: 2.4 KB (2370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:production` - linux; arm64 variant v8

```console
$ docker pull nextcloud@sha256:53aa7a6bc3f0fbebc0cd72d05c59e738f7dac40964d67f8efd80f14e2c28a34d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.2 MB (434182319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd566be601325b03faa0565007e2ce36d2c45266a07ae5ef261d97ed724b6cd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:17 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Fri, 27 Sep 2024 04:38:18 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:31:21 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 27 Sep 2024 05:31:21 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 27 Sep 2024 05:31:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:31:37 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 27 Sep 2024 05:31:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 27 Sep 2024 05:34:43 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 27 Sep 2024 05:34:43 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 27 Sep 2024 05:34:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 27 Sep 2024 05:34:51 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 27 Sep 2024 05:34:52 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 27 Sep 2024 05:34:52 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Sep 2024 05:34:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Sep 2024 05:34:52 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 27 Sep 2024 06:26:43 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 27 Sep 2024 06:26:43 GMT
ENV PHP_VERSION=8.2.24
# Fri, 27 Sep 2024 06:26:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.24.tar.xz.asc
# Fri, 27 Sep 2024 06:26:44 GMT
ENV PHP_SHA256=80a5225746a9eb484475b312d4c626c63a88a037d8e56d214f30205e1ba1411a
# Fri, 27 Sep 2024 06:26:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 27 Sep 2024 06:26:52 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 27 Sep 2024 06:30:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 27 Sep 2024 06:30:06 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 27 Sep 2024 06:30:06 GMT
RUN docker-php-ext-enable sodium
# Fri, 27 Sep 2024 06:30:06 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 27 Sep 2024 06:30:06 GMT
STOPSIGNAL SIGWINCH
# Fri, 27 Sep 2024 06:30:06 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 27 Sep 2024 06:30:07 GMT
WORKDIR /var/www/html
# Fri, 27 Sep 2024 06:30:07 GMT
EXPOSE 80
# Fri, 27 Sep 2024 06:30:07 GMT
CMD ["apache2-foreground"]
# Fri, 27 Sep 2024 08:57:03 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Fri, 27 Sep 2024 08:57:03 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 27 Sep 2024 08:57:04 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 27 Sep 2024 08:59:56 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.23;     pecl install imagick-3.7.0;     pecl install memcached-3.2.0;     pecl install redis-6.0.2;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 08:59:56 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 27 Sep 2024 08:59:56 GMT
VOLUME [/var/www/html]
# Fri, 27 Sep 2024 08:59:57 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip
# Fri, 27 Sep 2024 08:59:57 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Fri, 27 Sep 2024 08:59:57 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits
# Fri, 27 Sep 2024 09:05:12 GMT
ENV NEXTCLOUD_VERSION=29.0.7
# Fri, 27 Sep 2024 09:06:04 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-29.0.7.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-29.0.7.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 09:06:10 GMT
COPY multi:f3c1a1c702869b782886f0f296503f363039f205d0235bcaa3e4e0fa8b0d1d39 in / 
# Fri, 27 Sep 2024 09:06:10 GMT
COPY multi:26b6011f3864a7a1d1a6de6eafef4f376d2e08f7f7b1ef21b94e6d2658564826 in /usr/src/nextcloud/config/ 
# Fri, 27 Sep 2024 09:06:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 27 Sep 2024 09:06:10 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4075a2a900cbcc12ab034169fddf2bcdd894e0953be6ad883c380b275350502`  
		Last Modified: Fri, 27 Sep 2024 07:16:46 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd31999ed1795da18acdfe1dd60f9dde145223af54a887ef424786e8e885b85`  
		Last Modified: Fri, 27 Sep 2024 07:16:57 GMT  
		Size: 98.1 MB (98130981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:131265d95889b23e897a24b57123c95173e80ddd3d485f561737530371309615`  
		Last Modified: Fri, 27 Sep 2024 07:16:46 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a5d1249bb626a5f47a598928fd07fd4a19ad72531ffba7cc72915271a3ba1d8`  
		Last Modified: Fri, 27 Sep 2024 07:17:20 GMT  
		Size: 20.3 MB (20325543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a5db4ebb80f5842a34d9507b254e11285a6960058a9b8d5a6dcc4673b6167a3`  
		Last Modified: Fri, 27 Sep 2024 07:17:18 GMT  
		Size: 435.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1b2c6cdce0afc5c6e74c307dde16e25accbd2baad830908593184e9eba9d5d`  
		Last Modified: Fri, 27 Sep 2024 07:17:18 GMT  
		Size: 485.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6809e2f715ec177dbbff79e3215a246b238b8be6fc552cd8163304052389d56d`  
		Last Modified: Fri, 27 Sep 2024 07:22:47 GMT  
		Size: 12.4 MB (12442902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e8ce1d2fb13190d056cca21991ed3b93dade5f0256c936bc73111122b2a0db5`  
		Last Modified: Fri, 27 Sep 2024 07:22:45 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f6f00aafc3aba1e10cf12c5288378abcfe9e3ab2c91afb19c4c49d04f667534`  
		Last Modified: Fri, 27 Sep 2024 07:22:47 GMT  
		Size: 11.4 MB (11417828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1c42fd6a2f0ac25ab85f0e381c2b4b3945389a72179fcba1f35a0e8f19e85e1`  
		Last Modified: Fri, 27 Sep 2024 07:22:45 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c14eb04cdbad42f193a85516eb527e0ca84feca060cb5370cbc74e332a7dcc2`  
		Last Modified: Fri, 27 Sep 2024 07:22:45 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74353b86439842c9b13e968a6b50774677e15759fb0cf22189dc97975efb5f39`  
		Last Modified: Fri, 27 Sep 2024 07:22:45 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a74133d7d76d30f7ec3425a4047bc10e6676922c9d38c4cae499000d89fb691d`  
		Last Modified: Fri, 27 Sep 2024 09:10:07 GMT  
		Size: 20.1 MB (20148875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79695eb0a1e3deee6aa681025847d54c1557de2d332984808da2ae98fa4345b`  
		Last Modified: Fri, 27 Sep 2024 09:10:08 GMT  
		Size: 21.2 MB (21166663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6612c936a80a0b414155606266af30117064233de081e69a2326e25a881ba2`  
		Last Modified: Fri, 27 Sep 2024 09:10:04 GMT  
		Size: 709.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f36fca33b0afea08bf3743b712df085cbde3ebfe56c649bab182b4a2b22c8cc`  
		Last Modified: Fri, 27 Sep 2024 09:10:02 GMT  
		Size: 573.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19db9d20ac0e06ae761b04c684380ebcfbff53e8f1896dcd48cc125c95c6ba3`  
		Last Modified: Fri, 27 Sep 2024 09:10:02 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74452d3203821e4430be8d2cd74f27c445cd57d1f6210fe3483c5e617016939a`  
		Last Modified: Fri, 27 Sep 2024 09:11:46 GMT  
		Size: 221.4 MB (221379775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d359df06ba599f88017a399e9a0f3649c9b7f91ad43045377edce6f3273de929`  
		Last Modified: Fri, 27 Sep 2024 09:11:25 GMT  
		Size: 3.9 KB (3880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6848409616332d55e459d191826c86c28762ffd8c365715020a5e9b1f49968e0`  
		Last Modified: Fri, 27 Sep 2024 09:11:25 GMT  
		Size: 2.4 KB (2370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:production` - linux; 386

```console
$ docker pull nextcloud@sha256:034574dd07d232565b039b888949b1a94c2efa2dd50b4f667ed3b2c7a2d7831c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **441.4 MB (441396289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8e9b05d9bd2663b7ce3a05a73b2d464ca26a2e7499ac35807b6afbcb93baf20`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 27 Sep 2024 07:23:00 GMT
ADD file:7ad74dd13b6c84de2920c6d09de06e914d0b78ba06ae75260d6e6ff344a4b024 in / 
# Fri, 27 Sep 2024 07:23:01 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 08:12:16 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 27 Sep 2024 08:12:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 27 Sep 2024 08:12:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 08:12:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 27 Sep 2024 08:12:42 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 27 Sep 2024 08:19:39 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 27 Sep 2024 08:19:39 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 27 Sep 2024 08:19:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 27 Sep 2024 08:19:50 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 27 Sep 2024 08:19:51 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 27 Sep 2024 08:19:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Sep 2024 08:19:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Sep 2024 08:19:51 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 27 Sep 2024 10:00:57 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 27 Sep 2024 10:00:57 GMT
ENV PHP_VERSION=8.2.24
# Fri, 27 Sep 2024 10:00:57 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.24.tar.xz.asc
# Fri, 27 Sep 2024 10:00:58 GMT
ENV PHP_SHA256=80a5225746a9eb484475b312d4c626c63a88a037d8e56d214f30205e1ba1411a
# Fri, 27 Sep 2024 10:01:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 27 Sep 2024 10:01:09 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 27 Sep 2024 10:07:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 27 Sep 2024 10:07:16 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 27 Sep 2024 10:07:16 GMT
RUN docker-php-ext-enable sodium
# Fri, 27 Sep 2024 10:07:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 27 Sep 2024 10:07:17 GMT
STOPSIGNAL SIGWINCH
# Fri, 27 Sep 2024 10:07:17 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 27 Sep 2024 10:07:17 GMT
WORKDIR /var/www/html
# Fri, 27 Sep 2024 10:07:17 GMT
EXPOSE 80
# Fri, 27 Sep 2024 10:07:17 GMT
CMD ["apache2-foreground"]
# Fri, 27 Sep 2024 13:42:10 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Fri, 27 Sep 2024 13:42:10 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 27 Sep 2024 13:42:10 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 27 Sep 2024 13:45:52 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.23;     pecl install imagick-3.7.0;     pecl install memcached-3.2.0;     pecl install redis-6.0.2;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 13:45:53 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 27 Sep 2024 13:45:53 GMT
VOLUME [/var/www/html]
# Fri, 27 Sep 2024 13:45:54 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip
# Fri, 27 Sep 2024 13:45:54 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Fri, 27 Sep 2024 13:45:55 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits
# Fri, 27 Sep 2024 13:51:58 GMT
ENV NEXTCLOUD_VERSION=29.0.7
# Fri, 27 Sep 2024 13:53:07 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-29.0.7.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-29.0.7.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 13:53:10 GMT
COPY multi:f3c1a1c702869b782886f0f296503f363039f205d0235bcaa3e4e0fa8b0d1d39 in / 
# Fri, 27 Sep 2024 13:53:11 GMT
COPY multi:26b6011f3864a7a1d1a6de6eafef4f376d2e08f7f7b1ef21b94e6d2658564826 in /usr/src/nextcloud/config/ 
# Fri, 27 Sep 2024 13:53:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 27 Sep 2024 13:53:11 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:c953524ed27d53ce5e7d4e7487137789de73f4058e96b05284eefbcae1b47c26`  
		Last Modified: Fri, 27 Sep 2024 07:27:04 GMT  
		Size: 30.1 MB (30144216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:138795898cf1de35ac46bb272c1c2476a14caa25663387836c955b1d89e2f74e`  
		Last Modified: Fri, 27 Sep 2024 11:31:40 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86ec2d8cda04ca38232896364bf367b18146c275503f43c81e6298173cc87253`  
		Last Modified: Fri, 27 Sep 2024 11:32:02 GMT  
		Size: 101.5 MB (101514377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02e654bcb676bf538ed8701ea1e8b582043bd3457c58bfc84a0010d5d901176`  
		Last Modified: Fri, 27 Sep 2024 11:31:39 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee4662d7837b680b2cf24f465f80bcef0300f1ec9bbb06e018c3978e371c90e`  
		Last Modified: Fri, 27 Sep 2024 11:32:30 GMT  
		Size: 20.8 MB (20842963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:615b9307c3c3e45c2cfbb1dd17c4ff6c4be3f73f822dd0da5db7f24a3821eae7`  
		Last Modified: Fri, 27 Sep 2024 11:32:24 GMT  
		Size: 437.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef1d934e341d81156439ae04b7ad4f0a24a93ed31030a9ca4125ebd8a4745c0d`  
		Last Modified: Fri, 27 Sep 2024 11:32:24 GMT  
		Size: 486.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561f13185c087a79fc530e0ed7eeb43c9b00ba108a72cbbf8d847e436496c928`  
		Last Modified: Fri, 27 Sep 2024 11:38:59 GMT  
		Size: 12.4 MB (12442433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9ee77d2867650f5d0ee395cf3eab6fc4d26bf5668c4c4e39fc8d829070e5c55`  
		Last Modified: Fri, 27 Sep 2024 11:38:56 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d93e05390b3f91a4033a82c8f3866f29637272b66a4f744e92fe1764a87ebbcc`  
		Last Modified: Fri, 27 Sep 2024 11:38:59 GMT  
		Size: 11.6 MB (11641448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b384193b4d1845259a0626f62d93e5f4aca43c4963dcf826fbc2ba5f9c9a0463`  
		Last Modified: Fri, 27 Sep 2024 11:38:56 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10fc2478faa41313a1772a12469ae15c448e29f5bd6ca8dbdd47903438603be0`  
		Last Modified: Fri, 27 Sep 2024 11:38:56 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:937f269e68890d4e8fe8aec1c6482b95a6b6a9e80f584a55bb88e200c7bff387`  
		Last Modified: Fri, 27 Sep 2024 11:38:56 GMT  
		Size: 891.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d016606bf24a39a82b7de45cd284cb804298c2f3e006fc5dc6e4739bd55b434b`  
		Last Modified: Fri, 27 Sep 2024 13:58:15 GMT  
		Size: 22.3 MB (22264808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a955d66cdd21003cd542a365b5e9c0be4557763bbb1be53ae0bd29fd024a1e84`  
		Last Modified: Fri, 27 Sep 2024 13:58:15 GMT  
		Size: 21.2 MB (21153718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7765894263a85284280bc36cf403771d1bb9aaaa5b913e7775cd8a1dda6c6577`  
		Last Modified: Fri, 27 Sep 2024 13:58:08 GMT  
		Size: 708.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1471412da8fb034604421b51f108e5f8f08cb2811dca4c058a40c0c1fe4213e0`  
		Last Modified: Fri, 27 Sep 2024 13:58:06 GMT  
		Size: 576.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13d504ea48a1fdc28fc3ee018e8b34447c5a059ec7795dfb130744e9b1f20205`  
		Last Modified: Fri, 27 Sep 2024 13:58:06 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e6c057922d795ad717974725e28e85bee3b853cd1d785fb0022011ba803316c`  
		Last Modified: Fri, 27 Sep 2024 14:00:38 GMT  
		Size: 221.4 MB (221378938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59d5ab7e2157ae482da57d0a485d155e602b02d0701bbf3985a5de3cfdc2d525`  
		Last Modified: Fri, 27 Sep 2024 13:59:59 GMT  
		Size: 3.9 KB (3880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e85a783010bc9d22052a8e4f072c4ad5d451c1597177749624c1339033ccd53`  
		Last Modified: Fri, 27 Sep 2024 13:59:59 GMT  
		Size: 2.4 KB (2371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:production` - linux; mips64le

```console
$ docker pull nextcloud@sha256:6c7775e36c73a2456456251911a318bdb6b466528e506b0d4bed116ed3752726
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.2 MB (414196540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be60ad8580d62c249b03024b8474e65545003284f36811c0974c3fb093d61128`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 04 Sep 2024 22:15:45 GMT
ADD file:9ffa4d53a074e91efecf5e26e3b67077f46165e0d042c1e6cf1b93c531ed2bc4 in / 
# Wed, 04 Sep 2024 22:15:50 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:23:54 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 04 Sep 2024 23:23:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 04 Sep 2024 23:25:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:25:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 04 Sep 2024 23:25:47 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 04 Sep 2024 23:43:16 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 04 Sep 2024 23:43:19 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 04 Sep 2024 23:44:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 04 Sep 2024 23:44:16 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 04 Sep 2024 23:44:22 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 04 Sep 2024 23:44:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Sep 2024 23:44:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Sep 2024 23:44:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 05 Sep 2024 01:57:04 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 26 Sep 2024 23:45:08 GMT
ENV PHP_VERSION=8.2.24
# Thu, 26 Sep 2024 23:45:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.24.tar.xz.asc
# Thu, 26 Sep 2024 23:45:16 GMT
ENV PHP_SHA256=80a5225746a9eb484475b312d4c626c63a88a037d8e56d214f30205e1ba1411a
# Thu, 26 Sep 2024 23:46:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 26 Sep 2024 23:46:04 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 27 Sep 2024 00:01:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 27 Sep 2024 00:01:11 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 27 Sep 2024 00:01:18 GMT
RUN docker-php-ext-enable sodium
# Fri, 27 Sep 2024 00:01:21 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 27 Sep 2024 00:01:25 GMT
STOPSIGNAL SIGWINCH
# Fri, 27 Sep 2024 00:01:28 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 27 Sep 2024 00:01:32 GMT
WORKDIR /var/www/html
# Fri, 27 Sep 2024 00:01:36 GMT
EXPOSE 80
# Fri, 27 Sep 2024 00:01:40 GMT
CMD ["apache2-foreground"]
# Fri, 27 Sep 2024 03:07:37 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Fri, 27 Sep 2024 03:07:42 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 27 Sep 2024 03:07:46 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 27 Sep 2024 03:19:26 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.23;     pecl install imagick-3.7.0;     pecl install memcached-3.2.0;     pecl install redis-6.0.2;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 03:19:33 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 27 Sep 2024 03:19:38 GMT
VOLUME [/var/www/html]
# Fri, 27 Sep 2024 03:19:45 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip
# Fri, 27 Sep 2024 03:19:49 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Fri, 27 Sep 2024 03:19:57 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits
# Fri, 27 Sep 2024 03:47:30 GMT
ENV NEXTCLOUD_VERSION=29.0.7
# Fri, 27 Sep 2024 03:51:26 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-29.0.7.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-29.0.7.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 03:51:39 GMT
COPY multi:f3c1a1c702869b782886f0f296503f363039f205d0235bcaa3e4e0fa8b0d1d39 in / 
# Fri, 27 Sep 2024 03:51:50 GMT
COPY multi:26b6011f3864a7a1d1a6de6eafef4f376d2e08f7f7b1ef21b94e6d2658564826 in /usr/src/nextcloud/config/ 
# Fri, 27 Sep 2024 03:51:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 27 Sep 2024 03:52:08 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:89502a0eae32ab684bc9df3d9922ee2874839b178a693286c4b866f5ca8e93f3`  
		Last Modified: Wed, 04 Sep 2024 22:24:11 GMT  
		Size: 29.1 MB (29125054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd61d7a0bd26fdefd1fc3f6685c32109220be495dcc46fe17919766e554de48`  
		Last Modified: Thu, 05 Sep 2024 03:51:29 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1187d9c88570478f80b55a3e07d23bb40e2db5e9069089775ddb5d5a54f4af4`  
		Last Modified: Thu, 05 Sep 2024 03:52:27 GMT  
		Size: 80.7 MB (80667470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b165b263f070f18c828e0e5ed25251a1e38f37f96ea4eb4a5727bbc912240e5`  
		Last Modified: Thu, 05 Sep 2024 03:51:29 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92cf2db0d07ff107e570d1ad64e608d226d0998d047f4b4dc832bce52d785789`  
		Last Modified: Thu, 05 Sep 2024 03:53:14 GMT  
		Size: 20.1 MB (20069958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd9315d8d0d2454284a0444c9ce8871c9375f6576538cae76de0a5e2515df52`  
		Last Modified: Thu, 05 Sep 2024 03:53:00 GMT  
		Size: 439.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3803187dbdba9cb9774d484104df9298d89b63ccc059c603dd1baa1e7b0656e3`  
		Last Modified: Thu, 05 Sep 2024 03:53:00 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e916fd25d3ad4efd6ef69c09efd7f8682b0e4209247c5e332776dcabe146dfcb`  
		Last Modified: Fri, 27 Sep 2024 01:43:40 GMT  
		Size: 12.2 MB (12236894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a77f591cc61facc73b79b4eac99f1eec5c13e711be200be105eae917fda913`  
		Last Modified: Fri, 27 Sep 2024 01:43:35 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25961e785ed6a2eccd35934cecb03a97227613d22dae8a80893926f7e77165e2`  
		Last Modified: Fri, 27 Sep 2024 01:43:43 GMT  
		Size: 10.6 MB (10645869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cfc301457aaccf860a733da22fb77ab9a35b18e8a090b6c3b20535d82610c87`  
		Last Modified: Fri, 27 Sep 2024 01:43:35 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f530e90fc5cd81f1c09d860208df03caa928cda8fff11a238b889c03baec053`  
		Last Modified: Fri, 27 Sep 2024 01:43:35 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3bbe2ea4383b656d8f76afb5aaf6a99bef85458993af18c2b00580c61106341`  
		Last Modified: Fri, 27 Sep 2024 01:43:35 GMT  
		Size: 897.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b972d59ff1eb3e8655f62f1058a21da25fbb8841f120c795dfd204415cd82c1d`  
		Last Modified: Fri, 27 Sep 2024 04:14:38 GMT  
		Size: 19.8 MB (19803066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b453844ff90d1e91149c1d5bd173d0261e4263fcb031cd1f7b3397aa6f7984b5`  
		Last Modified: Fri, 27 Sep 2024 04:14:46 GMT  
		Size: 20.5 MB (20488105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c41ca0cae651a8abb3d056f4fb621de0e82e99a2a6d30b4e3a3f7164a5b135b`  
		Last Modified: Fri, 27 Sep 2024 04:14:17 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b41541004a0ab7a3ee99acedc694134b4cfddb9ac95bdcc63abc464c835a5e4`  
		Last Modified: Fri, 27 Sep 2024 04:14:11 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd55e07613086004419d103b129c6d50022a3225d0b5e6218a1b34affac05541`  
		Last Modified: Fri, 27 Sep 2024 04:14:11 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ba5dcb7daf265cad1f0fc19adcb3228802431a5031497ba3bbed80eefe16998`  
		Last Modified: Fri, 27 Sep 2024 04:22:13 GMT  
		Size: 221.1 MB (221146687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90c3ebb6933c671e77c730d02b6d2b1c1273d5e21c3e44bf3b9109e3812f119b`  
		Last Modified: Fri, 27 Sep 2024 04:19:53 GMT  
		Size: 3.9 KB (3879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4776b457f9cb13088b2dc3e44dceff61b4016c4567580121816a3367fe6ce52`  
		Last Modified: Fri, 27 Sep 2024 04:19:53 GMT  
		Size: 2.4 KB (2371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:production` - linux; ppc64le

```console
$ docker pull nextcloud@sha256:cdb06c3c2e2a5fd0481aacb1ec2605d561613211d20a98f1f1aa5064464c4c5c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.1 MB (448102393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79104ec5fac79601a3db8f6ce76c80e9a633a956a3cd10b5f12ca04b32344e02`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 27 Sep 2024 05:33:07 GMT
ADD file:13ecda46acf717bc6e96c8ad429d6c14016514befca636a168655d0e5c9c4fbd in / 
# Fri, 27 Sep 2024 05:33:08 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 06:10:05 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 27 Sep 2024 06:10:05 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 27 Sep 2024 06:10:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 06:10:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 27 Sep 2024 06:10:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 27 Sep 2024 06:13:59 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 27 Sep 2024 06:14:00 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 27 Sep 2024 06:14:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 27 Sep 2024 06:14:16 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 27 Sep 2024 06:14:17 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 27 Sep 2024 06:14:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Sep 2024 06:14:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Sep 2024 06:14:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 27 Sep 2024 06:39:22 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 27 Sep 2024 06:39:22 GMT
ENV PHP_VERSION=8.2.24
# Fri, 27 Sep 2024 06:39:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.24.tar.xz.asc
# Fri, 27 Sep 2024 06:39:23 GMT
ENV PHP_SHA256=80a5225746a9eb484475b312d4c626c63a88a037d8e56d214f30205e1ba1411a
# Fri, 27 Sep 2024 06:39:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 27 Sep 2024 06:39:37 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 27 Sep 2024 06:42:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 27 Sep 2024 06:42:34 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 27 Sep 2024 06:42:35 GMT
RUN docker-php-ext-enable sodium
# Fri, 27 Sep 2024 06:42:35 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 27 Sep 2024 06:42:36 GMT
STOPSIGNAL SIGWINCH
# Fri, 27 Sep 2024 06:42:36 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 27 Sep 2024 06:42:36 GMT
WORKDIR /var/www/html
# Fri, 27 Sep 2024 06:42:36 GMT
EXPOSE 80
# Fri, 27 Sep 2024 06:42:37 GMT
CMD ["apache2-foreground"]
# Fri, 27 Sep 2024 08:46:15 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Fri, 27 Sep 2024 08:46:16 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 27 Sep 2024 08:46:16 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 27 Sep 2024 08:50:00 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.23;     pecl install imagick-3.7.0;     pecl install memcached-3.2.0;     pecl install redis-6.0.2;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 08:50:02 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 27 Sep 2024 08:50:02 GMT
VOLUME [/var/www/html]
# Fri, 27 Sep 2024 08:50:03 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip
# Fri, 27 Sep 2024 08:50:04 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Fri, 27 Sep 2024 08:50:04 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits
# Fri, 27 Sep 2024 08:56:37 GMT
ENV NEXTCLOUD_VERSION=29.0.7
# Fri, 27 Sep 2024 08:57:51 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-29.0.7.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-29.0.7.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 08:57:52 GMT
COPY multi:f3c1a1c702869b782886f0f296503f363039f205d0235bcaa3e4e0fa8b0d1d39 in / 
# Fri, 27 Sep 2024 08:57:53 GMT
COPY multi:26b6011f3864a7a1d1a6de6eafef4f376d2e08f7f7b1ef21b94e6d2658564826 in /usr/src/nextcloud/config/ 
# Fri, 27 Sep 2024 08:57:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 27 Sep 2024 08:57:53 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:c0db683897d16fe6e2869a351dbd5deac2268d5820d4b3c1cf93ec3bd69cafb5`  
		Last Modified: Fri, 27 Sep 2024 05:36:18 GMT  
		Size: 33.1 MB (33122163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bbb4ae861a643bc7004f9327fc7d89ac6f4ea4f5a77bfded69b88f585ea01e1`  
		Last Modified: Fri, 27 Sep 2024 07:02:41 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc16434a3ca8eec5c8933adec752fafcba89db0a65fc61746120478da09bca93`  
		Last Modified: Fri, 27 Sep 2024 07:02:58 GMT  
		Size: 103.3 MB (103326181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2051474fc72a079e1611119dde76deefb71f3b4b15e86c02c8e21198bcb9f249`  
		Last Modified: Fri, 27 Sep 2024 07:02:41 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9589061db86204e594c406f6de20b8e8bc40c3bc4fbdff0ddcaf22b3253078`  
		Last Modified: Fri, 27 Sep 2024 07:03:25 GMT  
		Size: 21.5 MB (21511855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5201482f538d84823d22ea42aeaa4b071c48bc6693b7862c0a79bf390d689b6`  
		Last Modified: Fri, 27 Sep 2024 07:03:21 GMT  
		Size: 433.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2843dcc1fb30cdbf957b3c7273818bd5877c32b4dc91f2273111780f4eaae30b`  
		Last Modified: Fri, 27 Sep 2024 07:03:21 GMT  
		Size: 486.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d813628e013d7663e39adf1ebd1323cdd11b3c58a30a372f18d8eee63ed9e11`  
		Last Modified: Fri, 27 Sep 2024 07:07:19 GMT  
		Size: 12.4 MB (12442624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da6ae47d185ea74c696277a67f5e63bb39534b357e65564077b76db6d1c07371`  
		Last Modified: Fri, 27 Sep 2024 07:07:15 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9316162bc4d4f6a7fed0124b136ecd79bf288a5cd93f3fc82154167d7ffa5ff`  
		Last Modified: Fri, 27 Sep 2024 07:07:18 GMT  
		Size: 11.8 MB (11827343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97c5532898e7467372ef63509025ac2d7c86a310cb1c996b9679b4eef402dd83`  
		Last Modified: Fri, 27 Sep 2024 07:07:15 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f778f01f7fc101b62e9cb120708767d6e085b5958447266e42fd647972d90ce`  
		Last Modified: Fri, 27 Sep 2024 07:07:15 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beac6a6fe43d79c33a4bc98ab536ac2aa2ae7ac0f0dde11522778062b2252340`  
		Last Modified: Fri, 27 Sep 2024 07:07:15 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7c593f1c8580f3cb4985a47292d5e7b293425de7fea9d08ad2b592f89e26554`  
		Last Modified: Fri, 27 Sep 2024 09:02:51 GMT  
		Size: 22.6 MB (22624734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e4211dac9f3bcfd319d86ad48e838b33b91349388cf6c935b6867391f5b4e6`  
		Last Modified: Fri, 27 Sep 2024 09:02:51 GMT  
		Size: 21.9 MB (21853695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ead36215764679f375f05151a236a5e5f46ca5748e2d616debab3775fee9eb`  
		Last Modified: Fri, 27 Sep 2024 09:02:47 GMT  
		Size: 714.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:597492488187fde1e223b1ad27b2c095cd4effadb0be225abee64bb540138303`  
		Last Modified: Fri, 27 Sep 2024 09:02:45 GMT  
		Size: 576.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31f6ee4c48cbb04151bf64d5b2cc6f8d07c706445d590da6b839f0d0171f4fc3`  
		Last Modified: Fri, 27 Sep 2024 09:02:45 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2434c011e5156504be25941e5bc267fa04d701ef9337d97c79dc1c92479bd0d0`  
		Last Modified: Fri, 27 Sep 2024 09:04:44 GMT  
		Size: 221.4 MB (221380400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34aae0a053ba6bd7af4308aa642a476598f747f7b121d6e861fa3fce70f63249`  
		Last Modified: Fri, 27 Sep 2024 09:04:14 GMT  
		Size: 3.9 KB (3880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa1b6921e3a27b7d458b64ff49991a70912ac81ea65a2da271a6b45707bb568b`  
		Last Modified: Fri, 27 Sep 2024 09:04:14 GMT  
		Size: 2.4 KB (2372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nextcloud:production` - linux; s390x

```console
$ docker pull nextcloud@sha256:23f1965c929bf9764e87ccc9e245e04e7ca075e01d80d16441c9fa3fdf54d55a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **412.3 MB (412335521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf2d578dc76e60fdf5312f24a4f87279a77b6f85476b061a252a7db8ed8a8ad1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 27 Sep 2024 02:43:25 GMT
ADD file:ee3c94adee604dbcaddf5d6c372b1f325a4443f66bd717dedf1ff7d9fb1ba116 in / 
# Fri, 27 Sep 2024 02:43:26 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 03:23:32 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 27 Sep 2024 03:23:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 27 Sep 2024 03:23:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 03:23:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 27 Sep 2024 03:23:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 27 Sep 2024 03:26:58 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 27 Sep 2024 03:26:58 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 27 Sep 2024 03:27:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 27 Sep 2024 03:27:06 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 27 Sep 2024 03:27:06 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 27 Sep 2024 03:27:06 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Sep 2024 03:27:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Sep 2024 03:27:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 27 Sep 2024 03:53:41 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 27 Sep 2024 03:53:41 GMT
ENV PHP_VERSION=8.2.24
# Fri, 27 Sep 2024 03:53:42 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.24.tar.xz.asc
# Fri, 27 Sep 2024 03:53:42 GMT
ENV PHP_SHA256=80a5225746a9eb484475b312d4c626c63a88a037d8e56d214f30205e1ba1411a
# Fri, 27 Sep 2024 03:53:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 27 Sep 2024 03:53:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 27 Sep 2024 03:56:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 27 Sep 2024 03:56:20 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 27 Sep 2024 03:56:21 GMT
RUN docker-php-ext-enable sodium
# Fri, 27 Sep 2024 03:56:21 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 27 Sep 2024 03:56:21 GMT
STOPSIGNAL SIGWINCH
# Fri, 27 Sep 2024 03:56:21 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 27 Sep 2024 03:56:21 GMT
WORKDIR /var/www/html
# Fri, 27 Sep 2024 03:56:21 GMT
EXPOSE 80
# Fri, 27 Sep 2024 03:56:22 GMT
CMD ["apache2-foreground"]
# Fri, 27 Sep 2024 05:34:58 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         busybox-static         bzip2         libldap-common         libmagickcore-6.q16-6-extra         rsync     ;     rm -rf /var/lib/apt/lists/*;         mkdir -p /var/spool/cron/crontabs;     echo '*/5 * * * * php -f /var/www/html/cron.php' > /var/spool/cron/crontabs/www-data
# Fri, 27 Sep 2024 05:34:59 GMT
ENV PHP_MEMORY_LIMIT=512M
# Fri, 27 Sep 2024 05:34:59 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Fri, 27 Sep 2024 05:36:47 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         libcurl4-openssl-dev         libevent-dev         libfreetype6-dev         libgmp-dev         libicu-dev         libjpeg-dev         libldap2-dev         libmagickwand-dev         libmcrypt-dev         libmemcached-dev         libpng-dev         libpq-dev         libwebp-dev         libxml2-dev         libzip-dev     ;         debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";     docker-php-ext-configure ftp --with-openssl-dir=/usr;     docker-php-ext-configure gd --with-freetype --with-jpeg --with-webp;     docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch";     docker-php-ext-install -j "$(nproc)"         bcmath         exif         ftp         gd         gmp         intl         ldap         opcache         pcntl         pdo_mysql         pdo_pgsql         sysvsem         zip     ;         pecl install APCu-5.1.23;     pecl install imagick-3.7.0;     pecl install memcached-3.2.0;     pecl install redis-6.0.2;         docker-php-ext-enable         apcu         imagick         memcached         redis     ;     rm -r /tmp/pear;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }'         | sort -u         | xargs -r dpkg-query --search         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:36:48 GMT
RUN {         echo 'opcache.enable=1';         echo 'opcache.interned_strings_buffer=32';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidate_freq=60';         echo 'opcache.jit=1255';         echo 'opcache.jit_buffer_size=128M';     } > "${PHP_INI_DIR}/conf.d/opcache-recommended.ini";         echo 'apc.enable_cli=1' >> "${PHP_INI_DIR}/conf.d/docker-php-ext-apcu.ini";         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > "${PHP_INI_DIR}/conf.d/nextcloud.ini";         mkdir /var/www/data;     mkdir -p /docker-entrypoint-hooks.d/pre-installation              /docker-entrypoint-hooks.d/post-installation              /docker-entrypoint-hooks.d/pre-upgrade              /docker-entrypoint-hooks.d/post-upgrade              /docker-entrypoint-hooks.d/before-starting;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 27 Sep 2024 05:36:48 GMT
VOLUME [/var/www/html]
# Fri, 27 Sep 2024 05:36:49 GMT
RUN a2enmod headers rewrite remoteip ;     {      echo 'RemoteIPHeader X-Real-IP';      echo 'RemoteIPInternalProxy 10.0.0.0/8';      echo 'RemoteIPInternalProxy 172.16.0.0/12';      echo 'RemoteIPInternalProxy 192.168.0.0/16';     } > /etc/apache2/conf-available/remoteip.conf;     a2enconf remoteip
# Fri, 27 Sep 2024 05:36:49 GMT
ENV APACHE_BODY_LIMIT=1073741824
# Fri, 27 Sep 2024 05:36:49 GMT
RUN {      echo 'LimitRequestBody ${APACHE_BODY_LIMIT}';     } > /etc/apache2/conf-available/apache-limits.conf;     a2enconf apache-limits
# Fri, 27 Sep 2024 05:41:02 GMT
ENV NEXTCLOUD_VERSION=29.0.7
# Fri, 27 Sep 2024 05:41:43 GMT
RUN set -ex;     fetchDeps="         gnupg         dirmngr     ";     apt-get update;     apt-get install -y --no-install-recommends $fetchDeps;         curl -fsSL -o nextcloud.tar.bz2 "https://download.nextcloud.com/server/releases/nextcloud-29.0.7.tar.bz2";     curl -fsSL -o nextcloud.tar.bz2.asc "https://download.nextcloud.com/server/releases/nextcloud-29.0.7.tar.bz2.asc";     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 28806A878AE423A28372792ED75899B9A724937A;     gpg --batch --verify nextcloud.tar.bz2.asc nextcloud.tar.bz2;     tar -xjf nextcloud.tar.bz2 -C /usr/src/;     gpgconf --kill all;     rm nextcloud.tar.bz2.asc nextcloud.tar.bz2;     rm -rf "$GNUPGHOME" /usr/src/nextcloud/updater;     mkdir -p /usr/src/nextcloud/data;     mkdir -p /usr/src/nextcloud/custom_apps;     chmod +x /usr/src/nextcloud/occ;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:41:51 GMT
COPY multi:f3c1a1c702869b782886f0f296503f363039f205d0235bcaa3e4e0fa8b0d1d39 in / 
# Fri, 27 Sep 2024 05:41:52 GMT
COPY multi:26b6011f3864a7a1d1a6de6eafef4f376d2e08f7f7b1ef21b94e6d2658564826 in /usr/src/nextcloud/config/ 
# Fri, 27 Sep 2024 05:41:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 27 Sep 2024 05:41:52 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:eca1e192de25fb56826ff7ed14b2e1532a49c27a08147a6249506eafd8ab4472`  
		Last Modified: Fri, 27 Sep 2024 02:47:22 GMT  
		Size: 27.5 MB (27490024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:263aaad988f988011e1356f427631505912e90651f05e9b8127e438710e3424d`  
		Last Modified: Fri, 27 Sep 2024 04:18:13 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fe6bbb4a2c701c2e428aa64af29de71f25f3955f023abedbd742ba882d648c4`  
		Last Modified: Fri, 27 Sep 2024 04:18:25 GMT  
		Size: 80.8 MB (80817788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d56dc43f4c20142326de61889c1d809b383f6aee30517f4872c80305147c993`  
		Last Modified: Fri, 27 Sep 2024 04:18:13 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c52c41590c8426047a15f1969a92ae4add1c9047e56460d92a094cd534bd822`  
		Last Modified: Fri, 27 Sep 2024 04:18:41 GMT  
		Size: 20.1 MB (20099019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0050a91c477b0c2256727ec363cb8333b14cd8993f235bf2e788825fea5ba66`  
		Last Modified: Fri, 27 Sep 2024 04:18:38 GMT  
		Size: 434.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baed063e13cf0353d5655d6198ed7df04fdaeb730279a099f051e683ada2311f`  
		Last Modified: Fri, 27 Sep 2024 04:18:38 GMT  
		Size: 486.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:245b009057a3c847137ba2e2e4012150b891e8db01823a6edd44f831a8a18f65`  
		Last Modified: Fri, 27 Sep 2024 04:21:15 GMT  
		Size: 12.4 MB (12441770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2844dd1ced33ed2075394f94731f7aa0ad263e992bf7dbc0a3f643c2ec4a6fd`  
		Last Modified: Fri, 27 Sep 2024 04:21:13 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f8158b01ff9b6e0fa7aa2f1ee7ac08c7a452b62cca10a417fdc051510b9666e`  
		Last Modified: Fri, 27 Sep 2024 04:21:15 GMT  
		Size: 10.6 MB (10644674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c7a4c8366b9700dbadc776b31d7362bdb4017c6222d6c9a76f35fe9e801f07d`  
		Last Modified: Fri, 27 Sep 2024 04:21:13 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b8725b76676d868f065476a88cc34d82a84d3ca056bb80bb4f82da322142976`  
		Last Modified: Fri, 27 Sep 2024 04:21:13 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9849ccdf4f53873810b66a3d5b59d4b773a8a3a2f21b83ca53235f17ef6c4276`  
		Last Modified: Fri, 27 Sep 2024 04:21:13 GMT  
		Size: 891.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ef87f8349189029c6ebdea10b348c452e62fdf11756fe3647142e85b610b112`  
		Last Modified: Fri, 27 Sep 2024 05:46:14 GMT  
		Size: 19.3 MB (19299006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b76c7013ddf1e12324614bfb1f5fd7bf7980d0737cbf9b20ad48a6efebcbd08f`  
		Last Modified: Fri, 27 Sep 2024 05:46:14 GMT  
		Size: 20.2 MB (20152516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b7b4e5a4e1e9c0c2bc90fde3691f5a95337f7e1bb05167f8fc7d64161f53d5`  
		Last Modified: Fri, 27 Sep 2024 05:46:11 GMT  
		Size: 708.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5898c51241ca0454271f4e3339453506c2a2030638862aefe68bf3aaa2409382`  
		Last Modified: Fri, 27 Sep 2024 05:46:10 GMT  
		Size: 572.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942a68f1c85760b66b51457b0eac4c53756ebd3ca593d5ff8b17741558d6c16a`  
		Last Modified: Fri, 27 Sep 2024 05:46:10 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8f064e5253b76e3d080867d302c3f0534a6d91c946364ff0cc8d2f9c2b525c`  
		Last Modified: Fri, 27 Sep 2024 05:47:40 GMT  
		Size: 221.4 MB (221377347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b3a99781d8ada5d6369bb3171b78f2274f62a3e9358ec5c4f25ad094050ff7`  
		Last Modified: Fri, 27 Sep 2024 05:47:15 GMT  
		Size: 3.9 KB (3881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3b59dcf7b80e53dedc416b245cf522adba83501045726c304beee308e1c501d`  
		Last Modified: Fri, 27 Sep 2024 05:47:15 GMT  
		Size: 2.4 KB (2370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
